<h2 class="c-project-heading--task">Copy text as you type</h2>

--- task ---
Replace the alert with a keyup listener so the pirate text box copies whatever you type into the normal text box.
--- /task ---

<div class="c-project-callout c-project-callout--tip" style="font-size: 1.1em">
  <strong>Tip:</strong> <code>.val()</code> reads the text inside a text area, and it can also write new text back into one.
</div>

--- task ---
Update the jQuery code in `index.html`.

<div class="c-project-code">

--- code ---
---
language: html
filename: index.html
line_numbers: true
line_number_start: 13
line_highlights: 15-19
---
  <script>
    $(function() {
      $("#normal").on("keyup", function() { // Listen for key presses in the normal text box
          var words = $("#normal").val(); // Read the text from the normal text box
          $("#pirate").val(words); // Copy the same text into the pirate text box
      });
    });
  </script>
--- /code ---

</div>
--- /task ---

<div class="c-project-output">
<pre>Hello there

Hello there</pre>
</div>

--- task ---
**Test:** Type a sentence into the `Landlubbers` box and check that the same sentence appears in the `Pirates` box.
--- /task ---
