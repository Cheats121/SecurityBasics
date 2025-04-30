# SecurityBasics
Simple Encryption Algorithm and Firewall application 
-------------------------------------------------------------
# Task Report

This repository contains implementations for two main components:

- **Task 1**: `Encryption.py` implementing a Merkle–Hellman-style knapsack encryption/decryption system.  
- **Task 2**: `Firewall.py` providing a CLI firewall rule management tool.

---

## Task 1: Merkle–Hellman-Style Encryption (`Encryption.py`)

**Description**  
A simplified knapsack-based public-key cryptosystem.

### Files
- `Encryption.py`: Main module containing:
  - Key generation functions (`generate_private_key`, `generate_public_key`).
  - Encryption/decryption routines (`encrypt_message`, `decrypt_message`).
  - Conversion utilities (`text_to_binary_values`, `binary_to_text_values`).

### Usage Example
```bash
python Encryption.py
# Enter plaintext when prompted, then see the decrypted output.
Key Functions
generate_private_key(length=8, max_value=99) -> List[int]

generate_public_key(e: List[int]) -> Tuple[List[int], int, int]

encrypt_message(binary_message: List[int], h: List[int]) -> List[int]

decrypt_message(cipher_list: List[int], e: List[int], q: int, w: int) -> List[int]

Limitations
Demonstration only: 8-bit blocks, insecure for real use.

Performance degrades with larger key sizes.

Task 2: Firewall Rule Manager (Firewall.py)
Description
A command-line interface to add, list, and remove firewall rules with IP and direction filters.

Files
Firewall.py: Main module defining:

Firewall class with add_rule_command, remove_rule_command, list_rules_command.

Parsing logic (parse_input).

Usage Example
bash
Copy
Edit
python -c "from Firewall import Firewall, parse_input; fw=Firewall(); fw.add_rule_command(1, '-in', '192.168.1.10'); fw.list_rules_command()"
or run interactively:

bash
Copy
Edit
python Firewall.py
# Follow on-screen prompts: add/remove/list/syntax/exit
Features
Add Rule: add <rule_number> [-in|-out] <IP_or_CIDR>

Remove Rule: remove <rule_number> [direction]

List Rules: list [rule_number] [direction] [IP_or_CIDR]

Input validation using Python ipaddress module.
