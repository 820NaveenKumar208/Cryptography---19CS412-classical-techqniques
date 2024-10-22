# DEVELOP BY : NAVEEN KUMAR T
# REQ NO: 212223220067

# Cryptography---19CS412-classicaltechqniques
# Caeser CipherCaeser
Cipher using with different key values
## AIM:
To encrypt and decrypt the given message by using Ceaser Cipher encryption algorithm
## DESIGN STEPS:
### step :
Design of Caeser CipherCaeser algorithnm.
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
#include <string.h>
#include <ctype.h>
int main() {
char plain[100], cipher[100];
int key, i, length;
printf("\nEnter the plain text: ");
scanf("%s", plain);
printf("Enter the key value: ");
scanf("%d", &key);
length = strlen(plain);
printf("\nPLAIN TEXT: %s", plain);
printf("\nENCRYPTED TEXT: ");
for (i = 0; i < length; i++) {
if (isalpha(plain[i])) {
if (isupper(plain[i])) {
cipher[i] = ((plain[i] - 'A' + key) % 26) + 'A';
} else {
cipher[i] = ((plain[i] - 'a' + key) % 26) + 'a';
}
} else {
cipher[i] = plain[i];
}
printf("%c", cipher[i]);
}
cipher[length] = '\0';
printf("\nDECRYPTED TEXT: ");
for (i = 0; i < length; i++) {
if (isalpha(cipher[i])) {
if (isupper(cipher[i])) {
plain[i] = ((cipher[i] - 'A' - key + 26) % 26) + 'A';
} else {
plain[i] = ((cipher[i] - 'a' - key + 26) % 26) + 'a';
}
} else {
plain[i] = cipher[i];
}
printf("%c", plain[i]);
}
plain[length] = '\0';
return 0;
}


```
## Output:
![Screenshot 2024-10-22 050751](https://github.com/user-attachments/assets/6becdc43-d820-4fdc-8c5b-8ff758fa6983)




