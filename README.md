smartdel
========

Created for COMP 4262-001 at the University of Memphis, Fall 2014<br>
Instructor: Dr. Zhou Lu <br>
Project by Dr. Zhuo Lu <br>
Code by Keenan Diggs, 2014 <br>
Documentation by Keenan Diggs, 2014

<h2>Description</h2>
*This bash script should be placed in user's bin folder for global execution.* <br>

<p> 
smartdel is a linux file-manipulation utility and extension of the mv command. The code is contained in a single shell script. It is powerful and robust, capable of restoring all files in a recycle bin directory to the locations they were initially deleted from, while accounting for name collisions.
</p>

<p> 
smartdel initializes a 'smartdel_recycle' recycle bin directory as a child of the user's home directory and a '.table.txt' file inside the bin.
</p>

<p> 
Upon file deletion, files are moved to the recycle bin and the filename and filepath 2-tuples are stored in the .table.txt file, where they can later be recovered and used. In the bin, files are stored in the format filename_version, where version is an integer.
</p>

<p> 
Upon file recovery, the user specifies whether the selected files are moved to the present working directory or to the directory from which they were originally deleted from.
</p>

<p>
In addition, smartdel supports wilcard characters '*' and '?', but for restoring, parameters passed to smartdel with them must be contained in single or double quotes.
</p>

<p>
Finally, smartdel supports the deletion and restoration of identical filenames. If files with identical names are deleted from separate directories, smartdel can restore them simultaneously. However, if the same filename is deleted from the same directory 2 or more times, the user will decide which version of the file to restore. In this event, smartdel will provide a numbered list of file descriptions, from which the uses chooses one. The file descriptions contain the time last edited, filename_version as stored in the recycle bin, and directory from which the file was originally deleted from.
</p>

<h2>How to Use smartdel</h2>
Options: <br>
-d (delete) <br>
-r (restore) <br>
-o (smart restore) <br>
-s (smart restore simultaneous files) <br>
-c (permanently delete all files in recycle bin) <br>
(option omitted, behavior is identical to -d) 

<h3>-d</h3>
<p>
The delete option allows the user to send files, or file patterns if wildcards are used, from the specified directory to the recycle bin. The file is moved with a new name of the form oldfilename_version. If no option is specified and a paramenter is immediately input, smartdel behaves as though -d has been specified. 'smartdel -d filename' is equivalent to 'smartdel filename'.
</p>

<h3>-r</h3>
<p>
The restore option allows the user to restore files from the smartdel_recycle bin to the present working directory. Wildcards are supported, but such patterns must be passed in with single or double quotes. If multiple files of the same filename have been deleted and are residing in the recycle bin, the user will have to specify which file to restore by inputting an integer from the keyboard and pressing Enter.
</p>

<h3>-o</h3>
<p>
The restore option allows the user to restore files from the smartdel_recycle bin to the present working
directory. Wildcards are supported, but such patterns must be passed in with single or double quotes. If
multiple files of the same filename have been deleted and are residing in the recycle bin, the user will
have to specify which file to restore by inputting an integer from the keyboard and pressing Enter based
on a numbered list of file descriptions.
</p>

<h3>-s</h3>
<p>
The smart restore (simultaneous) option allows the user to restore files from the smartdel_recycle bin to the directory in which they were smartdeleted from. If multiple files of the same name with different source
directories are in the recycle bin, smartdel will restore them all simultaneously. Wildcard characters are
supported, but such patterns must be passed in with single or double quotes.
</p>

<h3>-c</h3>
<p>
The clear bin option allows the user to permanently delete all files in the recycle bin and reset the table.
It is invoked simply as 'smartdel -c'
</p>

<h2>Utility Call Examples</h2>
smartdel is of the form: smartdel [option] [parameters] <br><br>
smartdel -d filename, or equivalently: smartdel filename <br>
smartdel -d /home/path/to/filename <br>
smartdel -d ../filename <br>
smartdel -d ~/Documents/path/to/filename <br>
smartdel -d subdir/grandchild/filename <br>
smartdel -d filename1 filename2 filename3 <br><br>

smartdel -r filename1 <br>
smartdel -r filename1 filename2 filename3 path/to/filename4 <br>
smartdel -r 'filena*' <br>
smartdel -r 'fil?name?' <br><br>

smartdel -o filename1 <br>
smartdel -o 'fi*name' <br>
smartdel -o '?ilename2' <br>
smartdel -o filename1 filename2 filename3

smartdel -s filename <br>
smartdel -s '*'

smartdel -c
