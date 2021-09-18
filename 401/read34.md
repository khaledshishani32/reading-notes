## Dynamic Routes

### Page Path Depends on External Data

- Code has to be bundled using a bundler like webpack and transformed using a compiler like Babel.
- You need to do production optimizations such as code splitting.
- You might want to statically pre-render some pages for performance and SEO. You might also want to use server-side     rendering or client-side rendering.
- You might have to write some server-side code to connect your React app to your data store.


#### How to Statically Generate Pages with Dynamic Routes

#### In our case, we want to create dynamic routes for blog posts:

- We want each post to have the path /posts/<id>, where <id> is the name of the markdown file under the top-level posts directory.
- Since we have ssg-ssr.md and pre-rendering.md, we’d like the paths to be /posts/ssg-ssr and /posts/pre-renderingch is React component in Next.js. We can add <Head> into our first-post.js



### graphic summary 
![](https://nextjs.org/static/images/learn/dynamic-routes/how-to-dynamic-routes.png)

### mplement getStaticPaths

#### First, let’s set up the files:

- Create a file called [id].js inside the pages/posts directory.
- Also, remove first-post.js inside the pages/posts directory — we’ll no longer use this.

#### Then, open pages/posts/[id].js in your editor and paste the following code. We’ll fill in ... later:

```
import Layout from '../../components/layout'

export default function Post() {
  return <Layout>...</Layout>
}
```

#### Then, open lib/posts.js and add the following getAllPostIds function at the bottom. It will return the list of file names (excluding .md) in the posts directory:

```
export function getAllPostIds() {
  const fileNames = fs.readdirSync(postsDirectory)

  // Returns an array that looks like this:
  // [
  //   {
  //     params: {
  //       id: 'ssg-ssr'
  //     }
  //   },
  //   {
  //     params: {
  //       id: 'pre-rendering'
  //     }
  //   }
  // ]
  return fileNames.map(fileName => {
    return {
      params: {
        id: fileName.replace(/\.md$/, '')
      }
    }
  })
}

```
#### Finally, we'll import the getAllPostIds function and use it inside getStaticPaths. Open pages/posts/[id].js and copy the following code above the exported Post component:
```
import { getAllPostIds } from '../../lib/posts'

export async function getStaticPaths() {
  const paths = getAllPostIds()
  return {
    paths,
    fallback: false
  }
}

```

### Implement getStaticProps

#### We need to fetch necessary data to render the post with the given id.

### graphical Summary 

![](https://nextjs.org/static/images/learn/dynamic-routes/how-to-dynamic-routes.png)

### Polishing the Post Page
#### Adding title to the Post Page

#### In pages/posts/[id].js, let’s add the title tag using the post data. You'll need to add an import for next/head at the top of the file and add the title tag by updating the Post component:

```
import Head from 'next/head'

export default function Post({ postData }) {
  return (
    <Layout>
      {/* Add this <Head> tag */}
      <Head>
        <title>{postData.title}</title>
      </Head>

      {/* Keep the existing code here */}
    </Layout>
  )
}
```
### Adding CSS

#### Finally, let’s add some CSS using the file styles/utils.module.css we added before. Open pages/posts/[id].js, then add an import for the CSS file, and replace the Post component with the following code:

```
import utilStyles from '../../styles/utils.module.css'

export default function Post({ postData }) {
  return (
    <Layout>
      <Head>
        <title>{postData.title}</title>
      </Head>
      <article>
        <h1 className={utilStyles.headingXl}>{postData.title}</h1>
        <div className={utilStyles.lightText}>
          <Date dateString={postData.date} />
        </div>
        <div dangerouslySetInnerHTML={{ __html: postData.contentHtml }} />
      </article>
    </Layout>
  )
}
```

## Push to GitHub

#### Before we deploy, let’s push our Next.js app to GitHub if you haven’t done so already. This will make deployment easier.

- On your personal GitHub account, create a new repository called nextjs-blog.
- The repository can be public or private. You do not need to initialize it with a README or other files.
- If you need help setting up your repo, take a look at this guide on GitHub.

#### Then:

- If you haven’t initialized the git repository locally for your Next.js app, do so now.
- Push the Next.js app to your GitHub repository.

#### To push to GitHub, you can run the following commands (replace <username> with your GitHub username):
```
git remote add origin https://github.com/<username>/nextjs-blog.git
git push -u origin main
```
### Deploy to Vercel

#### Vercel is a serverless platform for static and hybrid applications built to integrate with your headless content, commerce, or database. We make it easy for frontend teams to develop, preview, and ship delightful user experiences, where performance is the default. You can start using it for free — no credit card required.

### Create a Vercel Account

#### First, go to https://vercel.com/signup to create a Vercel account. Choose Continue with GitHub and go through the sign up process.
#### Import your nextjs-blog repository

#### Once you’re signed up, import your nextjs-blog repository on Vercel. You can do so from here: https://vercel.com/import/git.

- You’ll need to Install Vercel for GitHub. You can give it access to All Repositories.
- Once you’ve installed Vercel, import nextjs-blog.

#### You can use default values for the following settings — no need to change anything. Vercel automatically detects that you have a Next.js app and chooses optimal build settings for you.

- Project Name
- Root Directory
- Build Command
- Output Directory
- Development Command


### Next.js and Vercel

#### Vercel is made by the creators of Next.js and has first-class support for Next.js. When you deploy your Next.js app to Vercel, the following happens by default:

- Pages that use Static Generation and assets (JS, CSS, images, fonts, etc) will automatically be served from the Vercel Edge Network, which is blazingly fast.
- Pages that use Server-Side Rendering and API routes will automatically become isolated Serverless Functions. This allows page rendering and API requests to scale infinitely.

#### Vercel has many more features, such as:

- Custom Domains: Once deployed on Vercel, you can assign a custom domain to your Next.js app. Take a look at our documentation here.
- Environment Variables: You can also set environment variables on Vercel. Take a look at our documentation here. You can then use those environment variables in your Next.js app.
- Automatic HTTPS: HTTPS is enabled by default (including custom domains) and doesn't require extra configuration. We auto-renew SSL certificates.
