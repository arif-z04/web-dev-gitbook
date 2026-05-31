# 9. Multimedia

## Audio Element

Embed audio content:

```html
<audio controls>
    <source src="audio.mp3" type="audio/mpeg">
    <source src="audio.ogg" type="audio/ogg">
    Your browser doesn't support HTML5 audio.
</audio>
```

### Audio Attributes

```html
<audio 
    controls 
    autoplay 
    loop 
    muted
    preload="metadata">
    <source src="audio.mp3" type="audio/mpeg">
</audio>
```

- `controls` - Show player controls
- `autoplay` - Start playing automatically
- `loop` - Repeat indefinitely
- `muted` - Start muted
- `preload="auto|metadata|none"` - Preload strategy

## Video Element

Embed video content:

```html
<video controls width="640" height="480">
    <source src="video.mp4" type="video/mp4">
    <source src="video.webm" type="video/webm">
    Your browser doesn't support HTML5 video.
</video>
```

### Video Attributes

```html
<video 
    controls 
    autoplay 
    loop 
    muted
    poster="thumbnail.jpg"
    preload="metadata">
    <source src="video.mp4" type="video/mp4">
</video>
```

- `controls` - Show video controls
- `width/height` - Video dimensions
- `poster` - Thumbnail image
- `autoplay` - Start playing automatically
- `loop` - Repeat indefinitely
- `muted` - Start muted

## Captions and Subtitles

```html
<video controls>
    <source src="video.mp4" type="video/mp4">
    <track kind="captions" src="captions-en.vtt" srclang="en" label="English">
    <track kind="captions" src="captions-es.vtt" srclang="es" label="Spanish">
</video>
```

Track kinds:
- `captions` - Captions for deaf/hard of hearing
- `subtitles` - Dialog translation
- `descriptions` - Video description
- `chapters` - Chapter titles
- `metadata` - Script/metadata

## Iframe (Embedded Content)

Embed external content:

```html
<!-- Embedded video player -->
<iframe 
    width="560" 
    height="315" 
    src="https://www.youtube.com/embed/dQw4w9WgXcQ"
    title="YouTube video player"
    frameborder="0"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
    allowfullscreen>
</iframe>

<!-- Google Map -->
<iframe 
    src="https://www.google.com/maps/embed?pb=..." 
    width="400" 
    height="300" 
    style="border:0;" 
    allowfullscreen="" 
    loading="lazy">
</iframe>

<!-- External website -->
<iframe src="https://example.com" width="100%" height="600"></iframe>
```

## Complete Media Example

```html
<section class="media-gallery">
    <h2>Our Media</h2>
    
    <!-- Audio player -->
    <article>
        <h3>Podcast Episode</h3>
        <audio controls>
            <source src="episode-1.mp3" type="audio/mpeg">
            Your browser doesn't support HTML5 audio.
        </audio>
    </article>
    
    <!-- Video player with captions -->
    <article>
        <h3>Tutorial Video</h3>
        <video controls width="640" height="480" poster="thumb.jpg">
            <source src="tutorial.mp4" type="video/mp4">
            <source src="tutorial.webm" type="video/webm">
            <track kind="captions" src="captions.vtt" srclang="en" label="English">
            Your browser doesn't support HTML5 video.
        </video>
    </article>
    
    <!-- Embedded YouTube -->
    <article>
        <h3>Featured Video</h3>
        <iframe 
            width="560" 
            height="315" 
            src="https://www.youtube.com/embed/VIDEO_ID"
            allowfullscreen>
        </iframe>
    </article>
</section>
```

## Key Takeaways

✅ Use `<audio>` and `<video>` for native media playback

✅ Provide multiple source formats for compatibility

✅ Include captions and transcripts for accessibility

✅ Use `poster` attribute for video thumbnail

✅ Use `controls` attribute for user controls

✅ Use iframes for embedded external content

---

**Next: [Semantic HTML →](10-semantic-html.md)**
