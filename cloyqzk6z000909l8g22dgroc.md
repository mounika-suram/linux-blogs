---
title: "Basic Commands Of Linux"
datePublished: Tue Nov 14 2023 19:50:01 GMT+0000 (Coordinated Universal Time)
cuid: cloyqzk6z000909l8g22dgroc
slug: basic-commands-of-linux
tags: basic-linux-commands

---

```bash
$pwd -->ptrint working directory
$ls -->list out all files and directories
$mkdir -->create directories
$cd -->change directory
$touch -->to cteate a file
$rmdir -->remove directory
$rm -->remove file
$cal -->display current month calander
$date -->display current date and time
$help -->diplay list of commands
$hello -->display breif system information
$clear -->clear terminal
$exit -->logout session
```

### FILE SYSTEM NAVIGATION COMMANDS:

```bash
Every directory contains implicitly contains 2 directories :
. and ..
. -->represents current directory
.. -->represents parent directory

$cd. -->changes to current directory 
$cd.. -->changes to parent directory
$cd --> If we are not passing any argument,Then changes to user home directory
$cd~ -->changes user home directory
$cd- -->changes to previous working directory
```

## ls, date and cal commands

### ls command:

ls command is used to listout all files and directories present in the given directory.

```bash
$ls -->to display all files and directories according to alphabetical order of names
$ls -r -->to display all files and directories in reverse of alphabetical order
$ls | more -->to display content line by line
$ls | pg --> to display content page by page
$ls -l --> to display long listing of files
$ls -t -->to display all files based on last modified date and time
$ls -rt -->to display all files based on reverse of last modified date and time
$ls -a -->to display all files including hidden files. Here . and .. also will be displayed
$ls -A -->to display all files including hidden files except . and ..
$ls -F -->to display all files by type
$ls -f -->to disable colors
$ls -i -->to disply all files including inode number
$ls -R -->it will list all files and directories including sub directory contents also. By default ls 
will display only direct contents but not sub directory contents
$ls -s -->the number of blocks used by file will be displayed
$ls -h -->display in human readable format
```

### date command:

We can use date command to display date and time of the system.

```bash
$date +%D -->to display only date in the form: mm/dd/yy
$date +%T -->to display only time in the form: hh:mm:ss
$date +%d -->to display only day value
$date +%m -->to display only month value
$date +%y -->to display only year value in yy form
$date +%Y-->to display only year value in yyyy form.
$date +%H -->to display only Hours value (in 24 hours scale format)
$date +%M -->to display only Minutes value
$date +%S -->to display only Seconds value
```

### cal command:

```bash
$cal -->to display current month calendar
$cal 2020 -->to display total year calendar
$cal 1 -->to display 1st year calendar
$cal 9999 -->to display 9999th year calendar
$cal 08 2023 -->to display august 2023 calendar
```

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text"><code>cal command : it can support only for the years 1 to 9999</code></div>
</div>