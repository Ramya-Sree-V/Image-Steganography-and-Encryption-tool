# Steganography and Encryption Tool

This project is a Python-based steganography tool with encryption capabilities, designed to hide text messages within an image and encrypt the image to secure the hidden message. Built with a graphical user interface (GUI) using Tkinter and image handling via Pillow (PIL), the program enables users to encode, encrypt, decode, and decrypt messages hidden within images.

## Features
- **Steganography:** Hide a text message in an image using Least Significant Bit (LSB) steganography.
- **Encryption:** Encrypt the steganographed image using AES encryption with CFB mode to add a layer of security.
- **Decryption and Decoding:** Decrypt the image to reveal the hidden message.
- **User-Friendly GUI:** Built with Tkinter for easy navigation and interaction.

## Installation
**Install required dependencies:**
```bash
pip install pillow
```

## Program Structure
**GUI Layout**
The tool features an organized interface with five sections for:

- **Image Display** - Shows the selected image.
- **Message Box** - Input box for the text to hide or display extracted messages.
- **Image Controls** - Buttons to load and save images.
- **Steganography Controls** - Buttons to hide or reveal the message.
- **Encryption Controls** - Buttons to encrypt and decrypt the image.

## Core Functions
**Steganography Functions:**

- **encode_image():** Hides a message within an image using LSB steganography.
- **decode_image():** Extracts the hidden message from the image.

**Encryption Functions:**
- **encrypt_image():** Encrypts the image using AES in CFB mode.
- **decrypt_image():** Decrypts the image using AES in CFB mode.

**GUI-Related Functions:**
- **showimage():** Opens an image and displays it.
- **Hide():** Encodes a message into the image.
- **Show():** Decodes the message from the image.
- **HideAndEncrypt():** Hides and then encrypts the image with a random key and IV.
- **DecryptAndShow():** Decrypts and then displays the hidden message.

**Encryption Details:**
AES encryption is applied in Cipher Feedback (CFB) mode, where each image is padded to match the AES block size (128 bits). A random key and IV are generated for encryption, ensuring that even if the image is accessed, decryption requires the key and IV.

## Workflow

**Hide a Message:**
- Select an image, enter a message, and click Hide to save the steganographed image as hidden.png.

**Encrypt the Image:**
- Click Hide & Encrypt to save an encrypted version as encrypted_hidden.png.

**Decrypt and Show the Message:**
- Enter the key and IV, click Decrypt & Show to reveal the original message.
