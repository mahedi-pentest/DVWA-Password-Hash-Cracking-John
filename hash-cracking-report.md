# Password Hash Cracking Report

## Target
DVWA Database

## Attack Type
Password Hash Cracking

## Tools Used
- SQLmap
- John the Ripper

## Hash Type
MD5 (Raw-MD5)

## Extracted Hash
8d3533d75ae2c3966d7e0d4fcc69216b

## Cracked Password
charley

## Risk Level
High

## Impact
Attackers can recover user passwords and gain unauthorized access.

## Recommendation
- Use strong hashing algorithms (bcrypt, Argon2)
- Add salt to hashes
- Enforce strong password policy
