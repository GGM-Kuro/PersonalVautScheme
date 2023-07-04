---
date: <% tp.date.now() %>
week: <% moment(tp.file.title).format("gggg-[W]ww")%>
bike: <%  await tp.system.prompt("How long on the bike today?", "0")%>
train: <% await tp.system.suggester(['✅','❌'], ['✅','❌'],true,'Gym day?') %>
mood: <% await tp.system.suggester(['😁','😣','😒'], ['😁','😣','😒'],true,'how was the day?') %>
englishClass: <% await tp.system.suggester(['✅','❌'], ['✅','❌'],true,'English day?') %>
practice: <% await tp.system.suggester(['✅','❌'], ['✅','❌'],true,'Practice day?') %>
ability: <%* let theme = app.vault.getFiles().filter(file => file.path.includes("Knowledge/Abilities/")); 
let random =Math.floor(Math.random() * theme.length );
theme = theme[random].basename;
tR += theme;%>
tags: Daily 
---

[[Journal/Daily/<%tp.date.now("YYYY-MM-DD",-1,tp.file.title,"YYYY-MM-DD")%>|Yesterday]] <-> [[Journal/Daily/<%tp.date.now("YYYY-MM-DD",1,tp.file.title,"YYYY-MM-DD")%>|Tomorrow]]
Week Summary: [[<% moment(tp.file.title).format("gggg-[W]ww")%>]]
Today have to practice: [[<% theme %>]] 


# Journal
<% tp.file.cursor(0) %>

# Tasks
**Alt + T to add task**


# Notes
```dataview
TABLE without id
"[" + topics + "]" + "(" + file.name + ")"  AS Notes, 
theme AS Theme,
file.frontmatter.date 

FROM #note 
where file.frontmatter.date = this.file.name
```
















