development of usable code to extract certain data of both the real bach chorale corpus in music21 and a custom-generated notagen corpus with a samplesize of 100 pieces.
More NotaGen-pieces need to be generated in the future (at least a few hundred ones, even better maybe 1e3, 1e4,...)

## So far:
- Key Extraction: determine key of chorale by applying music21's key finding algorithm.
- Time Signature Extraction (1st in the piece)
- Melody Extraction:
  - transpose everything to C major / a minor (Bach AND Notagen)
  - take only 10 first notes of Soprano
  - compare melody differences with heatmap
- Dominant-Seventh Chords
- Chord Name Extraction: Count all chord names 
- Extract percentage of sharp/flat notes employed within a chorale => detect key-missclassifications
- Relation between ascending and descending notes

- Interesting: Chord-Name-Distribution among the corpora are quite similar (=> AI learns chord-patterns?)
- Looking at measure / note relation: Standard deviation (of the notes) in the bach corpus is way higher, but averages are quite similar!

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
