# Privacy-First Architecture

**DevriQ Tools is built on a privacy-first foundation.** This document explains how we handle your data, why we prioritize privacy, and the technical measures we implement to keep your information secure.

---

## 📋 Table of Contents

- [Privacy Philosophy](#-privacy-philosophy)
- [Data Handling Model](#-data-handling-model)
- [Client-Side Processing](#-client-side-processing)
- [What We DO Collect](#-what-we-do-collect)
- [What We DON'T Collect](#-what-we-dont-collect)
- [Security Practices](#-security-practices)
- [Compliance & Regulations](#-compliance--regulations)
- [Your Rights](#-your-rights)
- [FAQ](#-faq)

---

## 🎯 Privacy Philosophy

**Our Core Principles:**

1. **Your Data Is Yours**
   - You control what information you share
   - No forced data collection
   - You can delete everything anytime

2. **Privacy by Default**
   - Privacy is a feature, not an afterthought
   - All tools process data locally
   - No server uploads needed

3. **Transparency**
   - We clearly explain what happens with your data
   - Simple privacy policy (no legal jargon)
   - Easy to understand terms

4. **Security First**
   - Industry-standard encryption
   - Regular security audits
   - Best practices throughout

5. **User Control**
   - No tracking without consent
   - Easy privacy settings
   - Full data access on request

---

## 📊 Data Handling Model

### The DevriQ Difference

#### ❌ **Traditional Cloud Tools**
```
User → Upload File → Cloud Server → Store Data → Process → Download
        └─ File stays on server
        └─ Potential data retention
        └─ Privacy risks
```

#### ✅ **DevriQ Tools (Privacy-First)**
```
User → Open Tool → Local Browser Processing → Download Result
       └─ File never leaves device
       └─ Processing happens instantly
       └─ No data retention
```

### Key Differences

| Aspect | Traditional Tools | DevriQ Tools |
|--------|-------------------|--------------|
| **Processing Location** | Remote server | Your browser |
| **Data Upload** | Required | Not needed |
| **Storage** | Servers | Your device only |
| **Processing Time** | Varies | Instant |
| **Privacy Risk** | High | Minimal |
| **Internet Requirement** | Always | Only to load tool |
| **Data Retention** | Indefinite | None |

---

## 🔒 Client-Side Processing

### What Is Client-Side Processing?

**Client-side processing** means the tool runs entirely in your web browser on your computer. Your data never touches our servers.

### How It Works

1. **Tool Loads**: You visit a DevriQ tool (e.g., JSON Formatter)
2. **Code Executes Locally**: JavaScript runs in your browser
3. **Data Processing**: Your file/text is processed on your device
4. **Results Generated**: Output is created locally
5. **Download**: You save results to your computer
6. **No Server Involved**: Servers only served the tool code initially

### Technical Implementation

```javascript
// Simplified example: Client-side processing

// 1. User uploads file
const file = document.getElementById('fileInput').files[0];

// 2. File processing happens IN THE BROWSER
const processedData = processData(file);

// 3. Results available for download
const downloadLink = URL.createObjectURL(processedData);

// Server is NOT involved in steps 2-3
```

### Tools Using Client-Side Processing

**All DevriQ tools** use client-side processing:

- ✅ **PDF Tools** — Merging, splitting, converting (all in-browser)
- ✅ **Image Tools** — Compression, resizing, conversion (all in-browser)
- ✅ **Dev Utilities** — JSON formatting, regex testing, encoding (all in-browser)
- ✅ **Text Tools** — Text transformation and analysis (all in-browser)
- ✅ **Calculators** — Instant calculations (all in-browser)

[View all tool categories →](../README.md#-complete-tools-directory)

### JavaScript Libraries Used (Non-Sensitive)

DevriQ uses well-known, open-source libraries for functionality:

- **PDF Processing**: pdf.js, jsPDF (open-source, auditable)
- **Image Processing**: Canvas API, WebGL (browser native)
- **Data Processing**: Standard ECMAScript (browser native)
- **Compression**: Compression algorithms (browser native)

*Note: We do not use proprietary or closed-source libraries for core processing.*

---

## ✅ What We DO Collect

### Minimal, Necessary Data

We collect **only essential information** needed to provide services:

#### 1. **Anonymous Usage Analytics** (Optional)
- **What**: Page visits, tool usage statistics
- **Why**: Understand which tools are popular
- **How**: Privacy-respecting analytics (no tracking)
- **Control**: You can opt-out anytime
- **Retention**: Aggregated only, never personal

#### 2. **Error Logs** (Technical)
- **What**: If a tool crashes, we log errors
- **Why**: Fix bugs and improve reliability
- **How**: Anonymous error reports only
- **Control**: Can be disabled in settings
- **Retention**: 30 days maximum

#### 3. **API Access Logs** (If Using API)
- **What**: Timestamp, tool used, response time
- **Why**: Monitor service health and abuse
- **How**: No personal identifiers stored
- **Control**: Rate limiting on excessive requests
- **Retention**: 7-30 days

#### 4. **Cookie Data** (Technical)
- **What**: Session preferences, language settings
- **Why**: Remember your preferences
- **How**: Stored only on your device
- **Control**: Clear cookies anytime
- **Retention**: Until you clear them

### What We DON'T Store From Your Data

- ❌ Files you upload or process
- ❌ Text content you enter
- ❌ Conversion results or outputs
- ❌ Personal information from documents
- ❌ Metadata from images (unless you store)
- ❌ Browsing history across tools

---

## ❌ What We DON'T Collect

### Explicit Non-Collection

We **explicitly DO NOT** collect:

- 🚫 **Personal Identifiable Information (PII)**
  - Name, email, address, phone number
  - User accounts (unless you create one)
  - Location data
  - IP addresses (logged but not stored)

- 🚫 **Behavioral Tracking**
  - Click tracking
  - Scroll depth
  - Hover patterns
  - Search history

- 🚫 **Third-Party Sharing**
  - We never sell data
  - We never share with advertisers
  - We never use data for marketing
  - We never allow data brokers

- 🚫 **File Contents**
  - We don't scan your files
  - We don't analyze content
  - We don't retain processed documents
  - We don't use AI to train models

- 🚫 **Device Information**
  - Hardware specifications
  - Software installed
  - System information
  - Device IDs

### No Third-Party Tracking

**DevriQ does NOT use:**
- Google Analytics (has tracking)
- Facebook Pixel
- Third-party ad networks
- Any external tracking services

---

## 🛡️ Security Practices

### Multi-Layer Security Approach

#### 1. **Data Encryption**

**In Transit:**
- ✅ HTTPS/TLS encryption for all connections
- ✅ 256-bit encryption standard
- ✅ Certificate pinning on custom domains
- ✅ Regular security audits

**At Rest:**
- ✅ No data stored on servers (eliminated risk)
- ✅ User device uses OS-level encryption
- ✅ No backup servers with data
- ✅ No redundant copies

#### 2. **Code Security**

- ✅ Regular security audits
- ✅ Vulnerability assessments
- ✅ Bug bounty program
- ✅ Secure coding practices
- ✅ Code review process

#### 3. **Infrastructure Security**

- ✅ Firewall protection
- ✅ DDoS mitigation
- ✅ Regular updates and patches
- ✅ Intrusion detection systems
- ✅ 24/7 monitoring

#### 4. **Browser Security**

- ✅ No plugins or extensions required
- ✅ No cross-site scripting (XSS) vulnerabilities
- ✅ No CSRF protections needed (no state changes)
- ✅ Content Security Policy (CSP) headers
- ✅ Subresource Integrity (SRI) for external resources

#### 5. **Access Control**

- ✅ Multi-factor authentication for staff
- ✅ Role-based access control
- ✅ Principle of least privilege
- ✅ Regular access reviews
- ✅ Audit logging

### Security Certifications

- 🔒 SSL/TLS Certificate (valid, regularly renewed)
- 🔒 OWASP Top 10 Compliance
- 🔒 NIST Cybersecurity Framework
- 🔒 Regular penetration testing

---

## ✅ Compliance & Regulations

### GDPR Compliance (European Regulation)

**EU General Data Protection Regulation**

We comply with GDPR because:

- ✅ **Minimal Data Collection**: We collect only necessary data
- ✅ **User Rights**: You can access, modify, delete your data
- ✅ **Privacy by Design**: Privacy built into all systems
- ✅ **Transparent Policies**: Clear, understandable privacy statements
- ✅ **Right to Be Forgotten**: Your request processed in 30 days
- ✅ **Data Processing Agreements**: Available for business users
- ✅ **Privacy Impact Assessments**: Regularly conducted

**Your GDPR Rights:**
- Right to access your data
- Right to rectify inaccurate data
- Right to erase data (right to be forgotten)
- Right to restrict processing
- Right to data portability
- Right to object to processing

### CCPA Compliance (California Regulation)

**California Consumer Privacy Act**

- ✅ Right to know what data is collected
- ✅ Right to delete collected data
- ✅ Right to opt-out of data selling (we don't sell)
- ✅ Right to non-discrimination
- ✅ Privacy notice at collection

### Other Regulations

- ✅ **COPPA**: Compliant with children's privacy (13+)
- ✅ **PIPEDA**: Canadian privacy law compliant
- ✅ **CASL**: Canadian anti-spam law compliant
- ✅ **LGPD**: Brazilian privacy law compliant
- ✅ **Data Localization**: Respect regional data storage laws

---

## 👤 Your Rights

### Data Subject Rights

You have the right to:

1. **Know What We Collect**
   - Request list of all data we hold
   - Understand how it's used
   - See retention policies

2. **Access Your Data**
   - Request copy of your information
   - Download in portable format
   - Export to another service

3. **Correct Your Data**
   - Update inaccurate information
   - Modify preferences
   - Fix personal details

4. **Delete Your Data**
   - Request permanent deletion
   - Remove from all backups
   - Irreversible deletion (right to be forgotten)

5. **Control Your Data**
   - Opt-out of analytics
   - Disable cookies
   - Restrict processing
   - Object to certain uses

6. **Port Your Data**
   - Get data in standard format
   - Transfer to another service
   - Vendor-neutral export

### How to Exercise Your Rights

**To access or manage your rights:**

1. **Visit Settings Page**: [tools.devriq.in/privacy-settings](https://tools.devriq.in/)
2. **Contact Support**: [contact@devriq.in](mailto:contact@devriq.in)
3. **Submit GDPR Request**: Privacy request form on [Privacy Policy](https://tools.devriq.in/privacy-policy/)
4. **Call Support**: Available during business hours

**Response Time:** 30 days (GDPR requirement)

---

## ❓ FAQ

### Q1: Do you sell my data?

**A:** Absolutely not. We never sell, rent, or share your data with third parties. This is a core principle.

### Q2: Can government agencies access my data?

**A:** We comply with lawful government requests through proper legal channels. However, since we don't retain user data, there's nothing to provide in most cases. [See our Transparency Report](https://tools.devriq.in/transparency/)

### Q3: What if I don't want any data collection?

**A:** You can:
- Disable analytics in settings
- Clear cookies after each use
- Use private browsing mode
- Process sensitive files offline
- Delete all usage data

### Q4: How do you make money if everything is free and you don't sell data?

**A:** DevriQ is supported by:
- DevriQ Agency services
- Premium features (optional, future)
- Enterprise solutions
- Donations from users

### Q5: Is my data safe from hackers?

**A:** Your data is safer with DevriQ because:
- We don't store files at all
- Processing happens on your device
- No servers = fewer attack vectors
- Your device's OS provides additional security
- No data retention = no honeypot for hackers

### Q6: Can I trust client-side processing?

**A:** Yes! You can:
- Inspect network traffic (browser dev tools)
- See files aren't uploaded to servers
- Verify in browser console
- Review open-source components
- Test with sensitive files

### Q7: What about HTTPS/SSL certificates?

**A:** DevriQ uses:
- Valid SSL certificates
- HTTPS for all pages
- Regular certificate renewal
- Industry-standard encryption
- Certificate pinning on critical domains

### Q8: Do you collect cookies?

**A:** We use cookies only for:
- Session management
- User preferences
- Security tokens (CSRF protection)
- Analytics (optional, opt-out available)

You can clear cookies anytime. We don't use tracking cookies.

### Q9: How often do you update security?

**A:** Continuously:
- Weekly security patches
- Monthly audits
- Quarterly penetration tests
- Annual third-party assessments
- Real-time threat monitoring

### Q10: What if you get hacked?

**A:** Our incident response plan includes:
1. Immediate service shutdown (if needed)
2. Detailed forensic investigation
3. Notification to affected users
4. Transparent communication
5. Remediation and prevention

Since we don't store data, damage is minimal.

---

## 🔐 Security Best Practices for Users

### Protect Your Privacy

1. **Use Latest Browser** ✅
   - Keep browser updated
   - Enable auto-updates
   - Use modern browser for security features

2. **Clear Cache Regularly** ✅
   - Delete cookies periodically
   - Clear browser cache
   - Use private browsing for sensitive files

3. **Use Secure Connection** ✅
   - Always use HTTPS (look for 🔒)
   - Avoid public WiFi for sensitive data
   - Use VPN if concerned

4. **Verify HTTPS** ✅
   - Look for 🔒 in browser
   - Click certificate to verify
   - Note: DevriQ uses valid certificates

5. **Check URLs** ✅
   - Verify you're on tools.devriq.in
   - Bookmark official site
   - Avoid suspicious links

6. **Keep Device Secure** ✅
   - Use strong password
   - Enable device encryption
   - Install antivirus/malware protection

---

## 📞 Privacy Contact

**Questions about privacy?**

- 📧 **Email**: [privacy@devriq.in](mailto:privacy@devriq.in)
- 🌐 **Privacy Policy**: [tools.devriq.in/privacy-policy](https://tools.devriq.in/privacy-policy/)
- 📋 **GDPR Requests**: [tools.devriq.in/gdpr](https://tools.devriq.in/)
- 💬 **Contact Form**: [devriq.in/contact](https://devriq.in/contact-us)
- 📞 **Phone**: Available during business hours
- 📍 **Data Processing Officer**: [dpo@devriq.in](mailto:dpo@devriq.in)

---

## 📚 Related Documentation

- [Main Privacy Policy](https://tools.devriq.in/privacy-policy/)
- [Terms of Service](https://tools.devriq.in/terms/)
- [Security Best Practices](./resources/SECURITY.md)
- [Troubleshooting Guide](./guides/troubleshooting.md)
- [Getting Started](./GETTING_STARTED.md)

---

## ✨ Our Privacy Commitment

**At DevriQ, privacy isn't just a feature — it's a promise.**

We believe technology should respect your privacy. Every tool we build, every line of code we write, and every decision we make is guided by this principle:

> **Your data is yours. Your privacy is sacred. Your trust is our responsibility.**

---

**Last Updated**: April 2, 2026  
**Status**: Privacy-First Certified ✅  
**Next Review**: Quarterly

---

**Need help?** Contact [privacy@devriq.in](mailto:privacy@devriq.in) or visit [devriq.in](https://devriq.in)
