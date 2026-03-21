# Academic GitHub Pages Site

This repository is a plain Jekyll website designed for a plant genomics postdoctoral researcher and structured for a GitHub user site.

## Edit the content

Update these files to personalize the site:

- `_data/profile.yml`
- `_data/home.yml`
- `_data/news.yml`
- `_data/publications.yml`
- `_data/activities.yml`
- `_data/projects.yml`
- `_data/contact.yml`

Replace the placeholder CV PDF at `assets/files/cv.pdf`.

## Deploy as a GitHub user site

1. Create or rename the repository to `<your-github-username>.github.io`.
2. Push this repository to the default branch.
3. In GitHub, open **Settings > Pages** and ensure deployment is set to **Deploy from a branch** using the default branch root.
4. Leave `_config.yml` with `baseurl: ""` for a user site.

## Optional local preview

If you have Ruby and Bundler installed:

1. Create a `Gemfile` with Jekyll or GitHub Pages dependencies if you want local builds.
2. Run `bundle exec jekyll serve`.

This site does not require a build step on GitHub Pages.
