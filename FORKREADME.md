
### Add gulp-plumber to stop reload crashing
```
npm install --save-dev gulp-plumber
```


## Github Pages deployment

### Add gulp-subtree and vinyl-paths
```
npm install --save-dev gulp-subtree
npm install --save-dev vinyl-paths
```
### Remove `dist` from `.gitignore` and delete contents

```diff
  node_modules
+#dist
- dist
 .tmp
 app.yaml
```

```
rm -rf dist/*
```

### Make gh-pages branch

git branch gh-pages
git checkout gh-pages

### Usage

1. Run `$ gulp deploy`.
2. Visit `http://[your-username].github.io/[repo-name]`.

### Normal dev cycle

1. Run `$ gulp serve` to write, debug, and test locally.
2. Commit changes with git to master.
   ```
   git add .
   git commit -m "a change message"   
   git push origin master
   ```
3. Run `$ gulp deploy` to build dist and push it to gh-pages branch


### References

- See [gulp-subtree](https://github.com/Snugug/gulp-subtree) for details on changing the branch and commit message.
- See [GitHub Pages documentation](https://help.github.com/categories/20/articles) for features such as custom domains.
