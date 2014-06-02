### gulp-rename-git

#### Install

```
npm install gulp-rename-git
```

#### Example use

```
var gulp = require('gulp'),
    gitRename = require('./index');

gulp.task('default', function() {
  return gulp.src('./src/*.js')

    // Look here
    .pipe(gitRename(function(path, gitHash) {
      path.dirname = '/' + gitHash + '/js/';
    }))

    .pipe(gulp.dest('./dist'));
});
```
