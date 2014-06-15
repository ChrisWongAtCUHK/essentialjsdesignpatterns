<html>
<head>
</head>
<body>
<!--
<h1><a href="http://www.addyosmani.com/resources/essentialjsdesignpatterns/book/#modulepatternjavascript">Learning JavaScript Design Patterns</a></h1>
<ul>
<li><a href="http://www.addyosmani.com/resources/essentialjsdesignpatterns/book/#introduction">Introduction</a></li>
<li><a href="http://www.addyosmani.com/resources/essentialjsdesignpatterns/book/#whatisapattern">What is a Pattern?</a></li>
-->
<script>
	var baseURL = "http://www.addyosmani.com/resources/essentialjsdesignpatterns/book/";
	var myListId = "myList";
	
	/*
	 * To add an item to unordered list
	 */
	function itemAdd(text, href){
		var li = document.createElement("LI");
		var a = document.createElement("A");
		var textNode = document.createTextNode(text);
		a.setAttribute("href", baseURL + '#' + href);
		
		var myList = document.getElementById(myListId);
		a.appendChild(textNode);
		li.appendChild(a);
		myList.appendChild(li);
	}
	   
	/*
	 * One-time element creation
	 */
	(function(){
		// top title
		var h1 = document.createElement("H1");
		var a = document.createElement("A");
		var textNode = document.createTextNode("Learning JavaScript Design Patterns");
		a.appendChild(textNode);
		a.setAttribute("href", baseURL);
		h1.appendChild(a);
		
		// table of contents
		var ul = document.createElement("UL");
		ul.setAttribute("id", myListId);
		
		document.body.appendChild(h1);
		document.body.appendChild(ul);
		itemAdd("Introduction", "introduction");
		itemAdd("What is a Pattern?", "whatisapattern");
		
	 })();
	 
</script>
</ul>
</body>
</html>
