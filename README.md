smartdel
========

This bash script should be placed in user's bin folder for global execution.
Additionally, a 'smardel_recycle' directory should be placed at the users home folder as the recycle bin.

Options: -d (delete)
         -r (restore)
            (option omitted, behavior is identical to -r)

Examples of smartdel execution include:

# move file(s) to recycle bin, supports wildcards
smartdel -d filename <br>
smartdel filename
smartdel -d file*
smartdel file*
smartdel file????

# restore file(s) to the current dictory, wilcards must be string literal 
smartdel -r filename
smartdel -r 'file*'


