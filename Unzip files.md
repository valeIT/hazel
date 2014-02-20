#Unzip files

For .tar and .zip files you simply use the unzip already included in hazel: 

<code>
if all [..] :
Extension is zip
-------------------
do:
Unarchive

Move to Trash
</code>
If you want to move the original file to the Trash ufter unzipping.

#Unrar file 

For rar file is a bit more elaborate since it doesn't have native support. you'll first need to download [winrar for the command line](http://www.rarlab.com/download.htm), and install it opening the archive.  

Here's what to tell Hazel to do:
<code>
if all [..] :
Extension is rar
-------------------
do:
Run shell script:
rar e $1

Move to folder Trash
</code>

<code>rar e $1</code>
is a simple version that simply unrar everything in the current folder, if you want a more specific behaviour write <code> rar -?</code> in the command line.

