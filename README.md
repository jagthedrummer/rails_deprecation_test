# README

A small repo to illustrate a problem with raising deprecation messages from inside templates.


* Pull down the repo
* Run a server with `rails s`
* Visit <http://localhost:3000>
* Check the console

You'll see a deprecation warning like this:

```
DEPRECATION WARNING: `deprecated_option` is deprecated. Please use `new_option` instead.
(called from public_send at .../actionview-7.0.8/lib/action_view/base.rb:244)
```

It points at Rails internals insted of at something in the app.

It would be nice if the message were more like:

```
DEPRECATION WARNING: `deprecated_option` is deprecated. Please use `new_option` instead.
(called from render at ./app/view/home/index.html.erb:4)
```
