# -in-class-wk4-2420
Week 4 Lab

1.1 - match a single character
'''
ls file?.* - result = file1.txt, file2.txt, fileA.txt
'''

1.2 - Match a character class
'''
ls file*.txt - matches zero or more digits 
'''

2.1 - Use cut and grep to find all of the people in their 30s in the dc.csv file 
'''
cut -d ',' -f 2, 3 | 

2.2 - Use grep to find all of the people who are not human. 
'''
grep -v "human" dc.csv | tail -n +2
'''

2.3 - use grep to see if the root user is permitted to connect to your server via SSH.
'''
grep -i "PermitRootLogin" /etc/ssh/sshd_config
'''<img width="483" height="63" alt="Screenshot From 2026-01-28 13-28-00" src="https://github.com/user-attachments/assets/fb537898-28f7-4c55-b7a9-44c048a0a12c" />

2.4 - Use grep to recursiely search for "URl" in all of the file in "etc/apt/sources.l<img width="649" height="104" alt="Screenshot From 2026-01-28 13-30-35" src="https://github.com/user-attachments/assets/e1e07a3a-7fc2-43f3-9ae4-b6435140cf6b" />
ist.d"

3.1 - Write a sed command to substitute "Human" with "human" so that human has consistent case. Dont change the original file. Use a redirect to write the altered contents to "dc-3.csv"
'''
sed 's/Human/human/g' dc.csv > dc-3.csv
'''
4.1 - Write a find command that will find all of the regular files on your sysem that end in .log. Use a redirect to discard any error message that you might get from the command
'''
find / -type f -name "*.log" 2>/dev/null
'''

<img width="650" height="238" alt="Screenshot From 2026-01-28 13-35-52" src="https://github.com/user-attachments/assets/bc45f2e0-46eb-4956-adbf-e788ab010f9c" />

4.2 - Rewrite the find command you used above and add-exec commdand to call grep and search error or warn (ignoring case) in all of the files found by your find command. 
'''
find / -type f -name "*.log" -exec grep -iE "error|warn" {} + 2>/dev/null
'''





