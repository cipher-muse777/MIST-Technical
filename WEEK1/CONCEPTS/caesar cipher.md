- caesar cipher is a type of substitution cipher(monoalphabetic), where each letter in the plaintext is replaced by another letter a fixed number of positions down the alphabet. This fixed number is called the shift or key. usually 3
- caesar cipher is a symmetric encryption technique, meaning that the same key is used for both encryption and decryption.


- python code
```
def caesar_brute_force(ciphertext):
    for shift in range(26):
        result = ""
        for char in ciphertext:
            if char.isalpha():
                base = ord('A') if char.isupper() else ord('a')
                shifted = (ord(char) - base - shift) % 26 + base
                result += chr(shifted)
            else:
                result += char
        print(f"Shift {shift}: {result}")

# Your encrypted string
ciphertext = "whatever"

# Run brute-force
caesar_brute_force(ciphertext)
```
