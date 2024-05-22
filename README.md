# Local chat whith Podman AI

Chat UI for local offline Llama3 Model to chat with.

## Architecture

![Alt text](architecture.png?raw=true "Architecture")

## Gradio UI

![Alt text](chat-example.png?raw=true "Streamlit UI")

## Prerequisites

- Install Podmain AI lan - <https://podman-desktop.io/docs/ai-lab>
- Install Python 3

## Download Llama 3 model

Downoad a model in Podman AI lab (see tab catalog). For example: instructlab/granite-7b-lab-GGUF

Start the model as a service (see tab Services)

Hint: In Service details check the local URL port used. If necessary, change it in gradio_app_v1.py in variable model_service.

## Crete and activate virtual environment

python3 venv -m venv
python3 source venv/bin/activate

## Install Python libraries

In your terminal:

  `pip3 install -r requirements.txt`

## Run the Gradio app

  `python3 gradio_app_v1.py`

## Create Shell alias

Add into your `bashrc` or `zshrc` file:

  `alias llama='cd ~/llama3_local; python3 gradio_app_v1.py'`

NOTE: update the `cd ~/llama3_local` with the path, where you've saved this project.

## Run the shell alias to call it from any directory

  `llama`
