- vigenère cipher is a polyalphabetic substitution cipher that encrypts text using a keyword. Each letter of the plaintext is shifted based on the corresponding letter in the keyword
- first we repeat the keyword till matches the length of plaintext
- then we use the formula  Ei = (Pi + Ki) mod 26. here Ei is the encrypted character, Pi is the plaintext character, and Ki is the key character
- then convert the resulting numbers back to letters to form the ciphertext

- code for generating ciphertext
```
def generate_key(plaintext, keyword):
   key = list(keyword)
   while len(key) < len(plaintext):
       key.append(keyword[len(key) % len(keyword)])
   return ''.join(key)
def vigenere_encrypt(plaintext, key):
   ciphertext = []
   for p, k in zip(plaintext, key):
       encrypted_char = chr(((ord(p) - ord('A') + ord(k) - ord('A')) % 26) + ord('A'))
       ciphertext.append(encrypted_char)
   return ''.join(ciphertext)
# Example Usage
plaintext = "GEEKSFORGEEKS"
keyword = "AYUSH"
# Ensure uppercase for consistency
plaintext = plaintext.upper()
keyword = keyword.upper()
key = generate_key(plaintext, keyword)
```
- code for decryption
```
def vigenere_decrypt(ciphertext, key):
    decrypted = []
    key = key.upper()
    key_length = len(key)
    key_index = 0

    for char in ciphertext:
        if char.isalpha():
            offset = ord('A') if char.isupper() else ord('a')
            key_char = key[key_index % key_length]
            key_shift = ord(key_char) - ord('A')
            decrypted_char = chr((ord(char) - offset - key_shift) % 26 + offset)
            decrypted.append(decrypted_char)
            key_index += 1
        else:
            decrypted.append(char)  # Non-alphabetic characters are unchanged

    return ''.join(decrypted)

# Example usage
ciphertext = "GCYCZFMLYLEIM"
key = "AYUSH"
plaintext = vigenere_decrypt(ciphertext, key)
print("Decrypted text:", plaintext)
```
ciphertext = vigenere_encrypt(plaintext, key)
print("Ciphertext:", ciphertext)
