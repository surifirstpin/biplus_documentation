---


---

<center><h1>Global Function</h1></center>
<h2 id="definition">Definition</h2>
<p>A common set of statements or operations can be defined globally as a function and it can be retrieved and used in any project. One global function shall be referred from another global function, But it should not be repeated in limitless.</p>
<p><strong>Getting Started :</strong></p>
<blockquote>
<p>Path :  Settings–&gt;click on global functions.</p>
</blockquote>
<ol>
<li>Click on Add-Functions to create new function.</li>
</ol>
<p><img src="https://raw.githubusercontent.com/sv18042016/fp1/d9712e86a6881444e961d60dfc6aab30bf665172/images/func1.png" alt="enter image description here"></p>
<p>** Syntax : **</p>
<pre><code>/* My Custom function*/

/*START*/ 
function myfunction_8(param1,param2)
{
 // Define function body   
   return 0;
}
/*END*/
</code></pre>
<p><strong>Example :</strong></p>
<pre><code>/* My Custom function*/

/*START*/ 
function _Addition(param1,param2)
{
 var add =param1+param2;  
  return add;
}
/*END*/
/* Returns value 3, if we provide 1 and 2 in Test*/
</code></pre>
<ol start="2">
<li>Click on <strong>Test</strong> Button  to run the function.</li>
<li>Click on <strong>Save</strong> Button to save the function.</li>
</ol>
<p><img src="https://raw.githubusercontent.com/sv18042016/fp1/2c15dfa03d8ed5eed5cdffdc1335c22ce759300c/images/global_functions.png" alt="enter image description here"></p>
<h2 id="ability-to-adopt-javascript">Ability to adopt Javascript</h2>
<p>This functions supports all the native java script supported functions and also refer other global functions using " bi.Function_name."</p>
<h2 id="edit-function">Edit Function</h2>
<ol start="4">
<li>Enable edit key to <strong>Edit</strong> the function.</li>
</ol>
<p><img src="https://raw.githubusercontent.com/sv18042016/fp1/733be26f2d58ffc41ec83bc979234243c5417a2e/images/edit_func.png" alt="enter image description here"></p>
<h2 id="delete-function">Delete Function</h2>
<ol start="5">
<li>Click on delete button to <strong>Delete</strong> the function.</li>
</ol>
<p><img src="https://raw.githubusercontent.com/sv18042016/fp1/3e9f75a909b59664ffe91af0ad16c2c9859586cf/images/del_func.png" alt="enter image description here"></p>
<h2 id="developer-privileges">Developer Privileges</h2>
<p>All the users have privilege to access global functions in calculated column,  but admin and developer has an ability to create, edit and delete a global function.</p>

