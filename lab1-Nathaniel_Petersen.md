# Command "cd" - changes the current working directory
## No arguments example:
![Image](example1.jpg)

In the code example above, the current working directory is first set to `/Users/nathanielpetersen/lecture1`

The `cd` command with no arguments is then run.

There is no output indicating an error nor any output in general. 

However, checking our current working directory with the `pwd` command shows that our current working directory has been changed to our home directory. This shows that using the `cd` command with no arguments results in our current working directory being changed to our home directory.


## Path to a directory as argument example:

![Image](example2.jpg)

In the code example above, the current working directory is first set to `/Users/nathanielpetersen/lecture1`

The `cd` command with the directory `messages` supplied as an argument is then run. 

Once again, no output is provided, including any output indicating an error. 

We can see that the `cd` command worked by running the `pwd` command, which shows us that the current working directory has been switched from `/Users/nathanielpetersen/lecture1` to `/Users/nathanielpetersen/lecture1/messages`. This shows that using the `cd` command with a directory supplied as its argument results in the current working directory being switched to the newly supplied directory.

## Path to a file as argument example:

![Image](example3.jpg)

In the code example above, the current working directory is first set to `/Users/nathanielpetersen/lecture1`

The `cd` command with the file `Hello.java` supplied as an argument is then run. 

This time, an error message appears in the terminal, stating `Hello.java: Not a Directory`. As the error message suggests, this error occured because `cd` cannot change the current working directory to anything other than a directory, including java files.

# Command "ls" - lists out files in a directory
## No arguments example:
![Image](example4.jpg)

In the code example above, the current working directory is first set to `/Users/nathanielpetersen/lecture1`

The `ls` command with no arguments is then run. The terminal then outputs `Hello.class Hello.java README messages`, which is a list of all the files contained in `lecture1`. In this case, the `ls` command with no arguments simply lists out all the files stored in the current working directory, ie, `/Users/nathanielpetersen/lecture1`

There is no additional output to indicate that this behavior is an error.


## Path to a directory as argument example:
![Image](example5.jpg)

In the code example above, the current working directory is first set to `/Users/nathanielpetersen/lecture1`

The `ls` command with the path to a directory (`/Users/nathanielpetersen/lecture1/messages`) supplied as an argument is then run. The terminal then outputs `en-us.txt es-mx.txt zh-cn.txt`, which is a list of all the files contained in the directory `messages`. Similar to when no arguments are supplies, the `ls` command supplied with a directory will list out the files contained in that directory.

There is no additional output to indicate that this behavior is an error.


## Path to a file as argument example:
![Image](example6.jpg)

In the code example above, the current working directory is first set to `/Users/nathanielpetersen/lecture1`

To demonstrate the difference in output between running `ls` with no argument and `ls` with the path to a file, `ls` is then run with no arguments, supplying the expected output `Hello.class Hello.java README messages`.

The `ls` command with the path to a file (`/Users/nathanielpetersen/lecture/README`) supplied as an argument is then run. The terminal outputs `/Users/nathanielpetersen/lecture/README`, which is the same file path we gave as an input. Running the `ls` command again with the file `README` supplied directly return the output `README`. This suggests that running the ls command with the path to a file as a argument simply returns the given argument. This is likely because the only file stored in a non-directory file is itself.

There is no additional output to indicate that this bahavior is an error. However, I do find it interesting that the argument is returned as opposed to the file ultimately being referenced by the argument.

# Command "cat" - outputs the contents of a file
## No arguments example:
![Image](example7.jpg)

In the code example above, the current working directory is first set to `/Users/nathanielpetersen/lecture1`

The `cat` command with no arguments is then run. With no arguments, the `cat` command places the terminal into a mode where every key on the keyboard is logged to some collection of characters, such as the up arrow key being mapped to "^[[A".

This is probably not an error. While when no argument is provided the `cat` command obviously has no file to read the contents of, unlike an example we will see later, no error message is provided, the terminal is simply put into the key-logging mode, suggesting this may be an intended feature of `cat`. 

## Path to a directory as argument example:
![Image](example8.jpg)

In the code example above, the current working directory is first set to `/Users/nathanielpetersen/lecture1`

The `cat` command is then run with the directory `messages` as its argument.

With a path to a directory as the argument, `cat` returns an error message stating `cat: messages: Is a directory`. As the error message suggests, this error occured because `cat` reads the contents of a normal, non-directory file, and the supplied argument leads to a directory, which `cat` cannot read.

## Path to a file as argument example:
![Image](example9.jpg)

In the code example above, the current working directory is first set to `/Users/nathanielpetersen/lecture1`

The `cat` command is then run three times, each time using one of the files contained in `lecture1/messages` as shown in the `ls` command run right before as an argument. The first time, the file `en-us.txt` is supplied as an argument, and the output reads `Hello World!`. The second time, `es-mx.txt` is supplied, and the output reads `¡Hola Mundo!`. Lastly, the file `zh-cn.txt` is supplied, and the output reads `你好世界`. In all three cases, running `cat` with a file supplied as its argument resulted in the content of the file being output into the terminal.

There is no additional output to indicate that this behavior is an error.
