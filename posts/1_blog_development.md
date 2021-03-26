2021-03-26 by Robert Schütte 
# :tada: Creating a DIY Blog

Originally my plan was to post some technical conent over Medium. But due to the paywall which was introduced and the genreal development of the Medium platform, I looked around for an alternative. I found nothing really matching to my requirements, which as so often mean I will do it on my own. My requiements and goals for this project are the following:

* Able to create blog-posts directly from a markdown file
* Integrated into my Single Page Application (SPA) website
* Minimal footprint to keep the website small and performant
* No additional development tools needed / I can makes changes from everywhere

I already had this website you are actually on. It only had the top parts with references to GitHub & LinkedIn and some genreal information. I quiete like the look of it, because its matching to my actual swiss location. 

The idea is to develop an Apple like scroll behavior which brings the user seamlessly to the blog by simply scrolling or clicking on the blog icon. User not interested in the blog keep still the same minimalistic website as before. So the first step is to create a small scroll logic, to move the elements nicely when a user scrolls, to actually see the blog. Furthermore the main page should be made smaller to give more space to the blog itself. This was archived by the following simple code.

<div class="code"><iframe
  src="https://carbon.now.sh/embed/5sOxoxtcdsDkvpkVsNrB"
  style="width: 400px; height: 268px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe></div>

To have something to scroll towards, I just added some white tiles with rounded corner to present the single blog posts in. With this dummy data in place the next step is to format the markdown to renderable html code. This is done by the <https://github.com/showdownjs/showdown> library, because they have pre-build `.min.js` files and github icon support :muscle:. The only downside here is that the library seems a bit not supported over the last year. But a working markdown formatter will just work, once done... Be aware that, icons etc. need to be activated like the following.

<div class="code"><iframe
  src="https://carbon.now.sh/embed/XgJOUdoEYC8XhZDOt6a8"
  style="width: 572px; height: 296px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe></div>

The development Code is inserted over <https://carbon.now.sh/> website which is creating the beatiful code views. If anyone has a small library running in the browser, please let me know!

Last step is to actually load the posts from the server. This is done by a simple javascript fetch function, which pulls posts as markfown files. Afterwards they are getting converted to html as mentioned above. To let the system know, which files to pull, I created an array with the markdown file names. This looks like the following.

<div class="code"><iframe
  src="https://carbon.now.sh/embed/K25BsMymjt8mFPTfBUB6"
  style="width: 1010px; height: 450px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe></div>

Last but not least all this need to get managed and I want to be able to post something easily to the new block. Writing is done in markdown files, wich allows me create them in an easy matter. Whenever I want to make or update a post I just do it. Afterwards a simple commit to Github is enough to ket all that going. With the push towards Github an action-workflow is automatically triggered, which is uploading the data automatically to my website via FTP. The action is defined like the following.


<div class="code"><iframe
  src="https://carbon.now.sh/embed/CMKcBdw7M3tv0FjA4Bsx"
  style="width: 546px; height: 500px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe></div>

These are of course only the important parts of the blog. If you are interested in more details, have a look to the public reposity of this website here <https://github.com/Roba1993/robertschuette.de>