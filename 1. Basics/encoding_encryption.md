# Encoding, Encryption, and HTTP vs HTTPS

---

## 1. Encoding
- **Purpose**: Converts data into a different format for compatibility, storage, or transmission. It is not meant to protect data but to make it readable by systems.
- **Example Formats**: Base64, ASCII, UTF-8.
- **How it works**: Encoding transforms data into another format using a reversible process.
  - Example: A text file is encoded into Base64 for email transmission.
- **Use Case**:
  - Making data compatible with different systems (e.g., text to binary).
  - Ensuring special characters in URLs are transmitted safely.

---

## 2. Encryption
- **Purpose**: Protects data by converting it into an unreadable format, making it accessible only to authorized users.
- **Types of Encryption**:
  1. **Symmetric Encryption**: The same key is used for encryption and decryption (e.g., AES).
  2. **Asymmetric Encryption**: A pair of public and private keys are used (e.g., RSA).
- **How it works**: Data is scrambled using an algorithm and can only be deciphered using a specific key.
  - Example: A message encrypted using RSA can only be decrypted with the private key.
- **Use Case**:
  - Securing sensitive data like passwords, credit card numbers, and communication.

---

## Key Differences Between HTTP and HTTPS

| **Feature**        | **HTTP**                     | **HTTPS**                    |
|--------------------|-----------------------------|-----------------------------|
| **Security**       | No encryption (insecure).   | Encrypted (secure).         |
| **Port**           | 80                          | 443                         |
| **Data Integrity** | Vulnerable to tampering.    | Ensures data integrity.     |
| **Use Case**       | Non-sensitive websites.     | Secure websites (e.g., banking, e-commerce). |

---

## Summary
- **Encoding**: Focuses on transforming data for compatibility, not security.
- **Encryption**: Secures data by making it unreadable without the correct key.
- **HTTP vs HTTPS**: HTTPS adds encryption and authentication to HTTP, ensuring secure communication.
