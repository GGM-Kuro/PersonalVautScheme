---
tag: project
project: <%* let project = await tp.system.prompt("Project Name:");
while (tp.file.find_tfile("Projects/" + project)){
project = await tp.system.prompt("Already exist, insert new name:")};
await tp.file.move("Projects/" + project )
tR += project; %>
---


# Tasks
### Earring
```tasks
not done
filename includes <% project %>
```

### Completed
```tasks
done
filename includes <% project %>
```

