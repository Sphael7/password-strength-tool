# 🛡️ Proton Pass: Secure Password Generator & Analyzer

Welcome to **Proton Pass**, a powerful and secure web-based tool designed to help you create, manage, and analyze strong passwords. In an era where digital security is paramount, this tool offers a simple yet robust solution to protect your online accounts. It's built with a focus on privacy and cryptographic security, ensuring that your passwords are not only strong but also generated using a reliable, privacy-respecting process.

---

## Key Security Features

Here’s a breakdown of the core features that make **Proton Pass** a trusted choice for your password needs.

### 1. Cryptographically Secure Generation
Unlike many generators that rely on simple pseudo-random functions, Proton Pass uses the browser's built-in **Web Crypto API** (`window.crypto.getRandomValues()`).  
This API is specifically designed to produce **high-quality, cryptographically secure random numbers**, making the generated passwords extremely unpredictable and resistant to brute-force attacks.

### 2. Advanced Password Strength Analysis (zxcvbn)
We integrate the renowned **zxcvbn** library, developed by Dropbox. This sophisticated algorithm doesn't just check for character types; it performs a comprehensive analysis to estimate the password's crack time based on common attack methods, including:

- Dictionary words and common phrases  
- Names and biographical data  
- Common keyboard and date patterns  
- Repetitions and sequences  

This provides a **realistic and actionable measure** of your password's security, helping you understand its true vulnerability.

### 3. Privacy-Respecting Data Breach Check
To ensure your passwords haven't been compromised in public data breaches, Proton Pass uses a **private and secure method** to check against the **Have I Been Pwned (HIBP)** database.  

- Only the **first 5 characters of a SHA-1 hash** of your password are sent.  
- This uses the **k-Anonymity method**, so your full password is **never transmitted** to a third-party server.  

This maintains your privacy while giving you critical security information.

### 4. Local-First Operation
All core functionalities—password generation, strength analysis, and history storage—are performed **directly within your browser**.  

- Proton Pass is a **client-side application**, meaning no passwords or sensitive data are sent to our servers.  
- Password history is stored **temporarily in your browser's memory** and is **not persisted**, providing an additional layer of privacy.

---

## How to Use

Proton Pass is designed to be intuitive and easy to use:

1. **Generate**: Select your desired password length and account type, then click the "Generate Password" button.  
2. **Analyze**: Switch to the "Analyze Password" tab to check the strength and data breach status of your existing passwords.  
3. **Copy**: Click the "Copy" button to quickly save the generated password to your clipboard.

---

## Technologies Used

- **HTML5, CSS3, JavaScript**: For the core application logic and UI  
- **zxcvbn**: For robust password strength estimation  
- **Have I Been Pwned API**: For secure data breach checking
