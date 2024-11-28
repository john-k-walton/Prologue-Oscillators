[NEW] M5 Versions coming soon... those posted are only 1/2 finished debug models; no LFO2 support yet, and reduced Envelope timing ranges. 

One shortcoming of the Korg Logue is a lack of control space for the User Oscillator. SDK provided only 8 controls, sounds like a lot, until you need to do some multidimensional modulation for complex models. then, you run out of control space fast; each input needs a Bias value for a starting point for input during the note, and a modulation intensity. so, a three input models consumes 6 of the available 8 SDK controls right of the bat. the remaining two controls are used to manage modulation sources, and modulation 'types'; LFO, Envelope, Key Tracking are assigned to inputs based on the inputs behavior; generally Timbre get an envelopes, Morph gets the envelope and the LFO, and the Harmonics input gets Key Tracking. although, some models may have different assignments where is makes sense to do so. mkII has a few extra controls, so more complex schemas with multiple permutations of modulation controls can be more easily implemented with an Index to select modulation assignment.

also, VCF from Plaits 1.2 models is included. very cool model. more to come. whee!

notes: there is a Logue SDK bug in the initialization of bipolar params (M5 params are all bipolar). Pro TIP: when first loading the model, goto the user oscillator param menu - each value initially will appear as zero, if you don't touch it, the next time it will be -100. to avoid this simply go through each param and increment/descrement it by one. this will *really* initialize it to zero, and save you a *lot* of encoder twisting.

Also, the Attack and Decay Modes are encoded into different envelope shapes - as noted in the doc - positive and negative envelope timing results in AD, AR, ADSR 40% and ADSR 70% sustain type envelopes. so, +1 Attack, and +20 Decay, will be an AR of 1/20. a -1 Attack and +20 Decay will result in an ADSR with attack of 1, and a decay and release of 20.

so, screw Trump and have some fun instead!
