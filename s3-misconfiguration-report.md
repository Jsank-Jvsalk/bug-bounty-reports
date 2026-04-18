# AWS S3 Bucket Misconfiguration Leading to Public Data Exposure

## 📌 Summary
A misconfigured AWS S3 bucket was identified that allowed public access to sensitive data through directory listing. This misconfiguration exposed student personally identifiable information (PII), creating a significant risk of unauthorized access and data leakage.

---

## 🎯 Vulnerability Type
- Misconfigured Cloud Storage (AWS S3)
- Improper Access Control
- Sensitive Data Exposure

---

## 🧪 Description

The S3 bucket was configured with public read permissions, allowing unauthenticated users to list and access stored objects.

By accessing the bucket URL directly via a web browser, it was possible to view and download files without authentication.

This indicates that the bucket policy or ACL settings were misconfigured, violating the principle of least privilege.

---

## 🔍 Steps to Reproduce

1. Identify the S3 bucket URL  
2. Open the bucket URL in a browser  
3. Observe that directory listing is enabled  
4. Access and download files without authentication  

---

## 📂 Impact

- Exposure of sensitive student data (PII)
- Unauthorized data access by external users
- Potential for identity theft or data misuse
- Reputational damage to the organization

---

## ⚠️ Risk Severity
**High**

Reason:
- Public access to sensitive data
- No authentication required
- Easy exploitation

---

## 🛠️ Recommended Fix

- Disable public access to the S3 bucket  
- Review and update bucket policies and ACLs  
- Enable "Block Public Access" settings in AWS  
- Implement proper authentication and authorization controls  
- Regularly audit cloud storage configurations  

---

## 🧠 Lessons Learned

- Importance of secure cloud configuration  
- Risks of improper access control in cloud environments  
- Need for continuous monitoring and auditing  

---

## 🏁 Conclusion

This vulnerability highlights how simple misconfigurations in cloud storage can lead to severe data exposure. Proper access control and regular audits are essential to prevent such issues.

---
Note: 
## 🔧 Tools Used
- Web browser
- Manual testing
- Basic reconnaissance techniques
