# EX. NO: 1(A) : IMPLEMENTATION OF CAESAR CIPHER

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
int main() {
    char plainText[100];
    char cipherText[100];
    char decryptedText[100];
    int key;
    printf("Enter the plain text:");
    fgets(plainText, sizeof(plainText), stdin);
    size_t len = strlen(plainText);
    if (len > 0 && plainText[len - 1] == '\n') {
        plainText[len - 1] = '\0';
    }
    printf("Enter the key value:");
    scanf("%d", &key);
    strcpy(cipherText, plainText);
    strcpy(decryptedText, plainText);
    for (int i = 0; cipherText[i] != '\0'; i++) {
        if (key > 0) {
            cipherText[i] = cipherText[i] + key; 
        } else {
            cipherText[i] = cipherText[i] - key; 
        }
    }
    for (int i = 0; decryptedText[i] != '\0'; i++) {
        if (key > 0) {
            decryptedText[i] = decryptedText[i];
        } 
    }
    for (int i = 0; cipherText[i] != '\0'; i++) {
        if (key > 0) {
            decryptedText[i] = cipherText[i] - key;
        } else {
            decryptedText[i] = cipherText[i] + key;
        }
    }
    printf("\nPLAIN TEXT: %s\n", plainText);
    printf("ENCRYPTED TEXT:%s\n", cipherText);
    printf("AFTER DECRYPTION : %s\n", decryptedText);

    return 0;
}
```
## OUTPUT:
<img width="627" height="317" alt="image" src="https://github.com/user-attachments/assets/c751c034-996d-4f5c-9645-f5877088baa5" />

## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
