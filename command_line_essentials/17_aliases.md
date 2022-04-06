# Aliases

**Commands**

- `alias`: Allows you to create short names for commands.

One more trick for customizing the Shell, this one is called `aliases`. It's a way of making long shell command shorter, because what you really need in the shell was for the commands to be even shorter.

- `$ alias ll='ls -la'`

So, the way aliases work is to use the `alias` command to give a short name, such as `ll` to a longer command such as `ls -la`. After you create an alias, any time you type the short command, like `ll`, the shell will run the long command, `ls -la`. If you want to list all of the aliases that you have just run the alias command with no argument.

```console
$ alias
alias ll='ls -la'
```
Now, this command `ll`, will only last as long as this terminal window is open. If you want your aliases to be there every time you start your shell, well, put them in your `bash_profile`.
