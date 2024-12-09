<%*
let type = await tp.system.suggester([
"Standard Note", 
"Source", 
"Project",
"Empty"
], [
"Standard Note", 
"Source", 
"Project",
"Empty"

], 
true, "Select type note")

if(type == "Standard Note"){
	return await tp.file.include("[[Page - Note]]")
	
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

