# First Command

Open the Terminal program on your computer.

```console
Last login: Tue Apr  5 12:44:19 on ttys002
Welcome master to the terminal
(base) ludo /~  $
```

Inside the Terminal window, we can see a little message on the top, and a cursor.

Now, this message `(base) ludo/~ $` is the Shell prompt. It usually displays some information about the computer you're logged into. Exactly, what message you see here will depend on your system. Later on, we'll see how to customize it.

If you type something in at the Shell prompt and press enter or `return` button on the keyboard, the **shell** will *try to run whatever you typed as a command*.

```console
(base) ludo /~  $  echo Hello, shello!
Hello, shello!
(base) ludo /~  $
```

The `echo` command is how we get the Shell to **print messages** back to us.

```console
(base) ludo /~  $  echo Hello, shello!!
echo Hello, shelloecho Hello, shello!
Hello, shelloecho Hello, shello!
```

What happen if we try `Hello, shello` followed by two exclamation marks. That's weird.

The point being, there are some characters that have a special meaning to the Shell. The exclamation mark is one of them.

```console
(base) ludo /~  $  echo 'Hello, shello!!'
Hello, shello!!
```

if you're ever typing something into the Shell and it seems to be treating what you're saying in a weird way, all you usually need to do is to put single quotes around it.
