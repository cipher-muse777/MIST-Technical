- base64 is a binary-to-text encoding that uses 64 printable characters to represent each 6-bit segment of a sequence of byte
- base64 encoding increases the size by 33% plus about 4% additional if inserting line breaks for typical line length
- it often used to embed binary data such as a digital image in text such as HTML and CSS
- the general strategy is to use printable characters that are common to most character encodings
- there are various varients
   - **Standard(RFC 4648)**
       - it uses + and /
       - no line breaks
       - padding is optional
   - **MIME (RFC 2045)**
       - same as standard
       - line breaks every 76 chars 
       - padding is required
   - **URL-safe (RFC 4648)**
       - it replaces the + in std with - and / with _
       - there are no line breaks 

python code
```
import base64

# Your original Base64 string
encoded = "ciphertext"

# Fix padding if needed
missing_padding = len(encoded) % 4
if missing_padding:
    encoded += '=' * (4 - missing_padding)

# Decode safely
decoded_bytes = base64.b64decode(encoded)
decoded_string = decoded_bytes.decode('utf-8')

print("Decoded string:", decoded_string)
```
