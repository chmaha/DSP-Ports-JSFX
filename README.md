# DSP to JSFX

Open-source DSP ported to JSFX for REAPER. Every plugin's header names the original it was ported from and its license.

## Install

There are two ways to install the plugins. Use one or the other, not both.

### ReaPack (recommended, keeps everything up to date)

1. In REAPER, open **Extensions → ReaPack → Import repositories…** and paste:

   ```
   https://github.com/chmaha/DSP-Ports-JSFX/raw/main/index.xml
   ```

2. Open **Extensions → ReaPack → Browse packages…**, filter by **DSP to JSFX**, and install the plugins you want.
3. The plugins then appear in the FX browser under **JS**.

ReaPack also installs each plugin's `Dependencies` files and keeps everything up to date.

### ReaperPkg bundles (no ReaPack needed)

Each [release](https://github.com/chmaha/DSP-Ports-JSFX/releases) has a single `.ReaperPkg` file that installs a whole set of plugins with their `Dependencies` files:

- **DSP to JSFX**: every plugin except Break Room ([latest release](https://github.com/chmaha/DSP-Ports-JSFX/releases/latest)).
- **Break Room**: the mini-games plugin and its music.

Download the `.ReaperPkg` file and open it in REAPER to install. The plugins then appear in the FX browser under **JS: DSP to JSFX/Plugin Ports**. Bundles don't update themselves: download the newer bundle when a new release comes out.

### Manual install

Copy the plugin's `.jsfx` file into your REAPER `Effects` folder (**Options → Show REAPER resource path…**). For every plugin that has files in `Dependencies` (the drum kits, the unplugred ports and others), also copy the `Dependencies` folder that sits next to the `.jsfx` (each plugin needs its own subfolder, such as `Drumkits`, `Scope` or `VU`), and keep it next to the `.jsfx`.

## User guide

See the [DSP to JSFX manual (PDF)](https://chmaha.github.io/DSP-Ports-JSFX/DSP-to-JSFX-Manual.pdf) for a quick start to each plugin's controls, with screenshots of every plugin.

## Instruments

- **Synthy McSynthface**: four instruments in one (ePiano, JX10, DX10 and Piano), ported from the mda plugins via [mda-lv2](https://gitlab.com/drobilla/mda-lv2).
- **Jexed**: DX7-style FM synthesizer, ported from [Dexed](https://github.com/asb2m10/dexed). Includes 1056 voices (Dexed_01 and SynprezFM_01–32 cartridges) and a full voice editor with operator copy/paste and a simple ADSR mode for setting several envelopes at once.
- **JamSynth**: subtractive synthesizer with 28 factory banks and a 128-slot user bank, ported from [amsynth](https://github.com/amsynth/amsynth).
- **Tolerable Tines**: electric piano, ported from Ardour's [ACE Reasonable Synth](https://github.com/Ardour/ardour/tree/master/libs/plugins/reasonablesynth.lv2).
- **Partiality**: additive and modulation synthesizer, ported from the ADsynth engine of [ZynAddSubFX](https://github.com/zynaddsubfx/zynaddsubfx). Includes eight voices per note, each with its own harmonic oscillator and modulator, unison, noise sources, envelopes and LFOs, five filter types, poly, mono and legato modes, 19 factory patches and 122 instruments converted from the ZynAddSubFX banks.
- **Console Yourself**: chip-synth instrument with the sound hardware of six game consoles: NES (with the Famicom VRC6 and VRC7 expansion chips, from [Nes_Snd_Emu](http://slack.net/~ant/libs/audio.html) and [ymfm](https://github.com/aaronsgiles/ymfm)), Game Boy, Master System / Game Gear and PC Engine (from [MAME](https://github.com/mamedev/mame)), Mega Drive (YM2612 or YM3438 FM with a patch editor, from ymfm) and Super NES (S-DSP with echo, from [snes_spc](http://slack.net/~ant/libs/audio.html), playing Doug Fraker's 203 [BRR samples](https://github.com/nesdoug/SNES_13)). Layer mode stacks up to 16 chips for chords (or plays a single channel, such as the NES triangle for bass), with drums on MIDI channel 10; Tracker mode maps MIDI channels to the chip's hardware channels. The Game Boy and PC Engine waves can be drawn by hand.
- **Dr. Nine**: drum synthesizer, ported from [9W9](https://github.com/athousanddetails/schwung-9W9).
- **Skin in the Game**: drum voice, ported from the 4ms [Drum and Djembe](https://github.com/4ms/metamodule-core-modules) modules (4ms CoreModules for MetaModule and VCV Rack). Drum is a two-operator FM drum with pitch, FM, tone and noise envelopes; Djembe is a 20-mode resonant hand drum struck by filtered noise (from Faust's pm.djembe). Any MIDI note strikes the drum and holding it holds the gate. Key Track lets the note set the pitch with up to four voices, and an optional Velocity switch scales each hit.
- **Strum und Drang**: chord harp and rhythm box in the style of the Suzuki Omnichord OM-84, ported from [KoniSynth](https://github.com/k0n1m4k1/KoniSynth)'s Omnichord engine. 84 chords from three rows of chord buttons (major, minor and 7th, combined for dim, maj7, m7 and aug), played from the keyboard as the hardware's button grid or by intervals, a 13-string strum plate on the keys above the split point or the mod wheel, a held chord voice, auto bass, 12 rhythms on CR-78 drum voices that sync to REAPER, and a plate reverb.
- **Kick Back**: analog rhythm machine with three kits: the Roland TR-808, ported from [Mz808](https://github.com/simozzer/Mz808) by Simon Moscrop (bridged-T resonators after Werner, Abel and Smith) and calibrated against Michael Fischer's recordings of a real TR-808, and the Roland CR-78 and Korg Mini Pops 7, ported from [KoniSynth](https://github.com/k0n1m4k1/KoniSynth)'s drum machine engine. The TR-808 panel has every level, tone, tuning, decay and snappy knob of the hardware. Includes 29 rhythm patterns that sync to REAPER, a second pattern to combine with the first, swing, a preview that plays while REAPER is stopped, eight user rhythms with an editor, MIDI out, clickable pads with step lights, named notes in the piano roll and an optional 11-output multi-out.
- **Acid Reign**: TB-303-style acid bass synth, ported from [Open303](https://github.com/RobinSchmidt/Open303). Includes the accent and slide behaviour, the Devil Fish envelope and slide mods, 16 filter modes and a 16-pattern step sequencer that follows a held key (Key Sync) or REAPER's transport (Host Sync).
- **Ring Leader**: resonator, ported from Mutable Instruments [Rings](https://github.com/pichenettes/eurorack/tree/master/rings). Modal resonator, sympathetic strings, inharmonic string, FM voice, quantized sympathetic strings and string + reverb, with 1, 2 or 4 voices, played from MIDI or excited by the track's audio, plus the module's hidden Disastrous Peace string synth.
- **Plait Tectonics**: macro oscillator, ported from Mutable Instruments [Plaits](https://github.com/pichenettes/eurorack/tree/master/plaits). Includes all 24 models of the current firmware: virtual analog (with and without filter), phase distortion, three banks of six-operator FM patches, wave terrain, string machine, chiptune, waveshaping, two-operator FM, granular formants, additive, wavetables, chords, speech, swarm, filtered and particle noise, inharmonic string, modal resonator and analog-style kick, snare and hi-hat. Played from MIDI through the module's low-pass gate.
- **In Your Element**: modal synthesizer, ported from Mutable Instruments [Elements](https://github.com/pichenettes/eurorack/tree/master/elements). Bow, blow and strike exciters feed a 64-mode resonator (or a string, or five strings tuned to a chord), followed by stereo spread and reverb, plus the module's hidden Ominous Voice. Playable from MIDI with velocity and pressure.
- **Chamber Organ**: pipe organ, ported from [Aeolus](https://kokkinizita.linuxaudio.org/linuxaudio/aeolus/).
- **Lord of the Rinks**: tonewheel organ, ported from [setBfree](https://github.com/pantherb/setBfree).
- **AVL Drumkits**: four sampled kits, ported from [avldrums.lv2](https://github.com/x42/avldrums.lv2) with the samples from Glen MacArthur's [AVL Drumkits](http://www.bandshed.net/avldrumkits/): **Captain's Kit**, **Led Head** and **Goldibops** (acoustic kits with five velocity layers) and **Busk Stop** (hand percussion). Each kit maps to the General MIDI drum notes, with hi-hat and cymbal chokes and a clickable kit photo.
- **Major General MIDI**: General MIDI wavetable synthesizer, ported from the [Sonivox EAS](https://github.com/pedrolcl/sonivox) engine.
- **Scoring Synth**: General MIDI and GS workstation, ported from [FluidSynth](https://www.fluidsynth.org) and playing S. Christian Collins' [GeneralUser GS](https://www.schristiancollins.com) sound set.
- **Sound Blasted!**: 16-channel multitimbral SoundFont (SF2) General MIDI synthesizer, ported from [FluidSynth](https://www.fluidsynth.org) and playing Stardream Studios' HL4MGM sound set. Includes FluidSynth's reverb and chorus, 80 historical temperaments and GM, GM2, GS and XG reset SysEx.
- **Kaminari**: taiko drums, ported from the [sfizz](https://sfz.tools/sfizz) SFZ engine and playing S. Christian Collins' SCC Taiko Drums. Fifteen drums and hits on key pairs from C2 to A#4, with velocity layers and round robins.
- **Evangelina Symphonica Brass**: orchestral brass, ported from the [sfizz](https://sfz.tools/sfizz) SFZ engine and playing [Sonatina Symphonic Orchestra](https://github.com/peastman/sso). Solo trumpet, horn, tenor and bass trombone, trumpet, horn and trombone sections, tuba and all brass, with every articulation of the library on key switches (sustains, legato, marcato, staccato) and dynamics on the mod wheel or from velocity. Eight multi-timbral slots, each with its own instrument, MIDI channel, volume and pan, with stereo or 16-channel output; samples load only for the instruments in use.
- **Evangelina Symphonica Chorus**: choir, ported from the [sfizz](https://sfz.tools/sfizz) SFZ engine and playing [Sonatina Symphonic Orchestra](https://github.com/peastman/sso). Mixed or large chorus singing a sustained "ah", with dynamics on the mod wheel or from velocity.
- **Evangelina Symphonica Espressivo String Ensemble**: string ensemble, ported from the [sfizz](https://sfz.tools/sfizz) SFZ engine and playing S. Christian Collins' SCC Expressive Strings. Seven key-switched articulations (legato with expression or velocity control, staccato, pizzicato, tremolo and a legato/tremolo crossfade on the soft pedal), with expression on the mod wheel, breath, foot or expression controller.
- **Evangelina Symphonica Harp**: concert harp, ported from the [sfizz](https://sfz.tools/sfizz) SFZ engine and playing [Sonatina Symphonic Orchestra](https://github.com/peastman/sso). Plays the full concert range, Cb1 to G#7.
- **Evangelina Symphonica Keys**: orchestral keyboards, ported from the [sfizz](https://sfz.tools/sfizz) SFZ engine and playing [Sonatina Symphonic Orchestra](https://github.com/peastman/sso). Grand piano with half-pedalling and sympathetic resonance, harpsichord with 8', 4' and both choirs, and a 14-stop church organ with clickable stop tabs, a swell pedal on the mod wheel and the library's registrations on key switches. Eight multi-timbral slots, each with its own instrument, MIDI channel, volume and pan, with stereo or 16-channel output; samples load only for the instruments in use.
- **Evangelina Symphonica Percussion**: orchestral percussion, ported from the [sfizz](https://sfz.tools/sfizz) SFZ engine and playing [Sonatina Symphonic Orchestra](https://github.com/peastman/sso). Timpani, bass drum and snare, cymbals and tamtam, triangle, congas, the full unpitched kit, glockenspiel, xylophone, marimba hits and rolls, vibraphone with motor speed and damper pedal, celeste, chimes and crotales. Eight multi-timbral slots, each with its own instrument, MIDI channel, volume and pan, with stereo or 16-channel output; samples load only for the instruments in use.
- **Evangelina Symphonica Strings**: string sections and soloists, ported from the [sfizz](https://sfz.tools/sfizz) SFZ engine and playing [Sonatina Symphonic Orchestra](https://github.com/peastman/sso). First and second violins, violas, celli, basses, five soloists and all strings, with every articulation of the library on key switches (sustain, legato, marcato, staccato, pizzicato, col legno, tremolo, harmonics), dynamics on the mod wheel or from velocity, and vibrato on CC21. Eight multi-timbral slots, each with its own instrument, MIDI channel, volume and pan, with stereo or 16-channel output; samples load only for the instruments in use.
- **Evangelina Symphonica Woodwinds**: woodwinds, ported from the [sfizz](https://sfz.tools/sfizz) SFZ engine and playing [Sonatina Symphonic Orchestra](https://github.com/peastman/sso). Piccolo, flutes, alto flute, oboes, cor anglais, clarinets, bass clarinet, bassoons, contrabassoon and all woodwinds, with every articulation of the library on key switches (sustains, legato, marcato, staccato) and dynamics on the mod wheel or from velocity. Eight multi-timbral slots, each with its own instrument, MIDI channel, volume and pan, with stereo or 16-channel output; samples load only for the instruments in use.
- **Tine Capsule**: sampled 1977 Mark I Stage 73 electric piano, ported from the [sfizz](https://sfz.tools/sfizz) SFZ engine and playing Jeff Learman's [jRhodes3d](https://github.com/sfzinstruments/jlearman.jRhodes3d) samples. Five velocity layers with or without crossfades, the instrument file's tremolo and autopan, and a sustain pedal with half-pedalling and re-pedalling. Plays E1 to E7, or the full 88 keys.
- **Grand Designs**: sampled Yamaha CP80 electric grand, ported from the [sfizz](https://sfz.tools/sfizz) SFZ engine and playing Greg Sullivan's [CP80 samples](https://github.com/sfzinstruments/GregSullivan.E-Pianos). Four velocity layers with the samples' own sustain loops, release and velocity tracking controls, and a sustain pedal with half-pedalling and re-pedalling. Plays the full 88 keys.
- **Sticky Situation**: sampled Hohner Pianet T reed piano, ported from the [sfizz](https://sfz.tools/sfizz) SFZ engine and playing Greg Sullivan's [Pianet T samples](https://github.com/sfzinstruments/GregSullivan.E-Pianos). Two velocity layers plus key-release samples that fade the longer a key is held, release and velocity tracking controls, and a sustain pedal with half-pedalling and re-pedalling. Plays F1 to E6.
- **Out of This Wurld**: sampled Wurlitzer EP200 electric piano, ported from the [sfizz](https://sfz.tools/sfizz) SFZ engine and playing Greg Sullivan's [EP200 samples](https://github.com/sfzinstruments/GregSullivan.E-Pianos). Four velocity layers with the samples' own sustain loops, release and velocity tracking controls, and a sustain pedal with half-pedalling and re-pedalling. Plays A1 to C7.
- **Super Color**: sampler with fifteen sounds playable from B3 to G5, ported from unplugred's [MPaint](https://github.com/unplugred/vsts).

## Effects

- **Mixing and mastering, from the x42 plugins** (Robin Gareus): Compressor ([darc](https://github.com/x42/darc.lv2)), EQ ([fil4](https://github.com/x42/fil4.lv2)), Limiter ([dpl](https://github.com/x42/dpl.lv2)) and Dizzy rotary speaker (b_whirl from [setBfree](https://github.com/pantherb/setBfree)).
- **Autotuner**: automatic pitch correction, ported from x42 [fat1](https://github.com/x42/fat1.lv2) (Robin Gareus), based on zita-at1 (Fons Adriaensen). Corrects to the notes you enable, a key/scale preset or live MIDI notes, with bias, filter, correction amount, offset, MIDI pitch bend, a fast low-latency mode and per-note microtonal detune. Stereo is linked.
- **From the [zam-plugins](https://github.com/zamaudio/zam-plugins)** (Damien Zammit): Gate ([ZamGateX2](https://github.com/zamaudio/zam-plugins/tree/master/plugins/ZamGateX2)), Maximizer ([ZaMaximX2](https://github.com/zamaudio/zam-plugins/tree/master/plugins/ZaMaximX2)), Multiband Compressor ([ZaMultiCompX2](https://github.com/zamaudio/zam-plugins/tree/master/plugins/ZaMultiCompX2)) and Delay ([ZamDelay](https://github.com/zamaudio/zam-plugins/tree/master/plugins/ZamDelay)).
- **From [lkjb](https://github.com/lkjbdsp/lkjb-plugins)**: Analog EQ ([Luftikus](https://github.com/lkjbdsp/lkjb-plugins/tree/master/Luftikus)) and Final Touch ([ReFine](https://github.com/lkjbdsp/lkjb-plugins/tree/master/ReFine)).
- **From [Airwindows](https://github.com/airwindows/airwindows)**: De-Esser ([DeEss](https://github.com/airwindows/airwindows/tree/master/plugins/LinuxVST/src/DeEss) and [DeBess](https://github.com/airwindows/airwindows/tree/master/plugins/LinuxVST/src/DeBess)) and Saturation ([ChannelX](https://github.com/airwindows/airwindows/tree/master/plugins/LinuxVST/src/ChannelX)).
- **Other ports**: Reverb ([Zita-Rev1](https://kokkinizita.linuxaudio.org/linuxaudio/downloads/index.html)), Inflator ([RCInflator2](https://github.com/ReaTeam/JSFX/tree/master/Distortion)), Intelligent Spectral Compressor ([Spectral Compressor](https://github.com/robbert-vdh/nih-plug)), JuKnow Chorus ([junologue-chorus](https://github.com/peterall/junologue-chorus)), ChronoDupe automatic double tracking ([ADT](https://github.com/SpotlightKid/adt)) and Analog Jam tape stop/start ([cStop](https://github.com/calgoheen/cStop)).
- **Potato Quality**: lo-fi degrader (bit depth down to 4 bits, sample-rate reduction, harmonic thickening, clipping and a steep post filter), ported from mda Degrade via [mda-lv2](https://gitlab.com/drobilla/mda-lv2). Starts clean so you can dial the damage in, in Mono (like the original) or Stereo.
- **Lip Service**: talk box and channel vocoder, ported from mda TalkBox and mda Vocoder via [mda-effects](https://github.com/pluginguru/mda-effects). TalkBox shapes a synth with the formants of your voice (LPC); Vocoder is an 8 or 16 band channel vocoder with freeze and five presets. The synth comes in on the sidechain (channels 3/4) or on one side of a stereo input.
- **Reel Talk**: reel-to-reel tape machine, ported from [CHOW Tape Model](https://github.com/jatinchowdhury18/AnalogTapeModel). Includes the magnetic hysteresis tape model (with RK, NR, neural-network and v1 solvers, oversampled up to 16x), tone and input filters, tape compression, playback head loss, wow and flutter, degradation and chew, and the 94 factory presets.
- **Wax Lyrical**: vinyl record simulator, ported from [Calf Vinyl](https://github.com/calf-studio-gear/calf) (Markus Schmidt). Includes the once-per-revolution drone wobble at 33, 45 or 78 rpm, aging that narrows the frequency range like a worn record, and seven noise layers (Hum, Motor, Static, Noise, Rumble, Crackle and Crinkle), each with its own level and pitch, played through the same FluidSynth port as Scoring Synth.
- **Silver Lining**: granular texture processor, ported from Mutable Instruments [Clouds](https://github.com/pichenettes/eurorack/tree/master/clouds). Granular, pitch shifter/time stretcher, looping delay and spectral modes, four buffer qualities from 16-bit stereo to lo-fi 8-bit mono, freeze, feedback and reverb, with MIDI triggering and transposition. Runs at the module's 32 kHz.
- **Bead Time Story**: granular texture synthesizer, ported from Mutable Instruments [Beads](https://github.com/pichenettes/eurorack/tree/master/beads). Grains seeded at random, regularly, by hand or by MIDI, a multi-tap delay and beat slicer with Size fully clockwise, random and smooth modulation on every knob, four quality settings from clean 48 kHz digital to dirty mu-law tape with wow and flutter, feedback, reverb and the module's wavetable synth.
- **Sugar and Space**: plate reverb, ported from [Plateau](https://github.com/ValleyAudio/ValleyRackFree) by Dale Johnson (Valley Audio Soft), after Jon Dattorro's 1997 design. Pre-delay, input and tank filters, size up to four times the original plate, diffusion, decay, modulation with rate, shape and depth, Hold for an endless tail, Clear, a tuned mode for resonator effects and an optional soft-drive output. The tank keeps the same size and decay at every sample rate (the original only does at 44.1 kHz).
- **Warp Factor**: meta-modulator, ported from Mutable Instruments [Warps](https://github.com/pichenettes/eurorack/tree/master/warps). Morphs two inputs through crossfade, wavefolding, analog and digital ring modulation, XOR and comparator to a 20-band vocoder with release and freeze. Includes the internal oscillator, sidechain input on channels 3/4 and the module's hidden frequency shifter.
- **Squishy**: a flexible compressor with a touch of citrus, ported from [Squeezer](https://github.com/mzuther/Squeezer) by Martin Zuther. Feed-forward or feed-back design, FET or optical gain stage, linear, smooth or logarithmic release, peak or RMS sensing, three knee widths, upward expansion below 1:1, stereo link, input trim, auto or manual make-up gain, wet mix for parallel compression, and a side-chain with an external input, filters and listen. Knobs snap to tuned values or turn continuously. Four skins.
- **Lumina Channel Strip**: tape, HPF/LPF, gate, analog EQ, compressor, saturation, limiter and true peak metering in one plugin, built from the ports above.
- **Original design**: Dynamic Tilt, a tilt EQ whose slope follows the signal.

## calfNXT

The complete [calfNXT](https://calfnxt.org) suite by Markus Schmidt (derived from Calf Studio Gear by Krzysztof Foltman and Thor Harald Johansen), apart from the Impulse convolver. Every plugin keeps the calfNXT look, with dark and light themes and five accent colours.

- **Aligner NXT**: eight-lane time aligner and mixer for multi-microphone recordings. Per-lane delay trim, join, polarity, gain, pan, mute and solo, a stereo reference input on channels 9/10, hit waveforms and per-lane correlation through an analysis band-pass, and a master delay reported as delay compensation.
- **Analyzer NXT**: stereo spectrum (1k to 8k FFT, three scales) with a difference view, BS.1770-4 loudness (momentary, short-term, integrated, range and true peak) with EBU, ATSC, -14 and -16 LUFS targets, level meters, correlation and a goniometer.
- **Bender NXT**: pitch-pedal shifter over +/-24 semitones with optional semitone or whole-tone snapping, glide, grain quality, tone and mix.
- **Chorus NXT**: stereo chorus with one to eight voices, phase spread and overlap, stereo phase, wet high and low pass and a channel selector.
- **Compressor NXT**: feed-forward compressor with peak, RMS and opto detection, soft knee, programme-dependent release, mix, stereo link modes and an external sidechain with 12 to 48 dB/oct filters and listen.
- **Crusher NXT**: bit crusher with continuous bit depth from 1 to 16 (linear or logarithmic), anti-aliasing, DC asymmetry and mix.
- **DeEsser NXT**: de-esser with a filtered detector, wide or split-band reduction, a Rumble mode that turns it into a de-rumbler, channel routing and detector listen.
- **Delay NXT**: tempo-based stereo delay with tap tempo or host sync, Stereo, Ping-Pong, L then R and R then L routings, filtered feedback, stereo width and an echo-pattern chart.
- **Denoiser NXT**: spectral noise reducer with three learnable noise profiles that can be blended, amount, floor, span and offset, a band limit, profile listen and a listen to what is removed.
- **Elliptic NXT**: bass mono maker. A Linkwitz-Riley crossover (12 or 24 dB/oct, 30 to 200 Hz) splits the side signal and Amount pulls the side bass to the centre, while the mid runs through the same filters so the mono sum stays flat. Listen solos the side bass being removed; a goniometer shows the bass band and a correlation meter the full output.
- **Equalizer NXT**: 16-band equalizer (parametric, shelves, pass filters up to 48 dB/oct) where every band works on stereo, left, right, mid or side and can turn dynamic with its own sidechain compressor.
- **Expander NXT**: downward expander and gate with range, hysteresis, hold, a filtered detector, external sidechain and two inhibit keys that keep the gate shut on spill.
- **Filter NXT**: multimode filter (low, high, band pass, band reject and allpass) with resonance, soft clip, mix, inertia, an envelope follower and MIDI note tracking.
- **Flanger NXT**: stereo flanger with feedback, stereo phase and a comb-filter chart.
- **Harmonics NXT**: exciter and saturator: a filtered feed band goes into a transistor-to-tube waveshaper with up to 4x oversampling, and only the added harmonics are mixed back in. Wide, Exciter and Bass presets.
- **Limiter NXT**: look-ahead brickwall limiter with up to 4x oversampling, true peak margin, adaptive release, three gain curves, release hold, transient emphasis, colour, auto level and a difference listen.
- **Multiband Compressor NXT**: two to six bands with flat-summing Linkwitz-Riley crossovers, a full compressor, bypass and listen per band, channel routing and mono.
- **Multiband Limiter NXT**: two to six bands of look-ahead limiting with per-band release and weight, a broadband limiter on the sum, true peak, oversampling, auto level and band and difference listen.
- **Octaver NXT**: pitch-tracking octaver with one and two octaves down, one octave up and a sub oscillator, each with level, balance, tone, formant and listen.
- **Phaser NXT**: stereo phaser with up to 12 stages, feedback, stereo phase and a response chart.
- **Pulsator NXT**: tremolo and auto-pan with five wave shapes, pulse width, per-channel phase, tap tempo or host sync.
- **Reverb NXT**: algorithmic reverb with image-source early reflections of a room you size, a modulated late tail with RT60 decay and damping, input filters, air, wet widening, ducking, gate and freeze.
- **Ringmod NXT**: ring modulator from 1 Hz to 20 kHz with four carrier waves, stereo phase and detune, and two LFOs that sweep the carrier, detune, LFO rate and amount.
- **Split NXT**: mono to stereo splitter with volume, mute and polarity on each side.
- **Stereo NXT**: stereo utility with a seven-mode channel matrix, mid and side level, pan and balance, a high-band side decorrelator, channel delay, stereo base, phase rotation, a goniometer and correlation.
- **Tamer NXT**: spectral resonance tamer that finds and cuts narrow peaks as they happen, with a search range, harmonic protection, an external sidechain and a listen to what is removed.
- **Transients NXT**: transient shaper with attack and sustain amounts, lookahead, soft clip, mix, delta listen and a filtered detector.
- **Tuner NXT**: real-time pitch correction to a scale or the notes held on a MIDI keyboard, with retune and release speed, vibrato and glide preservation, formant control, an optional synthetic vibrato and a pitch history chart.

## MIDI

- **Spaghetti Junction**: modular rack for the 34 x42 MIDI filters, ported from [midifilter.lv2](https://github.com/x42/midifilter.lv2). Patch up to eight filters with cables from MIDI IN to MIDI OUT for serial chains, parallel branches, key splits and layers. Requires REAPER 7 or later.
- **Grid Expectations**: topographic drum sequencer, ported from Mutable Instruments [Grids](https://github.com/pichenettes/eurorack/tree/master/grids). Moves around a 5 x 5 map of drum patterns with fill and chaos for each part, or plays three euclidean rhythms. Follows REAPER's transport or runs free, and drives any drum instrument after it on the track.
- **Losing My Marbles**: random gate and melody generator, ported from Mutable Instruments [Marbles](https://github.com/pichenettes/eurorack/tree/master/marbles). Three gate streams and three random pitch streams with Deja Vu looping, seven gate models and six scales, plus a slower random value sent as a MIDI CC. Follows REAPER's transport or runs free.

## Metering and analysis

- **From the x42 [meters](https://github.com/x42/meters.lv2), [spectra](https://github.com/x42/spectra.lv2) and [testsignal](https://github.com/x42/testsignal.lv2) plugins**: K-Meter, Loudness Meter (EBU R128), True Peak, Needle Meter, Bit Meter, Multiband Correlation Meter, Phase/Frequency Wheel, Stereo Phase Scope (goniometer), Stereo/Frequency Scope, Spectrum Analyzer, Test Signal Generator and Tuner ([tuna](https://github.com/x42/tuna.lv2)).
- **From [unplugred's vsts](https://github.com/unplugred/vsts)**: Oscilloscope (XY mode, sync, grid and colour settings) and VU Meter (adjustable nominal level, rise and decay speed).

## Visualization

- **Sight for Sore Ears** (original design): audio-reactive visualizer with 25 scenes, from Plasma, Nebula and Starfield to Live Score (smoke rising from an 88-key piano), Cymatics, Galaxy and Harmonograph. It reacts to drums on the hit and to note onsets in music without drums, so classical and ambient pieces stay alive too. Includes 12 colour palettes and adjustable sensitivity, speed and quality. Audio passes through untouched.

## Utility

- **Beep Show** (original design, after the feature set of Voxengo Beeper): preview watermarker that puts beeps, low-passed noise bursts or dips in level into audio at a set interval, to protect demos, previews and stems. The material dips during each insertion so the output stays below its peak, and Variation randomises timing, duration, frequency and gain so the marks are hard to remove. The pattern follows the project position, so every render is identical. Zero latency, any number of channels.
- **Side Hustle** (original design, after the feature set of Voxengo MSED): mid-side encoder, decoder and inline mid-side processor. Gain, mute and pan for the mid and side channels, channel swap, polarity flips for both channels or the side alone, correlation and balance meters and a plasma vector scope that draws each octave band at its own radius. Zero latency.
- **Stereo Typical** (original design, after the controls of FLUX:: Stereo Tool): stereo imaging tool with input gain, polarity, mute and pan for each channel, stereo width from mono to extra wide, rotation of the whole image, ten instant presets, input and output peak meters, a phase correlation meter and a goniometer.

## Break Room

**Break Room** (original design) is a collection of 15 little games to play when you need a breather, grouped into Zen and Games on the home screen. They range from calm pieces such as Koi Pond, Rain Window and Pixel Garden to Peggy, Krypton Gigablast, Flop House (Texas Hold'em against twelve rogues) and Hold Your Horses (the whole British racing year). Progress is saved with the project. Audio passes through untouched, and game sound only plays while the transport is stopped or paused, so it never ends up in a render or recording.

See the [Break Room manual (PDF)](https://chmaha.github.io/DSP-Ports-JSFX/BreakRoom-Manual.pdf) for a guide to every game.

## License

Each plugin keeps its original's license, and the JSFX code is released under the same or a compatible license (GPLv3 or later unless stated). The header of each `.jsfx` file gives the details, and each license file sits next to the assets it covers in `Dependencies`.

- **GPLv3 or later** (JSFX code): ports of GPL originals, including the x42 plugins (GPLv2 or later), zam-plugins (GPLv2 or later), Zita-Rev1, Aeolus, setBfree, amsynth, Dexed, mda-lv2, mda-effects (Lip Service, MIT or GPLv2 or later), Spectral Compressor, CHOW Tape Model and ZynAddSubFX, plus Acid Reign (from the MIT-licensed Open303), Wax Lyrical (from Calf Vinyl and FluidSynth, both LGPL 2.1), Console Yourself (from Nes_Snd_Emu and snes_spc, both LGPL 2.1 or later, and the BSD-3-Clause MAME sound cores and ymfm), Skin in the Game (from the GPLv3-or-later 4ms CoreModules), Sugar and Space (from the GPLv3-or-later ValleyRackFree), Squishy (from the GPLv3-or-later Squeezer), the calfNXT ports (from the GPLv3 calfNXT), Grid Expectations (from the GPLv3 Grids) and the other Mutable Instruments ports: Ring Leader, Silver Lining, Plait Tectonics, Bead Time Story, In Your Element, Warp Factor and Losing My Marbles (from the MIT-licensed eurorack code, including the tables in `Dependencies`).
- **MIT**: JuKnow Chorus (Peter Allwin), ChronoDupe (Christopher Arndt), Analog EQ and Final Touch (lkjb), and the Airwindows ports (Chris Johnson).
- **AGPLv3 or later**: the unplugred ports (Oscilloscope, VU Meter, Super Color). **AGPLv3**: Strum und Drang (from KoniSynth) and Kick Back (from Mz808 and KoniSynth). unplugred's image assets and samples are CC BY-NC (non-commercial).
- **Samples**: the AVL Drumkits samples and photos by Glen MacArthur are CC-BY-SA 3.0, and music made with the kits can be licensed freely.
- **Sonatina Symphonic Orchestra v4** (Evangelina Symphonica Brass, Chorus, Harp, Keys, Percussion, Strings and Woodwinds): Creative Commons Sampling Plus 1.0, by Mattias Westlund, Peter Eastman and contributors; the horn section sustains are CC BY-SA 3.0, and the grand piano and harpsichord samples are public domain.
- **SCC Expressive Strings** (Espressivo String Ensemble): released by S. Christian Collins as "use at your own risk", with samples collected from free SoundFont banks.
- **Console Yourself SNES samples**: Doug Fraker's BRR samples are public domain per their author (repository MIT).
- **jRhodes3d samples** (Tine Capsule): CC BY-NC 4.0 by Jeff Learman (non-commercial).
- **Greg Sullivan E-Pianos samples** (Grand Designs, Sticky Situation, Out of This Wurld): CC BY 4.0 by Greg Sullivan; SFZ mapping by kinwie, CC BY 3.0.
- **Sonivox EAS** (Major General MIDI): Apache 2.0 original.
- **Squeezer skin** (Squishy): CC BY-SA 4.0 by Martin Zuther, with a CC0 lemon image by Clker-Free-Vector-Images.

The GPLv3 text is in [LICENSE](LICENSE). The MIT notices are included in the JuKnow Chorus and ChronoDupe sources.
