# Reading Assignment 11

## HTML

---

### Images

- When using images in HTML, often the image doesn't completely fit the area you need it to fill or you want it to scale with the webpage. In these cases you use the `width` and/or `height` properties. It is also helpful when using multiple images on the same page of similar purpose so you set the size of all images to one default.
- Images can also be aligned horizontally and vertically with CSS.
- You can also set a background image for any box created by an HTML element.
  - The background image can appear only once or repeated multiple times in the background of a box.
  - Image rollover effects can also becreated by moving the background image in a box.
- Image sprites can used to reduce the number of images a page has to load.
  
### Practical Information

- If you are relying on users finding your site through the search engine, it helps to optimise your page and the information within it to make the site more likely to appear in the top results for a search query for a topic related to your site.
- A helpful tool for optimising your site is Google Analytics, which allows you to see how many people visit your site, how they find it, and what they do when they get there.
- However, before all that, to get your site on the web you need a domain name and a place to host your site.
- Another practical bit of information is FTP programs which allow you to transfer files from your local computer to your web server.
- To help people get started, there are many companies who provide templates and tools to make sites for blogging, email newsletters and more.

## MDN

---

### Video and Audio APIs

- HTML5 has elements for embedding video and audio into documents with the elemnets being named such, and both come with their own APIs for controlling the playback and seeking.
- When embedding audio and video, you can also include the attribute `controls` which enables the default controls, but while it has its advantages because of differing controls in each browser and most controls not being keyboard-acessible, some devs chose to program their own custom controls.
- One of the tools provided with HTML5 is the `HTMLMediaElement` API.
- If creating a custom control bar, make sure to not use the `controls` attribute to not show the default one.
