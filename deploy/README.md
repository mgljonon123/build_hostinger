# Hostinger Deployment Instructions

## Issue: "Unsupported framework or invalid project structure"

Hostinger sometimes has issues with Vite/React builds. Here are the solutions:

### Option 1: Manual File Upload
1. Upload all files from the `deploy/` folder to Hostinger's public_html
2. Ensure `.htaccess` is uploaded
3. Set environment variables in Hostinger control panel

### Option 2: Use Simple Structure
1. Upload only `index.html`, `assets/` folder, and `.htaccess`
2. Remove `package.json` - it's not needed for static sites
3. Ensure all paths are relative (./assets/)

### Option 3: Alternative Deployment
If Hostinger continues to reject the build, consider:
- Using Netlify, Vercel, or GitHub Pages
- Using Hostinger VPS instead of shared hosting
- Converting to a simple HTML/CSS/JS structure

### Files to Upload:
- index.html
- .htaccess  
- assets/ (entire folder)
- vite.svg

### Environment Variables Needed:
- VITE_SUPABASE_URL
- VITE_SUPABASE_ANON_KEY
