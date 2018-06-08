# Comandos Básicos do Linux
Baseado neste [site](https://www.linuxtrainingacademy.com/linux-commands-cheat-sheet/).

______________________________________________________________________________________________________________________________


## To go up one level of the directory tree.  (Change into the parent directory.)
cd ..

## Go to the $HOME directory
cd

## Change to the /etc directory
cd /etc

_____________________________________________________________________________________________________________________________

## List all files in a long listing (detailed) format
ls -al

## Display the present working directory
pwd

## Create a directory
mkdir directory

## Remove (delete) file
rm file

## Remove the directory and its contents recursively
rm -r directory

## Force removal of file without prompting for confirmation
rm -f file

## Forcefully remove directory recursively
rm -rf directory

## Copy file1 to file2
cp file1 file2

## Copy source_directory recursively to destination. If destination exists, copy source_directory into destination, otherwise create destination with the contents of source_directory.
cp -r source_directory destination

## Rename or move file1 to file2. If file2 is an existing directory, move file1 into directory file2
mv file1 file2

## Create symbolic link to linkname
ln -s /path/to/file linkname

## Create an empty file or update the access and modification times of file.
touch file

## View the contents of file
cat file

## Browse through a text file
less file

## Display the first 10 lines of file
head file

## Display the last 10 lines of file
tail file

______________________________________________________________________________________________________________________________

## File Permissions
U  | G  | W   | Example
---|----|-----|----------------------
rwx| rwx| rwx | chmod 777 filename
rwx| rwx| r-x | chmod 775 filename
rwx| r-x| r-x | chmod 755 filename
rw-| rw-| r-- | chmod 664 filename
rw-| r--| r-- | chmod 644 filename

NOTE: Use 777 sparingly!

LEGENDA|
---------|
U = User|  
G = Group|
W = World|
r = Read|
x = execute|
w = write|
\- = no access |

______________________________________________________________________________________________________________________________

## Search for pattern in file
grep pattern file

## Search recursively for pattern in directory
grep -r pattern directory

______________________________________________________________________________________________________________________________

## Connect to host as user
ssh user@host

______________________________________________________________________________________________________________________________

## Secure copy file.txt to the /tmp folder on server
scp file.txt server:/tmp

## Copy *.html files from server to the local /tmp folder.
scp server:/var/www/*.html /tmp

## Copy all files and directories recursively from server to the current system's /tmp folder.
scp -r server:/var/www /tmp

______________________________________________________________________________________________________________________________

## Standard Input (stdin)
cat

## Standard Output (stdout)
echo Sent to the terminal through standard output

## Stream Redirection
Overwrite|
---------|
\> - standard output|  
< - standard input|
    
    
Append|
---------|
\>> - standard output|  
<< - standard input|

## Pipes
ls | less

______________________________________________________________________________________________________________________________
