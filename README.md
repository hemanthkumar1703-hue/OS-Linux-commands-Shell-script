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

<img width="456" height="110" alt="437457677-967a622c-6563-4855-ab6e-bd33f3e1a973" src="https://github.com/user-attachments/assets/4dc7ba05-48e1-483f-876d-811a74fdfe5a" />


cat < file2
## OUTPUT

<img width="456" height="110" alt="437457779-9cb30c01-6ca1-4508-b567-920317d92ce7" src="https://github.com/user-attachments/assets/ed65e3cc-a15a-4254-a4b1-1b93e1a0fa75" />

# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="481" height="44" alt="437457912-356f08aa-5611-4bb9-bc5e-02c43c13d403" src="https://github.com/user-attachments/assets/8dbedb66-8f42-4917-bb7e-9166950e4d5d" />

comm file1 file2
 ## OUTPUT
<img width="481" height="198" alt="437458025-9b4f494f-3764-4004-89a7-b6554328d7c4" src="https://github.com/user-attachments/assets/cccafca0-70f5-4bdc-a9c7-a89f232f5efe" />

 
diff file1 file2
## OUTPUT

<img width="481" height="198" alt="437458079-dfe29c5f-7b65-4a49-b361-9bd4c5cb9430" src="https://github.com/user-attachments/assets/f149c9d4-7ec4-4091-8b1d-fcbcb2dec197" />

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

<img width="497" height="54" alt="437458179-f1d13611-bbec-432e-b9cb-85ffb7538742" src="https://github.com/user-attachments/assets/b17ee5fc-fd8b-4463-8eb1-464c15b0dad6" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="531" height="75" alt="437458250-be89e8ec-8d82-46ca-90f7-516446ea7551" src="https://github.com/user-attachments/assets/4e144bce-e279-4723-8d0b-11ca528f82da" />


cut -d "|" -f 2 file22
## OUTPUT
<img width="531" height="75" alt="437458334-06251dfd-c2e1-4033-b83c-699161f82a7d" src="https://github.com/user-attachments/assets/78a0a4aa-c34c-4cd4-b829-491a3ccb73f2" />


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

<img width="531" height="42" alt="437458430-027acbdf-56a3-46b0-862e-dadefb65295a" src="https://github.com/user-attachments/assets/40a7ac55-e5e2-404a-a906-3b869b91d9ca" />


grep hello newfile 
## OUTPUT

<img width="531" height="42" alt="437458510-66c88133-9569-4d73-a191-9b74b320b70c" src="https://github.com/user-attachments/assets/d52522f7-e9e4-4937-a1ab-46d892f1739d" />



grep -v hello newfile 
## OUTPUT
<img width="531" height="42" alt="437458605-54d7af23-a79e-46cb-b549-57664f1d5c57" src="https://github.com/user-attachments/assets/0d10c3f1-255c-47ea-b1a7-c70747e6f526" />



cat newfile | grep -i "hello"
## OUTPUT


<img width="597" height="57" alt="437458711-415d2950-f5c4-4d72-9a82-4eada399247b" src="https://github.com/user-attachments/assets/e0f1a6af-61d4-4068-a2d2-a5a6a3af074a" />


cat newfile | grep -i -c "hello"
## OUTPUT
<img width="630" height="49" alt="437458787-45757001-bf07-41a0-9ca0-f7d1ed2b84ab" src="https://github.com/user-attachments/assets/3ab69f44-cfbe-4503-8850-b598072155ad" />




grep -R ubuntu /etc
## OUTPUT

<img width="630" height="142" alt="437458863-41e662bb-ca4d-4dd5-94e5-10cf130c572d" src="https://github.com/user-attachments/assets/31e6dbfb-9a5e-4f41-a749-52697f6a96ce" />


grep -w -n world newfile   
## OUTPUT
<img width="630" height="59" alt="437458939-2959a482-0122-46d1-9c2b-bcf9d17cc219" src="https://github.com/user-attachments/assets/60ea0773-32ec-448d-8f13-c109cb3cc2ae" />


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
<img width="630" height="59" alt="437463455-78d128c6-04bc-40c6-bf8e-d8abbf76b086" src="https://github.com/user-attachments/assets/bf27ce8b-aaf1-4a2a-8afe-44d615b088fb" />



egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="630" height="59" alt="437463537-4bf9423d-4115-4702-b77d-652036301cc0" src="https://github.com/user-attachments/assets/985e55eb-d514-4f5f-852b-af8fb3407586" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="630" height="59" alt="437463627-14924440-952c-480e-83e3-68d0742c897f" src="https://github.com/user-attachments/assets/4e6eb866-d4fe-4317-b533-b8f2845e060e" />



egrep '(^hello)' newfile 
## OUTPUT
<img width="630" height="37" alt="437463736-1d2da7f4-7edd-4697-a5ab-08b3b15cbe93" src="https://github.com/user-attachments/assets/5a2c688f-e17a-4615-b1c1-92eeddba0690" />



egrep '(world$)' newfile 
## OUTPUT
<img width="630" height="58" alt="437463805-f8d8366d-ded2-41eb-83e4-ebdfba968dd2" src="https://github.com/user-attachments/assets/5984afd7-4044-4120-9a15-3fdab3e83b87" />



egrep '(World$)' newfile 
## OUTPUT

<img width="630" height="42" alt="437463872-3c0717c6-f676-4ea9-b28f-8850ea51a52c" src="https://github.com/user-attachments/assets/c6f0e2dd-0625-4cfc-90c5-c7c28fe82f81" />

egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="630" height="73" alt="437463953-f9c9d21b-2bc4-4b7d-8585-ac393785db8b" src="https://github.com/user-attachments/assets/76b723c5-db1c-4322-9688-63f15e3ddaed" />



egrep '[1-9]' newfile 
## OUTPUT

<img width="630" height="44" alt="437464029-df7c6665-f757-49cb-ac27-e218c651c7fe" src="https://github.com/user-attachments/assets/78bf5d8d-b7cd-48cd-8952-8bba348ee5b4" />


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="630" height="42" alt="437464120-e6f5f5cc-1313-415b-babd-30bf5c4828b9" src="https://github.com/user-attachments/assets/74b679c5-aaae-49f5-98e6-4db3b49e7a0a" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="630" height="42" alt="437464182-af4ce7ef-128f-4e4a-b1c9-6fe459f9cc59" src="https://github.com/user-attachments/assets/0c2dce3c-08f2-46fa-a73d-49997af87511" />


egrep l{2} newfile
## OUTPUT

<img width="630" height="58" alt="437464298-b8033a58-9387-4802-8ae1-e082b998bf40" src="https://github.com/user-attachments/assets/9d4c98c6-e50e-44fb-b9e6-e83764e1f9f7" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="630" height="77" alt="437464408-31237cb8-66ad-42f9-a942-5bd7478096c1" src="https://github.com/user-attachments/assets/cd2a0713-979e-4db3-9225-47af408e246c" />


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

<img width="889" height="44" alt="437489915-7b94549c-1754-4c4c-8d1c-3b4ef4057d90" src="https://github.com/user-attachments/assets/f8de55dd-b41d-42be-9b48-67035d212ba0" />


sed -n -e '$p' file23
## OUTPUT

<img width="889" height="44" alt="437489999-d6c1017b-dcfe-4ba2-9968-6fd515f70ccc" src="https://github.com/user-attachments/assets/1549eb37-f674-42c6-9a59-4eaabdd629ce" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="940" height="169" alt="437490090-defc7fe9-c3e9-43e5-9466-e52556533f6e" src="https://github.com/user-attachments/assets/d306f679-159a-4abc-8f35-b7c48359562d" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="950" height="169" alt="437490253-29a39431-6510-4cfa-97e7-4bcc7ff0899a" src="https://github.com/user-attachments/assets/25ed3755-b626-4ccf-b477-b41b84f73ed8" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="952" height="117" alt="437490339-b575e87f-9fb9-45a2-adb0-094b8315abb1" src="https://github.com/user-attachments/assets/0be109f3-5dc1-4c54-b832-44abffff5356" />


sed -n -e '1,5p' file23
## OUTPUT
<img width="952" height="117" alt="437490339-b575e87f-9fb9-45a2-adb0-094b8315abb1" src="https://github.com/user-attachments/assets/b981eacb-5ba3-4e8f-bdf0-3aea5d06a39f" />



sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="951" height="78" alt="437490429-b6783de6-e36c-48db-9ee8-1089bd9f6e99" src="https://github.com/user-attachments/assets/ab940fb3-3161-446d-98fd-e0cfba229165" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="969" height="62" alt="437490516-523a4b3c-1180-4cf8-8e3e-b7663c01c022" src="https://github.com/user-attachments/assets/b3743cc2-b0d3-4b4e-b419-bec14fcd82f3" />



seq 10 
## OUTPUT


<img width="969" height="62" alt="437490516-523a4b3c-1180-4cf8-8e3e-b7663c01c022" src="https://github.com/user-attachments/assets/a916452d-947d-4f74-bf81-4bf41550ca99" />

seq 10 | sed -n '4,6p'
## OUTPUT

<img width="754" height="198" alt="437490585-4f177b06-7938-4755-9924-6a3464e1bcc4" src="https://github.com/user-attachments/assets/8967a526-2ecf-4902-bdc8-2819731b99e0" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="888" height="79" alt="437490656-c722792b-646b-4b85-9124-a8f20ef42d96" src="https://github.com/user-attachments/assets/31a184d7-b6dc-44a1-b51a-eca764e04aa2" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="891" height="94" alt="437490895-805a4134-3397-4783-be68-6d1d061c650c" src="https://github.com/user-attachments/assets/2c616457-9311-42f0-b011-0028e86f5d77" />


seq 2 | sed '2i hello'
## OUTPUT
<img width="890" height="82" alt="437490965-c59f4705-58a5-47ff-b223-06733cbcb06e" src="https://github.com/user-attachments/assets/39e2c059-3fc0-477c-a93a-5e798d57d8fd" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="910" height="80" alt="437491048-9395f677-52f8-4f75-b137-adcc767a2519" src="https://github.com/user-attachments/assets/4a6380d3-db68-4cc6-8031-f21055537206" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="954" height="76" alt="437491145-4f70c8ec-cc80-47a2-8095-4215f0fa18f2" src="https://github.com/user-attachments/assets/a088edaf-dafb-44e0-b629-5faffb3f132f" />



sed -n '2,4{s/$/*/;p}' file23

<img width="954" height="76" alt="437491231-da603a99-e502-4770-8fc3-bb2ad1a032db" src="https://github.com/user-attachments/assets/3f265dc8-02f4-4223-95cf-4fb65c0ecd6b" />

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
<img width="796" height="112" alt="437493282-66fa5f6e-5852-46e9-b870-b38b84b512e6" src="https://github.com/user-attachments/assets/c1efcb66-5808-4573-aa22-4bde0c4e7432" />


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

<img width="796" height="112" alt="437493372-787b56a3-f849-4513-a704-237e72aa2ac6" src="https://github.com/user-attachments/assets/85160bf8-9790-4155-bc86-cb2e0e65d72f" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="1006" height="169" alt="437493522-2381e510-0bf0-4450-bc39-de38ea034bb9" src="https://github.com/user-attachments/assets/d13b076b-948b-46fb-9aa0-c3a70b2fd85e" />

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
<img width="947" height="75" alt="437494744-098afbcc-076c-4f85-b9d6-c51cf0fb0d46" src="https://github.com/user-attachments/assets/a6a6da1b-7011-4599-a2df-b3698ca07cb6" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="1055" height="76" alt="437493789-62e2fa63-7f75-481d-b9b0-cbd070534217" src="https://github.com/user-attachments/assets/8a18761f-f452-465e-a68b-7a3534407160" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="892" height="363" alt="437493876-c28c08b3-4839-4fa5-af49-da520d25b9f4" src="https://github.com/user-attachments/assets/c712d47b-d7d5-4c77-92c0-4c0f718d7a0e" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="967" height="1001" alt="437493953-95ee4d5e-81f5-46aa-b221-9d84cf353090" src="https://github.com/user-attachments/assets/95bd63e3-61b3-4bec-8667-9f26fbc3e048" />

tar -xvf backup.tar
## OUTPUT
<img width="967" height="1001" alt="437495171-a3ea4426-447a-423d-b238-37cfd64a32c2" src="https://github.com/user-attachments/assets/530ae9df-23ee-48ee-8fc7-ea9d9b810710" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="861" height="44" alt="437495364-0f4f0e96-53c3-4e67-ae22-3ff83d31cdad" src="https://github.com/user-attachments/assets/5b4970a7-65cd-49b6-a35a-be31b04bcbb7" />

gunzip backup.tar.gz
## OUTPUT
<img width="1662" height="279" alt="437495471-1545a8ab-15b6-4fea-b67c-d6778656d289" src="https://github.com/user-attachments/assets/342079b6-d998-49b5-83ac-6f6ded92754e" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 <img width="1110" height="134" alt="437497627-2cb093bc-b1c0-4927-9f44-8648e99bdee7" src="https://github.com/user-attachments/assets/12270336-1c9d-46aa-87af-d3f5290842d1" />

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="942" height="161" alt="437508416-6503d8ea-f020-4a33-bc54-d80d3bc44a30" src="https://github.com/user-attachments/assets/55ce85f4-d26c-442d-8529-3ab44ddc7555" />


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
<img width="901" height="507" alt="437508957-5eb11545-912f-44d6-bff7-fbc0cfbe09fe" src="https://github.com/user-attachments/assets/ad975d24-444d-4307-a0be-fccdcee76f46" />

 
ls file1
## OUTPUT
<img width="773" height="35" alt="437509029-8e0c0b06-7fa2-404f-8f27-57da942b2b3f" src="https://github.com/user-attachments/assets/8b6404e6-10e8-4491-88ed-bceab793e0bd" />

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 <img width="773" height="35" alt="437509029-8e0c0b06-7fa2-404f-8f27-57da942b2b3f" src="https://github.com/user-attachments/assets/7211a6d2-2e08-4dcb-b1d9-fa7cf6118188" />


echo $?
## OUTPUT 
 <img width="773" height="45" alt="437509313-fa3cc91f-4dc8-4c9c-b285-58fe15eead88" src="https://github.com/user-attachments/assets/04bec130-b537-4766-8eef-9c749d0ddd89" />

abcd
 
echo $?
 ## OUTPUT


<img width="769" height="185" alt="437509663-f01acb5d-8c5e-4542-8978-82bfef0a3ea5" src="https://github.com/user-attachments/assets/5f11c6f0-dfd9-463f-80f7-7ddefc698265" />



 
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

<img width="840" height="186" alt="437509891-6b566efb-6d31-498e-9c54-72874711055e" src="https://github.com/user-attachments/assets/e92ead8f-1cb5-4d08-a9d2-ea205786582f" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="804" height="45" alt="437511549-83070a40-be1d-4d2a-9c54-3ef580be930a" src="https://github.com/user-attachments/assets/e97068a8-9644-4c18-9b9b-65ba843ab24f" />


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
<img width="824" height="47" alt="437511842-9b815b7d-899c-4084-be1a-1a71b889e898" src="https://github.com/user-attachments/assets/ddce2b75-51d1-473c-8820-f540248cb6f7" />

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
<img width="820" height="82" alt="437512019-3d1162a1-7204-4f55-97b5-b77317da78f6" src="https://github.com/user-attachments/assets/c6047721-47a9-40f0-98ac-e04f234049f5" />



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
<img width="792" height="62" alt="437512535-d16f07c4-9edf-45f7-9286-86dd9ac47242" src="https://github.com/user-attachments/assets/3326ec12-2677-455b-8855-b79dfb27f00d" />

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
<img width="820" height="82" alt="437512682-df476fb2-bedd-4247-a5bf-b6e4ee9cbc67" src="https://github.com/user-attachments/assets/52ed8ef4-69b4-444c-8800-23d9619a433c" />

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
<img width="823" height="44" alt="437512754-fb6e93b7-597a-4a0d-ac44-6ae3c8006f04" src="https://github.com/user-attachments/assets/d5b224c4-5702-4ab8-af0a-d42db23fd7e2" />


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
<img width="823" height="44" alt="437512826-2ab8d86f-3071-40f3-a001-a61e19bd85ba" src="https://github.com/user-attachments/assets/4a7effdb-06ae-4cb4-82e6-a19a685ce4a1" />

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
 <img width="823" height="44" alt="437512980-f6846a1c-12ee-40bf-9922-0115741fd0c1" src="https://github.com/user-attachments/assets/96762000-45d8-45e3-aa4b-149857b705c9" />

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
 <img width="829" height="203" alt="437513129-e42d36e7-94c0-4d9a-bfab-6dce811876f2" src="https://github.com/user-attachments/assets/be951f86-8aa2-492b-9be3-d9823416861e" />cat untiltest.sh 
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
 
 
 <img width="829" height="100" alt="437513645-9cc518d6-6d3d-40b3-96ce-e07af2ba7387" src="https://github.com/user-attachments/assets/4dedb3cd-dc18-40c8-8ddf-86cb2c4e4790" />

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
 <img width="789" height="128" alt="437514299-10a7b7fc-bc85-41ec-9d29-c49e824c0d45" src="https://github.com/user-attachments/assets/dad51963-e065-480f-a85d-f1d578b062f6" />

 
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
 <img width="789" height="128" alt="437514299-10a7b7fc-bc85-41ec-9d29-c49e824c0d45" src="https://github.com/user-attachments/assets/bab76644-a1b6-430a-af23-e7276418b441" />

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
 <img width="784" height="80" alt="437513944-243b7eef-0e93-4b51-a93c-3af8a9284148" src="https://github.com/user-attachments/assets/cc37ab58-957e-453e-8af8-7d5eda956c68" />

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
 <img width="787" height="152" alt="437514672-c514697f-d795-4272-94cc-1e3b8945d19f" src="https://github.com/user-attachments/assets/d584dca2-49a6-45d5-9474-16dec9ce891a" />

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
<img width="816" height="113" alt="437515002-7f28d4a7-d821-4e95-8f38-e8223113babc" src="https://github.com/user-attachments/assets/fa931d10-bf3c-402c-9a8f-885fb583e0f8" />

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
<img width="823" height="115" alt="437515188-b26f7b95-3af3-4d24-a1ae-2a51477a4d19" src="https://github.com/user-attachments/assets/06e2c647-b1c6-44e0-8fbc-11f6f984f302" />

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
<img width="833" height="236" alt="437515376-352b921d-9e6f-491c-a625-08f4181bad6d" src="https://github.com/user-attachments/assets/89387f3a-4d76-4585-ad05-e194e0c4676b" />

 
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
<img width="825" height="79" alt="437515645-c103e0a5-3476-4c84-8cbd-f17b9bae9e2d" src="https://github.com/user-attachments/assets/873aebd0-9ef3-4aaf-855e-c8837e75c8d5" />

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
 <img width="837" height="113" alt="437515806-cf727495-c935-4877-b8c3-27a2f53f51c9" src="https://github.com/user-attachments/assets/4bec7bb1-cd65-4d0b-a764-c851af49dcb8" />

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

<img width="799" height="57" alt="437516678-2abd07e2-1944-4c70-a029-cd41d7f60800" src="https://github.com/user-attachments/assets/3b46e067-f721-44e1-bb56-966ca06d33d4" />

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
<img width="808" height="57" alt="437516575-fad684d9-006c-4bd7-bab5-50c8169f716b" src="https://github.com/user-attachments/assets/4717e063-1d3a-450f-a8fc-0e8d47070b9d" />



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
 <img width="869" height="72" alt="437516896-aae1f16d-9ff5-4d5b-8768-27f634a70e1f" src="https://github.com/user-attachments/assets/f0176bb8-4b4d-4dce-94cb-f84ba9dabe9c" />

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
 <img width="895" height="255" alt="437517140-01d807d9-9604-47db-80e4-04d90919cbe0" src="https://github.com/user-attachments/assets/6dbbfb0d-3516-4ccd-a1d5-0be69489e9c4" />

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

<img width="839" height="72" alt="437517320-ee6e9199-b040-49fd-90ee-f769859de031" src="https://github.com/user-attachments/assets/4ac66649-c92e-48b6-8c6d-92e1a161c75d" />

# RESULT:
The Commands are executed successfully.
