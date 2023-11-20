---
title: "Copy and moving directories"
datePublished: Mon Nov 20 2023 21:50:27 GMT+0000 (Coordinated Universal Time)
cuid: clp7fxjr300010al3amal12lh
slug: copy-and-moving-directories
tags: linux-commands

---

### copy command (cp)

**1) To Copy from File1 to File2 (File to File)**

* $cp source\_file destination\_file
    
* $cp file1 file2
    
* The total content of file1 will be copied to file2.
    
* If file2 is not already available, then this command will create that file.
    
* If file2 is already available and contains some data, then this data will be overwrite with file1 content.
    

**2) To Copy File to Directory:**

* $cp file1 file2 output
    
* file1 and file2 will be copied to output directory.
    
* Here we can specify any number of files, but the last argument should be a directory. output directory should be available already.
    

**3) To Copy all Files of One Directory to another Directory:**

* $cp dir1/\* dir2
    
* All files of dir1 will be copied to dir2
    
* But dir2 should be available already.
    

**4) To Copy Total Directory to another Directory:**

* $cp -r dir1 dir2
    

**5) To Copy Multiple Directories into a Directories:**

* $cp -r dir1 dir2 dir3 dir4 dir5
    
* dir1,dir2,dir3 and dir4 will be copied to dir5
    

### Moving and Renaming Directories:

Both moving and renaming activities can be performed by using single command: (mv)

**1) Renaming of files:**

* $mv oldname newname
    
* $file1.txt file2.txt
    
* file1.txt will be renamed to file2.txt
    

**2) Renaming of Directories:**

* $mv dir1 dir2
    
* dir1 will be renamed to dir2
    

**3) Moving files to directory:**

* $mv a.txt b.txt c.txt output
    
* a.txt,b.txt and c.txt will be moved to output directory.
    

**4) Moving all files from one directory to another directory:**

* $mv dir1/\* dir2
    
* All files of dir1 will be moved to dir2. After executing this command dir1 will become empty.
    

**5) Moving total directory to another directory:**

* $mv dir1 dir2
    
* If dir2 is already available then dir1 will be moved to dir2. If dir1 is not already available then dir1 will be renamed to dir2.
    

---

# working with files

### **1) Creation of Files:**

we can create files in the following ways

* cat command
    
* touch command
    
* by using editors like gedit,vi,nano etc.
    

**cat command**

```bash
$cat > file1.txt
```

* If file1.txt is not already available, then file1.txt will be created with our provided data.
    
* If file1.txt is already available with some content, then old data will be over written with our provided new data.
    
* Instead of overwriting, if we want append operation then we should use &gt;&gt; with cat command
    

```bash
$cat >> file1.txt
```

### 2) View the Content of the Files

We can view the content of the file by using the following commands

1. cat
    
2. tac
    
3. rev
    
4. head
    
5. tail
    
6. less
    
7. more
    

### **1\. View Content of the File by using cat Command:**

```bash
$cat < file1.txt Or $cat file1.txt --> to view the file content 
$cat -n file1.txt -->to display line numbers of the filecontent
$cat -b file1.txt --> to skip blank line numbers of the file content
$cat file1.txt file2.txt file3.txt --> to view multiple files content at a time
```

### **Various utilities of cat Command:**

**1) To create new file with some content**

$cat &gt; filename

**2) To append some extra data to existing file**

$cat &gt;&gt; filename

**3) To view the content of file**

$cat &lt; filename or $cat filename

**4) Copy content of one file to another file**

$cat input.txt &gt; output.txt

**5) To copy the content of multiple files to a single file**

$cat file1.txt file2.txt file3.txt &gt; file4.txt

**6) Merging/appending one file content to another file**

$cat file1.txt &gt;&gt; file2.txt

### **2\. tac Command:**

<mark>$tac file1.txt</mark>

* It is the reverse of cat command
    
* It will display file content in the reverse order of lines. i.e. first line will become the last line and the last line will become the first line.
    
* This is a vertical reversal.
    

### **3\. rev Command:**

<mark>$rev file1.txt</mark>

* rev means reverse.
    
* Here each line content will be reversed.
    
* It is a horizontal reversal.
    

### **4\. head Command:**

* We can use head command to view top few lines of content.
    

<mark>$head file1.txt</mark>

* It will display top 10 lines of file1.txt.
    

* 10 is the default value of number of lines.
    
    <mark>$head -n 30 file1.txt (Or) $head -30 file1.txt</mark>
    
* To display top 30 lines of the file.
    
* Instead of 30, we can specify any number
    
    <mark>$head -n -20 file1.txt</mark>
    
* To display all lines of file1.txt except last 20 lines.
    
    <mark>$head -c 100 file1.txt</mark>
    
* To display first 100 bytes of file content.
    

### **5\. tail Command:**

* We can use tail command to view few lines from bottom of the file.
    
* It is opposite to head command.
    

<mark>$tail file1.txt</mark>

* Last 10 lines will be displayed.
    

<mark>$tail -n 30 file1.txt (Or) tail -30 file1.txt (Or) tail -n -30 file1.txt</mark>

* It will display last 30 lines.
    

<mark>$tail -n +4 file1.txt</mark>

* It will display from 4th line to last line
    

<mark>$tail -c 200 file1.txt</mark>

It will display 200 bytes of content from bottom of the file

### 6\. more Command:

We can use more command to view file content page by page.

<mark>$more file1.txt</mark>

* It will display first page.
    
* Enter--&gt;To view next line
    
* Space Bar--&gt; To view next page
    
* q --&gt;To quit/exit
    

<mark>$more -d file1.txt</mark>

\-d option meant for providing details like

\--More--(5%)\[Press space to continue, 'q' to quit.\]

### 7\. less Command:

* By using more command, we can view file content page by page only in forward
    
    direction.
    
* If we want to move either in forward direction or in backward direction then we
    
    should go for less command
    
    <mark>less file1.txt</mark>
    
* It will display first page
    
* d --&gt;To go to next page.(d means down)
    
* b --&gt;To go to previous page. (b means backward)