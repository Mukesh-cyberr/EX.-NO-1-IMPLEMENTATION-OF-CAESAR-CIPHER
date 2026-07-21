# EX. NO: 1(A) : IMPLEMENTATION OF CAESAR CIPHER
## NAME: MUKESH RAJ D
## REG NO: 212224100038

## AIM:
To implement the simple substitution technique named Caesar cipher using C language.

## ALOGORITHM:

STEP-1: Read the plain text from the user.

STEP-2: Read the key value from the user.

STEP-3: If the key is positive then encrypt the text by adding the key with each character in the plain text.

STEP-4: Else subtract the key from the plain text.

STEP-5: Display the cipher text obtained above.

## PROGRAM:
```
#include <stdio.h> 
#include <string.h> 
#include <ctype.h> 
int main() 
{ 
    char plain[10],cipher[10]; 
    int key,i,length; 
    int result; 
    printf(" Enter the plain text:"); 
    scanf("%s", plain); 
    printf(" Enter the key value:"); 
    scanf("%d", &key); 
    printf(" Plain Text: %s", plain); 
    printf("\n Encypted Text:"); 
    for(i=0, length = strlen(plain); i<length; i++) 
    { 
        cipher[i]=plain[i] + key; 
        if (isupper(plain[i]) && (cipher[i] > 'Z')) 
        cipher[i] = cipher[i] - 26; 
        if (islower(plain[i]) && (cipher[i] > 'z')) 
        cipher[i] = cipher[i] - 26; 
        printf("%c", cipher[i]); 
    } 
    printf("\n After Deryption: "); 
    for(i=0;i<length;i++) 
    { 
        plain[i]=cipher[i]-key; 
        if(isupper(cipher[i])&&(plain[i]<'A')) 
        plain[i]=plain[i]+26; 
        if(islower(cipher[i])&&(plain[i]<'a')) 
        plain[i]=plain[i]+26; 
        printf("%c",plain[i]); 
    } 
}
```

## OUTPUT:
<img width="1364" height="500" alt="image" src="https://github.com/user-attachments/assets/3703846d-cc66-463a-b710-5a0e366705e1" />

## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
