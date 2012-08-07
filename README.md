#The Berkeley Restaurant Project (BeRP) Transcripts

This repository contains the most recent *transcripts* of the audio
files contained in the Berkeley Restaurant Project (BeRP) corpus. When
corrections come in, I will update this repository.

##BeRP Background

The Berkeley Restaurant Project (BeRP) was a testbed for a speech
recognition system developed by the International Computer Science
Institute (ICSI) in Berkeley, CA, USA, in the 1990's.

The BeRP system was designed to be an automated consultant whose domain
of knowledge was restaurants in the city of Berkeley. The system
served as a testbed for several research projects, including robust
feature extraction, connectionist phonetic likelihood estimation,
automatic induction of multiple pronunciation lexicons, foreign accent
detection and modeling, advanced language models, and lip-reading.

The BeRP corpus, collected at ICSI, currently contains approximately
8566 utterances, with about 1900 unique words, comprising about 7
hours of speech. The audio data was recorded with a Sennheiser
close-talking microphone and was sampled at 16 kHz.

The entire BeRP corpus (~500 megs) can be downloaded from:

http://www.icsi.berkeley.edu/ftp/pub/speech/wooters/berp.tgz

##Transcriptions

Each line in the *transcript.txt* file contains the transcript for
a single audio file. The first token on each line is the base name
of the corresponding audio file. So, for example, the line containing
the transcript for the audio file *4F_1_0010.wav.gz* looks like this:

> 4F_1_0010 i wanna spend about five dollars

See the file *transcription_guidelines.txt* for the guidelines that
the human transcribers were supposed to follow when transcribing the
audio data. If you find any issues, please let us know so that we can
update the transcripts!

##References

D. Jurafsky, C. Wooters, G. Tajchman, J. Segal, A. Stolcke, 
E. Fosler, and N. Morgan, *"The Berkeley Restaurant Project"*, Proceedings
ICSLP, 1994. [PDF](http://www.stanford.edu/~jurafsky/icslp-red.pdf)

C. Wooters, *"Lexical Modeling in a Speaker Independent Speech
Understanding System"*, PhD thesis, University of California,
Berkeley, CA, 1993. Available as ICSI TR-93-068. [PDF](http://www.icsi.berkeley.edu/ftp/pub/techreports/1993/tr-93-068.pdf)

A [YouTube video](http://www.youtube.com/watch?v=d9gDcHBmr3I) shot in
Nov. 1993 of Chuck Wooters using the BeRP system.

##Misc

The file *wordhist.txt* contains a frequency count of all of the words
in the BeRP transcripts. It is generated with this command:

```bash
cut -d" " -f2- transcript.txt | tr " " '\012' | sort | \
  uniq -c | sort -rn > wordhist.txt
```

