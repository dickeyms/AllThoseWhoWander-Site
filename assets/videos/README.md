# Video Assets

Place your background video file here.

## Required Files

- `background.mp4` - MP4 format (H.264 codec, recommended)
- `background.webm` - WebM format (optional, for better browser support)

## Video Specifications

**Recommended Settings:**
- Resolution: 1920x1080 (Full HD) or 2560x1440 (2K)
- Duration: 15-30 seconds (looping seamlessly)
- Frame Rate: 24-30 fps
- Codec: H.264 (MP4) or VP9 (WebM)
- File Size: Target 5-15 MB (compressed)
- Audio: None (will be muted anyway)

**Content Guidelines:**
- Ambient, slow-moving footage from your game
- Avoid fast movements or jarring cuts
- Should loop seamlessly (end frame matches start frame)
- Subtle, atmospheric - not distracting from content

## Compression Tips

Use a tool like HandBrake or FFmpeg to compress:

```bash
ffmpeg -i input.mov -vcodec libx264 -crf 28 -preset slow -vf scale=1920:1080 background.mp4
```

For WebM:
```bash
ffmpeg -i input.mov -c:v libvpx-vp9 -crf 35 -b:v 0 -vf scale=1920:1080 background.webm
```

## Fallback Behavior

If no video is present:
- Desktop: Falls back to `background.png`
- Mobile: Always uses `background.png` (for performance)
