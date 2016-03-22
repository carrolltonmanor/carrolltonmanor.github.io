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

    rename "s/ /-/" *
   
    for fn in `ls -1 *tif`; do pref=`echo $fn | awk 'BEGIN {FS="."};{print $1}'`; convert $pref.tif $pref.jpg; done

    for fn in `ls -1 *jpg`; do pref=`echo $fn | awk 'BEGIN {FS="."};{print $1}'`; convert -resize x100 ${pref}.jpg ${pref}_thumb.jpg; done

    for fn in `ls -1 halloween*.jpg`; do echo $fn; mv $fn ${fn//halloween/2008-10-31-CMIA-halloween_}; done


 [1]: http://phlow.github.io/feeling-responsive/documentation/
 [2]: https://github.com/Phlow/feeling-responsive/blob/gh-pages/LICENSE
 [3]: http://phlow.github.io/feeling-responsive/info/
 [4]: https://www.youtube.com/watch?v=rLS-BEvlEyY
