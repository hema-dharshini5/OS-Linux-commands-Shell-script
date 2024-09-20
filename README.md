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

![image](https://github.com/user-attachments/assets/6293bd51-1f68-4187-b459-936b2f2ba813)

cat < file2
## OUTPUT

![image](https://github.com/user-attachments/assets/d0722ff7-e8a8-49b6-b906-79d0d9768cb7) 

# Comparing Files
cmp file1 file2
## OUTPUT
![image](https://github.com/user-attachments/assets/faa5e325-ce88-4695-a929-55b4aa16c56c) 

comm file1 file2
 ## OUTPUT

![image](https://github.com/user-attachments/assets/ae8f2666-f6e0-442b-8d30-16a90fd00c28) 

diff file1 file2
## OUTPUT
![image](https://github.com/user-attachments/assets/c17aba4b-b3ab-4ba7-b57b-191aa4e277c4)

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

![image](https://github.com/user-attachments/assets/08812c72-9da6-4286-9096-92201927fb58)


cut -d "|" -f 1 file22
## OUTPUT

![image](https://github.com/user-attachments/assets/6b687bf8-552f-4c37-bc55-17125ca4b9b2)

cut -d "|" -f 2 file22
## OUTPUT

![image](https://github.com/user-attachments/assets/2cabdf1e-9cdc-4a65-b1aa-88829f3319c8) 

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
![image](https://github.com/user-attachments/assets/64940eb8-d6a1-4d9d-a929-e4a54be2ad4d)


grep hello newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/485e5375-a717-49d0-a697-cbea33fe398f)



grep -v hello newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/51df6f58-2a51-410e-9860-08c0afab9932)

cat newfile | grep -i "hello"
## OUTPUT
![image](https://github.com/user-attachments/assets/bb623617-1cba-431c-b56e-e228c4fe3180)



cat newfile | grep -i -c "hello"
## OUTPUT


![image](https://github.com/user-attachments/assets/15e16b5a-4432-49a8-abd6-a96040551651)

grep -R ubuntu /etc
## OUTPUT



grep -w -n world newfile   
## OUTPUT

![image](https://github.com/user-attachments/assets/4086bd0c-8e2a-4b6c-b4a2-d34bb5532e11)
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

![image](https://github.com/user-attachments/assets/65c5cd47-1d3f-4955-9a13-6098f0eab619)

egrep -w '(H|h)ello' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/de89faea-7147-4709-8908-bfdd24bd8099)

egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/16def152-e9fd-4814-8ce3-f4d0c594e63e)


egrep '(^hello)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/602e57c8-66cf-4c24-a7c1-aedeba905d4c)




egrep '(world$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/ba393abc-70c3-4fe9-b4cb-617967f9fed9)

egrep '(World$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/d4c5f115-e0f7-4105-a6bb-d1718d9ab6c6)
egrep '((W|w)orld$)' newfile 
## OUTPUT


![image](https://github.com/user-attachments/assets/13d6e98d-c3c3-491b-a973-f5ce10a9ff4f)
egrep '[1-9]' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/aae8cd6e-8460-4ef4-bce9-9bcdb9d7e159)

egrep 'Linux.*world' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/89b330e1-b11b-4410-91c0-d26e22469f06)
egrep 'Linux.*World' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/fb571249-cd6f-4ea2-9f2c-e34355494dc3)
egrep l{2} newfile
## OUTPUT

![image](https://github.com/user-attachments/assets/b1bda169-d4ad-4870-bcf1-a7f6a276d9fc)

egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/user-attachments/assets/3a495998-e763-437a-a92a-c41c78b640de)

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
![image](https://github.com/user-attachments/assets/a5be0116-8e10-4a74-90c8-054b11b5d4f8)


sed -n -e '$p' file23
## OUTPUT


![image](https://github.com/user-attachments/assets/a8ef4875-50bb-4799-be0d-5a35ea5bdcef)
sed  -e 's/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/9d896cc9-948f-4d6a-ae90-49486f6f5ac6)

sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/1f8fffc6-2e87-4246-8e81-555aa1cf613c)

sed  '/tom/s/5000/6000/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/678bef40-e25c-45d1-bc55-4a6a57c5cb5a)

sed -n -e '1,5p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/622ab7f2-684c-4a66-ae03-dbe89dcf7a96)


sed -n -e '2,/Joe/p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/731f92c3-8b51-4b76-830f-f18f58fef1d7)


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/55803cf1-9d22-4bb7-8d6f-5a91445ac296)

seq 10 
## OUTPUT

![image](https://github.com/user-attachments/assets/3afcceba-c9eb-43bc-847e-ad613037afcc)

seq 10 | sed -n '4,6p'
## OUTPUT

![image](https://github.com/user-attachments/assets/4e0b09e0-61fa-456a-aa2e-ccbdf11b9f0a)

seq 10 | sed -n '2,~4p'
## OUTPUT
![image](https://github.com/user-attachments/assets/18506e66-4fa1-470f-82e9-000419e8d3e5)


seq 3 | sed '2a hello'
## OUTPUT

![image](https://github.com/user-attachments/assets/07d6a5d3-df5e-47d3-bddc-a7fca4dc4bf4)

seq 2 | sed '2i hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/3fa93725-d974-4cf6-8c81-5b627cc1d5c1)

seq 10 | sed '2,9c hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/7162bbb1-637a-49fd-bd21-858dd40a7d41)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/c6152e39-79cb-47f3-a20d-aae0b2271f5e)

sed -n '2,4{s/$/*/;p}' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/5dfc0437-d59e-42fa-87d5-4a6351c50e37)


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

![image](https://github.com/user-attachments/assets/1e0fd469-dd69-46f0-b66f-a0357a38be0c)

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

![image](https://github.com/user-attachments/assets/813c60b8-e614-421f-9dfb-7417c15ae45d)

#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
 
![image](https://github.com/user-attachments/assets/6fa6ef42-479b-42a0-bc0a-d8494f45ebf9) 

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

![image](https://github.com/user-attachments/assets/6a379194-1125-4110-b2d9-6394770258a7)
 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![image](https://github.com/user-attachments/assets/b2efe1ad-6ea4-4575-9211-e65e380fb64f)

#Backup commands
tar -cvf backup.tar *
## OUTPUT
![image](https://github.com/user-attachments/assets/883b2cfe-8964-493b-937e-64f1e1e7c73a)

mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT

![image](https://github.com/user-attachments/assets/c7326ccd-6089-4fe1-b86b-05f0e3ec0a09)

![image](https://github.com/user-attachments/assets/628942bc-2399-4099-9ff9-5da149561907) 

tar -xvf backup.tar
## OUTPUT
![image](https://github.com/user-attachments/assets/bed6116b-02ba-44c7-a326-d0888ba14b9d)

gzip backup.tar

ls .gz
## OUTPUT
 
gunzip backup.tar.gz
## OUTPUT

![image](https://github.com/user-attachments/assets/ca97e74f-8123-4e9a-aad8-7029c3e18f8b)
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

![image](https://github.com/user-attachments/assets/40bb45f8-8e8a-4572-bf46-8f3d2c234fda)

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

![image](https://github.com/user-attachments/assets/8a622cf7-e184-4844-990c-96e2b939b0e1) 

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

 ![image](https://github.com/user-attachments/assets/37cc22a3-0d83-4792-8cc7-b5eff9522f1f) 
 
ls file1
## OUTPUT
![image](https://github.com/user-attachments/assets/3b00f4da-cc94-4667-92d2-e5fa3f4488fa)

echo $?
## OUTPUT 
![image](https://github.com/user-attachments/assets/724a6207-5cc5-405e-8f1b-6f5b81f98c00)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
![image](https://github.com/user-attachments/assets/2c84af1c-718d-4976-8b39-423e5f5604af)
 
abcd
 
echo $?
 ## OUTPUT

![image](https://github.com/user-attachments/assets/f3a53722-6040-46c5-a8ac-452666463bf4)

 
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

![image](https://github.com/user-attachments/assets/ffb9e7c5-6c4b-4edf-896a-9d335bf7a74f)

chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![image](https://github.com/user-attachments/assets/4ea27c8a-19ea-4680-ab74-2779c04878c5)

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

![image](https://github.com/user-attachments/assets/400a80c8-c74e-4f2a-a7a7-5bbbf84cbda8)

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

![image](https://github.com/user-attachments/assets/ca19927b-ee75-404a-bf82-7ab784764ab2)

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

![image](https://github.com/user-attachments/assets/b83bd2cb-c835-47e2-94ec-6337c66b7abd)

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

![image](https://github.com/user-attachments/assets/ef76638e-4b01-432d-bead-0f7a884b2188)

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

![image](https://github.com/user-attachments/assets/e70f3b72-cc66-4cbb-a44d-37441ad4f9b1)

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

![image](https://github.com/user-attachments/assets/997c829f-02ce-459f-8f45-187f70ab5bc5)

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

 ![image](https://github.com/user-attachments/assets/0bc1bfee-ee3a-449e-98ef-042f322356ec)
 
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
 
![image](https://github.com/user-attachments/assets/f3cd27c9-1991-4ec1-9877-433c406cf39e)
 
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
 
![image](https://github.com/user-attachments/assets/bf19bdde-2e30-470b-a33e-307d66a97107)

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

![image](https://github.com/user-attachments/assets/600294d5-9cb3-469b-8a12-f17c79fd68ad)

 
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

![image](https://github.com/user-attachments/assets/6f83449c-b902-4e67-95b1-276105beeed5)
 
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

![image](https://github.com/user-attachments/assets/f90f5b8e-ce2e-4537-9ec7-22eb4e785764)

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

![image](https://github.com/user-attachments/assets/e7aabd6c-0f20-42ca-be44-b46ee6e89a0d)

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

![image](https://github.com/user-attachments/assets/1c067b24-52be-4da4-9290-e900094936ba)

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

![image](https://github.com/user-attachments/assets/efee456a-8b42-4847-8c50-7391d273bfd0)
 
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

![image](https://github.com/user-attachments/assets/de88b515-cd60-4339-bb58-3472d192bf5a)

$ chmod 755 forbreak.sh

![image](https://github.com/user-attachments/assets/6be5233c-8643-4068-b288-fc0ab3bd3438)
 
$ ./forbreak.sh 

## here
 
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

![image](https://github.com/user-attachments/assets/c35bdac2-72cf-4dfe-b794-a20a3cb26917)

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

![image](https://github.com/user-attachments/assets/c35bdac2-72cf-4dfe-b794-a20a3cb26917) 

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

![image](https://github.com/user-attachments/assets/8be27805-30d8-41de-b802-8deaafe07e2f)

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
 

![image](https://github.com/user-attachments/assets/74b20eab-144c-4e22-8b0c-e6e46216def8) 

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

![image](https://github.com/user-attachments/assets/5a3fc33b-c6fb-412e-ba7a-85df9f12de4c)

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

![image](https://github.com/user-attachments/assets/08549cad-4ed8-47ad-86eb-47adbc6ca62e) 

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

 ![image](https://github.com/user-attachments/assets/a1620bc2-efef-45c9-9cd4-ca1c97156d37)


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

![image](https://github.com/user-attachments/assets/fda42f04-3629-443d-965e-d79c765b52f8) 

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

![image](https://github.com/user-attachments/assets/e7024bb7-0559-4aef-9b88-bcd32cf5674e)

# RESULT:
The Commands are executed successfully.
