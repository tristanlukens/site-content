---
title: An introduction to JavaScript - the setup
author: Tristan Lukens
date: 1 January 2022
tags: [introduction, javascript, programming]
---

This is the first part of the JavaScript introductory tutorial: the setup part.
We're going to set up Visual Studio Code and a couple of extensions. As a bonus, I'll go over installing \`node.js\`.
You don't need any prior programming knowledge to follow this tutorial, but knowing how to use a computer is pretty handy.

## Visual Studio Code

### Installation

Go to https://code.visualstudio.com and click on the download link. **This is a trusted program, made by Microsoft. Not a virus.
[There is some telemetry enabled](https://code.visualstudio.com/docs/getstarted/telemetry), which you can turn off.**
There is another program called Visual Studio, which you don't want. This is a full-blown IDE, made for coding in C#. C# and
JavaScript aren't interchangable; they're seperate programming languages.
I will talk more about that in the article about JavaScript's fundamentals, before which I'll talk about the concept of a
programming language. This is only a setup guide.

### Extensions

VSCode works with so-called extensions. These provide extra features etc, to make the editor better. You can install them in various
ways, the easiest being the in-app marketplace. You can access it by clicking on its tab icon, in the sidebar.
![extensions tab](/extensions-tab.png)
_Screenshot showing where the extensions tab is._
If you open this, you'll see a search bar. Search for and install the following extensions, and meet me back here. We'll talk about these later.

- Live Server
- HTMLHint
- Prettier

---

[Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) is used for hosting your web page, on your [loopback address](https://en.wikipedia.org/wiki/Localhost) (local ip address of your
computer that cannot be accessed from anywhere but your computer). It has live reload, which means that if
something in one of your files changes, the page will reload. You won't have to click the button anymore.
[HTMLHint](https://marketplace.visualstudio.com/items?itemName=mkaufman.HTMLHint) is error checking for HTML. If something is typed wrong, it'll tell you what went wrong and where.
[Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode) is for formatting your code. Not every language is supported, but the ones for web development are (HTML, CSS, JS, JSON, PHP and others).

### Extension setup

HTMLHint and Live Server work out of the box, but Prettier requires some setup.

- open settings, by clicking **⌘ + ,** on macOS, **Ctrl + ,** on Windows and Linux
- search for "default formatter"
- select "Prettier - Code Formatter"
  This should label Prettier as the leading code formatter, so it will format all supported file types. You can find a list of those
  in the Marketplace link I hyperlinked above.

## Bonus - installing Node

\`node.js\` is a browser alternative for running JavaScript code. It's built on Chrome's V8 core engine, and is mostly used with servers.
With node comes \`npm\`, which is the node package manager. There's thousands of packages in the repositories of npm, https://www.npmjs.com.
This is a little bit more advanced, and definately not a necessary step. If you want to proceed using JavaScript and want to become
a good dev, install node. Otherwise (or if you're not tech savvy enough), just move on to the tutorial blog post.
