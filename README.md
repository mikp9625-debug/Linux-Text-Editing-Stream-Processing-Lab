# Linux-Text-Editing-Stream-Processing-Lab
Learned how to use text editors like nano, vim, sed, awk, and printf
Overview 

Overview
This lab focused on using essential Linux text‑editing and text‑processing tools: nano, vim, sed, awk, and printf. These utilities are widely used in real IT environments for editing configuration files, analyzing logs, automating text changes, and formatting script output. The goal of the lab was to build confidence in navigating files, modifying content, and performing basic automation tasks from the command line.

Objectives
Create and edit files using nano and vim

Perform text substitution using sed

Extract and filter data using awk

Format output using printf

Understand how these tools support troubleshooting and system administration

Procedure
1. Creating and Editing Files with nano
I created a new text file using:

Code
nano test.txt
Inside nano, I added sample text and saved the file using:

Ctrl + O to write the file

Ctrl + X to exit

This demonstrated basic file creation and editing in a Linux environment.

2. Editing Files with vim
I opened the same file in vim:

Code
vim test.txt
I practiced the basic vim workflow:

i → enter insert mode

edit text

Esc → return to command mode

:wq → save and quit

:q! → quit without saving

This helped me understand vim’s modal editing system, which is essential when working on servers where vim is the only editor available.

3. Using sed for Text Replacement
I used sed to perform automated text substitution inside a file.

Replace the first occurrence of a word:

Code
sed 's/red/green/' test.txt
Replace all occurrences:

Code
sed 's/red/green/g' test.txt
Save changes directly to the file:

Code
sed -i 's/red/green/g' test.txt
This demonstrated how sed can automate edits without manually opening the file.

4. Using awk for Data Extraction
I practiced extracting specific fields from a file:

Code
awk '{print $6}' file.txt
Output:

Code
password
Then I printed multiple fields:

Code
awk '{print $5, $6}' file.txt
Output:

Code
Failed password
This showed how awk can parse logs and extract meaningful information based on field positions.

5. Using printf for Formatted Output
I used printf to produce clean, predictable output:

Code
printf "%s\n" "Hello"
Output:

Code
Hello
I also tested numeric formatting:

Code
printf "%d/" 22.22
Output:

Code
22/
This demonstrated how printf handles formatting more reliably than echo, especially in scripts.

Real‑World Applications
Editing configuration files
Using nano and vim to modify files such as:

/etc/ssh/sshd_config

/etc/hosts

service configuration files

Updating values in config files
Using sed to automate changes such as:

updating IP addresses

changing port numbers

fixing typos across multiple files

Investigating login failures
Using awk to extract fields from /var/log/auth.log, such as:

timestamps

usernames

IP addresses

Cleaning messy files
Using sed to remove blank lines or unwanted text.

Formatting script output
Using printf to produce readable, professional script output.

What I Learned
How to safely edit files using both nano and vim

How to automate text changes using sed

How to extract specific information from logs using awk

How to format output for scripts using printf

How these tools support real‑world Linux administration and troubleshooting
