<h2 class="c-project-heading--task">Create the page layout</h2>

--- task ---
Update the starter code so the page has two text areas for normal text and pirate text.
--- /task ---

<style>
.rpf-tip{
  position: relative;
  display: inline-block;
  border-bottom: 1px dotted currentColor;
  cursor: help;
}

.rpf-tip::after{
  content: attr(data-tip);
  position: absolute;
  left: 0;
  bottom: 125%;

  width: max-content;
  max-width: 38ch;
  white-space: normal;

  padding: .5em .6em;
  font-size: .85em;
  line-height: 1.25;

  background: #111;
  color: #fff;
  border-radius: .35em;

  opacity: 0;
  visibility: hidden;
  pointer-events: none;
  z-index: 9999;
}

.rpf-tip::before{
  content: "";
  position: absolute;
  left: 1em;
  bottom: 115%;
  border: .4em solid transparent;
  border-top-color: #111;

  opacity: 0;
  visibility: hidden;
  pointer-events: none;
  z-index: 9999;
}

.rpf-tip:hover::after,
.rpf-tip:focus::after,
.rpf-tip:hover::before,
.rpf-tip:focus::before{
  opacity: 1;
  visibility: visible;
}
</style>

<div class="c-project-callout c-project-callout--tip" style="font-size: 1.1em">
  <strong>Tip:</strong> The <span class="rpf-tip" tabindex="0"
      data-tip="An id lets jQuery target one specific element later in the project."><code>id</code></span> names <code>normal</code> and <code>pirate</code> are important because your script will use them later.
</div>

--- task ---
Update `index.html` in the starter project.

<div class="c-project-code">

--- code ---
---
language: html
filename: index.html
line_numbers: true
line_number_start: 1
line_highlights: 1,4-11,15-19
---
<!DOCTYPE html>
<html>
<head>
<style type="text/css">
  textarea {
    width: 400px; /* Make the text areas wider */
    height: 200px; /* Make the text areas taller */
    font-family: arial; /* Use a simple readable font */
  }
</style>
  <title>Talk like a Pirate</title> <!-- Update the page title -->
</head>
<body>

<h2>Landlubbers</h2> <!-- Label the normal text box -->
<textarea id="normal"></textarea> <!-- Create the input text area -->

<h2>Pirates</h2> <!-- Label the pirate text box -->
<textarea id="pirate"></textarea> <!-- Create the output text area -->

</body>
</html>
--- /code ---

</div>
--- /task ---

<div class="c-project-output">
  ![Two text areas labelled Landlubbers and Pirates on the page](images/boxes.png)
</div>

--- task ---
**Test:** Open `index.html` in a browser and check that you can see a title and two large text boxes.
--- /task ---
