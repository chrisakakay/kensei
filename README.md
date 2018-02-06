# Kensei

It's a small client library to host a blog on github.io.

It was inspired by [jekyll](https://github.com/jekyll/jekyll).

It is depending on [showdown](https://github.com/showdownjs/showdown).


## How to use

- Create an index.html
- Add this container html snippet
```html
<div id="content"></div>
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

Kensei.app.init({ posts: posts });
```
- Create a __posts__ folder
- And create the posts you added in the posts variable (ex: __2018-01-01-my-new-blog.md__)
- Thats it


## Notes

The bundle __kensei.bundle.js__ contains showdown by default.

You can use __kense.min.js__ which is just the kensei library, but you have to include showdown yourself.

Showdown version 1.4.3 because it is small.


## API

Kensei.app.init can take some options like:
* __posts__ (an array of the visible posts)
* __container__ (optional, container for the posts to be rendered in, ex.: document.getElementById('my-container'))
* __pagination.postPerPage__ _(optional, default is 4)_
* __disqus.pageUrl__ _(optional)_
* __disqus.disqusId__ _(optional)_
