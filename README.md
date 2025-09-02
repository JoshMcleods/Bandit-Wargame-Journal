# Bandit-Wargame-Journal
offensive security journal practice for levels 1-34

| Time  | Who | Process | How (commands/notes/actions taken) | Outcome (what happened as a result) |
|-------|-----|---------|------------------------------------|-------------------------------------|
| 3:07  | Me  | Navigated to https://overthewire.org/wargames/bandit/bandit0.html Level 0 | Told me to ssh into bandit.labs.overthewire.org with port 2220. Account: bandit0, Password: bandit0. Used `ssh bandit0@bandit.labs.overthewire.org -p 2220`, entered password `bandit0`. | Logged into bandit0 on bandit.labs.overthewire.org |
|       |     | Prior knowledge | Used ChatGPT to explain IO redirection. Learned to use `--` before calling a file with name starting with `-`, and to use quotes for files with spaces. | |
|       |     | Prior knowledge | Used `man find` to see format for the `find` command. Used ChatGPT to learn multiple arguments for `find`. Used `man grep` for `grep` syntax. | |
|       |     | Prior knowledge | Used https://ryanstutorials.net/linuxtutorial/piping.php. Learned to use `strings` command. | |
|       |     | Bandit1 | `ls`, `cat readme` → Password 0: `ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If`. Then `ssh bandit1@bandit.labs.overthewire.org -p 2220`, `ls`, `cat ./-`. Password 1: `263JGJPfgU6LtdEvgfWU1XP5yac29mFx`. | Successfully retrieved password 1 |
|       |     | Bandit2 | `ssh bandit2@bandit.labs.overthewire.org -p 2220`, `ls`, `cat -- "spaces in this filename"`. Password 2: `MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx`. | Retrieved password 2 |
|       |     | Bandit3 | `ssh bandit3@bandit.labs.overthewire.org -p 2220`, `ls`, `ls -a`, `cat hiddenfilename`. Password 3: `2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ`. | Retrieved password 3 |
|       |     | Bandit4 | `ssh bandit4@bandit.labs.overthewire.org -p 2220`, `cd inhere`, `cat -- -filename1-8`. Password 4: `4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw`. | Retrieved password 4 |
|       |     | Bandit5 | `ssh bandit5@bandit.labs.overthewire.org -p 2220`, `ls inhere`, `find . -size 100c`, `cat ./maybehere07/.file2`. Password 5: `HWasnPhtq9AVKe0dmk45nxy20cvUa6EG`. | Retrieved password 5 |
|       |     | Bandit6 | `ssh bandit6@bandit.labs.overthewire.org -p 2220`, `cd ..`, `find / -user bandit7 -group bandit6 -size 33c 2>/dev/null`, `cat /var/lib/dpkg/info/bandit7.password`. Password 6: `morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj`. | Retrieved password 6 |
|       |     | Bandit7 | `ssh bandit7@bandit.labs.overthewire.org -p 2220`, `ls`, `grep "millionth" data.txt`. Password 7: `dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc`. | Retrieved password 7 |
|       |     | Bandit8 | `ssh bandit8@bandit.labs.overthewire.org -p 2220`, `ls`, `sort data.txt | uniq -u`. Password 8: `4CKMh1JI91bUIZZPXDqGanal4xvAg0JM`. | Retrieved password 8 |
|       |     | Bandit9 | `ssh bandit9@bandit.labs.overthewire.org -p 2220`, `ls`, `strings data.txt | grep '='`. Password 9: `FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey`. | Retrieved password 9 |
|       |     | Bandit10 | `ssh bandit10@bandit.labs.overthewire.org -p 2220`, `ls`, `base64 -d data.txt`. Password 10: `dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr`. | Retrieved password 10 |
|       |     | Issue | Had copy/paste issue with VM. Even with bidirectional clipboard + guest additions. Fixed by reinstalling guest additions (`sudo -s`, `apt install`, upgrade guest additions, reboot). | Clipboard working, commands could be pasted |
