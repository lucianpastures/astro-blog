# Astro Blog

## Netlify

1. make an account and hook up your github
2. choose the repo with the astro blog
3. any changes you push to the repo will show on the actual website hosted on netlify (netlify automatically executes `npm run build` and uses the files in `dist/`)

## RSS

Has RSS functionality. File `src/pages/rss.xml.js` provides this functionality.

This enables users to subscribe to your posts via an RSS feed reader.

```md
Download a feed reader, or sign up for an online feed reader service and subscribe to your site by adding your own Netlify URL. You can also share this link with others so they can subscribe to your posts, and be notified when a new one is published.
```

## Astro Island

This is what astro calls an interactive component on an otherwise static page, e.g. a dark mode toggle button

We will use Preact. Use `npx astro add preact` to add it via astro (replace preact with whatever UI library or any other "plugin" you want in an Astro project, e.g. `npx astro add tailwind`). Preact is an extremly lightweight version of React that specializes in building lightweight interactive components.

### Preact + Astro

1. create `components/Greeting.jsx` (notice we end the file with `.jsx` not `.astro`)
2. import Preact and just make it like a regular React component with the same syntax
3. import it into your home route `pages/index.astro`
4. make sure to use `client:load` in the component `<Greeting client:load messages={["Hej", "Hallo", "Hola", "Habari"]} />` so Astro knows it is an island not a regular Astro component

`client:load` on a component = **hydrated component/island** which is astro terminology for "component that has permission to execute javascript on the client after the intial page load, i.e. this component is interactive." Look into `client:visible` too.

### Vanilla JS Island

Check out `components/ThemeIcon.astro` -- here you'll find how to make a standard Astro component interactive with vanilla JS without the need of a library like Preact.

## Astro + Tailwind

https://tailwindcss.com/docs/guides/astro
