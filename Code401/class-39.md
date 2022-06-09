# Reading Assignment 39

## React 3

---

### NextJs

- When building a React app from scratch there are many things to consider;
  - The code has to be bundled with a bundler like webpack and transformed by a compiler like babel.
  - Production optimizations like code splitting might be necessary.
  - Some pages when pre-rendered staticly might be better for performance and SEO.
  - There might be some server-side code to connect the React app to a data store.
- Using a framework can solve these problems but it must have the right level of abstraction, and it needs to have a good developer experience.
- The React framework of relevance today is Next.js.
- Next.js aims to solve the previous problems as well as having;
  - An intuitive page-based routing system
  - Pre-rendering for both static generation and server-side rendering
  - Automatic code splitting
  - Client-side routing
  - Built in CSS support
  - Development environment with Fast Refresh support
  - API routes for endpoints with serverless functions
  - Extendable
- Next.js is used by thousands of production-facing websites including some of the world's largest brands.
- In Next.js, when navigating between pages, the `<a>` tag is wrapped in a `Link` component.
- Next.js code splits automatically, where each page only loads what's necessary for that page.
- Next.js can serve static assets from a top-level directory called public.
- You can also use Third-Party JS with Next.js

---

### React Context for Beginners

- React context allows developers to pass down and use data in any component without using props.
- Using it is great when passing data that can be used by any component of the application.
- The data placed on React context shouldn't be data that will need to be updated often.
- React Context was created to solve the issue of "props drilling" where props are passed down through multiple component levels that don't need it.
- RC is an API built into React. To use it only requires 4 steps;
  - Create context with `createContext`.
  - Take the context and wrap the provider around the component tree.
  - Put any value you like on the provider with the `value` prop.
  - Read the value within any component with the context consumer.
- One thing to note is that just because you can use Context to avoid component drilling, doesn't mean it should be the only solution you use. In some cases, the issue can be solved by composing the components better.
- It is not recommended to use RC as a state management library because every change to it causes a re-render for every component that uses it.

---

### Why I’m using Next.js in 2020

- Next.js is a framework built on top of React and it lets you choose on a page by page basis whether it will render on client, server or both.
- They talked about a few different aspects of Next.js;
  - Performance
    - Next.js abstracts some of the complexity to allow the developer to think less about the complexites for building a performative application.
      - Minifying JS
      - Code Splitting
      - Pre-fetching assets
      - Rendering the minimal amount of HTML
      - Caching builds.
  - Developer Experience
    - React Fast Refresh
      - Allows React State to be preserved in components when changes are made.
      - Error Fixing is easier, because if something breaks, a model pops up showing what line is broken.
  - Deployment
    - Next.js despite common use, can be deployed anywhere that has a Node Server, or even self-hosted.
    - It also has support for turning the site into a static site for deployment to places like GitHub Pages.
    - It has support for Incremental Adoption with Redirects and Rewrites in the platform.
