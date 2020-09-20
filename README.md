# Basic usage of canvas

## The < canvas > element

### At first sight a < canvas > looks like the <img> element, with the only clear difference being that it doesn't have the src and alt attributes. Indeed, the < canvas > element has only two attributes, width and height. These are both optional and can also be set using DOM properties. When no width and height attributes are specified, the canvas will initially be 300 pixels wide and 150 pixels high. The element can be sized arbitrarily by CSS, but during rendering the image is scaled to fit its layout size: if the CSS sizing doesn't respect the ratio of the initial canvas, it will appear distorted.


## Fallback content
### The < canvas > element differs from an < img > tag in that, like for < video >, < audio >, or < picture > elements, it is easy to define some fallback content, to be displayed in older browsers not supporting it, like versions of Internet Explorer earlier than version 9 or textual browsers. You should always provide fallback content to be displayed by those browsers.

### Providing fallback content is very straightforward: just insert the alternate content inside the < canvas > element. Browsers that don't support < canvas > will ignore the container and render the fallback content inside it. Browsers that do support < canvas > will ignore the content inside the container, and just render the canvas normally.

![canvas](https://user-images.githubusercontent.com/70091044/93721137-9152a480-fb96-11ea-8134-4f7c41074474.PNG)

## The rendering context
### The < canvas > element creates a fixed-size drawing surface that exposes one or more rendering contexts, which are used to create and manipulate the content shown. 

### The canvas is initially blank. To display something, a script first needs to access the rendering context and draw on it. The < canvas > element has a method called *getContext()*, used to obtain the rendering context and its drawing functions. *getContext()* takes one parameter, the type of context. For 2D graphics, you specify "2d" to get a *CanvasRenderingContext2D*.

