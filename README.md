# Kensei

It's a small client library to host a blog on github.io.
It was inspired by jekyll.
It is depending on showdown.

# How to use

- Create an index.html
- Add this container html snippet
```html
<div id="content-container">
    <div id="content"></div>
</div>
```
- Add the script for kensei
```html
<script src="https://rawgit.com/chrisakakay/kensei/master/dist/kensei.bundle.js"></script>
```
- Create a small initialization script
```javascript
var posts = [
    {
        date: '2018-01-01',
        short: 'my-new-blog',
        title: 'My new blog',
        desc: 'I gonna share funny stories here or discuss React vs Angular stuff ..'
    }
];

Kensei.app.init({
    posts: posts,
    disqus: {
        pageUrl: 'http://chrisakakay.github.io',
        disqusId: 'your-disquss-id'
    }
});
```
- Create a posts folder
- And create the posts you added in the posts variable (ex: 2018-01-01-my-new-blog.md)
- Thats it

# Notes

Kensei relies on showdown (a markdown parser) and kensei.bundle.js contains it by default.
You can use kense.min.js which is without showdown, but you have to include showdown yourself.
Kensei relies on showdown version 1.4.3 because it is small.

# API

Kensei.app.init can take some options like:
* posts (an array of the visible posts)
* pagination.postPerPage (optional, default is 4)
* disqus.pageUrl (optional)
* disqus.disqusId (optional)
