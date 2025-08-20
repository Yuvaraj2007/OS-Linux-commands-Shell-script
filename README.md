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
### Display the content of the files
cat < file1
## OUTPUT
![Screenshot 2024-08-19 113533](https://github.com/user-attachments/assets/a46cf7a2-8904-4026-9e31-4282a06d3bd2)



cat < file2
## OUTPUT
![Screenshot 2024-08-19 113543](https://github.com/user-attachments/assets/a45738a3-c970-4ae5-b0e2-9a95e7df6f82)


# Comparing Files
cmp file1 file2
## OUTPUT
![Screenshot 2024-08-19 113558](https://github.com/user-attachments/assets/311cdc62-0f68-4e0d-b418-366e735fa865)

comm file1 file2
 ## OUTPUT
![Screenshot 2024-08-19 113612](https://github.com/user-attachments/assets/af3d5c01-e7d5-46e9-b2ec-dff1be315a68)

 
diff file1 file2
## OUTPUT
![Screenshot 2024-08-19 113744](https://github.com/user-attachments/assets/5d596308-c99a-49de-a67b-42897f56dbec)


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
![Screenshot 2024-08-19 113811](https://github.com/user-attachments/assets/3e373e45-f0b6-42bf-87c2-317e5fff7c43)




cut -d "|" -f 1 file22
## OUTPUT
![Screenshot 2024-08-19 113828](https://github.com/user-attachments/assets/a34a8423-ad78-4706-8759-8438909f0c7c)



cut -d "|" -f 2 file22
## OUTPUT
![Screenshot 2024-08-19 113841](https://github.com/user-attachments/assets/743e8292-3b87-4c01-a8d5-3002fc3ec594)


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
![Screenshot 2024-08-19 113859](https://github.com/user-attachments/assets/1b4e6456-29e0-4e22-8888-4fb7ff342570)



grep hello newfile 
## OUTPUT
![Screenshot 2024-08-19 113918](https://github.com/user-attachments/assets/889a0985-dc9a-4757-8e1f-beae667d656f)




grep -v hello newfile 
## OUTPUT
![Screenshot 2024-08-19 113927](https://github.com/user-attachments/assets/ce15902a-dd21-4d4b-a4b9-ec796d7ff79b)



cat newfile | grep -i "hello"
## OUTPUT
![Screenshot 2024-08-19 113939](https://github.com/user-attachments/assets/6926a1b2-3022-4195-9781-ed4641a3b096)




cat newfile | grep -i -c "hello"
## OUTPUT
![Screenshot 2024-08-19 114000](https://github.com/user-attachments/assets/3cbcdd09-feec-4f60-bd8a-f8c5fe451d30)




grep -R ubuntu /etc
## OUTPUT
![image](https://github.com/user-attachments/assets/c058bccd-1f9c-4b57-9c85-df12001ebefa)



grep -w -n world newfile   
## OUTPUT
![image](https://github.com/user-attachments/assets/5f5d6e5d-c2ed-45ee-b727-0c8da1f2c861)


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
![Screenshot 2024-08-27 091313](https://github.com/user-attachments/assets/99e8082e-aaea-4fc3-824f-0e07119e5ac5)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![Screenshot 2024-08-27 091408](https://github.com/user-attachments/assets/58c94a4e-82cd-4b0a-8f95-fb946f6e142f)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![Screenshot 2024-08-27 091442](https://github.com/user-attachments/assets/b7f97786-61fe-4ff6-8049-e1c1d82291ce)




egrep '(^hello)' newfile 
## OUTPUT
![Screenshot 2024-08-27 091533](https://github.com/user-attachments/assets/0919b3a9-9da6-464a-b320-9b35df8c207a)



egrep '(world$)' newfile 
## OUTPUT



egrep '(World$)' newfile 
## OUTPUT


egrep '((W|w)orld$)' newfile 
## OUTPUT
![Screenshot 2024-08-27 091739](https://github.com/user-attachments/assets/afb4d196-4ef2-46a2-be8d-e17a8094b1b8)



egrep '[1-9]' newfile 
## OUTPUT
![Screenshot 2024-08-27 091811](https://github.com/user-attachments/assets/92eafde7-a18b-4835-a9c5-775913d93ac5)



egrep 'Linux.*world' newfile 
## OUTPUT
![Screenshot 2024-08-27 091902](https://github.com/user-attachments/assets/2cb27590-c84d-44f3-9f8e-e1ab7070740b)


egrep 'Linux.*World' newfile 
## OUTPUT
![Screenshot 2024-08-27 091946](https://github.com/user-attachments/assets/c1f46d6b-d275-4a28-baee-ba66a5b656bf)


egrep l{2} newfile
## OUTPUT
![Screenshot 2024-08-27 092010](https://github.com/user-attachments/assets/cae87532-0377-46a0-aa44-64a541fd73ba)



egrep 's{1,2}' newfile
## OUTPUT 
![Screenshot 2024-08-27 092056](https://github.com/user-attachments/assets/7c4f3065-7a6d-4f96-9b69-0d128e38cb1a)


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


sed -n -e '3p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/d003d6f2-1960-45c0-a09b-887e49c4959a)



sed -n -e '$p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/881bc831-7b7d-4c75-9083-6037d2b032cb)



sed  -e 's/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/ff4c70f6-07fc-461f-8faa-577289226449)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/8c4dffea-7b85-4355-adcf-5f649ad09052)



sed  '/tom/s/5000/6000/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/adc7da01-e789-4f9a-a681-3daa4ef4c58c)


sed -n -e '1,5p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/27c1bb15-3180-48ca-84b9-90d6859e30c3)



sed -n -e '2,/Joe/p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/ef5f9fdb-8301-4304-9d37-1652a29c8a01)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/40140806-22e7-4b7a-811e-b33571572d5e)


seq 10 
## OUTPUT
```
1
2
3
4
5
6
7
8
9
10
```

seq 10 | sed -n '4,6p'
## OUTPUT
```
4
5
6
```


seq 10 | sed -n '2,~4p'
## OUTPUT
```
2
3
4
```


seq 3 | sed '2a hello'
## OUTPUT
```
1
2
hello
3
```


seq 2 | sed '2i hello'
## OUTPUT
```
1
hello
2
```
seq 10 | sed '2,9c hello'
## OUTPUT
```
1
hello
10
```
sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
```
$1001 | Ram | 10000 | HR
$1002 | tom |  5000 | Admin
$1003 | Joe |  7000 | Developer
```


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
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
```


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

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
 ```
www.yahoo.com
www.google.com
www.mrcet.com
```

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
```
www.yahoo.com
www.google.com
www.mrcet.com
```

#Backup commands
tar -cvf backup.tar *
## OUTPUT
![image](https://github.com/user-attachments/assets/3e5d78d4-e355-4516-b0de-3601f0201f12)

mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT

![image](https://github.com/user-attachments/assets/7abf1f6c-9761-45e0-b9f9-e6cc5e87895e)



gzip backup.tar

ls .gz
## OUTPUT
```
argshift1.sh   file11        fornested1.sh  OS-Linux-commands-Shell-script
argshift.sh    file2         funcex.sh      palindrome.sh
backupdir      file21        herecheck.txt  psswdperm.sh
backup.tar.gz  file22        ifcompound.sh  scriptest.sh
casecheck.sh   file23        ifnested1.sh   strcomp.sh
cities         forbreak.sh   ifnested.sh    untiltest.sh
data.dat       forctype.sh   iftest.sh      urllist.txt
elifcheck.sh   forin1.sh     my-script.sh   whiletest
exread1.sh     forin2.sh     nc.awk         whiletest.sh
exread.sh      forin3.sh     newfile
file1          forinfile.sh  one
```
gunzip backup.tar.gz 
gunzip backup.tar.gz
## OUTPUT
```
argshift1.sh   file11        fornested1.sh  OS-Linux-commands-Shell-script
argshift.sh    file2         funcex.sh      palindrome.sh
backupdir      file21        herecheck.txt  psswdperm.sh
backup.tar.gz  file22        ifcompound.sh  scriptest.sh
casecheck.sh   file23        ifnested1.sh   strcomp.sh
cities         forbreak.sh   ifnested.sh    untiltest.sh
data.dat       forctype.sh   iftest.sh      urllist.txt
elifcheck.sh   forin1.sh     my-script.sh   whiletest
exread1.sh     forin2.sh     nc.awk         whiletest.sh
exread.sh      forin3.sh     newfile
file1          forinfile.sh  one
(base) sec@sec-ThinkPad-E15-Gen-4:~/os/ex01/backupdir$ gunzip backup.tar.gz
(base) sec@sec-ThinkPad-E15-Gen-4:~/os/ex01/backupdir$ ls
argshift1.sh  file11        fornested1.sh  OS-Linux-commands-Shell-script
argshift.sh   file2         funcex.sh      palindrome.sh
backupdir     file21        herecheck.txt  psswdperm.sh
backup.tar    file22        ifcompound.sh  scriptest.sh
casecheck.sh  file23        ifnested1.sh   strcomp.sh
cities        forbreak.sh   ifnested.sh    untiltest.sh
data.dat      forctype.sh   iftest.sh      urllist.txt
elifcheck.sh  forin1.sh     my-script.sh   whiletest
exread1.sh    forin2.sh     nc.awk         whiletest.sh
exread.sh     forin3.sh     newfile
file1         forinfile.sh  one
```
 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT


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
```
./scriptest.sh: line 1: #!/bin/sh: No such file or directory
“File name is ./scriptest.sh ”
File name is  scriptest.sh
“First arg. is ” 1
“Second arg. is ” 2
“Third arg. is ” 3
“Fourth arg. is ”
The $@ is  1 2 3
The $\# is  1#
The $$ is  14337
    PID TTY          TIME CMD
  13614 pts/1    00:00:00 bash
  14337 pts/1    00:00:00 bash
  14340 pts/1    00:00:00 ps
```
 
ls file1
## OUTPUT
```
file1
echo $?
```
echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
```
127
abcd
 ```
echo $?
 ## OUTPUT
```
127
```

 
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
```
./strcomp.sh: line 1: #!/bin/bash: No such file or directory
baseball is less than hockey
./strcomp.sh: line 10: ^d: command not found
```

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
```
./ifnested.sh: line 1: #!/bin/bash: No such file or directory
“/home/sec The object exists, is it a file?”
“No,/home/sec it is not a file!”
“But /home/sec/.bash_history is a file!”
./ifnested.sh: line 18: ^d: command not found
```


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
##OUTPUT

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
##OUTPUT

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
 ```
 ./argshift.sh 1 2 3
 + ((  3  ))
+ echo 1
1
+ shift
+ ((  2  ))
+ echo 2
2
+ shift
+ ((  1  ))
+ echo 3
3
+ shift
+ ((  0  ))
+ set +x
```
 
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
```
 7 	 bcdfghj
8 	 abcdfghj
7 	 bcdfghj
8 	 ebcdfghj
7 	 bcdfghj
8 	 ibcdfghj
7 	 bcdfghj
8 	 obcdfghj
7 	 bcdfghj
8 	 ubcdfghj
total characters 75
Number of Lines are 10
No of Words count: 10
``` 
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
```
Enter the number
45
Number is NOT palindrome
```

# RESULT:
The Commands are executed successfully.
