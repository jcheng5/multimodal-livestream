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

### Notebook

The simplest and most primitive way to run the demo is to use the Jupyter notebook.

Replace the `input.mov` file with your own recording (or don't) and run the Jupyter notebook called `video-to-speech.ipynb`.

### Running the interactive app

There's also an interactive [Shiny](https://shiny.posit.co/py/) app that you can run with the following command:

```
shiny run app.py --port 0 --launch-browser
```

Or see a live version at [https://jcheng5.shinyapps.io/multimodal/](https://jcheng5.shinyapps.io/multimodal/).

### Running the bake-off app

Finally, there's a version of the app that you can use to compare GPT-4o with GPT-4 and an open source model called LLaVA:7B. To run it, you'll need to install [ollama](https://ollama.com) and then:

```
ollama pull llava:7b
```

Then run the bake-off app with:

```
shiny run app_bakeoff.py --port 0 --launch-browser
```
