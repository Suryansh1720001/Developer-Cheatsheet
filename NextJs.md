## NextJs CheatSheet

-  The react framework that enables us to build superfast and extremely user-friendly static websites, as well as full fledge production ready web application using react.
- We will write the react code only like components , props , state etc. in NextJS.
- File based routing is by default done in NextJs so we don't have to use third party library like react router dom.
- Next.js is used to create a production ready apps.

# How to install Next.js?
We create nextjs app using create-next-app in terminal or git bash.
```sh
npx create-next-app
```
After installing app we can immediately run the  app by running `npm run dev or yarn dev` in terminal.
We see the result on http://localhost:3000

For example :
`npx create-next-app myNextjsapp`

## What is Pages in Next.js?
React Component which is exported from a file in the pages directory is Called Pages in NextJs.
In NextJs Pages are associated with a route based on their file name that means we can access any file just by writing name after `/`.
For example in NextJs:

* pages/index.js is associated with the / route.
* pages/blog is associated with the /posts/blog route.

Steps For Creating Pages:
1.Open pages from project
2.Create any file lets take JS file name as Blog.js
3.Write following content inside it.

```sh
export default function blog() {
  return <h1>My Blog Content</h1>;
}
```

This is how we can exactly create different pages in Next.js.
The path to the file becomes the URL path means in above code snnipet `http://localhost:300/blog` is the URL path.

## Link Component
Usually we use the <a> HTML tag when linking between pages on websites.

In Nextjs, we can use the Link Component `next/link` to link between pages.
`<Link></Link>` allows us to do client-side navigation and accepts props that give us better control over the navigation nature.

# How to use Link in website?
1. Open pages/index.js
2.Import the Link component from next/link.

`import Link from 'next/link'`

# Example 
```sh
<div className="container">
  Lets Learn <a href="https://nextjs.org">NextJs </a>
</div>
```
And change it to `Link` in NextJs.
```sh
<div className="container">
  Refer <Link href="/nextjs">this page to learn.</Link>
</div>
```
`pages/nextjs ` contain all content or resources to learn NextJs.

```sh
import Link from 'next/link';

export default function nextjs() {
  return (
    <>
      <div>
      Nextjs content
      </div>
    </>
  );
}
```

## NextJs Navigate Between Pages

For Client-Side Navigation we usually use Link component which helps us to navigate between two pages in the same NextJs app.


# splitting and prefetching of Code 
Page only loads when it is necessary for that page. That means when productpage is rendered,then other pages code is not served initially.This will help to nssure that productpage loads fast regardless of number of pages.


# NextJs Assets
In NextJs Assests like images are inside top-level public directory.
This directory is useful in any static assets.

Steps to add file in public directory :

•	Download profile picture or any image in .jpg format (or any other valid format).
•	Create an images directory inside of the public directory.
•	Save the dowloaded picture as pic.jpg or any name in the public/images directory.
•	Take care of size of downloaded image for your website or app.
•	Now, we can use all image inside the `public/images` directory.

Also, NextJs is providing Image componentto handle images in website.
When we use `next/image` we have to mention height and width also with the image.

Example Code :
```sh
import Image from 'next/image';

const ComponentName = () => (
  <Image
    src="/images/pic.jpg" // This is the route of the image file
    height={400p} // Height in pixel
    width={500} // width in pixel
    alt="picname"
  />
);
```

# NextJs Metadata

If we want to change or want to do modification in metadata of the page,such as the <title> HTML tag then how can we do it in Nextjs?

1. Lets open `pages/index.js` in your editor and we will see these following lines : 

```sh
<Head>
  <title>Create Next App</title>
  <link rel="icon" href="/favicon.ico" />
</Head>
```
As <Head> is a React Component which is built in NextJs that's why it is not written in lowercase in NextJs.
In NextJs we can import the Head component from the next/head module as well.

Adding Head to blog.js
Previously in this cheatsheet We haven't added a <title> to our /posts/blog route. Let's add one.
Open the pages/blog.js file and add an import for Head from next/head at the beginning of the file.

`import Head from 'next/head';`

Then, we should update our exported Blog component to include the Head component in blog.

Code sample is following:

```sh
export default function blog() {
  return (
    <>
      <Head>
        <title>My Blog</title>
      </Head>
      <h1>My Blog Title</h1>
      <h2>
        <Link href="/">
          <a>Back to homepage</a>
        </Link>
      </h2>
    </>
  );
}
```
Now access the result on http://localhost:3000/blog URL Path. The browser is showing the result “My Blog Title ” and head title "My Blog". 

And also by using browser’s developer tools,we can see that the title tag is added to <head>.


# Script Use in NextJs

`next/script` is an extension of the HTML <script> element.
For using script tag in NextJs we add an import for Script from next/script at the beginning of the file.
```sh
import Script from 'next/script';
```

# CSS STYLING

In our created NextJs app we can see a folder called styles with two CSS files: 
1. global stylesheet i.e `globals.css`
2. CSS module i.e `Home.module.css` or `Contact.module.css`.

So why this 2 different CSS??

In global CSS whatever we add it will applied on any content of the project so we have to always take care of creating unique class names but moduleCss allows us to use the same CSS class name in different files without worrying about class name collisions.

# Creating API Routes in NextJs

API Routes helps us to create an API inside a NextJs app. We can do so by creating a function inside the pages/api directory which has following format:

`req = HTTP incoming message, res = HTTP server response`

```sh
export default function routehandler(req, res) {
  // ...
}
```

Example of simple API 

1. Creating a file called hello.js in pages/api with the following code:
```sh
export default function routehandler(req, res) {
  res.status(200).json({ text: 'Hello' });
}
```
And access it at http://localhost:3000/api/hello. 
we should see {"text":"Hello"} on web browser.Tha's how we successfully created our first route API.

Happy Learning!!

Thank You!
