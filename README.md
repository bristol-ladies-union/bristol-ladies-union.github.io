# BLU Website

This site uses Jekyll to create a simple statically generated site for Bristol Ladies Union Football Club.

## Editor's Guide

Content can be edited directly in [GitHub](https://github.com/bristol-ladies-union/bristol-ladies-union.github.io). When you have finished, save/commit your changes and the content will be published automatically.

Publishing takes a few moments, you can check progress in Github [actions](https://github.com/bristol-ladies-union/bristol-ladies-union.github.io/actions)

### Uploading a match report

1. Add a new `.md` file to [_posts/reports](./_posts/reports/).  e.g. `2024-06-21-u12-v-portishead.md`
   - File name should be lower case
   - File name should prefixed with the date, format as `YYYY-MM-DD-`.
   - Use lower case and hyphens insted of spaces
2. Copy the content from an existing report to get started.
3. Make any appropriate changes to the [front matter](#front-matter)
4. Add page content. Formatting can be controlled using [markdown](https://www.markdownguide.org/cheat-sheet/). Some basic examples can be found [below](#markdown)

### Uploading a sponsor

1. Add a new `.md` file to [_posts/sponsors](./_posts/sponsors/).  e.g. [2021-05-15-ince.md](./_posts/sponsors/2021-05-15-ince.md)
   - File name should be lower case
   - File name should prefixed with the date, format as `YYYY-MM-DD-`.
   - Use lower case and hyphens insted of spaces
2. Copy the content from an existing sponsor to get started.
3. Upload sponsor logo to [assets/images/sponsors](./assets/images/sponsors). Image size should be 640px x 249px.
4. Make any appropriate changes to the [front matter](#front-matter)
5. Add page content. Formatting can be controlled using [markdown](https://www.markdownguide.org/cheat-sheet/). Some basic examples can be found [below](#markdown)

### Uploading images

Images can be uploaded to [assets/images](./assets/images/) and embedded in page content using [markdown](#markdown).

Add an image using the format ![alt text](image URL) e.g.

```md
![Dev Team](/assets/images/2024-dev-team.jpg)
```

### Uploading documents

Documents can be uploaded to [assets/docs](./assets/docs/). They will automatically be categorised based on the folder and links will be generated based on the file name.

- File name should be lower case
- File name should prefixed with the date, format as `YYYY-MM-DD-`.
- Use lower case and underscore insted of spaces

### Editing a team page

Each team has a page in the [teams](./teams/) directory. These can be edited to provide useful information to your age group like training times, location, a team photo, coach bio etc.

### Editing the home page

There is a small amount of editable content on the home page that can be edited [here](./index.md).

For more advanced changes it may be necessary to edit the [front matter](#front-matter) or in the [homepage layout](./_layouts/home.html).

### Editing the registrations page

The registration page can be edited [here](./registration.md).

### Front Matter

Jekyll uses [front matter](https://jekyllrb.com/docs/front-matter/) to add page properties that will be used by the page layout.

The front matter must be the first thing in the file and placed between triple dashes.

Most of these front matter values are optional, the minimum required is simply to add a title.

```yaml
---
title: U12 BLU vs Shine Saints
---
```

For more advance use the following settings are available.

```yaml
---
title: U12 BLU vs Shine Saints # page title for the browser
author: Ernie (coach) # in some layouts this will display the author's name
layout: report # which layout to use, these can be found in _layouts
published: false # optional, defaults to true. If set to false the page will not be publically visible 
heading: Bristol Ladies Union # optional page heading if different tot he title
subheading: "Bristol's largest all female football club" # optional subheading for a page banner
banner: "/assets/images/banners/home-comedy.jpg" # optional page banner for the page hero section
email: u10@blufc.com # provide an email address for the page's contact link
top: 1 # pins a post to the top of the recent articles lists
priority: 5 # used in some menus to determine link order
sidebar: # choose which sidebar widgets to display
    - team-list    
    - document-list
categories: # add categories, this will add the post to the correct menus
    - U12
    - Match Report
tags: # add tags, these will appear under the post and enables grouping posts by tags
    - bluarmy
---
```

### Markdown

Markdown is a simple formatting syntax that will be converted to HTML when the site is published. For more advanced examples take a look at the [docs](https://www.markdownguide.org/cheat-sheet/).

### Headings

Add headings by adding  new line prefixed with

```md

# This is the primary header (H1)

Here is a paragraph of content.

New paragraphs are created by adding line breaks.

## This is the secondary header (H2)

Here is a paragraph of content.

### This is the tertiary header (H2)

Here is a paragraph of content.

```

### Lists

Create a numbered list by prefixing with numbers

```md

1. This is item 1
2. This is item 2
3. This is item 3

```

Create an unordered list by prefixing with `-`

```md

- This is item 1
- This is item 2
- This is item 3

```

Create a link using the format `[link text](link URL)`

```md

Visit the registrations page [here](/registration)

```

Add an image using the format ![alt text](image URL)

```md
![Dev Team](/assets/images/2024-dev-team.jpg)
```

Bold text by surrounding with **

```md
This is **bold** text.
```

Italicise text by surrounding with *

```md
This is *italic* text.
```

Add a separater by entering a new line with 3 hyphens

```md
---
```

Display block quotes by prefixing with >

```md
> This is a blockquote.
```

## Development

### Running locally

Running locally requires [jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/testing-your-github-pages-site-locally-with-jekyll) to be installed.

1. Clone the repo to your local machine.
2. In [Gemfile](./Gemfile), uncomment the line starting `gem "jekyll" ...`
3. In [Gemfile](./Gemfile), comment out the line starting `gem "github-pages" ...`
4. run `bundle install`
5. run `bundle exec jekyll serve`

### Credits

The BLU theme was built using [jekyll-theme-yat](https://github.com/jeffreytse/jekyll-theme-yat) as a starter. Many features of this original theme are still available so for more advanced options checkout the [documentation](https://github.com/jeffreytse/jekyll-theme-yat?tab=readme-ov-file#jekyll-yat-theme)
