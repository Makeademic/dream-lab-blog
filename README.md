# Dream Lab Blog Template

##  https://bit.ly/DreamLabBlog

This repository (aka. a repo; a central storage for your project's files, folders, and version history) has all the files and instructions to build a basic personal website with an about me page, a link to a CV [PDF], and a simple blog with the [Eleventy](https://www.11ty.dev/) site generator (using the [v3.0 release](https://github.com/11ty/eleventy/releases/tag/v3.0.0)).

>I recommend using Google Chrome for this exercise so you can easily use the Developer tools like "View Source" and "Inspect Elements".

## What are GitHub Codespaces and GitHub Pages?

GitHub is a company that was acquired by Microsoft that hosts git (version control) projects online. GitHub created [GitHub Pages](https://pages.github.com/), a way to host static sites for free, usually hosted at https://_username_.github.io/_repository_. This means that they are providing free _hosting_, meaning the server space to hold all your files and a free _domain_, the address/URL where others can navigate to your content. 

More recently, GitHub also developed [GitHub Codespaces](https://github.com/features/codespaces), a staging area that combines the functionality of a file **Explorer**, allowing you to visualize your folder structure, a code **Editor**, allowing you to make updates, a **Source Control**, allowing you to push and pull changes from your local to remote repository, and a **Terminal**, allowing you to run actions like previewing a demo of your site on a locally hosted address.

## Why Use Eleventy and GitHub instead of WordPress?

Eleventy is a static site generator (SSG) while WordPress is a content management system (CMS). While initially building a Wordpress site might seem easier because of its graphical user interface and templates and tutorials, WordPress introduces a lot of vulnerabilities because it dynamically generates content based on user requests and database interactions, while a static site's pages are all pre-generated. WordPress also relies on a lot of plugins that constantly require updating, while static sites are lightweight and have fewer dependencies, so they can be moved more easily. Using Eleventy gives you more control over your site and having a GitHub rather than a WordPress URL gives you more credibility in the coding/digital humanities circles.

## Getting Started

1. [Create a GitHub account](https://github.com/signup) if you do not already have one. (NOTE: You will want to pick a professional username because it will be in all of your URLs)
2. Navigate back to [this repository](https://github.com/Makeademic/dream-lab-blog/) and click the green 🟩 "Use this template" button and then "Create a new repository"
3. Type a name for your new repository (NOTE: lowercase and no spaces is best for URLs with hyphens or underscores separating each word)
4. Select "Public" repository visibility and you only need to include the "main" branch (We will build the gh-pages branch in a later step)
5. Click the green 🟩 "Create repository from template" button

**Review**
So far, what we have done is created a copy of a public project on our individual accounts so that we can edit and make changes to the files

## Setting Up Your Project in GitHub Codespaces

>Typically coders using GitHub use their favorite text editor like [Sublime Text](https://www.sublimetext.com/), [Atom](https://atom-editor.cc/), or [Visual Studio Code](https://code.visualstudio.com/), and then use a graphical user interface (GUI) like [GitHub Desktop](https://github.com/apps/desktop) or their command-line interface (CLI) like **Terminal** to push and pull changes to their project. GitHub created Codespaces to allow you to do both of those things right in the browser without having to download software applications (so you can do all of this on your iPad if you want!)  

1. On your repository's homepage, click the green 🟩 "Code" button and switch from the "Local" to the "Codespaces" tab. Then click the green 🟩 "Create codespace on main" button.
2. This will open up a new tab in your browser and will take some time, so be patient with it. [NOTE: As of authoring this document, GitHub provides 60 free hours of Codespaces every month]
3. You should see the **Explorer** on the left (this helps you see folder hierarchy), the **Editor** on the right (this is where you can edit the code), and the **Terminal** at the bottom (this is where we will provide instructions for building our project). The far left toolbar will let you switch between options: **Explorer**, **Search**, **Source Control**, **Run and Debug**, **Extensions**, and **GitHub**.
4. In the **Explorer** (stacked pages icon), navigate to `_data/metadata.js` and double-click to open the file in the **Editor** space. Change the title, URL (https://username.github.io/repositoryname), description, and author data.
5. In the **Terminal**, install dependencies (the needed files for this version of the project) by copying and pasting the code below and then pressing enter/return.
```
npm install
```
6. You should see new lines of text being generated in the **Terminal**.

## Editing Files in Your Project

### Previewing Changes
1. If you want to see a local test of your site before you put it on the web, copy and paste the following code in the **Terminal**
```
npx @11ty/eleventy --serve
```
2. Command + click on the local link to view a preview of your site in a new browser tab
3. This process will be constantly running, so any changes you make in the editor will populate in the 
> Note: Type Control+C in the **Terminal** to terminate the command if you don't want it running in the background.

### Editing Text
>Your text files will be in the "content" folder, your assets like images and documents will be in the "public" folder, and your styling will be in the "css" folder. Some file extensions you will want to know are: 
>- .html (Hypertext Markup Language (HTML) is the standard markup language for **documents** designed to be displayed in a **web** browser)
>- .css (Cascading Style Sheets (CSS) is a style sheet language used for specifying the presentation and **styling** of a document written in a markup language such as HTML)
>- .js (JavaScript (JS) is the programming language for creating interactive, dynamic websites)
>- .md (Markdown is a lightweight markup language for creating formatted text using a **plain-text** editor)
>- .njk (Nunjucks is a templating language for JavaScript)
>- .svg (Scalable Vector Graphics (SVG) is an XML-based vector graphics format for defining two-dimensional graphics, having support for interactivity and animation)
>- .jpg (jpg or jpeg, short for Joint Photographic Experts Group, is a compressed image format used for photos)
>- .ico (short for icon, this file format is for square icons like the favicon in your browser tab, can be based on a transparent .png (Portable Network Graphics))  

---

1. Navigate in the **Explorer** to `content/index.njk` and double-click to edit the file in the **Editor**
2. Edit line 16 between the opening and closing `<h1>` tags (primary header) to your preferred heading
3. Edit line 32 between the opening and closing `<h2>` tags (secondary header) to your preferred typewriter message
4. You can delete the SVG on lines 17-28 and paste in your own SVG code, or if you have an image file, you can replace it with `<img src="image.jpg" alt="text description of image" width="300px">`  

---

5. Navigate in the **Explorer** to `content/about.md` and double-click to edit the file in the **Editor**
6. Edit lines 7 and 8 between the opening and closing `<p>` tags (paragraph) to your preferred text description
7. Edit lines 16, 17, and 18; 26, 27, and 28; and 36, 37, and 38 with your top 3 research interests and descriptions
8. You can delete line 6 if you do not want to include an image  

---

9. Navigate in the **Explorer** to `content/blog.njk` and double-click to edit the file in the **Editor**
10. Edit line 12 between the opening and closing `<h2>` tags (secondary header) to your preferred blog title  

---

11. Navigate in the **Explorer** to `content/blog/firstpost.md` and double-click to edit the file in the **Editor**
12. On line 2 you can edit the title, line 3 edit the description, line 4 edit the date, and line 5 create any tags
13. On lines 7 and below, delete and replace with your own text
> [Markdown Cheat Sheet](https://www.markdownguide.org/cheat-sheet/)  

### Adding Files

1. Navigate in the **Explorer** to the `content/blog/` folder and select so you are in that folder rather than the root directory.
2. At the top of the **Explorer** menu, select the "New File" button (document with a + sign) and rename to `fifthpost.md`
3. Navigate in the **Explorer** to `content/blog/firstpost.md` and copy and paste everything into your new `fifthpost.md` file
4. Edit the date so that it is later than your fourthpost.md so that it will be located properly in the blog order, and edit the title and description


### Editing Styles

1. Navigate in the **Explorer** to `css/index.css` and double-click to edit the file in the **Editor**
> To find and replace, type Command+F for find, and then click the drop down arrow to the left of "Find" to show the option for "Replace".

#### Colors
>Hexcode is a color system on a scale from 0-9,A-F that designates a color RRGGBB. You can calculate a color using this [HTML Color Picker](https://www.w3schools.com/colors/colors_picker.asp) or you can type in a [HTML color](https://www.w3schools.com/colors/colors_names.asp)

2. Edit line 7 to change the background color, 9 to change the text color, 10 to change the link color, 11 to change the link hover color, and 12 to change the visited link color
3. Edit line 87 to change the text color for h1-h3 headers, line 94 to change the text color for h4-h5 headers, and line 106 for paragraph text color
4. Edit lines 306 and 330 to change the color of the blinking cursor in the typewriter CSS animation
5. Edit line 365 for title class color
6. Edit line 400 for background color of cards on about page  

#### Fonts
7. Edit line 38 to change the base font for the entire site
8. Edit line 88 to change the font for h1-h3 headers
9. Edit line 95 to change the font for h4-h5 headers
10. Edit line 104 to change the font for paragraph text
11. Edit line 116 to change the font for links
12. Edit line 119 to change the [font variant](https://www.w3schools.com/cssref/pr_font_font-variant.php) for links 
13. Edit line 171 to change the font for preformatted code  

14. To add Google Fonts, go to [https://fonts.google.com/](https://fonts.google.com/), browse/search for fonts, select as many fonts as you want, click the blue 🟦 "Get font" button, click the blue 🟦 "<>Get embed code" button, and in the <link> option, copy the code from "Embed code in the <head> of your html"
15. Navigate in the **Explorer** to `_includes/layouts/base.njk`
16. Paste your <links> on lines 10-12  

### Editing Assets
1. Rename the files on your local machine to CV.pdf for your CV and biophoto.jpg for your About photo
2. You can drag-and-drop files into the public folder in **Explorer**, or select the public folder and secondary click and choose the Upload... option

## Push Changes to GitHub and Run Eleventy to Create Site

1. In the toolbar to the left of the **Explorer**, go to **Source Control** (branch icon with 3 circles).
2. Write a short description of the changes you plan to "commit" from this local Codespaces copy of your repository to the remote copy of the repository that is publicly available at github.com/username/repository/
3. Click the blue 🟦 "Commit" button and answer Yes to any pop-up boxes.
4. In the **Terminal**, use the node package manager command npx (Node Package eXecute) to run eleventy, which will convert your markdown and nunjucks files to html files, by copying and pasting the code below and then pressing enter/return.
```
npx @11ty/eleventy
```
5. You should see new lines of text being generated in the **Terminal**. You may need to troubleshoot any errors.



## Deploy to GitHub Pages

1. Exit Codespaces and return to the main branch of your repository at github.com/username/repository.
2. Click on the ".github/workflows/" folder link
3. Click on the "gh-pages.yml.sample" link
4. Select the pencil icon in the toolbar to edit this file
5. At the top in the breadcrumbs (a graphical element showcasing folder hierarchy), edit the title "gh-pages.yml.sample" to "gh-pages.yml" and select the green 🟩 "Commit changes..." button
6. Navigate to Actions and you will see that the gh-pages branch is being created
7. Once the gh-pages branch is finished, navigate to Settings>Pages
8. Change the branch from None to gh-pages and click the "Save" button
9. Navigate back to Actions and you can see your site being built
10. Once you have the green ✅ checkmark, navigate back to Settings>Pages and you should see a link in a message that says "Your site is live at https://username.github.io/repository/"
11. Now that the gh-pages.yml is running, every time you commit a new change to your GitHub repo, it will build and deploy your changes to your gh-pages branch and your github.io site. 

 
### Implementation Notes
- The `public` folder in your input directory will be copied to the output folder (via `addPassthroughCopy` in the `eleventy.config.js` file). This means that anything in your public folder will live in your gh-pages branch after your build completes.
