smartdel
========

This bash script should be placed in user's bin folder for global execution. <br>
Additionally, a 'smardel_recycle' directory should be placed at the users home folder as the recycle bin. <br>

<Options: <br> 
-d (delete) <br>
-r (restore) <br>
(option omitted, behavior is identical to -r) <br>

Examples of smartdel execution include: 

<h2>move file(s) to recycle bin, supports wildcards</h2> <br>
smartdel -d filename <br>
smartdel filename <br>
smartdel -d file* <br>
smartdel file* <br>
smartdel file???? <br>

<h2>restore file(s) to the current dictory, wilcards must be string literal</h2> 
smartdel -r filename <br>
smartdel -r 'file*' <br>


