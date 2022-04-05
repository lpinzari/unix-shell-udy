# Current Working Directory (pwd)

Sometimes you will get lost in many directories, with this command you can see where you are.

Depending on your system, the *shell* prompt might or might not tell you **what directory you're in**, but there is a command that will always tell you, the `pwd` command that stands for **Printing Working Directory**.

```console
(base) ludo /Documents  $  pwd
/Users/ludovicopinzari/Documents
```

`pwd = Print Working Directory`

The **working Directory** is another word for whatever directory the *shell* **is currently looking at**. It's the default directory for commands like `ls`. And it's the default place that shell commands will look for data files.

- **/** Users **/** ludovicopinzari **/** Documents

You'll notice that the names of directories are separated by slashes. The Unix system uses the **forward** slash, not the backslash, **to separate the names of directories**.

Forward slash `/` is the same one you've seen in URLs on the web.

**Path**: `/Users/ludovicopinzari/Documents`

The whole string, **composed of several directories names separated by slashes**, is called a **Path**.

There are a few special directories names.

- `..`: it means the **Parent Directory** of the directory that a specific directory is inside.
- `.`: it means the **current directory**.
- `~`: it means the **home directory**.

Clearly the command `$ ls .` is equivalent to `$ ls`. And the *shell* also has a shortcut, the `~`, which stands for **my home directory**.

```console
(base) ludo /Documents  $  ls ~
Applications         Library              Projects
Desktop              Movies               Public
Documents            Music                RStudio-1.3.1093.dmg
Downloads            OneDrive             bin
GitHub               Pictures
```

Like regardless of what directory your CD'd into, `ls ~` will list your home directory.
