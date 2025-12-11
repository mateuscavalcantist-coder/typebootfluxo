# Deploying this project to GitHub + Vercel

This repository contains a pre-built static site inside `dist/public`. Vercel is configured to serve `dist/public` as static assets.

## Steps

1. Initialize a git repo:
```bash
cd repo
git init
git add .
git commit -m "Initial commit - prebuilt dist"
```

2. Create a GitHub repository and push:
```bash
git remote add origin git@github.com:<your-username>/<repo-name>.git
git push -u origin main
```

3. On Vercel:
- Create a new project → Import Git Repository (connect your GitHub)
- Select this repository.
- Vercel will use `vercel.json` which serves `dist/public` as static.
- No build step required.

4. (Optional) If you want a Node server instead of static hosting:
- Replace `vercel.json` with a serverless function in `/api` that serves `dist/public`.
- Let me know if you want that and I will add it.

That's it — your site should be live at `https://<project>.vercel.app`.