# whisper-test

## Get started

Python ENV:
`Python 3.11.3`

Install `ffmpeg` by `choco`
```bash
choco install ffmpeg
```

Install `PyTorch` with CPU Compute Platform (If you have GPU, you can choose anther one)
```bash
pip3 install torch torchvision torchaudio
```

Install `Whisper`
```bash
pip install -U openai-whisper
```
> NOTE: Use proxy to speed up `pip install` speed.

## Using

Then you can use `whisper` command like that:
```bash
whisper I-am-speaking.mp3 --model tiny.en
```
And it will download model:
```
 \Python\Python311\Lib\site-packages\whisper\timing.py:57: NumbaDeprecationWarning: The 'nopython' keyword argument was not supplied to the 'numba.jit' decorator. The implicit default value for this argument is currently False, but it will be changed to True in Numba 0.59.0. See https://numba.readthedocs.io/en/stable/reference/deprecation.html#deprecation-of-object-mode-fall-back-behaviour-when-using-jit for details.
  @numba.jit
 10%|███▍                                | 43.9M/461M [12:16<2:38:04, 46.1kiB/s]
```
You also add some parameters:
```bash
whisper I-am-speaking.mp3 --language English --task translate --model tiny.en
```
Warning: tiny.en is an English-only model but receipted 'Chinese'; using English instead.

> NOTE: You can download other large model: https://huggingface.co/openai

## REF
- https://dalaozhi.org/video_trans/submit
- https://www.youtube.com/watch?v=ABFqbY_rmEk&t=632s
- https://github.com/openai/whisper
- https://pytorch.org/