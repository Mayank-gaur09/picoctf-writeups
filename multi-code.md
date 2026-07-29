# Challenge: Multi Code - General Skills


## What the challenge asked

The challenge gave me an encoded message that was hiding a flag. The message description said that there was no encryption, just multiple layers of obfuscation. The challenge also had 2 hints which told me that "The flag has been wrapped in several layers of common encodings such as ROT13, URL encoding, Hex, and Base64." and about a tool called CyberChef to help me decode the text.

## My approach

I downloaded the message.txt file that was attached and inspected it to identify the outermost coding in terminal by looking at determining factors to see whether it was base64 encoded, hex, ROT13 or Url encoded.

Base 64 - letters, numbers signs or ended with "="
Hex - only numbers and lowercase alphabets
URL encoding - "%" followed by 2 characters
ROT13 - text that looks like scrambled up English words with spacing pattern as real words.


## The Solution

The message had been encoded in 4 layers 

1 - Base64 since it had an equal sign at the end along with numbers and letters this made the most sense. I decoded it with the command echo "the text..." | base64 -d
2 - The second layer was a hex layer since the text only contained numbers and some lowercase alphabets. I decoded it with the command echo "the text..." | xxd -r -p
3 - The third layer was URL encoding because of pairs of text that had % followed with 2 characters. I had to look how to decode this one as I was not entirely sure. 
4 - the final layer was ROT13 due to since it looked like scrambled English words such as picoCTF. I decoded it with the command echo "the text..." | tr 'A-Za-z' 'N-ZA-Mn-za-m'


## What I learnt

- How to visually identify the different encoding types by their character patterns
- That multiple encodings can be layered on top of each other and you have to decode it step by step to get the original message
- About the tool CyberChef



