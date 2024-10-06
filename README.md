**Tugas 1 - Keamanan Informasi B - Algoritma DES**

Johannes Daniswara Pratama
5025221276

**Example Use**
```python

DES = Des()
random_key = DES.Random_Bytes(8) # generate random 64 bits or 8 bytes

cipher_text1 = DES.Encrypt(b"HaloHalo", random_key)   # input: "HaloHalo" in bytes format
print("\nkey bytes: ", random_key)
print("key hex", random_key.hex())

print("\ncipher byte: ", cipher_text1)      # output: encrypted text in bytes
print("cipher hex: ", cipher_text1.hex())   # output: encrypted text in hex

print("decrypted: ", DES.Decrypt(cipher_text = cipher_text1))                             # output: HaloHalo (self stored key)
print("decrypted2: ", DES.Decrypt_using_key(cipher_text = cipher_text1, key=random_key))  # output: HaloHalo  (supplied key)

cipher_text2 = DES.Encrypt(b"Informatika", random_key)     # input: "Informatika" in bytes format
print("cipher byte:", cipher_text2)                        # output: encrypted text in bytes / hdex
print("cipher hex: ", cipher_text2.hex())                  # output: encrypted text in hex

print("encrypted: ", DES.Decrypt(cipher_text = cipher_text2))
# output: 'Informatika\x00\x00\x00\x00\x00' (padding \x00 )
# output with padding \x00 because input is not multiple of 8 bytes or 64bits
```
