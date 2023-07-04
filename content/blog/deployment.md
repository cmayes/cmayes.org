+++
title = "Deploying the Blog"
date = 2023-07-03

[taxonomies]
tags = ["meta"]
+++

That was pretty easy! [Zola](https://www.getzola.org/) is a solid choice for static site generation.

<!-- more -->

The main things I had to figure out were getting the configuration straight and the overrides in place. If you're
doing it right, you won't modify anything under the "themes" directory tree. If you want to override something,
make a copy of the theme's file in a mirrored section of your project and modify the file there. For instance,
I wanted to make a few changes to the index template, so I copied `themes/papaya/templates/index.html` to 
`templates/index.html` and made my changes there.

I have, in fact, made the theme's git repository a "[submodule](https://git-scm.com/book/en/v2/Git-Tools-Submodules)"
of my website's repository. I can't think of the last time I did that... [IDEA](https://www.jetbrains.com/idea/) was 
a bit wonky about handling the submodule, but it eventually caught on. It'll be handy to be able to pull any 
theme updates directly from the repository.

I also grabbed a weather icon for the site's favicon because I like it when websites have a nice and/or memorable
favicon. I thought about adding a search bar, but I like the uncluttered layout that the Papaya theme has, so
I'm going to skip search for now. Should I write enough to warrant a search, it'll be pretty simple to add.

Creating the build and deployment pipeline in [Cloudflare Pages](https://pages.cloudflare.com) was simple
and smooth. The first attempt timed out, but it went off without a hitch the second time around. The DNS integration
with my hosted domain was seamless (as one might expect from Cloudflare). I am very pleased.