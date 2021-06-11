PHP Libary Imagemiq
-------------------

The package helps to work with images easier, provides many functions such as image uploading, resizing, cropping, rotating, deleting.

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
 * Ex. you can use IMAGETYPE_PNG to convert the image from current format to PNG.
 */
$obj->load($_FILES['fileToUpload']['tmp_name'])
    ->resizeToWidth(500)
    ->save('destination/aaa.png', IMAGETYPE_PNG);


// Some additional methids may come in handy, follow the below examples.


$obj->load($_FILES['fileToUpload']['tmp_name']); // Or $obj->load('image/from/path.jpg');
$obj->scale(2); // new image resized by scaling
$obj->resize(10, 20) // resize the image by the specific width and height
$with = $obj->getWidth();
$height = $obj->getHeight();
```


Enjoy coding with the nice package!
