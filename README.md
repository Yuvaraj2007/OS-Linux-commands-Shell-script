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
<img width="987" height="120" alt="361642083-a46cf7a2-8904-4026-9e31-4282a06d3bd2" src="https://github.com/user-attachments/assets/9cb72abd-4502-47c8-85dd-13ccdb26485b" />



cat < file2
## OUTPUT
<img width="1032" height="123" alt="361642084-a45738a3-c970-4ae5-b0e2-9a95e7df6f82" src="https://github.com/user-attachments/assets/f1957fc7-a10a-468f-9c4f-52a06c5008cb" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="1123" height="53" alt="361642104-311cdc62-0f68-4e0d-b418-366e735fa865" src="https://github.com/user-attachments/assets/f198e718-2edd-49c2-81cc-9c24ca0b8c21" />

comm file1 file2
 ## OUTPUT
<img width="1027" height="190" alt="361642134-af3d5c01-e7d5-46e9-b2ec-dff1be315a68" src="https://github.com/user-attachments/assets/94d1cdb8-d52d-4b81-831e-5106ff8cee7d" />

 
diff file1 file2
## OUTPUT
<img width="992" height="241" alt="361642166-5d596308-c99a-49de-a67b-42897f56dbec" src="https://github.com/user-attachments/assets/f38358d2-4632-4a82-8d3b-5935d84e0464" />


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
<img width="1047" height="73" alt="361642220-3e373e45-f0b6-42bf-87c2-317e5fff7c43" src="https://github.com/user-attachments/assets/210f1a19-e146-45a9-b8f2-c76df37b04af" />




cut -d "|" -f 1 file22
## OUTPUT

<img width="982" height="96" alt="361642242-a34a8423-ad78-4706-8759-8438909f0c7c" src="https://github.com/user-attachments/assets/7f084b55-7e1f-44f9-8c2e-1111adbdfd2b" />


cut -d "|" -f 2 file22
## OUTPUT

<img width="977" height="93" alt="361642259-743e8292-3b87-4c01-a8d5-3002fc3ec594" src="https://github.com/user-attachments/assets/735a0127-bae1-4d6a-a500-c6d99c6e75b9" />


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
<img width="1072" height="46" alt="361642284-1b4e6456-29e0-4e22-8888-4fb7ff342570" src="https://github.com/user-attachments/assets/351a4e71-5862-418f-bf2c-3d2a5153b66d" />



grep hello newfile 
## OUTPUT

<img width="1055" height="56" alt="361642319-889a0985-dc9a-4757-8e1f-beae667d656f" src="https://github.com/user-attachments/assets/1b25a29d-7b93-48de-b0ce-4e77800ecbf0" />



grep -v hello newfile 
## OUTPUT


<img width="1081" height="48" alt="361642349-ce15902a-dd21-4d4b-a4b9-ec796d7ff79b" src="https://github.com/user-attachments/assets/8a86930f-b718-4c46-8bfc-06d02fe8517e" />

cat newfile | grep -i "hello"
## OUTPUT

<img width="1046" height="72" alt="361642430-6926a1b2-3022-4195-9781-ed4641a3b096" src="https://github.com/user-attachments/assets/b02fcd4e-01e1-4ed4-b861-ff17474bd88f" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="1009" height="47" alt="361642429-3cbcdd09-feec-4f60-bd8a-f8c5fe451d30" src="https://github.com/user-attachments/assets/03e3b998-575d-4aab-be71-2b50f795bef1" />



grep -R ubuntu /etc
## OUTPUT
<img width="1112" height="114" alt="361643991-5f5d6e5d-c2ed-45ee-b727-0c8da1f2c861" src="https://github.com/user-attachments/assets/7748e8a2-4356-41a8-a19d-4ff1a8a4b8b7" />



grep -w -n world newfile   
## OUTPUT

<img width="1289" height="446" alt="361643787-c058bccd-1f9c-4b57-9c85-df12001ebefa" src="https://github.com/user-attachments/assets/0cdc1e9f-c9ec-4738-8f56-cc777a97bcbf" />


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
<img width="995" height="73" alt="361646171-99e8082e-aaea-4fc3-824f-0e07119e5ac5" src="https://github.com/user-attachments/assets/bcbe84cc-f8a7-487c-b62d-4d4cc5e1b2d7" />



egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="957" height="74" alt="361646204-58c94a4e-82cd-4b0a-8f95-fb946f6e142f" src="https://github.com/user-attachments/assets/7ae7c525-356c-416b-9169-fa15df0f5cad" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="961" height="71" alt="361646230-b7f97786-61fe-4ff6-8049-e1c1d82291ce" src="https://github.com/user-attachments/assets/49a8acad-ea25-4184-b8a5-ff98e64f49e1" />



egrep '(^hello)' newfile 
## OUTPUT
<img width="961" height="55" alt="361646259-0919b3a9-9da6-464a-b320-9b35df8c207a" src="https://github.com/user-attachments/assets/6061b918-cb0e-4a0d-a5eb-92def5da70b0" />



egrep '(world$)' newfile 
## OUTPUT



egrep '(World$)' newfile 
## OUTPUT


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="958" height="103" alt="361646452-afb4d196-4ef2-46a2-be8d-e17a8094b1b8" src="https://github.com/user-attachments/assets/dc5b093b-1da1-450f-8409-f7a967176c57" />


egrep '[1-9]' newfile 
## OUTPUT
<img width="959" height="51" alt="361646453-92eafde7-a18b-4835-a9c5-775913d93ac5" src="https://github.com/user-attachments/assets/06d941be-7a2d-44e5-b4f0-dffba6beb1bd" />



egrep 'Linux.*world' newfile 
## OUTPUT

<img width="957" height="79" alt="361646451-2cb27590-c84d-44f3-9f8e-e1ab7070740b" src="https://github.com/user-attachments/assets/69ec5a72-c071-44bc-ab74-c7043c76c4d9" />

egrep 'Linux.*World' newfile 
## OUTPUT
<img width="959" height="54" alt="361646478-c1f46d6b-d275-4a28-baee-ba66a5b656bf" src="https://github.com/user-attachments/assets/08a78d10-754d-4b3a-abcd-55c88e5c5aaf" />


egrep l{2} newfile
## OUTPUT
<img width="959" height="75" alt="361646518-cae87532-0377-46a0-aa44-64a541fd73ba" src="https://github.com/user-attachments/assets/5ca9809a-dd89-41a0-867c-fd224cd77f30" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="960" height="102" alt="361646537-7c4f3065-7a6d-4f96-9b69-0d128e38cb1a" src="https://github.com/user-attachments/assets/9c7a300a-1caf-48a8-b1d2-04ed7a06a17f" />


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

<img width="851" height="99" alt="361646955-d003d6f2-1960-45c0-a09b-887e49c4959a" src="https://github.com/user-attachments/assets/1962f0ca-4e4d-45e9-b37e-fe52aa3be640" />


sed -n -e '$p' file23
## OUTPUT
<img width="851" height="99" alt="361646976-881bc831-7b7d-4c75-9083-6037d2b032cb" src="https://github.com/user-attachments/assets/9b9b57e4-421a-456a-9d5a-d5b20373b54b" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="835" height="197" alt="361647013-ff4c70f6-07fc-461f-8faa-577289226449" src="https://github.com/user-attachments/assets/1f0af3a6-e795-4c42-b19d-04ae151a83e4" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="835" height="197" alt="361647036-8c4dffea-7b85-4355-adcf-5f649ad09052" src="https://github.com/user-attachments/assets/836dd0df-200d-4957-b165-99f06f6aa225" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="835" height="197" alt="361647072-adc7da01-e789-4f9a-a681-3daa4ef4c58c" src="https://github.com/user-attachments/assets/d9f2506e-75e1-4f89-be2a-d10c7b8189af" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="838" height="148" alt="361647099-27c1bb15-3180-48ca-84b9-90d6859e30c3" src="https://github.com/user-attachments/assets/b87762c2-a1ec-4766-8c50-1479ef0599ec" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="838" height="105" alt="361647122-ef5f9fdb-8301-4304-9d37-1652a29c8a01" src="https://github.com/user-attachments/assets/fb7a02eb-680e-4b09-b5bb-c5201d0749da" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="1142" height="1000" alt="362677417-40140806-22e7-4b7a-811e-b33571572d5e" src="https://github.com/user-attachments/assets/7672aeff-5441-4844-9a7f-ca7981aeb26f" />



seq 10 
## OUTPUT

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

seq 10 | sed -n '4,6p'
## OUTPUT

4
5
6

seq 10 | sed -n '2,~4p'
## OUTPUT

2
3
4

seq 3 | sed '2a hello'
## OUTPUT
1
hello
2


seq 2 | sed '2i hello'
## OUTPUT
1
hello
10

seq 10 | sed '2,9c hello'
## OUTPUT
$1001 | Ram | 10000 | HR
$1002 | tom |  5000 | Admin
$1003 | Joe |  7000 | Developer

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev


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
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev


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
www.yahoo.com
www.google.com
www.mrcet.com

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

www.yahoo.com
www.google.com
www.mrcet.com

#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="1033" height="577" alt="362677477-3e5d78d4-e355-4516-b0de-3601f0201f12" src="https://github.com/user-attachments/assets/0c298d03-ec88-4423-920a-75e4406757ce" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar



tar -xvf backup.tar
## OUTPUT
<img width="1145" height="879" alt="362677723-7abf1f6c-9761-45e0-b9f9-e6cc5e87895e" src="https://github.com/user-attachments/assets/a3012d78-1e43-4216-b057-a0f37120dbe1" />

gzip backup.tar

ls .gz
## OUTPUT
 
gunzip backup.tar.gz
## OUTPUT

 
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

 
ls file1
## OUTPUT

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT


 
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


# RESULT:
The Commands are executed successfully.
