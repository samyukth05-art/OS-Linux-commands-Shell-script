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
<img width="420" height="116" alt="image" src="https://github.com/user-attachments/assets/7b9151a5-9ba4-4eb4-a6ce-ee56deeb7a69" />



cat < file2
## OUTPUT
<img width="452" height="183" alt="image" src="https://github.com/user-attachments/assets/3257d706-fbe7-4dbd-aa58-5b5c598906cd" />


# Comparing Files
cmp file1 file2
## OUTPUT
<img width="513" height="60" alt="image" src="https://github.com/user-attachments/assets/9b754b2a-b5a2-4596-8203-8fd4f68ea0f3" />
 
comm file1 file2
 ## OUTPUT
<img width="496" height="281" alt="image" src="https://github.com/user-attachments/assets/ff96f8da-bea6-4b6d-a641-36775446f3ef" />

 
diff file1 file2
## OUTPUT
<img width="572" height="355" alt="image" src="https://github.com/user-attachments/assets/9f92b7a0-7fde-4e0e-8872-c63cc95d45e9" />


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
<img width="463" height="112" alt="image" src="https://github.com/user-attachments/assets/7e5477f5-d41d-449c-9cd7-bb0ba7d85170" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="525" height="137" alt="image" src="https://github.com/user-attachments/assets/b776568d-d625-4bdf-9670-4e00f37aa228" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="521" height="132" alt="image" src="https://github.com/user-attachments/assets/471c1800-25b3-434f-9c24-300ae4004e55" />


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
<img width="522" height="70" alt="image" src="https://github.com/user-attachments/assets/1cd86e12-4a42-4160-b1f4-ac0041c932b8" />



grep hello newfile 
## OUTPUT
<img width="517" height="71" alt="image" src="https://github.com/user-attachments/assets/a4af7aa1-7cee-49bd-8f5f-3f07ac38912c" />




grep -v hello newfile 
## OUTPUT
<img width="530" height="82" alt="image" src="https://github.com/user-attachments/assets/a585caa0-069b-4c45-adb7-679787293432" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="667" height="98" alt="image" src="https://github.com/user-attachments/assets/75039795-dea8-4bc3-9bb8-e10891dcde67" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="687" height="68" alt="image" src="https://github.com/user-attachments/assets/aaa72c39-1ea8-4e18-b9f6-41b349a6605a" />




grep -R ubuntu /etc
## OUTPUT
<img width="777" height="245" alt="image" src="https://github.com/user-attachments/assets/b13b1365-8f04-4822-95bd-fde36e41eca0" />



grep -w -n world newfile   
## OUTPUT
<img width="697" height="91" alt="image" src="https://github.com/user-attachments/assets/7140deb3-2a37-4c1c-b6b1-e5989ff0b436" />


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
<img width="750" height="97" alt="image" src="https://github.com/user-attachments/assets/9f13b8bf-482a-4911-93bf-b10c3fd028c6" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="722" height="97" alt="image" src="https://github.com/user-attachments/assets/fe21074f-fa54-43c6-bcac-8154bdf03cd1" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="741" height="100" alt="image" src="https://github.com/user-attachments/assets/f330b551-cae4-4ffe-b3eb-1183ef64527f" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="705" height="80" alt="image" src="https://github.com/user-attachments/assets/9a79c306-a0db-4f68-85c1-55750b6610f1" />



egrep '(world$)' newfile 
## OUTPUT
<img width="658" height="73" alt="image" src="https://github.com/user-attachments/assets/488cd677-6375-4601-894a-ce549c1e82c5" />



egrep '(World$)' newfile 
## OUTPUT
<img width="833" height="72" alt="image" src="https://github.com/user-attachments/assets/1b72b651-c844-483b-98ef-370540d021b0" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="673" height="93" alt="image" src="https://github.com/user-attachments/assets/9f325aa1-2dec-4730-b38f-75f907ee9bfa" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="707" height="71" alt="image" src="https://github.com/user-attachments/assets/da6a3651-4ebd-447e-8ad5-5080b532cced" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="725" height="75" alt="image" src="https://github.com/user-attachments/assets/8f2b13c8-2a35-4b0f-92da-5b9a6a7f058b" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="667" height="65" alt="image" src="https://github.com/user-attachments/assets/4ce97986-2ba6-4cc6-9399-76de8d14fa0b" />


egrep l{2} newfile
## OUTPUT
<img width="775" height="100" alt="image" src="https://github.com/user-attachments/assets/5ea22950-46aa-4e5f-9b04-a4aaacbdb9fe" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="766" height="129" alt="image" src="https://github.com/user-attachments/assets/6c76b47c-82ce-4943-8ddd-c90163004072" />


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
<img width="536" height="61" alt="image" src="https://github.com/user-attachments/assets/390a977b-b2e8-4c6a-9e4a-8fb85592767a" />



sed -n -e '$p' file23
## OUTPUT
<img width="552" height="62" alt="image" src="https://github.com/user-attachments/assets/649bc1b5-7136-457c-a3f3-5f7655808fd0" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="592" height="270" alt="image" src="https://github.com/user-attachments/assets/f5af7909-0f27-448b-b31b-92d06a3caab4" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="603" height="281" alt="image" src="https://github.com/user-attachments/assets/924530d4-dc37-4138-84f0-899b7ebd4c6d" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="667" height="287" alt="image" src="https://github.com/user-attachments/assets/f6c494a5-32d7-4da9-906d-38ac2946b7e6" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="667" height="190" alt="image" src="https://github.com/user-attachments/assets/cc857af3-d4cc-47d3-9166-1e88bb83b0f1" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="612" height="128" alt="image" src="https://github.com/user-attachments/assets/f830cb9f-e8fc-442f-bde8-30bf971e4320" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="661" height="93" alt="image" src="https://github.com/user-attachments/assets/f9ed6af0-7319-48d3-a8f0-7cef305febe6" />



seq 10 
## OUTPUT
<img width="666" height="338" alt="image" src="https://github.com/user-attachments/assets/60e46bb8-8637-4b31-970f-75562f1419a3" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="655" height="132" alt="image" src="https://github.com/user-attachments/assets/72842a06-46a7-4502-a969-f5940b8de166" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="602" height="122" alt="image" src="https://github.com/user-attachments/assets/d171c3c4-a3cf-4649-a539-302fa998b627" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="661" height="123" alt="image" src="https://github.com/user-attachments/assets/405e28d3-805d-4222-9045-3202fdbd02f0" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="617" height="147" alt="image" src="https://github.com/user-attachments/assets/8b360795-6614-4dc9-9e8f-3dfeb17358ba" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="601" height="126" alt="image" src="https://github.com/user-attachments/assets/dd565ab6-28cc-40c6-acaf-08639a3cc260" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="652" height="117" alt="image" src="https://github.com/user-attachments/assets/1688a7fc-86f8-48db-b5ea-ac81590842ab" />



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
<img width="230" height="108" alt="image" src="https://github.com/user-attachments/assets/abcd99c7-b237-4698-8b53-1ce275a3f3cb" />


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
<img width="242" height="98" alt="image" src="https://github.com/user-attachments/assets/b091cc67-d9a5-4ed9-9a22-e420462f9406" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="413" height="148" alt="image" src="https://github.com/user-attachments/assets/e8d0c222-5608-465d-8040-7e6ccf41339c" />

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
<img width="415" height="68" alt="image" src="https://github.com/user-attachments/assets/d405088a-8371-48b8-9de9-5dbb75a05e5c" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="426" height="71" alt="image" src="https://github.com/user-attachments/assets/1b086b49-596c-40e5-a0a6-199444d78ab0" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="217" height="50" alt="image" src="https://github.com/user-attachments/assets/c7f9879e-e44c-4bd5-9a1a-e8a2a687bf02" />


tar -xvf backup.tar
## OUTPUT
<img width="217" height="50" alt="image" src="https://github.com/user-attachments/assets/5832d48d-3398-4ebc-8b60-7e407d3b8df7" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="432" height="87" alt="image" src="https://github.com/user-attachments/assets/d6c777eb-d083-4e58-a152-438b6a019c2a" />

gunzip backup.tar.gz
## OUTPUT

 <img width="431" height="126" alt="image" src="https://github.com/user-attachments/assets/81e33c1d-16bc-4d69-9a99-993e8acf833e" />

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 <img width="434" height="176" alt="image" src="https://github.com/user-attachments/assets/e6a80043-094b-412b-b26a-34ac5df16a17" />

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
<img width="321" height="247" alt="image" src="https://github.com/user-attachments/assets/8cf83edc-a5b9-409e-b57c-6161ab6d2e9e" />

 
ls file1
## OUTPUT
<img width="199" height="34" alt="image" src="https://github.com/user-attachments/assets/9049982a-38e4-4e71-bf0c-0584b0537a47" />

echo $?
## OUTPUT 
<img width="205" height="38" alt="image" src="https://github.com/user-attachments/assets/f0399863-fa38-46ab-8376-29c92946d640" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="188" height="41" alt="image" src="https://github.com/user-attachments/assets/9d070e93-32ad-4aed-b08e-ad2763bbbd0e" />

abcd
 
echo $?
 ## OUTPUT
<img width="362" height="164" alt="image" src="https://github.com/user-attachments/assets/89eab212-c7d7-4597-9d8f-f1c6fcd68b91" />


 
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

<img width="367" height="185" alt="image" src="https://github.com/user-attachments/assets/d3f57539-af0a-4af2-a265-5ccf4df89b20" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="433" height="182" alt="image" src="https://github.com/user-attachments/assets/0ab778a2-5bc3-43df-bf06-8a0126d2e23a" />

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
<img width="429" height="132" alt="image" src="https://github.com/user-attachments/assets/882d8b0f-c3e4-4ad6-9b82-8c3419399f7b" />


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
<img width="393" height="303" alt="image" src="https://github.com/user-attachments/assets/aa23a5af-8e1f-4c1f-a638-7b47f60d56a3" />



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
<img width="413" height="360" alt="image" src="https://github.com/user-attachments/assets/dcfa1ff5-a241-466e-86cf-efca79558cda" />

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
<img width="423" height="366" alt="image" src="https://github.com/user-attachments/assets/f592f502-bd13-4674-bd31-b0b287224cd6" />

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
<img width="416" height="357" alt="image" src="https://github.com/user-attachments/assets/de3437cf-06f7-4fcb-b9bf-33d275619e58" />


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
<img width="380" height="191" alt="image" src="https://github.com/user-attachments/assets/add83a81-d6e5-4dd6-99c5-d908b96855b8" />

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
<img width="358" height="117" alt="image" src="https://github.com/user-attachments/assets/0686eb7a-d808-4d44-b493-334309404052" />

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
<img width="316" height="150" alt="image" src="https://github.com/user-attachments/assets/a83dc7ec-f22f-40a0-82c0-5fb53f451b79" />


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
<img width="289" height="158" alt="image" src="https://github.com/user-attachments/assets/fcc69430-01ce-4ef6-9d28-e11621350a7a" />

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
<img width="432" height="166" alt="image" src="https://github.com/user-attachments/assets/944b13e9-dea3-4223-ba07-2013f28d8588" />

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
<img width="430" height="162" alt="image" src="https://github.com/user-attachments/assets/57e69546-b43a-4d7f-af44-8dc77e52e15f" />

 
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
<img width="431" height="164" alt="image" src="https://github.com/user-attachments/assets/226e5414-56eb-4213-bb0c-a889b777a216" />

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
 <img width="424" height="167" alt="image" src="https://github.com/user-attachments/assets/d4b7555e-4601-4f55-8801-76ce44326752" />

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
<img width="338" height="107" alt="image" src="https://github.com/user-attachments/assets/24635a83-8955-46c5-87f5-0bc1f286e298" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="377" height="79" alt="image" src="https://github.com/user-attachments/assets/b14064ba-3abd-4874-a3a6-7d4b48e6464c" />


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

 <img width="367" height="11" alt="image" src="https://github.com/user-attachments/assets/ff3cc2f7-bba7-4ba0-88d5-1117c667bf75" />

 ./funcex.sh 1 2
<img width="354" height="17" alt="image" src="https://github.com/user-attachments/assets/c05a183f-4a0e-491e-aa36-b40ec626abc7" />

 
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
 <img width="134" height="35" alt="image" src="https://github.com/user-attachments/assets/f9dc44f7-50c1-4fe2-bab3-0bb92d6d4052" />

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
<img width="73" height="38" alt="image" src="https://github.com/user-attachments/assets/3ba424fc-786a-4832-9872-b1878c8728bf" />

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
 <img width="350" height="209" alt="image" src="https://github.com/user-attachments/assets/38f18d40-5bcb-49cd-8e5b-6e49c74d0281" />

 
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
 <img width="267" height="136" alt="image" src="https://github.com/user-attachments/assets/b469381b-9a80-4c30-9f55-c8666cda3403" />

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
<img width="210" height="44" alt="image" src="https://github.com/user-attachments/assets/c9f46fd6-1c5a-4415-97db-706098faa554" />


# RESULT:
The Commands are executed successfully.
