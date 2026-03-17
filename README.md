# 📦 Prebuilt Wheels for `cumm` and `spconv`

[![cumm-gpu release](https://img.shields.io/github/release/rathaROG/cumm-gpu.svg?logo=github&logoColor=lightgray&label=cumm-gpu)](https://github.com/rathaROG/cumm-gpu/releases)
[![spconv-gpu release](https://img.shields.io/github/release/rathaROG/spconv-gpu.svg?logo=github&logoColor=lightgray&label=spconv-gpu)](https://github.com/rathaROG/spconv-gpu/releases)
[![Platforms](https://img.shields.io/badge/platform-windows%20%7C%20linux%20%7C%20macos-gold?logo=pypi&logoColor=deepskyblue)](https://github.com/rathaROG/cumm-spconv)
[![Python Versions](https://img.shields.io/badge/python-3.11%20%7C%203.12%20%7C%203.13%20%7C%203.14-blue?logo=python&logoColor=white)](https://github.com/rathaROG/cumm-spconv)

💡 This repository provides a [PyPI simple index](https://www.python.org/dev/peps/pep-0503/) of prebuilt wheels for my custom [`cumm`](https://github.com/rathaROG/cumm-gpu) and [`spconv`](https://github.com/rathaROG/spconv-gpu).

⚡ By using this index, you can conveniently install via `pip install`, saving time on local builds and configuration.

---

## 💽 Installation

To install specific wheel(s), use the `--extra-index-url` flag with `pip install`; for example, for CUDA 13.0:

```bash
pip install cumm-cu130 spconv-cu130 --extra-index-url https://ratharog.github.io/cumm-spconv/
```

And for CPU-only variants:

```bash
pip install cumm spconv --extra-index-url https://ratharog.github.io/cumm-spconv/
```

## 🌟 Recommended version pairings

To avoid compatibility issues, always use the recommended version pairs of `cumm` and `spconv` as below:

| `cumm` / `cumm-cuxxx` | `spconv` / `spconv-cuxxx` | Supported CUDA Version(s) |
|-----------------------|---------------------------|---------------------------|
| `0.8.5` (coming)      | `2.3.11` (coming)         | 12.8, 13.0                |
| `0.8.4` (latest)      | `2.3.10` (latest)         | 12.8, 13.0                |
| `0.8.3`               | `2.3.9`                   | 12.8                      |

- If you install without specifying versions, the versions you downloaded may **not** match the highest recommended pair. This often means a new `spconv` [release](https://github.com/rathaROG/spconv-gpu/releases) is coming soon, and `cumm` [release](https://github.com/rathaROG/cumm-gpu/releases) may already be ahead.
- The pairing table is updated as new versions arrive; always check here before upgrading either package to avoid incompatibility.
- For production or reproducible installs, **explicitly use the recommended version pairs**:  

  ```bash
  pip install cumm-cu130==0.8.4 spconv-cu130==2.3.10 --extra-index-url https://ratharog.github.io/cumm-spconv/
  ```

  ```bash
  pip install cumm-cu128==0.8.3 spconv-cu128==2.3.9 --extra-index-url https://ratharog.github.io/cumm-spconv/
  ```

## 🔭 Build scope

| Wheels | Linux | Windows | macOS |
|-|-|-|-|
| [`cumm`](https://ratharog.github.io/cumm-spconv/cumm/) | ✅ | ✅ | ✅ |
| [`spconv`](https://ratharog.github.io/cumm-spconv/spconv/) | ✅ | ❌ | ❌ |
| [`cumm-cu128`](https://ratharog.github.io/cumm-spconv/cumm-cu128/) | ✅ | ✅ | ❌ |
| [`spconv-cu128`](https://ratharog.github.io/cumm-spconv/spconv-cu128/) | ✅ | ✅ | ❌ |
| [`cumm-cu130`](https://ratharog.github.io/cumm-spconv/cumm-cu130/) | ✅ | ✅ | ❌ |
| [`spconv-cu130`](https://ratharog.github.io/cumm-spconv/spconv-cu130/) | ✅ | ✅ | ❌ |

<sup> * Only for Python **3.11 - 3.14**</sup><br>
<sup> * No ARM (aarch64) support for ***Linux***</sup><br>
<sup> * No ARM (ARM64) support for ***Windows***</sup><br>

## 📝 License

[![LICENSE](https://img.shields.io/badge/LICENSE-Apache_2.0-blue)](LICENSE)
