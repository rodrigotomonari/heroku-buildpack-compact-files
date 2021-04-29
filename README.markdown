# Compact Files Buildpack

A simple buildpack to compact files.

## Usage

```
# .buildpacks
https://github.com/heroku/heroku-buildpack-nodejs
https://github.com/heroku/heroku-buildpack-ruby
https://github.com/rodrigotomonari/heroku-buildpack-compact-files
```

The `.slug-compact` file supports single-file and single-directory
declarations, e.g.:

```
some_huge_file.psd
some/nested/directory
why_does_this_app_even_contain_a.tiff
```