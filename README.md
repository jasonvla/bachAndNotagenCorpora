development of usable code to extract certain data of both the real bach chorale corpus in music21 and a custom-generated notagen corpus with a samplesize of 100 pieces.

More NotaGen-pieces need to be generated in the future (at least a few hundred ones, even better maybe 1e3, 1e4,...)

## So far:

### Key Extraction
- determine key of chorale by applying music21's key finding algorithm.

### Time Signature Extraction
- the first one

### Melody Extraction
  - transpose everything to C major / a minor
  - take only 10 first notes of Soprano
  - convert to midi pitches
  - compare melody differences with a heatmap

### Chords

#### Count Dominant-seventh-chords

#### Chord Name Extraction
- Chordify the score
- Find all chord names (Counter)
- Interesting: Chord-Name-Distribution among the corpora are quite similar (=> AI learns chord-patterns?)

### Accidental Extraction
- Extract percentage of sharp/flat notes employed within a chorale => detect key-missclassifications

### Ascending/Descending Notes
- see the relative proportion of ascending/descending notes within the corpus
- right now, it takes all voices into account by recursing the score

#### Measures and Notes (Averages)
- count all notes and measures of the scores and calculate statistical parameters (variance, standard_dev, average)

- Standard deviation (regarding the amount of notes in a piece) in the bach corpus is way higher, but averages are quite similar!

## TODO
- add whether time signatures change during a piece
- respect modes (lydian, dorian, ...)
- Count Parallel fifths
- Evaluate ranges of voices during a piece / a phrase
- Extract and compare the bass parts

## Questions
- What are Segments? (see *music21.figuredBass.segment*)
- *music21.figuredBass.possibility.parallelFifths(possibA, possibB)* => possibilities in music21?
- *music21.voiceLeading*
