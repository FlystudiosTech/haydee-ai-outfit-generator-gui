# Haydee AI Outfit Generator GUI

[![Build Test](https://github.com/thegamerbay/haydee-ai-outfit-generator-gui/actions/workflows/ci.yml/badge.svg)](https://github.com/thegamerbay/haydee-ai-outfit-generator-gui/actions/workflows/ci.yml)
[![Build and Release EXE](https://github.com/thegamerbay/haydee-ai-outfit-generator-gui/actions/workflows/release.yml/badge.svg)](https://github.com/thegamerbay/haydee-ai-outfit-generator-gui/actions/workflows/release.yml)
[![Run Tests](https://github.com/thegamerbay/haydee-ai-outfit-generator-gui/actions/workflows/tests.yml/badge.svg)](https://github.com/thegamerbay/haydee-ai-outfit-generator-gui/actions/workflows/tests.yml)
[![Lint](https://github.com/thegamerbay/haydee-ai-outfit-generator-gui/actions/workflows/lint.yml/badge.svg)](https://github.com/thegamerbay/haydee-ai-outfit-generator-gui/actions/workflows/lint.yml)
[![codecov](https://codecov.io/gh/thegamerbay/haydee-ai-outfit-generator-gui/graph/badge.svg?token=YOUR_TOKEN_HERE)](https://codecov.io/gh/thegamerbay/haydee-ai-outfit-generator-gui)

A modern graphical user interface for the [Haydee AI Outfit Generator](https://github.com/thegamerbay/haydee-ai-outfit-generator) library. Easily generate custom outfits for Haydee without messing with terminals or environment variables!

### 📥 [Download the latest HaydeeOutfitGenerator.exe here](https://github.com/thegamerbay/haydee-ai-outfit-generator-gui/releases)

![GUI Generate Outfit Preview](assets/gui-generate-outfit.png)
![GUI Group Mods Preview](assets/gui-group-mods.png)

## 🖼️ Generated Examples

Check out what you can create! The following outfits were generated using this tool and are featured in the [Haydee: Tropical Harvest (Fruit-Themed Outfit Pack)](https://steamcommunity.com/sharedfiles/filedetails/?id=3677290023) mod on the Steam Workshop.

<p align="center">
  <a href="https://steamcommunity.com/sharedfiles/filedetails/?id=3677290023"><img src="assets/gen_preview_berry_juice.jpg" alt="Berry Juice"></a>
  <a href="https://steamcommunity.com/sharedfiles/filedetails/?id=3677290023"><img src="assets/gen_preview_citrus_spark.jpg" alt="Citrus Spark"></a>
  <a href="https://steamcommunity.com/sharedfiles/filedetails/?id=3677290023"><img src="assets/gen_preview_cyber_banana.jpg" alt="Cyber Banana"></a>
  <a href="https://steamcommunity.com/sharedfiles/filedetails/?id=3677290023"><img src="assets/gen_preview_dragon_bite.jpg" alt="Dragon Bite"></a>
  <a href="https://steamcommunity.com/sharedfiles/filedetails/?id=3677290023"><img src="assets/gen_preview_golden_pine.jpg" alt="Golden Pine"></a>
  <a href="https://steamcommunity.com/sharedfiles/filedetails/?id=3677290023"><img src="assets/gen_preview_kiwi_slice.jpg" alt="Kiwi Slice"></a>
  <a href="https://steamcommunity.com/sharedfiles/filedetails/?id=3677290023"><img src="assets/gen_preview_melon_crush.jpg" alt="Melon Crush"></a>
</p>

## ✨ Features

- **Modern Dark Interface**: Built with `CustomTkinter` for a sleek, game-themed appearance.
- **Two Unique Workflows**: Seamlessly switch between generating brand new outfits via AI and grouping your existing mods into single multi-mods.
- **No Terminal Required**: Configures all paths and handles logging automatically.
- **Asynchronous Processing**: The UI remains responsive while the outfit is being generated via AI or while mods are being grouped.
- **Standalone Executable**: Easily package the app into a single `.exe` file that any Windows user can run out-of-the-box.

## 🚀 Quick Start (For Users)

1. [Download the latest `HaydeeOutfitGenerator.exe` release](https://github.com/thegamerbay/haydee-ai-outfit-generator-gui/releases).
2. Launch the application.
3. Fill in the **Settings** panel:
   - Your **Gemini API Key**.
   - Path to your **Haydee** game installation directory.
   - Your **Author Name** (Optional, applied to all generated or grouped mods).
4. Click **Save Settings**.
5. Choose your workflow tab:
   - **✨ Generate Outfit**: Enter a unique mod name and a descriptive style prompt to create a new outfit.
   - **📦 Group Mods**: Combine multiple existing mods into one multi-mod. Enter the new multi-mod name, the source mods to group (e.g., `red, green, blue`), and the slot category (e.g., `color`).
6. Click **Start Generation** or **Group Outfits** and watch the magic happen in the built-in console window!

*(Note: The app will automatically save your settings in `AppData/Local/HaydeeOutfitGenerator/settings.json` so you don't have to enter your details every time.)*

### 🔑 Getting a Gemini API Key

1. Go to [Google AI Studio](https://aistudio.google.com/).
2. Sign in with your Google account.
3. Click the "Create API key" button.
4. If prompted, read and accept the terms of service.
5. Click on "Create API key in new project" (or use an existing project).
6. Copy the generated key. You will need to paste it into the **Settings** panel of the application.

## 🛠️ Developer Setup

If you want to contribute or build the application yourself:

### Prerequisites

- Python 3.12+
- Git

### Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/thegamerbay/haydee-ai-outfit-generator-gui.git
   cd haydee-ai-outfit-generator-gui
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the application from source:
   ```bash
   python main.py
   ```

### Building the Executable

This project includes an automated script that uses `PyInstaller` to package the app into a standalone `.exe` without a black console window.

To build:
```bash
python build.py
```

After the build completes, your application will be available in the `dist/` folder as `HaydeeOutfitGenerator.exe`.

### Running Tests

This project includes automated GUI tests written with `pytest` and `pytest-mock`.

1. Install the testing dependencies:
   ```bash
   pip install -r requirements-dev.txt
   ```

2. Run the tests:
   ```bash
   pytest tests/
   ```

### Running Linting

This project uses `flake8` to enforce code style.

1. Ensure testing dependencies are installed:
   ```bash
   pip install -r requirements-dev.txt
   ```

2. Run the linter:
   ```bash
   flake8 src tests main.py build.py
   ```

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
