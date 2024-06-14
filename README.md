# BLU Website

## Running locally

Running locally requires [jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/testing-your-github-pages-site-locally-with-jekyll) to be installed.

1. Clone the repo to your local machine.
2. In [Gemfile](./Gemfile), uncomment the line starting `gem "jekyll" ...`
3. In [Gemfile](./Gemfile), comment out the line starting `gem "github-pages" ...`
4. run `bundle install`
5. run `bundle exec jekyll serve`
