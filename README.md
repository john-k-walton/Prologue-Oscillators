[NEW] [12/01/24] retargeted some modulation channels, and added an MOD Channel 3 KT+LFO channel option for better voicing possibilities, also MOD Channel 1 Env+LFO. included all platforms for all supported 1.0 and 1.2 modules now. Also included are Plaits Wavetables. These were rendered as interpolated only (input 3 removed as well as lo-fi AUX model output), with it's own modulation channel definitions to accomodate the larger control schemas for wavetables. these version have more modulations, and more options for modulation. Layering is even wilder with these :0)

There are currently 75 available oscillators in the base Plaits release. other Wavetables oscillators are in the works.

*ugh, just noticed that BLOCKSIZE for NTS is probably wrong for VCF module. 1.2 VCF XD is fine, same as Prologue. 1.0's are ok on NTS. more work to do for next releases. lol).*

[NEW] [11/28/24] M5 Versions coming soon... those posted are only 1/2 finished debug models; no LFO2 support yet, and reduced Envelope timing ranges. 

One shortcoming of the Korg Logue is a lack of control space for the User Oscillator. SDK provided only 8 controls, sounds like a lot, until you need to do some multidimensional modulation for complex models. then, you run out of control space fast; each input needs a Bias value for a starting point for the note, and a modulation positive or negative Intensity. so, a three input Plaits model consumes 6 of the available 8 SDK controls for Bias and Intensity controls for each modulation channel just to get started. the remaining two controls are used to manage Envelope modulation sources and modulation types; LFO, Envelope, Key Tracking are assigned to inputs based on the inputs behavior; generally Timbre get an envelope, Morph gets the envelope and the LFO, and the Harmonics input gets Key Tracking. although, some models may have different assignments where it makes sense to do so. mkII has a few extra controls, so more complex schemas with multiple permutations of modulation controls can be more easily implemented with an Index to select modulation assignment in the future. in M5, all three modulation assignments are *concurrent*. you can get some very cool voicing this way. for instance, the physical models map the internal model decay into Key Tracking, so higher notes or lower notes can have different decay times. models with tonal, frequency or pitch modulation characteristics receive an LFO, envelope, or both; allowing twangs, pitch wobbles, arpeggiations, swoops, falls, and rises; very cool! 

To fit this new control schema, the AUX model output mixer was dropped. instead the AUX models were split off into their own models; Waveshaper split into Tides and Warps waveshapers; Virtual Analog into VA and VASync (hard synced oscillators); Granular into Grain and Zbraids (a CZ like filter simulation of Peaking, LP, BP, and HP filter responses); and finally Noise into Noise and NoiseDBP (Dual Bandpass).

Additionally, [NEW model] Virtual VCF from Plaits 1.2 models is included. very cool model. more to come. whee!

Note: the envelope mode controls are still in debug; avoid the '0' Attack setting for the moment; it won't do anything constructive at the moment, nor is it malevolent. the Attack and Decay Modes are encoded into different envelope shapes - as noted in the doc - positive and negative Attack and Decay timing combines to result in AD, AR, ADSR 40% and ADSR 70% sustain type envelopes. for example; +1 Attack and +20 Decay. will be an AR of 1/20; a -1 Attack and +20 Decay will result in an ADSR with attack of 1, and a decay and release of 20, with a sustain at 40%. +/- will present as AR, and -/- as ADSR 70%. these are the same envelope types in M4, but now you can apply the envelope to more than one input at a time.

A caution to new SDK users: there is a Logue SDK1 bug in the initialization of bipolar params (M5 params are *all* bipolar). Pro TIP: when first loading the model, go to the user oscillator param menu; each value initially will appear as zero, if you don't touch it, the next time it will be -100. to avoid this; simply go through each param first one by one, and increment/decrement it by one the first time you see it. this will *really* initialize the front panel to zero, instead of -100, and save you a *lot* of encoder param value twisting later. (yes, my encoder broke already, and i have to replace it very soon). this bug occurs because the front panel display only sends values to the voice cards where the user oscillators reside. it can't receive values from the many model instances, so it assumes any new model has zero as it's initial values; it can't tell if the model uses bipolar or unipolar values, so assume they're always univalue. Bipolar params came in a later firmware. 

In closing, please enjoy these progressive/liberal tariff-free user oscillators.
