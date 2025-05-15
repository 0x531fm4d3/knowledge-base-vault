---
created: 2024-12-22T08:34
updated: 2025-05-15T08:08
term_value: <% tp.file.title %>
type: term
origin_value: <%* const files = app.vault.getFiles().filter(f => ['01 - Origins', '04 - Systems'].some(folder => f.path.startsWith(folder + '/'))).map(f => f.basename), selectedFile = await tp.system.suggester(['Please choose the origin\'s value', ...files], ['', ...files]); tR += selectedFile || 'No selection'; %>
cssclasses:
  - dv-equal-columns
aliases:
  - <% tp.file.title.replace(/^.*_\d{4}-\d{2}-\d{2} - /, '') %>
maturity: baby
---

# Categories


# Summary




# Detailed Description




# Structure




# Contextual Use




# Related Terms




# Relevant Links