This page is intended for developers of the Carrollton Manor website (carrolltonmanor.github.io, carrolltonmanor.com).

# Backlog

This is a list of ideas for improvement to the website and associated tools.

* add wait list for boat slips - get list from Don Price; application for the wait list; application for beach key ('pier' tab for those three?)
* check analytics; add access to the carrolltonmanorweb@gmail.com email, and tell Lisa what I find
* for events, click-to-add to google calendar?
* RSS?
* username/pw login access to security cameras, or read-only access?
* set up private login section for kid babysitting signups?, etc.
* calendar of events?
* put newsletter stories on the web?
* google map for quick view of our community

# Using Jekyll with Pages

This site uses Jekyll, a static website builder.  It is tightly integrated with Github Pages.

See https://help.github.com/articles/using-jekyll-with-pages for more on using Jekyll with Github Pages.  Notably:

Execute
	
    bundle exec jekyll serve [--detach]

in the root directory to build and serve the page.  Use

    bundle exec build --watch &

to build only.  Use

    bundle update

in the root directory to update jekyll dependencies.

For more on Jekyll and Github Pages:
http://jekyllrb.com/
http://jekyllrb.com/docs/usage/
https://help.github.com/articles/using-jekyll-with-pages#installing-jekyll
https://www.andrewmunsell.com/tutorials/jekyll-by-example/tutorial

# About the "Feeling Responsive" Jekyll Theme

[![Start Video](https://github.com/Phlow/feeling-responsive/blob/gh-pages/images/video-feeling-responsive-1280x720.jpg)](https://www.youtube.com/embed/3b5zCFSmVvU)

## A Responsive Jekyll Theme: *Feeling Responsive*

http://phlow.github.io/feeling-responsive

To get to know *Feeling Responsive* check out all the features explained in the [documentation][1].

And what license is *Feeling Responsive* released under? [This one][2].

## Why use this theme?

Feeling Responsive is heavily customizable.

1. Language-Support :)
2. Optimized for speed and it's responsive.
3. Built on Foundation Framework.
4. Six different Headers.
5. Customizable navigation, footer,...

**[More ›][3]**

## Video Tutorial

Click the image to [watch the YouTube-Video-Tutorial][4].

[![Start Video](https://github.com/Phlow/feeling-responsive/blob/gh-pages/images/video-feeling-responsive-tutorial-frontpage.jpg)](https://www.youtube.com/watch?v=rLS-BEvlEyY)

# Preparing Images

## Using ImageMagick to convert an image to another format:

    convert file.tif file.jpg

## Using ImageMagick to resize a file (for e.g. creating thumbnails):

    convert -resize x100 file.jpg file_thumb.jpg

## Examples

    (Replace all spaces with dashes)
    rename "s/ /-/" *
   
    (Convert all tifs to jpgs)
    for fn in `ls -1 *tif`; do pref=`echo $fn | awk 'BEGIN {FS="."};{print $1}'`; convert $pref.tif $pref.jpg; done

    (Create thumbnails from regular-sized jpgs)
    for fn in `ls -1 *jpg`; do pref=`echo $fn | awk 'BEGIN {FS="."};{print $1}'`; convert -resize x100 ${pref}.jpg ${pref}_thumb.jpg; done

    (Rename all files to 1.jpg, 2.jpg, etc.)
    i=1; for f in `ls -1`; do mv $f $i.jpg; ((i++)); done

# Posting a new Gallery page

Assuming new gallery with date YYYY-MM-DD and title this-title and number of photos = NUM_PHOTOS:

1. Grab post template:
    cp resources/post-templates/gallery.md _posts/gallery/YYYY-MM-DD-this-title.md

2. Replace title, TOTAL_PICS_NO, and FOLDER_NAME values within that new page.

3. Create folder images/YYYY-MM-DD-this-title; convert, rename, and create thumbnails (see above) so that you have filenames 1.jpg, 1_thumb.jpg, 2.jpg, 2_thumb.jpg, etc. in that folder.



 [1]: http://phlow.github.io/feeling-responsive/documentation/
 [2]: https://github.com/Phlow/feeling-responsive/blob/gh-pages/LICENSE
 [3]: http://phlow.github.io/feeling-responsive/info/
 [4]: https://www.youtube.com/watch?v=rLS-BEvlEyY
