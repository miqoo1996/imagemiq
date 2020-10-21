PHP Libary Imagemiq
-------------------

The package was created by [Miqayel Ishkhanyan](http://imusthave.jermukcity.am) for php developers.

The package helps to work with images more easily.

This image upload package provides a lot of functions such as upload, resize, crop, rotate, delete.

How to use
-------------
1. composer require miqoo1996/imagemiq
2. HTML code
```
<form action="" method="post" enctype="multipart/form-data">
    Select image to upload:
    <input type="file" name="fileToUpload" id="fileToUpload">
    <input type="submit" value="Upload Image" name="submit">
</form>
```
3. PHP code
```
$obj = new \miqoo1996\imagemiq\image();

/**
 * Image types must be one of these.
 *
 * IMAGETYPE_PNG, IMAGETYPE_GIF, IMAGETYPE_JPEG
 */
$obj->load($_FILES['fileToUpload']['tmp_name'])
    ->resizeToWidth(500)
    ->save('destination/aaa.png', IMAGETYPE_PNG);
```
    
