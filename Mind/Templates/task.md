---
tags: task
project: <%* let project = (await tp.system.suggester((item) => item.basename, app.vault.getFiles().filter(file => file.path.includes("Projects/") &&  !file.path.includes("Tasks") && !file.path.includes("Knowledge")), false, 'Choice Project')).basename;
tR += `"${project.split("_").join(" ")}"`;
%>
title: <%*let title = await tp.system.prompt("Title task:");
let joinTitle = title.split(" ").join("_");
project = project.split("_").map(p => p.charAt(0).toUpperCase() + p.slice(1) ).join("");
await tp.file.move("Tasks/ProjectsTasks/" + joinTitle +".tsk" + project);
tR += title;
%>
---

# <% title %>

# Tasks Steps
- [ ]   


--- 
