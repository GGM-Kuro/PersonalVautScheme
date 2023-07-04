---
tags: task
title: <%*let title = await tp.system.prompt("Title task:");
await tp.file.move("/Knowledge/Tasks/" + title);
tR += title;
%>
---

# Task Steps
- [ ]  <% tp.file.cursor(0) %> 


--- 
