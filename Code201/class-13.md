# Reading Assignment 13

## The Past, Present, and Future of Local Storage for Web Applications

---

- Having persistent local storage is one of the areas that native client programs have an advantage over web applications. For native programs, the OS will usually provide a layer of abstraction to store and retrieve any data that is specific to the program like preferences or a runtime state that are typically stored in a registry, an INI file, or an XML file. And if the program needs local storage beyond key/value pairs then you can embed your own database, invent a file format, or any number of other solutions.
- Now, historically web applications have had none of these options and while cookies were invented early on in the web's history they are limited by three downsides;
  - Cookies are included with every HTTP request which slows the web app down
  - Cookies, also because they are included with every HTTP request send the data unencrypted unless the entire web app is served with SSL
  - Cookies have a 4KB space limit which is enough to slow down the app, but not enough to be useful.
- In essence, what developers want is;
  - A lot of storage space
  - Is on the client
  - It persists beyond a page refresh
  - It isn't transmitted to the server
- And before HTML5 the ways to try and get these were unsatisfactory in many ways.

### Before HTML5

---

- In the beginning, the winner of the first browser war, Internet Explorer had one of the first attempts at this, DHTML Behaviors and one of them was `userData` which allowed web pages to store 64KB of data in an XML structure with trusted domains called intranet sites being able to store 10 times that at 640KB. However, there was no permissions dialog and no way of increasing the storage allowed.
- Then in 2002, Adobe introduced a new feature with Flash 6 that had the unfortunate name of 'Flash Cookies'. They allow Flash objects to store up to 100KB per domain, then Brad Neuburg developed an early prototype of a JS to Flash bridge but was limited by the design quirks of Flash and by 2006 with the rise of `ExternalInterface` with Flash 8 accessing the LSOs from JS became easier and faster. After this Brad rewrote his prototype and integrated it with the Dojo Toolkit and allowed 100KB free with a prompt for each order of magnitude larger.
- After that in 2007, Google launched the browser plugin Gears that was aimed at providing additional capability in browsers. It provided an API to run an embedded SQL database that allowed unlimited amounts of data per domain.
- While this was happening, Brad and others were still working on a way for his program dojox.storage to be a unified interface for all the different plugins and APIs and by 2009 it could detect and use Flash, Gears, AIR, and an early prototype of HTML5 storage on early versions of Firefox.
- While reading about this, a pattern emerges that they are all specific to one browser or relient on a plugin and despite efforts to bridge the gap, they all were different in many ways which HTML5 desired to fix by providing a standard, natively available option.

### HTML5

---

- HTML5 storage, otherwise called `Web Storage` is a way for browsers to store named key/value pairs locally within the web browser and like cookies the data persists afterwards. And unlike cookies the data isn't transmitted to the web server unless specifically coded to do so.
- Within the JS code to access it you simply access the `localStorage` object on the `window` object.
- HTML5 storage is based on named key/value pairs that can support any type of data supported by JS but is still stored as a string.
- Using the `setItem()` function with a named key will silently overwrite the previous value and calling `getItem` with a non-defined key will return `null` rather than an error.
- To keep track of the changes, you can trap the `storage` event that is fired by the window object whenever one of the used functions is called and changes something.
- Now, there are some limitations to this;
  - Each origin gets 5MB by default
  - And at the time of the article being written the only browser that allows this limit to be raised is through individual user action within certain browsers.
- So, what is beyond these named key/value pairs?
  - Well, one vision is SQL but SQL is more of a marketing term than strict identifier with tons of different databases being different.
  - Another is the Indexed Database API. This API uses what is called an `object store` that is similar to SQL but has no structured query language.
