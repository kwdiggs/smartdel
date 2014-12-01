smartdel
========

Created for COMP 4262-001 at the University of Memphis<br>
Instructor: Dr. Zhou Lu <br>
Project by Dr. Zhuo Lu <br>
Code by Keenan Diggs 2014

<h2>Description</h2>
*This bash script should be placed in user's bin folder for global execution.* <br>

<p> 
smartdel is a linux file-manipulation utility and extension of the mv command. The code is contained in a single shell script.
</p>

<p> 
smartdel initializes a 'smartdel_recycle' recycle bin directory as a child of the user's home directory and a '.table.txt' file inside the bin.
</p>

<p> 
Upon file deletion, files are moved to the recycle bin and the filename and filepath 2-tuples are stored in the .table.txt file, where they can later be recovered and used. Unless the delete and forget option is used, in which case the file is deleted permanently. In the bin, files are stored in the format filename_version, where version is an integer.
</p>

<p> 
Upon file recovery, the user specifies whether the selected files are moved to the present working directory or to the directory from which they were originally deleted from.
</p>

<p>
In addition, smartdel supports wilcard characters '*' and '?', but for restoring, parameters passed to smartdel with them must be contained in single or double quotes.
</p>

<p>
Finally, smartdel supports the deletion and restoration of identical filenames. If files with identical names are deleted from separate directories, smartdel can restore them simultaneously. However, if the same filename is deleted from the same directory 2 or more times, the user will decide which file to restore. In this event, smartdel will provide a numbered list of file descriptions, from which the uses chooses 1. The file descriptions contain the time last edited, filename_version as stored in the recycle bin, and directory from which the file was originally deleted from. Listing the original directory may seems useless, but it is useful when the user wants to restore a file to the present working directory only.
</p>

<h2>How to Use smartdel</h2>
Options:
-d (delete) <br>
-f (delete and forget) <br>
-r (restore) <br>
-o (smart restore) <br>
(option omitted, behavior is identical to -d) 

<h3>-d</h3>
<p>
The delete option allows the user to send files, or file patterns if wildcards are used, from the specified directory to the recycle bin. The file is moved with a new name of the form oldfilename_version. 
</p>

<h3>-f</h3>
<p>

</p>

<h3>-r</h3>
<p>

</p>

<h3>-o</h3>
<p>

</p>

<h3>Additional Examples</h3>
smartdel is of the form: smartdel [option] [parameters] <br><br>
smartdel -d filename, or equivalently: smartdel filename
smartdel -d /home/path/to/filename <br>
smartdel -d ~/Documents/path/to/filename <br>
smartdel -d subdir/grandchild/filename <br><br>
smartdel -d filename1 filename2 filename3

smartdel -f filename <br>
smartdel -f path/with/whatever/variations/you/want/to/filename <br><br>

smartdel -r filename1
smartdel -r filename1 filename2 filename3 path/to/filename4 <br>
smartdel -r 'filena*' <br>
smartdel -r 'fil?name?' <br><br>

smartdel -o filename1 <br>
smartdel -o 'fi*name' <br>
smartdel -o '?ilename2' <br>
smartdel -o filename1 filename2 filename3





