# 1D Spectral_speech_enhancement
1D End-to-End Speech Ehancement using Spectral loss

## Dataset

### DEMAND dataset
Description from Thiemann et al ([link](https://zenodo.org/record/1227121#.X6iMAIhKhPY)) 

>The DEMAND (Diverse Environments Multichannel Acoustic Noise Database) aims to provide a setof recordings that allow testing of algorithms using real-world noise in a variety > >of settings. All recordingsare made with a 16-channel array, with the smallest distancebetween microphones being 5 cm and thelargest being 21.8 cm.

## Requirements:

[Tensorflow 2.0](https://www.tensorflow.org/install), [pysepm](https://github.com/schmiph2/pysepm), [ddsp](https://github.com/magenta/ddsp), [librosa](https://librosa.org/doc/latest/index.html)

## Evaluation metrics:

Using pysepm: fwSNRseg SNRseg LLR STOI PESQ 

## Loss function

Spectral Loss using the Google Magenta's DDSP library

```python
import ddsp

spectral_loss = ddsp.losses.SpectralLoss()

# Multi-scale spectrogram reconstruction loss.
loss = spectral_loss(audio, audio_input)
```

## References

[1] https://phillipi.github.io/pix2pix

[2] https://github.com/magenta/ddsp
