---
title: "Comparing files"
datePublished: Wed Nov 29 2023 21:55:35 GMT+0000 (Coordinated Universal Time)
cuid: clpkb2tr100020al29rqyhvz5
slug: comparing-files
tags: linux-for-beginners

---

We can compare the data of two files by using the following commands:

1. cmp
    
2. diff
    
3. sdiff
    
4. vimdiff
    
5. comm
    

### 1) cmp command:

It will compare data byte by byte

<mark>cmp file1.txt file2.txt</mark>

* If the content is the same then we won't get any output.
    
* If the content is different, then it provides information about only the first difference. byte number and line number will be provided.
    

### **2) diff Comamnd:**

It will show all the differences in the content.

<mark>diff file1.txt file2.txt</mark>

* If the content is the same then no output.
    
* If the content is different then it will show all the differences.
    

For the diff command, we can use the following options.

\-q shows a message when files are different.

\-s shows a message when files are the same | identical

\-y shows comparison line by line (parallel comparison)

If we want to suppress common lines then we should use --suppress-common-lines option with -y option.

<mark>$ diff -y --suppress-common-lines a.txt c.txt</mark>

### **3)sdiff Command:**

We can use sdiff command for side by side comparison (parallel comparison)

<mark>$ sdiff a.txt b.txt</mark>

### **4) vimdiff Command:**

It will highlight differences in vim

**<mark>vimdiff a.txt b.txt</mark>**

* ctrl+w+w --&gt;To go to the next window
    
* :q --&gt; Close the current window
    
* :qa --&gt; Close all windows
    
* :qa! --&gt; Close all windows forcely
    

### 5) comm Command:

By using this command we can compare data of two files.

c<mark>omm file1.txt file2.txt</mark>

It display results in 3 columns

* column-1: Data present only in file1.txt but not in file2.txt
    
* column-2: Data present only in file2.txt but not in file1.txt
    
* column-3: Common data of both files.
    
* With comm command we can use the following options
    
    \-1---If we don't want to display column-1
    
    \-2 ---If we don't want to display column-2
    
    \-3 ---If we don't want to display column-3
    
    \-12---If we don't want to display columns 1 and 2