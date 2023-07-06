---
date: <% tp.file.title %>
week: <% moment(tp.file.title).format("gggg-[W]ww")%>
mood: <% await tp.system.suggester(['😁','😣','😒'], ['😁','😣','😒'],true,'how was the day?') %>
bike: <%  await tp.system.prompt("How long are you going to ride a bike today??", "0")%>
gym: <% await tp.system.suggester(['✅','❌'], ['✅','❌'],true,'Today you go to the gym?') %>
englishClass: <% await tp.system.suggester(['✅','❌'], ['✅','❌'],true,'Today you have english class?') %>
practice: <% await tp.system.suggester(['✅','❌'], ['✅','❌'],true,'Today you are going to practice?') %>
ability: <%* let ability = app.vault.getFiles().filter(file => file.path.includes("Knowledge/Abilities/")); 
let random =Math.floor(Math.random() * ability.length );
ability = ability[random].basename;
tR += ability;%>
tags: daily 
---

[[Journal/Daily/<%tp.date.now("YYYY-MM-DD",-1,tp.file.title,"YYYY-MM-DD")%>|Yesterday]] <-> [[Journal/Daily/<%tp.date.now("YYYY-MM-DD",1,tp.file.title,"YYYY-MM-DD")%>|Tomorrow]]
Week Summary: [[<% moment(tp.file.title).format("gggg-[W]ww")%>]]
Today have to practice: [[<% ability %>]] 


# Journal
<% tp.file.cursor(0) %>

---
# Tasks **<span style="font-size: 20px;">Alt + T to add task</span>**
### **Earrings**
```tasks
not done
due <% tp.file.title %>
```

### **Completed**
```tasks
due <% tp.file.title %>
done
```
---

# Notes
```dataview
TABLE without id
"[" + title + "]" + "(" + file.name + ")"  AS Notes, 
theme AS Theme,
file.frontmatter.date 

FROM #note 
where file.frontmatter.date = this.file.name
```
















