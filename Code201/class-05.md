# Reading Assignment 4

## HTML

---

### Images

- When adding an image to a site, you use the `<img>` element.
  - The source of the image is provided with `src`
  - To provide an alternate text description you use `alt`
  - You can also add a title with `title`. This is usually shown when the image is hovered over.
  - `<img src="location of image" alt="an image of x" title="the image is of y'>`
- Images should be saved at the size they will be used at on the web page to prevent warping or slowing down the page loading.
- Photographs with lots of colors should be saved as a .jpeg, illustrations or logos that use flat colors are better saved as a .png.

### Color

- When specifying the color of anything on a color screen, you are essentially deciding on the values of three different colors. Red, Green, and Blue. an RGB value is just that, Red-Green-Blue. A hex code is the values of RGB in hexadecimals. Some colors have decided upon names and you can also use these names to have a preset color. In CSS3, you can also use the HSL values or Hue-Saturation-Lightness.
  - Hue is essentially a color circle with each angle corresponding to a color
  - Saturation is the amount of grey in a color from 0% - 100%.
  - Lightness is the amount of white in a color from 0% - 100%.
- In CSS3 you can also define the opacity of colors.
- One important thing to keep in mind is to have enough contrast in the colors between the background and the text otherwise it might not be readable.

### Text

- There are five main typefaces in text.
  - Serif
    - Serif has an extra detail on the end of each letter, and was typically used in print because it was considered easier to read.
  - Sans-Serif
    - San-serif does not have these extra details and are more often used in digital text due to some screens having too low of a resolution to read them clearly with the extra detail.
  - Monospace
    - Monospace letters are all the same width regardless of the letter, these are often used in code because they algn neatly.
  - Cursive
    - Cursive letters often have joining stroke or other cursive characteristic, oft mimicking handwriting.
  - Fantasy
    - Fantasy letters are often decorative and eye-catching, but not designed to be used for large amounts of text.
- Most text size fonts operate on a scale developed by typographers in the 16th century. This scale is one that most people who use a digital word processor will be familiar with.
  - The default text size is 16pt, or 16px.
- There are many properties to control different aspects of text. You can control the;
  - Font
  - Size
  - Weight
    - Bold lettering
  - Style
    - Italic lettering
  - Spacing
- There is only a certain number of fonts that the average computer has pre installed, so the majority of website text will be one of these choices.
- You can also align the text to a certain area relative to the box it's in.

## JPEG vs. PNG vs. GIF

---

- There are hundreds of file formats for images and the majority of people will have not heard of 90% of them. The three most common ones are the ones most widely used in internet images, but each one is used for different types of images.

- But first, to properly explain the differences between the three, one must understand the idea of image compression. Almost all data viewed on the internet is compressed in some way to reduce the size of the data and speed up transmission. Depending on what the goal is for the data, choosing the correct compression is important.<br> Compression of images comes in two types. Lossy and Lossless.
  - Lossy
    - Lossy compression has a higher compression ratio, resulting in smaller file sizes but has a degradation of quality, even if that degradation is slight. This degradation in quality is most easily seen when zooming in on a compressed image.
  - Lossless
    - A lossless compression however, has a lower compression ratio at the cost of a higher file size due to it not warping or degrading the data any.
- JPEG
  - JPEG, or Joint Photographic Experts Group for long, is a lossy compression file type that takes advantage of human perception to achieve a 1:10 ratio without a noticeable drop in quality. It does this by averaging the colors of nearby pixels and works best when used on photographs and paintings where the variation in color is smooth. It doesn't work as well with images that have a sharp contrast between colors.
- PNG
  - PNG or Portable Network Graphics for long, is a lossless compression file type designed to compress an image down as far as it can go without reducing the quality. For this reason it is best for images with text, logos or shapes with sharp edges. That isn't to say it doesn't work with photographs and paintings, it works perfectly, but because of the lossless compression the file size will be larger and thus slower to transmit.
- GIF
  - GIF or Graphics Interchange Format is a lossless file type that while early on was favored over PNGs due to the support for the format being low, it is nowadays used primarily for images that contain movement or animations as it is the only file type of the three to support it.
- Another thing to consider is Image Transparency.
  - Most images are boxes surrounding the image itself, which works perfectly well for images that are themselves a square, but if it is an unusual shape, or just text then the surrounding box just takes up space around it, obscuring anything that could be behind it.
  - Of the three formats, two of them have support for transparency, PNG and GIF.
  - All three image formats also have support for a certain number of colors too.
    - JPEGs can support 16 million colors, which is part of why they are so good at images of natural scenes.
    - PNGs, depending on the mode either support 256 colors or 16 million like JPEG.
      - PNG8 is used for simple shapes with few colors as it has 256 colors.
      - PNG24 is used for higher quality and more complex images as it has 16 million colors.
    - GIF supports 256 colors.
