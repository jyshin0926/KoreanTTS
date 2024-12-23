# KoreanTTS

This is a project to implement Korean Text-to-Speech (TTS) by combining the Tacotron model with vocoder models (GriffinLim, WaveNet, WaveGAN).

Based on

- https://github.com/TensorSpeech/TensorFlowTTS
- https://github.com/hccho2/Tacotron2-Wavenet-Korean-TTS



## Dataset

1. Korean Single Speaker Speech
   - Professional female voice actor (12 hours, WAV, 44.1 kHz, 12,853 files, 3 GB)

2. Actress Yoo In-na’s Speech
   - Source: KBS Radio Program “Raise the Volume with Yoo In-na” (3 hours, WAV, 16 kHz, 3,327 files, 480.6 MB)
   - Text generated using:
     - Google Speech-to-Text API
     - Kakao Speech API

## Preprocessing

1. Convert WAV files to numpy format.

2. Bundle metadata such as 'audio', 'mel', 'linear', and 'text' for storage. 

3. Generate files in the format: Data/kss/“audio_filename.npz”.

4. Create ground truth datasets for Mel-spectrogram and Linear-spectrogram.



## Project Phases

1. Tacotron + GriffinLim + Single speaker
2. Tacotron + GriffinLim + Multi-Speaker(Deep Voice 2)
4. Tacotron2 + Melgan + Single Speaker
5. Tacotron2 + Melgan + Multi-Speaker (Transfer learning)



## Results 

1. Tacotron2 + GriffinLim + Multispeaker(KSS + Yoo In-na)

   - KSS Dataset Alignment (50,000 Steps):

   ![50000_kss](https://user-images.githubusercontent.com/67999107/98225804-8b732000-1f98-11eb-8c4b-bc9a52a7443f.png)

2. Tacotron2 + GriffinLim + Multi-Speaker(KSS + Yoo In-na) 

   - Yoo In-na Dataset Alignment (90,000 Steps):

   ![90000_유인나](https://user-images.githubusercontent.com/67999107/98225863-9a59d280-1f98-11eb-8dd1-e2955402e825.png)

3. Tacotron2 + MelGan + Singlespeaker(KSS)

   - Alignment (90,000 Steps):

  ![melgan_90000](https://user-images.githubusercontent.com/67999107/98225892-a2b20d80-1f98-11eb-850b-0ce0d192696f.png)

