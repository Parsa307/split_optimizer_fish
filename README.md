### 📦 Split Optimizer Fish Shell Script

Optimize your `.apks`, `.apkm`, or `.zip` bundles by keeping only the APK splits **you actually need**, based on language, DPI, and architecture filters.

> ⚙️ Lightweight script written in `fish shell` to reduce APK size and improve installation speed.

---

### ✅ Example Usage:

```bash
./split_optimizer apk_bundle.apks
```

---

### 🔧 Configuration:

Before using, you **must create a config file** at:

```
~/.config/split_optimizer/split_optimizer.conf
```

Example configuration:

```
LANG=en,fa
DPI=hdpi,xhdpi
ARCH=arm64_v8a,armeabi_v7a
```

Each line accepts **comma-separated values**.

---

### 📥 Input:

Any of the following bundle formats:

* `.apks`
* `.apkm`
* `.zip`

The script unpacks the bundle, filters it according to your config, and repacks it.

---

### 📤 Output:

A new optimized file will be created in the same directory:

```
your_app_optimized.apks
```

It only includes:

* `base.apk`
* Matching `split_config.*.apk` files for the selected languages, DPIs, and architectures

---

### 💡 Features:

* ✅ Written in `fish shell`
* ✅ Configurable filters for LANG, DPI, ARCH
* ✅ Keeps only relevant APKs
* ✅ Lightweight and dependency-free (besides `unzip`, `zip`)

---

### 🛠 Requirements:

Ensure the following commands are available:

* `unzip`
* `zip`

Install with your package manager if missing:

```bash
sudo pacman -S zip unzip    # For Arch Linux
sudo apt install zip unzip  # For Debian/Ubuntu
```

---

### ❓ Help:

Run the script with `-h` or `--help` for usage and config validation:

```bash
./split_optimizer -h
```
