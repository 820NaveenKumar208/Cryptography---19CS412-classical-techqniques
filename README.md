# Cryptography---19CS412-classical-techqniques


# Caeser Cipher
Caeser Cipher using with different key values

# AIM:

To develop a simple C program to implement Caeser Cipher.

## DESIGN STEPS:

### Step 1:

Design of Caeser Cipher algorithnm 

### Step 2:

Implementation using C or pyhton code

### Step 3:

Testing algorithm with different key values. 

## PROGRAM:
~~~
#include <stdio.h>
#include <string.h>
#include <conio.h>
#include <ctype.h>

int main() {
    char plain[10], cipher[10];
    int key, i, length;
    int result;

    printf("\n Enter the plain text:");
    scanf("%s", plain);

    printf("\n Enter the key value:");
    scanf("%d", &key);

    printf("\n \n \t PLAIN TEXT: %s", plain);
    printf("\n \n \t ENCRYPTED TEXT: ");

    for (i = 0, length = strlen(plain); i < length; i++) {
        cipher[i] = plain[i] + key;

        if (isupper(plain[i]) && (cipher[i] > 'Z'))
            cipher[i] = cipher[i] - 26;

        if (islower(plain[i]) && (cipher[i] > 'z'))
            cipher[i] = cipher[i] - 26;

        printf("%c", cipher[i]);
    }

    printf("\n \n \t AFTER DECRYPTION : ");

    for (i = 0; i < length; i++) {
        plain[i] = cipher[i] - key;

        if (isupper(cipher[i]) && (plain[i] < 'A'))
            plain[i] = plain[i] + 26;

        if (islower(cipher[i]) && (plain[i] < 'a'))
            plain[i] = plain[i] + 26;

        printf("%c", plain[i]);
    }

    return 0;
}
~~~

## OUTPUT:
![WhatsApp Image 2024-02-29 at 14 04 00_9246ee39](https://github.com/SAKTHIPRIYASATHISH/Cryptography---19CS412-classical-techqniques/assets/119104282/fd3147e8-af74-4e3b-9489-426e62c67459)


## RESULT:
The program is executed successfully

---------------------------------

# PlayFair Cipher
Playfair Cipher using with different key values

# AIM:

To develop a simple C program to implement PlayFair Cipher.

## DESIGN STEPS:

### Step 1:

Design of PlayFair Cipher algorithnm 

### Step 2:

Implementation using C or pyhton code

### Step 3:

Testing algorithm with different key values. 

## PROGRAM:

## OUTPUT:

## RESULT:
The program is executed successfully


---------------------------

# Hill Cipher
Hill Cipher using with different key values

# AIM:

To develop a simple C program to implement Hill Cipher.

## DESIGN STEPS:

### Step 1:

Design of Hill Cipher algorithnm 

### Step 2:

Implementation using C or pyhton code

### Step 3:

Testing algorithm with different key values. 

## PROGRAM:

## OUTPUT:

## RESULT:
The program is executed successfully

-------------------------------------------------

# Vigenere Cipher
Vigenere Cipher using with different key values

# AIM:

To develop a simple C program to implement Vigenere Cipher.

## DESIGN STEPS:

### Step 1:

Design of Vigenere Cipher algorithnm 

### Step 2:

Implementation using C or pyhton code

### Step 3:

Testing algorithm with different key values. 

## PROGRAM:

## OUTPUT:

## RESULT:
The program is executed successfully

-----------------------------------------------------------------------

# Rail Fence Cipher
Rail Fence Cipher using with different key values

# AIM:

To develop a simple C program to implement Rail Fence Cipher.

## DESIGN STEPS:

### Step 1:

Design of Rail Fence Cipher algorithnm 

### Step 2:

Implementation using C or pyhton code

### Step 3:

Testing algorithm with different key values. 

## PROGRAM:

## OUTPUT:

## RESULT:
The program is executed successfully
