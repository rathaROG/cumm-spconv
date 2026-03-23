# 📦 Prebuilt Wheels for `cumm` and `spconv`

[![cumm-gpu release](https://img.shields.io/github/release/rathaROG/cumm-gpu.svg?logo=github&logoColor=lightgray&label=cumm-gpu)](https://github.com/rathaROG/cumm-gpu/releases)
[![spconv-gpu release](https://img.shields.io/github/release/rathaROG/spconv-gpu.svg?logo=github&logoColor=lightgray&label=spconv-gpu)](https://github.com/rathaROG/spconv-gpu/releases)
[![Platforms](https://img.shields.io/badge/platform-windows%20%7C%20linux%20%7C%20macos-gold?logo=pypi&logoColor=deepskyblue)](https://github.com/rathaROG/cumm-spconv)
[![Python Versions](https://img.shields.io/badge/python-3.11%20%7C%203.12%20%7C%203.13%20%7C%203.14-blue?logo=python&logoColor=white)](https://github.com/rathaROG/cumm-spconv)

💡 This repository provides a [PyPI simple index](https://www.python.org/dev/peps/pep-0503/) of prebuilt wheels for my custom [`cumm`](https://github.com/rathaROG/cumm-gpu) and [`spconv`](https://github.com/rathaROG/spconv-gpu).

⚡ By using this index, you can conveniently install via `pip install`, saving time on local builds and configuration.

🆕 Highlight in `cumm` [v0.9.0](https://github.com/rathaROG/cumm-gpu/releases/tag/v0.9.0) and `spconv` [v2.4.0](https://github.com/rathaROG/spconv-gpu/releases/tag/v2.4.0):

> - Added [`nvidia-arch`](https://github.com/rathaROG/nvidia-arch) for proper NVIDIA GPU architecture handling:
> 
>   - Auto detected arches for CUDA 13.0 builds: 
>     `'7.5;8.0;8.6;8.7;8.8;8.9;9.0;10.0;10.3;11.0;12.0;12.1+PTX'`
>   - Auto detected arches for CUDA 12.8 builds: 
>     `'7.5;8.0;8.6;8.7;8.9;9.0;10.0;10.1;12.0+PTX'`

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

## 🌟 Recommended version pairings for prebuilt wheels

The pairing table is updated as new versions arrive; always check here before upgrading either package to avoid incompatibility. Always use the recommended version pairs of `cumm` and `spconv` as below:

| Recommended Version Pairs<br>[`cumm`](https://github.com/rathaROG/cumm-gpu/releases) ⟵ [`spconv`](https://github.com/rathaROG/spconv-gpu/releases) | Available Prebuilt<br>CUDA Wheels | Supported CUDA Versions<br>(Source Build) |
|-|-|-|
| `0.9.0` (latest) ⟵ `2.4.0` (coming) | `cu128`, `cu130` | 12.x, 13.x |
| `0.8.5` ⟵ `2.3.11` (latest) | `cu128`, `cu130` | 12.x, 13.x |
| `0.8.4` ⟵ `2.3.10` | `cu128`, `cu130` | 12.x, 13.x |
| `0.8.3` ⟵ `2.3.9` | `cu128` | 12.x |

- If you install without specifying versions, the versions you downloaded may **not** match the highest recommended pair. This often means a new `spconv` [release](https://github.com/rathaROG/spconv-gpu/releases) is coming soon, and `cumm` [release](https://github.com/rathaROG/cumm-gpu/releases) may already be ahead.
- If there is no prebuilt wheel for a specific minor version of CUDA 12.x and 13.x, you can always build from source using the latest [cumm-gpu](https://github.com/rathaROG/cumm-gpu/tags) and [spconv-gpu](https://github.com/rathaROG/spconv-gpu/tags).
- For CUDA 11.x, you can always build from source using [cumm-gpu@v0.7.13](https://github.com/rathaROG/cumm-gpu/releases/tag/v0.7.13) and the latest [spconv-gpu](https://github.com/rathaROG/spconv-gpu/tags).
- For production or reproducible installs, **explicitly use the recommended version pairs**:  

  ```bash
  pip install cumm-cu130==0.8.5 spconv-cu130==2.3.11 --extra-index-url https://ratharog.github.io/cumm-spconv/
  ```

  ```bash
  pip install cumm-cu128==0.8.5 spconv-cu128==2.3.11 --extra-index-url https://ratharog.github.io/cumm-spconv/
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
