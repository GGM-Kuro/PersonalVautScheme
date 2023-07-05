---
<%*let title = await tp.system.prompt("Concept:");
while (tp.file.find_tfile("/Knowledge/Concept/" + title)){
title = await tp.system.prompt("Already exist, insert new name:")
};
let theme = (await tp.system.suggester((item) => item.basename, app.vault.getFiles().filter(file => file.path.includes("Knowledge/Themes")), false, 'Choice Theme')).basename;
tR += "title: " + title + "\ntheme: " + theme;
await tp.file.move("/Knowledge/Concepts/" + theme + '_' + title);
%>

tags: knowledge concept <% tp.file.cursor(0) %>
---


# <% title %>
<% tp.file.cursor(1) %>



---
[[<% theme %>]]