
# Web Storage
---

#### With web storage, web applications can store data locally within the user's browser.

#### Before HTML5, application data had to be stored in cookies, included in every server request. Web storage is more secure, and large amounts of data can be stored locally, without affecting website performance.

#### Unlike cookies, the storage limit is far larger (at least 5MB) and information is never transferred to the server.

#### Web storage is per origin (per domain and protocol). All pages, from one origin, can store and access the same data.


# TRACKING CHANGES
---
#### If you want to keep track programmatically of when the storage area changes, you can trap the storage event. The storage event is fired on the window object whenever setItem(), removeItem(), or clear() is called and actually changes something. For example, if you set an item to its existing value or call clear() when there are no named keys, the storage event will not fire, because nothing actually changed in the storage area.


## References:
---

[mozilla](https://developer.mozilla.org/)

