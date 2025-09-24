# Astro + Vercel Starter

This repository is a minimal Astro project configured to deploy to [Vercel](https://vercel.com/). Astro ships zero JavaScript by default, so you can launch a fast, content-driven site today and progressively add Vue (or any other framework) components later without rewriting your pages.

## Getting started

```bash
npm install
npm run dev
```

Visit `http://localhost:4321` to view the site locally.

## Deploying to Vercel

1. [Install the Vercel CLI](https://vercel.com/cli) and run `vercel login`.
2. Run `vercel` to create a new project (or link an existing one).
3. Deploy with `vercel --prod` once you are ready for production.

This project uses the official `@astrojs/vercel` adapter configured for serverless output. Vercel will automatically detect the framework when you push to a connected repository.

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
