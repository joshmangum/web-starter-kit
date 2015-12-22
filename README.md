
## Getting started

Clone repository to new location, or use the zip file.

Type `$ npm install` in directory.

### Make git repository and add to Github

Visit https://github.com/new and add repository name [repo].

Create the git repository and set it's remote to the new github repo.
```
git init
git add .
git commit -m "First commit"
git remote add origin https://github.com/[user]/[repo].git
git remote -v
git push origin master
```

Then type: `$ gulp deploy` to push to Github Pages.



### Normal development cycle guide

1. Run `$ gulp serve` to write, debug, and test feature locally.
2. Use gulp clean first to remove `dist` directory. Then commit code normally.
```
gulp clean
git add .
git commit -m "a change message"   
git push origin master
 ```
3. Run `$ gulp deploy` to build `dist` directory and push it to gh-pages branch.

## Original docs

View original [documentation](https://github.com/google/web-starter-kit) for more details.  

## Github Pages deployment setup

Changes from .6 version of google-web-starter-kit to make Github Pages deployment work.

### Add gulp-subtree and vinyl-paths
```
npm install --save-dev gulp-subtree
npm install --save-dev vinyl-paths
```
### Remove `dist` from `.gitignore` and delete contents

New .gitignore:
```diff
  node_modules
+#dist
- dist
 .tmp
 app.yaml
```
Delete `dist` directory contents
```
rm -rf dist/*
```

### Delete existing gh-pages branch

There's an existing branch in the tree.
`$ git push origin --delete gh-pages`

### See commit history for changes to gulp file

Added deploy task

### Usage

1. Run `$ gulp deploy`.
2. Visit `http://[your-username].github.io/[repo-name]`.

### References

- See [gulp-subtree](https://github.com/Snugug/gulp-subtree) for details on changing the branch and commit message.
- See [GitHub Pages documentation](https://help.github.com/categories/20/articles) for features such as custom domains.
