<h2 class="c-project-heading--task">Create the page layout</h2>

Update the starter code so the page has two text areas for normal text and pirate text.

<h2 class="c-project-heading--explainer">Follow these instructions</h2>

## Step 1

<div class="c-project-callout c-project-callout--tip" style="font-size: 1.1em">
  <strong>Tip:</strong> The <code>id</code> names <code>normal</code> and <code>pirate</code> are important because your script will use them later. An <code>id</code> lets jQuery target one specific element.
</div>

## Step 2

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

<div class="c-project-output">
  ![Two text areas labelled Landlubbers and Pirates on the page](images/boxes.png)
</div>

## Now run your code

Open `index.html` in a browser and check that you can see a title and two large text boxes.
