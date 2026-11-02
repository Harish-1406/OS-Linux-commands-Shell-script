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
<img width="461" height="122" alt="image" src="https://github.com/user-attachments/assets/7b0814d1-adcf-4009-8e3a-b51541ae5d3f" />



cat < file2
## OUTPUT

<img width="447" height="138" alt="image" src="https://github.com/user-attachments/assets/c7457836-a65f-40b1-b198-2df2bfb55486" />


# Comparing Files
cmp file1 file2
## OUTPUT

 <img width="525" height="50" alt="image" src="https://github.com/user-attachments/assets/16b1e565-9aa7-47e8-8a37-a540c0e22412" />

comm file1 file2
 ## OUTPUT

<img width="753" height="277" alt="image" src="https://github.com/user-attachments/assets/952d700a-5a57-4e77-9d91-ef1b786174ff" />

 
diff file1 file2
## OUTPUT

<img width="603" height="252" alt="image" src="https://github.com/user-attachments/assets/c743f3cf-a9a6-4a8e-8b5c-19dd7d2fea1a" />


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

<img width="562" height="87" alt="image" src="https://github.com/user-attachments/assets/c46dc4d2-3458-4693-8b63-b0db85c12711" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="596" height="115" alt="image" src="https://github.com/user-attachments/assets/625dbab7-8b80-43f9-aa74-68ae1f216737" />


cut -d "|" -f 2 file22
## OUTPUT

<img width="612" height="116" alt="image" src="https://github.com/user-attachments/assets/958c9198-f857-445b-91eb-31214dc0a74c" />


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

<img width="547" height="45" alt="image" src="https://github.com/user-attachments/assets/18fe2ff3-87c3-4e12-9e81-133d65718422" />


grep hello newfile 
## OUTPUT


<img width="540" height="48" alt="image" src="https://github.com/user-attachments/assets/69480a5a-9efa-406d-a917-c6a3f4192ce3" />


grep -v hello newfile 
## OUTPUT

<img width="573" height="67" alt="image" src="https://github.com/user-attachments/assets/5da13e21-73af-425d-8dac-63352ba5c644" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="673" height="70" alt="image" src="https://github.com/user-attachments/assets/a730e044-120b-4ec9-af84-033e427e818e" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="717" height="47" alt="image" src="https://github.com/user-attachments/assets/f922262a-3599-40b8-ad9e-b4a67599f745" />



grep -R ubuntu /etc
## OUTPUT

<img width="1895" height="1057" alt="image" src="https://github.com/user-attachments/assets/983557db-26a0-4df7-b6fe-0070f7537caa" />


grep -w -n world newfile   
## OUTPUT

<img width="620" height="67" alt="image" src="https://github.com/user-attachments/assets/9f0fe0dd-23c0-4b80-9703-cde9db2f8d28" />


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

<img width="707" height="72" alt="image" src="https://github.com/user-attachments/assets/04e438cd-4171-4f17-be8d-6399e37b5f51" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="680" height="67" alt="image" src="https://github.com/user-attachments/assets/55cd6453-fa1c-4f27-8cb4-3429b40d2af9" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="717" height="66" alt="image" src="https://github.com/user-attachments/assets/88db26c1-0062-469d-9a93-58b4068b674c" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="608" height="48" alt="image" src="https://github.com/user-attachments/assets/a10ef478-7827-4e47-b340-863a330d6294" />


egrep '(world$)' newfile 
## OUTPUT

<img width="653" height="70" alt="image" src="https://github.com/user-attachments/assets/cdbb0af1-d8ba-4d01-8aa6-91bfca0cacca" />


egrep '(World$)' newfile 
## OUTPUT

<img width="706" height="45" alt="image" src="https://github.com/user-attachments/assets/7e05ce87-df96-4695-a011-6c1fe76c5a6b" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="672" height="95" alt="image" src="https://github.com/user-attachments/assets/dea5f899-9fd4-4e88-99b5-e8c13f8230d2" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="636" height="48" alt="image" src="https://github.com/user-attachments/assets/49220a81-ddc4-48d0-abe7-d57755d8389f" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="658" height="45" alt="image" src="https://github.com/user-attachments/assets/0af47072-ed5e-4be7-87e3-bbd9def636df" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="672" height="47" alt="image" src="https://github.com/user-attachments/assets/c193c485-0479-4605-ba1b-65ce967c5dc3" />


egrep l{2} newfile
## OUTPUT

<img width="537" height="67" alt="image" src="https://github.com/user-attachments/assets/db1eec6d-0f08-43b1-9248-2ae1f48b9809" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="581" height="87" alt="image" src="https://github.com/user-attachments/assets/f30b2515-6331-42ac-b0ef-8390bd213949" />


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

<img width="595" height="47" alt="image" src="https://github.com/user-attachments/assets/a72c6b19-3eac-40a9-a36c-f6a8ac85ebcd" />


sed -n -e '$p' file23
## OUTPUT

<img width="595" height="50" alt="image" src="https://github.com/user-attachments/assets/f4a4d860-b428-44a4-be96-5efd4d143cf5" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="715" height="232" alt="image" src="https://github.com/user-attachments/assets/54cb0753-d847-4325-ae8b-a027a8727d25" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="677" height="230" alt="image" src="https://github.com/user-attachments/assets/2cb4ba41-fd97-45c8-a7f3-92e144bab96e" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="700" height="236" alt="image" src="https://github.com/user-attachments/assets/20bfd88d-b99f-4bf1-b774-ad6c039c703f" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="625" height="137" alt="image" src="https://github.com/user-attachments/assets/aff80dd2-c8a7-488d-92f3-f20e2ce54c39" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="651" height="92" alt="image" src="https://github.com/user-attachments/assets/669f384a-ec86-4ec6-8cee-7f2abb212c8b" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="692" height="67" alt="image" src="https://github.com/user-attachments/assets/e71f2d78-e6ef-4a8e-9ef0-5055904bc2d6" />


seq 10 
## OUTPUT

<img width="427" height="255" alt="image" src="https://github.com/user-attachments/assets/2afca18d-9be5-49d7-bc00-f6b236847fbd" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="581" height="92" alt="image" src="https://github.com/user-attachments/assets/be4fd420-2e13-4047-8810-582736b41317" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="591" height="90" alt="image" src="https://github.com/user-attachments/assets/15e4fd46-e4f1-4cf2-8437-663f8bc33037" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="588" height="115" alt="image" src="https://github.com/user-attachments/assets/061aed3a-4a20-4cbc-9a12-99c652496e85" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="592" height="93" alt="image" src="https://github.com/user-attachments/assets/33b1423d-75e9-4536-93c0-d507499d2a4b" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="643" height="93" alt="image" src="https://github.com/user-attachments/assets/5dd235cf-4c46-43d8-9020-286ac81485bc" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="748" height="90" alt="image" src="https://github.com/user-attachments/assets/1a4f0d24-0486-46d0-ad0e-0baecbd1a34f" />


sed -n '2,4{s/$/*/;p}' file23

<img width="677" height="92" alt="image" src="https://github.com/user-attachments/assets/640cf08e-b3be-4369-9907-8c210328bc34" />


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

<img width="477" height="138" alt="image" src="https://github.com/user-attachments/assets/f6df139b-0f7f-4410-af3a-d38bb6bc226f" />


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

<img width="480" height="141" alt="image" src="https://github.com/user-attachments/assets/0f7327ce-21be-4d15-aa93-2d5c06693235" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

<img width="738" height="230" alt="image" src="https://github.com/user-attachments/assets/5258b973-2764-40be-a770-82504b6ba64e" />


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

<img width="647" height="108" alt="image" src="https://github.com/user-attachments/assets/9016fd44-f9a7-445b-acf7-887b032bd301" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="796" height="100" alt="image" src="https://github.com/user-attachments/assets/6422c8c6-9fd7-4561-a1e1-c27b0a9b26fe" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="611" height="163" alt="image" src="https://github.com/user-attachments/assets/da1633de-1013-4173-bbda-e35b18a6b670" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="775" height="228" alt="image" src="https://github.com/user-attachments/assets/a5a6372c-5f58-4be2-98f9-3e5c3731b6a6" />


tar -xvf backup.tar
## OUTPUT

<img width="681" height="162" alt="image" src="https://github.com/user-attachments/assets/5604fa9a-a745-40cb-bea5-57e036523eb9" />


gzip backup.tar

ls .gz
## OUTPUT

<img width="536" height="47" alt="image" src="https://github.com/user-attachments/assets/b207cf23-6419-4fc1-a4b8-d60d63308131" />

 
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
