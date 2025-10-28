# Troubleshooting Guide
## Universal Canvas Learning Suite - Common Issues & Solutions

**Quick Tip:** Press `Ctrl+F` (or `Cmd+F` on Mac) to search this page for your specific problem!

---

## 📋 Table of Contents

1. [Installation & Setup Issues](#installation--setup-issues)
2. [Customization Problems](#customization-problems)
3. [Display & Formatting Issues](#display--formatting-issues)
4. [Sharing & Distribution Problems](#sharing--distribution-problems)
5. [Student Access Issues](#student-access-issues)
6. [Interactive Features Not Working](#interactive-features-not-working)
7. [Browser Compatibility Issues](#browser-compatibility-issues)
8. [Performance & Loading Problems](#performance--loading-problems)
9. [Privacy & Data Concerns](#privacy--data-concerns)
10. [Assessment & Form Issues](#assessment--form-issues)

---

## 🔧 INSTALLATION & SETUP ISSUES

### Problem: "I can't find the files!"
**Solution:**
1. Files should be in a ZIP download or GitHub repository
2. Check your Downloads folder
3. Extract the ZIP file (right-click → Extract All)
4. Look for these key files:
   - `universal-canvas-prototype.html`
   - `component-library.html`
   - `complete-lesson-cellular-respiration.html`
   - Documentation (`.md` files)

**Still can't find them?**
- Re-download from the source
- Check if your browser blocked the download
- Ask your tech coordinator for help

---

### Problem: "Files won't open - showing code instead!"
**Solution:**
Your computer is opening the HTML file in the wrong program.

**Fix for Windows:**
1. Right-click the HTML file
2. Choose "Open with" → "Choose another app"
3. Select your web browser (Chrome, Firefox, Edge)
4. Check "Always use this app to open .html files"
5. Click OK

**Fix for Mac:**
1. Right-click (or Ctrl+click) the HTML file
2. Choose "Open With" → "Google Chrome" (or Safari/Firefox)
3. To make permanent: Get Info → Open With → select browser → Change All

**Fix for Chromebook:**
1. Files should automatically open in Chrome
2. If not, upload to Google Drive
3. Open from Drive in browser

---

### Problem: "Where do I start? There are so many files!"
**Solution:**

**Start Here:**
1. Open `README.md` for overview
2. Open `TEACHER_QUICK_START_GUIDE.md` for step-by-step instructions
3. Try `universal-canvas-prototype.html` to see it in action
4. Then start customizing!

**Recommended Order:**
1. Read → Quick Start Guide
2. Explore → Prototype and Complete Lesson
3. Reference → Component Library
4. Build → Your first lesson
5. Share → With students!

---

## 🎨 CUSTOMIZATION PROBLEMS

### Problem: "Configuration panel won't open!"
**Solution:**

**Step 1:** Look for the button
- Should be in top-right corner
- Says "⚙️ Customize This Page"
- If you don't see it, the page might not have the configuration feature

**Step 2:** Check if JavaScript is enabled
- JavaScript must be on for interactive features
- Chrome: Settings → Privacy and Security → Site Settings → JavaScript → Allowed
- Firefox: about:config → javascript.enabled → true

**Step 3:** Try a different browser
- Test in Chrome, Firefox, or Edge
- Sometimes one works better than others

---

### Problem: "My changes aren't saving!"
**Solution:**

**Understanding how it works:**
- Changes in the configuration panel are TEMPORARY
- You must explicitly SAVE the file to keep changes

**How to save:**
1. Make your changes in the config panel
2. Click "Apply" to see them
3. Go to File → Save As (or Ctrl+S)
4. Save with a new name (like "my-math-lesson.html")
5. THAT saved file has your changes!

**Important:**
- Don't just refresh - changes will be lost
- Always "Save As" with a descriptive name
- Keep the original template unchanged (for future use)

---

### Problem: "I changed the colors but they look wrong!"
**Solution:**

**Common color mistakes:**

**Issue:** Colors are too similar (can't read text)
- **Fix:** Check contrast ratio at https://webaim.org/resources/contrastchecker/
- **Minimum:** 4.5:1 for normal text, 3:1 for large text

**Issue:** Hex code doesn't work
- **Fix:** Make sure hex codes start with # and have 6 characters
- **Examples:**
  - ✅ Correct: `#3498DB`
  - ❌ Wrong: `3498DB` (missing #)
  - ❌ Wrong: `#34DB` (too short)

**Issue:** Color names don't work
- **Fix:** Use hex codes instead of color names
- **Exception:** Basic colors work (red, blue, green, white, black)

---

### Problem: "I broke the page and don't know how to fix it!"
**Solution:**

**Quick fix:**
1. Close the broken file
2. Re-open the original template
3. Start over (this time, save more frequently!)

**Prevention:**
1. ALWAYS keep the original template file unchanged
2. Work on a COPY
3. Save versions: `lesson-v1.html`, `lesson-v2.html`, etc.
4. Save often!

**Advanced fix** (if you know HTML):
1. Right-click the page → View Page Source
2. Look for the error (missing closing tag, etc.)
3. Edit the HTML in a text editor
4. Save and test

---

### Problem: "Copy-paste from component library isn't working!"
**Solution:**

**Method 1: Using the Copy Button**
1. Click "Copy Code" button
2. Wait for "✓ Copied!" confirmation
3. Paste in your HTML file (Ctrl+V)

**Method 2: Manual Copy**
1. Select the code manually
2. Start AFTER the `<code>` and BEFORE the `</code>`
3. Copy (Ctrl+C)
4. Paste in your file

**Method 3: If clipboard doesn't work**
1. View the page source (Right-click → View Page Source)
2. Find the component
3. Copy from source
4. Paste in your file

**Common mistakes:**
- ❌ Copying the whole page (too much!)
- ❌ Copying only part of a component (breaks it)
- ❌ Pasting in the wrong place (test to see where it appears)

---

## 🖥️ DISPLAY & FORMATTING ISSUES

### Problem: "Page looks broken/messy!"
**Solution:**

**Checklist:**
1. **Are you viewing in a web browser?** (Not Notepad or Word)
2. **Is the file complete?** (Check if download finished)
3. **Did you accidentally edit the code?** (Revert to original)

**Specific issues:**

**Text is overlapping:**
- Browser zoom might be off → Press Ctrl+0 to reset
- Screen is too small → Try landscape mode or bigger device

**Images aren't showing:**
- Check internet connection (for external images)
- If images were embedded, file might be corrupted

**Colors are all wrong:**
- CSS might be broken
- Try a different browser
- Revert to original file

---

### Problem: "Mobile version looks terrible!"
**Solution:**

**Expected behavior:**
- Page should adapt to smaller screens
- Some elements stack vertically
- Font sizes adjust

**If it's NOT responsive:**
1. Check if this tag is in the `<head>`:
   ```html
   <meta name="viewport" content="width=device-width, initial-scale=1.0">
   ```
2. If missing, add it
3. Save and test again

**Mobile optimization tips:**
- Test on actual devices, not just browser resize
- Turn phone sideways for more space
- Some features work better on tablets than phones

---

### Problem: "Printing looks awful!"
**Solution:**

**Before printing:**
1. Use Print Preview first (Ctrl+P → see preview)
2. Adjust orientation (Portrait vs. Landscape)
3. Set margins to "Default" or "Minimum"
4. Choose "Print backgrounds" if you want colors

**Still looks bad?**
- Remove the configuration panel if visible
- Some gradients don't print well (expected)
- Consider saving as PDF first, then print PDF

**Better alternative:**
- Use browser's "Save as PDF" option
- Gives you a digital copy
- Students can annotate PDFs

---

## 📤 SHARING & DISTRIBUTION PROBLEMS

### Problem: "Students can't access the file!"
**Solution depends on how you're sharing:**

**Method 1: Google Classroom**
- Did you attach the file or just link it?
- Is it set to "Students can view"?
- Try re-uploading the file
- Make sure students are in the correct class

**Method 2: Email**
- Check file size (some email limits are 25MB)
- Students might need to click "Download" before opening
- Some schools block HTML attachments (security)
- Try uploading to Drive and sharing link instead

**Method 3: LMS (Canvas, Schoology, etc.)**
- Upload to Files/Resources section
- Make sure it's published (not draft)
- Check permissions (all students can view)
- Some LMS systems sandbox HTML (remove features)

**Method 4: Link/URL**
- Make sure link is "Anyone with link can view"
- Test the link yourself in an incognito window
- Check if school firewall blocks the domain

---

### Problem: "File is too big to share!"
**Solution:**

**Why it's big:**
- Embedded images (base64 encoded)
- Multiple embedded videos
- Lots of content

**How to reduce size:**

**Option 1:** Remove embedded images
- Link to images instead of embedding
- Use `<img src="https://...">` instead of base64

**Option 2:** Remove embedded videos
- Link to YouTube/Vimeo instead of embedding
- Students click to watch externally

**Option 3:** Split into multiple files
- One file per station/section
- Link between them

**Option 4:** Compress the file
- Use a tool like Gzip or ZIP
- Students download and extract

---

### Problem: "Link sharing isn't working!"
**Solution:**

**Check link permissions:**
1. Open file in Drive/storage
2. Click "Share"
3. Change to "Anyone with the link can view"
4. Copy link
5. Test in incognito/private window

**If using Google Drive:**
- File might need to be in "Shared Drive" not "My Drive"
- Check your school's sharing settings
- Some schools restrict external sharing

**Alternative:**
- Upload to a website (if you have one)
- Use school's file server
- Upload to LMS instead

---

## 👨‍🎓 STUDENT ACCESS ISSUES

### Problem: "Students say the page won't load!"
**Solution:**

**Diagnosis questions:**
1. **What device?** (Computer, tablet, phone?)
2. **What browser?** (Chrome, Safari, Firefox, Edge?)
3. **What error?** (Blank page, error message, infinite loading?)
4. **Just one student or many?** (Isolated issue vs. systemic)

**Common fixes:**

**If blank page:**
- Have student refresh (F5)
- Try different browser
- Check internet connection
- Disable browser extensions

**If error message:**
- Screenshot the error
- Google the error message
- Check if school firewall is blocking

**If loading forever:**
- File might be too large
- Internet might be slow
- Try downloading file instead of streaming

---

### Problem: "Student's progress keeps disappearing!"
**Solution:**

**Why this happens:**
- localStorage is browser/device specific
- Clearing browser cache deletes progress
- Using different device = different localStorage

**Solutions:**

**Short-term:**
- Have student check boxes for completed work
- Doesn't matter that technical progress was lost
- Their submitted work is still saved

**Long-term:**
- Advise students to use same device/browser
- Warn them not to clear browser history
- Consider disabling progress tracking if this is common

**Alternative:**
- Use Google Forms for each section
- Track progress on teacher's end instead

---

### Problem: "Student can't submit their work!"
**Solution:**

**If using Google Forms:**

**Issue:** Form won't open
- Check if pop-ups are blocked
- Allow pop-ups for this site
- Try opening form link directly

**Issue:** Form won't submit
- Make sure all required fields are filled (*)
- Check internet connection
- Try refreshing the form

**Issue:** Not sure if it submitted
- Look for "Your response has been recorded"
- Check teacher's form responses
- Submit again if unsure (teacher can delete duplicate)

**If using other submission method:**
- Check file upload limits
- Verify student is logged in correctly
- Try alternative submission (email, etc.)

---

## ⚙️ INTERACTIVE FEATURES NOT WORKING

### Problem: "Progress tracker won't update!"
**Solution:**

**Check if JavaScript is enabled:**
1. JavaScript is required for interactive features
2. Check browser settings (see [Configuration Problems](#problem-configuration-panel-wont-open) above)

**Try manually:**
1. Uncheck and re-check boxes
2. Refresh the page
3. Try different browser

**If still broken:**
- Feature might not be implemented in this version
- Check console for errors (F12 → Console)
- Report the issue with details

---

### Problem: "Differentiation tabs won't switch!"
**Solution:**

**Expected behavior:**
- Click tab (🟢/🟡/🔴)
- Content below changes

**If not working:**
1. JavaScript must be enabled
2. Click directly on the tab (not nearby)
3. Wait a second (might have slight delay)
4. Try different browser

**Workaround:**
- All content is actually on the page
- Just scroll to find different levels
- Use Ctrl+F to search for "Foundations", "Target", "Extensions"

---

### Problem: "Timer doesn't work!"
**Solution:**

**Checklist:**
1. JavaScript enabled? (Required)
2. Did you click Start button?
3. Is browser window active? (Timers pause when window is inactive)

**Known limitations:**
- Timer resets if page is refreshed
- Doesn't work if JavaScript is disabled
- May not be accurate to the exact second

**Alternative:**
- Use phone timer instead
- Use Google Timer (google.com, search "timer")
- Use browser extension timer

---

## 🌐 BROWSER COMPATIBILITY ISSUES

### Problem: "Works in Chrome but not Safari/Firefox/Edge!"
**Solution:**

**Test matrix:**
| Browser | Version | Status |
|---------|---------|--------|
| Chrome | 90+ | ✅ Best |
| Firefox | 88+ | ✅ Good |
| Safari | 14+ | ⚠️ Mostly works |
| Edge | 90+ | ✅ Good |
| IE 11 | Any | ❌ Not supported |

**Safari-specific issues:**
- Some CSS features render differently
- localStorage may have limits
- Try updating to latest Safari version

**Firefox-specific issues:**
- Usually works well
- Update to latest version if issues
- Check if Enhanced Tracking Protection is blocking features

**Edge-specific issues:**
- Modern Edge (Chromium-based) works like Chrome
- Old Edge (pre-2020) may have issues

**Internet Explorer:**
- NOT SUPPORTED
- Must upgrade to modern browser

---

### Problem: "Looks different on student's browser than mine!"
**Solution:**

**This is normal:**
- Different browsers render slightly differently
- Different OS (Windows/Mac/Chromebook) look different
- Different screen sizes show different layouts

**Concerning differences:**
- Content missing or broken
- Text unreadable
- Features completely non-functional

**What to do:**
1. Ask student for screenshot
2. Test on the same browser/device if possible
3. Provide workarounds for that browser
4. Consider simplifying the design

---

## ⚡ PERFORMANCE & LOADING PROBLEMS

### Problem: "Page loads very slowly!"
**Solution:**

**Likely causes:**
1. **Large file size** - Lots of embedded images/videos
2. **Slow internet** - Student's connection
3. **Old device** - Underpowered computer/tablet
4. **Too many tabs open** - Device running out of memory

**Fixes:**

**For large files:**
- Remove embedded videos (link instead)
- Compress images before embedding
- Split into smaller files

**For slow internet:**
- Provide downloadable version
- Host on fast server/CDN
- Reduce file size

**For old devices:**
- Create simplified version
- Remove animations and gradients
- Test on low-end devices

---

### Problem: "Page freezes or crashes!"
**Solution:**

**Immediate fix:**
- Close other tabs/programs
- Refresh the page (F5)
- Restart browser
- Restart device if needed

**Preventing crashes:**
1. Don't embed too many videos
2. Optimize images (smaller file size)
3. Test on lower-end devices
4. Remove complex animations

**If crash persists:**
- Try different browser
- Update browser to latest version
- Check if device meets minimum requirements
- Report the issue with device/browser details

---

## 🔒 PRIVACY & DATA CONCERNS

### Problem: "Parents asking about data collection!"
**Solution:**

1. Share the `PRIVACY_AND_DATA_POLICY.md` with them
2. Key points to emphasize:
   - No personal data collected by default
   - Progress tracking is local (device only)
   - Google Forms = Google's privacy policy
   - No third-party tracking/ads
   - Data is not sold

3. Send parent notification letter (template in Privacy Policy)
4. Answer specific questions
5. Offer to meet if concerns persist

---

### Problem: "Need FERPA/COPPA compliance documentation!"
**Solution:**

See `PRIVACY_AND_DATA_POLICY.md` for complete details.

**Quick answers:**
- **FERPA:** Compatible (no education records created by framework itself)
- **COPPA:** Compatible (no personal info collected from under-13)
- **Embedded tools:** Check each tool's compliance

**What you need:**
1. Review Privacy Policy document
2. Complete Privacy Checklist for Teachers
3. Get appropriate vendor agreements (Google, etc.)
4. Notify parents
5. Document compliance steps

---

## 📝 ASSESSMENT & FORM ISSUES

### Problem: "Google Form links are placeholders!"
**Solution:**

**Correct!** The template includes placeholder links.

**How to add real forms:**

**Step 1:** Create your Google Form
1. Go to forms.google.com
2. Create new form
3. Add your questions
4. Settings → Responses → Collect email addresses (if needed)

**Step 2:** Get embed link
1. Click Send (top right)
2. Click `< >` (embed icon)
3. Copy the HTML code

**Step 3:** Replace placeholder
1. Find `https://forms.gle/YOUR-FORM-LINK` in your HTML
2. Replace with your actual form link
3. Or use the embed code from Step 2

**Step 4:** Test
1. Open your page
2. Click the form link/button
3. Make sure it opens correctly

---

### Problem: "Can't see student responses!"
**Solution:**

**For Google Forms:**
1. Open your form at forms.google.com
2. Click "Responses" tab
3. You'll see all submitted responses
4. Can view individually or in spreadsheet

**Not seeing any responses?**
- Students might not have submitted yet
- Check if form is set to collect responses
- Make sure you're checking the correct form
- Ask a student to submit a test response

**Export responses:**
- Click green spreadsheet icon in Responses tab
- Creates Google Sheet with all data
- Can download as Excel/CSV

---

### Problem: "Form says 'You need permission to access this form'!"
**Solution:**

**Why this happens:**
- Form is restricted to your organization only
- Student is signed into wrong Google account
- Student doesn't have a Google account

**Fixes:**

**Option 1:** Change form settings
1. Open form editor
2. Settings (gear icon)
3. Uncheck "Restrict to [your organization]"
4. Now anyone with link can respond

**Option 2:** Require school accounts
1. Keep "Restrict to organization" checked
2. Ensure all students use school Google accounts
3. Students must sign in with school email

**Recommendation:**
- Option 2 is more secure
- Prevents outsiders from submitting
- Ensures authentic responses

---

## 🆘 STILL STUCK?

### Before You Contact Support:

**Gather this information:**
1. **What's the problem?** (Be specific!)
2. **What did you try?** (List troubleshooting steps)
3. **What device/browser?** (OS, browser, version)
4. **Screenshot?** (If visual issue)
5. **Error messages?** (Exact wording)

---

### How to Get Help:

**Option 1: Search Documentation**
- Check README.md
- Review Quick Start Guide
- Search this Troubleshooting Guide

**Option 2: Community Support**
- Join teacher community (if available)
- Post in discussion forum
- Ask colleagues who use the tool

**Option 3: Contact Developer**
- Email: [Your contact]
- Include all info from "Before You Contact Support"
- Allow 24-48 hours for response

**Option 4: School Tech Support**
- For device/browser issues
- For network/firewall issues
- For LMS integration issues

---

## 📚 Additional Resources

**Documentation:**
- `README.md` - Overview
- `TEACHER_QUICK_START_GUIDE.md` - Getting started
- `PRIVACY_AND_DATA_POLICY.md` - Privacy info
- `STUDENT_TUTORIAL.md` - Student help

**External Resources:**
- [Can I Use](https://caniuse.com/) - Check browser feature support
- [W3C Validator](https://validator.w3.org/) - Check HTML validity
- [WebAIM Contrast Checker](https://webaim.org/resources/contrastchecker/) - Check color accessibility

---

## 🔄 Version History & Known Issues

**Known Limitations:**
- localStorage data is device/browser specific
- Some features require JavaScript
- IE 11 not supported
- Mobile experience varies by device

**Planned Improvements:**
- Cloud-based progress sync
- More interactive assessment tools
- Better mobile optimization
- Additional templates

**Report Bugs:**
- Check if it's a known issue above
- Search existing bug reports (if GitHub)
- Submit new bug report with details
- Include steps to reproduce

---

## ✅ Troubleshooting Checklist

Before contacting support, try this checklist:

- [ ] Refreshed the page (F5)
- [ ] Tried a different browser
- [ ] Checked internet connection
- [ ] Verified JavaScript is enabled
- [ ] Tested on different device
- [ ] Cleared browser cache
- [ ] Reviewed relevant documentation
- [ ] Searched this troubleshooting guide
- [ ] Gathered error messages/screenshots
- [ ] Listed steps to reproduce problem

If you've done all this and still stuck, it's time to get help!

---

**Last Updated:** October 2025

**Have a problem not listed here?**
Please report it so we can add it to this guide and help others!
