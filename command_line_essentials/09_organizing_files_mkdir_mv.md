# Organizing Files (mkdir, mv)

With the Shell, you can use commands to organize your files into directories, move files, copy or remove the files.


## mkdir

```console
(base) ludo /00_basic_command_line  $  ls
01_intro_bash.md             03_organizing_files.md
02_navigating_directories.md images
```

I have a bunch of *markdown* files in the current directory as `.md` files, so I'll **make a directory** called `markdown` to move them into.

- `$ mkdir markdown`

```console
(base) ludo /00_basic_command_line  $  ls
01_intro_bash.md             03_organizing_files.md       markdown
02_navigating_directories.md images
```

## mv

Next, I'll move the `.md` files into that directory. The command for **moving things** is `mv`, which is short for **move**.

`$ mv ./*.md ./markdown`

I have to tell two things:

- `./*.md`: first **the things that I want to move**, in this case all the markdown files in the current directory.
- `./markdown`: second **where do I want to move them into**.

```console
(base) ludo /00_basic_command_line  $  ls
images   markdown
(base) ludo /00_basic_command_line  $  ls markdown
01_intro_bash.md             02_navigating_directories.md 03_organizing_files.md
```

Now, if I `ls` in the markdown directory we can actually see that the files have been moved.

Let's say we want to move the files back.

```console
(base) ludo /00_basic_command_line  $  cd markdown; mv ./*.md ..
(base) ludo /markdown  $  ls
(base) ludo /markdown  $  cd ..
(base) ludo /00_basic_command_line  $  ls
01_intro_bash.md             03_organizing_files.md       markdown
02_navigating_directories.md images
```

Or we can stay in the same directory.

```console
(base) ludo /00_basic_command_line  $  mv ./markdown/*.md .
(base) ludo /00_basic_command_line  $  ls
01_intro_bash.md             03_organizing_files.md       markdown
02_navigating_directories.md images
```

Or we can say move all the content of that directory.

```console
(base) ludo /00_basic_command_line  $  mv ./markdown/* .
(base) ludo /00_basic_command_line  $  ls
01_intro_bash.md             03_organizing_files.md       markdown
02_navigating_directories.md images
```

## Commands
- `mkdir`: Creates directories.
- `mv`: Move files from a directory to another.

### Notes

By the way, when you quote something in the shell, you always use straight quotes. This is what you'll get if you type into a terminal window. However, if you copy and paste from a web page or document, you should be really careful to make sure that it hasn't accidentally been written with “curly quotes”. Curly quotes will not work in the shell.

Single quotes and double quotes do slightly different things in the shell. If you're unsure which to use, go for single quotes.
