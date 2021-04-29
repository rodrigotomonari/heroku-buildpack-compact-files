# Pre-build Clean Buildpack

A simple buildpack to run before all other buildpacks, which removes a set
of files defined in `.slug-pre-clean`, so that they are not included in the
finished slug.

## Usage

The pre-build-clean buildpack **must** be the first one in the buildpack order:

```
# .buildpacks
https://github.com/rodrigotomonari/heroku-buildpack-pre-build-clean
https://github.com/heroku/heroku-buildpack-nodejs
https://github.com/heroku/heroku-buildpack-ruby
```

The `.slug-pre-clean` file supports single-file and single-directory
declarations only, e.g.:

```
some_huge_file.psd
some/nested/directory
why_does_this_app_even_contain_a.tiff
```