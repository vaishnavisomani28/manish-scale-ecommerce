# Deploy to Vercel

Your frontend (Vite + React) is ready to deploy on Vercel. Follow these steps.

## 1. Push the latest code (including `app/vercel.json`)

```bash
git add app/vercel.json DEPLOY_VERCEL.md
git commit -m "Add Vercel config and deploy guide"
git push origin main
```

## 2. Deploy on Vercel

1. Go to **[vercel.com](https://vercel.com)** and sign in (use **Continue with GitHub**).
2. Click **Add New…** → **Project**.
3. **Import** your repo: `vaishnavisomani28/manish-scale-ecommerce`.
4. **Important:** set **Root Directory** to `app`:
   - Click **Edit** next to “Root Directory”.
   - Enter `app` and confirm.
5. Vercel will detect **Vite** and set:
   - **Build Command:** `npm run build`
   - **Output Directory:** `dist`
6. Click **Deploy**.

After the build finishes, you’ll get a URL like `https://your-project.vercel.app`.

## 3. Optional: custom domain

In the Vercel project → **Settings** → **Domains**, add your own domain and follow the DNS instructions.

---

**Note:** Only the **frontend** (in `app/`) is deployed. The small Express backend in `backend/` is not used by the app right now. If you add API calls later, you can either host the backend elsewhere (e.g. Railway, Render) or move that logic into Vercel Serverless Functions.
