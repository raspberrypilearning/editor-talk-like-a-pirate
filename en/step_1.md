<h2 class="c-project-heading--task">You will make</h2>

--- task ---
In this project, you will build a webpage that turns everyday text into pirate speech as you type.
--- /task ---

<div class="c-project-output">
  <iframe src="https://editor.raspberrypi.org/en/embed/viewer/editor-talk-like-a-pirate-complete" width="600" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen>
  </iframe>
</div>

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
  <strong>Tip:</strong> In the finished example, type <span class="rpf-tip" tabindex="0"
      data-tip="This becomes a direct pirate word replacement later in the project.">hello</span> and <span class="rpf-tip" tabindex="0"
      data-tip="A regex later in the project changes this to ne'er.">never</span> to spot two different kinds of translation.
</div>

--- task ---
**Test:** Open the example and check that typing into the top box updates the pirate text in the bottom box.
--- /task ---
