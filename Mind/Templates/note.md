---
theme: <%* 
let choice = await tp.system.suggester(["Theme","Book","Project"],["Themes","Books","Projects"],true,"Choice note type");
let theme
if (choice == "Projects"){
 theme = (await tp.system.suggester((item) => item.basename, app.vault.getFiles().filter(file => file.path.includes(choice + "/") &&  !file.path.includes("Tasks") && !file.path.includes("Knowledge")), false, 'Choice ' + choice)).basename;
} else {
 theme = (await tp.system.suggester((item) => item.basename, app.vault.getFiles().filter(file => file.path.includes("Knowledge/"+ choice + "/")), false, 'Choice ' + choice)).basename;
}
tR += theme;

let tempTitle = await theme + '_' + tp.date.now("YYYY-MM-DD_HH-mm");

await tp.file.move('Knowledge/Notes/' + tempTitle);

%>
date: <% tp.file.creation_date("YYYY-MM-DD") %>
week: <% moment(tp.date.now()).format("gggg-[W]ww") %>
tags: knowledge note
title: <%* let title = await tp.system.prompt("Title",theme + "_note", true);
tR += title %>
---

# <% title %>
<% tp.file.cursor(0) %>



---
#[[<% theme %>]]



