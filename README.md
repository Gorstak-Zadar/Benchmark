# ⚡ Gorstak Benchmark

**Version 3.0** — Desktop app + PowerShell script.

> Benchmark your CPU, Memory, Disk, GPU, and Network. Run the **Windows desktop app** (recommended) or the **PowerShell script**.

---

## 🖥️ v3.0 Desktop App (recommended)

- **Benchmark.exe** — .NET 4.8 Windows app, dark theme, pie chart, share/export, bottleneck hint, screenshot.
- **Build:** `build.bat` (requires .NET 4.8; uses `Autorun.ico` and `app.manifest`).
- **Run:** `Benchmark.exe`. Close the window during a run to cancel gracefully.

---

## 📜 PowerShell Script (original)

```powershell
.\Benchmark.ps1
```

---

## ✨ Features

- **Zero Dependencies** — Pure PowerShell, no external tools required
- **Complete System Analysis** — Tests all major hardware components
- **Reference Scoring** — Results normalized to percentage for easy comparison
- **Color-Coded Output** — Visual performance indicators (Cyan/Green/Yellow/Red)
- **Portable** — Single script, runs on any Windows system with PowerShell

---

## 🚀 Quick Start

```powershell
.\Benchmark.ps1
```

That's it! The script will automatically test all components and display results.

---

## 📊 Benchmark Tests

### 🔥 CPU Benchmark
- **Prime Calculation** — Finds all primes up to 50,000
- **Math Operations** — 1 million sqrt and π calculations
- **Displays**: CPU model, cores, threads, and performance score

### 🧠 Memory Benchmark
- **Write Test** — Populates 10 million element array
- **Read Test** — Sequential iteration through array
- **Random Access** — 100,000 random index lookups
- **Displays**: Total RAM and throughput score

### 💾 Disk I/O Benchmark
- **Write Test** — 100 MB random data write
- **Read Test** — 100 MB file read
- **Displays**: Drive info, MB/s speeds, and I/O score

### 🎮 GPU Benchmark
- **Matrix Multiplication** — 200×200 matrix operations
- **Compute Operations** — 100,000 trigonometric calculations
- **Displays**: GPU model, VRAM, driver version, and compute score

> **Note**: This test measures CPU-based compute workloads. For actual GPU benchmarking, dedicated tools like FurMark or 3DMark are recommended.

### 🌐 Network Benchmark
- **Latency Test** — Pings Google DNS, Cloudflare, and google.com
- **Download Test** — Downloads 10 MB test file from multiple sources
- **Displays**: Average latency (ms), download speed (Mbps), and network score

---

## 📈 Sample Output

```
========================================
  POWERSHELL SYSTEM BENCHMARK SUITE
========================================

System: Microsoft Windows 11 Pro
PowerShell: 7.4.0
Date: 2026-02-21 15:30:45

========================================
  CPU BENCHMARK
========================================

[INFO] CPU: AMD Ryzen 7 5800X 8-Core Processor
[INFO] Cores: 8 | Threads: 16
[INFO] Running prime calculation test...

[RESULT] Primes Found: 5133
[RESULT] Time: 1.42 seconds
[RESULT] CPU Score: 70422.54
[RESULT] CPU Performance: 93.9%

...

========================================
  FINAL RESULTS
========================================

Component Scores:
  CPU      : 70422.54 [93.9%]
  Memory   : 4821.33 [104.8%]
  Disk I/O : 5234.67 [113.8%]
  GPU      : 892.45 [89.2%]
  Network  : 31.24 [124.9%]

========================================
  OVERALL SCORE: 16280.45 [105.3%]
========================================
```

---

## 📏 Scoring System

Results are compared against reference scores calibrated for a typical mid-range system:

| Component | Reference Score | 100% Means |
|-----------|-----------------|------------|
| CPU | 75,000 | Mid-range desktop processor |
| Memory | 4,600 | DDR4-3200 performance |
| Disk | 4,600 | SATA SSD speeds |
| GPU | 1,000 | Integrated graphics level |
| Network | 25 | 100 Mbps connection |

### Performance Tiers

| Score | Color | Rating |
|-------|-------|--------|
| ≥ 100% | 🔵 Cyan | Excellent |
| 75-99% | 🟢 Green | Good |
| 50-74% | 🟡 Yellow | Average |
| < 50% | 🔴 Red | Below Average |

---

## 🔧 Requirements

- **OS**: Windows 10/11 or Windows Server 2016+
- **PowerShell**: 5.1 or later (7.x recommended)
- **Permissions**: Standard user (admin not required)
- **Network**: Internet connection for network tests (optional)

---

## 📁 Project Structure

```
Benchmark/
├── Benchmark.ps1      # PowerShell benchmark script
├── Benchmark.exe      # Desktop app (build with build.bat)
├── Program.cs         # App entry
├── MainForm.cs        # UI, chart, share, screenshot
├── BenchmarkEngine.cs # Benchmark logic
├── BenchmarkResults.cs
├── app.manifest
├── build.bat
├── Autorun.ico
└── README.md
```

---

## ⚠️ Notes

- **Disk Test** creates a temporary 100 MB file in `%TEMP%` (auto-deleted)
- **Network Test** downloads ~10 MB from public speed test servers
- **GPU Test** is CPU-bound; for real GPU stress testing, use dedicated tools
- Results may vary based on background processes and system load
- Run multiple times and average for more consistent results

---

## 📄 License

This project is provided as-is for personal and educational use.

---

## 👤 Author

**Gorstak**

---

<p align="center">
  <sub>Built with 💻 PowerShell</sub>
</p>
