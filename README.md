## Video Watermark Removal

This repository provides a set of tools to download videos, convert them into frames, detect and remove watermarks, and reassemble the cleaned frames into a video. The watermark removal process leverages various methods, including OpenCV inpainting, GAN-based models (WDNet), and ProPianter. This project is ideal for researchers or developers working on video processing or watermark removal tasks.

## Features


Video Downloading: Download videos from various sources.


Frame Extraction: Convert videos to individual frames for processing.


Watermark Detection and Removal: Automatically detect and remove watermarks from frames using:


#### 1. OpenCV Inpainting


#### 2. GAN-based models (WDNet)


#### 3. ProPianter(best results)


Reassemble Video: Reconstruct the video from the cleaned frames.


Configurable Pipeline: Choose between different watermark removal techniques.


## Installation


To use this repository, clone it to your local machine and install the required dependencies.

```python
git clone https://github.com/aqsaa2/watermark-removal.git
```

cd watermark-removal


## Requirements
Python 3.6+
OpenCV
TensorFlow or PyTorch (for GAN-based models)
ProPianter

## Usage


### Step 1: Download a Video

You can download a video using a link or specify a local file path. The following command downloads a video:

```python
python download_video.py --url "video_url"
```

### Step 2: Extract Frames

After downloading the video, extract individual frames using the following command:

```python
python extract_frames.py --video_path "path_to_video"
```

### Step 3: Remove Watermark

You can choose from multiple methods to remove watermarks from the extracted frames.

Option 1: OpenCV Inpainting

```python
python remove_watermark.py --method opencv --frames_dir "path_to_frames"
```

Option 2: WDNet (GAN-based model)


Ensure that you have the necessary pre-trained model files for WDNet before using this option.

```python
python remove_watermark.py --method wdnet --frames_dir "path_to_frames"
```

Option 3: ProPianter(best results)

```python
python remove_watermark.py --method propianter --frames_dir "path_to_frames"
```

### Step 4: Reassemble the Video

Once the frames have been cleaned, reassemble them into a video:

```python
python reassemble_video.py --frames_dir "path_to_cleaned_frames" --output_video "outpu
```
