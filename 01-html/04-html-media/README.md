# HTML Media Guide

This guide explains how to use images, audio, and video in HTML with clear examples and common attributes.

---

## Images in HTML

To display an image in HTML, use the `<img>` tag.

### Basic Example

```html
<img src="images/photo.jpg" alt="Beautiful landscape">
```

### Most Common Attributes

| Attribute | Description |
| --- | --- |
| `src` | Path to the image file |
| `alt` | Alternative text (important for accessibility) |
| `width` | Sets image width |
| `height` | Sets image height |
| `title` | Tooltip text when hovering |

### Example with Attributes

```html
<img
  src="images/cat.jpg"
  alt="Cute cat"
  width="400"
  height="300"
  title="My Cat"
>
```

Best practice: Control image size using CSS instead of HTML `width` and `height` attributes.

---

## Audio in HTML

To add audio, use the `<audio>` element.

### Basic Example

```html
<audio controls>
  <source src="audio/music.mp3" type="audio/mpeg">
  Your browser does not support the audio element.
</audio>
```

### Common Audio File Types

| Format | MIME Type |
| --- | --- |
| MP3 | audio/mpeg |
| WAV | audio/wav |
| OGG | audio/ogg |

### Example with Multiple Formats

```html
<audio controls>
  <source src="audio/music.mp3" type="audio/mpeg">
  <source src="audio/music.ogg" type="audio/ogg">
  Your browser does not support the audio element.
</audio>
```

### Common Attributes

| Attribute | Description |
| --- | --- |
| `controls` | Shows play/pause controls |
| `autoplay` | Starts playing automatically |
| `loop` | Repeats audio |
| `muted` | Starts muted |

---

## Video in HTML

To display video, use the `<video>` element.

### Basic Example

```html
<video width="600" controls>
  <source src="video/movie.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
```

### Common Video File Types

| Format | MIME Type |
| --- | --- |
| MP4 | video/mp4 |
| WebM | video/webm |
| OGG | video/ogg |

### Common Attributes

| Attribute | Description |
| --- | --- |
| `controls` | Shows video controls |
| `width` | Sets video width |
| `height` | Sets video height |
| `autoplay` | Starts automatically |
| `loop` | Repeats video |
| `poster` | Image shown before video plays |

---

## Understanding the `poster` Attribute

The `poster` attribute is placed inside the `<video>` tag.

It displays an image before the video starts playing.

### Example

```html
<video width="600" controls poster="images/cover.jpg">
  <source src="video/demo.mp4" type="video/mp4">
</video>
```

### How It Works

- The image `cover.jpg` is shown first.
- When the user clicks play, the video replaces the image.
- If no poster is provided, the browser shows a blank state or the first frame.

---

## Recommended Folder Structure

```text
project/
|-- index.html
|-- images/
|   |-- photo.jpg
|   `-- cover.jpg
|-- audio/
|   |-- music.mp3
|   `-- music.ogg
`-- video/
    `-- movie.mp4
```

---

## Summary

- Use `<img>` for images.
- Use `<audio>` for sound files.
- Use `<video>` for videos.
- Always include `alt` text for images.
- Use `controls` for audio and video.
- Use multiple formats for better compatibility.
- Use `poster` to display a preview image before video playback.
- Prefer CSS for styling and sizing.
