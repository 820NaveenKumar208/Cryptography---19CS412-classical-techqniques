# DEVELOP BY : NAVEEN KUMAR T
# REQ NO: 212223220067

# Cryptography---19CS412-classicaltechqniques
# Rail Fence Cipher
Rail Fence Cipher using with different key values
Playfair Cipher using with different key values
## AIM:
To develop a simple C program to implement Rail Fence Cipher.
## DESIGN STEPS:
### step :
Design of Rail Fence Cipher algorithnm.
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

#include<stdio.h>
#include<string.h>
int main() { int i, j, k, l; char a[20], c[20], d[20];
printf("\n\t\t RAIL FENCE TECHNIQUE");
printf("\n\nEnter the input string : ");
scanf("%[^\n]%*c", a);
l = strlen(a);
/* Ciphering */
for(i = 0, j = 0; i < l; i++) {
if(i % 2 == 0)
c[j++] = a[i];
}
for(i = 0; i < l; i++) {
if(i % 2 == 1)
c[j++] = a[i];
}
c[j] = '\0';
printf("\nCipher text after applying rail fence :");
printf("\n%s", c);
/* Deciphering */
if(l % 2 == 0)
k = l / 2;
else
k = (l / 2) + 1;
for(i = 0, j = 0; i < k; i++) {
d[j] = c[i];
j = j + 2;
}
for(i = k, j = 1; i < l; i++) {
d[j] = c[i];
j = j + 2;
}
d[l] = '\0';
printf("\nText after decryption : ");
printf("%s", d);
return 0;
}
```
# Output:
![Screenshot 2024-10-24 040038](https://github.com/user-attachments/assets/ef825657-82cb-4a79-8d19-e375876f4720)







