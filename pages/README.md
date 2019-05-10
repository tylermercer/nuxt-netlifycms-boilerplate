# PAGES

This directory contains your Application Views and Routes.
The framework reads all the `*.vue` files inside this directory and creates the router of your application.

More information about the usage of this directory in [the documentation](https://nuxtjs.org/guide/routing).


Tyler's Note
>The index file here is a hard-coded page (the home page, with the list of posts),
whereas the ones inside `blog` and `pages` are templates used by Nuxt to create
the routes for each of my JSON files, as configured in nuxt.config.js--that's
what `getDynamicPaths` and the code that calls it are for.
