# Prologue Plaits Oscillators
This directory contains Seven zip files. Each zip file is a collection of digital oscillators modified from Peter Allwin's work on porting of Emilie Gillet's wonderful Plaits code to Prologue. Where Peter's original work included an builtin LFO2, these versions instead implement Envelope Generators, Key Tracking, as well as including support for the main hardware LFO modulated by envelope or key tracking. 

EGandKT - these files implement either a single AR Envelope Generator or a Key Tracking. The files were built on Peter's V1.6 code base, which included a bug in the wavetable oscillators row indexing. So waveforms were not in canonical order. The AR files are mostly deprecated by the M3 versions. However, the KT files are very useful for voicing the oscillator across the keyboard. KTStr is my favorite for mapping string voicing with respect to pitch, with Prologue layering. Very nice! 

M3_1.6.1a - these files implement, in a single version support for AR envelope, Key Tracking and LFO redirect all in one oscillator. These oscillators are based on Peter's 1.6.1 code, and thus correct waveform indexing for the six wavetable oscillators.

M3fast - these files implement the same functionality as M3_1.6.1a, however the attack period has been reduced by 1/5th for faster plucky envelopes, plus there is a small amount of Key Tracking with attack timing; faster envelopes with higher notes. 

Plaits_SineLFO - recompile of *all* Plaits models with Peter Allwin's port code base 1.6.1. So, all of Peter's original compiled modules are included with his LFO's PLUS addition to Noise, Particle, Swarm, Bass Drum, Snare, and Hi Hat. 

Modal 2 - a late addition was a sucessful porting of Modal model. other model in the Mini-Rings ensamble. 

----
I'm using Yorich Tech's Low Frequency Expander to demo some modulation schemes. With it, I've been able to create time varying modulations of the Shape and Shift-Shape model inputs, while using the builtin single-input modulation options of M3 to modulate the 3rd or 4th variable. Whoa!

This allows me to explore the most interesting 2-4 input modulation ideas without resorting to coding. I can get so many detailed tonalities with these models expressed in in more than 1 dimension. Looking forward to committing these ideas to code.
