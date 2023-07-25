---
date: <% tp.date.now() %>
week: <% moment(tp.file.title).format("gggg-[W]ww")%>
read: <%  await tp.system.prompt("How much will you read today?", "0")%>
stream: <%  await tp.system.prompt("How much will you stream today?", "0")%>
activity: <% await tp.system.suggester(['✅','❌'], ['✅','❌'],true,'Activity day?') %>
breackfast: <% await tp.system.suggester(['✅','❌'], ['✅','❌'],true,'Breackfast day?') %>
study: <% await tp.system.suggester(['✅','❌'], ['✅','❌'],true,'Study day?') %>
train: <% await tp.system.suggester(['✅','❌'], ['✅','❌'],true,'Gym day?') %>
mood: <% await tp.system.suggester(['😁','😣','😒'], ['😁','😣','😒'],true,'how was the day?') %>
english: <% await tp.system.suggester(['✅','❌'], ['✅','❌'],true,'English day?') %>
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

---
# Notes
```dataview
TABLE without id
"[" + title + "]" + "(" + file.name + ")"  AS Notes, 
"[[" + theme + "]]"  AS Theme,
file.frontmatter.date as date 

FROM #note 
where file.frontmatter.date = this.file.name
```

---
# Tasks **<span style="font-size: 20px;">Alt + T to add task</span>**
### **Earings**
```tasks
not done
due <% tp.file.title %>
```

### **Completed**
```tasks
due <% tp.file.title %>
done
```















