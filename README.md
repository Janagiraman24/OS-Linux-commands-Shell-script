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
![432225731-1bb3120c-1238-4920-a7ea-2ec3150d32b4](https://github.com/user-attachments/assets/7cecdb4c-d337-4259-9d84-6da565cb7968)



cat < file2
## OUTPUT
![432226609-af32b9fb-66a8-4474-b17b-d75b9b7926d4](https://github.com/user-attachments/assets/5c4ed8df-b15b-41a9-aadf-a330d7bd7c29)


# Comparing Files
cmp file1 file2
## OUTPUT
 ![432231466-fe022908-c0d6-4750-a3af-08e4f0928dcb](https://github.com/user-attachments/assets/c0650aff-4f4c-4178-beec-c7f2d7c91012)

comm file1 file2
 ## OUTPUT
![432231816-4e232ce9-64ca-4bde-9d12-5f98108d8346](https://github.com/user-attachments/assets/c50bb2f0-1cc1-44e4-bd1a-82de0450dc53)

 
diff file1 file2
## OUTPUT
![432232583-16204101-b55b-4a1c-835f-9bb417dfac40](https://github.com/user-attachments/assets/c7292ecb-9a32-4d1e-89d3-02cf50659841)


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
![432234070-00c489fe-0939-43f2-b5cf-f571c047250d](https://github.com/user-attachments/assets/730c0f76-5a72-4233-b02b-fb560b903c4b)




cut -d "|" -f 1 file22
## OUTPUT
![432235004-eef254a6-6aa9-4363-986d-af6a4e32503b](https://github.com/user-attachments/assets/d81b4a44-bd63-4449-951e-e1e30c8d2815)



cut -d "|" -f 2 file22
## OUTPUT
![432235451-b78a2f7e-6686-4576-a855-78896122233d](https://github.com/user-attachments/assets/a3106286-30fe-4ba9-a80d-11b2d6934eee)


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
![432236299-2572e17d-61ce-47f1-b253-d351109263a8](https://github.com/user-attachments/assets/5a1bda4b-8600-4030-acd0-9764b9dbe118)



grep hello newfile 
## OUTPUT
![432236570-1ee46c9f-b7df-4ecf-913c-0aea790402f6](https://github.com/user-attachments/assets/ae428526-dd9f-493e-8fb0-aa31deb4d9e0)




grep -v hello newfile 
## OUTPUT
![432237107-6a8b672b-5c17-41d6-840d-ad8af4cb25e7](https://github.com/user-attachments/assets/1bb37192-8a56-43aa-b09c-54795022cf62)



cat newfile | grep -i "hello"
## OUTPUT
![432237461-d7ff3b27-3730-4c8e-b763-fed7469c7cc2](https://github.com/user-attachments/assets/69d8160d-6ff3-41a9-8bf3-da1d342e7562)




cat newfile | grep -i -c "hello"
## OUTPUT
![432237716-31eda373-42d7-403e-93b8-3942a6f8823a](https://github.com/user-attachments/assets/bbefb521-7608-4b7b-9071-76c1c768283e)





grep -R ubuntu /etc
## OUTPUT
![432238537-8dde9438-13f6-4e9c-9ab6-1cd908c51940](https://github.com/user-attachments/assets/1d4abb99-29fa-425a-b85a-4e609e487ca7)



grep -w -n world newfile   
## OUTPUT
![432239195-9c65ea2b-f5ad-4a02-88fd-03ed6741c893](https://github.com/user-attachments/assets/7789679d-65a7-41a4-9c79-e9b231be236e)


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
![432240596-c39fda35-314c-4fd4-a263-9803cc1aaaf3](https://github.com/user-attachments/assets/7072ca25-5b7c-401d-82d3-4452182caee0)




egrep -w '(H|h)ello' newfile 
## OUTPUT
![432240869-eed0c643-a36c-44ea-a416-38dcf24bfd94](https://github.com/user-attachments/assets/4bc6533a-1559-4ed9-b243-c7851a719207)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![432241187-2407a2da-bc0d-4dd0-8551-76e5a0ea5e05](https://github.com/user-attachments/assets/865ddaa0-f2cb-4be9-934a-b4e21eefbc9e)




egrep '(^hello)' newfile 
## OUTPUT
![432241461-44050480-107a-4e3f-8ade-bc1ac9627d95](https://github.com/user-attachments/assets/fc900966-19eb-406d-bd89-ca5fe5b41fb6)



egrep '(world$)' newfile 
## OUTPUT
![432241702-93889252-1369-46d2-b8d9-e0e3fd509f7b](https://github.com/user-attachments/assets/7ed0c713-b887-41ae-8102-5ade217102bd)



egrep '(World$)' newfile 
## OUTPUT
![432241773-f7e818eb-8ce4-4f31-af9e-3749c6a32b5e](https://github.com/user-attachments/assets/687d8f0f-96f9-4ae9-b02f-22003a055df6)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![432242580-ad4c2dde-1e04-4590-8929-0b97142b2864](https://github.com/user-attachments/assets/51dabdea-afd5-43a0-9585-06e788da1b31)



egrep '[1-9]' newfile 
## OUTPUT
![432242780-de1e8d0a-93fd-4d58-9be3-12cc208f55b8](https://github.com/user-attachments/assets/bf16b3ba-ef00-4df1-bec5-546d55e23040)



egrep 'Linux.*world' newfile 
## OUTPUT
![432243473-8bd1e9ba-19d7-4fff-9ad9-e2bd30746e97](https://github.com/user-attachments/assets/0091f790-2325-4fa9-9298-34abf5d57c6e)


egrep 'Linux.*World' newfile 
## OUTPUT
![432243473-8bd1e9ba-19d7-4fff-9ad9-e2bd30746e97](https://github.com/user-attachments/assets/1a105562-ae15-42ae-a5bb-5643ce912e0b)


egrep l{2} newfile
## OUTPUT
![432243676-40fa2653-6700-4f6a-8f8b-719e562b415f](https://github.com/user-attachments/assets/67442414-b7cd-4d5f-b67d-195ac666b89c)



egrep 's{1,2}' newfile
## OUTPUT 
![432243972-1d2b3a5e-6409-474f-8be0-b21192414c1f](https://github.com/user-attachments/assets/5a314bda-261e-4fd7-b626-d632bd919ffc)


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
![432245212-14ceb3c8-6905-4c47-a233-72552615d761](https://github.com/user-attachments/assets/587dc90e-7d4e-4245-9320-3a903b1b53d7)




sed -n -e '$p' file23
## OUTPUT
![432245626-7084c57b-3cbc-4397-a455-4962d6372bfe](https://github.com/user-attachments/assets/85df832d-1fa7-4125-bece-2aa6f23f78bd)



sed  -e 's/Ram/Sita/' file23
## OUTPUT
![432246382-6cf2d482-f1e5-4271-bd04-352fd9c85d62](https://github.com/user-attachments/assets/31b24af3-3e7c-427b-beea-a060ed6a6b56)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![432246721-cce0ae77-a28f-4322-b316-c54d3eeea180](https://github.com/user-attachments/assets/45cab5e1-5e5b-4df6-ac6b-a14a7bf444fd)


sed  '/tom/s/5000/6000/' file23
## OUTPUT
![432246962-2598f70d-bee9-4e49-8bdc-e97761ce74a5](https://github.com/user-attachments/assets/5bf33274-3e22-4ef2-b5aa-2122a3e56d9e)



sed -n -e '1,5p' file23
## OUTPUT

![432247424-d70d7409-ec60-4000-ac14-8c6079528a09](https://github.com/user-attachments/assets/3a33148d-ccba-471e-a245-4beb6339dd6a)


sed -n -e '2,/Joe/p' file23
## OUTPUT
![432248018-5432ce87-44fd-42cc-9e5d-7cdfc31739b2](https://github.com/user-attachments/assets/158c830a-5d49-4272-afae-2394bbdf4c0f)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![432248018-5432ce87-44fd-42cc-9e5d-7cdfc31739b2](https://github.com/user-attachments/assets/9e4e7b93-7d51-4dae-9437-5785d4a64d64)



seq 10 
## OUTPUT
![432248797-fea8e390-8ae0-4a90-a28e-8d2b2c2c4c76](https://github.com/user-attachments/assets/14142e03-7e8f-4b83-8dde-db0b7108e17a)



seq 10 | sed -n '4,6p'
## OUTPUT
![432249057-5fae905a-ba24-4765-8c93-def41c9264b4](https://github.com/user-attachments/assets/6683131a-b2c6-4c06-ac04-4862f744740b)



seq 10 | sed -n '2,~4p'
## OUTPUT
![432249287-44312c45-a1f5-4c19-a82c-79e3f0d6d171](https://github.com/user-attachments/assets/428f92ea-dd76-4de5-ac6a-e29e53fb85f4)



seq 3 | sed '2a hello'
## OUTPUT
![432249640-76cd1775-4b5d-485c-a622-3de51dad01b4](https://github.com/user-attachments/assets/bafbcd53-e48c-4e82-9344-3769e00122f2)



seq 2 | sed '2i hello'
## OUTPUT
![432249866-9c38dd7b-fef7-4d2e-8791-caef77ced470](https://github.com/user-attachments/assets/fe9c83ba-0962-43a5-a69a-1143d3d38b2d)


seq 10 | sed '2,9c hello'
## OUTPUT
![432250148-39431da3-26f8-47ee-98eb-1e818f80398e](https://github.com/user-attachments/assets/ab8e554e-663b-4228-964f-d5a8da5f326c)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![432250572-28da254d-8c2f-4fb9-bb7c-e678a52d4b8f](https://github.com/user-attachments/assets/a6a9e2bd-02b8-4f30-b09d-b56acbcb1429)
![432251582-c1640cd5-0eda-4c6b-9eb7-cc4c06a9868e](https://github.com/user-attachments/assets/b6f40e58-ab79-4ab9-a52c-65fcefb4e388)



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
![432252380-5db50e6c-391d-4ba8-a38f-93846e4eba4c](https://github.com/user-attachments/assets/740a477c-99bd-4784-9199-58ea6b5da707)


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
![432252817-de81f100-b407-4b5d-a3c4-e564b3d9b3b2](https://github.com/user-attachments/assets/4bc098e6-3e50-4a66-8b84-97496fcd3914)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![432253098-8ba44fdd-6db2-4a8a-8768-397d16d1fb43](https://github.com/user-attachments/assets/cdfdd393-8b2c-4443-9ff1-0ef94e637353)

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
![432253858-b0f4cf88-27be-4ead-80f7-08225513dd8a](https://github.com/user-attachments/assets/7d0e9319-653d-4eed-80f3-fabf05d54095)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![432254220-9b25a0f1-e752-4909-8598-82e5eb880ad4](https://github.com/user-attachments/assets/d71e8467-4be9-4a93-9ab5-67737f144847)



#Backup commands
tar -cvf backup.tar *
## OUTPUT
![432254507-7f0aa5d5-785d-4c8e-949c-d1d879c66bef](https://github.com/user-attachments/assets/f7a48e6a-02cf-42ea-a0d6-e05bfdfd2386)


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
![432606968-8c56c8fb-bd94-4513-8599-0566c847d152](https://github.com/user-attachments/assets/6fc28527-ce43-4039-9ff0-73e31e7cd302)


tar -xvf backup.tar
## OUTPUT
![432607140-92c2b763-f1b8-4ded-90f3-0c1e51d63527](https://github.com/user-attachments/assets/ac55f811-c36e-4930-b538-8880cd110bc1)

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
![432608433-0932e73f-7810-4c97-bd78-241311cf159f](https://github.com/user-attachments/assets/52ae2a85-d5c4-4867-af8b-9175f8dc06a1)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![432608735-7f41c8dc-54c2-46c4-8da7-c5ab566be484](https://github.com/user-attachments/assets/c966588d-f66c-4b0a-a5f8-713f7231db69)



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
![432609654-e937d554-8cd1-4050-a573-3eeff4519d77](https://github.com/user-attachments/assets/462b5aa0-78d6-44df-a75a-d17ced6757c5)

 
ls file1
## OUTPUT
![432609787-2d3b80e3-d9a2-426f-a255-2fcf8b44b9c1](https://github.com/user-attachments/assets/190686c1-f4c1-464f-9778-c0eb2441cee7)

echo $?
## OUTPUT 
![432609898-80397abf-0009-41c7-9d67-c84ec7bae2ae](https://github.com/user-attachments/assets/019c426e-3a0d-48f9-92a4-3916997d0c48)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 ![432609988-e33fdeb7-12a1-46c6-b04a-c008a5119e00](https://github.com/user-attachments/assets/0d4a139f-90e0-46ac-aa53-5e0c4dfc8d68)

abcd
 
echo $?
 ## OUTPUT
![432610794-87d0f7ad-127f-481a-a2c6-95972550bfef](https://github.com/user-attachments/assets/c60ee6b9-8a9a-4986-a901-e9cd7a818f89)


 
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
![432611344-81fd545e-7fcf-42a1-bf9e-6985a6a971d2](https://github.com/user-attachments/assets/7d730e50-285d-4893-8158-dbe3dbac3a94)



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
![432612248-91a5283a-ca9d-4bea-8e7e-608d90716214](https://github.com/user-attachments/assets/3c05b96b-3fa5-4f7e-a838-56fd1b7632b7)

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
![432612760-bcdae15b-82d6-4040-8e87-289b1139f3c6](https://github.com/user-attachments/assets/c25f526c-34bb-4640-bdd2-53757ffb586e)



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
![432613192-a17bf600-aa8f-48eb-8e2c-01b27a7a2599](https://github.com/user-attachments/assets/29dc8345-48f0-458d-bc25-3d4cabc09d25)

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
![432613981-3bcbb9f8-ca91-41f3-9c29-f7a9986f88e0](https://github.com/user-attachments/assets/4dfadfa6-b3f0-453b-997d-9ed1cb23f60c)

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
![432614423-cddfced1-6aa4-4b6b-82c7-3ebd5633bee1](https://github.com/user-attachments/assets/c731a44d-3852-4a83-aa94-7703cb3ee96a)


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
![432614701-8f2eca5f-682c-42cd-bae5-b8bef51dfdb4](https://github.com/user-attachments/assets/5923319d-2dec-41a4-93f5-ea34b06b0f6b)

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
![432615797-e944ec20-f4d7-47df-a71b-9f5b69784b13](https://github.com/user-attachments/assets/b2bdb787-5d52-475f-9cf3-43bc75b5c895)

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
![432615962-c1e21c04-c88e-4989-86d5-635b2be6deef](https://github.com/user-attachments/assets/90a06d88-1cb5-4f53-b0d1-f496e5497997)


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
![432616282-cd8918fe-35f7-49e0-beb8-5b54a2b9682d](https://github.com/user-attachments/assets/7b26f3d3-440c-48bc-b943-d252c886c692)

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
![432617641-fa1001aa-71d9-4f42-b2c2-3c3c07094b0a](https://github.com/user-attachments/assets/40784443-1954-4a36-8a07-522286435c62)

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
![432617921-783c7ff7-c516-4b2f-bcd6-1f6fa1679cca](https://github.com/user-attachments/assets/19ee7986-d617-43cc-93b2-b9f23d132b6c)

 
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
![432618094-bf6125a8-7742-4fe5-99f6-ec98b7c75159](https://github.com/user-attachments/assets/5bdaf0bd-63c5-4f55-8c3b-5fc814f2ecab)


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
 ![432618458-55705e99-e14a-4115-9265-3ee37c3b1171](https://github.com/user-attachments/assets/891ee5ee-c783-41cb-9b82-09f502ff4eb9)

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
![432618802-845ac51b-7e90-4597-bd37-ac42fa97f1ff](https://github.com/user-attachments/assets/4f129089-1983-427a-a217-845412bfade5)


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
![432619079-460cd5d1-8fae-445b-a792-f1825e06ded0](https://github.com/user-attachments/assets/4f9e52b2-731c-404a-8670-0ec2d5cd1500)



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
 ./funcex.sh ![432619341-a2c100be-3240-4f81-a102-a50b269f95d6](https://github.com/user-attachments/assets/2ba48b86-1121-4e7d-b46c-2a150b524256)


 
 ./funcex.sh 1 2![432619459-be1ca228-9ad2-419c-9f81-ddabdda530d1](https://github.com/user-attachments/assets/5ed66447-def4-44fb-b82a-fa2817ca2718)


 
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
 ![432619779-7e9cc1cd-0a57-4764-9a35-1be41549d5ee](https://github.com/user-attachments/assets/7ddbd527-edf6-4a7d-9aa0-d6e482bb36f2)

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
 ![432620384-03faac37-2742-48f2-9a95-e8af707ba948](https://github.com/user-attachments/assets/feb330e0-9aec-4a0b-b538-c9a895273bbc)

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
 ![432620669-7bc797da-f3c8-4ca9-b4d6-4c3156d11f0e](https://github.com/user-attachments/assets/1ec7719a-73e9-43c3-92e5-cdd74753ee07)

 
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
 ![432621130-d7b4a7e9-17ee-40ad-841e-76fd7525e916](https://github.com/user-attachments/assets/41c9679f-5b81-4473-bab0-511e6f0a5247)

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
![432621807-fb4afc2b-262f-451f-a36e-7158fca52d2b](https://github.com/user-attachments/assets/6ed97653-df6c-4575-9263-c17e08d6a80c)


# RESULT:
The Commands are executed successfully.
