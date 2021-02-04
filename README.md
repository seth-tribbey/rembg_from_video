# rembg_from_video

Uses [ffmpeg-python](https://github.com/kkroening/ffmpeg-python) and [rembg](https://github.com/danielgatis/rembg) to attempt removal of a background from a video file.

Two directories will be created in the same directory as the script to hold the video frames (before and after rembg is applied).

### Installation:
```
pip install ffmpeg-python
pip install rembg
```
### Usage:
```
python .\rembg_video.py [-h] [-a] [-af AF] [-ab AB] [-ae AE] [--skip-extract] [--skip-process] input

positional arguments:
  input           Input video

optional arguments:
  -h, --help      show this help message and exit
  -a              Turns on alpha matting during background removal
  -af AF          Alpha matting foreground threshold
  -ab AB          Alpha matting background threshold
  -ae AE          Alpha matting erode size
  --skip-extract  Skips ffmpeg frame extraction
  --skip-process  Skips rembg frame processing
  ```
  Tip: [Alpha matting can be used to refine the results](https://github.com/danielgatis/rembg#advance-usage)
