
add gulp-plumber
add vinylPaths


## Github Pages deployment

### Add gulp-subtree
```
npm install --save-dev gulp-subtree
```
### Remove `dist` from `.gitignore`

```diff
 node_modules
-dist
 .tmp
 app.yaml
```

### Remove `dist` and make gh-pages branch
```
rm -rf dist/*
```
## Usage

1. Run `$ gulp deploy`.
2. Visit `http://[your-username].github.io/[repo-name]`.


### References

- See [gulp-subtree](https://github.com/Snugug/gulp-subtree) for details on changing the branch and commit message.
- See [GitHub Pages documentation](https://help.github.com/categories/20/articles) for features such as custom domains.
