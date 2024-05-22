Linux shell script that uses FFmpeg to create palettes from files in the current directory, then ImageMagick to enhance them and optipng for lossless compression.


![](exemple_files/Palettes/gorochu_exemple_palette.png)
![](exemple_files/Palettes/uranus_exemple_palette.png)

setup :		$ sudo apt-get install ffmpeg magick optipng

usage (positional) :		$ ./pic2pal [number_of_colors] [transparency] [size]

options :

-n : number of colors : takes '1' to '256' (default is '256')

-t : add transparency color,	useful to create ready-to-use palettes, like for a filter
  
-s : size : lenght and height of the square palette generated (default is '1000' giving 1000x1000 *.png files)
		size is both horizontal and vertical, because we are busy creating squares here!

-f : force square : useful to have a predictable output

-c : finish with lossless compression of palettes

Exemple :	$ ./pic2pal -n 32 -t -s 1000 -f
			will create a 1000x1000 32 colors palettes (31 + transparency)
			for every image in the current directory

sorry for the french lol (>'.')>

à ajouter

x flags (done)

x possibilité de crop automatiquement avec trim (done)

x possibilité d'ajouter une compression sans perte des PNG (done)

- autre méthodes de construction de palettes

- en go à tester pour de futurs améliorations : $ sudo apt-get install golang && go get -u github.com/mccutchen/palettor && palettor -help

