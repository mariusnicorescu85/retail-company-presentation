# Troubleshooting GitHub/Vercel Deployment Failures

If you're seeing a failure in GitHub after committing, here are the most common issues and solutions:

## Common Issues

### 1. **Vercel Deployment Failure**

If Vercel is connected to your GitHub repo, it will auto-deploy on commits. Common failures:

**Issue**: Build fails or deployment returns 404
**Solution**: 
- Check Vercel dashboard for deployment logs
- Ensure `index.html` is in the root directory
- Verify `vercel.json` syntax is correct
- Make sure `screenshots/` folder is included in the commit

### 2. **Missing Files in Git**

**Check if files are committed:**
```bash
git status
git ls-files | grep -E "(index.html|vercel.json|screenshots)"
```

**If files are missing, add them:**
```bash
git add index.html vercel.json screenshots/
git commit -m "Add missing deployment files"
git push
```

### 3. **Screenshot Files Too Large**

If screenshot files are very large (> 5MB each), they might cause issues:
- Optimize images before committing
- Check `.gitignore` isn't excluding them

### 4. **JSON Syntax Error**

**Validate vercel.json:**
```bash
node -e "JSON.parse(require('fs').readFileSync('vercel.json', 'utf8')); console.log('Valid')"
```

## How to Check Vercel Deployment Status

1. Go to [vercel.com/dashboard](https://vercel.com/dashboard)
2. Find your project
3. Click on the deployment that failed
4. Check the "Logs" or "Build Logs" section for error details

## Quick Fixes

### Fix 1: Re-deploy manually
```bash
vercel --prod
```

### Fix 2: Check Vercel project settings
- Framework Preset: **Other**
- Build Command: (empty)
- Output Directory: `.` or leave empty
- Install Command: (empty)

### Fix 3: Verify file structure
Your repo should have:
```
/
├── index.html                    ← Must exist
├── systems_overview_presentation.html
├── vercel.json                   ← Must exist
├── package.json                  ← Optional but recommended
├── screenshots/
│   ├── stock-dashboard.png
│   ├── hr-onboarding.png
│   ├── customer-support-dashboard.png
│   ├── warranty-form.png
│   └── sales-dashboard.png
└── (other files...)
```

## Getting Error Details from GitHub

1. Go to your GitHub repository
2. Click on the failed check (red X or yellow dot)
3. Click "Details" to see the full error log
4. Look for specific error messages

## Getting Error Details from Vercel

1. Go to Vercel dashboard
2. Click on your project
3. Go to "Deployments" tab
4. Click on the failed deployment
5. Check the "Logs" section

## If All Else Fails

1. **Disconnect and reconnect Vercel to GitHub:**
   - Vercel Dashboard → Project Settings → Git
   - Disconnect repository
   - Reconnect and redeploy

2. **Deploy directly via Vercel CLI:**
   ```bash
   vercel --prod
   ```

3. **Check file permissions:**
   - Ensure all files are readable
   - Check that screenshots folder is included

## Common Error Messages

- **"File not found"** → `index.html` missing or not in root
- **"Build failed"** → Check vercel.json syntax
- **"404 NOT_FOUND"** → Wrong routing configuration
- **"Module not found"** → Usually not applicable for static sites

## Need More Help?

Check the deployment logs in:
- GitHub: Repository → Actions tab
- Vercel: Dashboard → Project → Deployments → Failed deployment → Logs

