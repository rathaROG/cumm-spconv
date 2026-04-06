# 📦 Prebuilt Wheels for `cumm` and `spconv`

[![cumm-gpu release](https://img.shields.io/github/release/rathaROG/cumm-gpu.svg?logo=github&logoColor=lightgray&label=cumm-gpu)](https://github.com/rathaROG/cumm-gpu/releases)
[![spconv-gpu release](https://img.shields.io/github/release/rathaROG/spconv-gpu.svg?logo=github&logoColor=lightgray&label=spconv-gpu)](https://github.com/rathaROG/spconv-gpu/releases)
[![Platforms](https://img.shields.io/badge/platform-windows%20%7C%20linux%20%7C%20macos-gold?logo=pypi&logoColor=deepskyblue)](https://github.com/rathaROG/cumm-spconv)
[![Python Versions](https://img.shields.io/badge/python-3.9%20%7C%203.10%20%7C%203.11%20%7C%203.12%20%7C%203.13%20%7C%203.14-blue?logo=python&logoColor=white)](https://github.com/rathaROG/cumm-spconv)

💡 This repository provides a [PyPI simple index](https://www.python.org/dev/peps/pep-0503/) of prebuilt wheels for my custom [`cumm`](https://github.com/rathaROG/cumm-gpu) and [`spconv`](https://github.com/rathaROG/spconv-gpu).

⚡ By using this index, you can conveniently install via `pip install`, saving time on local builds and configuration.

<details><summary>&nbsp; 💯 pytest passed ! </summary><br>

<img alt="Image" src="https://raw.githubusercontent.com/rathaROG/cumm-spconv/refs/heads/main/assets/pytest.jpg" />

</details>

---

> 🆕 The new `cumm` [v0.9.1](https://github.com/rathaROG/cumm-gpu/releases/tag/v0.9.1) (and [v0.7.14](https://github.com/rathaROG/cumm-gpu/releases/tag/v0.7.14)) and `spconv` [v2.4.1](https://github.com/rathaROG/spconv-gpu/releases/tag/v2.4.1) now include additional prebuilt wheels for CUDA 11.3 12.1 and 12.6 along with many fixes and enhancements.

---

## 💽 Installation

To install specific wheel(s), use the `--extra-index-url` with `pip install` to ensure packages are installed exclusively from this index; for example, for CUDA 13.0:

```bash
pip install --extra-index-url https://ratharog.github.io/cumm-spconv/ cumm-cu130 spconv-cu130
```

And for CPU-only variants:

```bash
pip install --extra-index-url https://ratharog.github.io/cumm-spconv/ cumm spconv
```

Note: `--extra-index-url` may not provide the right wheels because pip will still install packages from PyPI when the package name and version are the same (or higher) on PyPI, which cause it to ignore the custom wheels from this index. To make sure the correct wheels from this index are installed, you can use `--index-url` or `-i`; for example, for CUDA 13.0:

```bash
pip install --extra-index-url https://ratharog.github.io/cumm-spconv/ cumm-cu130 spconv-cu130
pip uninstall -y cumm-cu130 spconv-cu130
pip install -i https://ratharog.github.io/cumm-spconv/ cumm-cu130 spconv-cu130
```

## 🌟 Recommended version pairings for prebuilt wheels

The pairing table is updated as new versions arrive; always check here before upgrading either package to avoid incompatibility. Always use the recommended version pairs of `cumm` and `spconv` as below:

| Recommended Version Pairs<br>[`cumm`](https://github.com/rathaROG/cumm-gpu/releases) ⟵ [`spconv`](https://github.com/rathaROG/spconv-gpu/releases) | Available Prebuilt<br>CUDA Wheels | Supported CUDA Versions<br>(Source Build) |
|-|-|-|
| `0.9.1` (latest) ⟵ `2.4.1` (latest) | `cu126`, `cu128`, `cu130` | 12.6+, 13.x |
| `0.9.0` ⟵ `2.4.0` | `cu128`, `cu130` | 12.6+, 13.x |
| `0.8.5` ⟵ `2.3.11` | `cu128`, `cu130` | 12.6+, 13.x |
| `0.8.4` ⟵ `2.3.10` | `cu128`, `cu130` | 12.6+, 13.x |
| `0.8.3` ⟵ `2.3.9` | `cu128` | 12.6+ |
| `0.7.14` ⟵ `2.4.1` (latest) | `cu113`, `cu121` |  11.x, 12.0-12.6 |

- If you install without specifying versions, the versions you downloaded may **not** match the highest recommended pair. This often means a new `spconv` [release](https://github.com/rathaROG/spconv-gpu/releases) is coming soon, and `cumm` [release](https://github.com/rathaROG/cumm-gpu/releases) may already be ahead.

- If there is no prebuilt wheel available for a specific minor version of CUDA, you can always build from source:
  - For CUDA 12.6+, use the latest [cumm-gpu](https://github.com/rathaROG/cumm-gpu/tags) and [spconv-gpu](https://github.com/rathaROG/spconv-gpu/tags).
  - For CUDA 11.0-12.6, use [cumm-gpu@v0.7.14](https://github.com/rathaROG/cumm-gpu/releases/tag/v0.7.14) and the latest [spconv-gpu](https://github.com/rathaROG/spconv-gpu/tags).

- For production or reproducible installs, **explicitly use the recommended version pairs**:  

  ```bash
  pip install --extra-index-url https://ratharog.github.io/cumm-spconv/ cumm-cu130==0.9.1 spconv-cu130==2.4.1
  ```

  ```bash
  pip install --extra-index-url https://ratharog.github.io/cumm-spconv/ cumm-cu128==0.9.1 spconv-cu128==2.4.1
  ```

> ### **Notes**:
> - [cumm-gpu@v0.7.14](https://github.com/rathaROG/cumm-gpu/releases/tag/v0.7.14) also supports CUDA 12.6; however, the prebuilt `cumm-cu126` and `spconv-cu126` wheels are based on the latest versions of [cumm-gpu@v0.9.1](https://github.com/rathaROG/cumm-gpu/releases/tag/v0.9.1) and [spconv-gpu@v2.4.1](https://github.com/rathaROG/spconv-gpu/releases/tag/v2.4.1).

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
