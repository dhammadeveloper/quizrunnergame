# Deploy Quiz Runner on Vercel

1. Extract this ZIP.
2. Create a GitHub repository and upload the CONTENTS of the quiz-runner folder. package.json must be at the repository root.
3. Visit https://vercel.com/new and import that repository.
4. Use Framework Preset: Vite, Build Command: npm run build, Output Directory: dist, Install Command: npm ci. These settings are also included in vercel.json.
5. Click Deploy. No API keys or environment variables are required.

Alternative: with Node.js 22 installed, open a terminal inside quiz-runner and run:

```sh
npm install
npm run build
npx vercel --prod
```

Sign in and follow the Vercel prompts. This publishes the game to your Vercel account.

## Included version
44 questions adapted from the supplied Class 6 PT-II question paper. Both the home-screen and gameplay runners face down the track. Progress is saved in each browser; progress from the old website does not automatically transfer to the new domain.

The ZIP contains source code, not node_modules. Vercel installs dependencies during the build. You do not upload the ZIP itself through the Git import workflow; extract it and upload the files to GitHub first.
