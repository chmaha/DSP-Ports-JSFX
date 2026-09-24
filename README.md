# DSP to JSFX

Open-source DSP ported to JSFX for REAPER.

- **Synthy McSynthface**: four instruments in one (ePiano, JX10, DX10 and Piano), ported from the mda plugins via [mda-lv2](https://gitlab.com/drobilla/mda-lv2).
- **Jexed**: DX7-style FM synthesizer, ported from [Dexed](https://github.com/asb2m10/dexed). Includes 1056 voices (Dexed_01 and SynprezFM_01–32 cartridges), an LCD voice browser, polyphony from 1 to 256, and a MIDI channel filter.
- **JamSynth**: two-oscillator subtractive polysynth, ported from [amsynth](https://github.com/amsynth/amsynth). Includes the 3482 presets from amsynth's 28 banks, an LCD preset browser, a full knob panel with live envelope, LFO and scope displays, and a playable on-screen keyboard.
- **JuKnow Chorus**: Juno-style chorus, ported from [junologue-chorus](https://github.com/peterall/junologue-chorus).
- **ChronoDupe**: automatic double tracking for vocals and other sources, ported from [ADT](https://github.com/SpotlightKid/adt). Four pitch-shifted, delayed copies spread across the stereo field, with a voice display.

## Install

1. In REAPER, open **Extensions → ReaPack → Import repositories…** and paste:

   ```
   https://github.com/chmaha/DSP-Ports-JSFX/raw/main/index.xml
   ```

2. Open **Extensions → ReaPack → Browse packages…**, filter by **DSP to JSFX**, and install the plugins you want.
3. The plugins then appear in the FX browser under **JS**.

ReaPack also installs each plugin's `Dependencies` files and keeps everything up to date.

### Manual install

Copy the plugin's `.jsfx` file into your REAPER `Effects` folder (**Options → Show REAPER resource path…**). For Synthy McSynthface, Jexed and JamSynth, also copy the `Dependencies` folder that sits next to the `.jsfx`, and keep it next to the `.jsfx`.

## License

Each plugin keeps its original's license:

- **Synthy McSynthface**: GPLv3 or later. Original mda plugins by Paul Kellett (Maxim Digital Audio); LV2 port by David Robillard.
- **Jexed**: GPLv3 or later. Dexed by Pascal Gauthier; its synth engine is based on Music Synthesizer for Android (Google, Apache 2.0).
- **JamSynth**: GPLv3 or later. amsynth by Nick Dowell (GPLv2 or later); reverb is Freeverb by Jezar at Dreampoint (public domain).
- **JuKnow Chorus**: MIT. Original by Peter Allwin.
- **ChronoDupe**: MIT. Original by Christopher Arndt.

The GPLv3 text is in [LICENSE](LICENSE). The MIT notices are included in the JuKnow Chorus and ChronoDupe sources.
