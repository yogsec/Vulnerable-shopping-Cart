## Overview

Vulnerable Shopping Cart is a deliberately insecure e-commerce application built for cybersecurity education and penetration testing practice. It demonstrates 16 common web application vulnerabilities and business logic flaws in a realistic shopping cart environment.

![Image](https://github.com/yogsec/Vulnerable-shopping-Cart/blob/main/Screenshot%20From%202026-07-01%2023-46-07.png?raw=true)

View the live demo: [https://yogsec.github.io/Vulnerable-shopping-Cart/](https://yogsec.github.io/Vulnerable-shopping-Cart/)

---

## Vulnerabilities Included

### Critical Vulnerabilities
1. **DOM-based XSS** - URL parameter injection via `?xss=`
2. **Price Manipulation** - Negative and decimal quantities
3. **Gift Card Exploitation** - Client-side balance manipulation
4. **Data Leakage** - Credit card and personal data exposure
5. **Insecure Storage** - Plaintext localStorage data

### High Severity Vulnerabilities
6. **Open Redirect** - Unvalidated `redirectto` parameter
7. **Session Fixation** - URL parameter session control
8. **IDOR** - Unauthorized cart access
9. **Coupon Reuse** - Stackable discounts
10. **Loyalty Points** - Client-side point inflation

### Medium Severity Vulnerabilities
11. **Free Shipping Bypass** - Minimum order validation
12. **CSRF** - Missing anti-CSRF tokens
13. **Clickjacking** - No X-Frame-Options header
14. **Missing CSP** - No Content Security Policy
15. **No Rate Limiting** - Unlimited requests
16. **Information Disclosure** - Error stack traces

## Ethical Use

This application is designed for educational purposes only. Users are expected to:

1. Use only in authorized environments
2. Never deploy in production
3. Respect all applicable laws
4. Use knowledge for defensive security only
5. Practice responsible disclosure

**Remember:** This is a vulnerable application for learning. Always practice responsible security testing and never use these techniques against systems without authorization.
