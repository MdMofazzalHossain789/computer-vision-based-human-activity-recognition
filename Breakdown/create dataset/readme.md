# How `create_dataset()` works?

## Overview

This function extracts data for selected classes and creates the dataset.

```python
def create_dataset(dataset_dir, # dataset directory
                   classes_list, # list of classes
                   sequence_length=20, # number of frames to extract per video
                   image_height=224, # height to resize frames to
                   image_width=224, # width to resize frames to
                   max_videos_per_class=None # max videos to process per class
                   )
```

### Args

- `dataset_dir`: The directory containing the UCF-50 dataset (e.g., "/kaggle/working/UCF50_dataset/UCF50").
- `classes_list`: List of class names to include in the dataset.
- `sequence_length`: Number of frames to extract per video (default: 20).
- `image_height`: Height to resize frames to (default: 224 for Xception).
- `image_width`: Width to resize frames to (default: 224 for Xception).
- `max_videos_per_class`: Maximum number of videos to process per class (optional, for testing).

### Returns

- `features`: A numpy array of extracted frame sequences with shape (n_videos, sequence_length, image_height, image_width, 3).
- `labels`: A numpy array of class indexes.
- `video_files_paths`: A list of video file paths.
