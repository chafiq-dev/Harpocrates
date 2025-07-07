Of course, here's a readme.md for your project.

# Harpocrates: Encrypt and Hide Files in Images 🤫

[](https://shields.io/)
[](https://shields.io/)

[cite\_start]Harpocrates is a web-based tool that allows you to encrypt and hide files within images directly in your browser. [cite: 34] [cite\_start]It offers a seamless and secure way to conceal your data, ensuring that only those with the correct password can access the hidden file. [cite: 62]

## ✨ Features

  * **In-Browser Encryption and Decryption** All operations are performed locally in your browser, ensuring that your files are never uploaded to a server.
  * [cite\_start]**Secure Encryption** Files are encrypted using the robust **AES-256-GCM** algorithm. [cite: 108, 111, 115]
  * [cite\_start]**Password-Based Key Derivation** The encryption key is derived from your password using **PBKDF2** with **100,000 iterations** and a **SHA-256** hash function, making it resistant to brute-force attacks. [cite: 108]
  * [cite\_start]**User-Friendly Interface** The application features a modern and intuitive interface with both light and dark modes available. [cite: 81, 83]

-----

## 🚀 How It Works

Harpocrates simplifies the process of steganography (the practice of concealing a file, message, image, or video within another file, message, image, or video) into two main functions: encoding and decoding.

### Encoding

1.  [cite\_start]**Carrier Image Selection** [cite: 37] [cite\_start]You start by selecting a carrier image (either a PNG or JPG file). [cite: 39] This is the image that will be used to hide your secret file.
2.  [cite\_start]**Secret File Selection** [cite: 43] Next, you choose the file you want to hide. [cite\_start]This can be any type of file. [cite: 45]
3.  [cite\_start]**Password Creation** [cite: 49] [cite\_start]You then set a password to encrypt your secret file. [cite: 50]
4.  [cite\_start]**Encryption and Hiding** When you click the "Encrypt & Hide File" button, [cite: 53] the tool encrypts your secret file and its name using AES-256-GCM. [cite\_start]The encrypted data is then appended to the carrier image, creating a new steganographic image. [cite: 126]

### Decoding

1.  [cite\_start]**Image Selection** [cite: 56] [cite\_start]You select the image that contains the hidden file. [cite: 59]
2.  [cite\_start]**Password Entry** [cite: 62] [cite\_start]You enter the same password that was used to encrypt the file. [cite: 63]
3.  [cite\_start]**Decryption and Extraction** The tool then searches for a unique delimiter within the image file to locate the hidden data. [cite: 128] [cite\_start]If the delimiter is found, it decrypts the data using your password and allows you to download the original secret file. [cite: 133]

-----

## 🛠️ Technology Stack

  * [cite\_start]**Frontend**: HTML[cite: 1], Tailwind CSS, JavaScript
  * [cite\_start]**Cryptography**: The application utilizes the Web Crypto API for all cryptographic operations. [cite: 107]

-----

## 💖 Support Me

If you find this project useful and would like to show your support, you can send a donation to my TON wallet. Your contribution will help me to continue developing and maintaining this and other open-source projects.

**TON Wallet Address**: `UQAbjx-d8UQ_FxEgONFB3Y412f4fW7e-zOdBXmMSs59pkYog`

Thank you for your support\!
