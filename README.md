[NEW] [12/14/24]
first half of LFO2 mode finished. four options are provided:
1. LFO2 + LFO; both LFO's are added then applied to the modulation channel. this superimposes both LFO's on thehsame channel for dual cresting wave romps. [done]
2. LFO2 * LFO, LFO's are multiplied together. this envelopes one LFO with the other; as one LFO diminishes it also reduces the other. this provides a 'beathing' LFO type of effect. [done]
3. LFO2 appears as slightly damped vibration, with key tracked vibration rate. this provides a pitch dependent vibraphone type of modulation.
4. LFO2 appears as a damped tremolo with key track amplitude.
5. BONUS Mode: DoubleZero! no modulation? nah... triphase LFO? hmmm...
   
... and i ran out of memory on the string model again. this happened last time as well. have to switch some stuff up on that model. so that model wasn't updated beyond LFO2 mode 1. Wavetable also got update, but haven't updaetd spreadsheet yet; LFO2[x]LFO on channel 1, LFO2 only on channel 2. download M5_demo_oscillators_3 for latest models.


Enter LFO2 mode 1 & 2 with Attack Mode = '0'. +/- Decay Mode will set the LFO2 frequency; + LFO2+LFO, - LFO2*LFO.

fun tip: layer VAsync with WTA. wowser! 

-------------------------------------
[12/13/24] models are now mostly playable. only the LFO2 implementation and some fine tuning of timing ranges after playing them a more. (download M5 demo oscillators 2).

finished Envelope options:
1. models with a spectral Timbre response get exponential, others a linear attack. this helps snappiness where it matters without giving up a a smoother onset for other models.
2. setting the Decay to +100 signals linear ramp attack with no decay/release. good for doppler shifts, long spectral rises, and other NRZ tricks.
3. exponential attacks will terminate with note_off, more natural than always completing. linear doesn't terminate early.
4. envelope timing is split into two ranges; a fast range, and a slow range (over 50-60 is slow) for now. currently using a log2 func for exp attack, may switch to LUT's for envelope and timing.

Each model now has customized envelope slope, and timing range depending on the models spectral response and expected envelope use cases.
minor retargetting of some mod channels on some models.

----------
[12/01/24] retargeted some modulation channels, and added an MOD Channel 3 KT+LFO channel option for better voicing possibilities, also MOD Channel 1 Env+LFO for some nice Timbre tickling fun. included all platforms for all supported 1.0 and 1.2 modules now. Also included are Plaits 2D Wavetables. These were rendered as interpolated only (input 3 removed as well as lo-fi AUX model output), with it's own modulation channel definitions to accomodate the larger control schemas for wavetables. these version have more modulations, and more options for modulation. Layering is even wilder with these :0)

There are currently 25 models available across 75 oscillators in this base Plaits release. other Wavetables oscillators are also in the works.

*ugh, just noticed that BLOCKSIZE for NTS is probably wrong for VCF module in new codebase. 1.2 VCF XD is fine, same as Prologue. 1.0's are ok on NTS. more work to do for next releases. lol).*

----------------------
[11/28/24] M5 Versions coming soon... those posted are only 1/2 finished debug models; no LFO2 support yet, and reduced Envelope timing ranges. 

One shortcoming of the Korg Logue is a lack of control space for the User Oscillator. SDK provided only 8 controls, sounds like a lot, until you need to do some multidimensional modulation for complex models. then, you run out of control space fast; each input needs a Bias value for a starting point for the note, and a modulation positive or negative Intensity. so, a three input Plaits model consumes 6 of the available 8 SDK controls for Bias and Intensity controls for each modulation channel just to get started. the remaining two controls are used to manage Envelope modulation sources and modulation types; LFO, Envelope, Key Tracking are assigned to inputs based on the inputs behavior; generally Timbre get an envelope, Morph gets the envelope and the LFO, and the Harmonics input gets Key Tracking. although, some models may have different assignments where it makes sense to do so. mkII has a few extra controls, so more complex schemas with multiple permutations of modulation controls can be more easily implemented with an Index to select modulation assignment in the future. in M5, all three modulation assignments are *concurrent*. you can get some very cool voicing this way. for instance, the physical models map the internal model decay into Key Tracking, so higher notes or lower notes can have different decay times. models with tonal, frequency or pitch modulation characteristics receive an LFO, envelope, or both; allowing twangs, pitch wobbles, arpeggiations, swoops, falls, and rises; very cool! 

To fit this new control schema, the AUX model output mixer was dropped and the AUX models were split off into their own models; Waveshaper split into Tides and Warps waveshapers; Virtual Analog into VA and VASync (hard synced oscillators); Granular into Grain and Zbraids (a CZ like filter simulation of Peaking, LP, BP, and HP filter responses); and finally Noise into Noise and NoiseDBP (Dual Bandpass).

Additionally, a [NEW model] Virtual VCF from Plaits 1.2 models is included. very cool model. more to come. whee! try layering VCF with itself, setting both layers Multirouting to POST; now you have have two digital OSC/VCF's and two analog VCO/VCF to play with, great for lush pads.

Note: the envelope mode controls are still in debug; the Attack and Decay Modes are encoded into different envelope shapes - as noted in the doc - positive and negative Attack and Decay timing combines to result in AD, AR, ADSR 40% and ADSR 70% sustain type envelopes. for example; +1 Attack and +20 Decay. will be an AR of 1/20; a -1 Attack and +20 Decay will result in an ADSR with attack of 1, and a decay and release of 20, with a sustain at 40%. +/- will present as AR, and -/- as ADSR 70%. these are the same envelope types in M4, but now you can apply the envelope to more than one input at a time.

A caution to new SDK users: there is a Logue SDK1 bug in the initialization of bipolar params (M5 params are *all* bipolar). Pro TIP: when first loading the model, go to the user oscillator param menu; each value initially will appear as zero, if you don't touch it, the next time it will be -100. to avoid this; simply go through each param first one by one, and increment/decrement it by one the first time you see it. this will *really* initialize the front panel to zero, instead of -100, and save you a *lot* of encoder param value twisting later. (yes, my encoder broke already, and i have to replace it very soon). this bug occurs because the front panel display only sends values to the voice cards where the user oscillators reside. it can't receive values from the many model instances, so it assumes any new model has zero as it's initial values; it can't tell if the model uses bipolar or unipolar values, so assume they're always univalue. Bipolar params came in a later firmware. 

In closing, please enjoy these progressive/liberal tariff-free user oscillators, a product of a free thinking, reality based, democratic society.... while it lasts.
