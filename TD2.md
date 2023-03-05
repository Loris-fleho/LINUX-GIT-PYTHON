# LINUX-GIT-PYTHON
## TD2 : Fundamental Linux functionalities
### Exercise 1 : Access general computer informations
#### Q1
sudo apt update
sudo apt upgrade
#### Q2 : Display
##### Linux version
cat /etc/os-release
lsb_release -a
hostnamectl
##### Current processes and memory usage associated
top
##### Display it in a more pleasant way ("more readable for humans")
htop
##### Number of processors
lscpu
##### L1, L2 and L3 cache size
lscpu | grep cache
##### Disk space
df -H /dev/root
lsblk -e 7,11
##### Monted devices
cat /proc/mounts
##### Connected usb devices
lsusb
##### Hostname
hostname
### Exercise 2 : Shell - Variables and scripts scope
#### Q1
x="piri pimpin"
#### Q2
echo $x
#### Q3
x="$x piri pimpon"
#### Q4
mkdir my_programs
cd my_programs
#### Q5
vim pilou
echo "pilou pilou"
#### Q6
source pilou
#### Q7
chmod +x pilou
#### Q8
pilou
#### Q9
echo $PATH
#### Q10
PATH="$PATH:$(pwd)"
echo $PATH
#### Q11
export PATH
#### Q12
cd
#### Q13
pilou
#### Q14
vim .profile
#### Q15
pilou
### Exercise 3 : Scheduling task - daemon
#### Q1
vim say_hello.sh
echo "$(date) - Hello" >> hellos.txt
#### Q2
chmod +x say_hello.sh
#### Q3
crontab -e
* * * * * /home/say_hello.sh >> log_hellos
### Exercise 4 : Hashing
#### Q1
mkdir hash_cheksum
cd hash_checksum
#### Q2
> .sensible_addresses > .sensible_passwords
#### Q3
ls -A
#### Q4
echo "echo 'Have a good day'" > gentle_script.sh
#### Q5
source gentle_script.sh
#### Q6
sha256sum gentle_script.sh >> log_sha
#### Q7
vim gentle_script.sh
rm .sensible*
#### Q8
sha256sum gentle_script.sh >> log_sha
#### Q9
source gentle_script.sh
#### Q10
ls -A
#### Q11
cat log_sha
### Exercise 5 :  Compressing
#### Q1
sudo apt install qpdf
#### Q2
mkdir compress
cd compress
#### Q3
> .hello
echo "echo 'Hello'" > .hello
#### Q4
zlib-flate -compress=1 < hello > hello_compressed
ls -l hello_compressed | awk '{print $5 "\t" $9}' >>
,→ log_compress
#### Q5
for i in {1..1000}; do echo "Hello 0000" >> hello_multiple;
,→ done
ls -l hello_multiple | awk '{print $5 "\t" $9}' >> log_compress
#### Q6
zlib-flate -compress=1 < hello_multiple >
,→ hello_multiple_compressed
ls -l hello_multiple_compressed | awk '{print $5 "\t" $9}' >>
,→ log_compress
#### Q7
for i in {1..1000}; do echo "Hello $i" >> hello_multiple_i;
,→ done
ls -l hello_multiple_i | awk '{print $5 "\t" $9}' >>
,→ log_compress
#### Q8
zlib-flate -compress=1 < hello_multiple_i >
,→ hello_multiple_i_compressed
ls -l hello_multiple_i_compressed | awk '{print $5 "\t" $9}'
,→ >> log_compress
#### Q9
cat log_compress
#### Q10
6/14 => 0.428 (3:7)
11000/6 => 103 (100:1)
9893/1900 => 5.21 (5:1)
#### Q11

### Exercise 6: ACLs : Access Control Lists
#### Q1




