# rembg_from_video

Uses [ffmpeg-python](https://github.com/kkroening/ffmpeg-python) and [rembg](https://github.com/danielgatis/rembg) to attempt removal of a background from a video file.

Two directories will be created in the same directory as the script to hold the video frames (before and after rembg is applied).

### Installation:
[Install rembg by following their instructions](https://github.com/danielgatis/rembg)

rembg specifically requires Python 3.9 as of the time of this writing. Note that you must choose the `rembg[gpu]` version and configure onnxruntime accordingly if you wish to use your GPU for the image processing.

Then:
```
pip install ffmpeg-python
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

### Example:
![](/example/input.gif)![](/example/output.gif)
