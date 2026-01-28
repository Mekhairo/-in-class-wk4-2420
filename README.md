# -in-class-wk4-2420
Week 4 Lab

1.1 - match a single character
'''
ls file?.* - result = file1.txt, file2.txt, fileA.txt
'''

1.2 - 
'''
ls file*.txt - matches zero or more digits 
'''

2.1 -
'''
cut -d ',' -f 2, 3 | 

2.2 - 
'''
grep -v "human" dc.csv | tail -n +2
'''

2.3 - 
'''
grep -i "PermitRootLogin" /etc/ssh/sshd_config
'''<img width="483" height="63" alt="Screenshot From 2026-01-28 13-28-00" src="https://github.com/user-attachments/assets/fb537898-28f7-4c55-b7a9-44c048a0a12c" />

2.4 - Use grep to recursiely search for "URl" in all of the file in "etc/apt/sources.l<img width="649" height="104" alt="Screenshot From 2026-01-28 13-30-35" src="https://github.com/user-attachments/assets/e1e07a3a-7fc2-43f3-9ae4-b6435140cf6b" />
ist.d"

3.1 - 
'''
sed 's/Human/human/g' dc.csv > dc-3.csv
'''
4.1 - 
'''
find / -type f -name "*.log" 2>/dev/null
'''

<img width="650" height="238" alt="Screenshot From 2026-01-28 13-35-52" src="https://github.com/user-attachments/assets/bc45f2e0-46eb-4956-adbf-e788ab010f9c" />

4.2 - 
'''
find / -type f -name "*.log" -exec grep -iE "error|warn" {} + 2>/dev/null
'''





