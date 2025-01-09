# Simple Image Encryption Tool

This repository contains a basic Python tool for encrypting and decrypting images using simple pixel manipulation techniques. The tool uses the Python Imaging Library (PIL) and NumPy to apply basic mathematical operations to each pixel for encryption and decryption.

## Features

- **Image Encryption**: Encrypts an image by applying a simple mathematical transformation to each pixel using a user-defined key.
- **Image Decryption**: Reverses the encryption process to restore the original image using the same key.
- **Supports Multiple Image Formats**: Can handle various image formats supported by PIL, such as JPEG, PNG, BMP, etc.
  
## How It Works

- The image is loaded and converted into a NumPy array of pixel values.
- For encryption, each pixel value is modified using the formula `(pixel_value + key) % 256`.
- For decryption, the inverse operation `(pixel_value - key) % 256` is applied to restore the original pixel values.
- The encrypted and decrypted images are then saved and can be displayed for verification.

## Usage

1. Clone the repository.
2. Install the required dependencies:
   ```bash
   pip install Pillow numpy
   ```
3. Run the script with your image and desired key:
   ```python
   key = 50
   original_image_path = 'path_to_your_image.jpg'
   encrypted_image = encrypt_image(original_image_path, key)
   encrypted_image.save('encrypted_image.png')

   decrypted_image = decrypt_image(encrypted_image, key)
   decrypted_image.save('decrypted_image.png')
   ```
