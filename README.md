# bulletin
build a bulletin board on Raspberry Pi, which is able to show custom message and read TTS from REST api

## hardware
* RPi
* LCD display HAT
* speaker for TTS (optional)

I'm using [Pirate Audio Speaker](https://shop.pimoroni.com/products/pirate-audio-mini-speaker) for both video and audio output

## tts (optional)
* homeassistant

this project makes use of [google_translate](https://www.home-assistant.io/integrations/tts/) platform from homeassistant via REST api

## installation
using pipenv to create virtualenv and install all dependencies from Pipfile

`pipenv install`

## configuration
edit settings to change font, color, etc..

## run
`pipenv run python3 rest.py settings`

## request to show text
`curl http://localhost:5000/text -d "content=hello world" -X POST -v`

## request to blank LCD
`curl http://localhost:5000/text -X DELETE -v`
