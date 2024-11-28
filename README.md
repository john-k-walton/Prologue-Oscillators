[NEW] [11/28/24] M5 Versions coming soon... those posted are only 1/2 finished debug models; no LFO2 support yet, and reduced Envelope timing ranges. 

One shortcoming of the Korg Logue is a lack of control space for the User Oscillator. SDK provided only 8 controls, sounds like a lot, until you need to do some multidimensional modulation for complex models. then, you run out of control space fast; each input needs a Bias value for a starting point for input during the note, and a modulation Intensity. so, a three input Plaits model consumes 6 of the available 8 SDK controls for Bias and Intensity controls for each modulation channel just to get started. the remaining two controls are used to manage Envelope modulation sources and modulation types; LFO, Envelope, Key Tracking are assigned to inputs based on the inputs behavior; generally Timbre get an envelope, Morph gets the envelope and the LFO, and the Harmonics input gets Key Tracking. although, some models may have different assignments where is makes sense to do so. mkII has a few extra controls, so more complex schemas with multiple permutations of modulation controls can be more easily implemented with an Index to select modulation assignment. all three assignments are *concurrent*. you can get some very cool voicing this way. for instance the physical models map the internal model decay into Key Tracking, so higher notes or lower notes will have different decay times. very cool! to fit the control schema, the AUX model output mixer was dropped. instead the AUX models were splits off into their own models; Waveshaper split into Tides and Warps waveshapers; Virtual Analog into VA and VASync (hard synced oscillators); Granular into Grain and Zbraids (a CZ like filter simulation of Peaking, LP, BP, and HP filter responses); and finally Noise into Noise and NoiseDBP (a dual Bandpass version).

Additionally, [NEW model] Virtual VCF from Plaits 1.2 models is included. very cool model. more to come. whee!

Notes: as folks should know by now... there is a Logue SDK bug in the initialization of bipolar params (M5 params are *all* bipolar). Pro TIP: when first loading the model, go to the user oscillator param menu; each value initially will appear as zero, if you don't touch it, the next time it will be -100. to avoid this; simply go through each param first one by one, and increment/decrement it by one the first time you see it. this will *really* initialize it to zero, and save you a *lot* of encoder param value twisting later. (yes, my encoder broke already, and i have to replace it). this bug occurs because the front panel display only sends values to the voice cards where the user oscillators reside. it can't receive values from the many model instances, so it assumes any new model has zero as it's initial values; it can't tell if the model uses bipolar or unipolar values, so assume they're always univalue. Bipolar params came in a later firmware. 

Further note: the Attack and Decay Modes are encoded into different envelope shapes - as noted in the doc - positive and negative envelope timing combins to result in AD, AR, ADSR 40% and ADSR 70% sustain type envelopes. so, +1 Attack, and +20 Decay, will be an AR of 1/20. a -1 Attack and +20 Decay will result in an ADSR with attack of 1, and a decay and release of 20, and a sustain of 40%. +/- will present as AR, and -/- as ADSR 70%. these are the same envelope types in M4, but now you can apply the envelope to more than one input.

So, please enjoy these progressive, and liberal tariff-free user oscillators; screw Trump and have some fun instead while Leopards Feast on their Faces.
