[Basics](https://github.com/bregman-arie/devops-resources/blob/master/resources/linux.md)

Basic Command Line Commands:
1) pwd - prints the current working directory
2) cd - change directory
3) ls - List directories
4) touch - Make new file. Touch is also used to change timestamps on existing files and directories. Give it a try, do an ls -l on a file and note the timestamp, then touch that file and it will update the timestamp. 
5) file - In Linux, filenames aren’t required to represent the contents of the file. You can create a file called funny.gif that isn’t actually a GIF.
To find out what kind of file a file is, you can use the file command.
6) cat - To read a file. A simple command to use is the cat command, short for concatenate, it not only displays file contents but it can combine multiple files and show you the output of them.
7) less - If you are viewing text files larger than a simple output, less is more. The text is displayed in a paged manner, so you can navigate through a text file page by page. <br/>
Use the following command to navigate through less: <br/>
q - Used to quit out of less and go back to your shell. <br/>
Page up, Page down, Up and Down - Navigate using the arrow keys and page keys. <br/>
g - Moves to beginning of the text file. <br/>
G - Moves to the end of the text file. <br/>
/search - You can search for specific text inside the text document. Prefacing the words you want to search with / <br/>
h - If you need a little help about how to use less while you’re in less, use help. <br/>

8) history - In your shell, there is a history of the commands that you previously entered, you can actually look through these commands. This is quite useful when you want to find and run a command you used previously without actually typing it again.
9) cp - to copy a file. <br/>
   cp mycoolfile /home/pete/Documents/cooldocs. mycoolfile is the file you want to copy and /home/pete/Documents/cooldocs is where you are copying the file to.
10) mv - Used for moving files and also renaming them. mv oldfile newfile <br/>
    Or you can actually move a file to a different directory: <br/>
    $ mv file2 /home/pete/Documents
