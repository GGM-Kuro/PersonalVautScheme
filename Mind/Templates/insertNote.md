[[<%* let note =(await tp.system.suggester((item) => item.basename, app.vault.getFiles().filter(file.basename => file.path.includes("Knowledge/Notes")), false, 'Choice Note')).file.basename;
tR += theme;
%>|<% tp.system.prompt("display text",note)%>]]<% tp.file.cursor(0)%>
