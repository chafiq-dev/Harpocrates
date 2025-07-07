# Harpocrates 🤫

**Encrypt and securely hide files inside images, right in your browser.**

Harpocrates is a client-side web application that uses modern cryptography and steganography to conceal a file within a standard image. Your data is encrypted with a password and never leaves your machine, providing a powerful tool for privacy and data concealment.

-----

## ✨ Key Features

  * **Entirely In-Browser**: No files are ever uploaded to a server. All encoding and decoding operations happen locally on your computer.
  * **Robust Encryption**: Your secret file is secured with **AES-256-GCM**, an authenticated encryption algorithm that ensures both confidentiality and integrity.
  * **Strong Password Protection**: The encryption key is derived from your password using **PBKDF2** with **100,000 iterations** and a **SHA-256** hash, making it highly resistant to brute-force attacks.
  * **Modern & Responsive UI**: A clean, Material You-inspired interface with automatic light and dark theme support for a great user experience.
  * **No Special Software Needed**: All you need is a modern web browser.

-----

## 🚀 How to Use

Using Harpocrates is simple. The interface is divided into two main modes: Encode and Decode.

### To Hide a File (Encode)

1.  Make sure you are on the **Encode** tab.
2.  In the "Carrier Image" section, click to upload a PNG or JPG image that will be used to hide your file.
3.  In the "Secret File" section, click to upload the file you wish to hide.
4.  Under "Set a Password", enter and confirm a strong password for encryption.
5.  Click the **Encrypt & Hide File** button.
6.  A success message will appear. Click the **Download** button to save your new image, which now secretly contains your file.

### To Reveal a File (Decode)

1.  Switch to the **Decode** tab.
2.  Click to upload the steganographic image (the image containing the hidden file).
3.  Enter the password that was used to hide the file.
4.  Click the **Decrypt & Reveal File** button.
5.  If the password is correct, a success message will appear, and you can download the original, revealed file.

-----

## ⚙️ The Technical Details

Harpocrates ensures security by combining steganography with strong, modern cryptography.

1.  **Payload Preparation**: When you encode a file, the application first creates a payload containing the secret file's name and its raw data.
2.  **Encryption**: This entire payload is then encrypted using **AES-256-GCM** with a key derived from your password and a random 16-byte salt. Using a new salt for each encryption prevents rainbow table attacks.
3.  **Embedding**: The application uses a unique 14-byte "magic delimiter" (`ENCRYPTEDSTEGO`) to mark where the original image data ends and the hidden data begins. The final file is constructed as: `[Original Image Bytes] + [Magic Delimiter] + [Encrypted Payload]`.
4.  **Decryption**: During decoding, the application first looks for this magic delimiter. If found, it takes the subsequent data, attempts to decrypt it with the provided password, and if successful, reconstructs the original file. An incorrect password will cause the decryption to fail, preventing access to the data.

-----

## 💖 Support This Project

If you find Harpocrates useful and appreciate the work, please consider supporting its development. Donations are greatly appreciated\!

**TON Wallet Address:**

```
UQAbjx-d8UQ_FxEgONFB3Y412f4fW7e-zOdBXmMSs59pkYog
```

Thank you\!
