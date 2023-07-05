---
bikeGoal: <% await tp.system.prompt(" How long are you going to ride a bike this week?", "0") %>
---
[[README]] || [[`To-Do|To-do Kanban ]] || [[Library.canvas|Library]]
[[Journal/Weekly/<% moment(tp.file.title).subtract(1,'week').format("gggg-[W]ww") %>|↶ Previous Week]] | [[Journal/Weekly/<% moment(tp.file.title).add(1,'week').format("gggg-[W]ww") %>|↷ Next Week]] 

# <% moment(tp.file.title).startOf('isoWeek').format("MMM DD") %> - <% moment(tp.file.title).endOf('isoWeek').format("MMM DD") %>

# Days

-[[Journal/Daily/<% moment(tp.file.title).startOf('isoWeek').add(0,'day').format("YYYY-MM-DD") %>|Monday]]
-[[Journal/Daily/<% moment(tp.file.title).startOf('isoWeek').add(1,'day').format("YYYY-MM-DD") %>|Tuesday]]
-[[Journal/Daily/<% moment(tp.file.title).startOf('isoWeek').add(2,'day').format("YYYY-MM-DD") %>|Wednesday]]
-[[Journal/Daily/<% moment(tp.file.title).startOf('isoWeek').add(3,'day').format("YYYY-MM-DD") %>|Thursday]]
-[[Journal/Daily/<% moment(tp.file.title).startOf('isoWeek').add(4,'day').format("YYYY-MM-DD") %>|Friday]]
-[[Journal/Daily/<% moment(tp.file.title).startOf('isoWeek').add(5,'day').format("YYYY-MM-DD") %>|Saturday]]
-[[Journal/Daily/<% moment(tp.file.title).startOf('isoWeek').add(6,'day').format("YYYY-MM-DD") %>|Sunday]]

---
# Daily overview
```dataview
TABLE without ID
	file.link AS Day,
	mood as "😶‍🌫️",
	bike as "🚴‍♂️",
	gym AS "🏋️‍♂️",
    practice + "| "  + "[[" + ability + "]]" AS " 📖 ✏️",
	englishClass  AS "🗽"
FROM "Journal/Daily"
WHERE week = "<% moment(tp.file.title).format("gggg-[W]ww")%>"
SORT file.name ASC
```
---
# Practice overview
```dataview
TABLE without ID 
		"🚴‍♂️ | Bike"  as "Trained This Week 🚵‍♂️",
		"![test](https://progress-bar.dev/" + round(sum(rows.bike)/this.file.frontmatter.bikeGoal*100) + "/?color=555555&width=150)"  as  "Percentage",
		sum(rows.bike) + " | " + this.file.frontmatter.bikeGoal + " ⏱️Hours "  as  Time 
FROM "Journal/Daily" and #Daily
WHERE week = "<% moment(tp.file.title).format("gggg-[W]ww")%>"
group by week
```
---
# Notes overview
```dataview
TABLE without id

"[" + title + "]" + "(" + file.name + ")" as Notes,
"[[" + theme + "]]" as Theme,
date

FROM #note
WHERE week = "<% moment(tp.file.title).format("gggg-[W]ww")%>"
```

# Tasks **<span style="font-size: 20px;">Alt + T to add task</span>**
### **Earrings**
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
