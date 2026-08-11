# Vercel Deployment Instructions

You have successfully prepared your project for deployment!

## Step 1: Upload to GitHub
1. Create a **NEW** empty repository on GitHub.
2. Go to the new repository page and click **uploading an existing file**.
3. Open this `weblive` folder on your computer.
4. Drag and drop **EVERYTHING** inside this folder directly into the GitHub upload box.
   *(This ensures the folders like `api`, `server`, `dashboard`, and `website` are preserved exactly as they should be.)*
5. Click **Commit changes**.

## Step 2: Configure Vercel
1. Go to your Vercel Dashboard and click **Add New... -> Project**.
2. Import the new GitHub repository you just created.
3. **DO NOT change the Framework Preset or Build Command**. Leave everything as default.
4. Open the **Environment Variables** section and add the following keys with your actual values:
   - `DATABASE_URL` (Your Prisma/Postgres connection string)
   - `DIRECT_URL` (Your Prisma/Postgres direct connection string)
   - `SHIPCORRECT_API_KEY` (Your Shiprocket/ShipCorrect API key)
   - `ADMIN_EMAIL` (Your login email for the dashboard)
   - `ADMIN_PASSWORD` (Your login password for the dashboard)
   - `MERCHANT_UPI_ID` (e.g., `yourname@bank`)
   - `MERCHANT_NAME` (e.g., `Happy Hair`)
   - `ALLOWED_ORIGINS` (e.g., `https://your-vercel-domain.vercel.app`)

5. Click **Deploy**.

That's it! Vercel will now properly build your backend and frontend using the correct structure.
