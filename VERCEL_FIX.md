# Fixing 404 Error on Vercel

Your Vercel deployment is returning 404 NOT_FOUND. This typically means Vercel can't find `index.html` or the project isn't configured correctly.

## Quick Fix: Update Vercel Project Settings

Go to your Vercel Dashboard and update these settings:

1. **Go to Project Settings**:
   - Dashboard → Your Project → Settings → General

2. **Update Build & Development Settings**:
   - **Framework Preset**: Select "Other" or "Static Site"
   - **Build Command**: Leave **EMPTY** (this is a static site, no build needed)
   - **Output Directory**: Leave **EMPTY** or set to `.` (current directory)
   - **Install Command**: Leave **EMPTY**
   - **Root Directory**: Leave **EMPTY** (unless your files are in a subdirectory)

3. **Save Settings**

4. **Redeploy**:
   - Go to Deployments tab
   - Click the "..." menu on the latest deployment
   - Select "Redeploy"

## Alternative: Verify Files Are Deployed

Check if `index.html` is actually in your deployment:

1. Go to Vercel Dashboard → Your Project → Deployments
2. Click on the latest deployment
3. Look at the "Source" or "Files" section
4. Verify `index.html` appears in the file list

If `index.html` is missing, it wasn't committed or pushed to Git.

## Verify Git Commit

Make sure `index.html` is committed:

```bash
git status
git ls-files index.html
```

If not committed:
```bash
git add index.html
git commit -m "Add index.html"
git push
```

## Still Getting 404?

If you've updated settings and files are committed, try:

1. **Redeploy from CLI**:
   ```bash
   vercel --prod
   ```

2. **Check deployment logs** in Vercel Dashboard for errors

3. **Try accessing the file directly**:
   - `https://retail-company-presentation.vercel.app/index.html`
   - If this works, the issue is routing configuration

