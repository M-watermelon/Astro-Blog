---
title: 'New years post!'
layout: ../../layouts/post.astro
date: '07 Jan 2025'
---
New year, new goals - so here's what I plan to do in 2025:

#### Computer Science:
 - Add finishing touches to this website (functionalities and design)
 - Have more green on my Github Contributions!
 - Finish building/fix my computer science club's website (before I graduate) 
 - Compete in PicoCTF 2025
 - Explore Hack the Box more!
 -[x] Develop the website for the [Market repository](https://github.com/M-watermelon/Market-Site)

#### Biology:
 - Finish the NIH course in Clinical Pharmacology and take the final exam

#### Life:
 - Write blog posts and create more content!
 - drink more water!!
 - Graduate :D
 - Gaming!

 ---

 ## Some small progress updates for the website:

This site is now my official personal website, and the site listed under my github profile. 

I finally used ```Astro.glob()``` to collect and insert my posts into my website! This is great for automating the tedious task of inserting each entry myself, which is why Astro (and using frameworks in general) is so helpful.



Mini-goal: Consider programming an image carousel, and find more ways to include user interactivity into the site
 - also reorder the posts to start with the most recent one at the top

Here's how I get my posts inserted into the index of this site:

1) I import <mark>``` type { MarkdownLayoutProps } from 'astro'```</mark>

2) Establish some javascript constants at the top of the page (between the --- lines)
```js
const posts = await Astro.glob('../pages/posts/*.md');
type Props = MarkdownLayoutProps<{
  title: string;
  date: string;
}>;

const { frontmatter, url } = Astro.props;

```
3) I use <mark>``` posts.map()```</mark> to finally insert the collected posts into the intedent format (in this case I am using my ```<Card/>``` Astro component)

```html
{posts.map(post =><Card href={post.url}, title={post.frontmatter.title}, body={post.frontmatter.date}/>)}

```