# How this blog is developed

Originally my plan was to post some technical conent over Medium. But due to the paywall which was introduced and the genreal development of the Medium platform, I looked around for an alternative. I found nothing really matching to my requirements, which as so often mean I will do it on my own.

I already had this website, which just acted as a reference to GitHub & LinkedIn, with some genreal information. The look is something which is quiete matching to my actual swiss location and should stay. So in the first step, I will create a small scroll logic, to move the elements nicely when a user scrolls, to actually see the blog.

This is done over
```javascript
// todo code for scroll
```

Afterwards I just created some white tiles with rounded corner to present the single blog posts in.
The data for the blogposts are defined as simple markdown files, which are located on the same web-server.
These markdown files getting loaded from an hard coded array in the `index.html` file, mentioning all blog posts.

In the final step I'm using the <https://github.com/showdownjs/showdown> library to convert the markdown files into valid html, directly in the browser.
