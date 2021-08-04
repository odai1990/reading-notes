# Read 40

## React 4



By default, Next.js pre-renders every page. This means that Next.js generates HTML for each page in advance, instead of having it all done by client-side JavaScript. Pre-rendering can result in better performance and SEO.

Each generated HTML is associated with minimal JavaScript code necessary for that page. When a page is loaded by the browser, its JavaScript code runs and makes the page fully interactive. (This process is called hydration.)

Check That Pre-rendering Is Happening

You can check that pre-rendering is happening by taking the following steps:

Disable JavaScript in your browser (here’s how in Chrome) and…

Try accessing this page (the final result of this tutorial).

You should see that your app is rendered without JavaScript. That’s because Next.js has pre-rendered the app into static HTML, allowing you to see the app UI without running JavaScript.

Note: You can also try the above steps on localhost, but CSS won’t be loaded if you disable JavaScript.

If your app is a plain React.js app (without Next.js), there’s no pre-rendering, so you won’t be able to see the app if you disable JavaScript. For example:

Enable JavaScript in your browser and check out this page. This is a plain React.js app built with Create React App.

Now, disable JavaScript and access the same page again.

You won’t see the app anymore — instead, it’ll say “You need to enable JavaScript to run this app.” This is because the app is not pre-rendered into static HTML.

Two Forms of Pre-rendering

Next.js has two forms of pre-rendering: Static Generation and Server-side Rendering. The difference is in when it generates the HTML for a page.

Static Generation is the pre-rendering method that generates the HTML at build time. The pre-rendered HTML is then reused on each request.

Server-side Rendering is the pre-rendering method that generates the HTML on each request.

Per-page Basis

Importantly, Next.js lets you choose which pre-rendering form to use for each page. You can create a "hybrid" Next.js app by using Static Generation for most pages and using Server-side Rendering for others.

We recommend using Static Generation (with and without data) whenever possible because your page can be built once and served by CDN, which makes it much faster than having a server render the page on every request.

You can use Static Generation for many types of pages, including:

Marketing pages

Blog posts

E-commerce product listings

Help and documentation

You should ask yourself: "Can I pre-render this page ahead of a user's request?" If the answer is yes, then you should choose Static Generation.

On the other hand, Static Generation is not a good idea if you cannot pre-render a page ahead of a user's request. Maybe your page shows frequently updated data, and the page content changes on every request.

In that case, you can use Server-side Rendering. It will be slower, but the pre-rendered page will always be up-to-date. Or you can skip pre-rendering and use client-side JavaScript to populate frequently updated data.

Static Generation with and without Data

Static Generation can be done with and without data.

So far, all the pages we’ve created do not require fetching external data. Those pages will automatically be statically generated when the app is built for production.

However, for some pages, you might not be able to render the HTML without first fetching some external data. Maybe you need to access the file system, fetch external API, or query your database at build time. Next.js supports this case — Static Generation with data — out of the box.
