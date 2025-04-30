# SecurityBasics
Simple Encryption Algorithm and Firewall application 
-------------------------------------------------------------
# Task Report

This repository contains implementations for two main components:

- **Task 1**: `Encryption.py` – A Merkle–Hellman–style knapsack encryption/decryption system.  
- **Task 2**: `Firewall.py` – A CLI-based firewall rule management tool.

---

## Task 1: Merkle–Hellman-Style Encryption (`Encryption.py`)

### Files  
- `Encryption.py`:  
  - **Key generation**  
    - `generate_private_key(length=8, max_value=99)`  
    - `generate_public_key(e)`  
  - **Conversion utilities**  
    - `text_to_binary_values(text)`  
    - `binary_to_text_values(binary_message)`  
  - **Encryption/decryption routines**  
    - `encrypt_message(binary_message, h)`  
    - `decrypt_message(encrypted_text_list, e, q, w)`  

### Usage Example  
```bash
$ python Encryption.py
Enter the text to encrypt: Hello, world!
Decrypted binary to Text: Hello, world!
```bash

## Task 2: CLI Firewall Rule Manager (Firewall.py)

### Usage Example
$ python Firewall.py
```bash
Welcome to F20CN Firewall Task!!
To add:    add [rule_number] [-in|-out] [address]
To remove: remove [rule_number] [-in|-out]
To list:   list [rule_number] [-in|-out] [address]

> add -in 192.168.1.0-192.168.1.255
Rule added: {'rule_number': 1, 'direction': '-in', 'address': '192.168.1.0-192.168.1.255'}

> list
Firewall Rules:
[Rule 1: -in 192.168.1.0-192.168.1.255]

> remove 1
Rule removed: {'rule_number': 1, 'direction': '-in', 'address': '192.168.1.0-192.168.1.255'}

> exit
Exiting firewall management, Goodbye......
```bash
