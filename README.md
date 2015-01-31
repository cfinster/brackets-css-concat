Brackets CSS Concat
==================

FORKED FROM [Brackets JS Concat](https://github.com/smiclea/brackets-js-concat) to create CSS version

Concatenates a list of files into one big file, useful when using only one CSS file for debugging and/or deployment. The extension needs you to create a 'css.concat' file in your project root. This file will set the extension with a few mandatory options:

* concatOnSave - if true, concatenates the list of files when saving one of them or when saving 'css.concat' itself. Otherwise you have to always right click 'css.concat' -> 'Concatenate files'
* output - the path (relative to project root, directories will be created if necessary) where the big concatenated file should be placed
* -pathToFile; - the list of files (paths relative to project root) to concatenate

Here is an example of a 'css.concat' file:
```
// THIS file should be placed in project root

// if true, concatenates the list of files when saving one of them or when saving this file
concatOnSave = true;

// the output path of the concatenated file, directories will be created if necessary
output = build/build-v0.0.1.css;

// the list of files (paths relative to project root) to concatenate
-css/*.js;
-main.css;
```

Right-click on 'css.concat' to manually concatenate the files in the list, useful if 'concatOnSave' is false.

<b>Wildcard support</b>
* if the path to file ends with '/' character, all the files in that folder will be concatenated
* if the path to file ends with '\*' followed by a group of characters, only files ending in that group of characters will be concatenating (ex.: views/*.css matches all the files in views folder ending with '.css' i.e. all CSS files)

<i>0.0.1</i>
<ul>
<li>First release</li>
</ul>