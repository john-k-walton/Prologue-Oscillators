**M5 Multidimensional Modulation Schema for Plaits on Prologue**

*"It's like a having a whole Modular inside your keyboard!"*

[check the bottom of this README for updates still happening regularly!]

the following Oscillators are available today for Prologue, Minilogue XD, and NTS-1 MKI
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
- String; physical model of inharmonic vibrating string; Karplus-Strong.
- Modal; physical model of modal resonator.
- Bassdrum Analog/Synth; simulation of bass drum.
- Snare Analog/Synth; simulation of snare drum.
- Hi Hat Harsh/Clean; simulation of hi hat; on hold for now.
- Wta-Wtf; Plaits 2D Wavetables. 32 Spectrally related Wavecycles arranged in a 2D table for modulating in two directions.
- VCF LP/HP Prologue only.

**Logue Platform Modulations available *to* User Oscillator:**
- Shape LFO, built in Logue hardware LFO.
- Key Tracking.
- EG note Velocity.
- Filter EG Envelope. (Velocity and EG Env access generously provided by Tsonic Front Panel code - not available on NTS)

**User Oscillator Built-in Modulations:**

Envelopes:
- AD, Attack, Decay envelope.
- ASR, Attack, Sustain, Release type envelope.
- ADSR 40%, an ADSR with 40% Sustain level. Release is a fixed multiple of Decay.
- ADSR 70%, an ADSR with 70% Sustain level. Release is a fixed multiple of Decay.
- Linear Ramp, linearly increasing or decreasing Ramp. (set Decay +100, Attack to taste).

Envelope Mode features:
- Logarithmic or Linear Envelope Attack is defined per model, Decay and Release slopes are linear.
- Pitched Spectral models receive Log, others prefer Linear.
- Log Attack features 'advance to Decay on Note Off' modeling analog synth envelopes for more dynamic behavior. 

LFO Mode features:
- LFO2 (Triangle wave). approx 0.5hz to 1.5hz.
- LFO2 + Shape LFO; LFO's are summed linearly.
- LFO2 * Shape LFO; Shape LFO envelopes LFO2 for 'breathing' LFO modulation.
- Tremolo LFO2 + Shape LFO; LFO2 frequency is key tracked. LFO2 frequency increases with pitch. LFO2 summed with Shape LFO.
- Tremolo LFO2 * Shape LFO; LFO2 frequency key tracked and enveloped by Shape LFO. using the Shape LFO you can make varying time dependant tremolo effects.

Key Tracking Mode for Physical Models (single mode models):
- EG Envelope and Shape LFO modulated Inharmonic inputs, with seperate Key Tracking and EG Velocity on Brightness and Decay inputs.

Double Zero "Quick" Modes:
- Spectral (Green) Models; two channels of EG Velocity modulated by EG Envelope and LFO, with Note Key Tracking on all three Channels. great starting modulations! see Pro Tip 1 & 2.
- Unpitched (Red) Models; EG Velocity modulated Shape LFO on all three channels. 

**Traditional Control Schema Description:**

The same schema is used across all M5 user oscillators. Plaits provides three inputs that describe a cubic sonic space for each model. Modulations in multiple dimensions produce the most interesting sounds for subtractive sculpting. 
- Shape - Bias 1; Initial input value for Modulation Channel One
- (S)Shape - Bias 2; Initial input value for Modulation Channel Two
- Param 1 - Bias 3; Iniitial input value for Modulation Channel Three
- Param 2 - Modulation Channel One Intensity* 
- Param 3 - Modulation Channel Two Intensity*
- Param 4 - Modulation Channel Three Intensity*
- Param 5 - Attack Mode*
- Param 6 - Decay Mode*

*- for all models except Wavetables refer to M5 General Modulation Control Mapping.PDF; Wavetables as described in M5 Wavetable Modulation and Control Mapping.PDF. Wavetable Schema provides two additional Modulation Channels per input use Key Tracking to skew table access proportional to pitch across wavecycles.

Modulations listed above are accessed via Attack and Decay Mode combinations; select modulation types and Modulation Channel assignments with various bipolar and zero values of these two controls. Please see PDF for modulation and control mapping.

**Pro Tip:**

When initializing a new model, proceed to MultiEngine Param Menu and *immediately* increment and decrement each Param 1-6 in turn. this will do two labor saving operations for you: 
1. prevent the Front Panel display Params from defaulting to -100 for Bipolar Params (M5's Params are all BiPolar), and save you and your encoder a lot of cranking. Please keep in mind that the Params the Voice cards see, and what you hear, is a value of -100 until they're initialized by hand, the Front panel just isn't in sync yet. this is known bug/feature of Logue.
2. now the model is in Double Zero ('Quick' Mode); a few Mode clicks from here takes you any of the modulation modes simply by entering combinations of postive and/or negative values for Attack Mode and Decay Mode. remember to use the Shift-Shortcut key to move leftward in the Params menus, much easier than going around and around.

Best model to start with is the Additive Model w/EG Velocity, or VAsync. don't forget to adjust EG Velocity Modulation Param in the menu's, or EG INT in DoubleZero Mode.

--------------------
License and credit files included for the very generous open source developers of Plaits and Logue-Panel-Demo Code (EG Velocity, EG Envelope and EG_INT) in distribution. Thank you Emilie, Mark, and Peter for your open source contributions; Plaits, Front Panel Code/Logue Internals, and the original Plaits Port respectively! you folks rock!

-------------------
**RELEASE HISTORY:**

**[NEW] [02/01/25] WT_Braids.zip**
took a while to remember what i had done before. today, five Braids wavetables originated for the M4 project are included in WT_Braids with the M5 Wavetable schema; Voices, Jazz, Clank, Strings, and India.

-------------------
[01/27/25] VAupdate.zip
VA and VAsync: removed Note Velocity from Quick mode Mod Channel 2 so pitch effects in Quick Mode can be tuned to repeatable pitches with LFO modulations. 

-------------------
[01/07/25] RC5 optional
release includes changes only to Spectral Models; an additional EG Filter Envelope in LFO Mode on MOD Channel 3, which otherwise has no envelope. 
both RC4 and RC5 are fun for the whole family and provides hours of entertainment! 

-------------------
[01/03/25] RC4/Final Release
finalized features added from Logue Front Panel; EG Velocity, EG Envelope, and EG INT control. finished EG Velocity and Key Tracked Schema's for Physical Models. reminder, you must be running firmware 2.10 for these added features to work. VCF only provided for Prologue ATM.  
