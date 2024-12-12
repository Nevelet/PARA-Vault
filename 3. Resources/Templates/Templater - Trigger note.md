
<%*
const title = tp.file.title


// Source Video
if (title.includes('+')) {
	return tp.file.include('[[Templater - Select Type Source]]')
}

// Projects
if (title.includes('pj')) {
	return tp.file.include('[[Page - Project]]')
}

// People
else if (title.startsWith("@")) {
 	return tp.file.include('[[Page - People]]')
} 

else {
	return tp.file.include('[[Templater - Select Type Note]]')
}

%>
