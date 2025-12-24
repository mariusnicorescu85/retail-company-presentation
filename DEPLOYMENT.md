# Deploying to Vercel

This guide will help you deploy the Systems Overview Presentation to Vercel.

## Quick Deploy (Recommended)

### Option 1: Using Vercel CLI (Fastest)

1. **Install Vercel CLI** (if not already installed):
   ```bash
   npm install -g vercel
   ```

2. **Login to Vercel**:
   ```bash
   vercel login
   ```

3. **Deploy**:
   ```bash
   vercel
   ```
   
   Follow the prompts:
   - Set up and deploy? **Yes**
   - Which scope? Select your account
   - Link to existing project? **No**
   - Project name? (press Enter for default or type a name)
   - Directory? **./** (current directory)
   - Override settings? **No**

4. **Production deploy**:
   ```bash
   vercel --prod
   ```

### Option 2: Using Vercel Dashboard

1. **Create a Git Repository** (if not already done):
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git remote add origin <your-repo-url>
   git push -u origin main
   ```

2. **Connect to Vercel**:
   - Go to [vercel.com](https://vercel.com)
   - Click "New Project"
   - Import your Git repository
   - Vercel will auto-detect the project

3. **Configure Project**:
   - Framework Preset: **Other**
   - Build Command: (leave empty)
   - Output Directory: **.** (current directory)
   - Install Command: (leave empty)

4. **Deploy**:
   - Click "Deploy"
   - Wait for deployment to complete
   - Your site will be live at `https://your-project.vercel.app`

### Option 3: Drag & Drop (Quick Test)

1. Go to [vercel.com](https://vercel.com)
2. Create a new project
3. Use the "Drag & Drop" option
4. Upload your entire folder (with screenshots folder)
5. Deploy

## Important Files for Vercel

The following files are needed for deployment:

```
/
├── systems_overview_presentation.html  (Main presentation file)
├── screenshots/                        (Screenshot images)
│   ├── stock-dashboard.png
│   ├── hr-onboarding.png
│   ├── customer-support-dashboard.png
│   ├── warranty-form.png
│   └── sales-dashboard.png
├── vercel.json                         (Vercel configuration)
└── package.json                        (Project metadata)
```

## Configuration

The `vercel.json` file configures:
- Routing to serve the HTML file at the root URL
- Cache headers for optimal performance
- Long-term caching for screenshots (immutable)

## After Deployment

Once deployed, your presentation will be available at:
- **Preview/Development**: `https://your-project.vercel.app`
- **Production**: `https://your-project.vercel.app` (or custom domain if configured)

## Custom Domain (Optional)

1. Go to your project settings in Vercel
2. Navigate to "Domains"
3. Add your custom domain
4. Follow DNS configuration instructions

## Troubleshooting

### Screenshots Not Loading

- Ensure the `screenshots/` folder is included in deployment
- Check file paths are correct (case-sensitive)
- Verify image files are not corrupted

### Page Not Found

- Check that `vercel.json` rewrite rules are correct
- Verify `systems_overview_presentation.html` exists
- Check Vercel deployment logs for errors

### Build Errors

- Ensure no build command is set (this is a static site)
- Check that all required files are committed to Git
- Review `.vercelignore` if files are being excluded

## File Structure for Vercel

```
presentation/
├── systems_overview_presentation.html  ← Main file
├── screenshots/                        ← Images folder
│   └── *.png
├── vercel.json                         ← Config (routing)
├── package.json                        ← Metadata
└── DEPLOYMENT.md                       ← This file
```

## Updates

To update the presentation:

1. Make changes to `systems_overview_presentation.html`
2. If using Git:
   ```bash
   git add .
   git commit -m "Update presentation"
   git push
   ```
   Vercel will auto-deploy

3. If using CLI:
   ```bash
   vercel --prod
   ```

## Support

For Vercel-specific issues, check:
- [Vercel Documentation](https://vercel.com/docs)
- [Vercel Support](https://vercel.com/support)

