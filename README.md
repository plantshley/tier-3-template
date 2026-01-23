# Mental Model Webpage Template

This repository serves as a starter template for the **Tier 3: Incorporate into Template** output option described at the [Making Thinking Visual Repo](https://github.com/plantshley/making-thinking-visual.git). It provides a basic HTML/CSS structure that allows you to display your mental model image and description on a live webpage without starting from scratch.

## How to Use This Template

**Do not Clone or Fork this repository directly.**

Instead, use the **Template** feature to create your own independent copy:

1. Click the green **Use this template** button at the top right of the file list.
2. Select **Create a new repository**.
3. Name your repository (e.g., `mental-model-1-webpage`).
4. Ensure visibility is set to **Public** (required for GitHub Pages).
5. Click **Create repository**.

## Project Structure

Once you have your own copy, you will see the following file structure:

- **index.html**: The main page of your website. You will edit this file to add your content.
- **styles.css**: Controls the look and feel (colors, fonts, layout).
- **images/**: A folder where you must save your mental model image file. Contains a placeholder image (`sample-mental-model.svg`) that will be replaced with your own.
- **README.md**: This instruction file.

## Customization Instructions

### 1. Add Your Image

1. Export your mental model as a `.png` or `.jpg`.
2. Save or move the file into the `images/` folder of this repository on your computer.

### 2. Edit the HTML

1. Open `index.html` in VS Code.
2. **Title & Heading:** Update the `<title>` tag and the main `<h1>` header with the name of your assignment.
3. **Image Source:** Find the comment `<!-- INSERT IMAGE HERE -->`. Update the `src` attribute of the `<img>` tag to match your filename (replacing the placeholder).
   - *Example:* `<img src="images/my-diagram.png" alt="Mental Model of Systems">`
   - Don't forget to also update the `alt` text to describe your image!
   - Make sure the file name of your image does NOT contain any spaces:
       + "my-diagram.png" ✅
       + "my diagram.png" ❌
4. **Description:** Update the paragraph text `<p>` to describe your thinking process.

### 3. Customize the Design (Optional)

You can customize the look of your page by editing `styles.css`. You can do this manually or use AI to help you write the code.

**Option A: Manual Changes**

Open styles.css and change the values inside the brackets:

- Change `background-color` in the `body` selector.
- Change font styles in the `h1` or `p` selectors.

**Option B: Using AI Assistance**

If you are not comfortable writing CSS or just want to explore, you can ask GitHub Copilot or another AI assistant to:

- Generate the code for you to paste into your files, OR
- Have it write code directly in your project via Copilot (or other)

### 4. Push: Stage, Commit, and Push your changes

### 5. [Optional] Deploy: See instructions below or [Setting up GitHub Starmap](https://plantshley.github.io/making-thinking-visual/pages/github-pages.html)

### 6. Submit:

1. If you chose to deploy the webpage, submit both the webpage URL and the repository URL.
2. If you did not deploy the webpage, submit a repository URL and a screenshot of the webpage preview.

## [Optional] Github Pages Deployment (Publishing to the Web)

To make your webpage live. (See [Starmap](https://plantshley.github.io/making-thinking-visual/pages/github-pages.html))

1. Commit and Push your changes to GitHub.
2. Go to your repository **Settings** tab.
3. Select **Pages** from the left sidebar.
4. Under **Branch**, select `main` (or `master`) and ensure the folder is set to `/ (root)`.
5. Click **Save**.
6. Wait 1–2 minutes, then refresh the page to see your live URL.
