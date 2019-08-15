# codecheckers.github.io

See `Makefile` for commands to build and view the site locally.

If you want to override a file from the `minima-reboot` template, run `bundle show minima-reboot` to see where the bundle files are and copy it into this project.

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