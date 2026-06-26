# Publish this PUBLIC showcase repo

This is your portfolio. It contains only 3 polished demo tools — safe to be public. Run on your own computer.

> Your **full 19-tool suite** lives in the separate `Solutions_Repo` folder and goes to a **private** repo. Keep them separate: never copy private tools or business/pricing files into this Showcase folder.

## Protect your email (it's public)
Use GitHub's free noreply email so your personal address isn't on every public commit:
1. GitHub → Settings → Emails → tick **"Keep my email addresses private."**
2. Copy the `…@users.noreply.github.com` address it shows.

## Set up and commit
```powershell
cd "$env:USERPROFILE\OneDrive\Desktop\20_AI Solutions for African NGOs\Showcase_Repo"
git init
git branch -M main
git config user.name "<your-name-or-username>"
git config user.email "<your-noreply-email@users.noreply.github.com>"
git add .
git commit -m "Showcase: 3 AI-for-African-NGOs tools (grants, M&E, program delivery)"
```

## Create the public repo and push
1. https://github.com/new
2. Name e.g. `ai-for-african-ngos` (this is the name people will see — make it good)
3. Visibility: **Public**
4. Don't add README/.gitignore/license (you have them)
5. Then:
```powershell
git remote add origin https://github.com/<your-username>/ai-for-african-ngos.git
git push -u origin main
```

## Before you push — check what's going out
```powershell
git ls-files     # read the whole list; only the 3 skills + README/LICENSE/.gitignore should be there
```

## After it's live
- Fill in your name, contact, and `[your email]` placeholders in `README.md` and `LICENSE` first — they currently have brackets.
- Add a repo description + topics: `ngo`, `africa`, `ai`, `claude`, `nonprofit`.
- Pin it on your GitHub profile. This is the link you put on your CV, LinkedIn, and proposals.
