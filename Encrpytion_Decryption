def caeser(text, n):
    word=''
    for i in text:
        if i.isdigit():
            new_i = chr(((ord(i) - ord('0')) + n) % 10 + ord('0'))

        elif i.islower():
            new_i = chr((ord(i) - ord('a') + n) % 26 + ord('a'))

        elif i.isupper():
            new_i = chr((ord(i) - ord('A') + n) % 26 + ord('A'))

        else:
            new_i=i
        word+=new_i

    return word

plain_text=input("Enter your plain text:")
n=len(plain_text)
key=int(input("Enter your shift value(key):"))

#ENCRYPTION
caeser_text=caeser(plain_text,key)
print("message after encryption:",caeser_text)
print("Encryption Done..")

#DECRYPTION
decrypted_text=caeser(caeser_text,-key)
print("message after decryption:",decrypted_text)
