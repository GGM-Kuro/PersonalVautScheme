[[<%*let abilitie =(await tp.system.suggester((item) => item.basename, app.vault.getFiles().filter(file => file.path.includes("Knowledge/Abilities")), false, 'Choice Concept')).basename;
abilitie += "|";
let display = await tp.system.prompt("display text");
tR += abilitie + display %>]] <% tp.file.cursor(0) %>