# Vercel Settings Checklist - Fix 404 Error

Since `/index.html` also returns 404, Vercel isn't finding your files. This means the project settings are incorrect.

## ⚠️ CRITICAL: Update Vercel Project Settings

Go to: **Vercel Dashboard → Your Project → Settings → General**

### Required Settings:

1. **Framework Preset**
   - ❌ NOT: Next.js, React, Vue, etc.
   - ✅ Set to: **"Other"** or **"Static Site"**

2. **Build Command**
   - ❌ NOT: Any build command
   - ✅ Set to: **EMPTY** (leave blank)

3. **Output Directory**
   - ❌ NOT: `.next`, `dist`, `build`, `out`, etc.
   - ✅ Set to: **EMPTY** or **`.`** (period/dot)

4. **Install Command**
   - ✅ Set to: **EMPTY** (leave blank)

5. **Root Directory**
   - ✅ Set to: **EMPTY** (unless files are in a subdirectory)

6. **Development Command**
   - ✅ Can leave as default or empty

### After Updating Settings:

1. **Click "Save"**
2. Go to **Deployments** tab
3. Find the latest deployment
4. Click **"..."** → **"Redeploy"**
5. Wait for deployment to complete

## Verify Deployment Contains Files

After redeploying, check the deployment:

1. Click on the deployment
2. Look for **"Source"** or **"Files"** section
3. Verify you see:
   - `index.html`
   - `vercel.json`
   - `screenshots/` folder

If files are missing, they weren't committed to Git.

## Alternative: Force Redeploy via CLI

If dashboard settings don't work:

```bash
# Make sure you're logged in
vercel login

# Link to your project (if not already linked)
vercel link

# Deploy with explicit settings
vercel --prod
```

## Still Not Working?

If after updating settings it still 404s:

1. **Check Deployment Logs**:
   - Vercel Dashboard → Deployment → Logs
   - Look for errors about missing files or build failures

2. **Verify Git Repository**:
   ```bash
   git ls-files index.html vercel.json
   ```
   Should show both files

3. **Check if build is running**:
   - If you see build logs, that's the problem
   - Static sites shouldn't have builds
   - Clear the Build Command in settings

4. **Try removing vercel.json temporarily**:
   - Rename `vercel.json` to `vercel.json.backup`
   - Commit and push
   - See if it works without vercel.json
   - If yes, the issue is in vercel.json syntax

## Quick Test

After fixing settings, try:
- `https://retail-company-presentation.vercel.app/`
- `https://retail-company-presentation.vercel.app/index.html`

Both should work.

