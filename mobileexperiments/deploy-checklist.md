# Netlify Deployment Checklist

## Files Present ✅
- [x] `index.html` - Main landing page
- [x] `Blood_Rheology/simulation.html` - Blood rheology simulation
- [x] `Diffusion/simulation.html` - Diffusion simulation  
- [x] `Poiseuille_Flow/simulation.html` - Poiseuille flow simulation
- [x] `README.md` - Documentation
- [x] `netlify.toml` - Netlify configuration
- [x] `_redirects` - Redirect rules

## Troubleshooting Steps

### 1. Check Netlify Build Settings
- Ensure **Publish directory** is set to `.` (root)
- Ensure **Build command** is empty (no build needed for static HTML)

### 2. Check Deployment Logs
- Go to your Netlify dashboard
- Check the "Deploys" tab
- Look for any build errors or warnings

### 3. Verify File Structure
Your repository should have this structure:
```
bioflow-sims-main/
├── index.html
├── README.md
├── netlify.toml
├── _redirects
├── Blood_Rheology/
│   └── simulation.html
├── Diffusion/
│   └── simulation.html
└── Poiseuille_Flow/
    └── simulation.html
```

### 4. Test Locally
Run this command to test locally:
```bash
python3 -m http.server 8000
```
Then visit `http://localhost:8000`

### 5. Common Issues
- **404 Error**: Usually means Netlify can't find `index.html`
- **Build Failures**: Check if Netlify is trying to run a build command
- **Redirect Issues**: Ensure `_redirects` or `netlify.toml` is properly configured

### 6. Force Redeploy
- Go to Netlify dashboard
- Click "Trigger deploy" → "Deploy site"
- This will force a fresh deployment

### 7. Check Custom Domain (if applicable)
- Ensure domain settings are correct
- Check DNS settings if using custom domain

## Quick Fixes

### If still getting 404:
1. Add a `public` folder and move all files there
2. Update `netlify.toml`:
```toml
[build]
  publish = "public"
```

### If redirects aren't working:
1. Ensure `_redirects` file has no extra spaces
2. Try using `netlify.toml` instead of `_redirects`

### If build is failing:
1. Remove any build commands from Netlify settings
2. Set build command to empty string
3. Set publish directory to `.` (root) 