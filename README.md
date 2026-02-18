development of usable code to extract certain data of both the real bach chorale corpus in music21 and a custom-generated notagen corpus with a samplesize of 100 pieces.
More NotaGen-pieces need to be generated in the future (at least a few hundred ones, even better maybe 1e3, 1e4,...)

## So far:

- Extract Soprano snippets (len=10 notes)
- Extract Time Signatures (1st in the piece)
- Count Dominant-Seventh Chords
- Count Key Signatures
- Extract percentage of sharp/flat notes employed within a chorale => detect key-missclassifications from the algorithm
- Relation between ascending and descending notes
## TODO
- add whether time signatures change during a piece
- respect modes (lydian, dorian, ...)
- Count Parallel fifths?
- Evaluate ranges of voices during a piece / a phrase
- Analyze how modulation works (are patterns recognizable, ...)
- Phrases starting on upbeat / downbeat, ...
- Usage of neapolitan chords
- Extract and compoare the bass parts
## Questions
- What are Segments? (see *music21.figuredBass.segment*)
- *music21.figuredBass.possibility.parallelFifths(possibA, possibB)* => what are possibilities in music21?
- *music21.voiceLeading*