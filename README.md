gulp-lodash-template
====================

> gul plugins will precompile lodash templates into function，supports JST, AMD and CommonJS output

> Precompile lodash.template to a function.

## Install
```
npm install gulp-lodash-template --save-dev
```

## Example
### `gulpfile.js`
```js
var template = require('gulp-lodash-template');

gulp.task('tmpl', function() {
  return gulp.src('./tmpl/*.html')
    .pipe(template({
      commonjs: true,
      // amd: true,
      strict: true
    }))
    .pipe(gulp.dest('./tmpl/'));
});
```

### template(options)

### options

Type: `Object`

#### options.strict
Type: `Boolean`
Default: false

Add `use strict;` at the first line of the compiled template function.

#### options.es6module
Type: `Boolean`
Default: false

#### options.commonjs
Type: `Boolean`
Default: false

#### options.amd
Type: `Boolean`
Default: false

#### options.namespace
Type: `String`
Default: 'JST'
