# LINUX-GIT-PYTHON
## TD1 : Use basic Linux commands
### Exercise 1 : Move Around
#### Q1
cd /
#### Q2
ls
#### Q3
pwd
#### Q4
mkdir test
#### Q5
cd home/
#### Q6
cd ~
#### Q7
cd ..
#### Q8
cd ..
#### Q9
cd
#### Q10
mkdir test
#### Q11
cd test
#### Q12
pwd

### Exercise 2 : Create, Rename, copy, delete
#### Q1
cd 
#### Q2
mkdir linux_ex_1
#### Q3
pwd
#### Q4
cd linux_ex_1
#### Q5
touch loris_fleho.txt
#### Q6
mkdir test
#### Q7
mv ../loris_fleho.txt .
#### Q8
mv notes/loris_fleho.txt notes/loris_fleho_2023.txt
#### Q9
cp -r notes notes_2022
#### Q10
rm -rv notes

### Exercise 3 : Create and run a script
#### Q1
vim script_1.sh
#### Q2
 #!/bin/bash
 echo "script running please wait ..."
 echo "done"
#### Q3
:wq
#### Q4
ls
#### Q5
cat script_1.sh

### Exercise 4 :  Accessing or modifying a file : permissions and root privilege
#### Exercise 4.1 : Change the rights for accessing or modifying a file
##### Q1
touch linux_ex_1/credentials
cat linux_ex_1/credentials 
ls -l linux_ex_1/credentials
##### Q2
chmod u=r,g=r,o=r linux_ex_1/credentials
ls -l linux_ex_1/credentials
vim /home/lorisfleho/linux_ex_1/confidentials
#Impossible to modify the file beacause all users only can read it 
#To save the file
:wq 
ls -l linux_ex_1/credentials
##### Q3
chmod u=rw,g=rw,o=rw linux_ex_1/credentials
ls -l linux_ex_1/credentials
vim /home/lorisfleho/linux_ex_1/confidential.txt
:wq
ls -l linux_ex_1/credentials
##### Q4
chmod u=rwx,g=rw,o=rw linux_ex_1/credentials
ls -l linux_ex_1/credentials
chmod u=rwx,g=w,o=w linux_ex_1/credentials
ls -l linux_ex_1/credentials
chmod u=rwx,g=rwx,o=rwx linux_ex_1/credentials
 
#### Exercise 4.2 : Access root files
##### Q1
cd /
##### Q2
sudo mkdir .private_file
sudo  vim /home/lorisfleho/linux_ex_1/.private_file
ls -la
##### Q3
It's impossible
##### Q4
sudo vim /home/lorisfleho/linux_ex_1/.private_file
ls -la .private_file
##### Q5
sudo chmod u=rwx,g=rwx,o=rwx .private_file
vim /home/lorisfleho/linux_ex_1/.private_file

#### Exercise 4.3 : Change a file owner
##### Q1
chmod a+rw .private_file
##### Q2
chown lorisfleho .private_file
##### Q3
chmod a+rw .private_file

#### Exercise 4.4 :  Manage Packages (tools / functions)
##### Q1
sudo apt update
##### Q2
sudo apt upgrade
##### Q3
sudo apt install cmatrix
##### Q4
cmatrix
##### Q5
q
##### Q6
sudo apt install tmux
##### Q7
tmux
##### Q8
echo "Hello session 0"
##### Q9
cmatrix
##### Q10
ctrl+b d
##### Q11
tmux new
##### Q12
echo "Hello session 1"
##### Q13
ctlr+b d
##### Q14
tmux list-sessions
##### Q15
tmux attach -t 0
##### Q16
ctlr+b d
##### Q17
tmux attach -t 1
##### Q18
ctlr+b d
##### Q19
tmux list-sessions
##### Q20
tmux kill-server
##### Q21
tmux list-sessions

#### Exercise 4.3 : Use functions arguments / parameters
##### Q1
cmatrix --help
##### Q2
cmatrix -C red
q
##### Q3
cmatrix -u 20
##### Q4
q
##### Q5
cmatrix -C blue -u 30
##### Q6
man cmatrix
##### Q7
tmux --help
##### Q8
man tmux
