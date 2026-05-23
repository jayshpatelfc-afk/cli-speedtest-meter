# cli-speedtest-meter
# ⚡ PySpeedTest

A fast, polished, and lightweight command-line internet speed test written entirely in **pure Python standard library** — no external dependencies required.

It measures:

* 📶 Ping / latency
* ⬇️ Download speed
* ⬆️ Upload speed

using Cloudflare's real speed test endpoints.

---

# ✨ Features

* ✅ Pure Python (no pip installs)
* ✅ Real download/upload testing
* ✅ Clean colorful terminal UI
* ✅ Progress status indicators
* ✅ Human-readable output
* ✅ Adjustable test sizes
* ✅ Cross-platform support
* ✅ Lightweight and fast

---

# 📸 Preview

```bash
+==========================+
|     PY SPEED TEST        |
+==========================+

Real download/upload measurement from Cloudflare test endpoints.

> Checking latency (4 samples)... done
> Testing download (50.0 MB)... done
> Testing upload (20.0 MB)... done

Results
  Ping         21.4 ms  best 18.7 ms
  Down      ########################  152.45 Mbps
  Up        ####################      84.12 Mbps
```

---

# 🚀 Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/pyspeedtest.git
cd pyspeedtest
```

No dependencies needed.

---

# ▶️ Usage

Run the script:

```bash
python speedtest.py
```

---

# ⚙️ Command Line Options

| Option           | Description                | Default |
| ---------------- | -------------------------- | ------- |
| `--download-mb`  | Download test size in MB   | `50`    |
| `--upload-mb`    | Upload test size in MB     | `20`    |
| `--ping-samples` | Number of latency checks   | `4`     |
| `--timeout`      | Network timeout in seconds | `30`    |

---

# 🧪 Examples

## Larger download test

```bash
python speedtest.py --download-mb 100
```

## More ping samples

```bash
python speedtest.py --ping-samples 10
```

## Custom upload/download

```bash
python speedtest.py --download-mb 150 --upload-mb 50
```

---

# 🛠 How It Works

The tool uses:

* `urllib.request`
* `time.perf_counter`
* Cloudflare speed test endpoints

to perform actual network transfer measurements.

### Download Test

Downloads a file from:

```text
https://speed.cloudflare.com/__down
```

### Upload Test

Uploads generated data to:

```text
https://speed.cloudflare.com/__up
```

### Ping Test

Measures response latency using lightweight requests.

---

# 📂 Project Structure

```text
pyspeedtest/
│
├── speedtest.py
├── README.md
└── LICENSE
```

---

# 🎨 Terminal Colors

The app automatically detects terminal color support and displays:

* Cyan status messages
* Green speed indicators
* Yellow ping display
* Red error messages

without breaking compatibility on unsupported terminals.

---

# ❌ Error Handling

Gracefully handles:

* Network failures
* Connection timeouts
* Keyboard interrupts (`CTRL+C`)
* Invalid responses

---

# 📋 Requirements

* Python 3.10+
* Internet connection

No third-party libraries required.

---

# 🌟 Why This Project?

Most speed test tools rely on:

* Large dependencies
* External packages
* Heavy frameworks

This project demonstrates how powerful Python’s standard library can be for real-world networking applications.

---

# 📄 License

MIT License

Feel free to use, modify, and distribute.

---

# ❤️ Contributing

Pull requests are welcome.

Ideas for future improvements:

* Live speed graph
* Multi-threaded downloads
* Server selection
* JSON output mode
* Historical logging

---

# ⭐ Support

If you like this project:

* Star the repository
* Share it with others
* Contribute improvements

---

# 👨‍💻 Author

Made with Python and caffeine ☕
