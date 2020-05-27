# TensorFlowLite_ESP32

https://www.tensorflow.org/lite/microcontrollers/overview

## Overview

This library runs TensorFlow machine learning models on microcontrollers, allowing you to build AI/ML applications powered by deep learning and neural networks. 

With the included examples, you can recognize speech, detect people using a camera, and recognise "magic wand" gestures using an accelerometer.

The examples work best with the M5StickC(ESP32) board, which has a microphone and accelerometer.

## Examples

### hello_world

Outputs sine waves to serial outputs and build-in LEDs.

### magic_wand

This is gesture recognition using acceleration.
The accelerometer_handler and output_handler must be modified according to the environment in which they are used.

### magic_wand_M5StickC
This is gesture recognition using acceleration.
This is a sample that acquires acceleration from the IMU(MPU6886) of M5StickC.

### micro_speech

This is a sample of speech recognition.
The audio_provider and command_responder must be modified according to the environment in which they are used.

### micro_speech_M5StickC

This is a sample of speech recognition.
We use the M5StickC's I2S built-in microphone.

### person_detection

It is a person detection using a camera.
The image_provider and detection_responder must be modified according to the environment in which they are used.

### person_detection_ESP32-Camera

It is a person detection using a camera.
This is a sample of using the ESP32 camera driver. Please configure the device you want to use in config.h.

### person_detection_T-CameraV05

It is a person detection using a camera.
This is an example of the use of TTGO T-Camera V05.

## How to make this library
```
wget https://github.com/tensorflow/tensorflow/archive/v2.1.1.tar.gz
tar zxvf v2.1.1.tar.gz
cd tensorflow-2.1.1
make -f tensorflow/lite/experimental/micro/tools/make/Makefile TARGET=esp generate_micro_speech_esp_project
```

This is the base file.

- Renamed *.cc to *.cpp
- Edit the include path
- And, Minor corrections

## special thanks

- https://www.tensorflow.org/lite/microcontrollers/overview
- Arduino_TensorFlowLite librarie
- https://github.com/boochow/TFLite_Micro_MagicWand_M5Stack
- https://github.com/boochow/TFLite_Micro_MicroSpeech_M5Stack/tree/m5stickc

