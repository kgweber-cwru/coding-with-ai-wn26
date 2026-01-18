# Welcome to Coding with AI (Winter 2026)
## Student Setup Guide: Get Ready Before Day 1

---

## Overview

Before the first class session, you'll need to:
1. **Access course materials** on GitHub
2. **Set up Google Colab** (our coding environment)
3. **Connect your Google Drive** to Colab (for saving your work)
4. **Obtain API keys** for accessing language models
5. **Redeem your Google Cloud educational credits** (optional, for advanced projects)

This guide walks you through each step. **Estimated time: 30-40 minutes**

**Key Concept:** You'll be working entirely in Google Colab, a cloud-based Jupyter notebook environment. Your notebooks are stored in your personal Google Drive, so all your work is automatically saved and accessible from any device.

---

## Part 1: Accessing Course Materials on GitHub

### Step 1: Create a GitHub Account (if you don't have one)
- Go to [github.com](https://github.com)
- Click "Sign up" in the top-right corner
- Follow the registration process (email, password, username)
- Verify your email address
- **You now have a GitHub account!**

*[INSERT IMAGE: Screenshot of github.com homepage with "Sign up" button highlighted]*

### Step 2: Navigate to the Course Repository
- Open this link in your browser: [github.com/kgweber-cwru/coding-with-ai-wn26](https://github.com/kgweber-cwru/coding-with-ai-wn26)
- You should see a folder-like structure with course materials
- Look for the "week-0" folder

*[INSERT IMAGE: Screenshot of the repository main page showing folder structure]*

### Step 3: Star the Repository (Optional)
- Click the **"Star"** button (top-right of the repository)
- This saves the repository to your GitHub profile so you can easily find it later.

---

## Part 2: Set Up Google Colab

### What is Google Colab?
Google Colab is a **free, cloud-based coding environment** where you can write and run Python code directly in your browser. You don't need to install anything on your computer - everything runs on Google's servers.

**Why we use it:**
- ✅ Integrated with Google Drive (easy saving)
- ✅ GPU access for AI/ML projects (free tier available)
- ✅ Pre-installed libraries for machine learning
- ✅ No setup needed - works immediately
- ✅ Easy sharing and collaboration

### Step 1: Use your CWRU Google Credentials
You'll use your CWRU Google account to use Colab (same one you'll use for Drive and GCP).

### Step 2: Access a Notebook from GitHub
1. Go to the course repository: [github.com/kgweber-cwru/coding-with-ai-wn26](https://github.com/kgweber-cwru/coding-with-ai-wn26)
2. Navigate to **week-1-llm-basics-and-api**
3. Click on **concepts.ipynb** (or any `.ipynb` file you want to open)
4. You'll see a preview of the notebook in GitHub

*[INSERT IMAGE: GitHub repository with week-1 folder and concepts.ipynb highlighted]*

### Step 3: Open Notebook in Google Colab
**Method 1: From GitHub (Recommended)**

In the GitHub preview of the `.ipynb` file, look for the **Colab badge/button** at the top of the notebook:
- Click the **"Open in Colab"** button (or similar badge)
- The notebook will automatically open in Google Colab in a new tab

*[INSERT IMAGE: Colab badge in GitHub preview, showing "Open in Colab" button]*

**Method 2: Manual Link**

If you don't see the badge, you can construct the link:
- Replace `github.com` with `colab.research.google.com/github` in the URL
- Example: `https://colab.research.google.com/github/kgweber-cwru/coding-with-ai-wn26/blob/main/week-1-llm-basics-and-api/concepts.ipynb`

### Step 4: Review the Notebook in Colab
- The notebook is now open in Colab, but it's **read-only** (you can't edit it yet)
- This is a view of the original from GitHub
- Scroll through to see what you'll be working on
- ✅ If you can read the code and explanations, you're all set!

*[INSERT IMAGE: Notebook open in Google Colab, showing code cells]*

---

## Part 3: Save Your Working Copy to Google Drive

### Why Make a Copy?
The GitHub notebook is the "master copy." When you open it, you're viewing the original. To write your own code and save your progress, you need to save a **copy to your Google Drive**.

### Step 1: Save a Copy to Drive
1. In Colab, go to **File** → **Save a copy in Drive**
2. A dialog will pop up asking where to save
3. Choose where in your Drive (or just accept the default: `Colab Notebooks` folder)
4. Click **OK**

*[INSERT IMAGE: File menu and "Save a copy in Drive" option highlighted]*

### Step 2: Switch to Your Copy
- A new tab will automatically open with **your personal copy**
- Notice the file name changes to something like "Copy of concepts.ipynb"
- **This is now YOUR notebook** - all your changes save automatically to your Drive
- You can edit the code, add notes, run experiments

*[INSERT IMAGE: New Colab window with file saved, showing "Copy of concepts.ipynb" in title]*

### Step 3: Rename Your Copy (Optional but Recommended)
1. Click the filename at the top of Colab ("Copy of concepts")
2. Edit it to something clear like "Week1-Concepts-[YourName]"
3. Press Enter to save the new name

*[INSERT IMAGE: Colab filename editor showing rename in progress]*

### Step 4: Verify Your Copy is in Drive
1. Go to [drive.google.com](https://drive.google.com) in a new tab
2. Look for your notebook file (should be in "Colab Notebooks" folder or where you saved it)
3. ✅ Your copy is safely stored in your Drive and will persist between sessions

*[INSERT IMAGE: Google Drive showing saved Colab notebook]*

---

## Part 4: Connect Google Drive to Colab (For File Access)

### Why Connect Drive to Colab?
As you progress through the seminar, you'll work with datasets, save results, and manage files. Connecting Drive allows your Colab notebooks to access files from your Drive directly.

### Step 1: Mount Google Drive in Your Notebook
In your Colab notebook, add this code cell at the top:

```python
from google.colab import drive
drive.mount('/content/drive')
```

*[INSERT IMAGE: Code cell in Colab with mount code]*

### Step 2: Run the Cell
1. Click the **Play button** (▶) next to the cell
2. A popup will appear asking for permission
3. Click **"Connect to Google Drive"**
4. Select your Google account
5. Click **"Allow"** to give Colab permission to access your Drive

*[INSERT IMAGE: Drive permission dialog in Colab]*

### Step 3: Verify Connection
After clicking "Allow," you should see:
```
Mounted at /content/drive
```

This means your Drive is now connected and accessible to your code.

*[INSERT IMAGE: Success message showing mounted drive]*

### Step 4: Access Your Drive Files
Now your notebook can read and write files to your Drive:
```python
# Example: Read a file from your Drive
import pandas as pd
df = pd.read_csv('/content/drive/My Drive/my_file.csv')

# Example: Save a file to your Drive
df.to_csv('/content/drive/My Drive/my_results.csv')
```

You'll learn more about this in class, but the key point: **your notebook can now access your Drive files!**

---

## Part 5: Redeem Your Google Cloud Educational Credits

### What Are These For?
Your instructor has provided **$50 in Google Cloud educational credits** for this course. These credits enable you to:
- ✅ Use Gemini 1.5 Ultra (advanced features)
- ✅ Run experiments with higher rate limits
- ✅ Access all premium Google AI services
- ✅ Scale your projects beyond free tier limits

**This course uses Vertex AI (built on Google Cloud), so you MUST redeem your credits to play!**

### How to Redeem
Your instructor will email you a coupon code. Follow these steps to activate it:

**Step 1: Navigate to Google Cloud Console**
1. Go to [console.cloud.google.com/edu](https://console.cloud.google.com/edu)
2. Sign in with your Google account

**Step 2: Redeem Your Coupon**
1. Enter your first and last names and verify your email
2. Paste your instructor's coupon code
3. Click **"Accept and continue"**
4. Complete the billing account setup (requires payment profile, but NO credit card is needed for student coupons)

*[INSERT IMAGE: Coupon redemption form]*

**Step 3: Verify Your Credits**
1. Go to **Billing** → **Credits**
2. You should see your credit balance (e.g. $50) applied to a new Billing Account (often named for the course)

*[INSERT IMAGE: Credit balance in GCP console]*

---

## Part 6: Set Up Your Google Cloud Project

### Why do I need a Project?
In Google Cloud, all resources (like the Gemini model) live inside a "Project". The project tracks your files, who has access, and importantly, **billing** (which your credits will cover).

### Step 1: Create a New Project
1. Go to [console.cloud.google.com](https://console.cloud.google.com)
2. Click the **project selector dropdown** (top left, next to "Google Cloud" logo)
3. Click **"New Project"** (top right of the popup window)
4. **Project Name:** `coding-with-ai-winter26` (or similar)
5. **Billing Account:** Ensure it is set to the Billing Account you just created with your credits.
6. Click **Create**

*[INSERT IMAGE: New Project creation screen]*

### Step 2: Enable the Vertex AI API
Your project needs permission to use the AI models.
1. Ensure your new project is selected in the top dropdown.
2. In the search bar at the very top, type: `Vertex AI API`
3. Select **"Vertex AI API"** (Marketplace result)
4. Click **"Enable"**
5. Wait a moment for it to finish.

*[INSERT IMAGE: Enabling Vertex AI API in Marketplace]*

### Step 3: Get Your Project ID (Critical!)
You will need your **Project ID** to configure your notebook. Note that **Project ID** is often different from **Project Name** (it may have numbers added).

1. Click the **Google Cloud Logo** (top left) to go to the Dashboard.
2. Look for the **"Project info"** card.
3. Find **"Project ID"** (e.g., `coding-with-ai-wn26-4123`).
4. **Copy this ID** and save it somewhere accessible (or just remember where to find it).

*[INSERT IMAGE: Dashboard showing Project Info card with ID highlighted]*

---

## Quick Verification Checklist

Before class begins, confirm you have completed:

- [ ] Created or verified GitHub account
- [ ] Accessed the course repository at [github.com/kgweber-cwru/coding-with-ai-wn26](https://github.com/kgweber-cwru/coding-with-ai-wn26)
- [ ] Opened a notebook in Google Colab (Week 1 concepts.ipynb)
- [ ] Saved a copy of a notebook to your Google Drive
- [ ] Connected your Google Drive to Colab using `drive.mount()`
- [ ] Redeemed Google Cloud educational credits using instructor's coupon code
- [ ] Created a new Google Cloud Project with billing linked
- [ ] Enabled the "Vertex AI API" in your project
- [ ] Located your "Project ID" (e.g., `my-project-123`)

---

## Troubleshooting

### "I can't access the GitHub repository"
- **Check:** Are you using the correct link? [github.com/kgweber-cwru/coding-with-ai-wn26](https://github.com/kgweber-cwru/coding-with-ai-wn26)
- **Solution:** The repository is public - no special access required. Try clearing your browser cache and refreshing.

### "I don't see an 'Open in Colab' button on the notebook"
- **Solution:** Use the manual link method (Part 3, Method 2) to open the notebook
- **Or:** Contact your instructor to add the Colab badge to the repository

### "I can't save a copy to my Drive"
- **Check:** Are you logged into your Google account?
- **Check:** Do you have space available in Google Drive?
- **Solution:** Try clearing your browser cache and logging in again

### "When I mount Google Drive, I get a permission error"
- **Solution:** Check that you're using the correct code: `from google.colab import drive` and `drive.mount('/content/drive')`
- **Check:** Did you click "Allow" when the permission dialog appeared?

### "My coupon code isn't working"
- **Check:** Did you copy the code exactly (no extra spaces)?
- **Check:** Has the coupon already been used? Each code is single-use.
- **Solution:** Contact your instructor - they can issue a new code if needed.

### "I can't find my Project ID"
- **Solution:** go to [console.cloud.google.com](https://console.cloud.google.com), make sure your project is selected in the top bar, and check the "Project Info" card on the dashboard.

### "PermissionDenied or 403 Error when running code"
- **Check:** Did you run the authentication cell (`auth.authenticate_user()`)?
- **Check:** Did you enable the **Vertex AI API** in your project? (Part 6, Step 2)
- **Check:** Did you enter the correct **Project ID** when prompted?

---

## Support

**Questions?** Contact your instructor at [instructor-email@cwru.edu]

**Google Colab Help:** [support.google.com/colab](https://support.google.com/colab)

**GitHub Help:** [docs.github.com](https://docs.github.com)

**Google Gemini API Help:**
- Google AI Studio: [ai.google.dev](https://ai.google.dev)
- API Documentation: [ai.google.dev/docs](https://ai.google.dev/docs)
- Gemini Models Guide: [ai.google.dev/models](https://ai.google.dev/models)
- Pricing & Credits: [ai.google.dev/pricing](https://ai.google.dev/pricing)

---

## Welcome! You're Ready!

Once you've completed all steps above, you're set for Day 1. 

**A few final tips:**
- All your work is automatically saved in Google Drive - no need to worry about losing code!
- You can access your notebooks from any computer with a browser
- API keys are securely stored in Colab Secrets - never share them
- If you need help during the seminar, ask your instructor - we're here for you!

**See you in class!**

---

---

# TESTING PROTOCOL FOR INSTRUCTORS

This section helps you verify that the instructions above work correctly from a "fresh start" perspective, even though you have extensive GCP experience.

## Instructor Setup: Simulate a New Student

### Before Testing:
1. **Create a separate Google account** (using an alias email you don't normally use)
2. **Do NOT use your existing GCP account** - this simulates fresh student experience
3. **Clear browser cookies/cache** to avoid auto-login to your main account
4. **Use an incognito/private browser window** for each test

### Testing Protocol (Estimated time: 50-60 minutes)

#### TEST 1: GitHub Access & Colab Opening Flow
**Objective:** Verify students can find course materials and open them in Colab

**Steps:**
1. Open new incognito browser window
2. Go to [github.com](https://github.com) - can you see "Sign up" clearly?
3. Follow the "Create a GitHub Account" section in the guide
   - Time how long GitHub signup takes
   - Document any confusion points
4. Navigate to [github.com/kgweber-cwru/coding-with-ai-wn26](https://github.com/kgweber-cwru/coding-with-ai-wn26)
   - Can you see the repository clearly?
   - Is the folder structure obvious?
   - Can you easily locate "week-1-llm-basics-and-api"?
5. Click on **concepts.ipynb**
   - Can you see the notebook preview in GitHub?
   - Look for the "Open in Colab" badge
   - Does clicking it open the notebook in Colab?
6. If no Colab badge:
   - Try the manual URL method from the guide
   - Does the notebook open successfully?

**Success Criteria:**
- [ ] GitHub access takes <5 minutes total
- [ ] Repository is publicly visible without permission requests
- [ ] week-1-llm-basics-and-api folder is easy to find
- [ ] Colab badge is visible OR manual link method works
- [ ] Notebook opens in Colab without errors
- [ ] All code cells are visible and readable

**Document Issues:**
- Was the Colab badge present in the repository?
- Did the notebook open with all content intact?
- Any cells missing or rendering incorrectly?

---

#### TEST 2: Save Copy to Drive & Access Flow
**Objective:** Verify students can save notebooks to Drive and access them later

**Steps:**
1. **In the opened Colab notebook** (from TEST 1)
2. Look for **File** menu at the top-left
   - Is it clearly visible?
3. Click **File** → **"Save a copy in Drive"**
   - Does the dialog appear?
   - Can you select a location (or accept default)?
   - Does the save succeed?
4. Does a new tab open with your copy?
5. Check the notebook name
   - Does it show "Copy of concepts" or similar?
   - Can you rename it (click filename at top)?
   - Does the rename save?
6. Go to [drive.google.com](https://drive.google.com) in a new tab
   - Log into the same test Google account
   - Navigate to where you saved the notebook
   - Can you see your notebook file?
   - Can you click it and open it again in Colab?

**Success Criteria:**
- [ ] File menu is visible and intuitive
- [ ] "Save a copy in Drive" appears in File menu
- [ ] Save dialog completes successfully
- [ ] New tab opens with your copy
- [ ] Notebook can be renamed from Colab
- [ ] Notebook appears in Google Drive
- [ ] Can re-open the notebook from Drive

**Document Issues:**
- Was the menu structure exactly as shown in guide?
- Did the save complete without errors?
- Could you find the file in Drive?
- Any delay or unexpected behavior?

---

#### TEST 3: Google Drive Connection in Colab
**Objective:** Verify students can mount Drive and access files

**Steps:**
1. **In your saved Colab notebook** (from TEST 2)
2. Create a new code cell (click **+ Code** button)
3. Paste this code:
```python
from google.colab import drive
drive.mount('/content/drive')
```
4. Click the Play button (▶) to run the cell
5. A permission popup should appear
   - Does it appear within 5 seconds?
   - Does it ask for Google Drive permission?
6. Click "Connect to Google Drive"
7. Select your test Google account
8. Click "Allow"
9. Check the output
   - Do you see "Mounted at /content/drive"?
   - Any error messages?
10. Test access to files:
    - In a new code cell, run:
```python
import os
drive_files = os.listdir('/content/drive/My Drive')
print(drive_files[:5])  # Show first 5 files
```
    - Does it list files from your Drive?

**Success Criteria:**
- [ ] Code cell creation is intuitive
- [ ] Permission dialog appears within 5 seconds
- [ ] Mount succeeds (see "Mounted at /content/drive")
- [ ] No authentication errors
- [ ] Can list files from /content/drive/My Drive
- [ ] File paths work correctly

**Document Issues:**
- Did the permission dialog appear?
- Any authentication errors?
- Could Colab access your Drive files?
- Any path confusion?

---

#### TEST 4: Google Cloud Credit Redemption Flow
**Objective:** Verify the coupon redemption process works

**Steps:**
1. **Start with your new test Google account** (from TEST 1)
2. Navigate to [console.cloud.google.com](https://console.cloud.google.com)
   - Are you prompted to sign in?
   - Does the console load fully?
3. Follow the "Redeem Your Educational Coupon" section
   - Look for "Billing" in the left menu
   - Is it immediately visible or does it require scrolling/menu expansion?
   - Can you find "Redeem a coupon"?
4. **Enter your instructor test coupon code**
   - Note: You may need to create a fresh test code or use a duplicate/partner code for this
   - Does the form accept the code?
   - Are error messages clear if you enter an invalid code?
5. Complete the billing account creation
   - What information is required? (name, address, etc.)
   - Is the form intuitive?
   - Are the terms clearly presented?
6. Verify credit appears
   - Go to Billing → Overview
   - Is your credit balance displayed prominently?
   - Does it show credit available?

**Success Criteria:**
- [ ] Google Cloud Console loads without errors
- [ ] "Billing" menu is discoverable
- [ ] Coupon redemption form is easy to find
- [ ] Code entry accepts coupon format correctly
- [ ] Billing account creation is straightforward
- [ ] Credit balance displays accurately after redemption

**Document Issues:**
- Was the Billing menu location accurate in your guide?
- Did any steps require different actions than described?
- Were error messages helpful?

---

#### TEST 5: GCP Project & Vertex API Setup
**Objective:** Verify students can create their project and enable API

**Steps:**
1. **In your test Google account** (with redeemed credits)
2. In Cloud Console, locate the **Project Selector** (top-left)
   - Is it clearly visible?
3. Look for **"New Project"** button
   - Is it obvious in the dropdown?
4. Click "New Project" and enter:
   - **Project Name:** "Coding-with-AI-WN26-Test"
   - **Billing:** Ensure it's linked to the education credits account
5. Click "Create"
   - Does the project initialize successfully?
6. **Enable Vertex AI API:**
   - Search for "Vertex AI API"
   - Click "Enable"
   - Does it finish without error?
7. **Find Project ID:**
   - Go to Dashboard
   - Locate "Project Info" card
   - Confirm you can see "Project ID" distinct from name

**Success Criteria:**
- [ ] Project Selector is intuitive to find and use
- [ ] "New Project" button is clearly visible
- [ ] Project creation completes (linked to credits)
- [ ] Vertex AI API enables successfully
- [ ] Project ID is findable on Dashboard
- [ ] Project is fully functional

**Document Issues:**
- Was the Project Selector location exactly as described?
- Did any unexpected dialogs or confirmations appear?
- Were there any delays or errors?

---

#### TEST 6: End-to-End Workflow (Complete Simulation)
**Objective:** Verify the entire sequence works as described for a brand new student

**Steps:**
1. **Start completely fresh:** Incognito window, new test Google account
2. Open the STUDENT-SETUP-GUIDE.md document
3. Follow EVERY step in order, exactly as written
4. Time how long the complete process takes
5. At each step, note:
   - Is the instruction clear?
   - Is there any ambiguity?
   - Did you need to search for clarification?
   - Are the visual cues (buttons, menus) where the guide says they are?
6. Complete all verification checkboxes

**Success Criteria:**
- [ ] Complete process takes <45 minutes
- [ ] No steps required external research
- [ ] All checkboxes can be marked complete
- [ ] No confusing terminology or jargon
- [ ] Screenshots/diagrams align with actual UI

**Timing Breakdown (expected):**
- GitHub access: 8 minutes
- Colab/Drive setup: 10 minutes
- Credit redemption: 10 minutes
- Project creation & API: 5 minutes
- Verification: 2 minutes
- **Total: ~35-40 minutes**

---

### Issues Log Template

For each issue found, document:

```
**Issue #[number]**
- **Section:** [Which part of guide]
- **Problem:** [What went wrong]
- **Expected:** [What should happen]
- **Actual:** [What actually happened]
- **Screenshot:** [Attach image if applicable]
- **Severity:** [Critical / High / Medium / Low]
- **Fix Required:** [What needs to change in the guide]
```

---

### Final Validation Checklist

After completing all tests, verify:

- [ ] GitHub section: All steps verified, no confusing UI elements
- [ ] GCP console navigation: Menu locations are accurate
- [ ] Coupon redemption: Process works and credit appears
- [ ] Project creation: Students can create projects successfully
- [ ] Vertex AI: API enables without issue
- [ ] Timing: Total setup <45 minutes
- [ ] Clarity: No steps requiring external research
- [ ] Screenshots: All images match actual UI
- [ ] Terminology: All terms defined or self-explanatory
- [ ] Troubleshooting: Covers the issues you found

---

### Pre-Semester Communication

**After running these tests**, send students an update if needed:

> "I've tested all the setup instructions and they work great! Here are a few tips:
> - The whole process takes about 35-40 minutes
> - Make sure you use a regular browser (not private/incognito) so your login stays active
> - Save your coupon code somewhere safe until you redeem it
> - Come to office hours if you hit any snags!"

---

### Version Control

After testing and updating the guide, include this header:

```
**Last Tested:** [Date - e.g., January 18, 2026]
**Tested By:** [Your name]
**Status:** ✅ Verified working / ⚠️ Needs updates
**Next Review:** [Recommended date, e.g., two weeks before next semester]
```

This helps you track when the guide was last validated and know if it needs re-testing before the next cohort.

---

## End of Testing Protocol- **Total: ~30 minutes** (under 45 minute estimate)

---

### Issues Log Template

For each issue found, document:

```
**Issue #[number]**
- **Section:** [Which part of guide]
- **Problem:** [What went wrong]
- **Expected:** [What should happen]
- **Actual:** [What actually happened]
- **Screenshot:** [Attach image if applicable]
- **Severity:** [Critical / High / Medium / Low]
- **Fix Required:** [What needs to change in the guide]
```

---

### Final Validation Checklist

After completing all tests, verify:

- [ ] GitHub section: All steps verified, no confusing UI elements
- [ ] GCP console navigation: Menu locations are accurate
- [ ] Coupon redemption: Process works and credit appears
- [ ] Project creation: Students can create projects successfully
- [ ] Timing: Total setup <45 minutes
- [ ] Clarity: No steps requiring external research
- [ ] Screenshots: All images match actual UI
- [ ] Terminology: All terms defined or self-explanatory
- [ ] Troubleshooting: Covers the issues you found

---

### Pre-Semester Communication

**After running these tests**, send students an update if needed:

> "I've tested all the setup instructions and they work great! Here are a few tips:
> - The whole process takes about 30 minutes
> - Make sure you use a regular browser (not private/incognito) so your login stays active
> - Save your coupon code somewhere safe until you redeem it
> - Come to office hours if you hit any snags!"

---

### Red Flags That Require Guide Updates

If you encounter ANY of these during testing, the guide needs revision:

- ❌ A menu item doesn't appear where described (UI changed)
- ❌ A form field is missing from the guide (incomplete instructions)
- ❌ The process takes >45 minutes (guide needs optimization)
- ❌ Error messages appear that aren't addressed in troubleshooting
- ❌ Screenshots don't match the current UI
- ❌ Students could reasonably get stuck at any step
- ❌ Jargon appears without explanation

---

### Version Control

After testing and updating the guide, include this header:

```
**Last Tested:** [Date - e.g., January 18, 2026]
**Tested By:** [Your name]
**Status:** ✅ Verified working / ⚠️ Needs updates
**Next Review:** [Recommended date, e.g., two weeks before next semester]
```

This helps you track when the guide was last validated and know if it needs re-testing before the next cohort.

---

## End of Testing Protocol
