What is Form Validation? Why is it important?
Form validation is a process used to ensure that the data entered into a form by a user meets certain criteria or requirements before it is submitted to a server or processed further. It's like double-checking the information you provide in a form to make sure it's correct and complete before you submit it.

Imagine filling out a long form only to discover at the end that you missed a required field or entered invalid data. This leads to unnecessary frustration and re-work for the user. Form validation catches these errors early,

Client-side validation
Checks user input directly in the user's web browser using JavaScript to develop the validation logic.

Server-side Validation
Validates user input on the server using server-side programming languages like PHP, Python, Nodejs 


Basic validation using html.
Demonstrate basic validation using built-in HTML attributes like required, type, min, max, minlength, and maxlength.

AFTER THE EXAMPLE

Remember, while these built-in attributes offer a good starting point, consider combining them with JavaScript for more robust and user-friendly validation experiences.

Accessing Form Elements and Values:

JavaScript
// Get the entire form element
const form = document.getElementById("myForm");

// Get specific elements by ID or name
const nameInput = document.getElementById("name");
const emailInput = document.getElementById("email");
const passwordInput = document.getElementById("password");
const confirmPasswordInput = document.getElementById("confirm-password");

// Get values from elements
const nameValue = nameInput.value;
const emailValue = emailInput.value;
const passwordValue = passwordInput.value;

Preventing default action
event.preventDefault() is a JavaScript method that's often used in web development to prevent the default behavior of an event from occurring. Let's break it down for beginners:

Events: In web development, events are actions or occurrences that happen in the browser as a result of user interactions or system events. Examples include clicking on a button, submitting a form, or pressing a key on the keyboard.

Default Behavior: When an event occurs, the browser usually has a default action associated with it. For example, clicking on a link typically navigates to the URL specified in the link's href attribute, and submitting a form usually sends the form data to a server for processing.

Preventing Default: event.preventDefault() is a method that can be called on an event object to stop the browser from performing its default action in response to that event. In other words, it tells the browser, "Hey, don't do what you normally do when this event happens."

Example:

Suppose you have a form on a webpage, and you want to perform some client-side validation before allowing the form to be submitted.
You can attach an event listener to the form's submit event. Within that event listener function, you can perform your validation checks.
If the validation fails (e.g., required fields are empty), you can call event.preventDefault() to prevent the form from being submitted to the server.
This gives you control over what happens next. You can display error messages to the user, prompt them to correct their input, or take any other action you deem necessary before allowing the form submission to proceed.
In summary, event.preventDefault() is a handy tool in JavaScript for controlling the behavior of events in web applications. It allows you to intervene and customize the browser's default behavior, giving you more control over how your web pages interact with users.

How to use it
Prevent Default Submission: Immediately upon entering the event handler, you call event.preventDefault() to prevent the form from being submitted by the browser.

Perform Validation: You then perform your validation checks on the form fields. If any validation check fails, you can display error messages to the user and exit the function early by using the return statement.

Allow Submission: If all validation checks pass, you can allow the form submission to proceed by either submitting the form programmatically (form.submit()) or by simply letting the event handler function finish executing.


REGEX or regular expression that helps you check if your the data a user provides matches a specific pattern. This secret code is called "pattern detective."

/: This is the starting delimiter of the regular expression.

^: This anchor asserts the start of the string.

[^\s@]+: This part matches one or more characters that are not whitespace (\s) or the "@" symbol. [^\s@] means any character that is not a whitespace or "@".

@: This matches the "@" symbol.

[^\s@]+: This part again matches one or more characters that are not whitespace or "@", representing the domain part of the email address.

\.: This matches a literal dot (.). Since dot is a special character in regex, it needs to be escaped with a backslash \. to be treated as a literal dot.

[^\s@]+: This part matches one or more characters that are not whitespace or "@", representing the top-level domain part of the email address (like ".com", ".org", etc.).

$: This anchor asserts the end of the string.

/: This is the ending delimiter of the regular expression.

form.submita()
When you call form.submit(), it triggers the same action as if the user had clicked the submit button on the form. This means that the form data is sent to the server for processing, and the browser may navigate to a new page or refresh the current page depending on the form's action attribute.

It's important to note that calling form.submit() bypasses any client-side validation checks that you may have implemented in your code. Therefore, you should only call form.submit() after ensuring that the form data is valid and ready to be submitted.





