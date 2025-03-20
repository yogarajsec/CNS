## EX. NO: 1(A) : IMPLEMENTATION OF CAESAR CIPHER
 ## Name: Yogaraj.S
 ## Reg no:212223040248

## AIM:

To implement the simple substitution technique named Caesar cipher using C language.

## DESCRIPTION:

To encrypt a message with a Caesar cipher, each letter in the message is changed using a simple rule: shift by three. Each letter is replaced by the letter three letters ahead in the alphabet. A becomes D, B becomes E, and so on. For the last letters, we can think of the
alphabet as a circle and "wrap around". W becomes Z, X becomes A, Y bec mes B, and Z
becomes C. To change a message back, each letter is replaced by the one three before it.

## EXAMPLE:



![image](https://github.com/Hemamanigandan/CNS/assets/149653568/eb9c6c43-8c80-4cdd-b9d4-91705a311c79)


## ALGORITHM:

### STEP-1: Read the plain text from the user.
### STEP-2: Read the key value from the user.
### STEP-3: If the key is positive then encrypt the text by adding the key with each character in the plain text.
### STEP-4: Else subtract the key from the plain text.
### STEP-5: Display the cipher text obtained above.


## PROGRAM :-
```
def caesar_cipher(text, shift, encrypt=True):
    result = ""
    
    for char in text:
        if char.isalpha():  
            shift_amount = shift if encrypt else -shift
            start = ord('A') if char.isupper() else ord('a')
            result += chr((ord(char) - start + shift_amount) % 26 + start)
        else:
            result += char 
    
    return result

message = input("Enter the name : ")
shift_value = int(input("Enter the key word : "))


encrypted_text = caesar_cipher(message, shift_value)
print("Encrypted:", encrypted_text)


decrypted_text = caesar_cipher(encrypted_text, shift_value, encrypt=False)
print("Decrypted:", decrypted_text)
```


## OUTPUT :-
![Screenshot 2025-03-20 085631](https://github.com/user-attachments/assets/73c39cc5-8724-45b7-91bd-09ad4467b5b3)

## Result:
The program is executed successfully
