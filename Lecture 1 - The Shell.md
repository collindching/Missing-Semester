# Lecture 1 - The Shell

Topics covered: Basic Bash commands, piping, and root user permissions

`date`

`echo hello`

`echo "Hello world"`

`echo $Path`: Shows all paths in machine where Shell will search for programs

Whenever you type the name of a program, Shell will look here.

`which echo`: Tells you which program Shell would use to run `echo`.

`pwd`: Prints current path

`cd`: Change directory

`ls`: List files in a directory

`.`: Current directory

`..`: Parent directory

`/`: Root directory

`cd ~`: Takes you to home directory

`cd -`: Takes you to directory you were previously in

`--help`: Prints out information about command

`mv`: Rename a file (takes old path and new path)

`cp`: Copy a file (path to copy from, path to copy to)

`rm`: Remove a file 

`rmdir`: Remove a directory, only if it's empty

`mkdir`: Create a new directory (escape space, or quote string)

`man`: Takes another program as argument, and takes you to the manual page - easier to navigate than --help

ctrl + L: Clears Shell

Input stream, output stream
- Default input = keyboard, default output = terminal
- Can be changed via `<` (rewire input) or `>` (rewire output)

`echo hello > hello.txt`: Construct file in current directory called hello.txt, write "hello" in it

`cat`: Prints contents of file (duplicates input to output

`cat < hello.txt > hello2.txt`: Input is hello.txt, output is hello2.txt

`>>`: Append, rather than just write

`|`: Pipe - take output of program to the left; make it the input of the program to the right

`tail -n[number]`: Print last n lines

Root user = administrative user
- User ID = 0
- Can do whatever it wants, has all privileges
- Usually don't operate as root user, since it's dangerous to system - use a program called sudo to get root user access rights
- Use `sudo` keyword; "do as super user"
- `#` means run as root
- `sudo su` turns terminal into root Shell
- `sudo tee` takes input and writes to file, as well as standard output (terminal)
- `echo 1060 | sudo tee brightness`

`open`

`chmod`