## 📌 Repository Overview

This repository is organized as follows:

* **`notagen-pieces/`**: contains chorales generated with NotaGen.
* **`Open_Day_eval/`**: data and evaluation results gathered during the Open Day experiment.
* **`poster_ICCCM/`**: analysis notebooks and PDFs for the research poster presented at ICCCM.

---

## Current state:

### Key Extraction
- determine key of chorale by applying music21's key finding algorithm.
- visualization of key distribution within the corpora

### Time Signature Extraction
- always the first one in each piece (only a handful pieces change TS during the piece)

### Melody Extraction
- transpose everything to C major / a minor
- take n first notes of Soprano (currently n=10)
- convert to midi pitches
- compare differences with a heatmap

### Chords
- Dominant-seventh chords (absolute counts + relative)

### Chord Name Extraction
- Chordify the score
- Find all chord names with *chord.commonName* (in a Counter)
- Interesting: Chord-Name-Distribution among the corpora are quite similar (=> AI learns chord-patterns?)

### Accidental Extraction
- Extract percentage of sharp/flat notes employed within a chorale (in relation to all notes in the piece)


### Ascending/Descending Notes
- see the relative proportion of ascending/descending notes within the corpus
- right now, it takes all voices into account by recursing the score

#### Measures and Notes (Averages)
- count all notes and measures of the scores and calculate statistical parameters (variance, standard_dev, average)

- Standard deviation (regarding the amount of notes in a piece) in the bach corpus is way higher, but averages are quite similar!