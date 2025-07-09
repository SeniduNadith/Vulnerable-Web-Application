# DressedToHack - Official Writeup

This TryHackMe room is based on a vulnerable clothing store web application designed for web exploitation practice.

## 🐞 Vulnerabilities Included
- **SQL Injection**: Classic login bypass using payloads like `' OR '1'='1`.
- **IDOR**: Insecure Direct Object Reference in the cart view.
- **XSS**: Reflected Cross-Site Scripting via input fields.
- **Path Traversal**: Access sensitive files through directory traversal in image or download parameters.
- **ReDoS**: Regular Expression Denial of Service triggered via crafted search input.

## 🧰 Tools & Techniques
- `sqlmap` for SQLi testing
- `ffuf` or `gobuster` for endpoint fuzzing
- `Burp Suite` for intercepting and manipulating requests
- Manual inspection and payload injection for XSS & IDOR

## 🎯 Walkthrough Summary
- Use SQLi on the login form to bypass authentication.
- Observe cart ID manipulation to access other users' carts (IDOR).
- Inject JavaScript payloads in the search or comment sections (XSS).
- Use directory traversal strings like `../../../../etc/passwd` in download URLs.
- Identify and test for regex-based input patterns to trigger ReDoS.

> ⚠️ This room is for educational use only.
