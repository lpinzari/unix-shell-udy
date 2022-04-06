# Shell and environment variables

The **Shell** is actually a little programming language. Just like *JS* or Python, it has **variables**. They look like a little different though.

`$ numbers='one two three'`

In the **shell**, whenever you create or modify a variable, you just give it a name and an equal sign followed by the value that you want it to have. Note that **you can't put any spaces around the equal sign**.

```console
$ echo $numbers
one two three
```

Then when you want to refer to the variable, you put a dollar sign `$` in front of its name. But there are actually two different kinds of variables.

## internal variables

```console
$ echo $LINES $COLUMNS
25 x 104
```

The `LINES` and `COLUMNS` variables are those kind that are just **internal** to the shell program itself. So, if we open another terminal window with different sizes then the values of those variables will be different.

## environment variables

The other kind of variables is called an **environment variable**.

```console
$ echo $PATH
/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin
```

Environment variables are **shared with programs that you run from within the Shell**. One environment variable  that's really important is the `PATH` variable.

The `PATH` variable tells your system **Where your program files are**. So, when you type a command, such as `ls`, it can find the `ls` program. The `ls` program in my system is in `/bin/ls`. So in the `/bin` directory. And the `/bin` directory is in my `PATH` variable.

The directories in the `PATH` variable are separated by colons **:**

So the directories in my `PATH` variable are:

`/usr/local/bin`**:**`/usr/bin`**:**`/bin`**:**`/usr/sbin`**:**`/sbin`

- `/usr/local/bin`
- `/usr/bin`
- `/bin`
- `/usr/sbin`
- `/sbin`

Whenever we run a command in the Terminal, the Shell searches from the start, with the first directory: `/usr/local/bin`. If the first directory doesn't contain the program file then the shell moves to the next directory `/usr/bin`, and so on.. That's how the shell is able to find the `ls` command when I want to run it.

You'll sometimes see instructions telling you to **add a directory** to your `PATH`, so that programs in it can be found.

To add a directory to the end of your `PATH` variable:

```console
$ PATH=$PATH:/new/dir/here
```

But if you do it like right at the shall prompt, that change will only last until you close the Shell.

We'll take a look at where you do it if you want to keep that change next.
