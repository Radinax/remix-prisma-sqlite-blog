# Welcome to our Remix Blog!

This is a fullstack project using Remix, Prisma, SQLite, where we create a blog that a user can register/login to create/delete posts.

## File Structure

```text
src/
├── app/
│   ├── routes/
│   │   ├── auth/
│   │   │   ├── login.jsx
│   │   │   └── logout.jsx
│   │   ├── posts/
│   │   │   ├── $postId.jsx
│   │   │   ├── index.jsx
│   │   │   └── new.jsx
│   │   ├── index.jsx
│   │   └── post.jsx
│   ├── styles/
│   │   └── globals.css
│   ├── utils/
│   │   ├── db.server.ts
│   │   └── session.server.ts
│   ├── entry.client.jsx
│   ├── entry.server.jsx
│   └── root.jsx
├── prisma/
│   ├── dev.db
│   ├── schema.prisma
│   └── seed.js
├── .env
├── jsconfig.json
├── package.lock.json
├── package.json
├── README.md
└── remix.config.js
```

## Development

From your terminal:

```sh
npm run dev
```

This starts your app in development mode, rebuilding assets on file changes.

## Deployment

First, build your app for production:

```sh
npm run build
```

Then run the app in production mode:

```sh
npm start
```

Now you'll need to pick a host to deploy it to.

### DIY

If you're familiar with deploying node applications, the built-in Remix app server is production-ready.

Make sure to deploy the output of `remix build`

- `build/`
- `public/build/`

### Using a Template

When you ran `npx create-remix@latest` there were a few choices for hosting. You can run that again to create a new project, then copy over your `app/` folder to the new project that's pre-configured for your target server.

```sh
cd ..
# create a new project, and pick a pre-configured host
npx create-remix@latest
cd my-new-remix-app
# remove the new project's app (not the old one!)
rm -rf app
# copy your app over
cp -R ../my-old-remix-app/app app
```
