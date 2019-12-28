# librarian

for build bookmark HTML

## How to use

Create base file with Pug:

```pug
include ./mixins/bookmark.pug
include ./mixins/folder.pug
include ./mixins/root.pug

include ./includes/header.html
+root
  +folder(name="dir1")
    +bookmark(href="https://example.com/1") example1
    +bookmark(href="https://example.com/2") example2
    +bookmark(href="https://example.com/3") example3
    +folder(name="dir1-2")
      +bookmark(href="https://example.com/4") example4
  +folder(name="dir2")
    +bookmark(href="https://example.com/5") example5
  +folder(name="dir3")
```

and execute below:

```console
$ yarn build ./path/to/file.pug
```

## License

The MIT license.
