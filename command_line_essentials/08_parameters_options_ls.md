# Parameters and options (ls -l)

**Use parameters and options in your commands**: Some commands have parameters or options to help you get more information or change the default behavior of those commands.

You've seen how many *shell* commands can be given the name of a file or a directory, like `ls` and `cd`. But that's not the only thing you can tell a *shell* command. Many of them also support **options**, **flags** or **parameters**.

## ls -l

```console
(base) ludo /00_basic_command_line  $  ls -l
total 24
-rw-r--r--@ 1 ludovicopinzari  staff  1254 18 Sep  2020 01_intro_bash.md
-rw-r--r--@ 1 ludovicopinzari  staff  3101 18 Sep  2020 02_navigating_directories.md
-rw-r--r--@ 1 ludovicopinzari  staff    24  2 Dec  2020 03_organizing_files.md
drwxr-xr-x  2 ludovicopinzari  staff    64 18 Sep  2020 images
(base) ludo /00_basic_command_line  $  ls -l images
```

The `-l` is an option to `ls` command. You can also use it along with the name of a directory. `ls -l images`. and what it does is **to print a longer more detailed listing of files**. The `l` is for **long**.

- `l = Long`

## pattern

The Shell let's you match filenames with a **pattern**. Let's say you want to list all the markdown files in your current directory.

`$ ls -l ./*.md`

```console
(base) ludo /00_basic_command_line  $  ls -l ./*.md
-rw-r--r--@ 1 ludovicopinzari  staff  1254 18 Sep  2020 ./01_intro_bash.md
-rw-r--r--@ 1 ludovicopinzari  staff  3101 18 Sep  2020 ./02_navigating_directories.md
-rw-r--r--@ 1 ludovicopinzari  staff    24  2 Dec  2020 ./03_organizing_files.md
```

The way to do this is with a `*`. The Shell turns the `*` into a list of all of the files whose names match that pattern `.md`. In this case, **that's all of the files whose file names end in** `.md`.

Which pieces of information can you find out from `ls -l`? You may want to do some research to answer this question; use your favorite search engine.

- The name of each listed file or directory.
- The date and time that file was modified.
- The size of a file, in byte

If you wanted to list **all the files whose names start with the word** `bear`, how would you do it?

- `ls bear*`
