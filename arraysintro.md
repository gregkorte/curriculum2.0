---
layout: default
title: "Interactive Arrays Lesson"
---

<h1>Arrays (a.k.a. collections of things)</h1>
<p>In software, values don't only have to be assigned individually to variables.</p>

<pre>
  <code class="language-js">
const flower1 = "Tulip";
const flower2 = "Rose";
const flower3 = "Daffodil";
const flower4 = "Daisy";
  </code>
</pre>

<p>Since you have four strings that are all describing a similar type of thing - flowers - you can put those four strings in a collection called an array in JavaScript. You can spot an array in code by seeing some comma-delimited values surrounded by square brackets: <code>[ ]</code>.</p>

<h2>Interactive Example</h2>
<p>Here’s an array of those four flowers. Edit it and run it to see what happens!</p>

<div class="code-editor">
  <textarea id="code-example">
const flowers = ["Tulip", "Rose", "Daffodil", "Daisy"];
document.write(flowers);
  </textarea>
  <button onclick="runCode('code-example')">Run Code</button>
  <div id="output-example" class="output"></div>
</div>

<h2>Exercise: Your First Array</h2>

<h3>Setup</h3>
<pre>
  <code class="language-sh">
cd
cd workspace
mkdir arrays-intro
cd arrays-intro
touch main.js
code .
  </code>
</pre>

<p>Once VS Code starts, open the <code>main.js</code> file and copy the following code into the file.</p>

<pre>
  <code class="language-js">
const yellowFruit = "Banana";
const orangeFruit = "Orange";
const redFruit = "Apple";
const greenFruit = "Watermelon";
const blueFruit = "Blueberry";

const fruits = [];

console.log(fruits);
  </code>
</pre>

<h3>Instructions</h3>
<p>Take the 5 values assigned to the 5 variables and store them in the provided blank array instead. When you are done, there should be no variables with string values left in your code - only the <code>fruits</code> variable.</p>

<h3>Run Your Code</h3>
<p>In your terminal, run your code with the following command:</p>

<pre>
  <code class="language-sh">
node main.js
  </code>
</pre>

<p>You should see the following output in the terminal:</p>

<pre>
  <code class="language-sh">
[ 'Banana', 'Orange', 'Apple', 'Watermelon', 'Blueberry' ]
  </code>
</pre>

<script src="https://cdnjs.cloudflare.com/ajax/libs/codemirror/5.65.7/codemirror.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/codemirror/5.65.7/mode/javascript/javascript.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/codemirror/5.65.7/addon/runmode/runmode.min.js"></script>

<script>
function runCode(editorId) {
  const code = document.getElementById(editorId).value;
  const outputElement = document.getElementById('output-' + editorId.split('-')[1]);
  try {
    const result = eval(code);  // Simple eval for demo; not recommended for complex or untrusted code.
    outputElement.innerText = result === undefined ? 'Code ran successfully!' : result;
  } catch (error) {
    outputElement.innerText = 'Error: ' + error.message;
  }
}
</script>

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/codemirror/5.65.7/codemirror.min.css">
<style>
  .code-editor {
    margin: 20px 0;
  }
  .output {
    background-color: #f7f7f7;
    padding: 10px;
    border: 1px solid #ddd;
    margin-top: 10px;
  }
</style>
