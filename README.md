#### Title : Quiz App####
#### Video Demo : <https://youtu.be/um5OhDO-MlQ> ####
#### Description ####
Quiz App is a way to test and improve your skills. Creating a JavaScript quiz is a cool learning exercise. It teaches you how to use events, manipulate the DOM, and handle user input.

 I have created 4 files for this program first one is for HTML file, the Second one is for CSS file, & the third one is for JavaScript ( JS ) file. I have put comments where you can add or change question answers in the JS file. You can change layout style in CSS file provided in this program.
File names are: 

•	index.html

•	style.css

•	question.js

•	script.js

•	Snap and Image Folder

index.html

This is the main file from where the execution begins Quiz app.
By using< link> tag under the head section we add the css file into main page.
<link rel="stylesheet" href="brain/css/style.css" />
By using <script> tag the js files are added in the index.html
<script src="brain/js/questions.js"></script>
<script src="brain/js/script.js"></script>
The <div> tag defines a division or a section in an HTML document. It is used as a container for HTML elements - which is then styled with CSS or manipulated with JavaScript. It is easily styled by using the class or id attribute.
<body onload="chkUser()">
		<div class="container box-shadow">
			<!-- The Form -->
			<div id="username">
				<form class="form" onsubmit="return false;">
					<i class="material-icons">face</i>
					<h2>What's Your Nick Name?</h2>
					<div class="form-group mx-sm-3 mb-3 passBox">
						<label for="pass" class="sr-only">Nick Name</label>
						<input
							type="text"
							class="form-control"
							id="uname"
							placeholder="Nick Name"
							onfocus="this.style.borderColor = '#007bff'"
							onblur="this.style.borderColor = '#ced4da'"
						/>
					</div>
					<button
						type="submit"
						class="btn btn-primary mb-2"
						onclick="askPass();"
					>
						Proceed...
					</button>
				</form>
			</div>
On loading the page, The Onload Event calls the chkUser() function. This function is used to check from localstorage whether the user provided name before...
Asking for name
function askPass() {
	// when user puts name and press enter
	if (uname.value == '' || uname.value == null || uname.value == 'undefined') {
		// if nothing is input, make name "BUDDY".
Checking for password: Confirms the identity.
function chkPass(btn) {
	// checking password
	if (pass.value == 11223344) {
		// if password is correct
After that we will proceed for quiz, with correct password.
function startQuiz() {
	theForm.style.display = 'none'; // hide the password form
	theQuiz.style.display = 'block'; // show the quiz page
	randomQ(); // trigger first question
}
For incorrect password
function resetErr() {
	// reset all error to default (This is triggered when user focus on pass input box)

style.css
The use of style sheets (which are separate to the HTML files) allows the quick re-styling of any document, without modifying the original HTML. It guarantees consistency throughout website. The smaller the files the faster the download. Using style sheets can help minimize file sizes, since, for example, every < font > tag, is defined in one place in a style sheet, rather than in multiple places in the HTML file.

question.js
This file is used to create the quiz, in this function CQuiz () is created.
function CQuiz(que, o1, o2, o3, o4, ans, d) {
	this.question = que;
	this.opt1 = o1;
	this.opt2 = o2;
	this.opt3 = o3;
	this.opt4 = o4;
	this.answer = ans;
	this.asked = d;
}
script.js
In this file various JavaScript functions and events are created related to the quiz app.
Events used this app are
On Body Load ()
Functions used in this app are:
chkUser()
askPass()
chkPass()
startQuiz()
randomQ()
validateForm()
 showResult()
logout()
retakeQuiz()













\
