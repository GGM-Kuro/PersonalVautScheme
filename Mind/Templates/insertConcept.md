[[<%*let concept =(await tp.system.suggester((item) => item.basename, app.vault.getFiles().filter(file => file.path.includes("Knowledge/Concepts")), false, 'Choice Concept')).basename;
concept += "|";
let display = await tp.system.prompt("display text");
tR += concept + display %>]] <% tp.file.cursor(0) %>