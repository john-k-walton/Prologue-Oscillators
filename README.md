![alt text](https://github.com/john-k-walton/Prologue-Oscillators/blob/main/IMG_0974.png)
**PlaitsXplorer for Prologue - Full Front Panel MultiEngine Modulation Control**

**[NEW!] Introducing ElementsXplorer - Peter's Modal Strike model based on Elements with front panel control and full key tracking!**

*"It's like a having the whole Modular inside your keyboard!"*


PlaitsXplorer turns your Prologue into a 'PlaitStation'; a fully digital, polyphonic, knobbilicious, modular modulation monster! PlaitsXplorer heavily utilizes Tsoniq's Logue Front Panel code (Thanks Mark!!!) to map User Oscillator modulation controls onto front panel VCO control instancing *eleven* user oscillator controls on the front panel, for a total of *seventeen* digital engine controls, plus User Oscillator access to EG Envelope, independent LFO and Note Velocity! Brandish Front Panel controls to sculpt modulations containing combinations of EG Envelope, built in Envelope, Two builtin Tri LFO's with Saw; tremolo and vibrato options, use LFO independently of Target and Intensity, Key Tracking on all inputs, and Velocity Sensitivity with wild abandon, all concurrently in a selectable modulation matrix of madness! 

PlaitsXplorer provides exceptional control of complex modulations for Plaits DSP models, all from the comfort of the front panel. The only menu diving is for modulation programming: the LFO2 rate, three KT settings, and the two MultiMod timing and configuration controls. PlaitsXplorer's reuse of front panel controls also supports Expression Pedal, Mod Wheel, After Touch and MIDI CC control access to digital engine programming, plus full preset save and restore of all configuration and modulation controls. See PlaitsXplorer DOC's for details! Release Candidate binaries are available NOW!

PlaitsXplorer demos https://soundcloud.com/john-walton-732877645/sets/plaitsxplorer-for-prologue

the following PlaitXplorer Oscillators are available today for Prologue.

- VA; Virtual Analog with classic waveforms.
- VAsync; Hard Sync Virtual Analog, lots of squelch on this one.
- Tides; Wavefolder found in Tides.
- Warps; Wavefolder found in Warps.
- FM; 1 and 2 operator Frequency Modulation with variable feedback.
- Grain; Granular formant synthesis.
- Zbraids; filter simulation with Peaking/LP/BP/HP response.
- Additive; Additive mixture of harmonically related sine waves.
- SWARM; Granular swarm of 8 enveloped SAW Waves.
- Particle; Dust noise processed by networks of all-pass or band-pass filters.
- Noise; Variable-clock white noise processed by a resonant filter.
- NoiseDBP; Variable-clock white noise processed by a resonant filter with dual bandpass filters.
- Bassdrum Analog/Synth; simulation of bass drum.
- Snare Analog/Synth; simulation of snare drum.
- Hi Hat Harsh/Clean; simulation of hi hat.
- Wta-Wtf; Plaits 2D Wavetables. 32 Spectrally related Wavecycles arranged in a 2D table for modulating in two directions.
- Braids Wavetables; Jazz, Clank, India, Voices, Strings 2D Braids wavetables [on hold for now]
- VCF 1.2 LP/HP

**Pro Tips:**

1. When initializing a new model, proceed to MultiEngine Param Menu and *immediately* increment and decrement each Param 1-6 in turn to prevent the Front Panel display Params from defaulting to -100 for Bipolar Params (PX's Params are all BiPolar), and save you and your encoder a lot of cranking. Please keep in mind that the Params the Voice cards see, and what you hear, is a value of -100 until they're initialized by hand, the Front panel just isn't in sync yet. this is known bug/feature of Logue. this is especially evident with VA's detune, which has confused even me once in a while sometimes Prologue forgets the params on layers. weird korg bug there.
2. A large Shape pointer knob is recommended for PlaitsXplorer to aid in Models with settings featuring Pitch. plus it helps in performance situations.


**XD and NTS are on hold for now, I hadn't had enough testing on either to determine what the problems are. now that's I've spent some time, and found discrepancies, i'm going to have to go back and recalibrate controls.**

Up Coming Changes ToDo List:
1. Fix MultiMod Vibrato LFO3 mode, i broke it when i put the LFO FM option, or replace with a 4 phase Logue LFO delay; one phase per input plus Cutoff.
2. convert Envelope timing to full log range from 2-piece linear approx. median range at the knee is coming into play lately. nice to have.
3. elaborate Wedge & Window Key Tracking Modulation curves for Matrix Modulation (2). linear ramps don't provide enough seperation in modulations across even five octaves. Wedge will seperate linear ramps somewhat, and Window will introduce a sliding window for hard spliting modulations. linear ramp is still available.

---------------
**[NEW][9/7/25]**
ElementsXplorer RC2 is up. changes includes Position as a new Envelope target (fun!) and a minor internal trigger delay that eliminate all or most fo the minor pitch 'schwing' the original model port had. yay!

**[9/6/25]**
ElementsXplorer RC1 is up with front panel control and draft modulation assignment docs.

**[9/4/25]**
ElementsXplorer is in the works now - a Front Panel controlled version of the Elements port to Korg prologue. will include support for Logue modulations, and key tracking each control. 

**[NEW][8/20/25]**
4th draft detailing Key Tracking with Bias and Modulations. this will probably be the last draft before todo list features are finished. enjoy!

**[8/15/25]**
3rd Draft Manual with Expression Controller section changes and additions, a Voicing and Modulation section, and VA oscillator programming example.

**[8/7/25]** RC4 release binaries and manual are UP! so, takes a while to play through all these models while testing and isolating issues without a debugger. in RC3 I found Additive had a hard crash on one Prologue but only intermittant crash on the other. i might have a dodgy voice in one Prologue. fwiw Additive and Particle are the most CPU intensive, and String the most memory intensive. I removed some function call thrashing and coverted those calls to global variables to reduce CPU to fix both models. also added aunipolar version of LFO for Matrix Modulation (1) for cleaner modulation enveloping without inverting the multiplicand. now Additive works fine, and Particle is back in play and modulation (1) is more defined. also more manual updates woo!

**[6/8/25]** RC3 release published. click on Releases to the right to download binaries and manual or follow this link https://github.com/john-k-walton/Prologue-Oscillators/releases/tag/plaits

**[6/7/25]** RC3 binaries and manual uploaded. WT[a-f] do not have Interpolation or 5-bit implemented atm. not enough memory with the newest LFO3 modulation. need to shake some more bytes out of the source to fit it all in RC4.
