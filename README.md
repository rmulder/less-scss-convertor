less-scss-convertor
-------------------

This npm package will convert all your less files to scss.

Installation
-------------

Install it via npm:-

```sh	
npm install -g less-scss-convertor
```
Usage
------
Go to the folder where you have less files, and run the below command in the terminal.
```sh
>less-scss-convertor filename1,filename2,filename3
```
It will convert all the files and will store all the converted files in the scss named folder inside the current directory of the given input files.

If you have bunch of less files in the Directory then you can run the command on the directory as well

```sh
>less-scss-convertor directory
```
It will store all the files in the scss folder inside the current directory. It can work with multiple directories like
```sh
>less-scss-convertor directory1,directory2
```
Further Usage
-------------
Now the awesome usage which is multiple files inside different directory. It can handle this case also pretty well. In this case run the below command.
```sh
>less-scss-convertor directory1/file1,directory2/file2
```
It will convert the file and store it in directory1/scss/file1.scss and directory2/scss/file2.scss respectively.

Extended Functionality
-----------------------
If you want to replace the existing file instead of creating new files then you can do that also.

```sh
>less-scss-convertor filename1,filename2 replace
```
You have to add an extra commanline parameter replace for the same and it will replace the existing file.

Probable Errors
----------------
You can find this below error sometimes. This error is because your folder don't have the permissions. Try run chmod at the folder.(In the below case the folder is 'skins/default/scss'. So to fix it we have to run **chmod skins/default/scss**)

```sh
Error: EEXIST, file already exists 'skins/default/scss/'
    at Object.fs.mkdirSync (fs.js:642:18)
```

Another error you can face when you will run
```sh
>less-scss-convertor directory
```
which is
```sh
Error: EISDIR, illegal operation on a directory
    at Object.fs.readSync (fs.js:476:19)
    at Object.fs.readFileSync (fs.js:310:28)
```
This error is because there is some other directory in the specified directory. Please make sure when you are putting the directory name there should be no other directory inside it.

Licence
--------
Copyright (c) 2014, Tarun Chaudhary (http://curioustechie.in)

Permission to use, copy, modify, and/or distribute this software for any purpose with or without fee is hereby granted, provided that the above copyright notice and this permission notice appear in all copies.

THE SOFTWARE IS PROVIDED "AS IS" AND THE AUTHOR DISCLAIMS ALL WARRANTIES WITH REGARD TO THIS SOFTWARE INCLUDING ALL IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS. IN NO EVENT SHALL THE AUTHOR BE LIABLE FOR ANY SPECIAL, DIRECT, INDIRECT, OR CONSEQUENTIAL DAMAGES OR ANY DAMAGES WHATSOEVER RESULTING FROM LOSS OF USE, DATA OR PROFITS, WHETHER IN AN ACTION OF CONTRACT, NEGLIGENCE OR OTHER TORTIOUS ACTION, ARISING OUT OF OR IN CONNECTION WITH THE USE OR PERFORMANCE OF THIS SOFTWARE.
