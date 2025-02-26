
# 📸 Text Extractor for Linux 🚀

A **PowerToys Text Extractor** alternative for **Linux**, specially designed for **Hyprland (Arch Linux)**. This script lets you take a screenshot of a selected region, extract text from it using **Tesseract OCR**, copy the text directly to your clipboard, and automatically delete the temporary screenshot. No more manually saving images just to extract text! 🎉

---

## ✨ Features

✅ **Inspired by PowerToys** – Bringing that sweet Windows feature to Linux 🐧  
✅ **Capture & Extract in One Go** – Select a region, extract text, and copy it instantly 📜✨  
✅ **Clipboard Magic** – No need to manually copy-paste; it's done for you 🔗  
✅ **Temporary Screenshots** – Keeps your storage clean by auto-deleting screenshots 🧹  
✅ **Lightweight & Fast** – Just a simple Bash script, no bloated dependencies ⚡  

---

## 🚀 Installation

### 1️⃣ Install Dependencies
Make sure you have the following installed:

```bash
pman -S tesseract tesseract-data-eng swappy grim slurp wl-clipboard
```

### 2️⃣ Clone This Repo
```bash
git clone [For later]
cd Text-Extractor-Linux
```

### 3️⃣ Make It Executable
```bash
chmod +x text-extractor.sh
```

### 4️⃣ Move It to `/usr/local/bin/` (Optional, for global use)
```bash
sudo mv text-extractor.sh /usr/local/bin/text-extractor
```

---

## 🎯 Usage

### 🖼️ Take a Screenshot & Extract Text
Simply run:
```bash
./text-extractor.sh
```
Or, if you moved it to `/usr/local/bin/`:
```bash
text-extractor
```
Then, select the region you want text extracted from – and boom! The text is copied to your clipboard. 🎉

---

## 🛠️ How It Works
1️⃣ Uses **SGrim with Slurp* to capture a selected region of the screen. 🖼️  
2️⃣ Saves the screenshot temporarily. 🗂️  
3️⃣ Runs **Tesseract OCR** to extract text from the image. 🔎  
4️⃣ Copies the extracted text to the clipboard. 📋  
5️⃣ Deletes the temporary screenshot to keep things clean..

