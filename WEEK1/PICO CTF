# 1. MOD 26 
Cryptography can be easy, do you know what ROT13 is? cvpbPGS{arkg_gvzr_V'yy_gel_2_ebhaqf_bs_ebg13_Ncualgvd}

## SOLUTION 
- i first put the given ciphertext into a cipher indetifier https://www.dcode.fr/cipher-identifier to confirm if its ROT 13
- once confirmed i used https://www.dcode.fr/rot-13-cipher to decode and obtain the flag

## FLAG
picoCTF{next_time_I'll_try_2_rounds_of_rot13_Aphnytiq}

## CONCEPTS LEARNED 
- ROT13 is a simple letter substitution cipher that replaces a letter with the 13th letter after it in the Latin alphabet.
- we could use python to solve if needed 

```
def gen_rot13_table(f):
    a = 'ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz'
    b = 'NOPQRSTUVWXYZABCDEFGHIJKLMnopqrstuvwxyzabcdefghijklm'
    return zip(map(f, a), map(f, b))

# Create the translation table
x, y = zip(*gen_rot13_table(ord))
table = str.maketrans(dict(zip(x, y)))

# Encrypted string
s = "cvpbPGS{arkg_gvzr_V'yy_gel_2_ebhaqf_bs_ebg13_Ncualgvd}"

# Decode using ROT13
decoded = s.translate(table)
print(decoded)
```
# 2. 13
Cryptography can be easy, do you know what ROT13 is? cvpbPGS{abg_gbb_onq_bs_n_ceboyrz}

## SOLUTION 
- i put it into the python code i generated earlier and obtained the flag

## FLAG 
picoCTF{not_too_bad_of_a_problem}

# 3. INTERENCDEC
Can you get the real meaning from this file.
Download the file here.

## SOLUTION
- i first put the given ciphertext to a cipher identifier to find its base64 so i got b'd3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrX20wMjEyNzU4fQ==' and since it still looked encryted 
- then i removed the b and ' ' cuz base64 doesnt have ' and usually the b in front refers to bytes
- so after decrypting using base64 i got wpjvJAM{jhlzhy_k3jy9wa3k_m0212758}, which looked closer to our flag
- then in tags i saw ceasar cipher so put it in a decrypter and obtained the flag

## FLAG
picoCTF{caesar_d3cr9pt3d_f0212758}

## CONCEPTS LEARNED
- base64 is a binary-to-text encoding that uses 64 printable characters to represent each 6-bit segment of a sequence of byte
- base64 doesnt use ' and how b in front usually refers to bytes
- caesar cipher is a type of substitution cipher, where each letter in the plaintext is replaced by another letter a fixed number of positions down the alphabet. This fixed number is called the shift or key. usually 3
- python code for base64 

```
import base64

# Your original Base64 string
encoded = "YidkM0JxZGtwQlRYdHFhR3g2YUhsZmF6TnFlVGwzWVROclgyMHdNakV5TnpVNGZRPT0nCg"

# Fix padding if needed
missing_padding = len(encoded) % 4
if missing_padding:
    encoded += '=' * (4 - missing_padding)

# Decode safely
decoded_bytes = base64.b64decode(encoded)
decoded_string = decoded_bytes.decode('utf-8')

print("Decoded string:", decoded_string)

```

- python code for ceasar cipher

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
ciphertext = "wpjvJAM{jhlzhy_k3jy9wa3k_m0212758}"

# Run brute-force
caesar_brute_force(ciphertext)
```
- this gives you all possible forms of answers and we get this in shift 7
