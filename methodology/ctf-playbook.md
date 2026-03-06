# CTF Playbook

A personal methodology and reference guide for approaching CTF challenges.

---

## General Approach

1. **Read the challenge description carefully** – look for hints, file types, or category clues.
2. **Identify the category** – cryptography, web exploitation, reverse engineering, binary exploitation, forensics, etc.
3. **Enumerate and gather information** – download files, inspect source, check headers, run `file` and `strings`.
4. **Research** – look up relevant techniques, tools, and past writeups for similar challenge types.
5. **Iterate** – try multiple approaches; document what you've tried to avoid repeating dead ends.
6. **Capture the flag** – submit and document your solution in the appropriate writeup directory.

---

## Categories

### Cryptography
- Identify the cipher or encoding (Caesar, Vigenère, XOR, RSA, AES, Base64, hex, etc.)
- Use tools: `CyberChef`, `hashcat`, `john`, `openssl`, `pycryptodome`
- Check for weak keys, reused nonces, padding oracle vulnerabilities

### Web Exploitation
- Inspect page source, cookies, HTTP headers, and JavaScript
- Test for SQLi, XSS, SSRF, IDOR, directory traversal, command injection
- Use tools: `Burp Suite`, `sqlmap`, `ffuf`, `gobuster`, `curl`

### Reverse Engineering
- Run `file`, `strings`, `ltrace`, `strace` on binaries
- Decompile/disassemble with `Ghidra`, `IDA`, `Binary Ninja`, `radare2`
- Look for hardcoded strings, flag-checking logic, anti-debug tricks

### Binary Exploitation
- Check protections: `checksec`
- Identify vulnerability type: buffer overflow, format string, heap, ret2libc, ROP
- Use tools: `pwntools`, `GDB` + `pwndbg`/`peda`, `ROPgadget`

### Forensics
- Use `file`, `binwalk`, `exiftool`, `strings`, `xxd` for initial triage
- Check for steganography: `steghide`, `zsteg`, `stegsolve`
- Analyse network captures with `Wireshark` / `tshark`
- Recover deleted files with `foremost`, `photorec`

---

## Useful Resources
- [CTF Field Guide](https://trailofbits.github.io/ctf/)
- [HackTricks](https://book.hacktricks.xyz/)
- [CyberChef](https://gchq.github.io/CyberChef/)
- [CTFtime](https://ctftime.org/)
