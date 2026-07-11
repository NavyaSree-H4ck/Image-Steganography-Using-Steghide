# Image Steganography Using Steghide in Kali Linux

> A practical implementation of image steganography using Steghide with metadata and cryptographic hash analysis before and after data embedding.


## 📖 Overview

This project demonstrates how to securely hide a secret message inside a JPEG image using **Steghide** in Kali Linux. The practical includes metadata analysis, MD5 and SHA-256 hash comparison, secret message embedding, and extraction to verify the steganography process.


## 🎯 Objectives

- Perform image steganography using Steghide.
- Analyze image metadata before and after embedding.
- Compare MD5 and SHA-256 hash values.
- Verify successful extraction of the hidden message.


## 🛠️ Tools Used

- Kali Linux
- Steghide
- ExifTool
- MD5
- SHA-256

## ⚙️ Project Workflow

1. Verify Steghide and ExifTool installation.
2. Create a working directory.
3. Select a JPEG image.
4. Analyze image metadata.
5. Generate MD5 and SHA-256 hashes.
6. Create a secret message.
7. Embed the secret message into the image.
8. Verify embedded information.
9. Extract the hidden message.
10. Compare metadata and hash values.


## 💻 Key Commands

```bash
steghide --version
exiftool -ver

mkdir Steganography
cd Steganography

file flower.jpg

exiftool flower.jpg

md5sum flower.jpg
sha256sum flower.jpg

nano secret.txt

steghide embed -cf flower.jpg -ef secret.txt

steghide info flower.jpg

steghide extract -sf flower.jpg

md5sum flower.jpg
sha256sum flower.jpg

exiftool flower.jpg
```


## 📊 Metadata Analysis

- JPEG image format remained unchanged.
- Image resolution remained the same.
- File size increased after embedding.
- Modification timestamp changed.
- Other image properties remained unchanged.


## 🔐 Hash Analysis

- MD5 hash value changed after embedding.
- SHA-256 hash value changed after embedding.
- The changed hash values confirm that the image's binary content was modified while maintaining its visual appearance.


## 📈 Results

- Successfully embedded a secret message into the image.
- Successfully extracted the hidden message.
- Image appearance remained unchanged.
- Metadata showed only minor modifications.
- MD5 and SHA-256 hash values changed after embedding.


## 📚 Learning Outcomes

- Understood image steganography.
- Learned to use Steghide and ExifTool.
- Performed metadata analysis.
- Verified file integrity using cryptographic hashes.
- Gained practical experience with secure data hiding.


## 📄 Documentation

The complete practical report, including **step-by-step procedures, command explanations, screenshots, observations, metadata analysis, and hash comparison**, is available in the attached PDF document.


## 📂 Repository Structure

```
Image-Steganography-Using-Steghide/
│
├── README.md
├── Image-Steganography-Using-Steghide.pdf
└── flower.jpg (optional)
```


## ✅ Conclusion

This project successfully demonstrated image steganography using Steghide in Kali Linux. Metadata and cryptographic hash analysis confirmed that the image's binary data changed after embedding while its visual appearance remained unchanged. The successful extraction of the hidden message verified the effectiveness of the steganography process.


## 📖 References

- Kali Linux Documentation
- Steghide Documentation
- ExifTool Documentation
- ImageMagick Documentation


## 👩‍💻 Author

**Navya Sree**

Cybersecurity Student | SOC Analyst Aspirant | Cybersecurity Enthusiast
