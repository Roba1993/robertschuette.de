# :tada: Creating a DIY Blog

Originally my plan was to post some technical conent over Medium. But due to the paywall which was introduced and the genreal development of the Medium platform, I looked around for an alternative. I found nothing really matching to my requirements, which as so often mean I will do it on my own. My requiements and goals for this project are the following:

* Able to create blog-posts directly from a markdown file
* Integrated into my Single Page Application (SPA) website
* Minimal footprint to keep the website small and performant
* No additional development tools needed / I can makes changes from everywhere

I already had this website you are actually on. It only had the top parts with references to GitHub & LinkedIn and some genreal information. I quiete like the look of it, because its matching to my actual swiss location. 

The idea is to develop an Apple like scroll behavior which brings the user seamlessly to the blog by simply scrolling or clicking on the blog icon. User not interested in the blog keep still the same minimalistic website as before.
So the first step is to create a small scroll logic, to move the elements nicely when a user scrolls, to actually see the blog.
Furthermore the main page of the site, should be made smaller to give more space to the blog itself. This was archived by the following code

<div class="code"><iframe
  src="https://carbon.now.sh/embed/5sOxoxtcdsDkvpkVsNrB"
  style="width: 327px; height: 200px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe></div>

The have something to scroll towards I just some white tiles with rounded corner to present the single blog posts in.
With this dummy data in place the next step is to format the markdown to renderable html code.
This is done by the <https://github.com/showdownjs/showdown> library, because they have pre-build `.min.js` files and github icon support :muscle:.
The only downside here is that the library seems a bit not supported over the last year. But a working markdown formatter will just work, once done...
The development Code is inserted over <https://carbon.now.sh/> website which is creating the beatiful code views. If anyone has a small library running in the browser, please let me know!

### :construction: The second part of the post will follow soon...
