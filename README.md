# Refined annotation for CSD

## Introduction

We provide the refined annotation for 50 songs in the CSD dataset. The refined annotation is based on the original annotation provided by the CSD dataset. The refined annotation is more accurate than the original annotation. Annotation is done with [Sonic Visualiser](https://www.sonicvisualiser.org), a free and open-source audio analysis and annotation application.

In this repository, we only share the refined annotation for the 50 songs in the CSD dataset. For the audio files, you can download them from the Zenodo page of [CSD](https://zenodo.org/record/4916302).

## Annotation Procedure

For the annotation procedure, we basically follow the strategy by [Molina et al.](https://riuma.uma.es/xmlui/handle/10630/8372). However, because there is no strategy for the offset in the reference, we set our original rules for offsets as follows:

- The number of notes are basically following the original score. Ornaments in the note are not treated as separate notes.
- The start of the vowel is treated as the onset, the same as the reference. The start of the voiced consonants is not treated as the onset.
- If the phoneme changes, notes are separated.
- If there is a note without a vowel, we set the onset position with the same timing of the elecpiano sound in Sonic Visualiser.
- The end of vowel or end of the voiced consonants, whichever is longer, is treated as an offset.

## Annotation Format

The refined annotation has two formats: note and txt. The note format is a csv file with "onset, MIDI pitch, note duration". The txt format is a text file with lyric information in syllable and phoneme level, which is the same as the original annotation format.

## References

[1] Soonbeom Choi, et al. "Children’s song dataset for singing voice research." in ISMIR Late Breaking and Demo Papers, 2020.
[2] Chris Cannam, et al. "The Sonic Visualiser: A Visualisation Platform for Semantic Descriptors from Musical Signals" in Proc. of the 7th Int. Society for Music Information Retrieval Conf., 2006, pp. 324-327.
[3] Emilio Molina, et al. "Evaluation Framework for Automatic Singing Transcription." in Proc. of the 15th Int. Society for Music Information Retrieval Conf., 2014, pp. 567-572.
