# rembg_from_video

Uses [ffmpeg-python](https://github.com/kkroening/ffmpeg-python) and [rembg](https://github.com/danielgatis/rembg) to attempt removal of a background from a video file.

Usage:
```
rembg_video.py [-h] [-a] [-af AF] [-ab AB] [-ae AE] [--skip-extract] [--skip-process] input

Applies rembg to the frames of a video

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