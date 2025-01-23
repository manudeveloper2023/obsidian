
```php
return response()->json(
            [
                'message' => 'File uploaded successfully',
                'file' => $file->path(),
                'size' => $file->getSize(),
                'extension' => $file->extension(),
                'mime_type' => $file->getMimeType()

            ]
        );
        
{
    "message": "File uploaded successfully",
    "file": "/tmp/phpp47befsuajqneGEFflm",
    "size": 54532,
    "extension": "webp",
    "mime_type": "image/webp"
}
```
## Tags

##### #Laravel
##### #Laravel-Request