# Local chat with Podman AI

Chat UI for local offline Granite or Llama 3 Model.

## Architecture

![Alt text](architecture.png?raw=true "Architecture")

## Gradio UI

![Alt text](chat-example.png?raw=true "Streamlit UI")

## Prerequisites

- Install Podmain AI lab - <https://podman-desktop.io/docs/ai-lab>
- Install Python 3

## Download model

Downoad a model in Podman AI lab (see tab catalog). For example: instructlab/granite-7b-lab-GGUF

To use LLama3: Download LLama3 model from Huggingface. For example:
<https://huggingface.co/TheBloke/LLaMA-Pro-8B-GGUF>

Import the model into Podman AI via the user interface.

## Start Podman AI service

Start the model as a service (see tab Services)

Hint: In Service details check the local URL port used. If necessary, change it in gradio_app_v1.py in variable model_service.

## Crete and activate virtual environment

```bash
python3 venv -m venv
```

```bash
python3 source venv/bin/activate
```

## Install Python libraries

In your terminal:

  ```bash
  pip3 install -r requirements.txt
  ```

## Run the Gradio app

  ```bash
  python3 gradio_app_v1.py
  ```

## Create Shell alias

Add into your `bashrc` or `zshrc` file:

  ```bash
  alias llama='cd ~/llama3_local; python3 gradio_app_v1.py'
  ```

NOTE: update the `cd ~/llama3_local` with the path, where you've saved this project.

## Run the shell alias to call it from any directory

  ```bash
  llama
  ```
