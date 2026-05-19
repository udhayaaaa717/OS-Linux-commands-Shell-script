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
<img width="822" height="287" alt="image" src="https://github.com/user-attachments/assets/e912604c-8a4e-4b51-beed-5c62d78b7dfb" />



cat < file2
## OUTPUT
<img width="737" height="176" alt="image" src="https://github.com/user-attachments/assets/597135fe-0a71-4110-9fd2-403bbf710d2d" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="800" height="197" alt="image" src="https://github.com/user-attachments/assets/ab2fd1c1-38f5-4771-ab11-f9c54a05bcd4" />

comm file1 file2
 ## OUTPUT
<img width="767" height="176" alt="image" src="https://github.com/user-attachments/assets/01e92cd5-3e54-4481-958b-3cda05cc1238" />

 
diff file1 file2
## OUTPUT
<img width="720" height="256" alt="image" src="https://github.com/user-attachments/assets/25f69cf5-15e9-43d0-944a-b44347ce7d62" />


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
<img width="887" height="112" alt="image" src="https://github.com/user-attachments/assets/696e5908-d6d3-45ab-ae80-6a736160fc71" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="787" height="250" alt="image" src="https://github.com/user-attachments/assets/ba3db8ae-2700-4c03-9b42-9c3957d38ebc" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="782" height="166" alt="image" src="https://github.com/user-attachments/assets/fc880df1-0913-4909-8f2b-c058368f0352" />


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
<img width="781" height="172" alt="image" src="https://github.com/user-attachments/assets/97585cda-8c4f-4c13-a993-1d2b233dfc93" />



grep hello newfile 
## OUTPUT

<img width="782" height="166" alt="image" src="https://github.com/user-attachments/assets/e857db65-cb2a-42ea-955c-246c95e8af42" />



grep -v hello newfile 
## OUTPUT
<img width="786" height="147" alt="image" src="https://github.com/user-attachments/assets/e8b2f502-0839-4dd5-81c5-6c0492692353" />



cat newfile | grep -i "hello"
## OUTPUT

<img width="887" height="136" alt="image" src="https://github.com/user-attachments/assets/1726496e-2fa5-4664-bd62-791af7137ae0" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="807" height="135" alt="image" src="https://github.com/user-attachments/assets/283e9300-f079-44c9-8652-fdea65262515" />



grep -R ubuntu /etc
## OUTPUT



grep -w -n world newfile   
## OUTPUT
<img width="822" height="120" alt="image" src="https://github.com/user-attachments/assets/80b6b332-8db8-4295-b65e-76d3a3438aba" />


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

<img width="677" height="51" alt="image" src="https://github.com/user-attachments/assets/2b5a04e1-b64e-4b23-a438-ae7ddf2f4ecf" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="666" height="47" alt="image" src="https://github.com/user-attachments/assets/cca922ee-9e08-431e-af77-16e1994fb850" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="682" height="51" alt="image" src="https://github.com/user-attachments/assets/b1dcf375-2f8e-461c-9923-00d962fa0ea7" />



egrep '(^hello)' newfile 
## OUTPUT
<img width="621" height="31" alt="image" src="https://github.com/user-attachments/assets/e5801b5d-5cec-4fd5-8ea8-45dfb94383e7" />



egrep '(world$)' newfile 
## OUTPUT



egrep '(World$)' newfile 
## OUTPUT
<img width="626" height="35" alt="image" src="https://github.com/user-attachments/assets/674ab788-136d-49d0-bc40-61d5330ff021" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="662" height="71" alt="image" src="https://github.com/user-attachments/assets/1e691a8c-3107-4729-8805-0234bd79adac" />



egrep '[1-9]' newfile 
## OUTPUT

<img width="606" height="32" alt="image" src="https://github.com/user-attachments/assets/bd774bed-e06b-4957-944a-4f0a7936e327" />


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="667" height="31" alt="image" src="https://github.com/user-attachments/assets/73b244d7-4005-4f0d-9a7a-69fe3c9c9428" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="665" height="36" alt="image" src="https://github.com/user-attachments/assets/da55eeb1-ac5c-4072-88b9-2733ea227962" />


egrep l{2} newfile
## OUTPUT
<img width="567" height="50" alt="image" src="https://github.com/user-attachments/assets/cfdec816-dc89-4cf6-8434-5ca0deafc81a" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="607" height="67" alt="image" src="https://github.com/user-attachments/assets/75b70d0a-2c4d-4365-be23-9f7698098382" />


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

<img width="606" height="32" alt="image" src="https://github.com/user-attachments/assets/9d04610b-a1e6-44a1-bf4a-af80b01ed656" />


sed -n -e '$p' file23
## OUTPUT
<img width="600" height="35" alt="image" src="https://github.com/user-attachments/assets/4ad0d257-a288-4370-bc87-a754478a2b02" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="647" height="162" alt="image" src="https://github.com/user-attachments/assets/14b5a758-c7d9-443b-a5f9-54e00a306fe7" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="657" height="157" alt="image" src="https://github.com/user-attachments/assets/e39a05c0-9473-422d-a263-b6a2d51b106c" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="660" height="161" alt="image" src="https://github.com/user-attachments/assets/26e5cff7-f462-4ea9-98f0-deb8e0bee767" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="606" height="106" alt="image" src="https://github.com/user-attachments/assets/a7bf2f6a-bcd7-4964-9439-033caf39ad5d" />


sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="647" height="72" alt="image" src="https://github.com/user-attachments/assets/12ae0d70-1150-46db-975c-33db23eed8da" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="692" height="52" alt="image" src="https://github.com/user-attachments/assets/bc6ab26b-7aff-4868-942d-7085681f3a01" />


seq 10 
## OUTPUT

<img width="455" height="197" alt="image" src="https://github.com/user-attachments/assets/2acde4f4-92e7-47d2-87bc-fa70504d6546" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="607" height="70" alt="image" src="https://github.com/user-attachments/assets/6ad45755-1fbf-4c9c-bd42-ef8a628eaba8" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="602" height="66" alt="image" src="https://github.com/user-attachments/assets/2b467f44-b874-4bdc-9755-e8229e8d8897" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="597" height="85" alt="image" src="https://github.com/user-attachments/assets/7638cf3c-29fc-4da8-b56b-e4b3ba07c9d5" />


seq 2 | sed '2i hello'
## OUTPUT
<img width="602" height="70" alt="image" src="https://github.com/user-attachments/assets/b4f63703-f620-4091-b176-d89432c47190" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="622" height="72" alt="image" src="https://github.com/user-attachments/assets/64af9e95-ebbd-4727-938a-f23e63815a87" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="667" height="72" alt="image" src="https://github.com/user-attachments/assets/afb5f479-5680-4341-b6d5-75ea6dc14fe9" />


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
<img width="515" height="105" alt="image" src="https://github.com/user-attachments/assets/af24ab0b-566d-406a-b4f5-714d91844653" />


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
<img width="705" height="146" alt="image" src="https://github.com/user-attachments/assets/f2b65800-5b11-4b1c-8c76-94c4c6f65f76" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="716" height="150" alt="image" src="https://github.com/user-attachments/assets/71026f4d-2d2a-4ccf-9fdb-a4de5d2dab3a" />

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
<img width="636" height="76" alt="image" src="https://github.com/user-attachments/assets/283d45a4-cc03-446e-baa0-b6539ffcc389" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="762" height="72" alt="image" src="https://github.com/user-attachments/assets/76648024-759b-4c59-aae7-d72b91a67c34" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="602" height="472" alt="image" src="https://github.com/user-attachments/assets/48632cfb-6e6d-4800-8ef2-92463894ffbc" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="840" height="467" alt="image" src="https://github.com/user-attachments/assets/31331769-470f-41bf-90c9-566fa7e54934" />


tar -xvf backup.tar
## OUTPUT
<img width="572" height="467" alt="image" src="https://github.com/user-attachments/assets/eb009898-d470-4a57-9a53-270e1b7d5fae" />

gzip backup.tar

ls .gz
## OUTPUT
<img width="927" height="107" alt="image" src="https://github.com/user-attachments/assets/90c4a490-35f3-4966-b8b6-84d1dda63f92" />
 
gunzip backup.tar.gz
## OUTPUT
<img width="920" height="105" alt="image" src="https://github.com/user-attachments/assets/3ac3f61f-f6d2-4c42-a5a5-9d9ff8fc9eb7" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 <img width="912" height="152" alt="image" src="https://github.com/user-attachments/assets/4139b0f3-367f-4380-a77f-6ce367c3940f" />

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
<img width="921" height="531" alt="image" src="https://github.com/user-attachments/assets/b7bcf674-dfd4-4311-a924-d60c97f856b5" />

 
ls file1
## OUTPUT
<img width="487" height="37" alt="image" src="https://github.com/user-attachments/assets/5aecec7b-66b8-463c-808a-2f41291727c4" />

echo $?
## OUTPUT 
<img width="480" height="32" alt="image" src="https://github.com/user-attachments/assets/aec66756-11e2-4b34-9726-e4e6dc3cd7ec" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT
<img width="477" height="202" alt="image" src="https://github.com/user-attachments/assets/dab4ae49-b172-4dec-ac7f-c0ae7c30fc00" />


 
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
<img width="917" height="205" alt="image" src="https://github.com/user-attachments/assets/78dee4a2-1f4e-4803-8d5d-95c75f64828a" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="892" height="47" alt="image" src="https://github.com/user-attachments/assets/594d03c8-2968-4cf0-8d05-f715e535506b" />


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
<img width="892" height="47" alt="image" src="https://github.com/user-attachments/assets/78d42149-80f5-4361-93e5-c7e96f7fee8d" />

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
<img width="882" height="77" alt="image" src="https://github.com/user-attachments/assets/2bb53d68-15bc-4161-a424-2ab3ce967c61" />



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
<img width="892" height="42" alt="image" src="https://github.com/user-attachments/assets/462a1305-1206-40b4-97ce-69c94207fee9" />

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
<img width="907" height="42" alt="image" src="https://github.com/user-attachments/assets/9dfaa25f-2f74-4730-86ba-65a29c321866" />

## OUTPUT
<img width="901" height="227" alt="image" src="https://github.com/user-attachments/assets/bcc34b07-6ae3-4ca7-9707-b2f1f2c91f4b" />


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
<img width="906" height="87" alt="image" src="https://github.com/user-attachments/assets/b30d8af0-56e6-4773-a68a-9398996ec5da" />

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
<img width="856" height="137" alt="image" src="https://github.com/user-attachments/assets/eaa2e1e0-b04e-4f23-843a-e9ffde8d300b" />

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
<img width="857" height="82" alt="image" src="https://github.com/user-attachments/assets/1a9b9e75-b660-49c7-a269-0d4cd77f0f04" />

 
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
<img width="867" height="161" alt="image" src="https://github.com/user-attachments/assets/c43edcc1-ca51-4074-96c9-a748f5dd2a45" />

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
 <img width="877" height="42" alt="image" src="https://github.com/user-attachments/assets/eed4109d-b3f8-403f-9822-e8ccf1a885ed" />

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
<img width="867" height="42" alt="image" src="https://github.com/user-attachments/assets/1ea2576f-8ad1-4a5b-8e74-a6b4a15e43b9" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="891" height="112" alt="image" src="https://github.com/user-attachments/assets/ba6d7323-0285-48d3-95fb-9aaff0fdf8ef" />


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
<img width="892" height="120" alt="image" src="https://github.com/user-attachments/assets/dd8a5e18-a74a-4cbe-89d9-f382fe3b6035" />

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
<img width="897" height="252" alt="image" src="https://github.com/user-attachments/assets/eb9b2541-3259-4541-8dce-2aff78218cec" />

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
<img width="882" height="71" alt="image" src="https://github.com/user-attachments/assets/99021896-7845-4767-8918-f561789678de" />

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
 <img width="887" height="72" alt="image" src="https://github.com/user-attachments/assets/8fe6bc6c-5a39-486d-8867-72c92cebb9cd" />

 
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
 <img width="912" height="117" alt="image" src="https://github.com/user-attachments/assets/dca577d5-ad73-4dc0-b0b6-974c8de7e0f9" />

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
<img width="912" height="81" alt="image" src="https://github.com/user-attachments/assets/4c644a6e-f5c9-44da-9fa1-00a9f9eb424d" />


# RESULT:
The Commands are executed successfully.
