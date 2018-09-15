# About Chunk upload

**Chunk upload** is a simple web software written in jQuery (client side) and PHP (server side) that helps you to send large files divided into chunks to your web server. This software is open source developed under [**MIT License**](./LICENSE).

## Prerequisites
- Web server (Apache, Nginx or other)
- PHP 5+

## Features
- Very small code size
- Large files upload
- Multiple files upload
- Progress bar
- Download speed

## Installation
1. Upload the content of **src** folder to your web server
2. Create **temp** and **done** folders in the same folder as source files and set 777 rights on them (chmod 777 folder_name)
3. Set the following values in your **php.ini** configuration file:

- upload_max_filesize = 30M
- post_max_size       = 40M
- memory_limit        = 512M
- max_execution_time  = 600

## Configuration
- You can set chunk size in **upload.js** file editing the value "window.chunksize" at the beggining of this file. This size is written as number of bytes (default: 20971520 = 20 MB). This value has to be lower than the values **upload_max_filesize** and **post_max_size** in **php.ini**
- You can change **temp** and **done** folders in **upload.php** file (**temp** is for files that are being uploaded, **done** is for finished uploads)

## Files description
- **index.html** - Chunk uploader index page
- **style.css** - Style sheet file for index page
- **upload.js** - Client side jQuery script
- **upload.php** - Server side PHP script
- **upload-template.html** - HTML template describing progress bar and other elements of single uploaded file