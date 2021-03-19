---
layout: page
title: Low-resource speech evaluation
ref: asr2021
lang: ru
---

* TOC
{:toc}

## Timeline

* <span style="color: red">25.02 — training data release</span>
* <span style="color: white">10.03 — test data release</span>
* <span style="color: white">20.03 — submissions due</span>
* <span style="color: white">23.03 — results published</span>
* <span style="color: white">30.03 — papers due</span>

## Task description
### General remarks
The participants can use the [Lingvodoc project data](../data/index_data_asr.html) provided by the organizers as well as any other available data. The source code of the solutions as well as the data used must be published.
All files are UTF-8 (without BOM) encoded
Every participant can make up to 3 submissions.


### Input data

Datasets are available at the [Datasets](content/data/index_data_asr.html) page.

There are files having the following structure:
* recording id
* text transcription / spelling
* language code according to [Ethnologue](https://www.ethnologue.com/browse/codes) with slight modifications used in [Lingvodoc](http://lingvodoc.ispras.ru):
    * alt-tub — Tubalar
    * koi-yzv — Komi-Yazva
    * yrk-for — Forest Nenets
* genus
* family
* the word can probably be repeated several times
* the data can contain words pronounced in Russian

The two latter columns have been calculated for the whole subcorpus the data has been extracted from.
The genus and the family are specified according to [Lingvodoc](http://lingvodoc.ispras.ru).

The track has three subtasks:

### 1. Language detection
The participants will detect the language, the genus and the family for an utterance. All genera and families will be specified in the training data. However, the test data will also have surprise languages. The participants should specify X for the surprise language utterances.
The data can have repetitions as well as Russian stimuli pronounced within the utterances. We suppose that the language detection task has already been accomplished in "cleaner" conditions so it would be useful to see how the solutions will perform on "field" data
#### Evaluation
We evaluate the following for the files submitted:
* the percentage of properly detected languages
* the percentage of properly detected genera
* the percentage of properly detected families


### 2. Speech recognition
The participants will transcribe utterances or spell them. A test dataset without repetitions will be provided. However we consider repetitions in utterances as a challenge for the participants as it well help work with common field data

#### Evaluation
Every file is evaluated with:
* character error rate


### 3. Automatic detection of Russian stimuli
See motivation in 2

## Evaluation scripts
[Codalab link](https://competitions.codalab.org/competitions/30008)

[Sample submission](https://drive.google.com/file/d/1Zgp9CK-lFLNy-AztQJjZ-kwTxmb6s6LC/view?usp=sharing)

[Evaluation script](https://github.com/lowresource-lang-eval/asr_evaluation_scripts/blob/main/evaluate.py)

[Evaluation script description](https://github.com/lowresource-lang-eval/asr_evaluation_scripts/blob/main/README.md)

## Participants
[Google-group]({{ site.contact_group }})

[Telegram channel and chat](https://t.me/joinchat/VEyIcKjL4efvhbKm)
