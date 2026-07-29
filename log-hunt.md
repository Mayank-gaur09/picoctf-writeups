# Challenge: Log Hunt - General Skills


## What the challenge asked

The challenge had attached a server.log file which had parts of the flag scattered in the file and duplicated and I had to find out the final flag. The challenge also gave me a hint to use the command
'grep' to filter only the matching lines from the log.

## My approach

I used the command 'head server.log' to give me the first 10 lines of the server.log since there was alot of lines, this helped me find out the first flag part - "INFO FLAGPART: picoCTF{us3_"
which showed that the flag parts are tagged with the keyword "FLAGPART".

I used 'grep' to filter out only the lines that have the keyword. 

## The Solution 

I used the command 'grep "FLAGPART" server.log | sort | uniq' which gave me all the lines that had the keyword. However, it didn't filter out the duplicates which led to me  researching the correct command:
'grep "FLAGPART" server.log | awk -F': ' '{print $2}' | sort | uniq' 

This gave me the 4 flag parts 
1. `picoCTF{us3_`
2. `y0urlinux_`
3. `sk1lls_`
4. `cedfa5fb}`


and the final flag: `picoCTF{us3_y0urlinux_sk1lls_cedfa5fb}`

## What I learned

- How to use the command 'grep' to filter out the large log file down to only relevant lines
- How to use 'awk -F' which splits each line and only extracts what you need.

