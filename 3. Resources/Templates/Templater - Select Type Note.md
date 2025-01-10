<%*
let type = await tp.system.suggester([
"Note", 
"Source", 
"Project",
"Empty"
], [
"Note", 
"Source", 
"Project",
"Empty"

], 
true, "Select type note")

if(type == "Note"){
	return await tp.file.include("[[Page - Note General]]")
	
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

