smartdel
========

**Created for COMP 4262-001 at the University of Memphis**

This bash script should be placed in user's bin folder for global execution. <br>
Additionally, a 'smartdel_recycle' directory should be placed at the users home folder as the recycle bin. <br>

<Options: <br> 
-d (delete) <br>
-r (restore) <br>
(option omitted, behavior is identical to -r) <br>

<h2>move file(s) to recycle bin, supports wildcards</h2> 
smartdel -d filename <br>
smartdel filename <br>
smartdel -d file* <br>
smartdel file* <br>
smartdel file???? <br>

<h2>restore file(s) to the current directory</h2> 
smartdel -r filename <br>
smartdel -r 'file*' <br>


