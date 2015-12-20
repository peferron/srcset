# srcset

`srcset` is a bash script that generate scaled-down versions of an image, and the corresponding `<img srcset="...">` HTML.

Example:

```bash
$ ls -lS
total 424
-rw-r--r--@ 1 peferron  staff  212277 Dec 17 09:22 picture.png

$ srcset picture.png
Generating picture_632w.png (full-size copy)
Generating picture_316w.png
Generating picture_158w.png
Generating picture_79w.png
Generating picture_39w.png

<img srcset="picture_632w.png 632w,
    picture_316w.png 316w,
    picture_158w.png 158w,
    picture_79w.png 79w,
    picture_39w.png 39w"
  sizes=""
  src="picture_632w.png">

<img> copied to clipboard.

$ ls -lS
total 1064
-rw-r--r--@ 1 peferron  staff  212277 Dec 17 09:22 picture.png
-rw-r--r--@ 1 peferron  staff  212277 Dec 20 03:35 picture_632w.png
-rw-r--r--  1 peferron  staff   68450 Dec 20 03:35 picture_316w.png
-rw-r--r--  1 peferron  staff   24952 Dec 20 03:35 picture_158w.png
-rw-r--r--  1 peferron  staff    9757 Dec 20 03:35 picture_79w.png
-rw-r--r--  1 peferron  staff    3964 Dec 20 03:35 picture_39w.png

```
