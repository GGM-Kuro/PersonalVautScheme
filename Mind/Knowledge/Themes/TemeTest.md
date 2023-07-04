---
theme: TemeTest
---


`="![progress](https://progress-bar.dev/" + round(length(filter(this.file.tasks.completed, (t) => t = true)) / length(this.file.tasks.text) * 100) + "/?title=progress)"`


## Description
#TODO

---

## Sections

- [ ] Add sections... #TODO
	- [ ] add subsections... #TODO 

---
```dataview
TABLE without id
"[" + title + "]" + "(" + file.name + ")" as Concepts

FROM ([[TemeTest]]) AND #concept 
```

---
```dataview
TABLE without id
"[" + topics + "]" + "(" + file.name + ")" as Notes, 
date


FROM ([[TemeTest]]) AND #note
```
