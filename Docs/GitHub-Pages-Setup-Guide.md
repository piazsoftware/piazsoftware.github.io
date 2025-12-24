# GitHub Pages Setup Guide for AfterVeil Legal Documents

This guide will walk you through setting up GitHub Pages for your AfterVeil legal documents repository.

## Prerequisites

- A GitHub account
- This repository (`piazsoftware.github.io`) already created on GitHub

## Step-by-Step Setup Instructions

### Step 1: Push Your Files to GitHub

1. Open your terminal/command prompt in the project directory
2. Initialize git (if not already done):
   ```bash
   git init
   ```

3. Add all files:
   ```bash
   git add .
   ```

4. Commit the files:
   ```bash
   git commit -m "Initial commit: Add legal documents for AfterVeil"
   ```

5. Add your GitHub repository as remote (replace with your actual repository URL if different):
   ```bash
   git remote add origin https://github.com/piazsoftware/piazsoftware.github.io.git
   ```

6. Push to GitHub:
   ```bash
   git branch -M main
   git push -u origin main
   ```

### Step 2: Enable GitHub Pages

1. Go to your GitHub repository in your web browser:
   `https://github.com/piazsoftware/piazsoftware.github.io`

2. Click on **Settings** (gear icon) in the repository menu

3. Scroll down the left sidebar and click on **Pages**

4. Under **Source**, select:
   - **Branch**: `main`
   - **Folder**: `/ (root)`

5. Click **Save**

6. GitHub will display a message: "Your site is ready to be published at `https://piazsoftware.github.io/`"

### Step 3: Wait for Deployment

- GitHub Pages typically takes 1-5 minutes to deploy your site
- You'll see a green checkmark when it's ready
- You can refresh the Settings > Pages page to check the status

### Step 4: Access Your Site

Once deployed, your legal documents will be available at:

- **Home Page**: `https://piazsoftware.github.io/`
- **Privacy Policy**: `https://piazsoftware.github.io/privacy-policy.html`
- **Terms of Use**: `https://piazsoftware.github.io/terms-of-use.html`

## Using These URLs in Your Game

You can now link to these pages from your game:

### For Unity (C#)
```csharp
Application.OpenURL("https://piazsoftware.github.io/privacy-policy.html");
Application.OpenURL("https://piazsoftware.github.io/terms-of-use.html");
```

### For Unreal Engine (C++)
```cpp
FPlatformProcess::LaunchURL(TEXT("https://piazsoftware.github.io/privacy-policy.html"), nullptr, nullptr);
```

### For Godot (GDScript)
```gdscript
OS.shell_open("https://piazsoftware.github.io/privacy-policy.html")
```

## Updating Content

When you're ready to replace the temporary text:

1. Edit the `privacy-policy.html` and `terms-of-use.html` files locally
2. Commit and push the changes:
   ```bash
   git add .
   git commit -m "Update privacy policy and terms of use"
   git push
   ```
3. GitHub Pages will automatically rebuild and deploy within a few minutes

## Custom Domain (Optional)

If you want to use a custom domain like `legal.piazsoftware.com`:

1. Purchase a domain from a domain registrar
2. In your domain's DNS settings, add a CNAME record pointing to `piazsoftware.github.io`
3. In GitHub repository Settings > Pages, add your custom domain
4. Follow GitHub's instructions for verifying the domain

## Troubleshooting

### Site Not Loading
- Wait 5-10 minutes after enabling GitHub Pages
- Check Settings > Pages for deployment status
- Ensure the repository is public (or you have GitHub Pro for private repos)

### 404 Error
- Verify that `index.html` is in the root directory
- Check that file names match exactly (case-sensitive)
- Clear your browser cache

### Changes Not Appearing
- Wait a few minutes for GitHub Pages to rebuild
- Check the Actions tab for build status
- Try a hard refresh (Ctrl+F5 or Cmd+Shift+R)

## Need Help?

- GitHub Pages Documentation: https://docs.github.com/en/pages
- GitHub Support: https://support.github.com/

---

**Note**: The repository name `piazsoftware.github.io` is a special format for GitHub Pages. This makes your site available at the root domain `https://piazsoftware.github.io/` instead of a subdirectory.

