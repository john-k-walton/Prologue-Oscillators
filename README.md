# Prologue Plaits Oscillators / NEW (12/23) content posted below the fold.
This is a collection of digital oscillators based on Peter Allwin's work porting Emilie Gillet's wonderful Plaits code to the Korg Prologue; PLUS 7 NEW models freshly ported from the original Plaits, AND 5 new wavetables from Braids, AND THEN some new wavetables derived from Shapershifter wavetables.

  *currently NTS versions are down for repair*

WHAT IS IT?
Plaits is a collection of DSP algorithms, wavetables, physical modeling, and traditional synthesis models combined together in one of the most popular macro oscillators in the eurorack world. These models aren't "load and go" Organ models or other synthesis methods focused solely on melodiusness; they're elegantly crafted DSP algorithms with interesting twists, sweet spots, and chaotic turns!

Each model represents a different type of synthesis method:
* Virtual Analog - digital synthesis of classic waveforms.
* Waveshaper - an asymmetric triangle processed by a waveshaper and a wavefolder.
* FM - two sine wave oscillators modulating each others phase.
* Granular - simulation of formants and filtered waveforms through the manipulation of segments of sine waves.
* Additive - modulate a mixture of harmonically related sine waves.
* Wavetables - explore many collections of 32 waveforms arranged in 4 x 8 wavecycle arrays; Plaits, Braids, ShapeShifter.
* Strings - Karpus Strong vibrating string physical model; guitars, plucks, plinks, and a whole lot more.
* Modal - vibrating material physical model; bells, wood blocks, metal bars [NEW].
* Swarm - a swarm of 8 enveloped saw waves [NEW].
* Noise - a variable-clock white noise processed by resonant filter [NEW].
* Particles - dust noise processed by networks of all-pass or bandpass filters [NEW].
* Bass Drum - behavioral simulation of circuits of classic Bass Drum [NEW].
* Snare - behavioral simulation of snare drum circuit [NEW].
* Hi Hat - behavioral model of hi-hat circuit [NEW].

Taken together it is a complete laboratory of sonic creation, exploration, and surprise! And while each model is interesting in and of itself, where this collection of techniques really accels, is in layering the  different synthesis methods. Then  slathering it all with analog VCO's, VCF's, and Prologue effects!

Plaits models use four inputs to express their individual wide ranging sonic landscapes; three orthogonal inputs that express the ful reach of the synthesis model - think of a cubic 3D space full of sonic textures - and a forth input that mixes the standard algorithm with an alternate expression, such as dual bandpass filters or different filter modes. Prologue presents eight control points to the user. With four algorithimic inputs, just setting starting values for inputs consumes half the Prologues eight user oscillator controls, leaving the rest for modulation controls. Since this can be unduly restrictive for multivariable models; therefore, the models have been packaged with a variety of control schemas; two are presented here:

* LFO2 - Peter's original schema presents a method of appling two LFO's freely to one or a pair of any inputs. in addition to the main LFO, a built-in LFO2 is provided for complex periodic variations. 
  
* ENV - this schema presents combinations of indexed modulations featuring envelope, key tracking, and the main LFO. key tracking can be used to cross fade modulations from Envelope to LFO, or LFO to Envelope across the keyboard. the LFO and Envelope may be summed, or multiplied together to produce delay vibrato like effects by enveloping the LFO. indicies with opposite slopes for key tracking modulations may be applied to sub and main layers for even more interesting intonations across the keyboard, or for very complex modulations. due to control complexity, this schema modulates one input variable.

Select the schema for the model you want to explore, then load and go crazy! 

# Todays selection of files are:

* NEW! SS_LFO_WT.zip - set of five Wavetable oscillators containing ShapeShifter LFO derived wavetables. They are spectrally active and fun to play with! only Env versions today.
  
* Also NEW SS_CVVE_WT.zip - a collection of wavetables set with Chirps, VideosGames, Vocals, ePiano's!

* Plaits_LFO2.zip - based entirely on Peter's original work with a builtin LFO2. The version provided here completes the entire set of Plaits models - with the exception of the Speech model (still in progress). This set also contins the following new models from the noisey set: Filtered Noise, Particle Noise, Bass Drum, Snare, Hi Hat, Modal (the "Minirings" Modal synthesis), Swarm (Granular Cloud of Saws). these new models have their sweet sonic spot, but they quickly range into chaotic, noisey, and interesting spaces. some level setting may be necessary. 

* Plaits_ENV.zip - all the models above, provided with an indexed modulation scheme described in the prototype document M3 Collection.pdf. A linear Envelope Generator combined with key tracking and Prologue's own LFO provide a variety of simple AD/ADR/ADSD envelope, LFO, and key tracking options to modulate the models. With these you can add an initial inharmonic twang to a Karplus Strong model, drift through a strobing panoply of harmonics with the addistive sine model, or perhaps create a slowly detuning swarm of polyphonic SAWs, or conversely a swarm of SAW's slowly tuning, your choice!

* Plaits_ENV_WT2.0.zip - Mutable's Plaits wavetables were derived from Braids (an earlier macro oscillator product without integrated wavetables). This Zip contains the representatives of the remaining WaveTables from Braids inplemented in the Integrated Wavetable method used by Plaits to improve anti-aliasing; Strings, Voices, Jazz, Clang, India. Each oscillator contains four wavetables, each wavetable contains 8 harmonically related wavecycles, for a total of 32 waveforms per oscillator. The envelope generator provided is linear - which is especially nice with wavetable scanning, as opposed to exponential where everything sounds like "Whoop!". Linear envlopes are adjustable from 1-10 seconds for long slow rolling washs of sonic development.

* Plaits_LFO2_WT2.0 - same oscillators as above but managed by Peter's LFO2 schema. wander the sonic landscape yourself with an Internal LFO modulating one direction, and Prologue's LFO in the other; mix it up with a square wave LFO! or audio rate for complete nonsense!

* Modal2.Zip - Envelope and LFO2 schemas for MiniRings Modal physical model for vibrating materials - not to be confused with Strike-model.

* Plaits.pdf - original online Plaits manual for reference only. please check it out!

* M4 Cheat Sheet.pdf - simple chart to describe index system used in the enveloped versions. tape it to something, you'll need it.

Note for Newbies to Korg SDK. the 6 menu params used to define the behavior of the oscillator are 'a must' to adjust. there is an outstanding bug with the SDK when instancing controls with a both a positice and negative value (referred to as BiPolar). Bipolar controls will default to -100, not zero. as a result, a newly installed oscillators will have to have it's bipolar controls set to meaningful value before the oscillator may render a sound, or at least a *good* sound. :0)

* lastly, here are some audio demos to listen to; Particle, Swarm and Noise examples, plus three layered pieces with Swarm, Modal, Particles, Granular, and Additive models in various combinations. The demos feature a sample backing track for context in the middle of the demo; then beginning and endings feature inspection of layers or alternative settings.

This set features selected models heard by itself, then with some ad hoc accompaniment. Runtime aprox 1.5 minutes each: 
https://soundcloud.com/plaits-for-prologue/sets/plaits-for-prologue

This set features Prologue and XD with various other instruments in more involved pieces. Somewhat longer 2-3 minutes song demo works. chronologically later works feature more complex arrangements for Prologue that include an XD:
https://soundcloud.com/plaits-for-prologue/sets/listening-stuff

----
I'm using Yorich Tech's Low Frequency Expander to demo some modulation schemes. most demo works use the LFE to modulate either Effects settings, and/or the first two model Paramaters. With it, I've been able to create time varying modulations of the Shape and Shift-Shape model inputs, while using the builtin single-input modulation options of M3 to modulate the 3rd or 4th model input. Whoa! that's a lot of modulation!

This allows me to explore the most interesting 2-4 input modulation ideas without resorting to coding. I can get so many detailed tonalities with these models expressed in in more than 1 dimension. Looking forward to committing these ideas to code.
