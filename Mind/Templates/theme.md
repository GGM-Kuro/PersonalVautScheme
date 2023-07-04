---
theme: <%* let title = await tp.system.prompt("Theme:");
while (tp.file.find_tfile("/Knowledge/Themes/" + title)){
title = await tp.system.prompt("Already exist, insert new name:")};
await tp.file.move("/Knowledge/Themes/" + title)
tR += title; %>
tag: theme
---


`="![progress](https://progress-bar.dev/" + round(length(filter(this.file.tasks.completed, (t) => t = true)) / length(this.file.tasks.text) * 100) + "/?title=progress)"`


## Description
<% tp.system.prompt("Describe theme", "#TODO", false, true) %>

---

## Sections

- [ ] <% tp.file.cursor(2) %>Add sections... #TODO
	- [ ] add subsections... #TODO 

---
```dataview
TABLE without id
"[" + title + "]" + "(" + file.name + ")" as Concepts

FROM ([[<% title %>]]) AND #concept 
```

---
```dataview
TABLE without id
"[" + title + "]" + "(" + file.name + ")" as Notes, 
date


FROM ([[<% title %>]]) AND #note
```
