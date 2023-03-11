# Blog

## Theme

[Hugo blog awesome](https://jamstackthemes.dev/theme/hugo-blog-awesome/)

### Install

```bash

git ls-files --stage themes/hugo-blog-awesome
git rm --cached themes/hugo-blog-awesome
git submodule add https://github.com/hugo-sid/hugo-blog-awesome.git themes/hugo-blog-awesome
```

### Remove

On windows use the following commands

```bash
# Remove the submodule entry from .git/config
git submodule deinit -f themes\ananke

# Remove the submodule directory from the superproject's .git/modules directory
rm .git\modules\themes\ananke -r -fo

# Remove the entry in .gitmodules and remove the submodule directory located at path/to/submodule
git rm -f themes\ananke
```