<h2 class="c-project-heading--task">Load jQuery when the page opens</h2>

--- task ---
Add jQuery and a ready event so you can confirm your page runs JavaScript after it has loaded.
--- /task ---

<div class="c-project-callout c-project-callout--debug" style="font-size: 1.1em">
  <strong>Debug:</strong> If no pop-up appears, refresh the page and check that the jQuery <code>script src</code> line is inside the <code>&lt;head&gt;</code> section.
</div>

--- task ---
Update `index.html` to load jQuery and show an alert when the page is ready.

<div class="c-project-code">

--- code ---
---
language: html
filename: index.html
line_numbers: true
line_number_start: 11
line_highlights: 12-17
---
  <title>Talk like a Pirate</title>
  <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.7.1/jquery.min.js"></script> <!-- Load the current jQuery library -->
  <script>
    $(function() { // Run the code after jQuery knows the page is ready
      alert("Page has loaded"); // Show a message when the page is ready
    });
  </script>
</head>
--- /code ---

</div>
--- /task ---

<div class="c-project-output">
  ![A browser alert that says Page has loaded](images/page-has-loaded.png)
</div>

--- task ---
**Test:** Refresh the page and check that a pop-up says `Page has loaded`.
--- /task ---
