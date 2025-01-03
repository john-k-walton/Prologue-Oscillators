**M5 Multidimensional Modulation Schema for Plaits on Prologue**

*"It's like a having a whole Modular inside your keyboard!"*

the following 23 Oscillators are available today for Prologue, Minilogue XD, and NTS-1 MKI
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

**The available Platform modulations are:**
- Shape LFO, built in Logue hardware LFO.
- Key Tracking.
- Note Velocity; currently only on XD and Prologue with RC3.
- Filter EG Envelope; currently only on XD and Prologue with RC4. both thanks to Tsonic's Logue Front Panel project!

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

Key Tracking Mode for Physicial Models:
- Key Tracking + Shape LFO; Key Tracked modulations per channel with an additional Note Velocity response on either Brightness, or Decay.

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

Modulations listed above are accessed via Attack and Decay Mode combinations; select modulation types and Modulation Channel assignments with various bipolar and zero values of these two controls. Please see PDF for control modulation control mapping.

**Pro Tip:**

When initializing a new model, proceed to MultiEngine Param Menu and *immediately* increment and decrement each Param 1-6 in turn. this will do two labor saving operations for you: 
1. prevent the Front Panel display Params from defaulting to -100 for Bipolar Params (M5's Params are all BiPolar), and save you and your encoded a lot of cranking. Please keep in mind that the Params the Voice cards see, and what you hear, is a value of -100 until they're initialized by hand, the Front panel just isn't in sync yet. this is known bug/feature of Logue.
2. now the model is in 3xLFO mode (Double Zero Mode). a few clicks from here takes you any of the modulation modes simply by entering combinations of postive and/or negative values for Attack Mode and Decay Mode. remember to use the Shift-Shortcut key to move leftward in the Params menus.

Best model to start with is the Additive Model w/EG Velocity, or Zbraids. don't forget to adjust EG Velocity Modulation Param in the menu's.

String and Modal have an Alternate Modulation mode for EG Velocity Key Tracking instead of LFO's.

--------------------
License and credit files included for the very generous open source developers of Plaits and Logue-Panel-Demo Code (EG Velocity) in distribution. Thank you Emilie, Mark, and Peter for your open source contributions; Plaits, Front Panel Code/Logue Internals, and the original Plaits Port! you folks rock!

-------------------
**[NEW] [01/02/25] working on RC4.**
replaced the DoubleZero 3xLFO mode with 3xKT mode on models with strong spectral Timbre; the Green models; Additive, Tides, VA, etc... 3xKT mode includes KT on all Mod Channels, plus hardware EG Envelope on Mod Channel 1 with the Front Panel EG Intensity, and LFO appears on Mod Channel 2. thanks again to Mark and his Front Panel code! Red models will keep 3xLFO mode for now.

-------------------
**[12/29/24] RC3 posted.** Note Velocity on all included models. witheld VCF issue with Velocity on XD for the moment. also, clean hihat is wonky.  i am down to only a few bytes on the String model, so the next spin will be a ripup and rewrite of that with special schema, along with Modal. i need to finish intregrating the 1.2 codebase; too many gotchas to managing two codebases of so many models on several platforms. i have no schedule for this at the moment, it's time to get back to playing after working on them. :0) Zipfile's contain all PDF's, licenses, and plugins.
