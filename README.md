# Hi There!

This is my experimental ground for GitHub Pages. Expect things to change frequently here!

# Setup

## Setup Skeleton

Clone the existing repo

```
git clone git@github.com:bryantam/bryantam.github.io.git
```

DO NOT cd into the repo yet. Create Skeleton App

```bash
npm create skeleton-app@latest bryantam.github.io
```

Choose the following settings

```text
◇  Which Skeleton app template?
│  AppShell starter
│
◇  Select a theme (top most selection will be default):
│  Skeleton
│
◇
What other packages would you like to install:
│  none
│
◇  Add type checking with TypeScript?
│  No
│
◇  What would you like setup in your project:
│  none
```

Run npm install

```bash
cd bryantam.github.io
npm install
```

## Setup static deployment

> Steps modified from https://www.okupter.com/blog/deploy-sveltekit-website-to-github-pages

Inside the repo

```bash
npm add -D @sveltejs/adapter-static
```

And then, in the `svelte.config.js` file, we need to replace `@sveltejs/adapter-auto` with 
`@sveltejs/adapter-static`.

Also, add a new file `src/routes/+layout.js` with content:

```js
export const prerender = true
```


# Svelte Stuff

Everything you need to build a Svelte project, powered by [`create-svelte`](https://github.com/sveltejs/kit/tree/main/packages/create-svelte).

## Creating a project

If you're seeing this, you've probably already done this step. Congrats!

```bash
# create a new project in the current directory
npm create svelte@latest

# create a new project in my-app
npm create svelte@latest my-app
```

## Developing

Once you've created a project and installed dependencies with `npm install` (or `pnpm install` or `yarn`), start a development server:

```bash
npm run dev

# or start the server and open the app in a new browser tab
npm run dev -- --open
```

## Building

To create a production version of your app:

```bash
npm run build
```

You can preview the production build with `npm run preview`.

> To deploy your app, you may need to install an [adapter](https://kit.svelte.dev/docs/adapters) for your target environment.
