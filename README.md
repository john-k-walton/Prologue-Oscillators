PlaitsXplorer IS NOT a firmware hack, it does not modify your machine in anyway. it doesn't use AI, and it doesn't violate any copy protection. it merely runs as any user oscillator does, while making READ references ONLY to new memory locations containing control values, envelope and LFO states. when not selected, your synth operates as it always does. Each line of code has been lovingly hand written by Émilie, Peter, and Mark, and myself for the enjoyment of others, love of music, and just being a good old fashion human. Please enjoy!

See End of File for Current Project Status.

![alt text](https://github.com/john-k-walton/Prologue-Oscillators/blob/main/IMG_0974.png)

**PlaitsXplorer and ElementsXplorer for Prologue (Only) - Full Front Panel MultiEngine Modulation Control**

*"It's like a having a whole Modular synthesizer inside your Prologue!"*

**PlaitsXplorer** turns your Prologue into a 'PlaitStation'; a fully digital, polyphonic, knobbilicious, modular modulation monster! PlaitsXplorer heavily utilizes Tsoniq's Logue Front Panel code (Thanks Mark!!!) to map User Oscillator modulation controls onto front panel VCO control instancing *eleven* user oscillator controls on the front panel, for a total of *seventeen* digital engine controls, plus User Oscillator access to EG Envelope, independent LFO and Note Velocity! Brandish Front Panel controls to sculpt modulations containing combinations of EG Envelope, built in Envelope, Two builtin Tri LFO's with Saw; tremolo and vibrato options, use LFO independently of Target and Intensity, Key Tracking on all inputs, and Velocity Sensitivity with wild abandon, all concurrently in a selectable modulation matrix of madness! 

PlaitsXplorer provides exceptional control of complex modulations for Plaits DSP models, all from the comfort of the front panel. The only menu diving is for modulation programming: the LFO2 rate, three KT settings, and the two MultiMod timing and configuration controls. PlaitsXplorer's reuse of front panel controls also supports Expression Pedal, Mod Wheel, After Touch and MIDI CC control access to digital engine programming, plus full preset save and restore of all configuration and modulation controls. See PlaitsXplorer DOC's for details! Release Candidate binaries are available NOW!

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
- Particle; Dust noise processed by networks of all-pass or band-pass filters.
- Noise; Variable-clock white noise processed by a resonant filter.
- NoiseDBP; Variable-clock white noise processed by a resonant filter with dual bandpass filters.
- Bassdrum Analog/Synth; simulation of bass drum.
- Snare Analog/Synth; simulation of snare drum.
- Hi Hat Harsh/Clean; simulation of hi hat.
- VCF 1.2 LP/HP

**ElementsXplorer**

What is Elements? "Elements is a full-blown synthesis voice based on modal synthesis - an under-appreciated flavour of physical modelling synthesis. With Elements, a sound is designed by specifying a resonant structure (plate, string, tube...), the properties of the material it is made of (stiffness, absorption...), and how the structure is excited to produce sound - struck, plucked, blown, bowed..."

ElementsXplorer Demos https://soundcloud.com/john-walton-732877645/sets/elementsxplorer-for-prologue

Original Elements Manual https://pichenettes.github.io/mutable-instruments-documentation/modules/elements/manual/

**Pro Tips:**

1. When initializing a new PX or EX model, proceed to MultiEngine Param Menu and *immediately* increment and decrement (by 1) each Param 1-6 in turn to prevent the Front Panel display Params from defaulting to -100 for Bipolar Params (PX's Params are all BiPolar), and save you and your encoder a lot of cranking. Once you do this new oscillator initialization it is not needed for this preset slot again - unles you change oscillators. Please keep in mind that the Params the Voice cards see, and what you hear, is a value of -100 until they're initialized by hand, the Front panel just isn't in sync yet. this is known bug/feature of Logue. this is especially evident with VA's detune, which has confused even me once in a while sometimes Prologue forgets the params on layers. weird korg bug there.
3. A large Shape pointer knob is recommended for PlaitsXplorer to aid in Models with settings featuring Pitch. plus it helps in performance situations.

----------
**[10/15/26]**
lots of new Pitch Modulations! In addition to using LFO2 as a vibrato modulation, now there is a short exponential decay envelope for horn blips, plus the four MultiMod LFO modulations (see below) are also available as pitch modulations too! Horn Blip is an alternate mode for LFO2 (when set to Zero), so you can also use it in Main and Velocity Modulations channels too! Update: added some Velocity controlled Pitch Intensity modes too. yum! total of 13 new vibratos mdoe to make for the single LFO or Chorus Vibrato. Some are windows by the LFO and some aren't. all can be modulated with the Mod Wheel.

**[10/11/26]**
RC5 coming soon to a Prologue near you....

![alt text](https://github.com/john-k-walton/Prologue-Oscillators/blob/main/ModMatrixRC5.png)

RC5 completely supplants LFO targets Selector, LFO generation for digital Oscillator, and LFO Int control. Providing four new Matrix Modulation modes with these additional features:

[All] Crossfade: In this mode two modulators are summed in Main Modulation channel. LFO Int crossfades between the two modulators allowing both an additional modulator per input as well as a method to manually crossfade between them. Also, here, MultiMod samples the LFO at the beginning of the note (should be in non-sync mode), for a Sample and Hold effect.

[VCO1+2] MultiRateLFO: This mode produces three multiples of the Main LFO selected by LFO Int control. Each of ten selections presents three preset rate multiples routed to ModMatrix selector for each input. Additionally, Pitch Target routes LFO2 to Oscillator pitch. LFO2 amplitude is modulated by the Triangle LFO for delayed/swelling vibrato effects. Also, Multimod produces the EG Velocity so it may be used control the amplitude of the MultiRateLFO's.

[VCO2] QuadPhaseLFO: In this mode, three additional LFOs are produced in a typical QuadPhase relation with the Main LFO; B, C, D Phases, while A remains with the Filter and Pitch modulation. LFO Int control adjusts the Phase interval between phases from 0-90 degrees. ModMatrix switches selecct among phases. Additionally, as in MultiRateLFO, Pitch Target routes LFO2 to Oscillator pitch. LFO2 amplitude is modulated by the Triangle LFO for delayed/swelling vibrato effects. Also, Multimod produces the EG Velocity so it may be used control the amplitude of the QuadLFO's.

[Multi] Windows and Wedges Key Tracking: This mode allows Keytracked (input Modulation channel intensities are proportional to the current pitch) modulators that individually applied to each input. KeyTracking menu controls are partitioned into two value regions: Windows, and Wedges. Windows splits Main and Velocity at a single pitch point: Main Modulation may be above or below the split, with Velocity occuping the opposite position. 60 split points are provided for Prologue 16 uses. Wedges produce opposing wedge shaped regions at each end of the keyboard (61 keys) with a settable resolution of one and a half keys. the Wedges vary from no keys modulated, to full overlap of regions as provided in RC4. Also, in this mode, Multimod also produces EG Velocity in this mode as a direct static modulator. LFO Int is reserved for Key Tracking Curves in a future release.

Multimod now produces one of nine types of modulators when selected:
- AR Linear Envelope
- AD Linear Envelope
- ADSR (30% Sustain) Linear Envelope
- ADSR (70% Sustain) Linear Envelope
- Linear Ramp 
- Triangle LFO
- Triangle LFO with Rate increasing with Pitch
- Triangle LFO Rate modulated by LFO Phase A Triangle
- Triangle LFO with Duty Cycle Modulated by LFO Phase A Triangle wave
- Sample + Hold of the LFO Phase A (use in non-keysync)
- EG Velocity for current note

Additionally, now both hardware Envelopes are available as well as both Velocity settings applied to each envelope respectively. EG envelope is assigned to Timbre Velocity channel, AMP Envelope is assigned to Morph Velocity channel. 

so... yeah, that's a lot of modulation.



