# Alexa_Arduino
Control Arduino Neopixel LED with Alexa

Requires
* Arduino MKR1000 (or similar)
* Neopixel LED Strip
* Dynamic DNS

Libraries used
* Adafruit Neopixel   https://github.com/adafruit/Adafruit_NeoPixel
* aRest   https://github.com/marcoschwartz/aREST

Alexa Integration inspired by
* Alexa_Particle    https://github.com/krvarma/Particle_Alexa

Issues
* Arduino aRest open to the world

## Create Skill on developer.amazon.com

1. Create Skill
2. Fill Skill Information
3. Interaction Model

**Intent Schema**

    {
      "intents": [
        {
          "intent": "ArduinoIntent",
          "slots": [
        {
              "name": "light",
              "type": "LITERAL"
            },
            {
              "name": "onoff",
              "type": "LITERAL"
            }
          ]
        },
        {
          "intent": "HelpIntent",
          "slots": []
        }
      ]
    }

**Sample Utterances**

    ArduinoIntent what is the {temperature|sensor} here
    ArduinoIntent what is the {humidity|sensor} here
    ArduinoIntent turn {on|onoff} {red|light} light
    ArduinoIntent turn {on|onoff} {green|light} light
    ArduinoIntent turn {off|onoff} {red|light} light
    ArduinoIntent turn {off|onoff} {green|light} light
    
    ArduinoIntent {red|light} 
    ArduinoIntent {green|light} 
    
    HelpIntent help
    HelpIntent help me
    HelpIntent what can I ask you
    HelpIntent get help
    HelpIntent to help
    HelpIntent to help me
    HelpIntent what can you do
    HelpIntent what do you do
    HelpIntent how do I use you
    HelpIntent how can I use you
    HelpIntent what can you tell me
