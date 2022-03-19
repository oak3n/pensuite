# imagemadick
## about
ImageMagick is a suite of command-line utilities for modifying and working with images. ImageMagick can quickly perform operations on an image from a terminal, perform batch processing of many images, or be integrated into a bash script.

ImageMagick can perform a wide variety of operations. This guide will introduce you to ImageMagick’s syntax and basic operations and show you how to combine operations and perform batch processing of many images.

## install
`sudo apt-get install imagemagick`

## use
### convert
convert png to jpg
`convert image.png image.jpg`

specify compression level for jpeg images
`convert image.png -quality 95 image.jpg`
*1 <= level <= 100*

resize image
`convert image.png -resize 200x100 image.png`

force resize (disregards aspect ratio)
`convert image.png -resize 200x100! image.png`
*you can input height, width, or heightxwidth*

rotate image
`convert image.jpg -rotate 90 image-rotated.jpg`

apply effects, ex. charcoal, implode
`convert image.jpg -charcoal 2 image-charcoal.jpg`
*`charcoal` is the effect and `2` is the strength*

**these operations can be combined**
`convert image.png -resize 400x400 -rotate 180 -charcoal 4 -quality 95 image.jpg`

batch processing
`for file in *.png; do convert $file -rotate 90 rotated-$file; done`
*the makings of a meme virus payload?*

### identify
print image specific properties (format, colorspace, channel information etc.)
`identify -verbose image.png`

## links
- [how to geek article](https://www.howtogeek.com/109369/how-to-quickly-resize-convert-modify-images-from-the-linux-terminal/)

