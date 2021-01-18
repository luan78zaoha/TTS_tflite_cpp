# TTS tflite cpp
A demo of Mandarin TTS and the pretrained [tflite-models](https://github.com/lr2582858/TTS_tflite_cpp/releases/tag/0.1.0) are available for linux platform.

TTS models (fastspeech2 and multibank_gan) are trained from the repository of [TensorFlowTTS](https://github.com/TensorSpeech/TensorFlowTTS).

TFlite model convert method see [colab notebook](https://colab.research.google.com/drive/1Ma3MIcSdLsOxqOKcN1MlElncYMhrOg3J?usp=sharing#scrollTo=KCm6Oj7iLlu5). This notebook provides a demonstration of the realtime E2E-TTS using TensorflowTTS for Chinese (Using Baker dataset).

TTS Demo with tflite model using c++ inference see [C++ Inference Demo](https://github.com/lr2582858/TensorFlowTTS/tree/cpptflite/examples/cpptflite)

## Results
- #### Comparison before and after conversion

  - Before conversion (Python)

    ![ori_mel](./results/ori_mel.png)


  - After conversion (C++)

    ![tflite_mel](./results/tflite_mel.png)

- #### Adding #3 in text could create pause prosody in audio
```shell
./demo 这是一个开源的#3端到端#3中文语音合成系统 test.wav
```
![tflite_mel](./results/tflite_mel2.png)
