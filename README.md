# Multimodal demo

This repo contains a Jupyter notebook that demonstrates simulating video input and audio output against GPT-4o, using OpenAI's API.

## Installation

### ffmpeg

You will need the `ffmpeg` utility installed. Either use the [official installers](https://ffmpeg.org/download.html), or `brew install ffmpeg` (for macOS brew users) or `choco install ffmpeg` (for Windows chocolatey users).

### OpenAI API key

Create a file called `.env` in the root of the project and add the following line:

```
OPENAI_API_KEY=<your-api-key>
```

If you have an OpenAI account, you can generate an API key from [this page](https://platform.openai.com/api-keys).

### Python dependencies

```
pip install -r requirements.txt
```

## Usage

Replace the `input.mov` file with your own recording (or don't) and run the Jupyter notebook called `video-to-speech.ipynb`.