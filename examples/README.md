# Examples Local Apps

## Install dependencies for the apps (we preinstall all of them on the device at /home/distiller/DistillerSDK/venv)
```
pip install -r lib/requirements.txt
``` 

## Overview
- `app_wifi_setting.py`: a simple WiFi settings configuration page we wrote, you should probably start with this first :)
- `app_tiny_diffusion.py` and `lib/stable_diffusion_tools.py`: Implements a stable diffusion generator using [ORT](https://github.com/huggingface/optimum/tree/main), with quantized SD1.5 models provided in path `/home/distiller/models/`.
- `app_ebook_kid.py`: Demonstrates generating stories using [llama.cpp-python](https://github.com/abetlen/llama-cpp-python), and a SDXS model for illustrations. You can try stream=True for the text generation but it might get I/O bottlenecked.  
- `app_transcription.py`: Shows audio transcription with [faster-whisper](https://github.com/SYSTRAN/faster-whisper) lib and a default tiny models.
- `app_gallery.py`: Just a displays a gallery of images from the assets folder.
- `app_camera_paint.py`: a [picamera2](https://github.com/raspberrypi/picamera2) Implementation then use [FastSAM](https://github.com/ultralytics/ultralytics/tree/main/ultralytics/models/fastsam) for sagmentations and SD1.5 inpainting.

## Usage and Dependencies
```
pip install -r examples/lib/requirements.txt
python examples/main.py # which we already made default to run when device boot up
```

# Examples Online Apps


## Overview
- `app_soul.py`: an example using the [soul-engine](https://github.com/Pamir-AI/community) to craft a conversational AI soul, join their community here https://discord.com/invite/opensouls. In this demo we used `lib/deepgram_stt_tools.py` for speech to text and `lib/elevenlabs_tts_tools.py` for text to speech.
- `app_game_engine.py` : an example to use openai asisstant apis to create an app to play with gpt4-o. use the `setup_assistant` to create your assistance first time using it.
- Note : bring your own api keys for them and put in .env file in the `lib` folder for example 
```
OPENAI_API_KEY=<>
DG_API_KEY=<>
ELEVEN_API_KEY=<> 
```
