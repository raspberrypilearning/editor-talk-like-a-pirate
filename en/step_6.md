<h2 class="c-project-heading--task">Use regex for trickier pirate phrases</h2>

--- task ---
Add regex rules so the translator can change punctuation, word patterns, and the order of some pirate phrases.
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

<div class="c-project-callout c-project-callout--debug" style="font-size: 1.1em">
  <strong>Debug:</strong> The <span class="rpf-tip" tabindex="0"
      data-tip="^ matches the start of the text, (\\w+)!\\s matches words before an exclamation mark, and (\\w+)ev(\\w+) finds words containing ev.">regex patterns</span> work best when you test with a full sentence such as <code>Hello! I was never ready</code>.
</div>

--- task ---
Add the final regex rules to `index.html`.

<div class="c-project-code">

--- code ---
---
language: html
filename: index.html
line_numbers: true
line_number_start: 34
line_highlights: 36-40
---
          words = words.replace(/ yes /gi, " aye ");

          words = words.replace(/^/, "Arr, me hearties. "); // Add a pirate greeting to the start of the text
          words = words.replace(/(\w+)!\s/g, "$1! Yo ho ho! "); // Add a pirate shout after exclamations
          words = words.replace(/(\w+)ev(\w+)\s/g, "$1e'$2 "); // Change words like never to ne'er
          words = words.replace(/was\s(\w+)ed\s/g, "be $1ing "); // Turn was ...ed into be ...ing
          words = words.replace(/was/gi, "wer"); // Change any remaining was to wer after the regex above

          $("#pirate").val(words);
--- /code ---

</div>
--- /task ---

<div class="c-project-output">
  ![The finished pirate translator with converted pirate phrases](images/finished-pirate.png)
</div>

--- task ---
**Test:** Type `Hello! I was never ready` and check that the pirate box adds `Arr, me hearties.`, adds `Yo ho ho!`, and changes `never` to `ne'er`.
--- /task ---
