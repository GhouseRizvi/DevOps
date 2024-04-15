Archiving in linux is a process of  saving files and directories to an archive file. This can be done on individual files or entire directories, depending on the requirements. The archiving utility used for this task will depend on the Linux distribution being employed.

to archive a file , you need to have the necessary permissions. 

tar  -czvf /path/to/archive.tar.gz /path/of/file1 /path/of/directory2

-c : create a new tarball archive
-z : gzip compression enabled
-v : verbosely list files processed (show name)
-f : use archive file or device ARCHIVE (if not specified, it will be taken from stdin)

To add files into an existing .tgz file:

tar --append -f /path/to/existing_archive.tgz /path/of/newfile

--append : append to an existing archive rather than creating a new one 

To untar a  .tgz file:

tar xzvf /path/to/archive.tar.gz
-x : extract files 
-z :gunzip before processing
-v : verbose 
-f : name of archive file

You can also specify multiple paths by separating them with spaces. For example:

tar cf /tmp/foo.tar /etc/passwd /etc/group 
The command above creates foo.tar and includes both passwd and group in that tar file.

How to zip a directory in linux?
zip -r /pathe/name.zip  /pathe/dirname  
-r : is used to include directories and their contents in the zip file 

Unzipping a zip file
unzip filename.zip
