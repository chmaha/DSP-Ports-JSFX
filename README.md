# DSP to JSFX

Open-source DSP ported to JSFX for REAPER.

- **Jexed**: DX7-style FM synthesizer, ported from [Dexed](https://github.com/asb2m10/dexed). Includes 1056 voices (Dexed_01 and SynprezFM_01–32 cartridges), an LCD voice browser, polyphony from 1 to 256, and a MIDI channel filter.
- **JuKnow Chorus**: Juno-style chorus, ported from [junologue-chorus](https://github.com/peterall/junologue-chorus).
- **OJ-X**: OB-X-inspired polysynth, ported from [OB-Xf](https://github.com/surge-synthesizer/OB-Xf). Includes OB-Xf's 492 CC0 factory patches, an LCD patch browser, polyphony from 1 to 256 (or the patch's own setting), and a MIDI channel filter.
- **Synthy McSynthface**: four instruments in one (ePiano, JX10, DX10 and Piano), ported from the mda plugins via [mda-lv2](https://gitlab.com/drobilla/mda-lv2).

## Install

1. In REAPER, open **Extensions → ReaPack → Import repositories…** and paste:

   ```
   https://github.com/chmaha/DSP-Ports-JSFX/raw/main/index.xml
   ```

2. Open **Extensions → ReaPack → Browse packages…**, filter by **DSP to JSFX**, and install the plugins you want.
3. The plugins then appear in the FX browser under **JS**.

ReaPack also installs each plugin's `Dependencies` files and keeps everything up to date.

### Manual install

Copy the plugin's `.jsfx` file into your REAPER `Effects` folder (**Options → Show REAPER resource path…**). For Jexed, OJ-X and Synthy McSynthface, also copy the `Dependencies` folder that sits next to the `.jsfx`, and keep it next to the `.jsfx`.

## License

Each plugin keeps its original's license:

- **Jexed**: GPLv3 or later. Dexed by Pascal Gauthier; its synth engine is based on Music Synthesizer for Android (Google, Apache 2.0).
- **JuKnow Chorus**: MIT. Original by Peter Allwin.
- **OJ-X**: GPLv3 or later. OB-Xf by the Surge Synth Team, continuing OB-Xd by Vadim Filatov (2DaT) and discoDSP. The bundled patches are CC0, by their authors as credited in each patch.
- **Synthy McSynthface**: GPLv3 or later. Original mda plugins by Paul Kellett (Maxim Digital Audio); LV2 port by David Robillard.

The GPLv3 text is in [LICENSE](LICENSE). The MIT notice is included in the JuKnow Chorus source.
