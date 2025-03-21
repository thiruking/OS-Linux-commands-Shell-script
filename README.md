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

![image](https://github.com/user-attachments/assets/d9115792-a641-4d2b-a0c1-0014f3eb5fbf)


cat < file2
## OUTPUT
![image](https://github.com/user-attachments/assets/3ca163d8-30a2-437c-ba12-e13687a29ca0)


# Comparing Files
cmp file1 file2
## OUTPUT
 ![image](https://github.com/user-attachments/assets/c8093300-6f99-45d0-8717-f2dbd70ea4d6)

comm file1 file2
 ## OUTPUT

 ![image](https://github.com/user-attachments/assets/2174be19-cb8c-4153-b60e-79b093c4f3b9)

diff file1 file2
## OUTPUT
![image](https://github.com/user-attachments/assets/f7f367c5-211d-4222-80d2-59a1c6de64f6)


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

![image](https://github.com/user-attachments/assets/ced3dd4e-7d25-4bfa-957a-0afaa3f522b0)



cut -d "|" -f 1 file22
## OUTPUT

![image](https://github.com/user-attachments/assets/2e4f615f-2d32-4c06-9948-115151fd5b0c)


cut -d "|" -f 2 file22
## OUTPUT

![image](https://github.com/user-attachments/assets/41e3adf9-4dd2-408c-8341-41058aff5a11)

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

![image](https://github.com/user-attachments/assets/4cd3a0b0-b70f-4ea1-adba-af5e8f5a4927)


grep hello newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/dff50da1-7ff9-468b-9e23-e4b58ac98cb4)



grep -v hello newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/b9d669ba-4fea-4d1c-9c70-016af75ed3cd)


cat newfile | grep -i "hello"
## OUTPUT


![image](https://github.com/user-attachments/assets/daa7f638-752c-4f83-8f5d-c28b38f92e47)


cat newfile | grep -i -c "hello"
## OUTPUT

![image](https://github.com/user-attachments/assets/7198d8a8-d793-4896-b5c5-f19939cd653b)



grep -R ubuntu /etc
## OUTPUT



grep -w -n world newfile   
## OUTPUT

![image](https://github.com/user-attachments/assets/2aa1c8fe-55b5-40a4-8147-f86e04710445)

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

![image](https://github.com/user-attachments/assets/e5030c89-2798-40b2-8a22-d3193415d9f0)


egrep -w '(H|h)ello' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/7b308aed-06ff-446a-a094-5751212b85a3)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


![image](https://github.com/user-attachments/assets/9313649f-84a2-4511-b4bc-0d37949d202e)


egrep '(^hello)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/72ca4055-6592-46c9-9f4d-6553d0b16000)


egrep '(world$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/5b9e8a4c-a004-4231-8e69-95862ff95e9e)


egrep '(World$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/766957b2-375d-4a18-98a3-02ed743fbac8)

egrep '((W|w)orld$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/92191db4-290d-4ee9-92b5-00ebf0a23931)


egrep '[1-9]' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/c174f391-2c92-4b9f-9e86-dd2d5372778d)


egrep 'Linux.*world' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/cf5a2a53-b56a-4083-ac96-f688e3b6faaf)


egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/4668c11f-1fc7-408a-9f2f-380b70ccb0c7)


egrep l{2} newfile
## OUTPUT

![image](https://github.com/user-attachments/assets/5696e10d-e601-44fc-bdcc-4639a5702962)


egrep 's{1,2}' newfile
## OUTPUT 

![image](https://github.com/user-attachments/assets/f7e93c7c-2c8e-4a59-a157-0ecc2da4efbf)

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

![image](https://github.com/user-attachments/assets/4a1f4304-9b2d-4e67-8746-792e7221ec59)


sed -n -e '$p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/aeec2a0f-4805-48f8-8d9b-ab6e90cdb285)



sed  -e 's/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/7641ec57-9815-479d-84cf-d53e4845006e)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/5e2f0c6b-76bf-4c8e-b290-20dc3605cee5)


sed  '/tom/s/5000/6000/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/c3589c71-344c-4869-818b-123d87a3c343)


sed -n -e '1,5p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/e3a93eca-9310-4b6f-8d0b-6f79bc91fd06)


sed -n -e '2,/Joe/p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/c2e539f9-9d65-43cf-9179-4633528bd493)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/e8823e25-ba3d-48f5-b53b-eba602bd5741)


seq 10 
## OUTPUT
![image](https://github.com/user-attachments/assets/b7c8e4ae-184e-4057-9c63-98db22d26730)



seq 10 | sed -n '4,6p'
## OUTPUT
![image](https://github.com/user-attachments/assets/a47551c4-fc10-4771-9e51-d68a58019a9f)



seq 10 | awk 'NR>=2 && (NR-2)%4==0' in parrot os

## OUTPUT

![image](https://github.com/user-attachments/assets/416bfe40-4e1a-4a74-8be1-a082bf3848de)



seq 3 | sed '2a hello'
## OUTPUT


![image](https://github.com/user-attachments/assets/644b3172-2f95-4c4b-ab73-48654d5dfa42)

seq 2 | sed '2i hello'
## OUTPUT

![image](https://github.com/user-attachments/assets/eefbc054-b5b2-49b0-98f4-44d6f9ed604c)


seq 10 | sed '2,9c hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/ba8a3124-e5d3-4afa-ae8d-e6b971d1ba25)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/7ef14033-ef6f-40b6-9be3-e1d056861554)


sed -n '2,4{s/$/*/;p}' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/8671baa1-c512-4c09-9c96-050c5170846f)


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
![image](https://github.com/user-attachments/assets/2ace0b88-e760-4d10-8720-f909e2cad976)


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

![image](https://github.com/user-attachments/assets/ffda6ffa-e6d0-4d63-bf62-98019ba5a362)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![image](https://github.com/user-attachments/assets/b18c4601-71e3-4259-9ced-147e7d4bf96b)

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

![image](https://github.com/user-attachments/assets/e0f9a24c-0a96-48c1-bc68-5ccc54c909f4)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![image](https://github.com/user-attachments/assets/f1129f14-4464-4254-9eee-9a9a2ea7626d)



#Backup commands
tar -cvf backup.tar *
## OUTPUT

![image](https://github.com/user-attachments/assets/88158872-0a69-4169-9834-f1be2ca46db2)

mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backupdir/backup.tar

## OUTPUT

![image](https://github.com/user-attachments/assets/e6125baf-069d-4aad-89c7-339055a613c2)

tar -xvf backupdir/backup.tar
## OUTPUT
![image](https://github.com/user-attachments/assets/fb360d39-c4a3-4c3e-8659-c3b73264fe2f)

gzip backupdir/backup.tar

ls backupdir/
## OUTPUT
 ![image](https://github.com/user-attachments/assets/14b1159e-8ee9-457c-b3ab-0a55a054c644)
 ![image](https://github.com/user-attachments/assets/396b50eb-90a1-4199-b1c2-9aea5b286f6f)


gunzip backupdir/backup.tar.gz
## OUTPUT
![image](https://github.com/user-attachments/assets/df2fa7fa-1d15-4d6d-9335-810dc9e10bde)



 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
 ![image](https://github.com/user-attachments/assets/fd1d24df-f1fd-4e76-867d-f643beb6fec8)

 ![image](https://github.com/user-attachments/assets/fc6babda-7d90-4ca5-a4da-67be6aed214b)

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![image](https://github.com/user-attachments/assets/8a9cf1ae-b21e-4c3c-b494-3187c2ca01d2)


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
![image](https://github.com/user-attachments/assets/e3632616-6c65-4a4d-94ea-6498b6c561bb)

![image](https://github.com/user-attachments/assets/1a650a1f-666c-4054-90d8-729536185a64)

 
ls file1
## OUTPUT
![image](https://github.com/user-attachments/assets/c4ffd8cc-4f2c-48e0-a64e-f22f739fe05b)


echo $?
## OUTPUT 

![image](https://github.com/user-attachments/assets/93e17c13-49c6-483e-966b-d99fc4b4b32f)
 
echo $?
## OUTPUT 
./file1
bash: ./file1: Permission denied
![image](https://github.com/user-attachments/assets/22ccaa13-591b-459e-8c1b-437217c19c0d)

 
abcd
 
echo $?
 ## OUTPUT

![image](https://github.com/user-attachments/assets/7f793372-65b8-449b-b65e-44a262e36815)

 
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
![image](https://github.com/user-attachments/assets/30c6cc64-7ff1-4644-bffa-81f1efe5e5f0)


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

![image](https://github.com/user-attachments/assets/60aa5cf4-00e4-4cee-bcfa-84185fa5a72a)

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

![image](https://github.com/user-attachments/assets/2336c782-1466-4ef8-bc3a-56de0b8ad386)


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
![image](https://github.com/user-attachments/assets/19d044b1-52d6-463f-b57b-0dfcd438614b)


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
![image](https://github.com/user-attachments/assets/2e8e3586-2b24-43ee-ac15-1985046445c5)

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

![image](https://github.com/user-attachments/assets/4c49abeb-e3de-48df-a83d-79a91e0d138e)


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
![image](https://github.com/user-attachments/assets/937a8eef-ca85-4fe3-8bb2-3ccd40fe8e38)

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
## OUTPUT
 ![image](https://github.com/user-attachments/assets/588cc96b-1ba0-48f0-8c56-a6a9a254465e)

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
## OUTPUT
 
 ![image](https://github.com/user-attachments/assets/6c31faaa-0dd9-4feb-870d-8bdd3f0fcc99)

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
 $ ./untiltest.sh
 ## OUTPUT
 
 ![image](https://github.com/user-attachments/assets/37efbfe1-4ecb-4796-a9b6-7bb0a8987b7f)

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
$ ./forin1.sh
 ![image](https://github.com/user-attachments/assets/f4b8d109-0606-4caf-93fe-cb691f627c1c)

 
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

![image](https://github.com/user-attachments/assets/5dc78afc-b96b-42e5-a8bb-aaaeb66b5179)


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
## OUTPUT
![image](https://github.com/user-attachments/assets/6bbc0de6-7371-4774-a47c-4ca219bc1990)

cat forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ chmod 755 forin2.sh
$ ./forin3.sh 
## OUTPUT
 ![image](https://github.com/user-attachments/assets/114e8547-69a4-4e4a-abc6-e9961beb4416)

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
![image](https://github.com/user-attachments/assets/f4b8d109-0606-4caf-93fe-cb691f627c1c)

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
![image](https://github.com/user-attachments/assets/056f316d-29d9-46fb-ba9b-3d0e15f71355)


cat forctype.sh 
```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
````
:$ chmod 755 forctype.sh
$ ./forctype.sh 
## OUTPUT
![image](https://github.com/user-attachments/assets/52c8e684-9dfd-4c38-88bd-357ac8ffd998)

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
![image](https://github.com/user-attachments/assets/9f1b37d5-ec69-472f-ba32-e805c325d5a4)

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
![image](https://github.com/user-attachments/assets/b9dbfeed-e1e9-40e0-b391-e4411e996f50)

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
 ![image](https://github.com/user-attachments/assets/fe70874e-9230-4485-abeb-38eae785dec3)

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
![image](https://github.com/user-attachments/assets/7afc07aa-d955-4c36-b361-2e12fa8969a0)


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 
$ ./exread1.sh 
## OUTPUT

![image](https://github.com/user-attachments/assets/6376cf19-0644-487f-b8b4-d7bdadb27570)



 
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

 ![image](https://github.com/user-attachments/assets/d8407858-9815-481a-bf35-eebb14031835)

cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh
$ ./argshift.sh 1 2 3
## OUTPUT

 ![image](https://github.com/user-attachments/assets/9f6f2c7b-b068-4c79-9571-ed0cedbbfa05)

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
 ![image](https://github.com/user-attachments/assets/0da7ce04-102a-4c8a-94b6-2543b0133b48)

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
 
 ![image](https://github.com/user-attachments/assets/ae4f4e98-a21f-43d2-9d1a-4dc4ea35155a)

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
 ![image](https://github.com/user-attachments/assets/b065bbe4-bb4e-44e1-a944-d7f24e092ac0)

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

![image](https://github.com/user-attachments/assets/49f7ceb4-fe89-492e-9df9-3398f469ae7a)

# RESULT:
The Commands are executed successfully.
