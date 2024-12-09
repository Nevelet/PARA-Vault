<%*
let type = await tp.system.suggester([
"Video", 
"Article",
"Book", 
"Movie (Film)",
"Movie (Serie Tv)"
], [
"Video", 
"Article",
"Book", 
"Movie (Film)",
"Movie (Serie Tv)"

], 
true, "Select type source")

if(type == "Video"){
	return await tp.file.include("[[Page - Source Video]]")
	
} 

else if(type == "Article"){
	return await tp.file.include("[[Page - Source Article]]")
}

else if(type == "Book"){
	return await tp.file.include("[[Page - Source Book]]")
} 

else if(type == "Movie (Film)"){
	return await tp.file.include("[[Page - Source Movie (Film)]]")
} 

else if(type == "Movie (Serie Tv)"){
	return await tp.file.include("[[Page - Source Movie (Serie Tv)]]")
} 

-%>

