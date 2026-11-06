# 🧠 Self-Control

> A simple one-page article about the importance of self-control, with a navbar that changes colour as you scroll.

A beginner-friendly web page built with plain HTML, CSS, and JavaScript. It has a full-screen hero image, a fixed navigation bar, and a readable article section below.



**Live demo:** https://importance-of-self-control.vercel.app

## Features

- Full-screen hero section with a background image and a bold title
- Fixed navbar that stays at the top while you scroll
- Navbar switches from light to dark when you scroll down to the article
- Clean, readable article layout with comfortable margins
- No frameworks or libraries, just open it and it works

## Built with

| Language | What I used it for |
|----------|--------------------|
| **HTML5** | Page structure: navbar, hero section, article paragraphs |
| **CSS3** | Flexbox layout, fixed positioning, background image, text shadow, hover and colour-change styles |
| **JavaScript (vanilla)** | Listening for scrolling and toggling the navbar's `active` class |

## How I made this

- **Tutorial or not:** [Pick one and edit: "I built this on my own, using MDN and Google when I got stuck." / "I followed [tutorial name/link] for the scrolling navbar idea, then wrote my own article, changed the colours, and picked my own images."]
- **Tools:** [e.g. VS Code, Live Server, Git and GitHub]
- **Images:** Hero image from [Unsplash](https://unsplash.com), logo is an SVG
- **Process:**
  1. Planned the layout: navbar, hero section, article
  2. Wrote the HTML structure and the article text
  3. Styled the hero section so the image fills the whole screen
  4. Made the navbar fixed and spaced out with flexbox
  5. Wrote JavaScript to change the navbar colour on scroll
  6. Fixed bugs and uploaded to GitHub

## How the scroll effect works

1. The script listens for the browser's `scroll` event.
2. On every scroll, it checks whether the page has scrolled past the top of the article section (`offsetTop`), minus the navbar's height.
3. If it has, the navbar gets the `active` class, which turns the background black and the links white.
4. If you scroll back up, the class is removed and the navbar goes back to normal.

```javascript
window.addEventListener("scroll", () => {
    if (window.scrollY > bottomContainerEl.offsetTop - navbarEl.offsetHeight - 50) {
        navbarEl.classList.add("active");
    } else {
        navbarEl.classList.remove("active");
    }
});
```

## What I learned

- How `position: fixed` keeps an element on screen while the page scrolls
- How to make a full-screen background image with `height: 100vh` and `background-size: cover`
- How to centre content with flexbox
- How to use `window.scrollY` and `offsetTop` to react to scrolling
- How to change styles by adding and removing a CSS class with JavaScript
- That one small typo in a selector can stop a style from working, with no error message

## What I struggled with

- **Typos in selectors and class names.** CSS doesn't warn you when a selector matches nothing, so a misspelled class just does nothing.
- **Getting the scroll timing right.** It took trial and error to decide exactly when the navbar should change colour.
- **Background images.** Getting the image to cover the whole screen without stretching.
- **Layout of the navbar.** Spacing the logo and links apart using flexbox.
- **Proofreading.** Catching spelling mistakes in a long block of text.

## Getting started

1. Clone the repository:
   ```bash
   git clone https://github.com/mahnoormhmmd-ops/self-control.git
   ```
2. Open the folder:
   ```bash
   cd self-control
   ```
3. Open `index.html` in your browser.

## Project structure

```
self-control/
├── index.html     # Page structure and article text
├── style.css      # Layout, hero image, navbar styles
├── script.js      # Scroll effect for the navbar
├── logo.svg       # Navbar logo
└── README.md
```

## Ideas for the future

- [ ] Make the navbar links scroll to real sections
- [ ] Add a mobile menu (hamburger button)
- [ ] Add a smooth scroll effect
- [ ] Build out the Blog and Contact pages
- [ ] Add a dark mode toggle

## Author

Made by **Mahnoor Muhammad**.

https://github.com/mahnoormhmmd-ops

