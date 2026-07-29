# Challenge: Piece by Piece - General Skills


## What the challenge asked

The challenge told me to connect to a remote server via SSH and gave me a password for the challenge instance, which provided me with a set of file parts in the home directory and a set of instructions
which told me that the file parts needed to becombined into a zip file and then extracted to a text file for the flag.

## My approach

I connected to the challenge instance using SSH: 'ssh ctf-player@dolphin-cove.picoctf.net -p 58135' then once I logged in, I ran 'ls' and found several files 'instructions.txt', and 
five split parts ('part_aa' through 'part_ae'). Opening 'instructions.txt' confirmed that the 5 parts needed to be combined into a zip file which required a password (which was stated in the file)

## The Solution

I combined the file parts using the command: 'cat part_aa part_ab part_ac part_ad part_ae > flag.zip' to turn the parts into a single zip file called "flag.zip". Then I used 'unzip flag.zip" to extract
the flag file using the password into "flag.txt" , then I used 'cat flag.txt' to find the text in the text file which was the flag required to complete the challenge.

## What I learned

- How to connect to a remote server using SSH
- Using cat to concatenate multiple split files into one original file
- How to extract password protected zip files
