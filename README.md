# Caesar Cipher Encryption & Manual Hashing Program

## What is caesar cipher?

One of the simplest and oldest encryption technique

Encryption: shifts each character of the message or the text by fixed no of character (key)  
Decryption: shifts each character of the message or the text by the same fixed no of character but in the opposite direction (negative of the key)

## Polynomial Rolling Hash Function

Converts the given input to a fixed length hash string

Base p = 31  
Large modulus m = 2^61 - 1 (a prime number)

### How it works:

- Each character is converted to its ASCII value  
- Multiplied by increasing powers of p  
- The sum is taken modulo m to avoid overflow  
- Result is converted into a base-62 string  
- Output is padded or trimmed to a fixed length (default = 12)

## Instruction to Run the file
- Start the program 
- Give plain text as input
- Give the number of characters to shift (key value)

## Flow of the Program
### Encryption
- Input: Plain text and the key are given as input  
- Encryption: Iterate through the plain text, and shift each character according to the given key 
- Hashing: Hash the encrypted ceasar text, get hash value
- Appending: Concatenate the encrypted text and the hash value

### Decryption
- Extraction: Separate the encrypted text and hash value
- Decrypting: Apply ceasar cipher with negative shift for decryption
- Integrity check: Apply hash function on the retrieved text and compare it with the retrieved hash


## Use of LLM in this

1) Analysis of the existing options of hash function available
   - Consideration of using an existing hash functions
   - Looking on the possibilities of using SHA-256 as secure hash function  
   - Skipped due to complex steps of manual implementation  

2) Generation of the custom hash function  
   Polynomial rolling hash function
