# Personal website

The site uses Jekyll with the existing HTML and CSS. Both pages use
`_layouts/default.html`, `_includes/profile.html`, and `_includes/navigation.html`.
Edit the shared profile in `_includes/profile.html`. Research content lives in
`index.html`; talk entries live in `slides/index.html`.

## Preview locally

With Ruby installed, install the Bundler version used by the lockfile, then run:

```sh
gem install bundler -v 2.4.22
bundle install
bundle exec jekyll serve
```

Open <http://localhost:4000>. To build without serving, run
`bundle exec jekyll build`; the generated files are written to `_site/`.

## Publish

For GitHub Pages' **Deploy from a branch** mode, select the source branch and
`/(root)` in the repository's Pages settings. GitHub builds Jekyll on each push
to that branch. Commit the source files rather than the generated `_site/`.
If Pages uses a custom GitHub Actions workflow, that workflow must build Jekyll
before deploying `_site/`.
