smartdel
========

This bash script should be placed in user's bin folder for global execution. <br>
Additionally, a 'smardel_recycle' directory should be placed at the users home folder as the recycle bin. <br>

#Options: <br> 
-d (delete) <br>
-r (restore) <br>
(option omitted, behavior is identical to -r) <br>

Examples of smartdel execution include: 

//move file(s) to recycle bin, supports wildcards
smartdel -d filename <br>
smartdel filename <br>
smartdel -d file* <br>
smartdel file* <br>
smartdel file???? <br>

//restore file(s) to the current dictory, wilcards must be string literal 
smartdel -r filename <br>
smartdel -r 'file*' <br>


