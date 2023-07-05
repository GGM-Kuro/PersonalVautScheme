---
tags: task
project: <%* let project =(await tp.system.suggester((item) => item.basename, app.vault.getFiles().filter(file => file.path.includes("Projects/")), false, 'Choice Project')).basename;
tR += project;
%>
title: <%*let title = await tp.system.prompt("Title task:");
await tp.file.move("Tasks/ProjectsTasks/" + project + "_"+ title);
tR += title;
%>
---

# Tasks Steps
- [ ]   

--- 
