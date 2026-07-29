# Challenge: Linux Text Transformations - General Skills


## What the challenge asked

The challenge gave me a flag that had undergone a series of linux text transformations and it asked me to reverse each step to recover the original flag.

## My approach

Worked through the transformations one at a time, in a reverse order using the Mac terminal. Each stage revealed a hint about what transformation was applied which helped me identify the correct command to undo it.

## Solution

The flag had been transformed in 5 stages. I reversed them in this order:
1. base 64 encoded - reversed with the command "base64 -r"
2. text reversed - reversed with "rev"
3. replace underscores with dashes - reversed with "tr '-' '_'"
4. replace curly braces with parentheses - "tr '()' '{}'"
5. ROT13 applied to letters - reverse with "tr 'A-Za-z' 'N-ZA-Mn-za-m'"


## What I learned

- "base64 -d" decodes base64-encoded strings
- tr` can substitute one set of characters for another, and can also apply ROT13 by shifting the alphabet.
