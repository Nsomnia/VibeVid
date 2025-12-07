Here is the corrected and refined `README.md`. I have fixed the formatting, professionalized
# VibeVid

A ProjectM-powered music visualizer featuring an advanced text overlay system and professional video recording capabilities.

## Overview

VibeVid is a sophisticated C++ application that transforms audio into stunning visual experiences. By integrating the legendary ProjectM visualization engine with modern features, VibeVid offers advanced text overlay systems, AI-enhanced workflows, and broadcast-ready video recording capabilities.

Designed with a modular architecture, it provides a robust platform for both casual listening and content creation, strictly adhering to modern Linux standards (XDG) and C++20 best practices.

## ✨ Features

### 🎵 Core Functionality
- **ProjectM Integration**: Full audio visualization support with the extensive configurability and preset library of ProjectM.
- **Smart Music Player**: Intuitive drag-and-drop interface into the main playlist. Includes automatic metadata parsing and file type detection for ID3 tags and track information.
- **High-Quality Recording**: FFmpeg-powered video capture engine featuring customizable encoding parameters and default quality presets.
- **Advanced Text Engine**: A dynamic overlay system capable of displaying file metadata, audio tags, or custom text. Includes text effects such as breathing, glow, positional translation, and drop-shadows.

### 🎨 Visual Customization
- **Resolution Independence**: Flawless scaling from 720p up to 4K resolutions.
- **Animation Effects**: Configurable text behaviors including sliding effects, static placement, or custom coordinate translation.
- **Watermark System**: Persistent branding options with customizable text and positioning, ideal for content creators.
- **Shader Preset Management**: Robust management of visualization presets. Includes support for Favorites, a "Record-only" filter, blacklists, and an automatic quarantine system for broken shader code.

### 🛠️ Developer Features
- **Debug Console**: Real-time logging with color-coded output, as well as file-based logging for troubleshooting and programmatic parsing.
- **Address Sanitizer Integration**: Native support for memory leak detection and debugging tools (e.g., GDB).
- **Configuration System**: Persistent settings storage in `$XDG_CONFIG_HOME` (e.g., `$HOME/.config`) using standard formats like TOML.
- **Modular Architecture**: Clean separation of concerns ensures code is maintainable and refactorable. This structure facilitates a cleaner git history and allows for granular modification.

## 🚀 Quick Start

### Automatic Build (Recommended)
```bash
# Clone the repository
git clone https://github.com/Nsomnia/vibevid
cd vibevid

# Run the program setup tui?
# The user would love to use a tui in the appropriate 
```

### Manual Build
```bash
# Create build directory
mkdir build && cd build

# Configure and compile (cmake and make based)
cmake .. && make -j$(nproc)

# If you only have Make available (only make fallback):
make
```






---

**AGENT NOTES:**
You can use git, gh, or jj to manage the users git repository. Commit and push frequently to have an easy way to revert or make manual patches/replacemnts to old logic later.  You may use any package on the users system or instal them via pacman, paru, yay, npm (via nvm), cargo, or otherwise. Keep docs upto date or new ones created when appropriate.


---

**OLD sCRATCHPAD README FROM HERE ON IF NEEDED ELSE REMOVE FROM HERE TO EOF:**


# VibeVid

- Create music videos features projectm visualizer canvas drawn with artist and track information displayed with optional animations over the canvas. 

- Every single possible customization or options for both projectM, this package, and every ascpect of the text, animations, video enoding, audio, hotkeys, etc is customizable to the fullest.

- Recording music videos with intelligent file handling

- Keyboard hotkeys for key actions

- Rate visualizer shader presets, blacklist broken ones manually (or automatically via stdout errors), and favorite (option to enable "only use favorite shaders when recording video mode enabled").

- Playlist of audio files. 

- Thorough multi-page settings window. 

- Configs saved persistantly in $HOME/.config/VibeVid along with any lists or other data needing persistance.  

- Anything windows based milkdrop visualizer packages can do PLUS BATTERIES, included. 

## Future Improvments

- copy Suno Downloader logic to tie to web browser in dev mode and download songs, lyrics, and album art, for your tracks. 



### Jr Dev-Ops Life
Hey, boss, can I push this broken vibe code.
"Did you do pre-commit checks?"
Hellz yes, son! Get some! I am 1337 to the max! 69 the ladies! Schwifity-schive.
"On home, work, production rack, and your toaster, do you use Arch, BTW?"
Uh, no? Sir I use Ubun...
"BE GONE WITH YOU SIRE FOR YOU HAVE FORSAKEN THESTALLMAN WAY! I AM A GOLDEN GOD [lead sr dev]!
