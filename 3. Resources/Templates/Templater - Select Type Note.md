<%*
let type = await tp.system.suggester([
"General Note", 
"Area Note",
"Source", 
"Project",
"Empty"
], [
"General Note", 
"Area Note",
"Source", 
"Project",
"Empty"

], 
true, "Select type note")

if(type == "General Note"){
	return await tp.file.include("[[Page - Note General]]")
	
} 

else if(type == "Area Note"){
	return await tp.file.include("[[Page - Note Area]]")
}

else if(type == "Source"){
	return await tp.file.include("[[Templater - Select Type Source]]")
}

else if(type == "Project"){
	return await tp.file.include("[[Page - Project]]")
} 

else if(type == "Empty"){
	return await tp.file.include("[[Page - Empty]]")
} 

-%>

