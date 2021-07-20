- What is HTML?
	- Hyper Text Markup Language (HTML)
		- Angle bracket based structure
		- Derived from SGML

			```jsx
			<html>
				<head>
				</head>
				<body>
					<h1>Hello World</h1>
				</body>
			</html>
			```

	- Angle-Brackets ≠ XML
		- Not Case sensitive
		- Mixed closing rules

			```jsx
			<html>
				<head>
				</head>
				<body>
					<h1>Hello World</h1>
				</body>
			</html>
			```

	- Document Object Model (DOM)
		![DOM image](/screenshots/DOM.png)

- Hello Markup

	```jsx
	// <foo></foo> // basic element
	// <bar /> //self-closing element

	<div>
		<img />
		<p> Hello <b>World</b>, Jay </p>
	</div> 
	```

- Structure of an HTML Page

	```jsx
	<!DOCTYPE html>
	<html>
		<head>
			<title> Github Hub </title>
		</head>
		<body>
			<h1> Github Hub </h1>
			<p> This is a <i>site</i> to search for interesting <b>projects</b>.</p>
			<p> This is a <em>site</em> to search for interesting <strong>projects</strong>.</p> 
			<p> In this sample site, we'll show a list of <a href="http://github.com/">Github</a> projects and data about those projects.</p>
		</body>
	</html>
	```

	- DOCTYPE tell the browser the type of the file
	- Each html has a head and a body
	- The title in the `<head>` is going to be displayed when you bookmark this page.
	- `<body>` section is what visible to the users
	- `<h1> ~ <h6>` is six different size of headers
	- `<p>` is a paragraph
	- `<i></i>` means italic the text, in HTML5 `<em></em>` does the same trick
	- `<b></b>` means bold the text, in HTML5 `<strong></strong>` does the same trick
	- The `<a>` HTML element (or anchor element), with its href attribute, creates a hyperlink to web pages, files, email addresses, locations in the same page, or anything else a URL can address.
- Tags

	```jsx
	<!DOCTYPE html>
	<html>
		<head>
			<title> Github Hub </title>
		</head>
		<body>
			<div> // <header>
				<h1> Github Hub </h1>
				<p> This is a <i>site</i> to search for interesting <b>projects</b>.</p>
				<nav>
					<ul>
						<a href="index.html"> Home</a>
						<a href="contact.html"> Contact</a>
						<a href="about.html"> About</a>
					</ul>
				</nav>
			</div> // </header>
			<div>
				<p> This is a <em>site</em> to search for interesting <strong>projects</strong>.</p> 
				<p> In this sample site, we'll show a list of <a href="http://github.com/">Github</a> projects and data about those projects.</p>
			<div>	
			<div> // <footer>
				&copy; 2014 Shawn Wildermuth LLC
			</div> // </footer>
		</body>
	</html>
	```

	- `<div></div>` means a rectangular container section of a html page
	- `&` is escaped characters, `&copy` shows copy right symbol
	- `<span></span>` in-line container
	- In HTML5, `<header></header>`, `<footer></footer>`, `<section></section>`, `<nav></nav>` are added to give semantic means to the body sections of the html page.
	- `<ol></ol>` means ordered list, this will display a vertical list with number before the content
	- `<ul></ul>` means un-ordered list, this will display a vertical bullet point of the list of contents.
- HTML Forms

	```jsx
	<!DOCTYPE html>
	<html>
		<head>
			<title> Github Hub </title>
		</head>
		<body>
			<div> // <header>
				<div> Github Hub </div>
				<div> This is a <i>site</i> to search for interesting <b>projects</b>.</div>
				<nav>
					<ul>
						<a href="index.html"> Home</a>
						<a href="contact.html"> Contact</a>
						<a href="about.html"> About</a>
					</ul>
				</nav>
			</div> // </header>
			<section>
				<p> This is a <em>site</em> to search for interesting <strong>projects</strong>.</p> 
				<p> In this sample site, we'll show a list of <a href="http://github.com/">Github</a> projects and data about those projects.</p>
				<form action="http://wilder.azurewebsites.net/echo" method="POST">
					<label for="search phrase">Search Phrase:</label>
					<input name="searchPhrase" id="searchPhrase"/><br/>
					<input type="checkbox" name="useStars" id="useStars" checked="true" /> 
					<label for="UseStars">Use Stars?</label><br/>
					<label for="langChoice">Language:</label>
					<select name="langChoice">
						<option>All</option>
						<option>JavaScript</option>
						<option selected>C#</option>
						<option>Java</option>
						<option>Ruby</option>
					</select>
					<br/>
					<input type="submit" value="search" />
				</form >
			</section>	
			<div> // <footer>
				&copy; 2014 Shawn Wildermuth LLC
			</div> // </footer>
		</body>
	</html>
	```

	- `<form></form>` is used for getting input from the user, so we can use it later
	- `<input/>` element take input form the user, `type` give the type of button, `value` shows text on the button, name give a reference for the text input
	- `<br/>` element is a break line so that each element is on its own line
	- `<select></select>` gives a list of options for user to choose, `selected` gives the default choice, `<option></option>` lists different options for a select
	- `<label>` gives the a description of the text input and its function
- Cross Browser HTML

	```jsx
	<!DOCTYPE html>
	<html>
		<head>
			<title> Github Hub </title>
		<!--
			comments
			Buildt for the PluralSight Course for new Web Developers
			-->
		</head>
		<body>
			<div> // <header>
				<div> Github Hub </div>
				<!--[if lt IE 9]>
					<script src="//html5shiv.googlecode.com/svn/trunk/html5.js></script>
				<![endif]-->
				<div> This is a <i>site</i> to search for interesting <b>projects</b>.</div>
				<nav>
					<ul>
						<a href="index.html"> Home</a>
						<a href="contact.html"> Contact</a>
						<a href="about.html"> About</a>
					</ul>
				</nav>
			</div> // </header>
			<section>
				<p> This is a <em>site</em> to search for interesting <strong>projects</strong>.</p> 
				<p> In this sample site, we'll show a list of <a href="http://github.com/">Github</a> projects and data about those projects.</p>
				<form action="http://wilder.azurewebsites.net/echo" method="POST">
					<label for="search phrase">Search Phrase:</label>
					<input name="searchPhrase" id="searchPhrase"/><br/>
					<input type="checkbox" name="useStars" id="useStars" checked="true" /> 
					<label for="UseStars">Use Stars?</label><br/>
					<label for="langChoice">Language:</label>
					<select name="langChoice">
						<option>All</option>
						<option>JavaScript</option>
						<option selected>C#</option>
						<option>Java</option>
						<option>Ruby</option>
					</select>
					<br/>
					<input type="submit" value="search" />
				</form >
			</section>	
			<div> // <footer>
				&copy; 2014 Shawn Wildermuth LLC
			</div> // </footer>
		</body>
	</html>
	```

	- `<!-- comments -->` is comment structure in HTML
	- You can use comments to handle cross platform HTML

		```
					<!--[if lt IE 9]>
						<script src="//html5shiv.googlecode.com/svn/trunk/html5.js></script>
					<![endif]-->
		```

- Summary
	- HTML has always been written by the winners — the browser makers.
	- Don't let HTML5 as a moniker scare you. It's a catch-all for a set of web technologies.
	- At it's core, HTML is just structural markup...a way to describe a hierarchical document.
	- Form elements in HTML are for accepting input, the rest is primarily for display.
	- Browsers inequality means you'll want to use simple techniques to level the playing field.