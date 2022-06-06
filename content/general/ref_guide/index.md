+++
title = "Reference Guide"
+++

## Wiki Update

### Setup Overview

The source files for the wiki are hosted on GitHub [here](https://github.com/LASSAT-YU/wiki/). We are using GitHub Pages
to host the [wiki](@/_index.md). GitHub renders the static website rooted in
the [`/docs`](https://github.com/LASSAT-YU/wiki/tree/main/docs) folder. We use a static site generator
named [Zola](https://www.getzola.org/) to generate the static html from templates and markdown files. The actual wiki
[content](https://github.com/LASSAT-YU/wiki/tree/main/content) is written in markdown files with a front matter section
that must be placed at the top of the file. We only need to set the page title in that section. It would look
something like:

```
+++
title = "Reference Guide"
+++

And content goes here
```

Followed by the content of the page. The structure is very simple, each folder
inside of [content](https://github.com/LASSAT-YU/wiki/tree/main/content) defines a section and each .md file inside
the folder defines a page.

If you are unfamiliar with markdown see the [markdown](#markdown) section. The
templates are part of the theme and can be found in the "themes" folder. To compile or preview the content you will need
to [install zola](https://www.getzola.org/documentation/getting-started/installation/). If you do not require to preview
your changes you can proceed to make your edit without installing zola and mention in your [pull request](#pull-request)
that the changes have not been compiled yet. Once the templates and markdown have been compiled using
the `zola build` [command](https://www.getzola.org/documentation/getting-started/cli-usage/#build) then the docs folder
should contain the generated html, css, js, etc files.

### Markdown

Zola and by extension this Wiki uses [CommonMark](https://commonmark.org/). They have very good reference material on
their site. For getting started quickly or easy reference they
have [Learn Markdown in 60 Seconds](https://commonmark.org/help/) and if you are new to markdown or want a more complete
tutorial they have a [10 Minute Markdown Tutorial](https://commonmark.org/help/tutorial/). The tutorial is very good. It
is interactive, and you get to try the content and get feedback in realtime.

#### Collapsable sections

Source: <https://gist.github.com/pierrejoubert73/902cc94d79424356a8d20be2b382e1ab>

Example:

<details>
  <summary>Click to expand!</summary>

Detailed body shows when you click.

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum enim lorem, placerat sed vestibulum a, pellentesque
at leo. Vivamus tincidunt nisi massa, nec pellentesque diam mollis vel. Vestibulum turpis mauris, placerat id lectus ac,
varius imperdiet libero. Ut tortor lorem, scelerisque eu elit vitae, eleifend gravida justo. Cras risus est, maximus non
dapibus quis, placerat ullamcorper diam. Ut vitae justo purus. Donec enim dolor, sodales et tempor vehicula, rutrum
vitae eros. Praesent commodo urna vitae pretium venenatis. Praesent lectus est, finibus sed lobortis at, finibus sit
amet velit. Maecenas varius tincidunt neque, sed ultricies lectus cursus ut. Phasellus auctor fermentum venenatis.
Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia curae; Phasellus eu velit consectetur,
pretium ipsum eget, pharetra massa. Duis sed posuere nisl. Proin a pharetra sapien, sit amet sollicitudin nisi. Nulla
dolor nunc, interdum id convallis vitae, maximus ac elit.

Proin ullamcorper lorem id dui commodo hendrerit. Etiam vitae commodo ipsum. Aliquam placerat ex sed dolor eleifend, id
pulvinar lorem dictum. Duis in massa tortor. Maecenas leo quam, luctus at egestas ac, tincidunt a odio. Pellentesque
cursus mi egestas leo viverra egestas. Nulla quis velit sit amet tellus aliquet mollis sed sed justo. Vivamus interdum
porta ultricies. Nulla quis ex in arcu consequat auctor quis et ligula. Phasellus pellentesque nibh quis risus pretium
malesuada.
**Generated 2 paragraphs, 219 words, 1490 bytes of [Lorem Ipsum](https://www.lipsum.com/)**

</details>

**How to Structure**

```
<details>
   <summary>Click to expand!</summary>

   Detailed body shows when you click.
   
   ...
   
   ... 

</details>
```

**Two important rules:**

1. Make sure you have an **empty line** after the closing `</summary>` tag, otherwise the markdown/code blocks won't
   show correctly.
2. Make sure you have an **empty line** after the closing `</details>` tag if you have multiple collapsible sections.

### Zola

The Zola documentation can be found on their [website](https://www.getzola.org/documentation/getting-started/overview/).
Knowing the details of how it works is not required to make updates to this wiki. Once you understand how to
write [markdown](#markdown) then you should be fine.

In summary what you need to know is:

- each subsystem has a section created for them which is represented by a folder inside the content folder.
- To add a new page create a file ending in `.md` in one of the subsystem folders.The top of the file must have the
  relevant front matter information as indicated in
  the [overview](#setup-overview).
- If you need to include images or other assets that need to be uploaded see the zola documentation
  regarding [asset collocation](https://www.getzola.org/documentation/content/overview/#asset-colocation). In their
  example the "research" folder corresponds to one of our subsystem folders.
- Feel free to reach out on [discord](https://discord.gg/JBCdZRm) if you have any questions.

### Creating the Pull request (Actually submitting your changes) {#pull-request}

#### Using only GitHub.com

Detailed instructions to come for now please reach out on [discord](https://discord.gg/JBCdZRm).

#### By cloning locally and previewing with zola

Detailed instructions to come for now please reach out on [discord](https://discord.gg/JBCdZRm).
