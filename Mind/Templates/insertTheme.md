[[<%* let theme =(await tp.system.suggester((item) => item.basename, app.vault.getFiles().filter(file => file.path.includes("Knowledge/Themes")), false, 'Choice Theme')).basename;
tR += theme;
%>]]