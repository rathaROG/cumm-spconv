# 📦 Prebuilt wheels for `cumm` and `spconv`

## 💡 What is this?

This repository provides a [PyPI simple index](https://www.python.org/dev/peps/pep-0503/) of prebuilt wheels for my custom [`cumm`](https://github.com/rathaROG/cumm-gpu) and [`spconv`](https://github.com/rathaROG/spconv-gpu) for easy installation using `pip` from GitHub Pages.

By using this index, you can conveniently install my custom wheels via pip, saving time on local builds and configuration.

## 🧪 Usage

[![Platforms](https://img.shields.io/badge/platform-windows%20%7C%20linux%20%7C%20macos-gold?logo=pypi&logoColor=deepskyblue)](https://github.com/rathaROG/cumm-spconv)
[![Python Versions](https://img.shields.io/badge/python-3.11%20%7C%203.12%20%7C%203.13%20%7C%203.14-blue?logo=python&logoColor=white)](https://github.com/rathaROG/cumm-spconv)

To install a specific wheel from this custom index, use the `--extra-index-url` flag with pip; for example, for CUDA 12.8:

```bash
pip install cumm-cu128 spconv-cu128 --extra-index-url https://ratharog.github.io/cumm-spconv/
```

And for CPU-only variants:

```bash
pip install cumm spconv --extra-index-url https://ratharog.github.io/cumm-spconv/
```

## 📇 Indexation

### 🔭 Build scope

| Wheels | Linux | Windows | macOS |
|-|-|-|-|
| [`cumm`](https://ratharog.github.io/cumm-spconv/cumm/) | ✅ | ✅ | ✅ |
| [`spconv`](https://ratharog.github.io/cumm-spconv/spconv/) | ✅ | ❌ | ❌ |
| [`cumm-cu128`](https://ratharog.github.io/cumm-spconv/cumm-cu128/) | ✅ | ✅ | ❌ |
| [`spconv-cu128`](https://ratharog.github.io/cumm-spconv/spconv-cu128/) | ✅ | ✅ | ❌ |
| [`cumm-cu130`](https://ratharog.github.io/cumm-spconv/cumm-cu130/) | ✅ | ✅ | ❌ |
| [`spconv-cu130`](https://ratharog.github.io/cumm-spconv/spconv-cu130/) | ✅ | ✅ | ❌ |

<sup> - Only for Python **3.11 - 3.14**</sup><br>
<sup> - No ARM (aarch64) support for ***Linux***</sup><br>
<sup> - No ARM (ARM64) support for ***Windows***</sup><br>

## 📝 License

[![LICENSE](https://img.shields.io/badge/LICENSE-Apache_2.0-blue)](LICENSE)
