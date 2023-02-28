# Tool-Steganography
Steganography is hiding a file or a message inside of another file , there are many fun steganography CTF challenges out there where the flag is hidden in an image , audio file or even other types of files. Here is a list of the most tools I use and some other useful resources.
## Exiftool
Sometimes important stuff is hidden in the metadata of the image or the file , exiftool can be very helpful to view the metadata of the files.
<p>Useful commands:
<br><code class="language-plaintext highlighter-rouge">sudo apt-get install exiftool</code> : use to install exiftool 
<br><code class="language-plaintext highlighter-rouge">exiftool file</code> : shows the metadata of the given file</p>

<img style="display: block;-webkit-user-select: none;margin: auto;cursor: zoom-in;background-color: hsl(0, 0%, 90%);transition: background-color 300ms;" src="https://linuxhint.com/wp-content/uploads/2020/02/1-3.png" width="629" height="562">

## Steghide
Steghide is a steganography program that hides data in various kinds of image and audio files , only supports these file formats : JPEG, BMP, WAV and AU. but it’s also useful for extracting embedded and encrypted data from other files.
<p>Useful commands:

- use to install the steghide

```
sudo apt-get install steghide
```

- displays info about a file whether it has embedded data or not.

```
steghide info file
```

- extracts embedded data from a file

```
steghide extract -sf file
```
<img style="display: block;-webkit-user-select: none;margin: auto;cursor: zoom-in;background-color: hsl(0, 0%, 90%);transition: background-color 300ms;" src="https://miro.medium.com/v2/resize:fit:720/format:webp/1*T_QGzFDccUfRbBbyVl5PIw.jpeg" width="629" height="247">

## Stegsolve
Sometimes there is a message or a text hidden in the image itself and in order to view it you need to apply some color filters or play with the color levels. You can do it with GIMP or Photoshop or any other image editing software but stegsolve made it easier. it’s a small java tool that applies many color filters on images.

- steps to install stegsolve

```
wget http://www.caesum.com/handbook/Stegsolve.jar -O stegsolve.jar
chmod +x stegsolve.jar  
```
- use to stegsolve
```
java -jar stegsolve.jar
```

