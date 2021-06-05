# Audio, Video, Images

## Images

The `<img>` tag is used to embed an image in an HTML page.

Images are not technically inserted into a web page; images are linked to web pages. The `<img>` tag creates a holding space for the referenced image.

The `<img>` tag has two required attributes:

- `src` - Specifies the path to the image
- `alt` - Specifies an alternate text for the image, if the image for some reason cannot be displayed

*Note: Also, always specify the width and height of an image. If width and height are not specified, the page might flicker while the image loads.*

HTML 
```html
<img src="img_logo.jpg" alt="Logo" width="500" height="600">
```

HTML with CSS
```html
<img src="hello.gif" alt="Welcome" width="42" height="42" style="border:5px solid black">
```

Image in CSS
```css
img {
  display: inline-block;
}
```
## HTML Audio and Video
The HTML DOM has methods, properties, and events for the `<audio>` and `<video>` elements.Which makes it simple to add media to a website. You need to set src attribute to identify the media source and include a controls attribute so the user can play and pause the media.


### HTML Audio/Video Methods

- `addTextTrack()` Adds a new text track to the audio/video.
- `canPlayType()`	Checks if the browser can play the specified audio/video type.
- `load()`	Re-loads the audio/video element.
- `play()`	Starts playing the audio/video.
- `pause()`	Pauses the currently playing audio/video.


### HTML Video


```html
<video width="320" height="240" controls>
  <source src="movie.mp4" type="video/mp4">
  <source src="movie.ogg" type="video/ogg">
Your browser does not support the video tag.
</video>

```

The controls attribute adds video controls, like play, pause, and volume.
It is a good idea to always include width and height attributes. If height and width are not set, the page might flicker while the video loads.
The `<source>` element allows you to specify alternative video files which the browser may choose from. The browser will use the first recognized format.

The text between the `<video>` and `</video>` tags will only be displayed in browsers that do not support the `<video>` element.


### Video Attribute Specification:

- **autoplay** This Boolean attribute if specified, the video will automatically begin to play back as soon as it can do so without stopping to finish loading the data.
	
- **autobuffer** This Boolean attribute if specified, the video will automatically begin buffering even if it's not set to automatically play.
	
- **controls** If this attribute is present, it will allow the user to control video playback, including volume, seeking, and pause/resume playback.
	
- **height** This attribute specifies the height of the video's display area, in CSS pixels.
	
- **loop** This Boolean attribute if specified, will allow video automatically seek back to the start after reaching at the end.
	
- **preload** This attribute specifies that the video will be loaded at page load, and ready to run. Ignored if autoplay is present.
	
- **poster** This is a URL of an image to show until the user plays or seeks.
	
- **src** The URL of the video to embed. This is optional; you may instead use the `<source>` element within the video block to specify the video to embed.

- **width** This attribute specifies the width of the video's display area, in CSS pixels.



### Audio Attribute Specification:

- **autoplay** This Boolean attribute if specified, the audio will automatically begin to play back as soon as it can do so without stopping to finish loading the data.

- **autobuffer** This Boolean attribute if specified, the audio will automatically begin buffering even if it's not set to automatically play.

- **controls** If this attribute is present, it will allow the user to control audio playback, including volume, seeking, and pause/resume playback.
	
- **loop** This Boolean attribute if specified, will allow audio automatically seek back to the start after reaching at the end.

- **preload** This attribute specifies that the audio will be loaded at page load, and ready to run. Ignored if autoplay is present.
	
- **src** The URL of the audio to embed. This is optional; you may instead use the <source> element within the video block to specify the video to embed.

### HTML Audio - Media Types

- **MP3**	audio/mpeg
- **OGG**	audio/ogg
- **WAV**	audio/wav