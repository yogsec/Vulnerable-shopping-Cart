# Vulnerable Shopping Cart

A deliberately insecure e-commerce application designed for cybersecurity education and penetration testing practice. This project demonstrates common web application vulnerabilities in a controlled, educational environment.

## Disclaimer

**WARNING: This application contains serious security vulnerabilities and is intended for educational purposes only.**

- Do not deploy this application on any production system or public network
- Do not use this application against any system without explicit written authorization
- Use only in isolated, controlled environments for learning and testing
- The creators assume no liability for any misuse of this software
- By using this software, you agree to use it responsibly for educational purposes only

## Overview

This vulnerable shopping cart application is built with HTML, Bootstrap, and vanilla JavaScript, designed to run on GitHub Pages. It contains multiple security vulnerabilities that are commonly found in web applications, making it an excellent tool for:

- Security training and workshops
- Penetration testing practice
- Vulnerability identification exercises
- Secure coding education
- Understanding common web application attacks

## Features

The application simulates a functional e-commerce platform with the following features:

- Product browsing and display
- Shopping cart management
- Product reviews system
- Checkout functionality
- Discount code application
- Session management

## Implemented Vulnerabilities

The application contains the following security vulnerabilities, all verified to be working in modern browsers:

### Cross-Site Scripting (XSS)

1. **Reflected XSS** - The search functionality directly outputs user input without sanitization
2. **Stored XSS** - Product reviews are stored and displayed without proper encoding
3. **DOM-based XSS** - URL hash parameters are injected directly into the page
4. **JavaScript Injection** - eval() function executes user-supplied code

### Access Control Issues

5. **Insecure Direct Object Reference (IDOR)** - Cart and review data can be accessed without proper authorization
6. **Session Fixation** - Session identifiers can be arbitrarily set by users
7. **Missing Authentication** - No login mechanism or access controls

### Data Security Issues

8. **Client-Side Data Exposure** - Sensitive data stored in localStorage in plaintext
9. **Data Leakage** - Checkout data transmitted via GET requests and exposed in console
10. **Information Disclosure** - Detailed error messages and stack traces exposed

### Input Validation Issues

11. **Price Manipulation** - Product prices can be modified on the client side
12. **No Input Sanitization** - Lack of proper input validation across the application

### Security Misconfigurations

13. **Missing Content Security Policy (CSP)** - No CSP headers, allowing inline scripts and eval()
14. **Missing X-Frame-Options** - Application can be embedded in iframes (clickjacking)
15. **CORS Misconfiguration** - Cross-origin requests are not properly restricted

### Other Vulnerabilities

16. **Cross-Site Request Forgery (CSRF)** - No anti-CSRF tokens implemented
17. **Open Redirect** - Unvalidated redirect functionality
18. **No Rate Limiting** - Unlimited requests can be made
19. **Insecure Storage** - All data stored in localStorage without encryption
20. **Global Variable Exposure** - Sensitive data exposed in global scope

### GitHub Pages Deployment

1. Fork or clone this repository to your GitHub account
2. Enable GitHub Pages in repository settings
3. Access the application at `https://yourusername.github.io/Vulnerable-Shopping-Cart`

## Testing Guide

### Quick Start

1. Open the application in your browser
2. Open Developer Tools (F12 or right-click > Inspect)
3. Keep the Console and Network tabs visible
4. Follow the testing guide below to explore each vulnerability

## Expected Behavior

### What You Should See

- **XSS Attacks**: Alert boxes appear, scripts execute, page content changes
- **Price Manipulation**: Cart totals change to unexpected values
- **Session Fixation**: Session ID changes to user-defined values
- **IDOR**: Access to other users' cart and review data
- **Data Leakage**: Sensitive information visible in URL, console, and localStorage
- **Open Redirect**: Redirection to arbitrary websites
- **CSRF**: Simulated cross-origin request execution
- **Clickjacking**: Page can be embedded in iframes
- **No Rate Limiting**: Unlimited requests accepted

## Security Recommendations

If you wish to create a secure version of this application, consider implementing:

### Critical Security Fixes

1. **Input Validation and Output Encoding**
   - Use DOMPurify or similar libraries for HTML sanitization
   - Implement proper output encoding
   - Use textContent instead of innerHTML

2. **Access Control**
   - Implement server-side authentication
   - Use UUIDs instead of sequential IDs
   - Add proper authorization checks

3. **Secure Data Handling**
   - Never store sensitive data client-side
   - Use HTTPS exclusively
   - Implement proper session management

4. **Security Headers**
   - Content Security Policy (CSP)
   - X-Frame-Options: DENY
   - X-Content-Type-Options: nosniff
   - Referrer-Policy: strict-origin-when-cross-origin

5. **Request Validation**
   - Implement CSRF tokens
   - Add rate limiting
   - Validate all inputs server-side

## Technical Architecture

### Technology Stack

- **Frontend**: HTML5, CSS3, Bootstrap 5
- **JavaScript**: Vanilla JS (ES6)
- **Storage**: Browser localStorage (insecure by design)
- **Hosting**: GitHub Pages

### File Structure

```
Vulnerable-Shopping-Cart/
├── index.html          # Main application file
├── README.md           # Documentation
└── LICENSE             # License information
```

## Use Cases

### Security Training

- Classroom demonstrations of web vulnerabilities
- Hands-on labs for security courses
- Capture The Flag (CTF) challenges
- Security awareness training

### Testing Practice

- Vulnerability identification practice
- Penetration testing methodology training
- Security tool familiarization
- Exploit development learning

### Development Education

- Understanding secure coding practices
- Learning from insecure implementations
- Code review training
- Security integration in SDLC

## Contributing

This project is designed for educational purposes. Contributions that add additional vulnerabilities or improve testing documentation are welcome. Please ensure any contributions maintain the educational nature of the project.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Support

For educational questions or clarifications about the vulnerabilities, please open an issue in the repository. Remember, this is for educational purposes only.
