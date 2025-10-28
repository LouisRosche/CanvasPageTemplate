# Privacy Policy & Data Handling Guidelines
## Universal Canvas Learning Suite

**Last Updated:** October 2025
**Effective Date:** October 2025

---

## 📋 Overview

The Universal Canvas Learning Suite is designed with privacy and student data protection as core principles. This document outlines how student data is handled, stored, and protected when using this framework.

---

## 🔒 Core Privacy Principles

### 1. **Student Data Ownership**
- **Students and parents own all student-created data**
- Schools/districts are stewards, not owners
- Data can be exported and deleted at any time

### 2. **Minimal Data Collection**
- Only collect data necessary for educational purposes
- No tracking, analytics, or behavioral profiling
- No third-party data sharing (except as explicitly noted)

### 3. **Transparency**
- Clear communication about what data is collected
- How data is used and stored
- Who has access

### 4. **Security**
- Data stored locally on student devices (by default)
- No centralized database unless explicitly configured
- Encryption recommended for sensitive data

---

## 📊 What Data Is Collected?

### By the HTML Page Itself:

**Progress Data (Optional - localStorage)**
- Which sections students have completed
- Completion percentage
- Timestamp of last activity
- **Location:** Student's browser localStorage only
- **Retention:** Until browser cache cleared
- **Access:** Only the individual student on that device

**No Personal Information Collected:**
- ❌ No names
- ❌ No email addresses
- ❌ No IP addresses
- ❌ No location data
- ❌ No device identifiers
- ❌ No browsing history

### By Embedded Tools (Third-Party):

**If you embed Google Forms:**
- Google's Privacy Policy applies
- Google collects: responses, timestamps, email (if required)
- Data stored in: Teacher's Google account
- **Teacher Responsibility:** Inform students and parents

**If you embed YouTube videos:**
- YouTube's Privacy Policy applies
- May collect: viewing data, cookies
- **Teacher Responsibility:** Use youtube-nocookie.com domain

**If you embed other tools:**
- That tool's privacy policy applies
- **Teacher Responsibility:** Review and approve all embedded tools

---

## 🎓 Compliance with Education Laws

### FERPA (Family Educational Rights and Privacy Act)

**Compliance Status:** ✅ Compatible

The Universal Canvas framework itself does not create "education records" under FERPA because:
- No centralized data collection
- No student identification
- Data remains on local devices

**However:**
- If teachers collect student work via embedded forms → FERPA applies
- Schools must have appropriate agreements with Google/other vendors
- Parents have rights to access, amend, and control student data

**Teacher Responsibilities:**
- Obtain appropriate consent for data collection
- Maintain security of collected student work
- Provide parent access to student records
- Follow district FERPA policies

---

### COPPA (Children's Online Privacy Protection Act)

**Compliance Status:** ✅ Compatible

The framework is COPPA-compliant because:
- No personal information collected by default
- No accounts or registration required
- No persistent identifiers
- No behavioral advertising

**However:**
- If embedding tools that collect data from children under 13 → COPPA applies
- Schools can consent on behalf of parents for educational purposes (school exception)
- Must not use student data for non-educational purposes

**Teacher Responsibilities:**
- Do not embed tools that require student accounts (under 13) without parent consent
- Verify all embedded tools are COPPA-compliant or covered by school exception
- Use Google Workspace for Education (has COPPA provisions) rather than consumer Google

---

### GDPR (General Data Protection Regulation - EU)

**Compliance Status:** ⚠️ Requires Configuration

If serving students in the EU:
- **Right to Access:** Students can export their localStorage data
- **Right to Erasure:** Students can clear localStorage
- **Data Minimization:** Only collect necessary data
- **Lawful Basis:** Educational purpose with parent consent

**Teacher Responsibilities:**
- Obtain explicit parent consent for data processing
- Provide data export mechanisms
- Maintain data processing records
- Appoint Data Protection Officer if required

---

### State Laws (California SOPIPA, New York EdLaw 2-d, etc.)

**Compliance Status:** ✅ Generally Compatible

Most state student privacy laws require:
- ✅ No sale of student data (not applicable - nothing sold)
- ✅ No behavioral advertising (not applicable - no ads)
- ✅ Reasonable security (teacher responsibility)
- ✅ Data deletion upon request (student can clear localStorage)

**Teacher Responsibilities:**
- Review your state's specific requirements
- Ensure embedded tools comply with state law
- Maintain required vendor agreements

---

## 🛡️ Data Security Best Practices

### For Teachers:

1. **Review All Embedded Tools**
   - Before embedding Google Forms, YouTube, or other tools
   - Check their privacy policies
   - Verify school/district has approved vendor agreements
   - Confirm FERPA/COPPA compliance

2. **Use School-Approved Accounts**
   - Use Google Workspace for Education (not personal Gmail)
   - Use district-approved LMS accounts
   - Follow school authentication policies

3. **Secure File Sharing**
   - When sharing HTML files, use secure methods (LMS, password-protected links)
   - Don't email files with student names/data
   - Use school-approved cloud storage

4. **Student Work Collection**
   - If collecting via Google Forms: limit to school accounts only
   - Don't require students to create third-party accounts
   - Store student work securely (district-approved systems)

5. **Inform Parents**
   - Send parent notification about digital tools used
   - Explain what data is collected and how it's used
   - Provide opt-out mechanisms if required

### For Students:

1. **Protect Your Device**
   - Don't share your device with others during lessons
   - Log out of shared computers
   - Use school-provided devices when possible

2. **Be Careful What You Share**
   - Don't include personal information in responses
   - Don't share login credentials
   - Report any privacy concerns to your teacher

3. **Manage Your Data**
   - You can clear your progress by clearing browser data
   - Your teacher can't see your progress unless you submit it
   - Ask questions if you're unsure about privacy

---

## 📝 Parent/Guardian Rights

### You Have the Right To:

1. **Know What Data Is Collected**
   - Ask your child's teacher what tools are embedded
   - Request copies of privacy policies
   - Review data collection practices

2. **Access Your Child's Data**
   - Request copies of student work submitted
   - Review responses and progress
   - Receive data in portable format

3. **Request Deletion**
   - Ask for student data to be deleted
   - Timeframe: typically 30-45 days
   - Exceptions: required records (transcripts, etc.)

4. **Opt Out**
   - Some data collection may be optional
   - Alternative assignments may be provided
   - Discuss concerns with teacher/administrator

5. **File Complaints**
   - Contact school/district privacy officer
   - File FERPA complaint with: [Family Policy Compliance Office](https://www2.ed.gov/policy/gen/guid/fpco/ferpa/index.html)
   - Contact state education department

---

## 🔧 Technical Implementation

### Data Storage Options:

**Option 1: No Data Storage (Default)**
- Students complete work in the page
- Submit via embedded form
- No progress saved
- **Privacy Level:** Highest

**Option 2: localStorage Only**
- Progress saved in browser
- Data never leaves device
- Lost if browser cache cleared
- **Privacy Level:** High

**Option 3: Cloud-Based (Teacher Configured)**
- Progress syncs across devices
- Requires student authentication
- Teacher can view all student progress
- **Privacy Level:** Medium (depends on vendor)

### Recommended Configuration:

For **Elementary (K-5):**
- No data storage
- Teacher-led activities
- Submit work via form or physical paper
- Minimize embedded tools

For **Middle School (6-8):**
- localStorage for progress tracking
- School Google accounts for forms
- Parent notification required
- Regular privacy reminders

For **High School (9-12):**
- localStorage or cloud-based (student choice)
- Digital citizenship education
- Student responsibility emphasized
- More complex embedded tools allowed

---

## 📜 Required Disclosures

### For Teachers to Include:

**Sample Parent Notification Letter:**

```
Dear Parents/Guardians,

This year, I will be using digital learning pages created with the
Universal Canvas Learning Suite. Here's what you need to know:

WHAT IS IT?
An HTML-based learning page that students access via their web browser.
It includes lessons, activities, and assessments for [Subject].

WHAT DATA IS COLLECTED?
- Students' responses to assignments (submitted via Google Forms)
- Optional: Progress tracking (saved only on student device)
- NO personal information, browsing history, or behavioral data

HOW IS DATA USED?
- To assess student learning and provide feedback
- To track completion of assignments
- To personalize instruction

HOW IS DATA PROTECTED?
- Google Workspace for Education is FERPA/COPPA compliant
- Data is not shared with third parties
- Data is deleted when no longer needed

YOUR RIGHTS:
- Access your child's data at any time
- Request deletion of data
- Opt out of optional data collection

QUESTIONS?
Contact me at [teacher email] or our school privacy officer at [email].

[Teacher Signature]
```

---

## ⚠️ Important Disclaimers

### This Framework:
- ✅ Is designed to be privacy-friendly
- ✅ Minimizes data collection by default
- ✅ Gives teachers control over what tools to embed
- ❌ Cannot guarantee privacy of embedded third-party tools
- ❌ Does not provide legal advice
- ❌ Does not replace school/district privacy policies

### Teacher Responsibilities:
- You are responsible for all embedded content
- You must comply with your district's policies
- You must obtain required consents
- You must maintain data security
- You must respond to parent requests

### School/District Responsibilities:
- Establish clear privacy policies
- Provide vendor agreements for tools (Google, etc.)
- Train teachers on privacy requirements
- Designate privacy/data protection officer
- Respond to complaints and requests

---

## 📚 Additional Resources

### For Teachers:
- [Student Privacy Pledge](https://studentprivacypledge.org/)
- [Future of Privacy Forum - Education](https://fpf.org/issues/education/)
- [FERPA Guidance for Teachers](https://www2.ed.gov/policy/gen/guid/fpco/ferpa/index.html)
- [COPPA FAQs](https://www.ftc.gov/business-guidance/privacy-security/childrens-privacy)

### For Administrators:
- [PTAC (Privacy Technical Assistance Center)](https://studentprivacy.ed.gov/)
- [CoSN Privacy Toolkit](https://www.cosn.org/focus-areas/leadership-vision/protecting-privacy/)
- [Common Sense Privacy Evaluation](https://privacy.commonsense.org/)

### For Parents:
- [Parent's Guide to Student Privacy](https://studentprivacy.ed.gov/resources/parent-guide-protecting-student-privacy)
- [Common Sense Media - Privacy](https://www.commonsense.org/education/privacy)

---

## 🔄 Updates to This Policy

This privacy policy will be updated as:
- Laws and regulations change
- New features are added
- Privacy best practices evolve

**How to stay informed:**
- Check this document regularly
- Subscribe to project updates
- Review school/district communications

---

## 📞 Contact Information

**For Privacy Questions:**
- Review this policy
- Contact your school's privacy officer
- Email: [Insert district privacy contact]

**For Technical Questions:**
- Review the documentation
- Contact: [Insert technical support contact]

**For General Questions:**
- Review the README and Quick Start Guide
- Contact: [Insert project contact]

---

## ✅ Privacy Checklist for Teachers

Before using this tool with students:

- [ ] Read this entire privacy policy
- [ ] Review your district's privacy policies
- [ ] Verify all embedded tools are approved by district
- [ ] Confirm vendor agreements are in place (Google, etc.)
- [ ] Prepare parent notification letter
- [ ] Obtain required consents
- [ ] Plan how you'll respond to data access requests
- [ ] Test data export/deletion procedures
- [ ] Train students on privacy best practices
- [ ] Document all embedded tools used
- [ ] Review and update privacy practices annually

---

**Remember:** Privacy is not a one-time task. It's an ongoing commitment to protecting student data and rights!

---

## 📄 License & Legal

**This Privacy Policy:**
- Is provided as a template and starting point
- Must be customized for your specific use case
- Does not constitute legal advice
- Should be reviewed by your legal counsel

**The Universal Canvas Learning Suite:**
- Is open-source software
- Comes with no warranties
- Users assume all responsibility for compliance
- See LICENSE file for software license terms

---

**For the most current version of this policy, visit:**
[GitHub Repository URL]

**Last Updated:** October 2025
