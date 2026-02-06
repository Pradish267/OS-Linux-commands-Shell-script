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
<img width="339" height="152" alt="image" src="https://github.com/user-attachments/assets/bcfd5053-b217-4eaa-b5eb-1260945bf687" />





cat < file2
## OUTPUT
<img width="317" height="173" alt="image" src="https://github.com/user-attachments/assets/9d436d5a-3a0c-47cc-97d5-c33deba7c06a" />



# Comparing Files
cmp file1 file2
## OUTPUT
<img width="372" height="73" alt="image" src="https://github.com/user-attachments/assets/f6f8efff-70ec-4d67-a546-da22e9da9650" />

 
comm file1 file2
 ## OUTPUT
 <img width="348" height="225" alt="image" src="https://github.com/user-attachments/assets/0702f2c8-fbc5-4412-83c0-0bd7eefeb363" />


 
diff file1 file2
## OUTPUT
<img width="331" height="276" alt="image" src="https://github.com/user-attachments/assets/c1d60252-e5b0-46fc-97f1-d2ea3e07682d" />



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




cut -d "|" -f 1 file22
## OUTPUT
<img width="317" height="123" alt="image" src="https://github.com/user-attachments/assets/12f233c5-206d-48f1-87dd-1bd362c32f27" />




cut -d "|" -f 2 file22
## OUTPUT
<img width="318" height="121" alt="image" src="https://github.com/user-attachments/assets/9c615851-3f8f-4f36-9b8d-6d7fd99a590e" />


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
<img width="318" height="75" alt="image" src="https://github.com/user-attachments/assets/f254ff51-1da7-4a6c-9fbd-98788b515622" />




grep hello newfile 
## OUTPUT
<img width="323" height="73" alt="image" src="https://github.com/user-attachments/assets/bc07f7c6-1ca1-45a5-8330-d83ff5c0b93a" />





grep -v hello newfile 
## OUTPUT
<img width="325" height="72" alt="image" src="https://github.com/user-attachments/assets/9ff19853-6785-49b3-b967-56142fd7ed45" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="360" height="96" alt="image" src="https://github.com/user-attachments/assets/ed5be728-e6fd-416b-9fcc-b0437126dc7d" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="393" height="75" alt="image" src="https://github.com/user-attachments/assets/1423ebf6-aeaf-45a7-a81e-652160135fd9" />





grep -R ubuntu /etc
## OUTPUT
<img width="944" height="123" alt="image" src="https://github.com/user-attachments/assets/4fffd0ff-c3cb-4942-bb98-ded8252fc673" />



grep -w -n world newfile   
## OUTPUT
<img width="320" height="98" alt="image" src="https://github.com/user-attachments/assets/ad9e2d96-568f-4909-8ab8-e929506930d8" />



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
<img width="372" height="99" alt="image" src="https://github.com/user-attachments/assets/5a8a7ea0-2c46-41e1-a109-694aff2e5004" />




egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="353" height="101" alt="image" src="https://github.com/user-attachments/assets/a07e317b-f5a5-4667-8436-49ff0a1634fc" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="394" height="98" alt="image" src="https://github.com/user-attachments/assets/c11ebdb4-b057-41ee-8dd2-bcf376f340bb" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="318" height="75" alt="image" src="https://github.com/user-attachments/assets/38316e33-62d5-4e26-bfa1-1673efb32767" />




egrep '(world$)' newfile 
## OUTPUT
<img width="315" height="98" alt="image" src="https://github.com/user-attachments/assets/707ca8a1-5a6e-4ae2-be4b-657fb0c39937" />



egrep '(World$)' newfile 
## OUTPUT
<img width="330" height="70" alt="image" src="https://github.com/user-attachments/assets/793c6fd4-33e0-463c-96d6-91ea20dee4ae" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="368" height="121" alt="image" src="https://github.com/user-attachments/assets/71bfc905-94ca-4136-bf12-136533aba163" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="318" height="75" alt="image" src="https://github.com/user-attachments/assets/f8561407-f03c-4092-b611-d89ba56dce4b" />




egrep 'Linux.*world' newfile 
## OUTPUT
<img width="354" height="74" alt="image" src="https://github.com/user-attachments/assets/a1189638-787b-4175-b07b-e2896c893fcc" />



egrep 'Linux.*World' newfile 
## OUTPUT
<img width="348" height="71" alt="image" src="https://github.com/user-attachments/assets/3b1a982c-6467-49c7-a590-87c0672b0504" />



egrep l{2} newfile
## OUTPUT
<img width="321" height="98" alt="image" src="https://github.com/user-attachments/assets/26ccc0f5-9680-41bf-bb75-1d6c019e798b" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="326" height="123" alt="image" src="https://github.com/user-attachments/assets/ea41dc85-25bc-4637-a3ec-fddd2ff59082" />



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
<img width="319" height="76" alt="image" src="https://github.com/user-attachments/assets/714f3511-12c1-4ce1-99a0-1105a42b4795" />




sed -n -e '$p' file23
## OUTPUT
<img width="314" height="75" alt="image" src="https://github.com/user-attachments/assets/6e454f11-8d2b-4e89-96c4-2a44aa90ae0e" />




sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="354" height="252" alt="image" src="https://github.com/user-attachments/assets/e76e4046-2e97-4445-b736-92712881693e" />




sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="369" height="250" alt="image" src="https://github.com/user-attachments/assets/e18cf75e-d534-44e0-b829-d14c0d3bd6b6" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="395" height="248" alt="image" src="https://github.com/user-attachments/assets/7c7e6b94-5ade-4593-9e4a-5ed115c6b359" />




sed -n -e '1,5p' file23
## OUTPUT
<img width="395" height="248" alt="image" src="https://github.com/user-attachments/assets/42e29f62-f58d-45be-9f10-a79a3a1ac24d" />




sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="329" height="176" alt="image" src="https://github.com/user-attachments/assets/7ec69373-5ec0-4445-85c9-4f9eb557ca3a" />





sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="350" height="123" alt="image" src="https://github.com/user-attachments/assets/ecaf4d90-683e-4d87-8457-c7b2f747b085" />




seq 10 
## OUTPUT
<img width="384" height="100" alt="image" src="https://github.com/user-attachments/assets/479979f1-6e66-437b-9491-4c83fa345105" />




seq 10 | sed -n '4,6p'
## OUTPUT
<img width="318" height="123" alt="image" src="https://github.com/user-attachments/assets/403ac314-05dd-4f13-a129-057acfef2a97" />




seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="318" height="120" alt="image" src="https://github.com/user-attachments/assets/940fb12e-003e-43e9-9005-e493ecea46bc" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="318" height="149" alt="image" src="https://github.com/user-attachments/assets/12477b32-e24a-45e8-84f7-d73abf87e1bf" />




seq 2 | sed '2i hello'
## OUTPUT
<img width="311" height="123" alt="image" src="https://github.com/user-attachments/assets/00cce2f2-6777-4109-a39b-821bee38c5b2" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="326" height="119" alt="image" src="https://github.com/user-attachments/assets/1ca14112-472c-4d67-8db8-e27f7c432bac" />



sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="326" height="119" alt="image" src="https://github.com/user-attachments/assets/b47d3ba8-b38b-46fa-abd9-44cfaa268c55" />



sed -n '2,4{s/$/*/;p}' file23
<img width="363" height="126" alt="image" src="https://github.com/user-attachments/assets/ec765360-ccad-4070-a2aa-e2fa27dd3083" />



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
<img width="335" height="175" alt="image" src="https://github.com/user-attachments/assets/38aca296-ea90-4aa5-9f8f-fed530b1f167" />


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
<img width="336" height="173" alt="image" src="https://github.com/user-attachments/assets/5495efce-c167-47fb-ab75-b2715826ad5e" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
 <img width="424" height="249" alt="image" src="https://github.com/user-attachments/assets/1999e0db-dda7-48c9-88d9-ce2abb9ee0d8" />


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
 <img width="343" height="123" alt="image" src="https://github.com/user-attachments/assets/4b2aa451-15e9-425f-af26-542b14874341" />



 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="474" height="125" alt="image" src="https://github.com/user-attachments/assets/e9c4c904-dda1-4148-a9ef-1742064f8543" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="333" height="249" alt="image" src="https://github.com/user-attachments/assets/b3645495-5ba6-4c9e-8832-4e33c0582a44" />



mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="619" height="250" alt="image" src="https://github.com/user-attachments/assets/538059db-c76f-479e-ad24-12cb6cb80c08" />



tar -xvf backup.tar
## OUTPUT
<img width="619" height="250" alt="image" src="https://github.com/user-attachments/assets/c4a541f2-271d-4dc7-a74b-d11fbdbe9c9e" />

gzip backup.tar

ls .gz
## OUTPUT
<img width="424" height="249" alt="image" src="https://github.com/user-attachments/assets/4705a624-dbff-4338-bab8-3a51b391d64c" />

 
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
<img width="435" height="98" alt="image" src="https://github.com/user-attachments/assets/fdee2e95-7ebb-49b2-8477-131ba25dbe29" />


 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="449" height="127" alt="image" src="https://github.com/user-attachments/assets/24d9034d-764d-4ced-ba43-7581ae85a1e2" />



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
<img width="619" height="447" alt="image" src="https://github.com/user-attachments/assets/cf61446a-226b-49e8-80f6-88fd53b3ffd6" />

 
ls file1
## OUTPUT
<img width="423" height="72" alt="image" src="https://github.com/user-attachments/assets/9f7b651b-12e2-48a3-80a1-4de03088adf8" />


echo $?
## OUTPUT
<img width="423" height="74" alt="image" src="https://github.com/user-attachments/assets/bd342f87-ac96-4105-b6fb-4040222f7a0d" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 

 
abcd
 
echo $?
 ## OUTPUT
 <img width="468" height="148" alt="image" src="https://github.com/user-attachments/assets/8911be5a-a81e-4f07-84c9-a0df8b278475" />



 
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
<img width="427" height="272" alt="image" src="https://github.com/user-attachments/assets/dc06e0db-3998-4934-b094-e0296ccde56e" />




chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="609" height="100" alt="image" src="https://github.com/user-attachments/assets/ab4b03fc-cb0f-483a-86e2-d9964d07e625" />



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
<img width="457" height="76" alt="image" src="https://github.com/user-attachments/assets/a6375747-95cd-462e-adb6-1c5d03658997" />


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
<img width="423" height="75" alt="image" src="https://github.com/user-attachments/assets/d4ede7fb-c7cd-455a-aee3-e2e0af81c991" />




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
<img width="609" height="125" alt="image" src="https://github.com/user-attachments/assets/32bbe213-61f7-452f-86e2-f17930b29264" />


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
<img width="633" height="150" alt="image" src="https://github.com/user-attachments/assets/95d4607c-e854-4c7a-afa5-3250aeb5239f" />

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
<img width="629" height="105" alt="image" src="https://github.com/user-attachments/assets/4113ecac-4bc8-4a52-a603-66dd5b6324c2" />



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
<img width="644" height="103" alt="image" src="https://github.com/user-attachments/assets/24e76758-dfe8-4712-afb3-b2ab5e74a1a3" />


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

##OUTPUT
<img width="423" height="77" alt="image" src="https://github.com/user-attachments/assets/195c2c7c-3f39-4af9-ba68-5692eaf86d30" />

 
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

<img width="441" height="304" alt="image" src="https://github.com/user-attachments/assets/1e11bc50-4f27-4e29-8ffc-da659e168c00" />

 
 
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
 <img width="504" height="175" alt="image" src="https://github.com/user-attachments/assets/48fdf6a7-4755-4ac7-a917-9b76b1b83435" />

 
 
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
<img width="603" height="249" alt="image" src="https://github.com/user-attachments/assets/45d0c5ad-646f-4305-be02-8b11c0e5b732" />

 
 
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
 <img width="605" height="177" alt="image" src="https://github.com/user-attachments/assets/05bbc1db-3a97-4629-bcc8-5abb9f1fa68f" />

cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
```
$ chmod 755 forin2.sh $ ./forin2.sh 
<img width="605" height="177" alt="image" src="https://github.com/user-attachments/assets/716a63e8-b1ee-4fb6-8b62-8fcd92335607" />

 
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
<img width="618" height="252" alt="image" src="https://github.com/user-attachments/assets/bbc957be-dc52-4973-bc94-b8afe3fdce8d" />

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
<img width="618" height="252" alt="image" src="https://github.com/user-attachments/assets/a51a8293-eef0-431b-8220-a34458da4283" />

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
<img width="417" height="223" alt="image" src="https://github.com/user-attachments/assets/aab8853c-3a02-4bf7-9c99-a177e1e511e9" />




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
<img width="422" height="175" alt="image" src="https://github.com/user-attachments/assets/f3b9c824-ff2a-456d-9000-e51288942d18" />


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
<img width="428" height="76" alt="image" src="https://github.com/user-attachments/assets/d4058f46-d796-4f39-8d78-a65445bff63b" />


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
 <img width="414" height="353" alt="image" src="https://github.com/user-attachments/assets/7c1fe717-5635-4ccc-a36b-13bdf4d07d2a" />


 
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
<img width="414" height="353" alt="image" src="https://github.com/user-attachments/assets/5a734846-f716-4bb8-9659-a7a8d2b150b8" />


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
<img width="435" height="147" alt="image" src="https://github.com/user-attachments/assets/217c9ea4-849c-434b-9e96-22e5a8b84d6b" />

 
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
<img width="442" height="100" alt="image" src="https://github.com/user-attachments/assets/c601fd5b-aa9e-4790-91bf-2ebb1d6f3708" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
<img width="451" height="101" alt="image" src="https://github.com/user-attachments/assets/c7118bad-1e9b-4d8d-9582-206d9539692a" />




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
 ./funcex.sh ./funcex.sh 1 2
<img width="423" height="74" alt="image" src="https://github.com/user-attachments/assets/1020af20-da11-4c92-87b8-33a2898f6ba0" />

 
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
<img width="420" height="124" alt="image" src="https://github.com/user-attachments/assets/96d678cd-4c25-4f9b-a334-c874e148fd01" />

 
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
<img width="419" height="124" alt="image" src="https://github.com/user-attachments/assets/ee20e8f7-6409-4055-86ce-ffe64997ab41" />

 
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
 <img width="418" height="401" alt="image" src="https://github.com/user-attachments/assets/42e1f824-8f02-40f0-8cf4-100e828dc9b1" />


 
 
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
<img width="433" height="126" alt="image" src="https://github.com/user-attachments/assets/1dc85d22-8b6f-40fb-8f2c-0ece4083e4ab" />


# RESULT:
The Commands are executed successfully.
