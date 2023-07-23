<!-- PROJECT DESCRIPTION -->

# 📖 RSA CIPHER <a name="about-project"></a>

**RSA CIPHER** A minimal implemetation of asymetric encryption operations using [RSA](<https://en.wikipedia.org/wiki/RSA_(cryptosystem)>)

Functionalities include:

- File encryption and decryption
- File signature and verification

## Setup

### Prerequisites

In order to run this project you need to:

- Install [Python](https://www.python.org/)

### Install

Install the package via pip

```bash
pip install rsa_cipher
```

### Usage

**Encryption**

```python
from rsa_cipher import Encryption

# Create an object
encryptor = Encryption()

# Generate keys or load recivers public key using encryptor.load_keys(public_key_path='path_to_public_key.pem')
encryptor.generate_key_pair()

# You can export keys as .pem
encryptor.export_keys()

# Encrypt a file
encryptor.encrypt_file('path_to_file')

```

**Decryption**

```python
from rsa_cipher import Encryption

# Create an object
encryptor = Encryption()

# Load your private key
encryptor.load_keys(private_key_path='path_to_private_key.pem')

# Decrypt an encrypted file
encryptor.decrypt_file('path_to_encrypted_file')

```

**Signature**

```python
from rsa_cipher import Signature

# Create an object
signer = Signature()

# Generate keys or load your private key using encryptor.load_keys(private_key_path='path_to_private_key.pem')
encryptor.generate_key_pair()

# Sign a file
signer.sign('path_to_file')

```

**Signature Verfication**

```python
from rsa_cipher import Signature

# Create an object
signer = Signature()

# Generate keys or load your private key using encryptor.load_keys(private_key_path='path_to_private_key.pem')

# Load senders public key
encryptor.load_keys(public_key_path='path_to_public_key.pem')

# Verify the signature
signer.verify('path_to_file','path_to_signature')

```

<p align="right"><a href="#readme-top">👆</a></p>

<!-- AUTHORS -->

## 👥 Authors <a name="authors"></a>

👤 **Bahir Hakimi**

- <a href='https://www.linkedin.com/in/bahir-hakimi/' target="_blank"><img alt='LinkedIn' src='https://img.shields.io/badge/Bahir_Hakimi-100000?style=flat&logo=LinkedIn&logoColor=white&labelColor=0099FF&color=0099FF'/></a>
- <a href='mailto:bahirhakimy2020@gmail.com' target="_blank"><img alt='Gmail' src='https://img.shields.io/badge/Bahir_Hakimi-100000?style=flat&logo=Gmail&logoColor=FFFFFF&labelColor=FF2C10&color=FF2C10'/></a>
- <a href='https://twitter.com/bahir_hakimi_' target="_blank"><img alt='Twitter' src='https://img.shields.io/badge/Bahir_Hakimi-100000?style=flat&logo=Twitter&logoColor=FFFFFF&labelColor=0DE3FF&color=0DE3FF'/></a>

<p align="right"><a href="#readme-top">👆</a></p>

<!-- Contributing -->

## 🤝 Contributing <a name="contributing"></a>

Contributions, issues, and feature requests are welcome!

Feel free to check the [issues page](../../issues/).

<p align="right"><a href="#readme-top">👆</a></p>

<!-- Show your support -->

## ⭐️ Show your support <a name="support"></a>

If you like this project leave a start for it.

<p align="right"><a href="#readme-top">👆</a></p>

<!-- ACKNOWLEDGEMENTS -->

## 🙏 Acknowledgments <a name="acknowledgements"></a>

The package functionalities are based on [rsa](https://pypi.org/project/rsa/) by [sybrenstuvel](https://pypi.org/user/sybrenstuvel/).

<p align="right"><a href="#readme-top">👆</a></p>

<!-- LICENSE -->

## 📝 License <a name="license"></a>

This project is [MIT](./LICENSE) licensed.

<p align="right"><a href="#readme-top">👆</a></p>
