# C++ Inference using TFlite
TensorFlow Lite is an open source deep learning framework for on-device inference. On Android and Linux (including Raspberry Pi) platforms, we can run inferences using TensorFlow Lite APIs available in C++. The repository TensorFlowTTS and TensorFlow Lite help developers run popular text-to-speech (TTS) models on mobile, embedded, and IoT devices.

A demo of English or Mandarin TTS is available for linux platform [(C++ Inference Demo)](https://github.com/TensorSpeech/TensorFlowTTS/tree/master/examples/cpptflite). The pretrained models to be converted are download from the colab notebook ([English](https://colab.research.google.com/drive/1akxtrLZHKuMiQup00tzO2olCaN-y3KiD?usp=sharing#scrollTo=4uv_QngUmFbK) or [Mandarin](https://colab.research.google.com/drive/1Ma3MIcSdLsOxqOKcN1MlElncYMhrOg3J?usp=sharing#scrollTo=KCm6Oj7iLlu5)). Mel-generator and Vocoder select FastSpeech2 and Multiband-MelGAN, respectively.

TFlite model convert method see [colab notebook](https://colab.research.google.com/drive/1Ma3MIcSdLsOxqOKcN1MlElncYMhrOg3J?usp=sharing#scrollTo=KCm6Oj7iLlu5).



## Results
- #### Comparison before and after conversion (English TTS)
  ```
  "Bill got in the habit of asking himself “Is that thought true?” \ 
  And if he wasn’t absolutely certain it was, he just let it go."
  ```
- Before conversion (Python)

  ![ori_mel](./results/lj_ori_mel.png)


- After conversion (C++)

  ![tflite_mel](./results/lj_tflite_mel.png)

- #### Adding #3 in chinese text will create pause prosody in audio
```
这是一个开源的端到端中文语音合成系统"
```
![tflite_mel](./results/tflite_mel.png)
```
"这是一个开源的#3端到端#3中文语音合成系统"
```
![tflite_mel](./results/tflite_mel2.png)