# Yifftag

### Description

When a joke with friends goes to far and you're a developer. Yifftag is a python program for adding e621 or inkbunny tags to your favorites foxes and kitten pictures. Its work by searching the md5 of each pictures on e621 and inkbunny API.

**Note : Program use Exif and its only work with jpg picture format.**

![alt text](http://image.noelshack.com/fichiers/2019/01/5/1546609791-yifftag.jpg "Yifftag")

### Requirements

* Python 3.5+
* Piexif
* Tkinter

If you're on Windows you can download a standalone executable build including all the requirements in releases section.

### Usage

**On Windows** for a classic usage, download the standalone version and run the executable file.

**On other platform**, clone or download the repository and launch `yifftag.py`. Be sure to fill all the requirements before.

Add your files and folders, choose your search parameters and click on Run.

You can also use console mode, for that you need to add `--nogui` tag in launch params. See the list below for all params :

```
usage: yifftag.py [-h] [--nogui] [-f FILE] [-d DIR] [--force] [--e621]
                  [--e621_u E621_U] [--inkbunny] [--inkbunny_u INKBUNNY_U]
                  [--inkbunny_p INKBUNNY_P] [--interval INTERVAL]

optional arguments:
  -h, --help            show this help message and exit
  --nogui               Toggle shell mode
  -f FILE, --file FILE  Image to tag (multiple file allowed separated by a
                        coma)
  -d DIR, --dir DIR     Folder containing images (multiple folder allowed
                        separated by a coma)
  --force               Force information check even if image is already
                        tagged
  --e621                Enable e621 search
  --e621_u E621_U       e621 username (recommended but not required)
  --inkbunny            Enable Inkbunny search
  --inkbunny_u INKBUNNY_U
                        Inkbunny username (required for fetching image where
                        artist disallow guest)
  --inkbunny_p INKBUNNY_P
                        Inkbunny password
  --interval INTERVAL   Limit time between two search request
```

### Build

For generating standalone version, we use `pyinstaller` on `yifftag.py` with this following parameters : `--onefile`, `--noconsole`

### Changelog

**version 1.0.2**
* Project Yiffdex renamed to Yifftag

**version 1.0.1**
* Multiple GUI change
* Force to have almost one folder/file to run yiffdex
* Fix crash when trying to open non JPEG file with .jpg extension
* Fix error when application logout of inkbunny in console mod
* Fix bug that add an empty line in list if you cancel the "Add folder"
* Fix bug where progress don't show correctly when picture is cached or marked

**version 1.0b**
* Add GUI

**version 0.2a**
* Add Inkbunny support
* Fix bugs when filename contains non ascii caracters

**version 0.1a**
* Initial version

### License

MIT License

Copyright (c) 2018, Noryx your fluffy dev :3

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
