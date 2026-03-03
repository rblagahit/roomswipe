# How to Push to GitHub

Your RoomSwipe files have been created locally, but we need to authenticate with GitHub to push them.

## Option 1: Using Personal Access Token (Recommended)

1. Go to https://github.com/settings/tokens
2. Click "Generate new token" → "Generate new token (classic)"
3. Give it a name like "RoomSwipe"
4. Select scopes: **repo** (full control of private repositories)
5. Click "Generate token" and **copy the token**

6. In your terminal (in the roomswipe folder), run:
```powershell
git push -u origin main
```

7. When prompted:
   - Username: rblagahit
   - Password: [paste your token here]

## Option 2: Using GitHub CLI

1. Install GitHub CLI (gh):
```powershell
winget install --id GitHub.cli
```

2. Authenticate:
```powershell
gh auth login
```

3. Follow the prompts to authenticate via browser

4. Then push:
```powershell
git push -u origin main
```

## Option 3: Use GitHub Desktop

1. Download and install GitHub Desktop: https://desktop.github.com/
2. Sign in with your GitHub account
3. Add the existing repository: `C:\Users\rblagahit\roomswipe`
4. Publish the repository to GitHub

## Verify the Push

After successful push, your files will be visible at:
https://github.com/rblagahit/roomswipe

## Enable GitHub Pages

Once pushed, you can host it for free:

1. Go to https://github.com/rblagahit/roomswipe/settings/pages
2. Under "Source", select **main** branch
3. Click Save
4. Your site will be live at: **https://rblagahit.github.io/roomswipe/**

---

All files are ready in: `C:\Users\rblagahit\roomswipe\`
- index.html (main app)
- README.md (project documentation)
- PUSH_INSTRUCTIONS.md (this file)
