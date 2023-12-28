# Prologue Plaits Oscillators
This is a collection of digital oscillators based on Peter Allwin's work porting Emilie Gillet's wonderful Plaits code to the Korg Prologue. Plaits algorythmic models use four input to express the wide ranging sonic landscape. Currenty provided are two sets of of zipfiles:

Plaits_LFO2.zip - based entirely on Peter's original work with an included an builtin LFO2, the version provided here complete the entire set of Plaits models - with the exception of the Speech model. This set also contins the following new models from the noisey set: Filtered Noise, Particle Noise, Bass Drum, Snare, Hi Hat, Modal (the "Minirings" Modal synthesis), Swarm (Granular Cloud of Saws). these new models have thier sweet sonic spoot, but they quickly range into chaotic, noisey, and intersting spaces. some level setting may be necessary. 

Plaits_ENV.zip - all the models above, provided with an indexed modulation scheme described in the prototype document M3 Collection.pdf. A linear Envelope Generator combined with key tracking and Prologue' LFO provide a variety of simple AD/ADR/ADSD emvelope, LFO and key tracking options to modulate the models. With these you can add an initial inharmonic twang to a Karplus Strong model, drift through a strobing panoply of harmonics with the addistive sine model, or perhaps create a slowly detuning swarm of polyphonic SAWs, or conversely a swarm of SAW's slowly tuning, your choice!

Plaits_ENV_WT.zip - Mutable's Plaits wavetables were derived from Braids (an earlier macro oscillator product without integrated wavetables). This Zip contains the remaining WaveTables from braids inplemented in the Integrated Wavetable method used by Plaits. Each oscillator contains four wavetables, each wavetable contains 8 harmonically related wavecycles, for a total of 32 waveforms per oscillator. The envelope generator provided is linear - which is espeically nice with wavetable scanning, as opposed to exponential, where everything sounds like "Whoop!". Linear envleope are adjustable from 1-10 seconds for long slow rolling washs of sound.

Plaits_LFO2_WT - same oscillators as above but managed by Peter's LFO2 schema. 

These models aren't "load and go" they're complicated with interesting twists, sweet spots, and chaotic turns, ported from one of the most popular macro oscillators in the eurorack world. see the manual. they are hours of interesting discovery and manipulation. for ease of use every model has the same control structure - learn one, learn them all! but the controls will take you in vastly different spaces.... and sometime, you'll make some music :0) enjoy! 

Plaits.pdf - Mutable's manual for Plaits for reference only.

M4 Cheat Sheet.pdf - simple chart to describe index system used in the enveloped versions. tape it to something.

Note for Newbies to Korg SDK. the 6 menu params used to define the behavior of the oscillator are 'a must' to adjust. there is an outstanding bug with the SDK when instancing controls with a both a positice and negative value (referred to as BiPolar). Bipolar controls will default to -100, not zero. as a result, a newly installed oscillators will have to have it's bipolar controls set to meaningful value before the oscillator may render a sound, or at least a *good* sound. :0) 

----
I'm using Yorich Tech's Low Frequency Expander to demo some modulation schemes. With it, I've been able to create time varying modulations of the Shape and Shift-Shape model inputs, while using the builtin single-input modulation options of M3 to modulate the 3rd or 4th variable. Whoa!

This allows me to explore the most interesting 2-4 input modulation ideas without resorting to coding. I can get so many detailed tonalities with these models expressed in in more than 1 dimension. Looking forward to committing these ideas to code.
