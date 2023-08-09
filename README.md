# Astro Blog

## Netlify

1. make an account and hook up your github
2. choose the repo with the astro blog
3. any changes you push to the repo will show on the actual website hosted on netlify (netlify automatically executes `npm run build` and uses the files in the `dist/`)

## RSS

Has RSS functionality. File `src/pages/rss.xml.js` proovides this functionality.

This enables users to subscribe to your posts via an RSS feed reader.

```md
Download a feed reader, or sign up for an online feed reader service and subscribe to your site by adding your own Netlify URL. You can also share this link with others so they can subscribe to your posts, and be notified when a new one is published.
```
