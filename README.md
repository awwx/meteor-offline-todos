# Offline "todos" Example

This is the
[Meteor "todos" example](https://github.com/meteor/meteor/tree/release/0.6.5/examples/todos)
modified to use
[offline data](https://github.com/awwx/meteor-offline-data).


## Run Using Meteorite

```
$ git clone git://github.com/awwx/meteor-offline-todos.git
$ cd meteor-offline-todos
$ mrt install
$ meteor
```


## Changes

* In [server/publish.js](https://github.com/awwx/meteor-offline-todos/blob/master/server/publish.js#L17),
  publish all "todos" so that the todos for all lists are available
  when offline.

* Use [`new Offline.Collection` instead of `new Meteor.Collection`](https://github.com/awwx/meteor-offline-todos/blob/master/client/todos.js#L4).

* Use [`Offline.subscribe` instead of `Meteor.subscribe`](https://github.com/awwx/meteor-offline-todos/blob/master/client/todos.js#L25).

* Subscribe to [all todos](https://github.com/awwx/meteor-offline-todos/blob/master/client/todos.js#L34).
