# Adding a news post

1. Go to https://github.com/carrolltonmanor/carrolltonmanor.github.io
2. Click Sign In; username:  carrolltonmanor; password = Hillb0tt0mBeach
3. Navigate to carrolltonmanor.github.io/_drafts/YYYY-MM-DD-news-post.md; select-all and copy the text
4. Create a new document (look for the plus sign) in carrolltonmanor.github.io/_posts/news/; use this format for the file name:

    YYYY-MM-DD-title-of-article.md

For example:

    2015-01-02-community-yard-sale.md

5. Paste the copied text into that new file
6. Add contents for the news post below the last "---"; see this cheatsheet for syntax help:  https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet 

# Using Jekyll with Pages

See https://help.github.com/articles/using-jekyll-with-pages for more on using Jekyll with github-pages.  Notably:

Execute
	
    bundle exec jekyll serve

in the root directory to build and serve the page.  Use

    bundle update
	
in the root directory to update jekyll dependencies.

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

# About the "Feeling Responsive" Theme

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


 [1]: http://phlow.github.io/feeling-responsive/documentation/
 [2]: https://github.com/Phlow/feeling-responsive/blob/gh-pages/LICENSE
 [3]: http://phlow.github.io/feeling-responsive/info/
 [4]: https://www.youtube.com/watch?v=rLS-BEvlEyY
 [5]: #
 [6]: #
 [7]: #
 [8]: #
 [9]: #
 [10]: #
