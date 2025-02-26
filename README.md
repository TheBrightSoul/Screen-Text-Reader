# 📸 Text Extractor for Linux 🚀

A **PowerToys Text Extractor** alternative for **Linux**, designed for **Hyprland (Arch Linux)**. Capture a screen region, extract text using **Tesseract OCR**, and copy it to your clipboard—all in one go! No more saving images just to extract text. 🎉

---

## ✨ Features

✅ **Inspired by PowerToys** – Bring Windows-like text extraction to Linux 🐧  
✅ **One-Click Workflow** – Capture, extract, and copy text instantly 📜✨  
✅ **Clipboard Integration** – Automatically copies text to your clipboard 🔗  
✅ **Temporary Files** – Screenshots are auto-deleted for a clean workspace 🧹  
✅ **Lightweight & Fast** – Minimal dependencies, maximum efficiency ⚡  

---

## 🚀 Installation

### 1️⃣ Install Dependencies
Ensure these packages are installed:
```bash
sudo pacman -S --needed tesseract tesseract-data-eng grim slurp wl-clipboard
```

### 2️⃣ Clone the Repo
```bash
git clone https://github.com/TheBrightSoul/Screen-Text-Reader
cd Screen-Text-Reader
```

### 3️⃣ Make the Script Executable
```bash
chmod +x ocr-screenshot.sh
```

### 4️⃣ (Optional) Move to `/usr/local/bin/` for Global Access
```bash
sudo mv ocr-screenshot.sh /usr/local/bin/ocr-screenshot
```

---

## 🎯 Usage

Run the script:
```bash
./ocr-screenshot.sh
```
Or, if moved to `/usr/local/bin/`:
```bash
ocr-screenshot
```
Select a screen region, and the extracted text will be copied to your clipboard. 🎉

---

## 🛠️ How It Works
1️⃣ **Capture**: Uses `grim` and `slurp` to select and capture a screen region. 🖼️  
2️⃣ **Extract**: Runs `tesseract` OCR to extract text from the screenshot. 🔎  
3️⃣ **Copy**: Sends the extracted text to your clipboard using `wl-copy`. 📋  
4️⃣ **Cleanup**: Deletes the temporary screenshot automatically. 🧹  

---

## ⚙️ Hyprland Keybind Setup

Add this to your Hyprland configuration file (`~/.config/hypr/hyprland.conf`) to set a keybind:

```bash
bind = SUPER SHIFT, T, exec, /path/to/ocr-screenshot.sh
```
Replace `/path/to/ocr-screenshot.sh` with the actual path to the script. For example:
- If you moved it to `/usr/local/bin/`, use:
  ```bash
  bind = SUPER SHIFT, T, exec, ocr-screenshot
  ```
- If it's in your home directory, use:
  ```bash
  bind = SUPER SHIFT, T, exec, ~/Screen-Text-Reader/ocr-screenshot.sh
  ```

Now, press `SUPER + SHIFT + T` to trigger the text extraction tool! 🎮

---

## 💡 Tips
- **Change OCR Language**: Modify the script to use a different Tesseract language pack (e.g., `tesseract-data-fra` for French).  
- **Debugging**: Temporary files are stored in `/tmp/` if you need to inspect them.  
