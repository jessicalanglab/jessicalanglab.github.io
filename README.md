#Introduction

Our page is modeled after the remote theme [Bootstrap - Clean Blog Jekyll](https://startbootstrap.com/themes/clean-blog-jekyll/) - Official Jekyll Version

"[Clean Blog Jekyll](https://startbootstrap.com/themes/clean-blog-jekyll/) is a stylish, responsive blog theme for [Bootstrap](https://getbootstrap.com/) created by [Start Bootstrap](https://startbootstrap.com/). This theme features a blog homepage, about page, contact page, and an example post page along with a working contact form powered by [Formspree](https://formspree.io/)."

## Copyright and License

Copyright 2013-2021 Start Bootstrap LLC. Code released under the [MIT](https://github.com/StartBootstrap/startbootstrap-clean-blog-jekyll/blob/master/LICENSE) license.

## Our Website

Website is found [here](jessicalanglab.github.io)

This README will give instructions on how to make changes or additions to the website.

# Installation & Setup Using Core Files

1. [Download](https://github.com/jessicadlang/jessicadlang.github.io/archive/refs/heads/main.zip) or Clone the repository "CoreFiles".

2. I set this up on my local computer and created a project for the file in Atom for editing.

# About

## Add a Page

Create a file ending in .md (markdown file type) in the "startbootstrap-clean-blog-jekyll" folder.

- It must contain header similar to that in "startbootstrap-clean-blog-jekyll/about.md"
- Use md language (for basics, see this [cheatsheet](https://www.markdownguide.org/cheat-sheet/))
- An additional example page is also available in this repository as the "testmd.md" file (view outcome of this code [here](https://jessicadlang.github.io/testmd))
- html code can sometimes be used if md language doesn't do what you want

## Add a Post to the "News" Page

Similar to "Add a Page" instructions above, create an .md file in the "posts" folder.

## Change Navigation Bar Items

Edit file in "_includes/navbar.html" to change items. Text for the actual display can be modified within the following code lines:

> `<a class="nav-link" href="{{"/publications" | relative_url }}">**Publications**</a>`

If you need to add an item to the nav bar, or want to rearrange navbar items, use the following block of code:

> <li class="nav-item">
>  <a class="nav-link" href="{{"/publications" | relative_url }}">Publications</a>
>  </li>

# Other notes

- Remember to manually update publications.md to put new publications on the [Publications](https://jessicadlang.github.io/publications) page.
- Update team.md with new lab members [Team](https://jessicadlang.github.io/Team)
- Add any relevant lab resources to the Resources.md file, and be sure to make sure anything private to the lab is protected in some way, as there is no way to do this inherently on GitHub Pages
- All images from other sources must be Open Source images (requiring no attribution), our own lab's work, or cited to the original source.
- Contact form goes to the Lab's Google Drive.
