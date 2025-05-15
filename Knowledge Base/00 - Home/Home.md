---
created: 2024-12-23T09:42
updated: 2025-05-15T07:39
---

# Topics to add


| Name | Link to resource |
| ---- | ---------------- |
|      |                  |

# Tasks
```tasks
```


# Origins to second level links table

```dataviewjs
const origins = dv.pages().where(p => p.type === "origin" && !p.file.path.includes("06 - Templates"));

let rows = [];

origins.forEach(origin => {
    const originLinks = Array.from(origin.file.outlinks || [])
        .filter(link => link !== origin.file.link) // Remove self-links
        .filter(link => !link.path.endsWith(".pdf")) // Exclude .pdf files
        .filter((link, index, self) => self.indexOf(link) === index); // Ensure uniqueness

    // Helper function to create a clickable Markdown link with just the note name
    const makeLink = path => {
        const fileName = path.split("/").pop().replace(".md", ""); // Extract file name without extension
        return `[[${fileName}]]`; // Dataview uses [[ ]] to create clickable links
    };
    originLinks.forEach(link => {
        // Extract second-level links (links from the notes linked by the origin), excluding .pdf links
        const linkedPage = dv.page(link.path);
        const secondLevelLinks = linkedPage
            ? Array.from(linkedPage.file.outlinks || [])
                .filter(link => link !== origin.file.link && !originLinks.includes(link)) // Remove duplicates and self-links
                .filter(link => !link.path.endsWith(".pdf"))
                .filter(link => !link.path.endsWith(".png"))
                .filter((link, index, self) => self.indexOf(link) === index) 
            : [];

        const secondLinksFormatted = secondLevelLinks.map(l => makeLink(l.path)).join("\n");

        rows.push([
            originLinks.indexOf(link) === 0 ? makeLink(origin.file.path) : "",
            makeLink(link.path), 
            secondLinksFormatted 
        ]);
    });
});

// Step 3: Render the table with grouped links
dv.table(["Origins", "Direct Links", "Second-Level Links"], rows);

```

