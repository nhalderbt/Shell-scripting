# Shell-scripting

The mkdir command is used to create a new directory, but it requires a directory name.

**$ mkdir**

Creates a new directory named chapter1 in the current location.

**$ mkdir chapter1**

Lists all files and directories in the current directory.

**$  ls**

This lists files and directories in the current directory in long format, showing:
Permissions
Owner
File size
Modification date
Filename

**ls -l**

**Example Output:**

drwxr-xr-x  2 user user  4096 Mar 28 10:30 Documents

-rw-r--r--  1 user user  1234 Mar 27 14:22 report.txt

-rwxr-xr-x  1 user user  5678 Mar 26 09:10 script.sh

**Here’s what each part means:**

d → Directory (drwxr-xr-x)

- → File (-rw-r--r--)
- 
rwx → Permissions (Read, Write, Execute)

user user → Owner & Group

1234 → File size (bytes)

Mar 27 14:22 → Last modified date

report.txt → File name


📌 **Additional ls Options**
ls -lh → Human-readable sizes (K, M, G)
ls -la → Show hidden files (.files)
This lists all files, including hidden files (files that start with a dot .)

Example Output

.  ..  .bashrc  .profile  .ssh  Documents  Downloads  script.sh

. → Represents the current directory

.. → Represents the parent directory

.bashrc, .profile, .ssh → Hidden files (usually configuration files)

$ ls‐a
. .. .bash_history .bash_logout .bash_profile
.bashrc .kshrc .mozilla .viminfo

Each hidden file or directory starts with a DOT character.
Therefore, files such as .bash_history, .bashrc, .kshrc are hidden
files, whereas .mozilla is a hidden folder.

ls -lt → Sort by modification time
ls -ltr → Reverse order (oldest first)

To change into Linux_tutorial directory and make it our working directory, we would use the command:
**$ cd Linux_tutorial**

The pwd (Print Working Directory) command shows the full path of the current directory you are in.
**$ pwd**

Removes the chapter1 directory recursively (-r), meaning it deletes the directory along with all its contents.

Be careful when using rm -r, as it permanently deletes files and directories without sending them to the Trash.

**$ rm –r chapter1/**

creates a new empty file named lesson.txt in the current directory if it doesn’t already exist. If the file already exists, touch updates its timestamp (last modified time)

Create an empty file:

**$ touch myfile.txt**

Create multiple files at once:

**$ touch file1.txt file2.txt file3.txt**

Update the timestamp of an existing file:

**$ touch existing_file.txt**

Verify file creation using ls:

**$ ls -l lesson.txt**

**sudo apt-get install wget -y** is used to install the wget package on a Debian-based Linux system (like Ubuntu).

![image](https://github.com/user-attachments/assets/929fcd21-1430-4cdf-a3a1-294b05e0a9cf)

The ‘wget’ command is used to download files from your Linux terminal provided you already have web link of that file. By using ‘wget’ we can also download FASTQ files from the public databases by providing the exact URL of the file.

For instance, let’s download a FASTQ file from https://trace.ncbi.nlm.nih.gov/Traces/sra-reads-be/fasta?acc=SRR098026

**wget https://trace.ncbi.nlm.nih.gov/Traces/sra-reads-be/fasta?acc=SRR098026**

![image](https://github.com/user-attachments/assets/358bfef5-d9d0-43ac-b974-b883814238c2)


Confirm whether FASTQ file is downloaded or not by using:
**$ ls ‐lh**

**File Compression**
‘gzip’ command is used to compress as well as uncompress/decompress
all the files with .gz file extension.

To uncompress SRR2079545.fastq.gz, type:
$ gzip ‐d SRR2079545.fastq.gz

**fastq.gz is a compressed format having .gz as an extension**

Similarly, you can compress the SRR2079545.fastq file using the ‘gzip’ command as follows:
**$gzip SRR2079545.fastq**


https://trace.ncbi.nlm.nih.gov/Traces/sra-reads-be/fasta?acc=SRR098026

The ‘cat’ command which stands for concatenate is used to display the contents of a file. To display the contents of SRR2079545.fastq file, type:
**$ cat SRR2079545.fastq**

This command will display contents of your FASTQ file on the terminal. However, in larger files such as FASTQ, most of the output will scroll up the screen with only the last part that can be accessed on the terminal.

Other handy commands to quickly check the contents of bigger files are ‘head’ and ‘tail’ commands.
**$ head SRR2079545.fastq**
This will display the first 10 (the default number) lines from the file.

To print the first 15 lines, type:
**$ head -15 SRR2079545.fastq**

Similarly, to print the last 10 and last 15 lines of a file, use:
**$ tail SRR2079545.fastq
$ tail ‐15 SRR2079545.fastq**




