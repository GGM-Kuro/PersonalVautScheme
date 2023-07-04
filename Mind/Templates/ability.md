---
tags: ability
<%*  let title = await tp.system.prompt("Ability:");
while (await tp.file.find_tfile("/Knowledge/Abilities/" + title)){
title = await tp.system.prompt("Already exist, insert new ability:")
};
await tp.file.move("/Knowledge/Abilities/" + title)
-%>
---

## Util links / References
**Alt + L to add link**

---
<% tp.file.cursor(0) %>

---

```dataview
TABLE without id
practice + "| " + file.link AS "Days you have practiced"
FROM "Journal/Daily" AND #Daily 
WHERE ability = this.file.name
```
