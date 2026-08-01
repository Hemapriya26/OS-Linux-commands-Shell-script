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

<img width="559" height="162" alt="Screenshot 2026-07-24 193525" src="https://github.com/user-attachments/assets/967ee3ae-fb62-4ed7-8cf9-539ad7d47bdf" />


cat < file2
## OUTPUT

<img width="567" height="173" alt="Screenshot 2026-07-24 193710" src="https://github.com/user-attachments/assets/820841b9-2ad0-4b38-b1fc-ab045a5def19" />


# Comparing Files
cmp file1 file2
## OUTPUT

<img width="562" height="80" alt="Screenshot 2026-07-24 193821" src="https://github.com/user-attachments/assets/a97037be-c0d8-429e-9086-ce79163334db" />

 
comm file1 file2
 ## OUTPUT

<img width="560" height="227" alt="Screenshot 2026-07-24 194045" src="https://github.com/user-attachments/assets/c777416c-f488-490f-a697-12091f201cc8" />

 
diff file1 file2
## OUTPUT

<img width="565" height="280" alt="Screenshot 2026-07-24 193944" src="https://github.com/user-attachments/assets/dae08e92-0b4e-44fd-bd23-696e0caabd8e" />


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

<img width="564" height="101" alt="Screenshot 2026-07-24 194320" src="https://github.com/user-attachments/assets/d2919af2-2478-4f3f-be17-56a529b3653b" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="559" height="133" alt="Screenshot 2026-07-24 194515" src="https://github.com/user-attachments/assets/dfc777f6-61b0-4311-bb81-0bc70fc2edf4" />


cut -d "|" -f 2 file22
## OUTPUT

<img width="561" height="133" alt="Screenshot 2026-07-24 194428" src="https://github.com/user-attachments/assets/226ffa5c-8f11-4c91-92dd-01adccf728cd" />


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

<img width="569" height="81" alt="Screenshot 2026-07-24 194737" src="https://github.com/user-attachments/assets/a584500b-9cd5-4013-ade0-e4c8b5a2ff56" />


grep hello newfile 
## OUTPUT


<img width="567" height="70" alt="Screenshot 2026-07-24 194818" src="https://github.com/user-attachments/assets/7d58bd9b-3e0a-4398-93b7-52810868b263" />


grep -v hello newfile 
## OUTPUT

<img width="561" height="85" alt="Screenshot 2026-07-24 194922" src="https://github.com/user-attachments/assets/f80b839d-0f54-42f7-83b6-672cab380bf7" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="568" height="95" alt="Screenshot 2026-07-24 195055" src="https://github.com/user-attachments/assets/f00bb576-a422-4d85-b9ac-4a142d4e6209" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="562" height="78" alt="Screenshot 2026-07-24 204451" src="https://github.com/user-attachments/assets/ed13ff82-897c-4be1-8d3d-a4df6ac047a1" />



grep -R ubuntu /etc
## OUTPUT

<img width="1332" height="561" alt="Screenshot 2026-07-24 204741" src="https://github.com/user-attachments/assets/ea97eb5d-ea4f-44f5-a8f4-912c68350681" />


grep -w -n world newfile   
## OUTPUT

<img width="639" height="100" alt="Screenshot 2026-07-24 205013" src="https://github.com/user-attachments/assets/baa1efd3-f5c8-43b9-a886-63fbb5e0ddbc" />


cat > newfile 
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

<img width="644" height="100" alt="Screenshot 2026-07-24 205537" src="https://github.com/user-attachments/assets/87e5a7d9-afd6-497c-bdc6-67ba1f6aa432" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="645" height="96" alt="Screenshot 2026-07-24 205709" src="https://github.com/user-attachments/assets/21faeca5-b150-4004-8f52-b05040797961" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="648" height="96" alt="Screenshot 2026-07-24 205820" src="https://github.com/user-attachments/assets/c774c997-c218-4ceb-bd25-84a6245f1ad7" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="655" height="72" alt="Screenshot 2026-07-24 205921" src="https://github.com/user-attachments/assets/1870daa8-a2cd-418e-8688-244fa2e654eb" />


egrep '(world$)' newfile 
## OUTPUT

<img width="648" height="103" alt="Screenshot 2026-07-24 210020" src="https://github.com/user-attachments/assets/66531c8e-c67e-4bfc-8b0f-89947af257a0" />


egrep '(World$)' newfile 
## OUTPUT

<img width="647" height="85" alt="Screenshot 2026-07-24 210156" src="https://github.com/user-attachments/assets/5f284d85-1673-4041-bf1b-92787beae821" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="640" height="126" alt="Screenshot 2026-07-24 210303" src="https://github.com/user-attachments/assets/0aa0ad2a-8cf2-4fc0-84a7-7fd780fb0499" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="647" height="87" alt="Screenshot 2026-07-24 210344" src="https://github.com/user-attachments/assets/f4c5bdf0-4427-4685-bf86-e8353f33fae4" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="648" height="77" alt="Screenshot 2026-07-24 210438" src="https://github.com/user-attachments/assets/8e45f58b-1aeb-4f77-bc44-8a962e768d21" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="643" height="75" alt="Screenshot 2026-07-24 210534" src="https://github.com/user-attachments/assets/18b19123-f858-4c51-9d56-7f1fc20ab3b0" />


egrep l{2} newfile
## OUTPUT

<img width="640" height="109" alt="Screenshot 2026-07-24 210735" src="https://github.com/user-attachments/assets/ed1bb07d-756a-4657-a4ac-0f1342f9fa79" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="639" height="122" alt="Screenshot 2026-07-24 210837" src="https://github.com/user-attachments/assets/5cf55b1f-2903-409f-8f59-302d830119d5" />


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


<img width="641" height="77" alt="Screenshot 2026-07-24 211030" src="https://github.com/user-attachments/assets/6ee86c85-e2e5-44f4-8c0d-5fccbd453f41" />

sed -n -e '$p' file23
## OUTPUT

<img width="648" height="75" alt="Screenshot 2026-07-24 211306" src="https://github.com/user-attachments/assets/4a31e988-d6c2-432f-abc6-2b671790fafe" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="649" height="262" alt="Screenshot 2026-07-24 211537" src="https://github.com/user-attachments/assets/0689c7b3-e131-454e-9af1-7f35072ba30a" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="646" height="258" alt="Screenshot 2026-07-24 211928" src="https://github.com/user-attachments/assets/bfb3a757-9905-4700-ae7a-ff1cdf39954d" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="644" height="250" alt="Screenshot 2026-07-24 212059" src="https://github.com/user-attachments/assets/b51c7360-4307-4439-8032-3df8d0749fdb" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="645" height="169" alt="Screenshot 2026-07-24 212208" src="https://github.com/user-attachments/assets/29b67ab1-d80a-468f-954c-7c84d5f61d6a" />


sed -n -e '2,/Joe/p' file23
## OUTPUT


<img width="648" height="126" alt="Screenshot 2026-07-24 212340" src="https://github.com/user-attachments/assets/3ff11298-b6ba-4581-8367-7c6a6c2c0395" />


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="640" height="105" alt="Screenshot 2026-07-24 212443" src="https://github.com/user-attachments/assets/1d55316c-0a78-45a1-923d-f97e9a168ed9" />


seq 10 
## OUTPUT

<img width="648" height="303" alt="Screenshot 2026-07-24 212552" src="https://github.com/user-attachments/assets/1b56dcda-463f-4647-95cf-a472ef37ef7c" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="647" height="134" alt="Screenshot 2026-07-24 212641" src="https://github.com/user-attachments/assets/37a9a997-d602-4ab6-abe0-6996f2b81d9c" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="641" height="125" alt="Screenshot 2026-07-24 212750" src="https://github.com/user-attachments/assets/143e7f31-8afe-4024-a130-cc579863cbad" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="643" height="160" alt="Screenshot 2026-07-24 212842" src="https://github.com/user-attachments/assets/bd613762-885b-47dd-9fbf-11fb144579f0" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="642" height="136" alt="Screenshot 2026-07-24 213031" src="https://github.com/user-attachments/assets/04918c73-d913-474a-ae68-6c4834cbbb60" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="644" height="132" alt="Screenshot 2026-07-24 213140" src="https://github.com/user-attachments/assets/773070fa-128a-4acb-a87d-b78afc5318ad" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="643" height="128" alt="Screenshot 2026-07-24 213427" src="https://github.com/user-attachments/assets/3b6ab101-ed1b-48fd-9f99-353de4bb6680" />


sed -n '2,4{s/$/*/;p}' file23

<img width="634" height="135" alt="Screenshot 2026-07-24 213610" src="https://github.com/user-attachments/assets/466a9e38-92f9-42a8-a454-7c00a720e36b" />


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

<img width="647" height="182" alt="Screenshot 2026-07-24 213807" src="https://github.com/user-attachments/assets/a7c7f23a-085e-4d30-8b93-10d99ebdb3f6" />


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

<img width="648" height="174" alt="Screenshot 2026-07-24 214116" src="https://github.com/user-attachments/assets/b7c513d6-9fe0-47b5-9fd2-17491cb1d564" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

 <img width="646" height="253" alt="Screenshot 2026-07-24 214315" src="https://github.com/user-attachments/assets/207162bc-e0c5-4e02-8531-bfd8c822847d" />


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

<img width="645" height="127" alt="Screenshot 2026-07-24 214528" src="https://github.com/user-attachments/assets/62dd5f44-aca3-441c-8670-b84d66674912" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="645" height="128" alt="Screenshot 2026-07-24 214628" src="https://github.com/user-attachments/assets/3f482d0e-f03d-41d5-97c5-1ace2fba06c4" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="647" height="253" alt="Screenshot 2026-07-24 214747" src="https://github.com/user-attachments/assets/1acbcdcf-c7c4-4c25-8a78-c1c7a9ecec76" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="641" height="410" alt="Screenshot 2026-07-24 215528" src="https://github.com/user-attachments/assets/b005da0d-19c7-4a17-a01e-fdab83b12ead" />


tar -xvf backup.tar
## OUTPUT

<img width="644" height="252" alt="Screenshot 2026-07-24 215720" src="https://github.com/user-attachments/assets/210c1387-378b-4ac0-ad2d-32ce1b59ac70" />


gzip backup.tar

ls .gz
## OUTPUT

<img width="643" height="130" alt="Screenshot 2026-07-24 215910" src="https://github.com/user-attachments/assets/6b428ff8-e76f-40e8-bdda-240a9f23e9af" />

 
gunzip backup.tar.gz
## OUTPUT

<img width="653" height="58" alt="Screenshot 2026-07-24 220357" src="https://github.com/user-attachments/assets/ebb1d5e7-e145-40af-b91f-5f256baecf2b" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

<img width="637" height="177" alt="image" src="https://github.com/user-attachments/assets/ba602f0b-3807-4782-b01f-ee49d9360ad0" />
 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="632" height="287" alt="image" src="https://github.com/user-attachments/assets/e177beae-cf9b-4d3b-b3b4-9429ccbfe3c8" />

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

<img width="798" height="415" alt="image" src="https://github.com/user-attachments/assets/323294cc-1194-4dfd-9103-be1f098eed75" />

ls file1
## OUTPUT

<img width="803" height="86" alt="image" src="https://github.com/user-attachments/assets/79f7f1c1-42c8-479f-a6ed-8fdf1f042d37" />

echo $?
## OUTPUT 

<img width="640" height="75" alt="image" src="https://github.com/user-attachments/assets/a6907e99-53d9-49b7-99a7-2c9646dcdd46" />


./one
bash: ./one: Permission denied
echo $?
## OUTPUT

<img width="628" height="207" alt="image" src="https://github.com/user-attachments/assets/e93b9886-9f7d-4ffb-b98c-251e03d87324" />

 
abcd
 
echo $?
 ## OUTPUT

<img width="628" height="207" alt="image" src="https://github.com/user-attachments/assets/b9c16fc3-169a-4c7b-b515-1ae8e5a3b07e" />

 
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
if [ $val1 \> $val
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
```
##OUTPUT

<img width="627" height="207" alt="image" src="https://github.com/user-attachments/assets/e8ce490a-4b4d-487d-9e95-9e10a884c483" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="627" height="207" alt="image" src="https://github.com/user-attachments/assets/e8ce490a-4b4d-487d-9e95-9e10a884c483" />

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

<img width="697" height="206" alt="image" src="https://github.com/user-attachments/assets/6e635305-dcb0-41ae-96c9-eb7cd858165f" />


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
thenchmod 
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

./ifnested.sh 
## OUTPUT

<img width="712" height="233" alt="image" src="https://github.com/user-attachments/assets/55a4b66c-dbb5-437b-8c04-5d88474c48e2" />


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

<img width="701" height="236" alt="image" src="https://github.com/user-attachments/assets/22117bdc-0bb4-40ab-a778-e83ffce0f7a3" />


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

<img width="627" height="258" alt="image" src="https://github.com/user-attachments/assets/85fd3ab5-b137-4656-b975-8dabdf6e3f08" />

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

<img width="633" height="207" alt="image" src="https://github.com/user-attachments/assets/9dc86cb1-35a2-4d34-83ce-df70c24cab66" />


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

<img width="637" height="177" alt="image" src="https://github.com/user-attachments/assets/c7621c33-bf48-4814-9924-fe5d339d6ab0" />


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

 <img width="637" height="181" alt="image" src="https://github.com/user-attachments/assets/cc963a71-9674-4faa-9425-cd35cf3ee630" />

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

 <img width="632" height="398" alt="image" src="https://github.com/user-attachments/assets/836de66f-564a-47a0-926b-01925cb6fdba" />

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
 
 ## OUTPUT

 <img width="638" height="180" alt="image" src="https://github.com/user-attachments/assets/8b625f93-b87a-4a5a-ae1c-83020ea84fa6" />

 
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
 
# OUTPUT

<img width="631" height="352" alt="image" src="https://github.com/user-attachments/assets/2b00cd6c-211d-402c-a28c-8fd7dfb5809e" />

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

## OUTPUT

<img width="641" height="281" alt="image" src="https://github.com/user-attachments/assets/f111859a-2587-43dd-8a1d-21ebe62bbef3" />

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

## OUTPUT

<img width="630" height="352" alt="image" src="https://github.com/user-attachments/assets/52f76736-c486-4a8d-a416-3418de78ee4d" />

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

<img width="642" height="355" alt="image" src="https://github.com/user-attachments/assets/1a0b7160-7845-4f0b-a680-2fcc28f4b660" />

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

<img width="637" height="195" alt="image" src="https://github.com/user-attachments/assets/ba3af868-ab4d-455d-9194-a189df8e86d6" />

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

<img width="637" height="277" alt="image" src="https://github.com/user-attachments/assets/6dd34031-b462-4032-ab50-ba6dada71cd6" />

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

<img width="631" height="378" alt="image" src="https://github.com/user-attachments/assets/269adea5-d0a3-47c1-a5dd-df5635ee3af8" />

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

<img width="635" height="457" alt="image" src="https://github.com/user-attachments/assets/3c8769b3-7776-439b-9a1a-37b26550886b" />
 
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

<img width="642" height="210" alt="image" src="https://github.com/user-attachments/assets/4951d6b2-20ce-4187-aae0-f776e5df274f" />

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
cat forcontinue.sh 
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

 <img width="627" height="235" alt="image" src="https://github.com/user-attachments/assets/0f17c0bb-a4e2-4fbd-92d7-4fd8d97ebb32" />

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

<img width="627" height="215" alt="image" src="https://github.com/user-attachments/assets/1c51edc3-aaa2-4c51-b195-363ad15033c0" />

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="806" height="217" alt="image" src="https://github.com/user-attachments/assets/ab51e859-0b8f-4b98-aa48-a2af0c2baf4c" />


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

<img width="638" height="196" alt="image" src="https://github.com/user-attachments/assets/fbfcf15a-abb4-49e5-9bc8-08949a907a7c" />

 
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

 <img width="641" height="280" alt="image" src="https://github.com/user-attachments/assets/c26d1144-1f3b-42d0-94a4-7ad3b096ae2a" />

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

 ./argshift.sh 1 2 3

 # OUTPUT
 
 <img width="643" height="340" alt="image" src="https://github.com/user-attachments/assets/3f285c10-5158-4654-9a89-d0292c02b8f2" />

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

 <img width="807" height="535" alt="image" src="https://github.com/user-attachments/assets/37e388be-7617-450a-883c-ec040395d002" />

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

<img width="802" height="374" alt="image" src="https://github.com/user-attachments/assets/111a8b5e-4c38-4fef-ac21-94e3d8e5de6e" />


# RESULT:
The Commands are executed successfully.
