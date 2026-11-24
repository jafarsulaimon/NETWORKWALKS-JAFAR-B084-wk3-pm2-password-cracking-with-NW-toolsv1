# NETWORKWALKS-JAFAR-B084-wk3-pm1-password-cracking-with-NW-toolsv1
Password Cracking with Networkwalks Tools (No-Install Browser Method)
Overview

This project demonstrates PDF password recovery using Networkwalks' free browser-based tools — the Hash Calculator and Password Cracker — as a no-install alternative to John the Ripper / Johnny. It's Week 3, Module 2 of a Networkwalks Cybersecurity & Ethical Hacking project series, paired with Module 1 (JTR/Johnny).

Objective

Recover the password of a locked PDF (My Locked PDF1.pdf) entirely in-browser, without installing any local cracking tools.

Tools Used
Networkwalks Hash Calculator — extracts a crackable, hashcat/John-compatible hash ($pdf$... format) from a password-protected PDF, using client-side parsing (no file upload to a server)
Networkwalks Password Cracker — runs a dictionary attack against the extracted hash, matching it word-by-word against a wordlist
Methodology
Uploaded the locked PDF to the Hash Calculator, which parsed it locally in-browser and extracted the $pdf$... hash (the same format pdf2john produces for John the Ripper)
Copied the full hash string
Pasted the hash into the Password Cracker and ran the built-in dictionary attack (100-word list)
Tool iterated through candidate passwords, logging each attempt (service, canada, hockey, george...) until it found a match
Password recovered: password1
Verified the password by opening the PDF in Adobe Acrobat Reader
Key Concepts Demonstrated
Hash extraction: converting a password-protected file's encryption metadata into a crackable hash format
Dictionary attacks: testing a finite wordlist against a hash rather than brute-forcing all combinations
Encryption vs. hashing: encryption is reversible with a key; hashing is a one-way function used to verify password matches without storing the plaintext
Takeaway

Weak, common passwords (like password1) are crackable in seconds even using lightweight, browser-only tools with no local installation — reinforcing the need for long, unique, high-entropy passwords.
