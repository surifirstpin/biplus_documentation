---


---

<center><h1>Database Connection</h1></center>
<h2 id="definition">Definition</h2>
<p><strong>Connection</strong> specifies a database connection from which a model can retrieve the data. Following are the steps to be followed to set up database connection.</p>
<p><strong>I.</strong>  Get the connection details for database such as Host name, port, username and password etc from <strong>Database Administrator</strong>.</p>
<p><strong>II.</strong> Enable secure access to database, such as :</p>
<ul>
<li>Using  IP Address Whitelist, optionally adding SSL Encryption.</li>
<li>Using SSH Tunnel, which provides a secured and encrypted connection with extra authentication</li>
</ul>
<p><strong>III.</strong> Set up database to work with Bi+. Instructions may vary from dialect to dialect. Typically it includes providing approval to Bi+ to access database.</p>
<h2 id="create-connection">Create Connection</h2>
<p><strong>Getting started :</strong></p>
<blockquote>
<p>Path : Database–&gt;New connection</p>
</blockquote>
<p><strong>1.</strong> Click on <strong>Database Section</strong> to setup a database connection.</p>
<p><strong>2.</strong> Click on <strong>+New connection</strong>  button to start setting up the connection to database. In general,  specify the below mentioned fields:<br>
<img src="https://raw.githubusercontent.com/sv18042016/fp1/master/images/demo%20image.png" alt="enter image description here"></p>
<p><strong>Name</strong> specify a name to define connection.<br>
<strong>Database(dialect)</strong> choose appropriate dialect based on  connection.</p>
<blockquote>
<p>Note: As per your requirement we can include the dialects needed to run the business.</p>
</blockquote>
<ul>
<li><strong>Host</strong>  database host path.</li>
<li><strong>Database</strong> name of the database.</li>
<li><strong>Username and Password</strong> are the credentials used to connect the database.</li>
<li><strong>Maximum connection</strong> concurrent connection used by  database.</li>
<li><strong>Additional Parameters</strong> includes any additional JDBC parameter.</li>
</ul>
<h2 id="ssh">SSH</h2>
<p>a)  To connect Bi+ SSH tunnel with same database host, provide following information to BiPlus analyst :</p>
<ul>
<li>IP address or DNS name of the database server</li>
<li>SSH port of the database server</li>
<li>Database port number</li>
</ul>
<p>b) If connecting with separate database host, provide following information to BI+ analyst:</p>
<ul>
<li>IP address or DNS name of the database server as seen from the tunnel server.</li>
<li>Database port number as seen from the tunnel server.</li>
<li>IP address or DNS name of the tunnel server as seen from the public internet.</li>
<li>SSH port of the tunnel server as seen from the public internet.</li>
<li>Username on the tunnel server for the SSH connection (the standard is looker).</li>
</ul>
<p><strong>3. Dialects</strong> select the accurate dialect from the list using drop down option.</p>
<h2 id="test-and-save-connection">Test and Save Connection</h2>
<p><strong>4. Test Connection</strong> check if the entered information is running accurately.</p>
<p><strong>5. Add Connection</strong> establish and save the connection.</p>
<blockquote>
<p>After establishing the connection you can see the list of connections names on left side toolbar</p>
</blockquote>
<h2 id="edit-a-connection">Edit a connection</h2>
<p><strong>6.</strong> Click on <strong>Edit</strong> option to make changes.</p>
<p><img src="https://raw.githubusercontent.com/sv18042016/fp1/eae5d23007893f45fcaab8db33c5a707e1a7911a/images/edit_conn.png" alt="enter image description here"></p>
<h2 id="delete-a-connection">Delete a connection</h2>
<p><strong>7.</strong> Click on <strong>Delete</strong> option to delete the connection from database.</p>
<p><img src="https://raw.githubusercontent.com/sv18042016/fp1/eae5d23007893f45fcaab8db33c5a707e1a7911a/images/del_conn.png" alt="enter image description here"></p>
<h2 id="dialects-supported">Dialects supported</h2>
<p><img src="https://raw.githubusercontent.com/sv18042016/fp1/3bbaa9982fbbf193443bb882f359d2b1cf683390/images/dialects.png" alt="enter image description here"></p>

