## Demo

### [https://next-blog.sanity.build](https://next-blog.sanity.build)

## Deploy your own

Use the Deploy Button below, you'll deploy the example using [Vercel](https://vercel.com?utm_source=github&utm_medium=readme&utm_campaign=next-example) as well as connect it to your Sanity dataset using [the Sanity Vercel Integration][integration].

[![Deploy with Vercel](https://vercel.com/button)][vercel-deploy]

## How to use

Execute [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app) with [npm](https://docs.npmjs.com/cli/init), [Yarn](https://yarnpkg.com/lang/en/docs/cli/create/), or [pnpm](https://pnpm.io) to bootstrap the example:

```bash
npx create-next-app --example cms-sanity next-sanity-blog
```

```bash
yarn create next-app --example cms-sanity next-sanity-blog
```

```bash
pnpm create next-app --example cms-sanity next-sanity-blog
```

Whenever you edit a GROQ query you update the TypeScript types by running:

```bash
npm run typegen
```

# Configuration

- [Step 1. Set up the environment](#step-1-set-up-the-environment)
  - [Reuse remote envionment variables](#reuse-remote-envionment-variables)
  - [Using the Sanity CLI](#using-the-sanity-cli)
    - [Creating a read token](#creating-a-read-token)
- [Step 2. Run Next.js locally in development mode](#step-2-run-nextjs-locally-in-development-mode)
- [Step 3. Populate content](#step-3-populate-content)
- [Step 4. Deploy to production](#step-4-deploy-to-production)
- [Next steps](#next-steps)

## Step 1. Set up the environment

### Reuse remote envionment variables

If you started with [deploying your own](#deploy-your-own) then you can run this to reuse the environment variables from the Vercel project and skip to the next step:

```bash
npx vercel link
npx vercel pull
```

### Using the Sanity CLI

Copy the `.env.local.example` file to `.env.local` to get started:

```bash
cp -i .env.local.example .env.local
```

Run the setup command to get setup with a Sanity project, dataset and their relevant environment variables:

```bash
npm run setup
```

```bash
yarn setup
```

```bash
pnpm run setup
```

You'll be asked multiple questions, here's a sample output of what you can expect:

```bash
Need to install the following packages:
sanity@3.30.1
Ok to proceed? (y) y
You're setting up a new project!
We'll make sure you have an account with Sanity.io.
Press ctrl + C at any time to quit.

Prefer web interfaces to terminals?
You can also set up best practice Sanity projects with
your favorite frontends on https://www.sanity.io/templates

Looks like you already have a Sanity-account. Sweet!

✔ Fetching existing projects
? Select project to use Templates [r0z1eifg]
? Select dataset to use blog-vercel
? Would you like to add configuration files for a Sanity project in this Next.js folder? No

Detected framework Next.js, using prefix 'NEXT_PUBLIC_'
Found existing NEXT_PUBLIC_SANITY_PROJECT_ID, replacing value.
Found existing NEXT_PUBLIC_SANITY_DATASET, replacing value.
```

It's important that when you're asked `Would you like to add configuration files for a Sanity project in this Next.js folder?` that you answer `No` as this example is alredy setup with the required configuration files.

#### Sanity website

1. Go to [manage.sanity.io](https://manage.sanity.io/) and select your project.


## Step 2. Run Next.js locally in development mode

```bash
npm install && npm run dev
```

Your blog should be up and running on [http://localhost:3000](http://localhost:3000)! If it doesn't work, post on [GitHub discussions](https://github.com/vercel/next.js/discussions).

## Sanity Studio

Open your Sanity Studio that should be running on [http://localhost:3000/studio](http://localhost:3000/studio).
