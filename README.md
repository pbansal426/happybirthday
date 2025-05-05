# Personal Portfolio Template

Welcome! This is a simple and modern personal portfolio website template designed for you to customize and showcase your skills, projects, resume, and contact information.

No coding experience? No problem. This guide is designed to walk you through every step clearly and simply.

---

## 1. Getting Started: Create a GitHub Account

If you don't already have one, you'll need a free GitHub account. This is where your website code will live and how you'll publish it online.

* Go to [https://github.com](https://github.com) and sign up.
* **Tip:** Choose a username you like! It will be part of your portfolio's web address (URL), so something professional or memorable is a good idea (e.g., `yourname`, `yourname-codes`, `johndoe-portfolio`).

---

## 2. Getting the Template Files

You need to get a copy of this template's code into your own GitHub account.

### Step 2.1: Fork the Repository
* Click the "**Fork**" button at the top-right corner of this page on GitHub.
* This creates a complete copy of the template repository under *your* GitHub account. Now you can edit it freely.

### Step 2.2: Choose Your Editing Method

#### Option A: Use GitHub Codespaces (Easiest - Works Directly in Your Browser)
1.  On *your forked repository page* on GitHub, click the green "**<> Code**" button.
2.  Go to the "**Codespaces**" tab.
3.  Click "**Create codespace on main**".
4.  Wait a moment while GitHub prepares a complete editing environment for you in your browser. You'll see the project files on the left and an editor area.

#### Option B: Edit Locally on Your Computer
1.  On *your forked repository page* on GitHub, click the green "**<> Code**" button.
2.  Go to the "**Local**" tab.
3.  Click "**Download ZIP**".
4.  Find the downloaded ZIP file on your computer and extract it (unzip it).
5.  You'll need a text editor. Simple ones like Notepad (Windows) or TextEdit (Mac) work, but we recommend **Visual Studio Code** (free, powerful, works on Windows/Mac/Linux - download from [https://code.visualstudio.com/](https://code.visualstudio.com/)).
6.  Open the extracted folder in your text editor (In VS Code: File -> Open Folder).

---

## 3. Previewing Your Website as You Edit

It's important to see how your changes look! Here are ways to preview your `index.html` file:

* **Simple Double-Click:**
    * Navigate to the folder where you saved the files.
    * Double-click the `index.html` file. It should open in your web browser.
    * **Note:** This is quick but sometimes doesn't perfectly reflect the final online version, especially if more complex features are added later. After making changes in your editor, *save the file* and *refresh the browser tab* to see the update.

* **Using Live Server (Recommended for VS Code or Codespaces):**
    * This tool automatically refreshes your browser preview whenever you save a file, making editing much faster.
    * **In Visual Studio Code (Local):**
        1.  Go to the Extensions view (click the square blocks icon on the left sidebar).
        2.  Search for "Live Server".
        3.  Install the one by Ritwick Dey.
        4.  Once installed, go back to your file explorer view (top icon on the left sidebar).
        5.  Right-click on the `index.html` file.
        6.  Choose "**Open with Live Server**". A new browser tab will open with a live preview.
    * **In GitHub Codespaces:**
        1.  Codespaces often prompts you automatically when it detects you're working on a web page. Look for a pop-up notification asking if you want to open the page in a browser.
        2.  Alternatively, go to the "**Ports**" tab (usually at the bottom panel or find it via the Command Palette: Ctrl+Shift+P -> "Ports: Focus on Ports View").
        3.  You should see an entry for your web server (often on port 5500 if using Live Server extension, or another port). Click the "Open in Browser" (globe) icon next to the Local Address.

---

## 4. Editing Your Portfolio Content (`index.html`)

Now it's time to personalize the website.

* Open the file named `index.html` in your editor (Codespaces or your local text editor).
* Carefully read through the file. You will see text like `[YOUR_FULL_NAME]` or `[PROJECT_DESCRIPTION]`.
* Replace **all** text enclosed in `[SQUARE BRACKETS]` with your actual information.
    * Example: Replace `[YOUR_FULL_NAME]` with `Jane Doe`.

### 🔹 Managing Assets (Resume, Profile Picture, Project Images)

The `assets/` folder contains files used by your site.

1.  **Delete Placeholders:** Go into the `assets/` folder (and its subfolders like `assets/images/`). Delete any placeholder files you see (e.g., `placeholder_resume.pdf`, `placeholder_profile.jpg`, example project images).
2.  **Upload Your Resume:**
    * Rename your resume PDF file to a simple format, like `YourName_Resume.pdf` (e.g., `JaneDoe_Resume.pdf`).
    * Place this PDF file directly inside the `assets/` folder.
    * In `index.html`, find the link for the resume (it might look like `<a href="assets/[RESUME_FILE_NAME]">...</a>`) and make sure the `href` value matches your PDF file name exactly: `href="assets/JaneDoe_Resume.pdf"`.
3.  **Upload Your Profile Picture:**
    * Save your profile picture (e.g., a `.jpg`, `.png`, or `.webp` file) directly inside the `assets/` folder. Keep the filename simple (e.g., `profile_picture.jpg`).
    * In `index.html`, find the profile image tag (`<img ...>`). Update the `src` attribute to point to your image file: `<img src="assets/profile_picture.jpg" alt="Profile Image" />`.
4.  **Add Project Images:**
    * For each project, save a relevant image (e.g., a screenshot) inside the `assets/images/` folder. Use clear filenames (e.g., `project1_screenshot.png`).
    * In `index.html`, within each project's section, update the `<img>` tag's `src` attribute to point to the correct image in the `assets/images/` folder (e.g., `src="assets/images/project1_screenshot.png"`).

### 🔹 Adding Projects

* Find the section in `index.html` for projects. You'll see blocks of code for each project card.
* To add a new project, copy an entire existing project block (usually starting with something like `<div class="project-card">` and ending with `</div>`) and paste it below the others.
* Update the pasted block with your new project's details:
    * `[PROJECT_NAME]`
    * `[PROJECT_DESCRIPTION]`
    * `[GITHUB_LINK]` (Link to your project's code on GitHub, if available)
    * Update the image `src` as described above.

### 🔹 Adding Skills Icons

* Find the Skills section in `index.html`.
* **Option 1: FontAwesome Icons (Easy for common tech)**
    1.  Go to [https://fontawesome.com/search](https://fontawesome.com/search).
    2.  Search for a skill (e.g., "Python", "JavaScript", "HTML5").
    3.  Click the icon you want.
    4.  Copy the HTML code snippet provided (it usually looks like `<i class="fa-brands fa-python"></i>`).
    5.  Paste this snippet where you want the icon to appear in your Skills list in `index.html`.
* **Option 2: SVG Icons (For specific logos/graphics)**
    1.  Find an SVG icon (e.g., from [https://www.svgrepo.com](https://www.svgrepo.com)). Download the `.svg` file.
    2.  Place the downloaded `.svg` file inside the `assets/images/svg/` folder.
    3.  In `index.html`, use an `<img>` tag like this, replacing the `src` with your filename:
        `<img src="assets/images/svg/your-icon-name.svg" alt="Skill Icon" class="custom-icon">` (The `custom-icon` class might be needed for styling - check `styles.css`).

---

## 5. Customizing the Look and Feel (`styles.css`)

The file `styles.css` controls the visual appearance of your website – colors, fonts, spacing, layout, etc.

* Open `styles.css` in your editor.
* You can browse the file to see selectors (like `body`, `h1`, `.project-card`) and their CSS rules (like `background-color: #FFFFFF;` or `font-family: 'Arial', sans-serif;`).
* **Making Changes:**
    * To change colors, look for properties like `background-color`, `color` (for text), `border-color`. You can use color names (`red`, `blue`), hex codes (`#FF5733`), or RGB values (`rgb(255, 87, 51)`).
    * To change fonts, look for `font-family`.
    * Save the `styles.css` file and refresh your browser preview (or Live Server will do it automatically) to see the effects.

* **Need Help with CSS? Use AI!**
    * CSS can be tricky if you're new to it. Don't hesitate to use AI assistants like ChatGPT or Google Gemini.
    * **How:** Copy a section of your `styles.css` code (or the whole file) and paste it into the AI chat. Then, describe the change you want in plain English.
    * **Example Prompts:**
        * "Here is my CSS code. Can you change the main background color to a dark grey (#333333) and the main text color to white (#FFFFFF)?"
        * "How can I make the project titles bigger in this CSS?"
        * "Make the borders around the project cards thicker and dashed."
    * The AI can provide you with the exact CSS code changes. Copy the updated code back into your `styles.css` file.

---

## 6. Adding a Contact Form (Using Google Forms)

This template includes a section for a contact form. Using Google Forms is a free and easy way to collect messages.

1.  Go to [https://forms.google.com](https://forms.google.com) and log in with your Google account.
2.  Create a **New Form**.
3.  Add fields for:
    * Name (Short answer)
    * Email (Short answer - consider enabling email collection in settings)
    * Message (Paragraph)
4.  Once your form is ready, click the "**Send**" button (top right).
5.  In the "Send form" popup, click the "**<> Embed HTML**" tab (it's the third icon).
6.  You'll see HTML code starting with `<iframe ...`. Click the "**Copy**" button.
7.  Go back to your `index.html` file in your editor.
8.  Find the Contact section. Look for a comment like: ``.
9.  **Delete** any existing placeholder `<iframe...>` tag if there is one there.
10. **Paste** the code you copied from Google Forms directly below that comment.

### Viewing Form Submissions
* Go back to your form on Google Forms.
* Click the "**Responses**" tab at the top.
* You can view responses directly here, or click the green **Sheets icon** ("Link to Sheets") to create/view a spreadsheet that collects all submissions automatically.

---

## 7. Publishing Your Website with GitHub Pages

Now, let's make your portfolio live on the internet! GitHub Pages is a free hosting service provided by GitHub.

### Understanding Commits and Pushing
Before publishing, you need to save your changes *to GitHub*. In the world of `git` (the system GitHub uses), this involves two steps:

1.  **Commit:** Think of this as taking a snapshot of your changes. You add a brief message describing what you changed (e.g., "Updated profile picture", "Added project details").
2.  **Push:** This sends your saved commits (snapshots) from your editing environment (Codespaces or your local computer) up to your main repository on GitHub.com.

**How to Commit and Push:**

* **In GitHub Codespaces:**
    1.  Look for the **Source Control** icon on the left sidebar (it usually looks like three dots connected by lines). Click it.
    2.  You'll see a list of files you've changed.
    3.  In the "Message" box at the top, type a brief description of your changes (e.g., "Customize portfolio content").
    4.  Click the **Commit** button (or sometimes a checkmark icon). You might be asked to "stage" changes first - if so, click the '+' icon next to "Changes" or the "Stage All Changes" button.
    5.  After committing, you'll often see a button saying "**Sync Changes**" or "**Push**". Click this to send your changes to GitHub.
* **Locally (If you downloaded the ZIP):** This is more complex and usually involves using `git` commands in a terminal or a desktop app like GitHub Desktop. *For beginners, using Codespaces is highly recommended to simplify this process.*

**Key Point:** Every time you make changes, **commit** them with a message and **push** them to GitHub. This updates the code stored on GitHub, which is necessary for GitHub Pages to show the latest version.

### Publishing Steps

1.  Make sure you have **committed and pushed** all your latest changes to your repository on GitHub.com.
2.  Go to your forked repository page on GitHub (`https://github.com/your-username/repo-name`).
3.  Click the "**Settings**" tab (near the top right of the repo page).
4.  In the left sidebar menu, click on "**Pages**".
5.  Under the "**Build and deployment**" section:
    * For "**Source**", make sure "**Deploy from a branch**" is selected.
    * Under "**Branch**", select the `main` branch (or `master` if that's your default). Keep the folder as `/ (root)`.
    * Click "**Save**".
6.  **Wait a few minutes.** GitHub Pages needs a little time to build and deploy your site. The page might show a message indicating the progress.
7.  Once it's ready, the **Pages** settings page will display the live URL at the top, usually in a green box. It will look like:

    `https://your-username.github.io/your-repo-name/`

    **Special Tip:** If you want your *main* portfolio website to be at the simplest URL (`https://your-username.github.io/`), you need to name your repository *exactly* `your-username.github.io` (replace `your-username` with your actual GitHub username). If you do this, the deployment steps are the same, but the final URL won't have the repository name at the end.

### Automatic Updates
Once GitHub Pages is set up, **every time you commit and push changes** to your `main` branch, GitHub Pages will automatically rebuild and update your live website within a minute or two! Just remember to commit and push after making edits.

---

## 8. Leveraging AI for Assistance

Don't feel stuck! Modern AI assistants are incredibly helpful for tasks like this, even if you don't know coding.

* **Tools:** Use assistants like **ChatGPT**, **Google Gemini**, or **Microsoft Copilot**.
* **How to Ask:**
    * **Be specific:** Instead of "Fix my website," describe the problem: "My profile picture isn't showing up. Here is the HTML code I'm using: `<img src='assets/photo.jpg'>`"
    * **Provide Context:** Copy and paste the relevant code snippet (`index.html` section, `styles.css` rule) into the chat. (You can paste the entire file too!)
    * **Describe Your Goal:** Explain what you *want* to achieve. "I want to add a new section between 'About Me' and 'Projects' to list my certifications." or "How can I change the font for all the headings?"
    * **Ask for Explanations:** If the AI gives you code you don't understand, ask: "Can you explain what this CSS code does?"

You can ask AI to help write content, debug issues, explain concepts, or even generate code snippets for new features.

---

## 9. Need More Help?

* **AI First:** Try asking an AI assistant as described above. It's often the fastest way to get unstuck.
* **Official GitHub Pages Docs:** For publishing issues, visit [https://docs.github.com/en/pages](https://docs.github.com/en/pages).
* **Template Specific Question?** If you think there's an issue with the template itself or the instructions are unclear, you can use this contact form: [https://forms.gle/tSx8kLA9jDUL7TNNA](https://forms.gle/tSx8kLA9jDUL7TNNA) (Please try AI and GitHub Docs first!)

---

## 10. Quick Checklist

* [ ] Created a GitHub account.
* [ ] Forked the repository to your account.
* [ ] Chose an editing method (Codespaces or Local).
* [ ] Know how to preview changes (Double-click or Live Server).
* [ ] Deleted placeholder files from `assets/`.
* [ ] Replaced all `[PLACEHOLDER]` text in `index.html` with your info.
* [ ] Uploaded your profile picture and resume to `assets/` and updated links in `index.html`.
* [ ] Added your projects (text and images) and updated `index.html`.
* [ ] Added your skills icons to `index.html`.
* [ ] Customized `styles.css` (optionally using AI help).
* [ ] Created a Google Form, copied the **Embed HTML**, and pasted it into `index.html`.
* [ ] Committed and pushed all changes to your GitHub repository.
* [ ] Configured and deployed website using GitHub Pages under Settings -> Pages.
* [ ] Checked your live website URL!

You’re done! Your personal portfolio is now live and ready to share. Remember to push updates whenever you make changes.