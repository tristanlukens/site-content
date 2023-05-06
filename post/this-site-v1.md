---
title: This site - v1
author: Tristan Lukens
date: January 1 2022
tags: [this site]
---

## UPDATE @ OCTOBER 19th

So I redid this site again, (and again before that, but that iteration never got anywhere). Thus, the information in this post is outdated.

## UPDATE @ MARCH 11th

Not all information in this article belongs to the current website, which is why I this article is called v1. I now use graphcms and vercel instead of just files and github pages, but I think I'll write a new blog post for the current site.

---

Let's talk about this site for a bit.

It was made using [Svelte](https://svelte.dev), Svelte's in-house router [SvelteKit](https://kit.svelte.dev), [TailwindCSS](https://tailwindcss.com) and its [Typography](https://tailwindcss.com/docs/typography-plugin) plugin and [SvelteMarkdown](https://www.npmjs.com/package/svelte-markdown), a [Markdown](https://en.wikipedia.org/wiki/Markdown) "converter" for Svelte.

I'm using GitHub Pages to host the site, and as of the time of writing, just including articles in the
standard repo. Where I want to go however, is using either a CMS like Graph CMS or Ghost CMS, or just
another GitHub repo with the files. I would then use a slug in SvelteKit, but I'm simply not experienced
enough with APIs and async JS.

## Svelte

Svelte is awesome. Just writing blocks of HTML, CSS and JavaScript (or HTML + TailwindCSS classes and TypeScript in this site's case) is very natural. React and Vue are more convoluted, and I'm not ready for them yet. I've been doing a lot with web development for a while now, but barely know anything when it comes to async and other intermediate level JavaScript concepts.

### SvelteKit

SvelteKit is Sapper's successor. They're both pretty simple routers for Svelte. It uses Vite under the hood
and makes the development expierence incredibly quick and nice.

### SvelteMarkdown

A markdown compiler for Svelte. It does what the name suggests: you give it a markdown source string,
and it compiles it to HTML and does this with a Svelte component. Example:

```svelte
<script>
	import SvelteMarkdown from 'svelte-markdown';

	const source = '# This is a title! This article is about the title.';
</script>

<section class="prose">
	<SvelteMarkdown {source} />
</section>
```

## TailwindCSS

You simply cannot talk about quick and nice developer experience without name-dropping Tailwind; I don't know how I could stand writing websites with CSS before. Even with SASS, CSS is a nightmare. Powerful yet simple, yes, but once Tailwind's got ya hooked, you cannot go back. Since I'm 15 and this schoolyear's my first year of being in computer sience class, I get to help people making websites for the first time. That's lovely, but actually writing CSS again is "even wennen" as we say here in the Netherlands (which means that it took a while to get used to).

### Typography plugin

Besides vanilla Tailwind, I'm using the Typography plugin. This means I have access to `prose` classes.
These deliver sane defaults for HTML blocks. It might look like this for example (with using SvelteMarkdown):

```js
<script>
	import SvelteMarkdown from "svelte-markdown"
	const source = "# This is a title!"
</script>

<section class="prose prose-sm prose-a:text-emerald-500">
	<SvelteMarkdown {source} />
</section>
```

## Markdown

Markdown is rather simple: it's plain text with some symbols for markup. For instance, you make some text a heading by putting a `#` in front of it, or make a list using `-` for all the elements, like this (but you can do more than this!):

```md
# A markdown example

This is some **markdown**.

You can do a lot with it!

- ordered and unordered lists
- **bold text**
- _italic text_
- headings with #
- hr elements with ---
- [hyperlinks](https://tristanlukens.github.io)
- ![images](https://images.unsplash.com/photo-1531297484001-80022131f5a1?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1120&q=80)

Pretty cool right?

## Readability

You don't need a markdown processor for the text to be readable, which
is where markdown really shines. This is perfectly readable!
I'm planning to do a whole article on markdown one day!
```

## GitHub Pages

GitHub Pages is a service which you can use to host a website for free #notsponsored. I'm building my SvelteKit app and pushing it to GitHub (like how [this](https://blog.stranianelli.com/sveltekit-et-github pages-english/) article says) and it's pretty much flawless.

## The future of this website

This might be the second version, but it will definately not be the last iteration. I'm still not using slugs and want to fully understand Svelte and JS before I try again, but I'm pretty happy with how I did things this time around.

### How I'm doing things now and how I want to do things

As you can see on [GitHub](https://github.com/tristanlukens/tristanlukens.github.io) I now have a Svelte Store with an array of objects with data about blog articles, but everytime I'm writing a new one I'm create a new object in the array and creating a new page with Article component in `src/routes/blog/post/` which is an inefficient way of doing things. I want to use [slugs], which have to do with dynamic routing. I took a good look at the SvelteKit docs about dynamic routing and came to the conclusion I just need to stick to how I was doing things before for now :)

---

Thank you for reading!

I just decided I'm going to put an emoji of the article at the bottom of every one from now on, so see if you can collect 'em all.

Happy new year btw.

🥰
