# Reading Assignment 41

## React 4

---

### Dynamic Routes

- Next.js allows you to statically generate pages that have paths that are dependent on external data. This allows for dynamic URLs in Next.js
- First you create a page called [dynamic_name].js in pages and within the file, we write the code that renders the page.
- Whats new is an async function called `getStaticPaths` that gets exported and within it you return all the possible values for the dynamic name.
  - Then you need to implement `getStaticProps` to fetch the necessary data for the page with a given dynamic_name
- In summation of the basics, to get a dynamic route page you need;
  - A React Component to render the page
  - getStaticPath which return an array of all the possible values for dynamic_name
  - getStaticProps which fetches the necessary data for the relevant dynamic_name page.
- If you want to render markdown you need the `remark` library.
- You can add CSS simply by importing it.
- Like `getStaticProps`, `getStaticPaths` can fetch data from an external API endpoint too.
- `getStaticPaths` runs at different points in Development vs Production;
  - In development it runs on every request.
  - In production it runs at build time.
- For `getStaticPaths` if you return `fallback: false` then all paths not returned by `getStaicPaths` will result in a 404 page whereas if it is true then Next.js will serve a fallback version of the page the first time a request is sent there and then in the background it will generate a page so that other requests in the future will reach the new generated page.
- You can also have "catch-all" paths that capture all the possible paths specified. For example, `pages/[...id].js` would capture `pages/a`, `pages/a/b` and so on.
- To access the Next.js router, you use the `useRouter` hook.
- You can also create custom 404 pages if you wish.

---

### Deployment

- To deploy, first you need to push the app up to GitHub and ensure the main branch is up to date.
- The easiest deployment for Next.js is with Vercel which was developed by the creators of Next.js.
  - Vercel is Serverless, and allows for static and hybrid apps.
- With Vercel, you import your GitHub repository and it will begin building automatically.
- Once the Repo has been imported to Vercel and built, any future pull requests to the Main branch will automatically have a preview build done and if the request is merged, then it will automatically build into production.
- You do have other hosting options if they have support for Node.js
- If you have the inclination you can also use Typescript with Next.js.
