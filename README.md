# 📦 Prebuilt Wheels for `cumm` and `spconv`

[![cumm-gpu release](https://img.shields.io/github/release/rathaROG/cumm-gpu.svg?logo=github&logoColor=lightgray&label=cumm-gpu)](https://github.com/rathaROG/cumm-gpu/releases)
[![spconv-gpu release](https://img.shields.io/github/release/rathaROG/spconv-gpu.svg?logo=github&logoColor=lightgray&label=spconv-gpu)](https://github.com/rathaROG/spconv-gpu/releases)
[![Platforms](https://img.shields.io/badge/platform-windows%20%7C%20linux%20%7C%20macos-gold?logo=pypi&logoColor=deepskyblue)](https://github.com/rathaROG/cumm-spconv)
[![Python Versions](https://img.shields.io/badge/python-3.11%20%7C%203.12%20%7C%203.13%20%7C%203.14-blue?logo=python&logoColor=white)](https://github.com/rathaROG/cumm-spconv)

💡 This repository provides a [PyPI simple index](https://www.python.org/dev/peps/pep-0503/) of prebuilt wheels for my custom [`cumm`](https://github.com/rathaROG/cumm-gpu) and [`spconv`](https://github.com/rathaROG/spconv-gpu).

⚡ By using this index, you can conveniently install via `pip install`, saving time on local builds and configuration.

---

> 🆕 Highlight in `cumm` [v0.9.0](https://github.com/rathaROG/cumm-gpu/releases/tag/v0.9.0) and `spconv` [v2.4.0](https://github.com/rathaROG/spconv-gpu/releases/tag/v2.4.0):
> 
> - Updated logic to support more arch in default build
> - Added [`nvidia-arch`](https://github.com/rathaROG/nvidia-arch) for proper NVIDIA GPU architecture handling
> - Arches for CUDA 13.0 builds: 
>   `'7.5;8.0;8.6;8.7;8.8;8.9;9.0;10.0;10.3;11.0;12.0;12.1+PTX'`
> - Arches for CUDA 12.8 builds: 
>   `'6.0;6.1;6.2;7.0;7.2;7.5;8.0;8.6;8.7;8.9;9.0;10.0;10.1;12.0+PTX'`

---

## 💽 Installation

To install specific wheel(s), use the `--index-url` or `-i` with `pip install` to ensure packages are installed exclusively from this index.

Note: `--extra-index-url` is not ideal because pip will prefer packages from PyPI if the package name and version are the same (or higher) on PyPI, which cause it to ignore the custom wheels from this index.

For CUDA 13.0:

```bash
pip install -i https://ratharog.github.io/cumm-spconv/ cumm-cu130 spconv-cu130
```

For CUDA 12.8:

```bash
pip install -i https://ratharog.github.io/cumm-spconv/ cumm-cu128 spconv-cu128
```

And for CPU-only variants:

```bash
pip install -i https://ratharog.github.io/cumm-spconv/ cumm spconv
```

## 🌟 Recommended version pairings for prebuilt wheels

The pairing table is updated as new versions arrive; always check here before upgrading either package to avoid incompatibility. Always use the recommended version pairs of `cumm` and `spconv` as below:

| Recommended Version Pairs<br>[`cumm`](https://github.com/rathaROG/cumm-gpu/releases) ⟵ [`spconv`](https://github.com/rathaROG/spconv-gpu/releases) | Available Prebuilt<br>CUDA Wheels | Supported CUDA Versions<br>(Source Build) |
|-|-|-|
| `0.9.1` (pre-release) ⟵ `2.4.1` (coming) | `cu126`, `cu128`, `cu130` | 12.6+, 13.x |
| `0.9.0` (latest) ⟵ `2.4.0` (latest) | `cu128`, `cu130` | 12.6+, 13.x |
| `0.8.5` ⟵ `2.3.11` | `cu128`, `cu130` | 12.6+, 13.x |
| `0.8.4` ⟵ `2.3.10` | `cu128`, `cu130` | 12.6+, 13.x |
| `0.8.3` ⟵ `2.3.9` | `cu128` | 12.6+ |
| `0.7.14` (pre-release) ⟵ `2.4.1` (coming) | `cu113`, `cu121` |  11.x, 12.0-12.6 |

- If you install without specifying versions, the versions you downloaded may **not** match the highest recommended pair. This often means a new `spconv` [release](https://github.com/rathaROG/spconv-gpu/releases) is coming soon, and `cumm` [release](https://github.com/rathaROG/cumm-gpu/releases) may already be ahead.

- If there is no prebuilt wheel available for a specific minor version of CUDA, you can always build from source:
  - For CUDA 12.6+, use the latest [cumm-gpu](https://github.com/rathaROG/cumm-gpu/tags) and [spconv-gpu](https://github.com/rathaROG/spconv-gpu/tags).
  - For CUDA 11.0-12.6, use [cumm-gpu@v0.7.14](https://github.com/rathaROG/cumm-gpu/releases/tag/v0.7.14) and the latest [spconv-gpu](https://github.com/rathaROG/spconv-gpu/tags).

- For production or reproducible installs, **explicitly use the recommended version pairs**:  

  ```bash
  pip install cumm-cu130==0.9.0 spconv-cu130==2.4.0 --extra-index-url https://ratharog.github.io/cumm-spconv/
  ```

  ```bash
  pip install cumm-cu128==0.9.0 spconv-cu128==2.4.0 --extra-index-url https://ratharog.github.io/cumm-spconv/
  ```

> ### **Notes**:
> - [cumm-gpu@v0.7.14](https://github.com/rathaROG/cumm-gpu/releases/tag/v0.7.14) also supports CUDA 12.6; however, the prebuilt `cumm-cu126` and `spconv-cu126` wheels are based on the latest versions.
> - Both [cumm-gpu@v0.7.14](https://github.com/rathaROG/cumm-gpu/releases/tag/v0.7.14) and [cumm-gpu@v0.9.0](https://github.com/rathaROG/cumm-gpu/releases/tag/v0.9.0) (and later) already have [`nvidia-arch`](https://github.com/rathaROG/nvidia-arch) integrated for proper NVIDIA GPU architecture handling.

## 🔭 Build scope

| Wheels | Linux | Windows | macOS | Python Versions |
|-|-|-|-|-|
| [`cumm`](https://ratharog.github.io/cumm-spconv/cumm/) | ✅ | ✅ | ✅ | 3.9-3.14 |
| [`spconv`](https://ratharog.github.io/cumm-spconv/spconv/) | ✅ | ❌ | ❌ | 3.9-3.14 |
| [`cumm-cu113`](https://ratharog.github.io/cumm-spconv/cumm-cu113/) | ✅ | ❌ | ❌ | 3.9-3.11 |
| [`spconv-cu113`](https://ratharog.github.io/cumm-spconv/spconv-cu113/) | ✅ | ❌ | ❌ | 3.9-3.11 |
| [`cumm-cu121`](https://ratharog.github.io/cumm-spconv/cumm-cu121/) | ✅ | ❌ | ❌ | 3.9-3.11 |
| [`spconv-cu121`](https://ratharog.github.io/cumm-spconv/spconv-cu121/) | ✅ | ❌ | ❌ | 3.9-3.11 |
| [`cumm-cu126`](https://ratharog.github.io/cumm-spconv/cumm-cu126/) | ✅ | ✅ | ❌ | 3.11-3.14 |
| [`spconv-cu126`](https://ratharog.github.io/cumm-spconv/spconv-cu126/) | ✅ | ✅ | ❌ | 3.11-3.14 |
| [`cumm-cu128`](https://ratharog.github.io/cumm-spconv/cumm-cu128/) | ✅ | ✅ | ❌ | 3.11-3.14 |
| [`spconv-cu128`](https://ratharog.github.io/cumm-spconv/spconv-cu128/) | ✅ | ✅ | ❌ | 3.11-3.14 |
| [`cumm-cu130`](https://ratharog.github.io/cumm-spconv/cumm-cu130/) | ✅ | ✅ | ❌ | 3.11-3.14 |
| [`spconv-cu130`](https://ratharog.github.io/cumm-spconv/spconv-cu130/) | ✅ | ✅ | ❌ | 3.11-3.14 |

<sup> * No ARM (aarch64) support for ***Linux***</sup><br>
<sup> * No ARM (ARM64) support for ***Windows***</sup><br>

## 📝 License

[![LICENSE](https://img.shields.io/badge/LICENSE-Apache_2.0-blue)](LICENSE)
