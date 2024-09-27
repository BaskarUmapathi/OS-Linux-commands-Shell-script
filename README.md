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
![image](https://github.com/user-attachments/assets/2e2dcde0-db9c-4fd0-997e-2a66636e63b6)

cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```
![image](https://github.com/user-attachments/assets/bb5d6958-a366-46bc-90e6-69057382852e)

### Display the content of the files
cat < file1
## OUTPUT

![image](https://github.com/user-attachments/assets/d011b797-4c53-44dc-a089-ab6e2ffcffb0)

cat < file2
## OUTPUT

![image](https://github.com/user-attachments/assets/886db0bd-f5c5-4afc-9c8b-7910f701e160)

# Comparing Files
cmp file1 file2
## OUTPUT
 ![image](https://github.com/user-attachments/assets/9c3ad246-5a3f-4162-b6b3-64a9a372318c)

comm file1 file2
 ## OUTPUT
![image](https://github.com/user-attachments/assets/ec63a94e-97d4-4fa8-9a0e-744b70344de3)

 
diff file1 file2
## OUTPUT
![image](https://github.com/user-attachments/assets/cefd9015-b27a-407b-b9de-2ba0ce70b7d9)


#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```
![image](https://github.com/user-attachments/assets/b93f3368-94bd-4759-97d8-21530a17ee2d)

cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```
![image](https://github.com/user-attachments/assets/e8072b14-2063-4a4d-9e7e-8db2f6b36fb8)

cut -c1-3 file11
## OUTPUT

![image](https://github.com/user-attachments/assets/ed2a7190-b03f-4463-95b2-c1cf716d1b2c)

cut -d "|" -f 1 file22
## OUTPUT

![image](https://github.com/user-attachments/assets/04fdb41b-7f25-45be-86f3-f9f0c698f51b)

cut -d "|" -f 2 file22
## OUTPUT

![image](https://github.com/user-attachments/assets/a77e8daa-03c5-415f-889c-6adc93caf4a2)

cat < newfile 
```
Hello world
hello world
^d
````
![image](https://github.com/user-attachments/assets/b21de201-bfdb-4f55-97a9-f2de14897afa)

cat > newfile 
Hello world
hello world

 ![image](https://github.com/user-attachments/assets/0be41c2b-5a92-4c18-b342-2183551b458d)

grep Hello newfile
grep hello newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/8721e0bd-72e0-4c66-9307-08f0a3946982)

grep -v hello newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/7afe6638-0bc4-40fb-b631-3fa3b977994b)

cat newfile | grep -i "hello"
## OUTPUT

![image](https://github.com/user-attachments/assets/dcb5a76b-557c-4f5f-8191-024de45f4a05)

cat newfile | grep -i -c "hello"
## OUTPUT

![image](https://github.com/user-attachments/assets/f8e5c8b5-16b9-48fa-899e-12f343802150)

grep -R ubuntu /etc
## OUTPUT

![image](https://github.com/user-attachments/assets/194d3843-4b0a-45ee-b7c3-af24f027dbb1)

grep -w -n world newfile   
## OUTPUT

![image](https://github.com/user-attachments/assets/803bd8af-59ed-4fff-ac39-da9831c8f85f)

cat < newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```
![image](https://github.com/user-attachments/assets/20c66dca-0665-4773-a808-c9f5525d6c74)

cat > newfile
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 ```
![image](https://github.com/user-attachments/assets/af3b7dd2-f2a2-4734-bbb9-d29923761993)

egrep -w 'Hello|hello' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/6aebf2bc-9bf6-4e65-a361-d084543ebaca)

egrep -w '(H|h)ello' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/486801d9-9d25-4685-94ca-a30a45782f6f)

egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/4dbd51d4-5f0f-42ce-812b-b2079bcf2369)

egrep '(^hello)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/e4ec62c7-5b52-471f-9fc4-deab4fe0016a)

egrep '(world$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/aac9b258-6d6d-46ef-a700-862ba7446733)

egrep '(World$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/8639d2b3-4235-498f-87db-d81481088a08)

egrep '((W|w)orld$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/244da231-b511-4d5c-b5eb-2a19c91f2202)

egrep '[1-9]' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/2fa51854-9c88-4c4b-9e46-9eb0feabf307)

egrep 'Linux.*world' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/b65c1c09-3b5d-431a-a1e1-fec32a7b261d)

egrep 'Linux.*World' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/eece6261-4fbb-4f0c-b274-488401db4459)

egrep l{2} newfile
## OUTPUT

![image](https://github.com/user-attachments/assets/83fdd0e7-4165-4dcd-b123-7dc1e153cb21)

egrep 's{1,2}' newfile
## OUTPUT 

![image](https://github.com/user-attachments/assets/b54a1e17-0bad-4e3d-87bd-9c80d4e089f9)

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

![image](https://github.com/user-attachments/assets/25d0f3bf-10c2-4c80-aa53-66cb2dbfcf79)

sed -n -e '$p' file23

## OUTPUT
![image](https://github.com/user-attachments/assets/9e9b671d-98b8-4d0a-ab18-f3df84ebe4fb)

sed  -e 's/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/57fbd95c-ca4d-4c8e-b19e-810a7148914a)

sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/edbaa823-b6b7-44f4-bae9-9af2a9ac2d9f)

sed  '/tom/s/5000/6000/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/6b109bb2-188d-40c3-8612-ff734ebb2459)

sed -n -e '1,5p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/90973766-1b21-4c19-b9a9-9955d06f264a)

sed -n -e '2,/Joe/p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/9d722478-6db9-4937-901f-45b06e852e95)

sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/d6cdf7c6-5867-49af-8d46-cb25c090493b)

seq 10 
## OUTPUT

![image](https://github.com/user-attachments/assets/49097e51-7504-4adb-bc46-bc17d5bec26a)

seq 10 | sed -n '4,6p'
## OUTPUT

![image](https://github.com/user-attachments/assets/982c21db-4409-46e8-9f63-5ceacd82cced)

seq 10 | sed -n '2,~4p'
## OUTPUT

![image](https://github.com/user-attachments/assets/499e9aae-c63b-4d46-89ea-ccce1c7e2473)

seq 3 | sed '2a hello'
## OUTPUT

![image](https://github.com/user-attachments/assets/4d97f8f4-f693-4794-9501-b6390aa966d3)

seq 2 | sed '2i hello'
## OUTPUT

![image](https://github.com/user-attachments/assets/a2df4962-7652-4fd4-8ea9-3650151836f6)

seq 10 | sed '2,9c hello'
## OUTPUT

![image](https://github.com/user-attachments/assets/1d0866bd-dc2e-42d8-b1da-721bf8354929)

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/40c9f1a6-c069-4ff5-bd13-c52a226e69a9)

sed -n '2,4{s/$/*/;p}' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/40961369-382f-4791-a6ac-1db6155fe65d)

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

![image](https://github.com/user-attachments/assets/41cf872f-c0fe-4a43-bd9a-5550fcad927c)

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

![image](https://github.com/user-attachments/assets/e9bc108a-c451-46c4-b8cd-f57be0fde2b0)

#Using tr command

cat file23 | tr [:lower:] [:upper:]
## OUTPUT

![image](https://github.com/user-attachments/assets/b7b8c95a-dcef-4363-8c4f-a2ceba4a9d07)

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

![image](https://github.com/user-attachments/assets/d9e36930-0cca-4cf0-963d-a79c08ea5038)
 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![image](https://github.com/user-attachments/assets/53a242fe-5a16-4adb-b42b-8cad143ed0c1)

#Backup commands
tar -cvf backup.tar *
## OUTPUT

![image](https://github.com/user-attachments/assets/f5826540-61ad-4152-aea3-15cf8d56d7b2)

mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT

![image](https://github.com/user-attachments/assets/aa9310c6-e6f6-42ae-9b74-61e00eea841b)

tar -xvf backup.tar
## OUTPUT

![image](https://github.com/user-attachments/assets/4b0404d6-f2de-417f-8da0-01f906327e88)

gzip backup.tar
## OUTPUT

![image](https://github.com/user-attachments/assets/446b3219-93d4-4f63-8cf4-3181893d43fe)

ls .gz
## OUTPUT

![image](https://github.com/user-attachments/assets/1f8bf07a-8f5f-4a49-a59f-df42006a54ea)

gunzip backup.tar.gz
## OUTPUT

![image](https://github.com/user-attachments/assets/994ffe6d-d736-4a16-89e5-db678b397d64)
 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

![image](https://github.com/user-attachments/assets/c7a6a468-86e3-4c25-a5ef-c8b41a2c976b)

![image](https://github.com/user-attachments/assets/3c681bfd-e0f9-4417-a36e-0b07fe9deda8)

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

![image](https://github.com/user-attachments/assets/dd87b3e5-6562-41b7-932e-4693ba743b95)

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

![image](https://github.com/user-attachments/assets/8abfcdb0-332f-42de-80da-7dbfb938e8ef)

ls file1
## OUTPUT

![image](https://github.com/user-attachments/assets/58ed7c0a-0ff8-473f-8610-5a487a1abe4b)

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
 ## OUTPUT

![image](https://github.com/user-attachments/assets/13d10dce-debf-4a69-a9c5-00ccdb7d2c13)
 
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
## OUTPUT

![image](https://github.com/user-attachments/assets/d458f47c-9c87-4f9d-ae88-4db75d1b9b43)

chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

![image](https://github.com/user-attachments/assets/1171921b-8c22-489c-8a92-a59339d3d152)

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

![image](https://github.com/user-attachments/assets/357dc885-263f-4892-9da2-7db649f33553)

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

![image](https://github.com/user-attachments/assets/b1c629f9-ee13-4ed9-b6b8-2f57dc0e19ed)

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
## OUTPUT

![image](https://github.com/user-attachments/assets/42e4ffa6-20ae-4470-81c0-effd9fdb59eb)

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
## OUTPUT

![image](https://github.com/user-attachments/assets/b939d5fa-dd09-4413-8703-fba4caa4f60c)

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

![image](https://github.com/user-attachments/assets/c58920d8-d1ac-40ce-8bbe-034663163b08)

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

![image](https://github.com/user-attachments/assets/4ec537a1-e213-430a-b0c7-bef15789e4f0)

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

![image](https://github.com/user-attachments/assets/19e583b7-b353-407e-8448-765b937fc396)

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

![image](https://github.com/user-attachments/assets/6d60458d-90c2-4261-8b13-c21f7a88ee39)

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

![image](https://github.com/user-attachments/assets/1b184161-681c-44ec-8f24-4777600998aa)

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

![image](https://github.com/user-attachments/assets/6a983832-864a-45ac-9107-0a3a34e1e8bd)
 
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

![image](https://github.com/user-attachments/assets/98d5efa3-0284-41c1-88ae-de379c5c042c)

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

![image](https://github.com/user-attachments/assets/f057efeb-504d-4fd3-a976-0e7bb7a63b53)

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

![image](https://github.com/user-attachments/assets/58070457-02e5-42da-a048-62c8851e4a34)

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

![image](https://github.com/user-attachments/assets/854b5384-a278-4ce6-acee-24b073822edd)

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

![image](https://github.com/user-attachments/assets/0885cd08-f154-4186-8718-e3e19d9fdf50)

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

![image](https://github.com/user-attachments/assets/bc84423e-f49c-4308-97c6-571cbf90be33)

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

![image](https://github.com/user-attachments/assets/0a41d904-0116-41da-a3e8-6dd1e89bbf71)

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

![image](https://github.com/user-attachments/assets/f78294ac-bf70-47df-b4fa-38b889c4834d)

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

![image](https://github.com/user-attachments/assets/f2af533f-51ab-4816-82fe-f17d47922a41)
 
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

![image](https://github.com/user-attachments/assets/c13d4ccf-04e9-4105-adaa-1976a140f9aa)

# RESULT:
The Commands are executed successfully.
