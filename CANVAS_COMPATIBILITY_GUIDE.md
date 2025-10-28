# Canvas LMS Compatibility Guide
## What Works, What Doesn't, and How to Work Around It

---

## ⚠️ Critical Information About Canvas LMS

**Canvas LMS (Learning Management System) has strict HTML restrictions for security reasons.**

When you paste HTML into Canvas's Rich Content Editor or create a Canvas Page:
- ❌ **JavaScript is stripped** (timers, interactive buttons, etc. won't work)
- ❌ **Event handlers removed** (`onclick`, `onload`, etc. are deleted)
- ❌ **localStorage doesn't work** (progress tracking breaks)
- ❌ **Some CSS is filtered** (animations, positioning may not work)
- ❌ **External scripts blocked** (no CDN links)
- ⚠️ **Forms are limited** (use Canvas Quizzes instead)

---

## ✅ What DOES Work in Canvas

### Safe HTML/CSS Features:

**✅ Structure & Content:**
- Headings (`<h1>` through `<h6>`)
- Paragraphs (`<p>`)
- Lists (`<ul>`, `<ol>`, `<li>`)
- Links (`<a href="">`)
- Images (uploaded to Canvas or absolute URLs)
- Tables
- Divs and spans for organization

**✅ Styling (Inline CSS):**
- Colors (`color`, `background-color`)
- Fonts (`font-family`, `font-size`, `font-weight`)
- Spacing (`margin`, `padding`)
- Borders (`border`, `border-radius`)
- Basic layout (`width`, `max-width`, `text-align`)
- Display (`display: flex`, `display: grid` - mostly works)

**✅ Embedded Content:**
- Canvas-hosted images
- YouTube embeds (using Canvas's embed feature)
- External links
- Canvas files and resources

---

## ❌ What DOESN'T Work in Canvas

### Features That Get Stripped:

**❌ JavaScript:**
```html
<!-- THIS WILL NOT WORK -->
<button onclick="startTimer()">Start Timer</button>
<script>
function startTimer() { ... }
</script>
```

**Why:** Security risk - Canvas removes all JavaScript to prevent malicious code

**❌ Progress Tracking via localStorage:**
```javascript
// THIS WILL NOT WORK
localStorage.setItem('progress', 'completed');
```

**Why:** Canvas manages its own data; localStorage is unreliable or blocked

**❌ Interactive Buttons (with JavaScript):**
```html
<!-- THIS WILL NOT WORK -->
<button onclick="showAnswer()">Reveal Answer</button>
```

**Why:** The `onclick` attribute gets stripped for security

**❌ Collapsible Sections (JavaScript-based):**
```html
<!-- THIS WILL NOT WORK -->
<div onclick="toggleSection()">Click to expand</div>
```

**Why:** Requires JavaScript; Canvas removes it

---

## 🔄 Canvas-Compatible Alternatives

### Instead of JavaScript Timers → Use These Alternatives:

**Option 1: Link to External Timer**
```html
<div style="background: #E3F2FD; padding: 20px; border-radius: 10px; border-left: 5px solid #2196F3;">
    <h3 style="color: #1976D2;">⏱️ Time for This Activity: 15 minutes</h3>
    <p><strong>Use a timer:</strong></p>
    <ul>
        <li>📱 Your phone's timer app</li>
        <li>⏰ A classroom timer</li>
        <li>🌐 Online timer: <a href="https://www.online-stopwatch.com/timer/15minutes/" target="_blank">15-Minute Timer</a></li>
    </ul>
</div>
```

**Option 2: Use Canvas's Built-in Timer**
When creating a Canvas Quiz or Assignment, Canvas has a built-in timer feature:
- Go to Quiz/Assignment settings
- Set "Time Limit"
- Canvas enforces it automatically

---

### Instead of Collapsible Sections → Use These Alternatives:

**Option 1: Accordion-Style Formatting (Visual Only)**
```html
<div style="background: white; border: 2px solid #667EEA; border-radius: 8px; padding: 15px; margin: 10px 0;">
    <h4 style="color: #667EEA; margin-bottom: 10px;">🔽 Click to Expand: Hints for Problem 1</h4>
    <div style="margin-left: 20px; padding: 15px; background: #F8F9FA; border-left: 3px solid #667EEA; border-radius: 5px; display: none;">
        <p><strong>Hint 1:</strong> Start by identifying the variables</p>
        <p><strong>Hint 2:</strong> Use the distributive property</p>
    </div>
    <p style="font-size: 0.9em; color: #666; margin-top: 10px;"><em>Note: Scroll down to see the hints below this section!</em></p>
</div>

<!-- Hints displayed separately below -->
<div style="background: #FFF3E0; padding: 20px; border-radius: 8px; margin: 20px 0;">
    <h4 style="color: #E65100;">💡 Hints for Problem 1 (Try the problem first!)</h4>
    <p><strong>Hint 1:</strong> Start by identifying the variables</p>
    <p><strong>Hint 2:</strong> Use the distributive property</p>
</div>
```

**Option 2: Use Canvas's Built-in Module/Page Structure**
- Create separate Canvas Pages for different sections
- Use Canvas Modules to organize hierarchically
- Students click through pages instead of expanding sections

**Option 3: Details/Summary Element (LIMITED CANVAS SUPPORT)**
```html
<!-- MAY work in some Canvas installations -->
<details style="background: #F8F9FA; padding: 15px; border-radius: 8px; border: 2px solid #667EEA; margin: 10px 0;">
    <summary style="cursor: pointer; font-weight: bold; color: #667EEA;">🔽 Click to see hints</summary>
    <div style="margin-top: 15px;">
        <p><strong>Hint 1:</strong> Start by identifying the variables</p>
        <p><strong>Hint 2:</strong> Use the distributive property</p>
    </div>
</details>
```
**Note:** The `<details>` element is native HTML5 and SOMETIMES works in Canvas, but NOT guaranteed. Test in your Canvas instance!

---

### Instead of Progress Tracking → Use These Alternatives:

**Option 1: Canvas's Built-in Progress Tracking**
- Canvas automatically tracks:
  - Page views (in Course Analytics)
  - Assignment submissions
  - Quiz completion
  - Module completion requirements

**How to use:**
1. Create Modules with completion requirements
2. Add Pages/Assignments to modules
3. Set "Students must complete requirements" in module settings
4. Canvas shows progress bars automatically

**Option 2: Student Self-Tracking (Paper/Digital)**
```html
<div style="background: #E8F5E9; padding: 20px; border-radius: 10px; margin: 20px 0;">
    <h3 style="color: #2E7D32;">📋 Track Your Progress</h3>
    <p><strong>As you complete each section, check it off:</strong></p>
    <ul style="list-style: none; padding-left: 0;">
        <li style="margin: 10px 0;">☐ Introduction</li>
        <li style="margin: 10px 0;">☐ Section 1: Understanding the Concept</li>
        <li style="margin: 10px 0;">☐ Section 2: Examples</li>
        <li style="margin: 10px 0;">☐ Section 3: Practice Problems</li>
        <li style="margin: 10px 0;">☐ Reflection</li>
    </ul>
    <p style="margin-top: 15px;"><em>💡 Tip: Copy this list to your notebook or a separate document to track your progress!</em></p>
</div>
```

**Option 3: Use Canvas Quizzes for Checkpoints**
- Create ungraded "knowledge checks" throughout content
- Students submit to mark completion
- You can see who's completed what in SpeedGrader

---

### Instead of "Copy Code" Buttons → Use These Alternatives:

**Option 1: Provide Downloadable Files**
```html
<div style="background: #F3E5F5; padding: 20px; border-radius: 10px; margin: 20px 0;">
    <h4 style="color: #6A1B9A;">📥 Download This Component</h4>
    <p>Download the HTML file and upload it to your Canvas course:</p>
    <a href="/files/component-example.html" style="background: #9C27B0; color: white; padding: 10px 20px; border-radius: 6px; text-decoration: none; display: inline-block; font-weight: 600;">Download HTML File</a>
    <p style="margin-top: 15px; font-size: 0.9em;"><em>Then upload to Files in your Canvas course and link to it!</em></p>
</div>
```

**Option 2: Provide Components in a Google Doc**
- Create a Google Doc with all components
- Teachers can copy-paste from there
- Share link: "Make a copy" template

---

### Instead of Interactive Quizzes → Use Canvas Quizzes

**❌ Don't create JavaScript-based quizzes in Pages**
**✅ Use Canvas's Quiz feature instead**

**Why:** Canvas Quizzes have:
- Automatic grading
- Built-in question types (multiple choice, fill-in-blank, essay)
- Timed options
- Randomization
- Partial credit
- Integration with Gradebook

**How:**
1. Go to Quizzes in your Canvas course
2. Create New Quiz
3. Add questions using Canvas's question bank
4. Set parameters (time limit, attempts, etc.)

---

## 🎨 Canvas-Safe Component Library

### 1. Lesson Header (Canvas-Compatible)

```html
<div style="background: linear-gradient(135deg, #667EEA 0%, #764BA2 100%); color: white; padding: 40px 20px; border-radius: 15px; margin-bottom: 30px; text-align: center;">
    <h1 style="font-size: 2.5em; margin-bottom: 10px;">YOUR LESSON TITLE</h1>
    <p style="font-size: 1.2em; opacity: 0.95;">Grade Level | Subject | About XX minutes</p>
</div>
```

**✅ Works in Canvas:** Yes, inline styles work perfectly

---

### 2. Learning Objectives Box

```html
<div style="background: #F8F9FA; border-left: 5px solid #667EEA; padding: 20px; margin: 20px 0; border-radius: 5px;">
    <h2 style="color: #667EEA; margin-bottom: 15px;">🎯 By the end of this lesson, you'll be able to:</h2>
    <ul style="line-height: 1.8; font-size: 1.05em;">
        <li>Objective 1</li>
        <li>Objective 2</li>
        <li>Objective 3</li>
    </ul>
</div>
```

**✅ Works in Canvas:** Yes

---

### 3. Kind Support Box

```html
<div style="background: #E8F5E9; border-left: 5px solid #4CAF50; padding: 20px; margin: 20px 0; border-radius: 5px;">
    <p><strong style="color: #2E7D32;">💙 Need Help?</strong></p>
    <p>If you're stuck, that's totally normal! Here are some options:</p>
    <ul style="margin-top: 10px;">
        <li>Review the example above</li>
        <li>Ask a classmate</li>
        <li>Raise your hand or send me a message</li>
    </ul>
</div>
```

**✅ Works in Canvas:** Yes

---

### 4. Activity Box with Choices

```html
<div style="background: #FFF9E6; border: 3px solid #FFD700; padding: 25px; margin: 20px 0; border-radius: 10px;">
    <h3 style="color: #F4A460; margin-bottom: 15px;">📝 Choose Your Activity</h3>
    <p><strong>Pick ONE of the following:</strong></p>

    <div style="background: white; border: 2px solid #667EEA; padding: 15px; margin: 15px 0; border-radius: 8px;">
        <h4 style="color: #667EEA;">Option A: Written Response</h4>
        <p>Write 1-2 paragraphs explaining...</p>
    </div>

    <div style="background: white; border: 2px solid #52C75A; padding: 15px; margin: 15px 0; border-radius: 8px;">
        <h4 style="color: #52C75A;">Option B: Visual Representation</h4>
        <p>Create a diagram or drawing that shows...</p>
    </div>

    <div style="background: white; border: 2px solid #9C27B0; padding: 15px; margin: 15px 0; border-radius: 8px;">
        <h4 style="color: #9C27B0;">Option C: Teach Someone</h4>
        <p>Explain this concept to a family member and have them sign off...</p>
    </div>
</div>
```

**✅ Works in Canvas:** Yes - purely visual, no JavaScript needed

---

### 5. Differentiation Levels (Canvas-Compatible)

```html
<div style="margin: 30px 0;">
    <h3 style="margin-bottom: 15px;">📚 Choose Your Learning Path</h3>
    <p style="margin-bottom: 20px;">All three options teach the same concept—pick the one that feels right for you today!</p>

    <!-- Foundations -->
    <div style="background: white; border: 3px solid #4CAF50; padding: 20px; margin: 15px 0; border-radius: 10px;">
        <h4 style="color: #4CAF50; margin-bottom: 10px;">🟢 Foundations: Extra Support</h4>
        <p><strong>Choose this if:</strong> This topic is new to you, you want step-by-step help, or you prefer more examples and guidance.</p>
        <p style="margin-top: 10px;"><a href="[LINK TO FOUNDATIONS PAGE]" style="background: #4CAF50; color: white; padding: 10px 20px; border-radius: 6px; text-decoration: none; display: inline-block; font-weight: 600;">Go to Foundations Version</a></p>
    </div>

    <!-- Target -->
    <div style="background: white; border: 3px solid #FFD700; padding: 20px; margin: 15px 0; border-radius: 10px;">
        <h4 style="color: #F57C00; margin-bottom: 10px;">🟡 Target: Grade-Level</h4>
        <p><strong>Choose this if:</strong> You feel comfortable with the basics and are ready to practice independently.</p>
        <p style="margin-top: 10px;"><a href="[LINK TO TARGET PAGE]" style="background: #FFD700; color: #333; padding: 10px 20px; border-radius: 6px; text-decoration: none; display: inline-block; font-weight: 600;">Go to Target Version</a></p>
    </div>

    <!-- Extensions -->
    <div style="background: white; border: 3px solid #E74C3C; padding: 20px; margin: 15px 0; border-radius: 10px;">
        <h4 style="color: #E74C3C; margin-bottom: 10px;">🔴 Extensions: Extra Challenge</h4>
        <p><strong>Choose this if:</strong> This topic is easy for you and you want to go deeper or try something creative.</p>
        <p style="margin-top: 10px;"><a href="[LINK TO EXTENSIONS PAGE]" style="background: #E74C3C; color: white; padding: 10px 20px; border-radius: 6px; text-decoration: none; display: inline-block; font-weight: 600;">Go to Extensions Version</a></p>
    </div>
</div>
```

**✅ Works in Canvas:** Yes - uses Canvas Pages instead of JavaScript tabs
**Implementation:** Create 3 separate Canvas Pages (one for each level)

---

### 6. Reflection Prompts

```html
<div style="background: #FAFAFA; border: 2px dashed #999; padding: 25px; margin: 20px 0; border-radius: 10px;">
    <h3 style="color: #444; margin-bottom: 15px;">💭 Reflection Questions</h3>
    <p style="margin-bottom: 15px;"><strong>Think about or write down your answers:</strong></p>
    <ol style="line-height: 2;">
        <li>What's one thing you learned today?</li>
        <li>What's still confusing?</li>
        <li>How could you use this in real life?</li>
    </ol>
    <p style="margin-top: 20px; font-size: 0.95em; color: #666;"><em>💡 You can type your answers in the "Comments" section below, submit them as a text entry, or just think about them!</em></p>
</div>
```

**✅ Works in Canvas:** Yes
**Integration:** Students can submit responses via Canvas Assignment submission

---

### 7. Example/Non-Example Comparison

```html
<div style="margin: 30px 0;">
    <h3 style="margin-bottom: 20px;">✅ Example vs. ❌ Non-Example</h3>

    <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 20px; margin-bottom: 20px;">
        <!-- Example -->
        <div style="background: #E8F5E9; border: 3px solid #4CAF50; padding: 20px; border-radius: 10px;">
            <h4 style="color: #2E7D32; margin-bottom: 10px;">✅ Good Example</h4>
            <p style="font-family: monospace; background: white; padding: 15px; border-radius: 5px;">
                Example content here
            </p>
            <p style="margin-top: 15px;"><strong>Why this works:</strong> Explanation here</p>
        </div>

        <!-- Non-Example -->
        <div style="background: #FFEBEE; border: 3px solid #F44336; padding: 20px; border-radius: 10px;">
            <h4 style="color: #C62828; margin-bottom: 10px;">❌ Needs Work</h4>
            <p style="font-family: monospace; background: white; padding: 15px; border-radius: 5px;">
                Non-example content here
            </p>
            <p style="margin-top: 15px;"><strong>Why this needs work:</strong> Explanation here</p>
        </div>
    </div>
</div>
```

**✅ Works in Canvas:** Yes
**Note:** Grid layout usually works, but might stack on mobile (which is fine!)

---

## 📋 Canvas Workflow Best Practices

### How to Use These Components in Canvas:

**Method 1: Rich Content Editor (HTML View)**
1. Click "Edit" on your Canvas Page
2. Click the `<>` HTML Editor button (usually top right)
3. Paste the HTML code
4. Click `<>` again to return to visual editor
5. Save Page

**Method 2: Import from File**
1. Create complete HTML file locally
2. Upload to Canvas Files
3. Link to file from Page/Module
4. Students click to open in new tab

**Method 3: Use Canvas Templates**
1. Create ONE perfect page with these components
2. Use "Copy To..." to duplicate it
3. Edit the duplicated version for each lesson
4. Saves time!

---

## ⚠️ Common Canvas Issues & Fixes

### Issue 1: My styles disappeared when I saved!

**Cause:** Canvas stripped some CSS

**Fix:** Only use inline styles on individual elements:
```html
<!-- ✅ THIS WORKS -->
<div style="background: #E3F2FD; padding: 20px;">Content</div>

<!-- ❌ THIS MIGHT GET STRIPPED -->
<style>
.my-class { background: #E3F2FD; }
</style>
<div class="my-class">Content</div>
```

---

### Issue 2: My buttons don't do anything!

**Cause:** JavaScript was stripped

**Fix:** Use links instead of interactive buttons:
```html
<!-- ❌ THIS WON'T WORK -->
<button onclick="showAnswer()">Reveal Answer</button>

<!-- ✅ THIS WORKS -->
<a href="#answer-section" style="background: #667EEA; color: white; padding: 10px 20px; border-radius: 6px; text-decoration: none; display: inline-block;">Jump to Answer</a>

<!-- Later on the page -->
<div id="answer-section" style="background: #E8F5E9; padding: 20px; border-radius: 10px;">
    <h4>Answer:</h4>
    <p>The answer is...</p>
</div>
```

---

### Issue 3: My progress tracker doesn't save!

**Cause:** localStorage doesn't work in Canvas

**Fix:** Use Canvas's module requirements:
1. In Modules, click the 3 dots next to a module
2. Choose "Edit"
3. Check "Students must complete requirements in order"
4. Set requirements for each item
5. Canvas tracks completion automatically!

---

### Issue 4: My images broke!

**Cause:** External image links may be blocked

**Fix:** Upload images to Canvas Files:
1. Go to Files in your Canvas course
2. Upload images
3. Insert image using Canvas's image tool (not manual HTML)
4. Canvas provides proper URL

---

## ✅ Final Canvas Compatibility Checklist

Before publishing content in Canvas:

- [ ] All JavaScript removed or replaced with Canvas features
- [ ] Only inline CSS used (no `<style>` blocks or external CSS)
- [ ] Images uploaded to Canvas Files (not external URLs)
- [ ] Interactive elements replaced with Canvas-native tools (Quizzes, Assignments)
- [ ] Links use Canvas's internal linking (Pages, Files, Assignments)
- [ ] Tested in Canvas's preview mode
- [ ] Tested on mobile (Canvas mobile app)
- [ ] Checked with screen reader if accessibility matters

---

## 📚 Resources

**Canvas Guides:**
- [Canvas HTML Editor Guide](https://community.canvaslms.com/t5/Canvas-Basics-Guide/tkb-p/basics)
- [Canvas Accessibility Guide](https://community.canvaslms.com/t5/Canvas-Resource-Documents/Canvas-Accessibility-Standards/ta-p/1989)

**What to Use Instead:**
- **JavaScript timers** → Canvas Quiz time limits or external timer links
- **Progress tracking** → Canvas Module requirements
- **Interactive quizzes** → Canvas Quizzes feature
- **Collapsible sections** → Multiple Canvas Pages organized in Modules
- **Copy buttons** → Download links to files

---

## 💙 Remember

**Canvas LMS restrictions exist for good security reasons.** They protect students from malicious code.

**The good news:** Canvas has BUILT-IN features that replace most JavaScript functionality:
- Modules (organization & progress tracking)
- Quizzes (assessments with auto-grading)
- Assignments (collecting work)
- SpeedGrader (feedback & grading)
- Analytics (tracking engagement)

**Our framework still works in Canvas—just use Canvas-native features instead of JavaScript!** 🌟

