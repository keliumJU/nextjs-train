<p align="center">
  <a href="https://kommit.co">
    <img  src="https://user-images.githubusercontent.com/2568221/230443523-26d29f2c-93d1-4084-af04-21619a41908e.jpg"  alt="Chaincerts"   />
  </a>
</p>

<h1 align="center">
  <img  src="https://user-images.githubusercontent.com/84339390/230207851-5a3c1b87-cff7-457a-acf5-f254535c76e0.png"  alt="Chaincerts" width="250" />
</h1>

#### www is the code for kommit's website and landing page, developed and designed to provide our visitors with a fast, seamless and high-quality browsing experience that's in alignment with our brand's identity. The professionalism of our company is reflected in every aspect of the website, from its performance to its visual appeal, leaving a positive impression on our visitors.
<hr>

## ⚒️ Setup Node.js

- `asdf install`: Install current tools/runtime for the project
- Install Node js version >= **18.13.0**


You can install asdf [here](https://asdf-vm.com/guide/getting-started.html)

## 🚀 Run the app

- `yarn install`: Install dependencies
- `yarn dev`: Runs the project in dev and restarts with each change
- `yarn build`: Generate production build
- `yarn preview`: Locally preview production build

## 🧪 Testing

- `yarn test`: Run unit tests with Jest

## 🔦 Linting

- `yarn lint`: Run linter
- `yarn lint-fix`: Fix lint issues

## 📑 Add a new blog post

To add a new blog posts follow the next steps: 

**NOTE:** The blog post should be written in Markdown format, and the images used in it should be located in the folder: `static/images/posts` and have a maximum size of `80kB`.

1. Add a new JSON file in the folder `src/assets/blogPosts` with the file name of the blog post in kebab-case, for example: `blog-post-example.json`.

2. The JSON file should have a structure like the example located in `src/assets/blogPosts/blog-post-example.json`:

```json
{
  "slug": "blog-post-example", // Same as the file name
  "imageURL": "/images/example.jpg", // The image url should be located in `static/images` and the path should be based on the static folder as in the example
  "date": "Sunday, 1 Jan 2023", // Date of publish (Use the same format)
  "title": "This is a blog post example", // Title of the blog post
  "description": "This json is the example for a new blog post added to the repo.", // First paragraph of the blog post
  "content": "# Content", // Content in markdown codified in JSON
  "topics": ["Topic 1", "Topic 2"], // Topics of the blog post
}
```

3. You can write the blog post in any markdown editor but you have to encode it into a JSON to paste it into the `content` field of the JSON file, you can use https://jsonformatter.org/json-stringify-online.

4. Add the JSON file to the blog posts index `src/assets/blogPosts/index.ts`:

- Import the file into the index.ts as follows: 
```typescript
import blogPostExample from './blog-post-example.json';
```
- Add the file to the blog post object adding a new line with the respective blog post:
```typescript
{
  ...rest,
  'blog-post-example': blogPostExample
}
```

5. Make a Pull Request with the new files and changes.
