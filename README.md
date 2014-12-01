smartdel
========
*This bash script should be placed in user's bin folder for global execution.* <br>

Created for COMP 4262-001 at the University of Memphis<br>
Instructor: Dr. Zhou Lu <br>
Project by Dr. Zhuo Lu

<h2>Description</h2>
<p> smartdel is a linux file-manipulation utility and extension of the mv command. The code is contained entirely in one shell script
</p>

<p> smartdel initializes a 'smartdel_recycle' recycle bin directory as the user's home directory and a '.table.txt' file inside the bin 
</p>

<p> Upon file deletion, files are moved to the recycle bin and the filename and filepath 2-tuples are stored in the .table.txt file, where they can later be recovered and used
</p>

<p> Upon file recovery, the user specifies whether the selected files are moved to the present working directory or to the directory from which they were originally deleted from
</p>

<h2>How to Use smartdel</h2>
<Options: <br> 
-d (delete) <br>
-r (restore) <br>
-o (smart restore) <br>
-f (delete and forget) <br>
(option omitted, behavior is identical to -d) <br>


<h3>-d</h3> 
<h3></h3>
<h3></h3>
<h3></h3>

<h2>restore file(s) to the current directory</h2> 
smartdel -r filename <br>
smartdel -r 'file*' <br>


