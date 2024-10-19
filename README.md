**Tugas 1 - Keamanan Informasi B - Algoritma DES**

Johannes Daniswara Pratama
5025221276

**Example Use**
```python

DES = Des()
# Key must be 8 bytes or 16 bytes or 24 bytes (Triple DES Supported)
random_key = DES.Random_Bytes(8)

cipher_text1 = DES.Encrypt(b"HaloHalo", random_key)   # input: "HaloHalo" in bytes format
print("\nkey bytes: ", random_key)
print("key hex", random_key.hex())

print("\ncipher byte: ", cipher_text1)      # output: encrypted text in bytes
print("cipher hex: ", cipher_text1.hex())   # output: encrypted text in hex

print("decrypted: ", DES.Decrypt(cipher_text = cipher_text1))                             # output: HaloHalo (self stored key)
print("decrypted2: ", DES.Decrypt_using_key(cipher_text = cipher_text1, key=random_key))  # output: HaloHalo  (supplied key)

cipher_text2 = DES.Encrypt(b"Informatika", random_key)     # input: "Informatika" in bytes format
print("cipher byte:", cipher_text2)                        # output: encrypted text in bytes
print("cipher hex: ", cipher_text2.hex())                  # output: encrypted text in hex

print("decrypted: ", DES.Decrypt(cipher_text = cipher_text2))
# output: 'Informatika' (It has padding \x00 because it is not multiple of 8 bytes, But the padding will be automatically removed )
```
