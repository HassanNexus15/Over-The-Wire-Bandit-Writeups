<h1>Bandit Level 2</h1>

<h2>Objective</h2>
<p>
The password for the next level is stored in a file called
<code>--spaces in this filename--</code> located in the home directory.
</p>

<hr>

<h2>How It Was Solved</h2>

<ol>
    <li>I first searched for <b>"spaces in filename"</b>, as suggested in the <b>Helpful Reading</b> section on the OverTheWire Bandit website.</li>

    <li>After reading the documentation, I experimented with a few different command combinations on my own.</li>

    <li>I learned that filenames containing spaces must either be enclosed in quotation marks or have each space escaped using a backslash (<code>\</code>).</li>

    <li>Using the correct syntax, I successfully displayed the contents of the file and obtained the password.</li>
</ol>

<hr>

<h2>Commands Used</h2>

<pre><code>cat "./--spaces in this filename--"</code></pre>

<p><b>OR</b></p>

<pre><code>cat ./--spaces\ in\ this\ filename--</code></pre>

<hr>

<h2>Key Takeaways &amp; Lessons Learned</h2>

<ul>
    <li>Filenames containing spaces are treated as multiple arguments by the shell.</li>

    <li>Spaces can be escaped using a backslash (<code>\</code>) or the entire filename can be enclosed in quotation marks.</li>

    <li>Reading the documentation and experimenting with different commands helped me understand how Linux interprets filenames.</li>
</ul>


<h2>Password Obtained Successfully and Used to Access the Next Level</h2>

<p><i>(Password intentionally omitted.)</i></p>
