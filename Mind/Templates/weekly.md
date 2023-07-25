---
readGoal: <% await tp.system.prompt(" How long will you read this week?", "0") %>
streamGoal: <% await tp.system.prompt(" How long will you stream this week?", "0") %>
---
[[README]] || [[`To-Do|To-do Kanban ]] || [[Library.canvas|Library]]
[[Journal/Weekly/<% moment(tp.file.title).subtract(1,'week').format("gggg-[W]ww") %>|↶ Previous Week]] | [[Journal/Weekly/<% moment(tp.file.title).add(1,'week').format("gggg-[W]ww") %>|↷ Next Week]] 

# <% moment(tp.file.title).startOf('isoWeek').format("MMM DD") %> - <% moment(tp.file.title).endOf('isoWeek').format("MMM DD") %>

# Days
```dataview
List From "Journal/Daily"
Where file.name = date(today)
```
-[[Journal/Daily/<% moment(tp.file.title).startOf('isoWeek').add(0,'day').format("YYYY-MM-DD") %>|Monday]]
-[[Journal/Daily/<% moment(tp.file.title).startOf('isoWeek').add(1,'day').format("YYYY-MM-DD") %>|Tuesday]]
-[[Journal/Daily/<% moment(tp.file.title).startOf('isoWeek').add(2,'day').format("YYYY-MM-DD") %>|Wednesday]]
-[[Journal/Daily/<% moment(tp.file.title).startOf('isoWeek').add(3,'day').format("YYYY-MM-DD") %>|Thursday]]
-[[Journal/Daily/<% moment(tp.file.title).startOf('isoWeek').add(4,'day').format("YYYY-MM-DD") %>|Friday]]
-[[Journal/Daily/<% moment(tp.file.title).startOf('isoWeek').add(5,'day').format("YYYY-MM-DD") %>|Saturday]]
-[[Journal/Daily/<% moment(tp.file.title).startOf('isoWeek').add(6,'day').format("YYYY-MM-DD") %>|Sunday]]

---
# Daily
```dataview
TABLE without ID
	file.link AS Day,
	mood as "😶‍🌫️",
	activity as "🚶‍♂️",
	train AS "🏋️‍♂️",
	read AS "📖",
	stream AS "🎥🐵",
    practice + "| "  + "[[" + ability + "]]" AS " 📃 ✏️",
	english  AS "🗽",
	breackfast As "🥞"
FROM "Journal/Daily"
WHERE week = "<% moment(tp.file.title).format("gggg-[W]ww")%>"
SORT file.name ASC
```
---
# Notes
```dataview
TABLE without id

"[" + title + "]" + "(" + file.name + ")" as Notes,
"[[" + theme + "]]" as Theme,
date

FROM #note
WHERE week = "<% moment(tp.file.title).format("gggg-[W]ww")%>"
```
---
# Goals
```dataview
List without id
"## 📖Read "+" ![test](https://progress-bar.dev/" + round(sum(rows.read)/this.file.frontmatter.readGoal*100) + "/?title=progress&width=70)" +"
⏱️__**Hours:**__ **" + sum(rows.read)+ "/" +this.file.frontmatter.readGoal + "**"
FROM "Journal/Daily" and #Daily
WHERE week = "<% moment(tp.file.title).format("gggg-[W]ww")%>"
group by week
```
```dataview
List without id
"## 👾Stream "+" ![test](https://progress-bar.dev/" + round(sum(rows.stream)/this.file.frontmatter.streamGoal*100) + "/?title=progress&width=70)" +"
⏱️__**Hours:**__ **" + sum(rows.stream)+ "/" +this.file.frontmatter.streamGoal + "**"
FROM "Journal/Daily" and #Daily
WHERE week = "<% moment(tp.file.title).format("gggg-[W]ww")%>"
group by week
```
---
# Tasks **<span style="font-size: 20px;">Alt + T to add task</span>**
### **Earings**
```tasks
not done
due (after <% moment(tp.file.title).startOf('isoWeek').format("YYYY-MM-DD")%>) and (before <% moment(tp.file.title).endOf('isoWeek').format("YYYY-MM-DD")%>)
```

### **Completed**
```tasks
due <% tp.date.now() %>
done
```
---
