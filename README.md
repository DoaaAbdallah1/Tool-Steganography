# Tool-Steganography
Steganography is hiding a file or a message inside of another file , there are many fun steganography CTF challenges out there where the flag is hidden in an image , audio file or even other types of files. Here is a list of the most tools I use and some other useful resources.
## Exiftool
Sometimes important stuff is hidden in the metadata of the image or the file , exiftool can be very helpful to view the metadata of the files.
<p>Useful commands:
<br><code class="language-plaintext highlighter-rouge">sudo apt-get install exiftool</code> : use to install exiftool 
<br><code class="language-plaintext highlighter-rouge">exiftool file</code> : shows the metadata of the given file</p>

<img style="display: block;-webkit-user-select: none;margin: auto;cursor: zoom-in;background-color: hsl(0, 0%, 90%);transition: background-color 300ms;" src="https://linuxhint.com/wp-content/uploads/2020/02/1-3.png" width="629" height="562">

- challenge [click here](https://drive.google.com/file/d/1ebn7YYpG8ZpryfwrRaSM_a3ZmQZT2ffU/view)

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

- challenge [click here](https://drive.google.com/drive/mobile/folders/1Ym7doxMOW658EyBehBCeVyYwgTgN9I79?usp=sharing)

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

- challenge [click here](https://play.cyberstart.com/downloads/W0169/lance-reno-boxes.jpg?Expires=1677769754&amp;Signature=ZlH5Ky7g1iswtTk11Gz8Du2JOYVVmUG8A0zR3N~CYJcwTAzfNRMCnopTl9joobrIGbKm6HsTWNx0z0VR6-dPTAr~N599SSjmYHwRCxcyn1AV6-IOYoODARVQ-JPyN8dRAQ3LeEaTFvySO94H8vaJxgXioH2QlT7R~vzg1YriJquhgerlnstQMkeD5UDmdZxYSD2Rplu5v5x57XeXg~3A-hmD-17mCIj8qe9LansW6~0Dx5nDa4HV0MiikzWnxWMj3aMs-lVkNJPBZWYNhdLTwK9ermEfsl7u0~PNdCOKORBo-t99~9o2axSxqSGTT9ie8tE4VOvaEmR08dnxtE6T8A__&amp;Key-Pair-Id=K27W57836V8L1J)

## Zsteg
To extract data inside png and bmp files.

- steps to install

```
apt-get install -y ruby-dev
gem install rake
gem install zsteg
```
- Example

```
# zsteg flower_rgb3.png

imagedata           .. file: 370 XA sysV pure executable not stripped - version 768
b3,rgb,lsb,xy       .. text: "SuperSecretMessage"
```
- Challenge [click here](https://play.picoctf.org/practice/challenge/305?category=4&page=4)

 ## Binwalk
 Hiding files within other files.
 - to install tool :
  ```
  <br><code class="language-plaintext highlighter-rouge">sudo apt-get install binwalk</code> 
  ```
- To extract, use <code class="language-plaintext highlighter-rouge">binwalk -e File_name</code> .  
- To extract all files, run <code class="language-plaintext highlighter-rouge"> binwalk --dd='.*' [filename]</code> .
  
 <img style="display: block;-webkit-user-select: none;margin: auto;cursor: zoom-in;background-color: hsl(0, 0%, 90%);transition: background-color 300ms;" src="https://hackinglethani.com/wp-content/uploads/2018/09/1-5.png" width="629" height="272">
  
 - challenge [click here](https://ctflearn.com/challenge/108/8406)

## Stegseek
<p dir="auto">Stegseek is a lightning fast steghide cracker that can be used to extract hidden data from files. It is built as a fork of the original steghide project and, as a result, it is <em>thousands of times</em> faster than other crackers and can run through the entirety of <strong><code>rockyou.txt</code>* in under 2 seconds.</strong></p>
<img style="display: block;-webkit-user-select: none;margin: auto;cursor: zoom-in;background-color: hsl(0, 0%, 90%);" src="https://raw.githubusercontent.com/RickdeJager/stegseek/master/.demo/crack.gif" width="629" height="205">

<p dir="auto">On recent Ubuntu and other Debian-based systems, you can use the provided <code>.deb</code> package for installation:</p>
<ol dir="auto">

<li>Download the latest <a href="https://github.com/RickdeJager/stegseek/releases">Stegseek release</a></li>
<li>Install the <code>.deb</code> file using <code>sudo apt install ./stegseek_0.6-1.deb</code></li>
</ol>

- <strong>use tool</strong> :

```
stegseek [stegofile.jpg] [wordlist.txt]
```
- <strong>How to install rockyou.txt</strong> :[click here](https://www.geeksforgeeks.org/how-to-extract-rockyou-txt-gz-file-in-kali-linux/)

## Opensteg 
you can either hide the data (file) inside an image or extract the data from the image.
<h4>Hide data</h4>
<img style="display: block;-webkit-user-select: none;margin: auto;cursor: zoom-in;background-color: hsl(0, 0%, 90%);transition: background-color 300ms;" src="https://www.openstego.com/image/screenshot/01.png" width="629" height="366">
<h4>Extract data</h4>
<img style="display: block;-webkit-user-select: none;margin: auto;cursor: zoom-in;background-color: hsl(0, 0%, 90%);transition: background-color 300ms;" src="https://www.openstego.com/image/screenshot/02.png" width="629" height="366">

- install openstego :[click here](https://github.com/syvaidya/openstego/releases/tag/openstego-0.6.1)

- use to openstego

```
java -jar openstego.jar
```

## Sheet 1

[Challenge 1](https://ctflearn.com/challenge/108)

[Challenge 2](https://cybertalents.com/challenges/forensics/hidden-message)

[Challenge 3](https://cybertalents.com/challenges/forensics/message-in-bottle)

[Challenge 4](https://cybertalents.com/challenges/forensics/i-love-images)

[Challenge 5](https://cybertalents.com/challenges/forensics/keep-it-simple)

[Challenge 6](https://cybertalents.com/challenges/forensics/hack-a-nice-day)

[Challenge 7](https://play.picoctf.org/practice/challenge/44?category=4&page=1)
