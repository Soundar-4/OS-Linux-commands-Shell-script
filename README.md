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
<img width="1018" height="317" alt="{01BFB38A-4654-4621-9C18-3C9A3DADAA1C}" src="https://github.com/user-attachments/assets/85d79524-1197-4c7c-9533-407b73caa79a" />



cat < file2
## OUTPUT
<img width="995" height="374" alt="{D963EF8C-E604-4728-A641-F4251716B893}" src="https://github.com/user-attachments/assets/93c6c4b8-0c91-4ded-b64f-233ecc3c0efc" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="1019" height="119" alt="image" src="https://github.com/user-attachments/assets/46f92a6c-d2f9-463d-8bfa-591ba3f541ec" />

comm file1 file2
 ## OUTPUT
<img width="1046" height="518" alt="{9473B503-7A03-44FC-BA2D-6842D63662F7}" src="https://github.com/user-attachments/assets/701f8218-cfbe-48c1-bf90-bc05fcefe015" />

 
diff file1 file2
## OUTPUT
<img width="762" height="480" alt="image" src="https://github.com/user-attachments/assets/3da62a78-2d71-49a5-ac86-44ab60a45e66" />


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
<img width="772" height="134" alt="image" src="https://github.com/user-attachments/assets/ce9e1b94-636c-49f1-a1f9-943893a9747c" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="949" height="189" alt="image" src="https://github.com/user-attachments/assets/1edd9fa6-ae2c-42f5-b46b-958f38b05f40" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="905" height="178" alt="image" src="https://github.com/user-attachments/assets/ff2c74a8-c8eb-46d5-bae9-1e8e2a3afcf5" />


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
<img width="837" height="88" alt="image" src="https://github.com/user-attachments/assets/d32cde2a-82d4-4aa0-8bcc-b93bc7a30577" />



grep hello newfile 
## OUTPUT
<img width="836" height="86" alt="image" src="https://github.com/user-attachments/assets/6bc8bafb-a220-4a12-8edf-f3ef7a66f126" />




grep -v hello newfile 
## OUTPUT
<img width="895" height="130" alt="image" src="https://github.com/user-attachments/assets/460d5e17-0a47-43fe-a6fe-c38bb0ef83a7" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="1084" height="140" alt="image" src="https://github.com/user-attachments/assets/200ab9ea-a2f3-4e44-97ef-33f3a44cd3f7" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="1122" height="81" alt="image" src="https://github.com/user-attachments/assets/38939ec1-a13d-485f-8a95-3d6aec5188f9" />




grep -R ubuntu /etc
## OUTPUT
<img width="967" height="152" alt="image" src="https://github.com/user-attachments/assets/57cdc477-d375-4106-891a-d99f40d7888c" />



grep -w -n world newfile   
## OUTPUT
<img width="1460" height="200" alt="image" src="https://github.com/user-attachments/assets/ccb1108e-8668-4a16-838f-e422e2de6ddd" />


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
<img width="991" height="129" alt="{525371AB-3871-4B3C-A780-7CD61B4087D4}" src="https://github.com/user-attachments/assets/dbdf4df4-da87-46b8-a87b-0ff0d8ba7113" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="1051" height="116" alt="{3D7292FA-E9AA-4630-9613-11FA995F1A58}" src="https://github.com/user-attachments/assets/7eec471d-92c4-412d-b0a5-7ebcc56bb7d8" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="1052" height="119" alt="image" src="https://github.com/user-attachments/assets/6739e8fe-4cc6-4ddc-a43f-ad7c18c1eab1" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="892" height="89" alt="image" src="https://github.com/user-attachments/assets/5e70b96a-7701-40bc-b352-2898ae320cfe" />



egrep '(world$)' newfile 
## OUTPUT
<img width="888" height="130" alt="image" src="https://github.com/user-attachments/assets/f3c03ceb-6e13-41e7-876d-c06c3c3846e9" />



egrep '(World$)' newfile 
## OUTPUT
<img width="875" height="117" alt="image" src="https://github.com/user-attachments/assets/c688e1b1-7ec3-41f3-8b49-abf68eed5b9e" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="938" height="171" alt="image" src="https://github.com/user-attachments/assets/247b9488-333a-4be4-9fae-0e3e8b7b4cf2" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="875" height="80" alt="image" src="https://github.com/user-attachments/assets/bd39d3d0-26db-43fd-8165-7f648b52151f" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="958" height="76" alt="image" src="https://github.com/user-attachments/assets/88da198a-7109-4476-bc04-64ce535cc3da" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="956" height="86" alt="image" src="https://github.com/user-attachments/assets/c7f0c1cd-2717-4c94-8a44-51c764172dd3" />


egrep l{2} newfile
## OUTPUT
<img width="746" height="123" alt="image" src="https://github.com/user-attachments/assets/dab6c88e-debb-4dd5-9514-524c7b4238ac" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="856" height="156" alt="image" src="https://github.com/user-attachments/assets/5a8675cf-a5c5-439b-94a2-f03db1b033f3" />


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
<img width="801" height="86" alt="image" src="https://github.com/user-attachments/assets/589d2a30-ef2e-4fb3-a87a-7c0352ed494e" />



sed -n -e '$p' file23
## OUTPUT
<img width="743" height="89" alt="{C28EF453-3B05-4545-96BF-CB477645ECE8}" src="https://github.com/user-attachments/assets/4777c61e-b145-4ddb-a20a-90016ec9b785" />




sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="953" height="375" alt="{30293D90-DA6F-4196-922D-991D065FDC89}" src="https://github.com/user-attachments/assets/cd94d185-11aa-4b4e-9896-09c8d96291b8" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="1014" height="384" alt="image" src="https://github.com/user-attachments/assets/5c8013b5-9b29-4c50-97a0-69eec0528764" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="1000" height="378" alt="image" src="https://github.com/user-attachments/assets/ee85d1d6-38a5-406b-8ff6-286de8c0ad72" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="851" height="238" alt="image" src="https://github.com/user-attachments/assets/983973f3-cca6-4b86-b298-b4d07fbe7aaf" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="921" height="162" alt="image" src="https://github.com/user-attachments/assets/c327acb9-a845-4f22-a959-4aec8b97d8bb" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="1032" height="120" alt="image" src="https://github.com/user-attachments/assets/d291506b-bdc0-4708-8783-c1740e31da74" />



seq 10 
## OUTPUT
<img width="555" height="443" alt="image" src="https://github.com/user-attachments/assets/3bc87603-ea4b-4432-8aeb-461d6a108521" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="819" height="157" alt="image" src="https://github.com/user-attachments/assets/35cdccb6-85b4-4732-aa32-eb0bad5f3ea3" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="1074" height="157" alt="image" src="https://github.com/user-attachments/assets/08d9cf9f-8f05-4c75-9f72-6121b22105b3" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="829" height="205" alt="image" src="https://github.com/user-attachments/assets/1d7512e2-e8d8-4013-8955-1a96916f4298" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="821" height="163" alt="image" src="https://github.com/user-attachments/assets/5d271dfc-0131-4f88-a176-eb9881ac4f0e" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="885" height="155" alt="image" src="https://github.com/user-attachments/assets/db82348d-7bc8-4bfb-95a1-940629acfa50" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="958" height="166" alt="image" src="https://github.com/user-attachments/assets/0da51913-641f-483e-8757-3844a68b9a2d" />



sed -n '2,4{s/$/*/;p}' file23
<img width="964" height="156" alt="image" src="https://github.com/user-attachments/assets/2830ba8b-1816-419b-a0d0-974ad4664fd4" />


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
<img width="620" height="238" alt="image" src="https://github.com/user-attachments/assets/d9d76e01-042f-4fa6-9a4a-d46811af8156" />


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
<img width="616" height="243" alt="image" src="https://github.com/user-attachments/assets/84e2d0b0-4eaa-46b1-a3f8-326db1747d2f" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="1088" height="360" alt="image" src="https://github.com/user-attachments/assets/87b2092f-ef03-40d6-ba65-be654d5c9e0f" />

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
<img width="932" height="160" alt="image" src="https://github.com/user-attachments/assets/c39b2a69-3348-4d15-a70b-9671ca6c4980" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="1183" height="159" alt="image" src="https://github.com/user-attachments/assets/df98f7fe-5f53-4064-adee-413ec249c22c" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="817" height="360" alt="image" src="https://github.com/user-attachments/assets/c709aa54-39b9-43f4-bfc8-59362fcd7ba0" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="1217" height="373" alt="image" src="https://github.com/user-attachments/assets/761b1c8d-506d-479c-b122-f6481318ce4c" />


tar -xvf backup.tar
## OUTPUT
<img width="1031" height="362" alt="image" src="https://github.com/user-attachments/assets/5ddcda1f-c6da-40c9-80ad-f31fb50b0400" />

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
<img width="675" height="139" alt="{476B7848-5921-4CC2-99E8-95B2128F7B7B}" src="https://github.com/user-attachments/assets/bd645402-2922-4557-9071-d892d186bb91" />


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
<img width="567" height="463" alt="{1863F665-C1F8-45C6-9289-67E4180BB612}" src="https://github.com/user-attachments/assets/2373bb38-cf3c-44c7-8ae5-976013ef4bde" />

echo $?
## OUTPUT 
<img width="325" height="45" alt="{8F6ABAC6-8C3B-454B-8367-D152490A8127}" src="https://github.com/user-attachments/assets/0ab6a3d3-fb4d-4779-8163-da39d83b13c2" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="320" height="46" alt="{3BE38D21-E6C7-4736-B58C-AA3AC6020779}" src="https://github.com/user-attachments/assets/1a4221a4-f562-490c-aa0c-efe0c4ed8770" />

abcd
 
echo $?
 ## OUTPUT
 <img width="326" height="51" alt="{EE8C8FD4-1903-4F16-99FC-2C6BA85CB5A9}" src="https://github.com/user-attachments/assets/2d119dc6-6cd5-439a-b9c3-cc6e992a7051" />


 
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
<img width="408" height="238" alt="{068CF702-A5EF-47B3-96C9-629B4EE96333}" src="https://github.com/user-attachments/assets/e7814f01-5064-49ca-abb4-db3966caab73" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="507" height="73" alt="{34162B8C-80DD-41DD-9AB5-E97DF774B4D6}" src="https://github.com/user-attachments/assets/2bcba34f-de1c-4b07-b9d9-fc7a69cc6dab" />


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
<img width="440" height="53" alt="{197F2B62-650F-4847-B94C-4F068D952C44}" src="https://github.com/user-attachments/assets/ffa06486-d988-472d-9712-bc7dcad6b3df" />

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
<img width="415" height="49" alt="{F7CC528B-636D-4843-97AA-5AF7A4CA35A7}" src="https://github.com/user-attachments/assets/4d20b09c-3f49-478e-ade7-982b5457e7a1" />



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
<img width="492" height="94" alt="{EB48D388-9329-40AF-ADAC-6A725C889B21}" src="https://github.com/user-attachments/assets/d55ae846-59f6-47cc-a540-e45f1ec42a15" />

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
