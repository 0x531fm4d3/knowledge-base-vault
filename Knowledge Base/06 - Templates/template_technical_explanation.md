---
created: 2024-12-22T08:34
updated: 2025-05-15T08:07
term_value: <% tp.file.title %>
type: technical_explanation
origin_value: <%* const files = app.vault.getFiles().filter(f => f.path.startsWith('01 - Origins/') || f.path.startsWith('04 - Systems/')).map(f => f.basename), selectedFile = await tp.system.suggester(['Please choose the origin\'s value', ...files], ['', ...files]); tR += selectedFile || 'No selection'; %>
aliases:
  - <% tp.file.title.replace(/^.*_\d{4}-\d{2}-\d{2} - /, '') %>
maturity: baby
cssclasses:
  - dv-equal-columns
---
# Categories



# Objective




# Tooling




# Steps




# Notes




# Relevant Links

