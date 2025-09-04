# PR Preview Setup Guide

This repository includes workflows for deploying PR previews to either Netlify or Vercel. Choose one and follow the setup instructions below.

## Option 1: Netlify (Recommended)

Netlify offers a generous free tier and is easy to set up.

### Setup Steps:

1. **Create a Netlify account** at https://netlify.com

2. **Create a new site**:
   - Go to your Netlify dashboard
   - Click "Add new site" → "Configure manually"
   - Note the Site ID

3. **Get your auth token**:
   - Go to User Settings → Applications → Personal Access Tokens
   - Create a new token and save it

4. **Add GitHub Secrets**:
   - Go to your GitHub repository settings
   - Navigate to Secrets and Variables → Actions
   - Add these secrets:
     - `NETLIFY_AUTH_TOKEN`: Your personal access token
     - `NETLIFY_SITE_ID`: Your site ID

5. **Enable the workflow**:
   - Keep `pr-preview-netlify.yml` 
   - Delete `pr-preview-vercel.yml` if not using Vercel

## Option 2: Vercel

Vercel is also free for open source projects and offers excellent performance.

### Setup Steps:

1. **Create a Vercel account** at https://vercel.com

2. **Install Vercel CLI** locally:
   ```bash
   npm i -g vercel
   ```

3. **Link your project**:
   ```bash
   vercel link
   ```
   This will create a `.vercel` folder with your project settings

4. **Get your tokens**:
   - Create a token at: https://vercel.com/account/tokens
   - Get your Org ID and Project ID from `.vercel/project.json`

5. **Add GitHub Secrets**:
   - Go to your GitHub repository settings
   - Navigate to Secrets and Variables → Actions
   - Add these secrets:
     - `VERCEL_TOKEN`: Your access token
     - `VERCEL_ORG_ID`: Your organization ID
     - `VERCEL_PROJECT_ID`: Your project ID

6. **Enable the workflow**:
   - Keep `pr-preview-vercel.yml`
   - Delete `pr-preview-netlify.yml` if not using Netlify

## Security Benefits

Using Netlify or Vercel for PR previews instead of GitHub Pages provides:

- **Isolation**: PR previews are completely separate from your production site
- **No write access**: PRs cannot modify your main GitHub Pages deployment
- **Automatic cleanup**: Previews are automatically removed after PRs are merged
- **Access control**: You can add password protection if needed (paid feature)

## Choosing Between Services

| Feature | Netlify | Vercel |
|---------|---------|--------|
| Free tier | 100GB bandwidth/month | 100GB bandwidth/month |
| Build minutes | 300 min/month | 6000 min/month |
| Setup complexity | Simple | Moderate |
| Preview URLs | Custom aliases | Automatic unique URLs |
| Comments on PR | ✅ Automatic | ✅ Automatic |

Both services work great for PR previews. Choose based on your preference and existing infrastructure.