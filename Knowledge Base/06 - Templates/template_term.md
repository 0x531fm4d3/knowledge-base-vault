---
created: 2024-12-22T08:34
updated: 2025-05-06T08:39
term_value: <% tp.file.title %>
type: term
origin_value: <%* const files = app.vault.getFiles().filter(f => ['01 - Origins', '04 - Systems'].some(folder => f.path.startsWith(folder + '/'))).map(f => f.basename), selectedFile = await tp.system.suggester(['Please choose the origin\'s value', ...files], ['', ...files]); tR += selectedFile || 'No selection'; %>
category: <% tp.system.suggester(["Windows internals","Malware Analysis","Malware Development","Object oriented programming","AI"],["windows_internals","malware_analysis","malware_development","object oriented programming","ai"],throw_on_cancel=false, placeholder="Term category?")%>
cssclasses:
  - dv-equal-columns
aliases:
  - <% tp.file.title.replace(/^.*_\d{4}-\d{2}-\d{2} - /, '') %>
status: in progress
maturity: baby
---

# Summary




# Detailed Description




# Structure




# Contextual Use




# Related Terms




# Relevant Links