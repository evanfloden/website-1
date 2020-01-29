# codecheckers.github.io

## Logo and badge

Find the source files for the CODE CHECK logo and badge in the following directories in this repository.

- `logo`
- `badge`

All graphics unless noted otherwise are published under a [Creative Commons Attribution 4.0 International license](https://creativecommons.org/licenses/by/4.0/) (CC BY 4.0).

## Website

See `Makefile` for commands to build and view the site locally.

If you want to override a file from the `minima-reboot` template, run `bundle info minima-reboot` to see where the bundle files are and copy it into this project.

- Jekyll GitHub pages: https://jekyllrb.com/docs/github-pages/
- `minima-reboot` theme: https://github.com/aterenin/minima-reboot

## Prerequisites

- `ruby` and `ruby-dev`
- gem `bundler`

## Preview and build

```
make preview
make build
```

## Deploy

We built the site using Travis CI, so we are not limited to the Jekyll features/plugins etc. supported by GitHub.

See https://tonyzhangnd.github.io/2018/06/Integrating-Jekyll-and-Travis-CI.html
The PAT is [encrypted for Travis CI](https://docs.travis-ci.com/user/encryption-keys/).

You can run the build locally with

```bash
TRAVIS_PULL_REQUEST=false TRAVIS_BRANCH=master TRAVIS_BUILD_NUMBER=local PAT="..." ./travis.sh
```

## License

Except where otherwise this repository is licensed under a [Creative Commons Attribution Share-Alike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/).

![CC-BY-SA 4.0](https://mirrors.creativecommons.org/presskit/buttons/88x31/svg/by-sa.svg)
