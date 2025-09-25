# Astro + Vercel Starter

This repository is a minimal Astro project configured to deploy to [Vercel](https://vercel.com/). Astro ships zero JavaScript by default, so you can launch a fast, content-driven site today and progressively add Vue (or any other framework) components later without rewriting your pages.

## Getting started

```bash
npm install
npm run dev
```

Visit `http://localhost:4321` to view the site locally.

## Deploying to Vercel


You do **not** need to start from a Vercel template (“kit”) if you are working from this repository. Instead, clone the repo locally, then connect it to a new or existing Vercel project using the CLI or the Vercel dashboard.

1. [Install the Vercel CLI](https://vercel.com/cli) and run `vercel login`.
2. Run `vercel link` inside this project to associate it with a Vercel project (create one if prompted).
3. Run `vercel` for a preview deployment or `vercel --prod` for production once the link step succeeds.

> If you prefer to begin from Vercel’s Astro template in the dashboard, you can still copy this project’s files into that repository afterwards. The runtime and adapter configuration used here are already compatible with Vercel’s infrastructure.

This project uses the official `@astrojs/vercel` adapter configured for serverless output on the supported `nodejs20.x` runtime. Vercel will automatically detect the framework when you push to a connected repository.


## Adding Vue components

Astro lets you mix and match UI frameworks. To add Vue support:

```bash
npm install @astrojs/vue vue
```

Then update `astro.config.mjs` to include the Vue integration:

```js
import vue from '@astrojs/vue';

export default defineConfig({
  integrations: [vue()],
});
```

Once configured, you can import Vue components into any `.astro` page using the [client directives](https://docs.astro.build/en/reference/directives-reference/#client-directives) to control hydration.
