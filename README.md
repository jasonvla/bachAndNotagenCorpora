development of usable code to extract certain data of both the real bach chorale corpus in music21 and a custom-generated notagen corpus with a samplesize of 100 pieces.

More NotaGen-pieces need to be generated in the future (at least a few hundred ones, even better maybe 1e3, 1e4,...)

## Current state:

### Key Extraction
- determine key of chorale by applying music21's key finding algorithm.
- visualization of key distribution within the corpora

### Time Signature Extraction
- always the first one in each piece

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

## TODO

Depending on how we're continuing after the explorative phase, ideas could be:

- add whether time signatures change during a piece
- Count Parallel fifths
- Evaluate ranges of voices during a piece / a phrase
- Extract and compare the bass parts

## Questions
- What are Segments? (see *music21.figuredBass.segment*)
- *music21.figuredBass.possibility.parallelFifths(possibA, possibB)* => possibilities in music21?
- *music21.voiceLeading*
