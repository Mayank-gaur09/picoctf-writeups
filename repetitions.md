# Challenge: Repetitions - Multiple decoding | General Skills


## What the challenge asked

The challenge provided me with a file that had scrambled text in it. The challenge also provided a hint that said "Multiple decoding is always good.", which meant I had to decode the file multiple 
times to find the final flag.

## My approach

The file had 2 equal signs at the end of the scrambled up text which meant that It was base64 encoded.

## The Solution

I used the command 'echo "the text..." | base64 -d' to decode the base64 and I kept doing it until I found the flag for a total of 6 times.

## What I Learned

- Using the tool CyberCafe to quickly decode text.
