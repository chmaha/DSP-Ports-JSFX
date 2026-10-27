# DSP to JSFX

Open-source DSP ported to JSFX for REAPER.

- **Synthy McSynthface**: four instruments in one (ePiano, JX10, DX10 and Piano), ported from the mda plugins via [mda-lv2](https://gitlab.com/drobilla/mda-lv2).
- **Jexed**: DX7-style FM synthesizer, ported from [Dexed](https://github.com/asb2m10/dexed). Includes 1056 voices (Dexed_01 and SynprezFM_01–32 cartridges) and a full voice editor: every DX7 parameter is an automatable control, with an algorithm diagram, six operator pages with live envelopes, LFO, pitch envelope and key scaling, plus Dexed's filter, mono mode, tuning, pitch-bend and controller routing. A 32-slot user cartridge stores your own voices with the project. Polyphony from 1 to 256 and a MIDI channel filter.
- **AVL Drumkits**: four sampled kits, ported from [avldrums.lv2](https://github.com/x42/avldrums.lv2) with the samples from Glen MacArthur's [AVL Drumkits](http://www.bandshed.net/avldrumkits/). Each kit maps to the General MIDI drum notes, with hi-hat and cymbal chokes and a clickable kit photo.
  - **Captain's Kit** (Black Pearl): 4-piece acoustic kit, 26 pieces, five velocity layers, stereo or multi-channel outputs.
  - **Led Head** (Red Zeppelin): 4-piece acoustic kit, 26 pieces, five velocity layers, stereo or multi-channel outputs.
  - **Goldibops** (Blonde Bop): jazz kit played with sticks or Hot Rods, 27 pieces, five velocity layers, stereo or multi-channel outputs.
  - **Busk Stop** (Buskman's Holiday): hand percussion (cajon, congas, shakers, tambourines, claves, cowbell, bucket, bell tree and more), 21 pieces, ten velocity layers.
- **JuKnow Chorus**: Juno-style chorus, ported from [junologue-chorus](https://github.com/peterall/junologue-chorus).
- **ChronoDupe**: automatic double tracking for vocals and other sources, ported from [ADT](https://github.com/SpotlightKid/adt). Four pitch-shifted, delayed copies spread across the stereo field, with a voice display.
- **unplugred ports**, from [unplugred's vsts](https://github.com/unplugred/vsts):
  - **Oscilloscope** (Scope): oscilloscope with XY mode, time and scale controls, hold, sync, grid and colour settings. Click the scope to open the settings panel.
  - **VU Meter** (VU): VU meter with adjustable nominal level, rise and decay speed, and mono or stereo display. Click the meter to open the settings panel.
  - **Super Color** (MPaint): sampler with fifteen sounds playable from B3 to G5, an icon grid to pick the sound, an on-screen keyboard and optional voice limiting.

## Install

1. In REAPER, open **Extensions → ReaPack → Import repositories…** and paste:

   ```
   https://github.com/chmaha/DSP-Ports-JSFX/raw/main/index.xml
   ```

2. Open **Extensions → ReaPack → Browse packages…**, filter by **DSP to JSFX**, and install the plugins you want.
3. The plugins then appear in the FX browser under **JS**.

ReaPack also installs each plugin's `Dependencies` files and keeps everything up to date.

### Manual install

Copy the plugin's `.jsfx` file into your REAPER `Effects` folder (**Options → Show REAPER resource path…**). For every plugin that has a folder in `Dependencies` (Synthy McSynthface, Jexed, the AVL Drumkits, Oscilloscope, VU Meter, Super Color and others), also copy the `Dependencies` folder that sits next to the `.jsfx` (each plugin needs its own subfolder, such as `Drumkits`, `Scope`, `VU` or `SuperColor`), and keep it next to the `.jsfx`.

## License

Each plugin keeps its original's license:

- **Synthy McSynthface**: GPLv3 or later. Original mda plugins by Paul Kellett (Maxim Digital Audio); LV2 port by David Robillard.
- **Jexed**: GPLv3 or later. Dexed by Pascal Gauthier; its synth engine is based on Music Synthesizer for Android (Google, Apache 2.0).
- **AVL Drumkits** (Captain's Kit, Led Head, Goldibops, Busk Stop): JSFX code GPLv3 or later, based on avldrums.lv2 by Robin Gareus (GPLv2 or later). Samples and kit photos by Glen MacArthur, as modified for avldrums.lv2 and reduced to 12-bit, under CC-BY-SA 3.0; each kit's licence file sits next to its samples in `Dependencies/Drumkits`. Music made with the kits can be licensed freely.
- **JuKnow Chorus**: MIT. Original by Peter Allwin.
- **ChronoDupe**: MIT. Original by Christopher Arndt.
- **Oscilloscope, VU Meter, Super Color**: JSFX code AGPLv3 or later, ported from unplugred's vsts. The image assets (Scope, VU) and the samples and images (Super Color) are by unplugred under CC BY-NC (non-commercial); each licence file sits next to the assets in `Dependencies/Scope`, `Dependencies/VU` and `Dependencies/SuperColor`.

The GPLv3 text is in [LICENSE](LICENSE). The MIT notices are included in the JuKnow Chorus and ChronoDupe sources.
