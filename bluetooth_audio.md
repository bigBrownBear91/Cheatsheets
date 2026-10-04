# Switch audio between laptop and Bluetooth buds (blueman + pavucontrol)
The laptop output stays the system default. Buds are only used when you choose them.

## Prerequisite: connect the buds
Open `blueman-manager`, right-click the buds (OnePlus Buds Pro 2) and choose Connect. If connecting fails, remove the device, put the buds in pairing mode and pair again (Search, Pair, Trust, Connect).

Open `pavucontrol` for all steps below.

## Switch to buds (everything)
1. Tab Configuration: set the buds profile
   - Headset Head Unit (HFP) for calls (speaker and mic, mono, lower quality)
   - High Fidelity Playback (A2DP) for music only (stereo, no mic)
2. Tab Output Devices: click the green check mark next to the buds (set as fallback)
3. For calls, tab Input Devices: set the buds as fallback for the microphone

## Switch back to laptop output
1. Tab Output Devices: click the green check mark next to Built-in Audio (Analog Stereo)
2. Tab Input Devices: same for the built-in microphone
3. Optional: tab Configuration, set the buds profile back to A2DP, or disconnect them in `blueman-manager`

## Switch to buds for one app only
Use this when the laptop stays the default, e.g. only Teams in the browser should use the buds. The app must be playing or recording, otherwise it is not listed.
1. Tab Configuration: set the buds profile to Headset Head Unit (HFP) if the app needs the mic
2. Tab Playback: use the dropdown next to the app and choose the buds
3. Tab Recording: use the dropdown next to the app and choose the buds as the microphone

Browser alternative: choose speaker and mic in the settings of the app (e.g. Teams, Settings, Devices).

## Notes
- The choice for one app is forgotten when the app closes or the buds disconnect.
- Mic active means HFP, so the sound is worse. Switch back to A2DP after the call.
