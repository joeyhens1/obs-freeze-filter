# Freeze Filter for OBS Studio

Plugin for OBS Studio to freeze a source using a filter

# Loop mode
Set **Mode** to **Loop** to play a short clip of the source on repeat instead of a single frozen frame.
When the filter is enabled it records the next **Loop Length** ms of video (live video keeps showing while it records), then loops it:
- **Repeat** plays the clip from start to end over and over
- **Boomerang** plays it forwards, then backwards, then forwards again

The loop is recorded at the OBS output frame rate and kept in video memory only while the filter is enabled.
Each frame takes width x height x 4 bytes (about 8 MB at 1080p), so a 1 second loop at 60 fps uses about 500 MB of video memory.
Loops are limited to 5000 ms and 300 frames.

# Download
https://obsproject.com/forum/resources/freeze-filter.950/

# Build
- Build OBS Studio: https://obsproject.com/wiki/Install-Instructions
- Check out this repository to plugins/freeze-filter
- Add `add_subdirectory(freeze-filter)` to plugins/CMakeLists.txt
- Rebuild OBS Studio

# Donations
https://www.paypal.me/exeldro
