# [PHP] file to base64

[中文说明](https://github.com/wuyumin/File2base64/blob/master/README-CN.md)

base64 files are used for embedding in web pages.

### usage:

install in Composer

`composer require wuyumin/file2base64`

php code
```php
require __DIR__ . '/../vendor/autoload.php';

use File2base64\File2base64;

$file2base64 = new File2base64();
# $file2base64 = new File2base64(['bmp' => 'image/bmp']);

$file2base64->toFile('file2base64.png', 'file2base64.txt');
# echo $file2base64->toBase64('file2base64.png');
```

### result:

base64 file string
```html
data:image/gif;base64,R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw==
```

### HTML code use like this:

html code
```html
<img src="data:image/gif;base64,R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw==" alt="">
```
