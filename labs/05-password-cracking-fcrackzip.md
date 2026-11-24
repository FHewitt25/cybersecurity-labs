# Lab 5: Password Cracking with fcrackzip

**Tool:** Linux Security Workstation VM · **Focus:** Cryptography and password strength

## Scenario
A company policy allows only encrypted ZIP files on USB drives. An executive lost the password to one. Could it be recovered, and what does that say about password strength?

## What I did
1. Created sample files and encrypted them into five ZIP archives with passwords of **1 to 5 characters** (`zip -e file-1.zip sample*`).
2. Confirmed a wrong password fails to open them.
3. Ran a brute-force recovery with **fcrackzip**:
   ```bash
   fcrackzip -vul 1-4 file-1.zip   # -v verbose, -u verify with unzip, -l length range
   fcrackzip -vul 1-5 file-5.zip
   ```

## Results
| Password length | Time to crack |
|---|---|
| 1–3 characters | about a second |
| 4 characters | seconds |
| 5 characters | much longer; depends on the system and the password |

## Security takeaways
- Short passwords fall to brute force almost instantly, even when the file is "encrypted."
- **Length and complexity** are what make brute force impractical; each added character multiplies the search space.
- The same tools defenders use for recovery (fcrackzip, John the Ripper, hashcat) are used by attackers, which is why strong password policies and MFA matter.
