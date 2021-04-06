# deepspeech 
This [MLHUB](https://mlhub.ai/) provides a demonstration and command line tools built from the [pre-trained deepspeech model](https://deepspeech.readthedocs.io/en/v0.9.3/) provided by Mozilla. The model is trained by machine learning techniques based on [Baidu's Deep Speech research paper](https://arxiv.org/abs/1412.5567). This package can take an audio file as the input and transcribe it to the text as the output. 

The deepspeech source code is available from [https://github.com/mozilla/DeepSpeech](https://github.com/mozilla/DeepSpeech).

## Quick Start

Download the pre-trained model
```console
$ wget https://github.com/mozilla/DeepSpeech/releases/download/v0.9.3/deepspeech-0.9.3-models.pbmm
```

Download example audio files
```console
$ wget https://github.com/mozilla/DeepSpeech/releases/download/v0.9.3/audio-0.9.3.tar.gz
$ tar xvf audio-0.9.3.tar.gz
```
Run demo
```console
$ ml demo deepspeech --model deepspeech-0.9.30models.pbmm --audio audio/2830-3980-0043.wav
```
## Usage

* To install and demonstate the algorithm
```console
$ pip3 install mlhub
$ ml install   deepspeech
$ ml configure deepspeech
$ ml demo deepspeech --model deepspeech-0.9.30models.pbmm --audio audio/2830-3980-0043.wav
```
* Command line tools
```console
$ ml demo deepspeech --model [(--model) <pre-trained model>] [(--scorer) <external score file>] [(--audio) <audio file>] [(--beam_width) <beam width for the CTC decoder>] [(--lm_alpha) <langauge model weight>] [(--lm_beta) <word insertion bonus>] [(--version) <print version>] [(--extended) <output string>] [(--json) <output json>] [(--candidate_transcripts) <number of candidate transcripts>] [(--hot_words) <hot-words>]
```
