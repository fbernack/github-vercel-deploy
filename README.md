# Use GitHub Actions to Deploy to Vercel

Angular project with Github Actions for preview and production deployment to [Vercel](https://vercel.com).

🍿 YouTube Tutorial: https://youtu.be/FHVaWZjWec4

## The Pipelines

Have a look at the pipelines in this repository. Both require some environment variables (`VERCEL_TOKEN`, `VERCEL_PROJECT_ID` and `VERCEL_ORG_ID`) which are configured via the GitHub repository settings.

- [preview.yaml](.github/workflows/preview.yaml): testing & preview deployment for all pushes to all branches except `main`
- [production.yaml](.github/workflows/production.yaml): production deployment for all pushes to `main`

## Vercel config

To initially create a Vercel project from your local machine, install Vercel CLI via `npm i -g vercel`, login with `vercel login` and then run `vercel link`. This will create a project in the Vercel cloud and furthermore it will create a subfolder `.vercel` in your project where you can find the `projectId` and the `orgId` which you need to run the pipelines. Furthermore you need a API acess token. You can get this directly [from Vercel](https://vercel.com/account/tokens).
