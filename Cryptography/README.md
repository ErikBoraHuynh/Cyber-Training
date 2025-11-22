## Cryptography Completion
<img width="1904" height="918" alt="Cryptography 1" src="https://github.com/user-attachments/assets/dd5cc51c-2f64-4841-947f-df36772b97eb" />
<img width="1171" height="567" alt="Cryptography 2" src="https://github.com/user-attachments/assets/510bedd6-44c3-4853-af8b-977c85f96f36" />
<img width="1911" height="398" alt="Cryptography 3" src="https://github.com/user-attachments/assets/6bd33d14-6a68-4eb8-a351-9a40a3017d15" />

## Cryptography Write-up
### XOR and What It Is

XOR (“exclusive OR”) is a basic mathematical/logical operation often used in simple encryption. It’s not secure by modern standards, but it’s great for learning how encryption and decryption work.

XOR works on bits (0s and 1s) and it outputs 1 only if the two bits are different.

The thing about XOR encryption is if you XOR the ciphertext with the same key you used to encrypt, you get the original message back.

Mathematically:

- plaintext XOR key = ciphertext
- ciphertext XOR key = plaintext

### Decrypting XOR
To decrypt an XOR-encrypted message, you need:
- The ciphertext (the scrambled message)
- The key (the secret number used to encrypt)

You can think of it like:
- Ciphertext is a list of numbers
- Key is a single number used repeatedly

Example With Actual Text:

Let’s say someone encrypted the message "Hi" using key 20.

Example Plaintext (ASCII codes):
- "H" = 72
- "i" = 105

Encrypt (just for context):
- Remember: plaintext XOR key = ciphertext
- 72 XOR 20 = 92
- 105 XOR 20 = 125

So the ciphertext is:
- 92 125

Now decrypt it:
- Remember: ciphertext XOR key = plaintext
- 92 XOR 20 = 72  → "H"
- 125 XOR 20 = 105 → "i"

You'll get "Hi" back.
  
