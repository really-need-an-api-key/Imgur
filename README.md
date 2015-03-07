##About

This is a 100% Bash script used to download imgur albums while making sure that
the order of the pictures is retained.

Author:  
    manabutameni  
    https://github.com/manabutameni/Imgur

##Usage

    bash imgur.sh [-sd] URL [URL]

    OPTIONS
        -h       Show this message.
        -s       Silent mode. Overrides debug mode.
        -d       Debug mode.

Multiple albums can be downloaded like so: `bash imgur.sh URL1 URL2 ...`

##Requirements

  * [jsawk](https://github.com/micha/jsawk)
  * [iconv](man7.org/linux/man-pages/man1/iconv.1.html)
  * [curl](http://curl.haxx.se/)


##Installation

This is only necessary if you want to run the script without having it in the
same folder you want the imgur album, or if you want to install imgur.desktop
for KDE.

    curl -L https://raw.github.com/manabutameni/Imgur/master/imgur.sh -o /usr/local/bin/imgur
    chmod +x /usr/local/bin/imgur

NOTE: This assumes you have /usr/local/bin/ in your $PATH

After you have installed the script with this method you can always update to
the latest version of the script with the following command:

    curl -L https://raw.github.com/manabutameni/Imgur/master/imgur.sh -o /usr/local/bin/imgur

To use:  
In any directory type: `imgur imgur.com/a/XXXXX`  

#####KDE

Copy imgur.desktop to your local `kde4-config --path services` folder
location and make sure it's executable. `chmod +x imgur.desktop`.

To use: Copy the url of an imgur album into your clipboard and right
click on an empty area in dolphin. Under actions you should see "Imgur
Album DL".

NOTE: This will only work if you have installed the script in the
Installation part of this readme.

##### What this script does not do

This script will not update an album. For example, if there's an album
that is frequently updated that you enjoy following, this script (by
design) cannot and will not update that album with the newest images.
This is to prevent clobbering existing files when a directory already
exists, e.g. "Pictures".
