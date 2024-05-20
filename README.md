Linux shell script that uses ffmpeg to create palettes from files in the current directory, then ImageMagick to enhance them.

![](exemple_files/Palettes/gorochu_exemple_palette.png)
![](exemple_files/Palettes/uranus_exemple_palette.png)

setup :		$ sudo apt-get install ffmpeg magick
usage (positional) :		$ ./pic2pal [number_of_colors] [transparency] [size]
options :
'number_of_colors' takes '1' to '256' (default is '256')
'transparency' take '0' (no) or '1' (yes) (default is '0')
		the transparency color is added to the colors
		useful to create ready-to-use palettes, like for a filter
 'size' is both horizontal and vertical, because we are busy creating squares here!
 exemple :		$ ./pic2pal 32 1 500
 will create a 500x500 33 colors palettes (32 + transparency) for every image in the current directory

sorry for the french lol (>'.')>
à ajouter
possibilité de crop automatiquement avec trim
possibilité d'ajouter une compression sans perte des PNG
autre méthodes de construction de palettes
autres colorspace
en go à tester pour de futurs améliorations :
sudo apt-get install golang && go get -u github.com/mccutchen/palettor && palettor -help
