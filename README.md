# DEVELOP BY : NAVEEN KUMAR T
# REQ NO: 212223220067

# Cryptography---19CS412-classicaltechqniques
# Vigenere Cipher
## AIM:
Vigenere Cipher using with different key values
## DESIGN STEPS:
### step :
Design of Hill Cipher algorithnm.
### Step:
Implementation using C or pyhton code.
### Step:
Testing algorithm with different key values. ALGORITHM DESCRIPTION: The Hill cipher
is a substitution cipher invented by Lester S. Hill in 1929. Each letter is represented by
a number modulo 26. To encrypt a message, each block of n letters is multiplied by
an invertible n × n matrix, again modulus 26. To decrypt the message, each block is
multiplied by the inverse of the matrix used for encryption. The matrix used for
encryption is the cipher key, and it should be chosen randomly from the set of
invertible n × n matrices (modulo 26). The cipher can, be adapted to an alphabet with
any number of letters. All arithmetic just needs to be done modulo the number of
letters instead of modulo 26.
## PROGRAM:
```
#include <stdio.h>
#include <ctype.h>
#include <string.h>
#include<stdlib.h>
void encipher();
void decipher();
void main()
{
int choice;
while(1)
{
printf("\n1. Encrypt Text");
printf("\t2. Decrypt Text");
printf("\t3. Exit");
printf("\n\nEnter Your Choice : ");
scanf("%d",&choice);
if(choice == 3)
break;
else if(choice == 1)
encipher();
else if(choice == 2)
decipher();
else
printf("Please Enter Valid Option.");
}
}
void encipher()
{
unsigned int i,j;
char input[50],key[10];
printf("\n\nEnter Plain Text: ");
scanf("%s",input);
printf("\nEnter Key Value: ");
scanf("%s",key);
printf("\nResultant Cipher Text: ");
for(i=0,j=0;i<strlen(input);i++,j++)
{
if(j>=strlen(key))
{ j=0;
}
printf("%c",65+(((toupper(input[i])-65)+(toupper(key[j])-
65))%26));
}}
void decipher()
{
unsigned int i,j;
char input[50],key[10];
int value;
printf("\n\nEnter Cipher Text: ");
scanf("%s",input);
printf("\n\nEnter the key value: ");
scanf("%s",key);
for(i=0,j=0;i<strlen(input);i++,j++)
{
if(j>=strlen(key))
{ j=0; }
value = (toupper(input[i])-64)-(toupper(key[j])-64);
if( value < 0)
{ value = value * -1;
}
printf("%c",65 + (value % 26));
}
}
```
## Output:
![Screenshot 2024-10-22 044653](https://github.com/user-attachments/assets/25249a1c-982f-42ab-aa28-4955243d1501)






