# How `frame_extraction()` works

## Overview

This function extracts the required frames from a video, resizes and normalizes them for model input.

```python
def frame_extraction(video_path, sequence_length=20, image_height=224, image_width=224)
```

### Args

- `video_path`: The path of the video in the disk, whose frames are to be extracted.
- `sequence_length`: Number of frames to extract per video (default: 20).
- `image_height`: Height to resize frames to (default: 224 for Xception).
- `image_width`: Width to resize frames to (default: 224 for Xception).

### Returns

- `frames_list`: A list containing the resized and normalized frames of the video, or None if extraction fails.
