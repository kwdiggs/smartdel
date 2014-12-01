smartdel
========
*This bash script should be placed in user's bin folder for global execution.* <br>

Created for COMP 4262-001 at the University of Memphis<br>
Instructor: Dr. Zhou Lu <br>
Project by Dr. Zhuo Lu

<h2>Description</h2>
<p> smartdel is a linux file-tree utility and extension of the mv command. The code is contained entirely in one shell     script
</p>

<h2>How to Use smartdel</h2>
<Options: <br> 
-d (delete) <br>
-r (restore) <br>
(option omitted, behavior is identical to -r) <br>


<h3>move file(s) to recycle bin, supports wildcards</h3> 
smartdel -d filename <br>
smartdel filename <br>
smartdel -d filena* <br>
smartdel filena* <br>
smartdel file???? <br>

<h2>restore file(s) to the current directory</h2> 
smartdel -r filename <br>
smartdel -r 'file*' <br>


