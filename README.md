# EXP NO -1
# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting

# AIM:
To practice Linux Commands and Shell Scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

### Step 2:

Execute the following commands

### Step 3:

Testing the commands for the desired output. 

# COMMANDS:
### Create the following files file1, file2 as follows:
cat > file1
```
chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d
```
cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```
### Display the content of the files
cat < file1
## OUTPUT
![image](https://github.com/user-attachments/assets/194f2b34-5f9c-4c5f-ab6b-af06e51005b3)

cat < file2
## OUTPUT
![image](https://github.com/user-attachments/assets/71d3d3fe-1c62-4ec7-907e-4d12343bfd5c)

# Comparing Files
cmp file1 file2
## OUTPUT
![image](https://github.com/user-attachments/assets/8222f93c-cce4-4987-b852-0f70745a09eb)
 
comm file1 file2
 ## OUTPUT
![image](https://github.com/user-attachments/assets/ee482dfa-c851-4407-9002-70159c1908b4)

diff file1 file2
## OUTPUT
![image](https://github.com/user-attachments/assets/f55ad3bd-959e-4eb0-95f5-0812698c027b)

#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```
cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```


cut -c1-3 file11
## OUTPUT
![image](https://github.com/user-attachments/assets/140d2b58-acca-4bf1-9c20-0a46cb1e2372)

cut -d "|" -f 1 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/b8b8aa64-23a0-4c98-8290-a65b7dda7555)

cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/b6079978-2fc7-4d65-b721-79a541a77012)

cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/5485f73a-3d68-4216-a931-e4f5a47a986a)

grep hello newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/41d25a32-f17a-47f3-8498-ce7924473369)

grep -v hello newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/a5bbfb1a-b94c-495a-9887-59a74864c69c)

cat newfile | grep -i "hello"
## OUTPUT
![image](https://github.com/user-attachments/assets/720a1270-b0db-4dcd-9a08-c4c110fe83fd)

cat newfile | grep -i -c "hello"
## OUTPUT
![image](https://github.com/user-attachments/assets/7a310bd9-6647-4e44-a5b7-285ac0df6c0c)

grep -R ubuntu /etc
## OUTPUT
grep -w -n world newfile   
## OUTPUT
cat < newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```

cat > newfile
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 ```
egrep -w 'Hello|hello' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/e4039416-3ebf-4455-8d35-31cb6174ca07)

egrep -w '(H|h)ello' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/e167f9b6-58ea-4fb9-8da8-281a38ed8162)

egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/e246e576-d568-4c0a-8436-6887ee9f6d81)

egrep '(^hello)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/8ce084c7-b94f-40a9-a929-be5c8701283f)

egrep '(world$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/e84b450c-6626-4308-b342-0c2d92706721)

egrep '(World$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/5f612fe0-9ad3-4117-b76a-2d5d7a4b6c61)

egrep '((W|w)orld$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/651dc5b0-12ec-4749-8313-9e421ba0dbe3)

egrep '[1-9]' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/18eb1294-b63c-42ac-8950-559e07ab5c48)

egrep 'Linux.*world' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/5f6eb0f3-01f2-4430-a8d8-ec0a628a5f86)

egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/27d6fa0a-0d09-46fd-8885-9f1486037c57)

egrep l{2} newfile
## OUTPUT
![image](https://github.com/user-attachments/assets/365ec9ff-679c-436d-aaa1-199dcac12590)

egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/user-attachments/assets/54535be0-70a3-4657-a2d9-0d8ec6e9bb84)


cat > file23
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
^d
```


sed -n -e '3p' file22
## OUTPUT
![image](https://github.com/user-attachments/assets/5b51f776-eb4d-4c51-bfa7-244d40eaa479)

sed -n -e '$p' file22
## OUTPUT
![image](https://github.com/user-attachments/assets/e2d0accd-979b-4e46-bb51-98d1a1567d21)

sed  -e 's/Ram/Sita/' file22
## OUTPUT

![image](https://github.com/user-attachments/assets/17bcda39-3582-46cf-a325-497280b8ae4b)


sed  -e '2s/Ram/Sita/' file22
## OUTPUT
![image](https://github.com/user-attachments/assets/06897945-8451-49a3-917e-fd72ae3581e9)

sed  '/tom/s/5000/6000/' file22
## OUTPUT
![image](https://github.com/user-attachments/assets/8656931d-bf82-4765-ae8b-9e321695b367)

sed -n -e '1,5p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/1f52f4b1-fc58-4530-a890-2799caf6ba16)



sed -n -e '2,/Joe/p' file23
## OUTPUT


![image](https://github.com/user-attachments/assets/f9f39ce9-08ef-427e-a2cb-ab603b59f64a)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/0155d04d-3c1e-4566-be25-de042fc67e7b)

seq 10 
## OUTPUT

![image](https://github.com/user-attachments/assets/601c666c-8ce2-49d4-a799-c08f407505c7)

seq 10 | sed -n '4,6p'
## OUTPUT


![image](https://github.com/user-attachments/assets/25b4210a-80f7-47b8-94bc-6d777069372b)

seq 10 | sed -n '2,~4p'
## OUTPUT

![image](https://github.com/user-attachments/assets/4d70fea9-e2c4-4472-abe1-87b1aa3bf4b6)

seq 3 | sed '2a hello'
## OUTPUT

![image](https://github.com/user-attachments/assets/2f4c049b-2a03-414f-871f-6d1f4cc82785)

seq 2 | sed '2i hello'
## OUTPUT

![image](https://github.com/user-attachments/assets/c7a85230-153d-4563-a7d6-584033bea007)


seq 10 | sed '2,9c hello'
## OUTPUT

![image](https://github.com/user-attachments/assets/51451307-2304-4184-a55b-977cd52db6dc)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/1a3f6499-37de-4320-9a37-0e2c6bb1ff5c)


sed -n '2,4{s/$/*/;p}' file23


#Sorting File content
cat > file21
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
sort file21
## OUTPUT

![image](https://github.com/user-attachments/assets/962f9b24-e849-4ab2-b5fa-0523e753a414)


cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
uniq file22
## OUTPUT

![image](https://github.com/user-attachments/assets/dad2a403-bcf9-4213-8856-3341fde6fd5c)

#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

![image](https://github.com/user-attachments/assets/480383a3-0e8c-4fc7-9fcf-2649b580ee7f)

cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '
 ## OUTPUT

![image](https://github.com/user-attachments/assets/76ca8446-1251-403e-83ee-e52126385ba5)

cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![image](https://github.com/user-attachments/assets/c3fe5058-6a89-45be-93c9-b7c942457fc5)

#Backup commands
tar -cvf backup.tar *
## OUTPUT

bench.py
file1
file11
file2
file21
file22
file23
hello.c
hello.js
newfile
readme.txt
urllist.txt


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
-rw-r--r-- user/group 0 2024-02-25 14:30:00 file1.txt
drwxr-xr-x user/group 0 2024-02-25 14:30:00 directory1/
-rw-r--r-- user/group 1024 2024-02-25 14:30:00 directory1/file2.txt
-rw-r--r-- user/group 2048 2024-02-25 14:30:00 directory1/file3.txt

tar -xvf backup.tar
## OUTPUT
x file1.txt
x directory1/
x directory1/file2.txt
x directory1/file3.txt

gzip backup.tar

ls .gz
## OUTPUT
  backup.tar.gz
gunzip backup.tar.gz
## OUTPUT
backup.tar
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

![image](https://github.com/user-attachments/assets/863d3634-6fe0-4fe8-8832-85ce03d19d00)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

![image](https://github.com/user-attachments/assets/fa10689f-f0c7-464b-8ade-5624ad05038e)


cat < scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $1#
echo 'The $$ is ' $$
ps
^d
 ```

cat scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $\#
echo 'The $$ is ' $$
ps
```
 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT
File name is ./scriptest.sh
File name is scriptest.sh
First arg. is 1
Second arg. is 2
Third arg. is 3
Fourth arg. is
The $@ is 1 2 3
The $\# is $#
The $$ is 124
 
ls file1
## OUTPUT

![image](https://github.com/user-attachments/assets/07aef8c1-e6b2-4747-a169-40a259ca7293)

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied

![image](https://github.com/user-attachments/assets/a0fd60d9-8152-48ea-b588-5f9961266225)
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT
1
# mis-using string comparisons

cat < strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
^d
```

cat strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
```
##OUTPUT



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

![image](https://github.com/user-attachments/assets/107abbda-a6e7-416b-86a4-937868f79061)


# check file ownership
cat < psswdperm.sh 
```bash
\#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
^d
```

cat psswdperm.sh 
```bash
/#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
 ```
./psswdperm.sh
## OUTPUT
You are the owner of the /etc/passwd file
# check if with file location
cat>ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```
cat ifnested.sh 
```
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

./ifnested.sh 
## OUTPUT

![image](https://github.com/user-attachments/assets/353f2caf-1563-492b-80a4-b53402431791)

# using numeric test comparisons
cat > iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
^d
```


cat iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
```

$ chmod 755 iftest.sh
 
$ ./iftest.sh 
# OUTPUT

![image](https://github.com/user-attachments/assets/d8989359-9bf9-4b35-b664-267bf8199b04)

# check if a file
cat > ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```

cat ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
# OUTPUT

![image](https://github.com/user-attachments/assets/91bc502b-0766-4553-bddd-96912b2fa334)

# looking for a possible value using elif
cat elifcheck.sh 
```bash
\#!/bin/bash
if [ $USER = Ram ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Rahim ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Robert ]
then
echo "Special testing account"
elif [ $USER = gganesh ]
then
echo "$USER, Do not forget to logout when you're done"
else
echo "Sorry, you are not allowed here"
fi
```

$ chmod 755 elifcheck.sh
 
$ ./elifcheck.sh 
## OUTPUT
Welcome Ram
Please enjoy your visit
Welcome Rahim
Please enjoy your visit
Special testing account
gganesh, Do not forget to logout when you're done
Sorry, you are not allowed here

# testing compound comparisons
cat> ifcompound.sh 
```bash
\#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi
```
$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
## OUTPUT

![image](https://github.com/user-attachments/assets/c11c0418-49bc-4fb8-803a-d5ad148258a5)

# using the case command
cat >casecheck.sh 
```bash
case $USER in
Ram | Robert)
echo "Welcome, $USER"
echo "Please enjoy your visit";;
Rahim)
echo "Special testing account";;
gganesh)
echo "$USER, Do not forget to log off when you're done";;
*)
echo "Sorry, you are not allowed here";;
esac
```
$ chmod 755 casecheck.sh 
 
$ ./casecheck.sh 
# output 
Welcome Ram/Rahim
Please enjoy your visit
Special testing account
gganesh, Do not forget to logout when you're done
Sorry, you are not allowed here

cat > whiletest
```bash
#!/bin/bash
#while command test
var1=10
while [ $var1 -gt 0 ]
do
echo $var1
var1=$[ $var1 - 1 ]
done
```
$ chmod 755 whiletest.sh
 
$ ./whiletest.sh
 # output
 10
9
8
7
6
5
4
3
2
1
 
cat untiltest.sh 
```bash
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
``` 
$ chmod 755 untiltest.sh
 # output  
 100
75
50
25
cat forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh
 
 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```
 
$ chmod 755 forin2.sh
# output
The next state is Alabama
The next state is Alaska
The next state is Arizona
The next state is Arkansas
The next state is California
The next state is Colorado
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
```
$ chmod 755 forin2.sh
 
$ ./forin2.sh 
 
cat forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ ./forin3.sh 
 # output 
 word:I
word:dont know if thisll
word:work
cat forin1.sh 
```bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
$ chmod 755 forin1.sh

## OUTPUT
cat forinfile.sh 
```bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file“
done
```
$ chmod 777 forinfile.sh
$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT


cat forctype.sh 
```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
````
$ chmod 755 forctype.sh
$ ./forctype.sh 
## OUTPUT

cat forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
$ chmod 755 forctype.sh
$ ./forctype1.sh 
## OUTPUT

cat fornested1.sh 
```bash
#!/bin/bash
# nesting for loops
for (( a = 1; a <= 3; a++ ))
do
echo "Starting loop $a:"
for (( b = 1; b <= 3; b++ ))
do
echo " Inside loop: $b"
done
done
```
$ chmod 755 fornested1.sh
 
$ ./fornested1.sh 
 ## OUTPUT
Visit beautiful Hyderabad
Visit beautiful Alampur
Visit beautiful Basara
Visit beautiful Warangal
Visit beautiful Adilabad
Visit beautiful Bhadrachalam
Visit beautiful Khammam
 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
break
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```
## OUTPUT

$ chmod 755 forbreak.sh
 The value of i is 1
The value of i is 2
The value of i is 3
The value of i is 4
The value of i is 5
$ ./forbreak.sh 
 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
continue
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```

 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT
 
cat exread.sh 
```bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 ```
 
$ chmod 755 exread.sh 
 
$ ./exread.sh 
## OUTPUT


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
1 - 5
2 - 4
3 - 3
4 - 2
5 - 1


$ ./exread1.sh 
 
cat funcex.sh
```bash
#!/bin/bash
# trying to access script parameters inside a function
function func {
echo $[ $1 * $2 ]
}
if [ $# -eq 2 ]
then
value=`func $1 $2`
echo "The result is $value"
else
echo "Usage: badtest1 a b"
fi
```
## OUTPUT
 ./funcex.sh 
Iteration number: 1
Iteration number: 2
The for loop is completed
 
 ./funcex.sh 1 2

 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

## OUTPUT
$ ./argshift.sh 1 2 3
 
 cat argshift1.sh
```bash
 #/bin/bash 
 # store arguments in a special array 
args=("$@") 
# get number of elements 
ELEMENTS=${#args[@]} 
 # echo each element in array  
# for loop 
for (( i=0;i<$ELEMENTS;i++)); do 
    echo ${args[${i}]} 
done
```
$ chmod 777 argshift.sh
## OUTPUT
$ ./argshift.sh 1 2 3
 
cat argshift.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```
## OUTPUT
 ./argshift.sh 1 2 3
 
 
cat > nc.awk
```bash
BEGIN{}
{
print len=length($0),"\t",$0 
wordcount+=NF
chrcnt+=len
}
END {
print "total characters",chrcnt 
print "Number of Lines are",NR
print "No of Words count:",wordcount
}
 ```
cat>data.dat
```bash
bcdfghj
abcdfghj
bcdfghj
ebcdfghj
bcdfghj
ibcdfghj
bcdfghj
obcdfghj
bcdfghj
ubcdfghj
```
awk -f nc.awk data.dat
## OUTPUT 
 
cat > palindrome.sh
```bash
#num=545
echo "Enter the number"
read num
s=0
rev=""
temp=$num
while [ $num -gt 0 ]
do
	# Get Remainder
	s=$(( $num % 10 ))
	# Get next digit
	num=$(( $num / 10 ))
	# Store previous number and
	# current digit in reverse
	rev=$( echo ${rev}${s} )
done
if [ $temp -eq $rev ];
then
	echo "Number is palindrome"
else
	echo "Number is NOT palindrome"
fi
```
## OUTPUT 
Enter the number
121
Number is palindrome
Enter the number
69
Number is NOT palindrome

# RESULT:
The Commands are executed successfully.
