<h1>Bandit Level 1</h1>

<h2>Objective</h2>
<p>
The password for the next level is stored in a file called <code>-</code> located in the home directory.
</p>

<hr>

<h2>How It Was Solved</h2>
<p>
While trying to read the file using the <code>cat</code> command, I realized that the filename was only a single dash (<code>-</code>). The OverTheWire Bandit homepage has a section called <b>Helpful Reading Material</b>, which suggested searching for "dashed filename." After reading about it, I learned that files beginning with a dash are treated as command-line options, so they must be referenced differently. I used the correct syntax to successfully display the contents of the file and obtain the password.
</p>

<hr>

<h2>Commands Used</h2>

<pre><code>cat ./-</code></pre>

<hr>

<h2>Key Takeaways &amp; Lessons Learned</h2>

<ul>
    <li>Files whose names begin with a dash (<code>-</code>) are interpreted as command-line options.</li>
    <li>Prefixing the filename with <code>./</code> tells Linux to treat it as a file in the current directory instead of an option.</li>
</ul>

<hr>

<h2>Picture of Successful Working Image</h2>

<img src="images/bandit1.png" alt="Bandit Level 1 Solution" width="900">

<hr>

<h2>Password Obtained Successfully and Used to Access the Next Level</h2>
