# AWS S3 Bucket Misconfiguration – Data Exposure via Public Access

---

## 📌 Summary

A misconfigured AWS S3 bucket was identified that allowed unauthenticated public access to stored objects. This resulted in exposure of sensitive data due to improper access control configuration.

The issue represents a classic **cloud storage misconfiguration vulnerability**, leading to potential unauthorized data access and privacy risks.

---

## 🎯 Vulnerability Type

- Cloud Misconfiguration (AWS S3)
- Broken Access Control
- Sensitive Data Exposure (PII)

---

## ⚔️ Attack Chain (Threat Flow)
Attacker > Finds exposed S3 bucket URL > Accesses bucket via browser (no authentication required) > Directory listing enabled > Downloads sensitive files > Exfiltrates exposed data (PII risk)

---

## 🧠 Visual Attack Flow
[ Attacker ] > [ Public S3 Bucket URL ] > [ Directory Listing Enabled ] > [ Sensitive Files Accessible ] > [ Data Exposure / PII Leak ]

---

## 🔍 Technical Description

The S3 bucket was configured with public read permissions, allowing unauthenticated users to:

- List all stored objects
- Access and download files directly

This indicates improper configuration of:
- Bucket Policy OR
- Access Control List (ACL)

---

## 🧪 Steps to Reproduce

1. Identify the public S3 bucket URL  
2. Open the URL in a browser  
3. Observe directory listing of objects  
4. Access and download files without authentication  

---

## 📂 Impact

- Exposure of sensitive student data (PII)
- Unauthorized access to confidential files
- Potential identity theft or misuse of data
- Compliance and privacy violations

---

## ⚠️ Risk Rating

**High**

### Reasoning:
- No authentication required  
- Public exposure of sensitive data  
- Easily exploitable  
- High impact on confidentiality  

---

## 🛠️ Root Cause

- Misconfigured S3 bucket permissions  
- Lack of "Block Public Access" settings  
- Weak access control enforcement  

---

## 🛡️ Recommended Fixes

- Enable AWS "Block Public Access" settings  
- Restrict bucket access to authenticated users only  
- Apply principle of least privilege  
- Regularly audit S3 permissions  
- Use AWS Access Analyzer for monitoring  

---

## 🧠 Security Lessons

- Cloud misconfiguration is a leading cause of data leaks  
- Public storage should NEVER contain sensitive data  
- Continuous security auditing is critical in cloud environments  

---

## 🏁 Conclusion

This vulnerability demonstrates how simple misconfigurations in cloud storage can lead to serious data exposure. Proper access control policies and regular security audits are essential to prevent such incidents.

---
