# Human Dura Rebuttal Analysis

This project contains the analysis code for the Human Dura Rebuttal, formatted as an R Markdown website.

## Project Structure

- `index.Rmd`: The main analysis file (converted from `src/human_dura_rebuttle.R`). This file generates the `index.html` homepage.
- `src/`: Helper scripts (e.g., `global.R`) and original source code.
- `_site.yml`: Configuration for the R Markdown website.

## How to Deploy as a Website

To deploy this analysis as a website using GitHub Pages, follow these steps:

### 1. Prerequisites
Ensure you have the necessary R packages installed (see `src/global.R`) and place your data files (e.g., `39.0_samples_seurat_all.qs`) in the project root directory.

### 2. Render the Website
Open the project in RStudio and run the following command in the R console to generate the HTML file:

```r
rmarkdown::render_site()
```

This will create an `index.html` file and a `site_libs/` directory containing the website assets.

### 3. Deploy to GitHub
1.  Initialize a git repository (if not already done):
    ```bash
    git init
    git add .
    git commit -m "Initial commit"
    ```
2.  Create a new repository on GitHub.
3.  Push your local repository to GitHub:
    ```bash
    git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
    git branch -M main
    git push -u origin main
    ```

### 4. Enable GitHub Pages
1.  Go to your repository on GitHub.
2.  Click on **Settings** > **Pages**.
3.  Under **Source**, select `Deploy from a branch`.
4.  Under **Branch**, select `main` and ensure the folder is set to `/ (root)`.
5.  Click **Save**.

Your website will be live at `https://YOUR_USERNAME.github.io/YOUR_REPO_NAME/`.
