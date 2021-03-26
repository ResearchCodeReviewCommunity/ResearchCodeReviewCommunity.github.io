# [Research Code Review Community Website](https://researchcodereviewcommunity.github.io/)

 

This repository contains the Website for the Research Code Review Community. It is automatically built from [markdown](https://commonmark.org/) files by [Hugo](https://gohugo.io/) using [GitHub Actions](https://github.com/features/actions).

This site is available here:
https://researchcodereviewcommunity.github.io/

The following branches are important:

- `main`: the markdown files corresponding to the current live version of the website
- `gh-pages`: the static html site, automatically built by Hugo on new commits to `main` by [this script](.github/workflows/deploy.yml)

:warning: **Do not commit directly to `main` or `gh-pages`.** :warning:
Instead, commit changes to any other branch and open a pull request.
Once your changes are merged into `main` the site will be automatically built and deployed and will be live roughly 1 minute later.

## Previewing changes locally

Install hugo:

- macOS
  ```
  $ brew install hugo
  ```

- Windows
  ```
  $ choco install hugo -confirm
  ```

- Linux
  ```
  $ snap install hugo
  ```

- [other options](https://gohugo.io/getting-started/installing/)

Once installed, from the `hugo_site` directory simply run

```bash
hugo server
```

and click through to the localhost link you're given.


## Editing content

- All pages are in `hugo_site/content`
- Static content such as photos is in `hugo_site/static`, following the directory structure of the page it is required in

Homepages are `_index.md` in each top level content directory.
All subpages are `name.md`, where `name` corresponds to the part of the URL after the top level.


## HTML warning

:warning: **You should not have to write any HTML.** :warning:
If you can't get a page to look like you want it to look, you might need to write a [shortcode](https://gohugo.io/content-management/shortcodes/).
