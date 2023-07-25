---
tag: project
project: <%* let project = await tp.system.prompt("Project Name:");
while (tp.file.find_tfile("Projects/" + project)){
project = await tp.system.prompt("Already exist, insert new name:")};
project = project.split(" ").join("_");
await tp.file.move("Projects/" + project )
tR += project; 
let title= await project.split("_").join(" ");
%>
title: "<% title %>" 
---


# Tasks
### Earring
```tasks
not done
filename includes .tsk<% project.split("_").map(p => p.charAt(0).toUpperCase() + p.slice(1) ).join("")%>
```

### Completed
```tasks
done
filename includes .tsk<% project.split("_").map(p => p.charAt(0).toUpperCase() + p.slice(1) ).join("")%>
```

---
```dataview
TABLE without id
"[" + title + "]" + "(" + file.name + ")" as Notes, 
date


FROM #note  where (file.frontmatter.theme = this.file.frontmatter.title)
```
