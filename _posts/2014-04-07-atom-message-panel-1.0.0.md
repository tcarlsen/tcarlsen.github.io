---
layout: post
title:  "Atom Message Panel 1.0.0"
date:   2014-04-07
category: atom
---

`npm publish 1.0.0` and here we are! I'm proud to say that I have just released [Atom Message Panel](https://github.com/tcarlsen/atom-message-panel) with a whole new API.

## Whats Atom Message Panel?

When I got my hands on [Atom](https://atom.io) I was trilled about the openness and I had to write some packages for it A:zap:

All of my packages had a message panel at the bottom of the screen for presenting output for the user in a nice way. But every time I had a good idea on how the panel could look even better I had to update the same daam code in all of my plugins.

Thats how I cam up with [Atom Message Panel](https://github.com/tcarlsen/atom-message-panel), a npm module that easely could be install as a dependency and then be required inside the atom package. :bowtie:

The code was not that pretty and the features was few, but it worked and it sovled my problem!

## 1.0.0

I did a post on [discuss.atom.io](http://discuss.atom.io/t/atom-message-panel/4112) about my module and I some positive feedback and feature ideas.

The big one was to port the code to extend the Atom View and that is exactly was 1.0.0 is all about! And I own a big thanks to @fangel for making this a reality! :joy_cat:

## Great, how do I get it?

Like any other npm module you can run `npm install atom-message-panel --save` and you are good to go!

**JavaScript example**

```javascript
var MessagePanelView = require('atom-message-panel').MessagePanelView,
    PlainMessageView = require('atom-message-panel').PlainMessageView;

var messages = new MessagePanelView({
  title: 'It\'s alive..... IT\'S ALIIIIIVE!!!!'
});

messages.attach();

messages.add(new PlainMessageView({
  message: 'I did it mommy, I made my first Atom Message Panel!',
  className: 'text-success'
}));
```

For full API visit the [repo on GitHub](https://github.com/tcarlsen/atom-message-panel).
