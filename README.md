![alt text](https://github.com/john-k-walton/Prologue-Oscillators/blob/main/IMG_0974.png)
**PlaitsXplorer for Prologue - Full Front Panel MultiEngine Modulation Control**

*"It's like a having a whole Modular inside your keyboard!"*


PlaitsXplorer turns your Prologue into a 'PlaitStation'; a fully digital, polyphonic, knobbilicious, modular modulation monster! PlaitsXplorer heavily utilizes Tsoniq's Logue Front Panel code (Thanks Mark!!!) to map User Oscillator modulation controls onto front panel VCO control instancing *eleven* oscillator controls on the front panel, for a total of *seventeen* digital engine controls, plus User Oscillator access to EG Envelope, independent LFO and Note Velocity! Brandish Front Panel controls to sculpt modulations containing combinations of EG Envelope, built in Envelope, Two builtin Tri LFO's with Saw; tremolo and vibrato options, use LFO independently of Target and Intensity, Key Tracking on all inputs, and Velocity Sensitivity with wild abandon, all concurrently in a selectable modulation matrix of madness! 

PlaitsXplorer provides exceptional control of complex modulations for Plaits DPS models, all from the comfort of the front panel. The only menu diving is for modulation programming: the LFO2 rate, three KT settings, and the two MultiMod timing and configuration controls. PlaitsXplorer's reuse of front panel controls also supports Expression Pedal, Mod Wheel, After Touch and MIDI CC control access to digital engine programming, plus full preset save and restore of all configuration and modulation controls. See PlaitsXplorer DOC's for details! Release Candidate binaries are available NOW!

PlaitsXplorer demos https://soundcloud.com/john-walton-732877645/sets/plaitsxplorer-for-prologue

the following PlaitsXplorer Oscillators are available today for Prologue.

- VA; Virtual Analog with classic waveforms.
- VAsync; Hard Sync Virtual Analog, lots of squelch on this one.
- Tides; Wavefolder found in Tides.
- Warps; Wavefolder found in Warps.
- FM; 1 and 2 operator Frequency Modulation with variable feedback.
- Grain; Granular formant synthesis.
- Zbraids; filter simulation with Peaking/LP/BP/HP response.
- Additive; Additive mixture of harmonically related sine waves.
- SWARM; Granular swarm of 8 enveloped SAW Waves.
- Particle; Dust noise processed by networks of all-pass or band-pass filters. [on hold]
- Noise; Variable-clock white noise processed by a resonant filter.
- NoiseDBP; Variable-clock white noise processed by a resonant filter with dual bandpass filters.
- Bassdrum Analog/Synth; simulation of bass drum.
- Snare Analog/Synth; simulation of snare drum.
- Hi Hat Harsh/Clean; simulation of hi hat.
- Wta-Wtf; Plaits 2D Wavetables. 32 Spectrally related Wavecycles arranged in a 2D table for modulating in two directions.
- Braids Wavetables; Jazz, Clank, India, Voices, Strings 2D Braids wavetables [on hold for now]
- VCF 1.2 LP/HP

**Pro Tips:**

1. When initializing a new model, proceed to MultiEngine Param Menu and *immediately* increment and decrement each Param 1-6 in turn to prevent the Front Panel display Params from defaulting to -100 for Bipolar Params (M5's Params are all BiPolar), and save you and your encoder a lot of cranking. Please keep in mind that the Params the Voice cards see, and what you hear, is a value of -100 until they're initialized by hand, the Front panel just isn't in sync yet. this is known bug/feature of Logue.
2. A large Shape pointer knob is recommended for PlaitsXplorer to aid in Models with settings featuring Pitch. plus it helps in performance situations.


**XD and NTS are on hold for now, I hadn't had enough testing on either to determine what the problems are. now that's I've spent some time, and found discrepancies, i'm going to have to go back and recalibrate controls.**

---------------
**[NEW][6/8/25]** RC3 release published. click on Releases to the right to download binaries and manual or follow this link https://github.com/john-k-walton/Prologue-Oscillators/releases/tag/plaits

**[6/7/25]** RC3 binaries and manual uploaded. WT[a-f] do not have Interpolation or 5-bit implemented atm. not enough memory with the newest LFO3 modulation. need to shake some more bytes out of the source to fit it all in RC4.
