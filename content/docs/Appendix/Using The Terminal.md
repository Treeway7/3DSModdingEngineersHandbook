---
title: "Using The Terminal"
weight: 1
# bookFlatSection: false
# bookToc: true
# bookHidden: false
# bookCollapseSection: false
# bookComments: false
# bookSearchExclude: false
---

# Using The Terminal

There are many different tools available at your disposal, some of which only have a command-line interface. You'll need to use a terminal to run certain programs.

{{< hint info >}}

A computer terminal lets you run apps with a *command-line interface* (CLI), as opposed to a graphical interface (GUI). Terminals let you use your computer by writing commands into a text box.

Many development tools are *command-line only,* and don't have a graphical interface (or GUI).

{{< /hint >}}

## Essential Commands

Here are a couple of essential commands you'll need on any OS.

{{< hint warning >}}

Some of these commands are different in Windows Command Prompt.

On Windows Powershell, these commands are *aliases* that correspond to longer Powershell commands, such as `Get-ChildItem` and `Set-Location`.

{{< /hint >}}


-----------

### `ls`

Lists your current directory.

```
/home/MyComputer> ls
Desktop   Documents   Downloads   Music   Pictures   Videos
```

You can also type a directory after `ls` to list that directory's files:

```
/home/MyComputer> ls Desktop/
'Deep Rock Galactic.lnk'   'Fallout New Vegas.lnk'   funny-waifu.png
lunatic-princess.mp3   project-stuff.txt   'Super Secret Stash'
```

-----------

### `cd`

Change directories.

```
/home/MyComputer> cd Desktop/
/home/MyComputer/Desktop>
```

-----------

## Folder Paths

These are important for navigating through files and executing programs.

### `..`

This is one directory up from your current path.

```
/home/MyComputer/Desktop> cd ..
/home/MyComputer/> cd ../..
/>
```

-----------

### `~`

This is a terminal shortcut that leads to your home directory.

```
/> cd ~
/home/MyComputer>
```

-----------

### `.`

This is the current directory's path. You can run apps located in the current folder with `./`

```
/home/MyComputer> ls .
Desktop   Documents   Downloads   Music   Pictures   Videos
/home/MyComputer> ./ctrtool --help
CTRTool v1.2.0 (C) jakcron
Built: 01:31:11 Apr  1 2023

Usage: ctrtool [options... ] <file>
Options:
  ...

/home/MyComputer>
```

{{< hint info >}}

Most applications have a `--help` menu.
If you need instructions, try adding this flag when you're running a program!

{{< /hint >}}

-----------

## File Manipulation

Move, copy and delete files.

### `mv`

Moves a file to a different directory, and/or renames a file in the current directory.

In this example, we move the file and rename it at the same time:

```
/home/MyComputer> ls Desktop/
'Deep Rock Galactic.lnk'   'Fallout New Vegas.lnk'   funny-waifu.png
lunatic-princess.mp3   project-stuff.txt   'Super Secret Stash'
/home/MyComputer> mv funny-waifu.png ~/Pictures/super-serious-person.png
/home/MyComputer> ls Pictures/
super-serious-person.png
```

-----------

### `cp`

Works just like `mv` but instead copies a file from one place to another. See above!

-----------

### `rm`

Removes a file from your drive.

{{< hint danger >}}

**Removing files this way permanently deletes them, and is IRREVERSIBLE!**

Be very careful when using this command.

{{< /hint >}}

Add the `-r` command line option to delete entire directories.

Also, `-f` lets you *force delete,* bypassing any delete confirmations and file locks.

```
/home/MyComputer/Desktop> ls
'Deep Rock Galactic.lnk'   'Fallout New Vegas.lnk'   lunatic-princess.mp3
project-stuff.txt   'Super Secret Stash'
/home/MyComputer/Desktop> rm "lunatic-princess.mp3"
/home/MyComputer/Desktop> rm "Super Secret Stash" -rf
/home/MyComputer/Desktop> ls
'Deep Rock Galactic.lnk'   'Fallout New Vegas.lnk'   project-stuff.txt
```

-----------

## Conclusion

There are many other built-in commands. Don't forget to Google if you need more information!
