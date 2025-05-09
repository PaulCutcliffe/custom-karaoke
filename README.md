# Custom Karaoke Python Script

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](https://opensource.org/licenses/MIT)

## Description

The Custom Karaoke Python Script is a command-line tool that allows users to create custom karaoke tracks by removing vocals from audio files.

## Features

- Create a karaoke video from any source video


## Installation

1. Clone the repository:

    ```shell
    git clone https://github.com/muddylemon/custom-karaoke.git
    ```

2. Install the required dependencies:

    ```shell
    cd custom-karaoke
    python -m venv venv
    ./venv/bin/activate 
    pip install -r requirements.txt
    ```

3. Install an FFmpeg build with NVENC support (Windows):
   - Download a static FFmpeg build with NVENC enabled from https://www.gyan.dev/ffmpeg/builds/ (look for the "full" or "git full" build).
   - Extract the archive and copy the `bin\ffmpeg.exe` into your project folder or add the `bin` directory to your system PATH.
   - Open a new terminal and run `ffmpeg -hwaccels`. You should see `h264_nvenc` listed.
   - MoviePy will automatically detect and use `h264_nvenc` when CUDA is available.

## Usage

1. Acquire a video file from YouTube:

    ```shell
    yt-dlp -f best https://www.youtube.com/watch?v=VIDEO_ID
    ```

2. Run the script with the desired video file:

    ```shell
    python main.py path/to/video_file.mp4
    ```

3. If unsatisfied with the transcription, you can edit and re-run , it will skip the previous steps and just redo the final video. 


## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvements, please open an issue or submit a pull request.

## License

This project is licensed under the [MIT License](LICENSE).
