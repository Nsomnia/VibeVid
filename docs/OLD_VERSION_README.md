# VibeVid

ProjectM powered music visualizer with advanced text overlay system and video recording capabilities.

## Overview

VibeVid is a sophisticated C/C++ application that transforms your music into stunning visual experiences using the ProjectM audio visualization. It combines the legendary ProjectM visualizer with modern AI features, advanced text overlay systems, and professional-grade video recording capabilities.

- LLM developed to Chad level its over 9000 with an "Arch, BTW" quality.
- Jr Dev's of all kinds best read the man pages and get some Stallman quotes to hang in your $XDG_USER_HOME!

## ✨ Features

### 🎵 Core Functionality --- "My artist and song title text dont overlay because its two separate render layers! Do you even write shaders, bro?"
- **ProjectM Integration**: Full audio visualization with custom preset support and the fine-grained advanced configurability and customizability of projectM.
- **Smart Music Player**: Drag-and-drop or open audio files into the main playlist portion of the main UI. Defaults to parsing filename and filetypes for song and file info metadata and ID tag extraction.
- **High-Quality Recording**: FFmpeg-powered video capture with many customizable encoding parameters as well as default quality presets.
- **Advanced Text Engine**: Can display file info, audio tags, and nearly any kind of custom text either manually or dynamically. Text FX i.e. breathing, glow, posiiton translation manipulation, and drop-shadow.

### 🎨 Visual Customization --- "Argys, we have the customizable meat parameters!"
- **Resolution Independent**: Perfect scaling from 720p to 4K.
- **Animation Effects**: Breathing text, sliding effects, static or custom translating positioning.
- **Watermark System**: Allows for persistant and static branding with customizable text and position to brand your videos for advertising.
- **Shader Preset Management**: Handle any number of presets in easy and configurable ways to allow for automation and a unique viewing experiance. Favorites, "Only Use Favorites While Recording" option, blacklist, and automatic broken shader code quarantine system.

### 🛠️ Developer Features "This... IS... CODE SPARTA!"
- **Debug Console**: Real-time logging with color-coded output as well as to log files for manual or programatic parsing to troubleshoot (development focused initally).
- **Address Sanitizer**: Memory leak detection and debugging support (i.e. packages such as gdb etc)
- **Configuration System**: Persistent settings in $HOME/.config aka $XDG_CONFIG_HOME with support for most appropriate type(s) such as TOML.
- **Modular Architecture**: Clean separation of concerns. Keeps code more easily maintable, refactorable, or otherwise modified, leads to cleaner,and more granular git histoy, and overlal just bumps you to the next level of being leet.

## 🚀 Quick Start

### Automatic Build (Recommended)
```bash
# Clone the repository
# Alternativly gh repo clone `<URL>``
git clone https://github.com/Nsomnia/vibevid
cd vibevid

# Run the build script/package/file
# PLANNING TO-DO: Best method to make configuring, customizing, system optomizing, and compiling/building the codebase? Is a shell script may get unweildly and be a pain to update as compile time config oper?
```

### Manual Build
```bash
# If you have CMake and dependencies:
mkdir build && cd build
cmake .. && make -j$(nproc)

# If you only have Make:
make
```

### Test the Build <AI LLM NOTe TO-DO: From old readme but maybe possible to build into the system/script/pipelines?>
```bash
# Check version and features
./vibe-sync --version

# Verify system dependencies (Only archlinux currently)
./vibe-sync --check-deps

# Get detailed build information
./vibe-sync --build-info

# Show help
./vibe-sync --help
```

## 📋 Prerequisites

### For Full Functionality
```bash
sudo pacman -S ... ... ... --needed


```

# RHEL/CentOS
sudo dnf install ... ... ...
```

### Minimal Build (Console Mode)
- **Compiler**: GCC ??+ or Clang ??+
- **C++ Standard**: C++??
- **Build Tools**: Make and/or CMake and/or Ninja and/or auto...?


## 🏗️ Build System

### Supported Build Methods

1. **Automated Build Script** (`build.sh`)
   - Detects available dependencies
   - Attempts to install missing packages
   - Falls back to minimal build if needed

2. **CMake** (When available)
   ```bash
   mkdir build && cd build
   cmake ..
   make -j$(nproc)
   ```

3. **Makefile** (Fallback)
   ```bash
   make
   ```

### Dependency Detection

The build system automatically detects and adapts to available packages:

| Feature | Required Package | Build Status |
|---------|------------------|--------------|
| GUI Framework | Qt6 | Optional |
| Visualizer | ProjectM | Optional |
| Config Parsing | TOML++ | Optional |
| Audio Processing | SDL2, ALSA | Optional |
| Video Recording | FFmpeg | Optional |
| Metadata | TagLib | Optional |

## 🔧 Configuration

### Default Configuration Files
- `config/default-settings.toml` - Application settings
- `config/audio-presets.toml` - Audio processing presets  
- `config/video-presets.toml` - Video recording presets
- `config/help.html` - User help documentation

### Command Line Options
```bash
./vibe-sync --help           # Show help
./vibe-sync --version        # Show version
./vibe-sync --check-deps     # Check dependencies
./vibe-sync --build-info     # Detailed build info
```

### Environment Variables
```bash
# Override config directory
export VIBE_SYNC_CONFIG_DIR="/path/to/config"

# Enable debug mode
export VIBE_SYNC_DEBUG=1
```

## 🎯 Usage Examples

### Basic Usage
1. **Load Music**: Drag audio files into the playlist
2. **Select Preset**: Browse visualizer presets
3. **Configure Text**: Set up watermarks and overlays
4. **Record Video**: Capture your music visualization

### Advanced Recording
```bash
# High quality recording
./vibe-sync --preset "crown" --quality ultra

# Custom output location
./vibe-sync --output "/path/to/video.mp4"

# Debug mode
./vibe-sync --debug --log-level 5
```

## 🏛️ Project Structure

```
vibe-sync/
├── src/                     # Source code
│   ├── main.cpp            # Application entry point
│   ├── core/               # Core utilities and systems
│   ├── engine/             # Audio/visual engines
│   ├── ui/                 # User interface components
│   ├── integrations/       # External library integrations
│   ├── utils/              # Utility functions
│   └── debug/              # Debug and monitoring
├── config/                  # Configuration files
├── assets/                  # Application assets
├── docs/                    # Documentation
├── build.sh                # Automated build script
├── Makefile                # Fallback build system
└── CMakeLists.txt          # CMake build configuration
```

## 🐛 Troubleshooting

### Build Issues

**CMake not found:**
```bash
# Install CMake
sudo apt install cmake

# Or use Makefile fallback
make
```

**Qt6 not found:**
```bash
# Install Qt6 development packages
sudo apt install qt6-base-dev qt6-multimedia-dev

# Build will continue in console mode
```

**ProjectM not found:**
```bash
# Install ProjectM
sudo apt install libprojectm-dev

# Visualizer will be disabled
```

### Runtime Issues

**Permission denied on build script:**
```bash
# Run with bash directly
bash build.sh
```

**Missing dependencies at runtime:**
```bash
# Check what's available
./vibe-sync --check-deps

# Install missing packages
sudo apt install <package-name>
```

### Common Solutions

1. **Clean rebuild:**
   ```bash
   rm -rf build
   bash build.sh
   ```

2. **Check compiler version:**
   ```bash
   g++ --version  # Need C++20 support
   ```

3. **Verify library paths:**
   ```bash
   pkg-config --list-all | grep -E "(qt6|projectM|ffmpeg)"
   ```

## 🧪 Testing

### Build Verification
```bash
# Test basic functionality
./vibe-sync --version
./vibe-sync --check-deps

# Test all features
make test  # (when tests are available)
```

### Debug Mode
```bash
# Enable all debug output
./vibe-sync --debug --log-level 5

# Check memory leaks
valgrind ./vibe-sync --test-mode
```

## 🚧 Development

### Adding Dependencies

1. **Update CMakeLists.txt** to find the new package
2. **Modify main.cpp** to use conditional compilation
3. **Test build** with and without the dependency

### Code Style
- Follow C++20 standards
- Use RAII principles
- Implement proper error handling
- Add comprehensive logging

### Contribution Guidelines
1. Fork the repository
2. Create feature branch: `git checkout -b feature-name`
3. Test with minimal dependencies
4. Update documentation
5. Submit pull request

## 📄 License

This project is open source. See LICENSE file for details.

## 🙏 Acknowledgments

- **ProjectM Team** - Audio visualization engine
- **Qt Framework** - Cross-platform UI toolkit  
- **FFmpeg** - Multimedia processing
- **MiniMax** - AI integration and support

---

**Vibe-Sync** - AI-powered music visualization platform 🎵✨

For support and questions, please check the troubleshooting section or create an issue.
