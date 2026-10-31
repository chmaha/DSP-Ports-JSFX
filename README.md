# DSP to JSFX

Open-source DSP ported to JSFX for REAPER. Every plugin's header names the original it was ported from and its license.

## Instruments

- **Synthy McSynthface**: four instruments in one (ePiano, JX10, DX10 and Piano), ported from the mda plugins via [mda-lv2](https://gitlab.com/drobilla/mda-lv2).
- **Jexed**: DX7-style FM synthesizer, ported from [Dexed](https://github.com/asb2m10/dexed). Includes 1056 voices (Dexed_01 and SynprezFM_01–32 cartridges) and a full voice editor.
- **JamSynth**: subtractive synthesizer with 28 factory banks and a 128-slot user bank, ported from [amsynth](https://github.com/amsynth/amsynth).
- **Tolerable Tines**: electric piano, ported from Ardour's [ACE Reasonable Synth](https://github.com/Ardour/ardour/tree/master/libs/plugins/reasonablesynth.lv2).
- **Dr. Nine**: drum synthesizer, ported from [9W9](https://github.com/athousanddetails/schwung-9W9).
- **Chamber Organ**: pipe organ, ported from [Aeolus](https://kokkinizita.linuxaudio.org/linuxaudio/aeolus/).
- **Lord of the Rinks**: tonewheel organ, ported from [setBfree](https://github.com/pantherb/setBfree).
- **AVL Drumkits**: four sampled kits, ported from [avldrums.lv2](https://github.com/x42/avldrums.lv2) with the samples from Glen MacArthur's [AVL Drumkits](http://www.bandshed.net/avldrumkits/): **Captain's Kit**, **Led Head** and **Goldibops** (acoustic kits with five velocity layers) and **Busk Stop** (hand percussion). Each kit maps to the General MIDI drum notes, with hi-hat and cymbal chokes and a clickable kit photo.
- **Major General MIDI**: General MIDI wavetable synthesizer, ported from the [Sonivox EAS](https://github.com/pedrolcl/sonivox) engine.
- **Scoring Synth**: General MIDI and GS workstation, ported from [FluidSynth](https://www.fluidsynth.org) and playing S. Christian Collins' [GeneralUser GS](https://www.schristiancollins.com) sound set.
- **Sound Blasted!**: 16-channel multitimbral SoundFont (SF2) General MIDI synthesizer, ported from [FluidSynth](https://www.fluidsynth.org) and playing Stardream Studios' HL4MGM sound set. Includes FluidSynth's reverb and chorus, 80 historical temperaments and GM, GM2, GS and XG reset SysEx.
- **Kaminari**: taiko drums, ported from the [sfizz](https://sfz.tools/sfizz) SFZ engine and playing S. Christian Collins' SCC Taiko Drums. Fifteen drums and hits on key pairs from C2 to A#4, with velocity layers and round robins.
- **Evangelina Symphonica Espressivo String Ensemble**: string ensemble, ported from the [sfizz](https://sfz.tools/sfizz) SFZ engine and playing S. Christian Collins' SCC Expressive Strings. Seven key-switched articulations (legato with expression or velocity control, staccato, pizzicato, tremolo and a legato/tremolo crossfade on the soft pedal), with expression on the mod wheel, breath, foot or expression controller.
- **Super Color**: sampler with fifteen sounds playable from B3 to G5, ported from unplugred's [MPaint](https://github.com/unplugred/vsts).

## Effects

- **Mixing and mastering, from the x42 plugins** (Robin Gareus): Compressor ([darc](https://github.com/x42/darc.lv2)), EQ ([fil4](https://github.com/x42/fil4.lv2)), Limiter ([dpl](https://github.com/x42/dpl.lv2)) and Dizzy rotary speaker (b_whirl from [setBfree](https://github.com/pantherb/setBfree)).
- **From the [zam-plugins](https://github.com/zamaudio/zam-plugins)** (Damien Zammit): Gate ([ZamGateX2](https://github.com/zamaudio/zam-plugins/tree/master/plugins/ZamGateX2)), Maximizer ([ZaMaximX2](https://github.com/zamaudio/zam-plugins/tree/master/plugins/ZaMaximX2)), Multiband Compressor ([ZaMultiCompX2](https://github.com/zamaudio/zam-plugins/tree/master/plugins/ZaMultiCompX2)) and Delay ([ZamDelay](https://github.com/zamaudio/zam-plugins/tree/master/plugins/ZamDelay)).
- **From [lkjb](https://github.com/lkjbdsp/lkjb-plugins)**: Analog EQ ([Luftikus](https://github.com/lkjbdsp/lkjb-plugins/tree/master/Luftikus)) and Final Touch ([ReFine](https://github.com/lkjbdsp/lkjb-plugins/tree/master/ReFine)).
- **From [Airwindows](https://github.com/airwindows/airwindows)**: De-Esser ([DeEss](https://github.com/airwindows/airwindows/tree/master/plugins/LinuxVST/src/DeEss) and [DeBess](https://github.com/airwindows/airwindows/tree/master/plugins/LinuxVST/src/DeBess)) and Saturation ([ChannelX](https://github.com/airwindows/airwindows/tree/master/plugins/LinuxVST/src/ChannelX)).
- **Other ports**: Reverb ([Zita-Rev1](https://kokkinizita.linuxaudio.org/linuxaudio/downloads/index.html)), Inflator ([RCInflator2](https://github.com/ReaTeam/JSFX/tree/master/Distortion)), Intelligent Spectral Compressor ([Spectral Compressor](https://github.com/robbert-vdh/nih-plug)), JuKnow Chorus ([junologue-chorus](https://github.com/peterall/junologue-chorus)), ChronoDupe automatic double tracking ([ADT](https://github.com/SpotlightKid/adt)) and Analog Jam tape stop/start ([cStop](https://github.com/calgoheen/cStop)).
- **Lumina Channel Strip**: HPF/LPF, gate, analog EQ, compressor, saturation, limiter and true peak metering in one plugin, built from the ports above.
- **Original design**: Dynamic Tilt, a tilt EQ whose slope follows the signal.

## MIDI

- **Spaghetti Junction**: modular rack for the 34 x42 MIDI filters, ported from [midifilter.lv2](https://github.com/x42/midifilter.lv2). Patch up to eight filters with cables from MIDI IN to MIDI OUT for serial chains, parallel branches, key splits and layers. Requires REAPER 7 or later.

## Metering and analysis

- **From the x42 [meters](https://github.com/x42/meters.lv2), [spectra](https://github.com/x42/spectra.lv2) and [testsignal](https://github.com/x42/testsignal.lv2) plugins**: K-Meter, Loudness Meter (EBU R128), True Peak, Needle Meter, Bit Meter, Multiband Correlation Meter, Phase/Frequency Wheel, Stereo Phase Scope (goniometer), Stereo/Frequency Scope, Spectrum Analyzer, Test Signal Generator and Tuner ([tuna](https://github.com/x42/tuna.lv2)).
- **From [unplugred's vsts](https://github.com/unplugred/vsts)**: Oscilloscope (XY mode, sync, grid and colour settings) and VU Meter (adjustable nominal level, rise and decay speed).

## User guide

See [CONTROLS.html](https://htmlpreview.github.io/?https://github.com/chmaha/DSP-Ports-JSFX/blob/main/CONTROLS.html) for the chmaha DSP to JSFX user guide, a quick start for each plugin's controls.

## Install

1. In REAPER, open **Extensions → ReaPack → Import repositories…** and paste:

   ```
   https://github.com/chmaha/DSP-Ports-JSFX/raw/main/index.xml
   ```

2. Open **Extensions → ReaPack → Browse packages…**, filter by **DSP to JSFX**, and install the plugins you want.
3. The plugins then appear in the FX browser under **JS**.

ReaPack also installs each plugin's `Dependencies` files and keeps everything up to date.

### Manual install

Copy the plugin's `.jsfx` file into your REAPER `Effects` folder (**Options → Show REAPER resource path…**). For every plugin that has files in `Dependencies` (the drum kits, the unplugred ports and others), also copy the `Dependencies` folder that sits next to the `.jsfx` (each plugin needs its own subfolder, such as `Drumkits`, `Scope` or `VU`), and keep it next to the `.jsfx`.

## License

Each plugin keeps its original's license, and the JSFX code is released under the same or a compatible license (GPLv3 or later unless stated). The header of each `.jsfx` file gives the details, and each license file sits next to the assets it covers in `Dependencies`.

- **GPLv3 or later** (JSFX code): ports of GPL originals, including the x42 plugins (GPLv2 or later), zam-plugins (GPLv2 or later), Zita-Rev1, Aeolus, setBfree, amsynth, Dexed, mda-lv2 and Spectral Compressor.
- **MIT**: JuKnow Chorus (Peter Allwin), ChronoDupe (Christopher Arndt), Analog EQ and Final Touch (lkjb), and the Airwindows ports (Chris Johnson).
- **AGPLv3 or later**: the unplugred ports (Oscilloscope, VU Meter, Super Color). unplugred's image assets and samples are CC BY-NC (non-commercial).
- **Samples**: the AVL Drumkits samples and photos by Glen MacArthur are CC-BY-SA 3.0, and music made with the kits can be licensed freely.
- **SCC Expressive Strings** (Espressivo String Ensemble): released by S. Christian Collins as "use at your own risk", with samples collected from free SoundFont banks.
- **Sonivox EAS** (Major General MIDI): Apache 2.0 original.

The GPLv3 text is in [LICENSE](LICENSE). The MIT notices are included in the JuKnow Chorus and ChronoDupe sources.
