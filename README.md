M5 Multidimensional Modulation Schema for Plaits on Prologue 

"It's like a having a whole Modular inside your keyboard!"

the following 24 Oscillators are available today for Prologue, Minilogue XD, and NTS-1 mki
- VA; Virtual Analog with classic waveforms.
- VAsync; Hard Sync Virtual Analog, lots of squelch on this one.
- Tides; Wavefolder found in Tides.
- Warps; Wavefolder found in Warps.
- FM; 1 and 2 operator Frequency Modulation with variable feedback.
- Grain; Granular formant synthesis.
- Zbraids; filter simulation with Peaking/LP/BP/HP response.
- Additive; Additive mixture of harmonically related sine waves.
- SWARM; Granular swarm of 8 enveloped SAW Waves. great for super saw and massive detuned effects.
- Particle; Dust noise processed by networks of all-pass or band-pass filters.
- Noise; Variable-clock white noise processed by a resonant filter.
- NoiseDBP; Variable-clock white noise processed by a resonant filter with dual bandpass filters.
- String; physical model of inharmonic vibrating string; Karplus-Strong.
- Modal; physical model of modal resonator.
- Bassdrum Analog/Synth; simulation of bass drum.
- Snare Analog/Synth; simulation of snare drum.
- Hi Hat Harsh/Clean; simulation of hi hat; on hold for now.
- Wta-Wtf; Plaits 2D Wavetables. 32 Wavecycles arranged in a 2D table for modulatin in two directions.


The final list of modulations are:
- Shape LFO, built in Logue hardware LFO.
- Key Tracking.
- Note Velocity; thanks to Tsonic's Logue Front Panel project! currently only on Prologue with RC3.

Envelope Mode: (both logarithmic and linear attacks are available)
- Logarithmic or Linear Envelope Attack is defined per model. Pitched Spectral models receive Log, others prefer Linear. Log Attack features 'advance to Decay on Note off' for more dynamic behavior. 
- AD, Attack, Decay envelope.
- ASR, Attack, Sustain, Release type envelope.
- ADSR 40%, an ADSR with 40% Sustain level. Release is a fixed multiple of Decay.
- ADSR 70%, an ADSR with 70% Sustain level. Release is a fixed multiple of Decay.
- Linear Ramp, linearly increasing or decreasing Ramp. (set Decay +100, Attack to taste).

LFO2 Mode:
- LFO2 (Triangle wave). approx 0.50hz to 1.5hz; Tremolo has a higher range.
- LFO2 + Shape LFO; LFO's are summed linearly.
- LFO2 * Shape LFO; Shape LFO envelopes LFO2 for 'breathing' LFO modulation.
- Tremolo LFO2 + Shape LFO; LFO2 frequency is key tracked. LFO2 frequency increases with pitch. LFO2 summed with Shape LFO.
- Tremolo LFO2 * Shape LFO; LFO2 frequency key tracked and enveloped by Shape LFO. using the Shape LFO you can make varying time dependant tremolo effects.

Key Tracking Mode:
- Key Tracking + Bipolar Shape LFO; various combinations of Key Tracking and Shape LFO.

please see included PDF's for detailed directions. 

here is the traditional control schema description. it is the same across all M5 user oscillators. think of a cube as the sonic space of each model, then the three inputs navigate that sonic space in a time varying fashion. modulations in multiple dimensions produce the most interesting sounds for subtractive sculpting. 
- Shape - Bias 1; Initial input value for Modulation Channel One
- (S)Shape - Bias 2; Initial input value for Modulation Channel Two
- Param 1 - Bias 3; Iniitial input value for Modulation Channel Three
- Param 2 - Modulation Channel One Intensity* 
- Param 3 - Modulation Channel Two Intensity*
- Param 4 - Modulation Channel Three Intensity*
- Param 5 - Attack Mode*
- Param 6 - Decay Mode*

*- for all models except Wavetables refer to M5 Modulation Channel Assignment and Control Mapping.PDF; Wavetables as described in M5 Wavetable Channel Assignment and Control Mapping.PDF.

Attack and Decay Mode combinations select modulation types and Modulation Channel assignments. please see PDF's for details.

Pro Tip:
when initializing a new model, proceed to MultiEngine Param Menu and *immediataly* increment and decrement each Param 1-6 in turn. this will do two labor saving things for you: 
1. prevent the Front Panel display Params from defaulting to -100 for Bipolar Params (M5's Params are all BiPolar), and save you and your encoded a lot of cranking. keep in mind that the Params the Voice cards see's is -100, the Front panel just isn't in sync. this is known bug/feature of Logue.
2. now the model is in 3xLFO mode (Double Zero Mode). a few clicks from here takes you any of the modulation modes simply by entering combinations of postive and/or negative values for Attack Mode and Decay Mode. remember to use the Shift key to move leftward in the Params menus.

Start with the Additive Model w/EG Velocity, or Zbraids. 

String and Model have an Alternate Modulation mode for EG Velocity Key Tracking instead of LFO's.


--------------------
License and credit files provided for the generous open source for Plaits and Logue-Panel-Demo Code (EG Velocity) in distribution. Thank you Emilie and Mark! you rock!


-------------------
[NEW] [12/29/24] RC3 posted. Note Velocity on all included models. witheld VCF issue with Velocity on XD. 
