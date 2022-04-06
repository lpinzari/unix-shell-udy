# Removing Files or Directories (rm, rmdir)

With the Shell, you can use commands to remove files or directories.

## Commands
- `rm`: **Delete files**.
- `rmdir`: **Delete directories**.


### Removing Files (rm)

The Shell command for **deleting files** is `rm`, which is short for **remove**

`rm -> remove`

`rm` works the same as you'd probably expect from other Shell commands, you just give it the name of the file, or the names of the files that you want to remove.

- `$ rm sillyFile.txt`

```console
(base) ludo /exercises  $  touch sillyFile.txt
(base) ludo /exercises  $  ls
sillyFile.txt
(base) ludo /exercises  $  rm sillyFile.txt
(base) ludo /exercises  $  ls
(base) ludo /exercises  $
```

:warning: **Safety Warning** :warning:

Now, I've got to give you a safety warning. In your GUI, you've probably got a trash can or *recycle bin*, where files go when you want to get rid of them, but you can take them back out if you change your mind.

The `rm` command **does not work like this**. **It just remove the files**. If you want a little more warning maybe you're afraid you might remove a valuable file by mistake, well you can use the option `-i`. The `i` is for **interactive**. which will prompt you for every file it's going to remove.

- `$ rm -i valuableFile.txt`

```console
(base) ludo /exercises  $  rm -i valuableFile.txt
remove valuableFile.txt? no
(base) ludo /exercises  $  ls
valuableFile.txt
(base) ludo /exercises  $  rm -i valuableFile.txt
remove valuableFile.txt? yes
(base) ludo /exercises  $  ls
(base) ludo /exercises  $
```

To **delete multiple files at once**, use the `rm` command followed by the file names separated by space.

- `$ rm filename1 filename2 filename3`

You can also use a **wildcard** (`*`) and **regular expansions to match multiple files**. For example, to remove all `.pdf` files in the current directory, use the following command:

- `$ rm *.pdf`

When using regular expansions, first list the files with the ls command so that you can see what files will be deleted before running the rm command.

To **remove files without prompting, even if the files are write-protected**, pass the `-f` (force) option to the rm command:

- `$ rm -f filename(s)`

You **can also combine** `rm` **options**. For example, to remove all .txt files in the current directory without a prompt in verbose mode, use the following command:

- `$ rm -fv *.txt`


## Removing Directories (rmdir)

Now, for directories, there's a different command, which is `rmdir` for **remove directory**.

```console
base) ludo /exercises  $  mkdir terribleDirectory
(base) ludo /exercises  $  ls
terribleDirectory
(base) ludo /exercises  $  rm terribleDirectory
```

- `$ rmdir terribleDirectory`
- `$ rm -d terribleDirectory`

**To remove an empty directory**, use either `rmdir` or `rm -d` followed by the directory name.

Now, let's delete the directory and all the files within the directory.

```console
ase) ludo /exercises  $  mkdir terribleDirectory
(base) ludo /exercises  $  ls
terribleDirectory
(base) ludo /exercises  $  cd terribleDirectory/
(base) ludo /terribleDirectory  $  touch file1.txt
(base) ludo /terribleDirectory  $  cd ..
(base) ludo /exercises  $  ls
terribleDirectory
(base) ludo /exercises  $  rmdir terribleDirectory/
rmdir: terribleDirectory/: Directory not empty
```

We see that the `rmdir` commands does not work.

```console
(base) ludo /exercises  $  rmdir terribleDirectory/
rmdir: terribleDirectory/: Directory not empty
(base) ludo /exercises  $  rm -r terribleDirectory/
(base) ludo /exercises  $  ls
(base) ludo /exercises  $
```

To **remove non-empty directories and all the files within them**, use the `rm` command with the `-r` (recursive) option:

- `rm -r dirname`

If a directory or a file within the directory is write-protected, you will be prompted to confirm the deletion.

To **remove non-empty directories and all the files without being prompted**, use `rm` with the `-r` (recursive) and `-f` options:

- `rm -rf dirname`

To **remove multiple directories at once**, use the `rm -r` command followed by the directory names separated by space.

- `rm -r dirname1 dirname2 dirname3`

Same as with files, you can also use a wildcard (`*`) and regular expansions to match multiple directories.
