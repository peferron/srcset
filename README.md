# srcset

`srcset` is a bash script that generate scaled-down versions of an image, and the corresponding `<img srcset="...">` HTML.

Example:

```bash
$ ls -lS
total 7648
-rw-r--r--  1 peferron  staff  3913850 Mar  9 18:29 picture.jpg

$ srcset picture.jpg 500 1000 5000
Generated picture_500x500.jpg
Generated picture_1000x1000.jpg
Generated picture_2300x2300.jpg (full-size copy)

<img srcset="picture_500x500.jpg 500w,
  picture_1000x1000.jpg 1000w,
  picture_2300x2300.jpg 2300w"
  sizes=""
  src="picture.jpg">

<img> copied to clipboard.

$ ls -lS
total 18744
-rw-r--r--  1 peferron  staff  3913850 Mar  9 18:29 picture.jpg
-rw-r--r--  1 peferron  staff  3913850 Apr 12 19:16 picture_2300x2300.jpg
-rw-r--r--  1 peferron  staff  1358584 Apr 12 19:16 picture_1000x1000.jpg
-rw-r--r--  1 peferron  staff   402301 Apr 12 19:16 picture_500x500.jpg
```
