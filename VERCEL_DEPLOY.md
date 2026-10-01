# Deploy JSP Web Lab to Vercel

This project is configured as a Vite SPA for Vercel.

## Vercel settings
- Framework Preset: Vite
- Install Command: `npm install` (default is fine)
- Build Command: `npm run build`
- Output Directory: `dist`

## Important: Base44 backend
The exported site still uses Base44 for the contact enquiry entity and authentication. In Vercel, add the same Base44 values used by the exported app under Project > Settings > Environment Variables:

- `VITE_BASE44_APP_ID`
- `VITE_BASE44_APP_BASE_URL`
- `VITE_BASE44_FUNCTIONS_VERSION` (only if required by your Base44 project)

Do not put private API keys in VITE_ variables because Vite exposes them to the browser.

After deploying, test the Contact form and any Login/Register features before pointing your custom domain at Vercel.
