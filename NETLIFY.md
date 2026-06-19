Netlify deployment instructions

1. Create a free Netlify account at https://app.netlify.com/
2. In Netlify, choose "New site from Git" and connect your GitHub repository, or use the **Continuous Deployment** option.
3. If you prefer CI-based deploy, add these repository secrets in GitHub Settings → Secrets:
   - `NETLIFY_AUTH_TOKEN` — a personal access token from Netlify (User settings → Applications → Personal access tokens).
   - `NETLIFY_SITE_ID` — your Netlify site ID (found in Site settings → Site information).
4. The repository includes a GitHub Actions workflow at `.github/workflows/deploy_netlify.yml` that runs on push to `main` and uses those secrets to deploy automatically.
5. To deploy manually with the Netlify CLI:

```bash
# install netlify-cli
npm install -g netlify-cli

# login (opens browser)
netlify login

# deploy a draft (interactive)
netlify deploy --dir=.

# deploy to production (requires linked site or --site)
netlify deploy --dir=. --prod --site <YOUR_SITE_ID>
```

If you need help creating the Netlify token or site ID, tell me and I can guide you step-by-step.
