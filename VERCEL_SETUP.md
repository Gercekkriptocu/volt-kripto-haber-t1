# Vercel Deployment Setup

## Environment Variables

After deploying to Vercel, you need to add the following environment variables in your Vercel Dashboard:

### Required Variables

1. Go to your Vercel project dashboard
2. Navigate to **Settings** → **Environment Variables**
3. Add the following variables:

#### OPENAI_API_KEY (Required)
- **Name:** `OPENAI_API_KEY`
- **Value:** Your OpenAI API key (starts with `sk-proj-...`)
- **Environment:** Production, Preview, Development
- **Description:** Used for translating crypto news from English to Turkish

**How to get it:**
1. Go to https://platform.openai.com/api-keys
2. Click "Create new secret key"
3. Copy the key and paste it in Vercel

#### DEEPL_API_KEY (Optional, but recommended)
- **Name:** `DEEPL_API_KEY`
- **Value:** Your DeepL API key
- **Environment:** Production, Preview, Development
- **Description:** Provides better quality Turkish translations (used as primary translator if available)

**How to get it:**
1. Go to https://www.deepl.com/pro-api
2. Sign up for free or paid plan
3. Copy your API key from the account page

## After Adding Environment Variables

1. Click **Save** for each variable
2. Go to **Deployments** tab
3. Click **...** menu on the latest deployment
4. Select **Redeploy**
5. Wait for the new build to complete

Your VOLT crypto news app will now work with Turkish translations! 🎉

## Testing Translation

After deployment with environment variables:
1. Open your deployed app
2. Wait for news to load
3. Translations should appear in Turkish automatically
4. Check browser console for any translation errors

## Troubleshooting

### "Translation failed" errors
- Check if OPENAI_API_KEY is correctly set in Vercel
- Make sure the key starts with `sk-proj-` or `sk-`
- Verify the key is active on OpenAI platform

### News showing in English
- Environment variables may not be loaded yet
- Try redeploying the project
- Check Vercel build logs for errors

### Need Help?
Open an issue on GitHub or check Vercel's deployment logs for detailed error messages.
