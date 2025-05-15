---
created: 2024-12-22T08:34
updated: 2025-04-22T13:00
term_value: <% tp.file.title %>
type: technical_explanation
origin_value: <%* const files = app.vault.getFiles().filter(f => f.path.startsWith('01 - Origins/') || f.path.startsWith('04 - Systems/')).map(f => f.basename), selectedFile = await tp.system.suggester(['Please choose the origin\'s value', ...files], ['', ...files]); tR += selectedFile || 'No selection'; %>
category: <% tp.system.suggester(["Windows internals","Malware Analysis","Malware Development","Object oriented programming","C language"],["windows_internals","malware_analysis","malware_development","object oriented programming","c_language"],throw_on_cancel=false, placeholder="Technical explanation category?")%>
aliases:
  - <% tp.file.title.replace(/^.*_\d{4}-\d{2}-\d{2} - /, '') %>
cssclasses:
  - dv-equal-columns
status: in progress
maturity: baby
---
# Objective




# Tooling




# Steps




# Notes




# Linked concepts




# Relevant Links

