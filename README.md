# DSPIRA Lessons

This is a website that provides instructions for designing and using a horn telescope through the Digital Signal Processing in Radio Astronomy (DSPIRA) project. Visit it at https://wvurail.org/dspira-lessons/

## Local Development

Follow these steps to work on the website and view a preview locally.

Clone the repository:

```sh
git clone https://github.com/WVURAIL/dspira-lessons
cd dspira-lessons
```

Configure a virtual environment:

```sh
bundler config set --local path 'vendor'
```

Install dependencies and serve. Make sure you have Ruby headers installed (the `ruby-dev` package on Debian).

```sh
bundle install
bundle exec jekyll serve # pass --watch for live reloads
```

The web server will run at http://localhost:4000

## Adding a New Post

[New Post](https://wvurail.org/dspira-lessons/newpost/)
