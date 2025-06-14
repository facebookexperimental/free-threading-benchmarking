# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
- [Most recent  pystats on main (8fdbbf8)](results/bm-20250607-3.15.0a0-8fdbbf8/bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8-pystats.md)
- [Most recent PYTHON_UOPS pystats on main (8fdbbf8)](results/bm-20250607-3.15.0a0-8fdbbf8-PYTHON_UOPS/bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8-pystats.md)

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-06-13](results/bm-20250613-3.15.0a0-56eabea-NOGIL) | python/56eabea056ae1da49b55 | 56eabea (NOGIL) | 1.016x ↑<br>[📄](results/bm-20250613-3.15.0a0-56eabea-NOGIL/bm-20250613-vultr-x86_64-python-56eabea056ae1da49b55-3.15.0a0-56eabea-vs-3.12.6.md)[📈](results/bm-20250613-3.15.0a0-56eabea-NOGIL/bm-20250613-vultr-x86_64-python-56eabea056ae1da49b55-3.15.0a0-56eabea-vs-3.12.6.svg) | 1.020x ↓<br>[📄](results/bm-20250613-3.15.0a0-56eabea-NOGIL/bm-20250613-vultr-x86_64-python-56eabea056ae1da49b55-3.15.0a0-56eabea-vs-3.13.0rc2.md)[📈](results/bm-20250613-3.15.0a0-56eabea-NOGIL/bm-20250613-vultr-x86_64-python-56eabea056ae1da49b55-3.15.0a0-56eabea-vs-3.13.0rc2.svg) | 1.092x ↓<br>[📄](results/bm-20250613-3.15.0a0-56eabea-NOGIL/bm-20250613-vultr-x86_64-python-56eabea056ae1da49b55-3.15.0a0-56eabea-vs-base.md)[📈](results/bm-20250613-3.15.0a0-56eabea-NOGIL/bm-20250613-vultr-x86_64-python-56eabea056ae1da49b55-3.15.0a0-56eabea-vs-base.svg)[🧠](results/bm-20250613-3.15.0a0-56eabea-NOGIL/bm-20250613-vultr-x86_64-python-56eabea056ae1da49b55-3.15.0a0-56eabea-vs-base-mem.svg) |
| [2025-06-13](results/bm-20250613-3.15.0a0-56eabea) | python/56eabea056ae1da49b55 | 56eabea | 1.112x ↑<br>[📄](results/bm-20250613-3.15.0a0-56eabea/bm-20250613-vultr-x86_64-python-56eabea056ae1da49b55-3.15.0a0-56eabea-vs-3.12.6.md)[📈](results/bm-20250613-3.15.0a0-56eabea/bm-20250613-vultr-x86_64-python-56eabea056ae1da49b55-3.15.0a0-56eabea-vs-3.12.6.svg) | 1.074x ↑<br>[📄](results/bm-20250613-3.15.0a0-56eabea/bm-20250613-vultr-x86_64-python-56eabea056ae1da49b55-3.15.0a0-56eabea-vs-3.13.0rc2.md)[📈](results/bm-20250613-3.15.0a0-56eabea/bm-20250613-vultr-x86_64-python-56eabea056ae1da49b55-3.15.0a0-56eabea-vs-3.13.0rc2.svg) |  |
| [2025-06-12](results/bm-20250612-3.15.0a0-3978e35-NOGIL) | nascheme/gh_133136_qsbr_defer | 3978e35 (NOGIL) | 1.015x ↑<br>[📄](results/bm-20250612-3.15.0a0-3978e35-NOGIL/bm-20250612-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-3978e35-vs-3.12.6.md)[📈](results/bm-20250612-3.15.0a0-3978e35-NOGIL/bm-20250612-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-3978e35-vs-3.12.6.svg) | 1.020x ↓<br>[📄](results/bm-20250612-3.15.0a0-3978e35-NOGIL/bm-20250612-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-3978e35-vs-3.13.0rc2.md)[📈](results/bm-20250612-3.15.0a0-3978e35-NOGIL/bm-20250612-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-3978e35-vs-3.13.0rc2.svg) | 1.000x ↓<br>[📄](results/bm-20250612-3.15.0a0-3978e35-NOGIL/bm-20250612-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-3978e35-vs-base.md)[📈](results/bm-20250612-3.15.0a0-3978e35-NOGIL/bm-20250612-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-3978e35-vs-base.svg)[🧠](results/bm-20250612-3.15.0a0-3978e35-NOGIL/bm-20250612-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-3978e35-vs-base-mem.svg) |
| [2025-06-12](results/bm-20250612-3.15.0a0-2b0c684-NOGIL) | python/2b0c684e0759dc3fec0e | 2b0c684 (NOGIL) | 1.015x ↑<br>[📄](results/bm-20250612-3.15.0a0-2b0c684-NOGIL/bm-20250612-vultr-x86_64-python-2b0c684e0759dc3fec0e-3.15.0a0-2b0c684-vs-3.12.6.md)[📈](results/bm-20250612-3.15.0a0-2b0c684-NOGIL/bm-20250612-vultr-x86_64-python-2b0c684e0759dc3fec0e-3.15.0a0-2b0c684-vs-3.12.6.svg) | 1.020x ↓<br>[📄](results/bm-20250612-3.15.0a0-2b0c684-NOGIL/bm-20250612-vultr-x86_64-python-2b0c684e0759dc3fec0e-3.15.0a0-2b0c684-vs-3.13.0rc2.md)[📈](results/bm-20250612-3.15.0a0-2b0c684-NOGIL/bm-20250612-vultr-x86_64-python-2b0c684e0759dc3fec0e-3.15.0a0-2b0c684-vs-3.13.0rc2.svg) | 1.089x ↓<br>[📄](results/bm-20250612-3.15.0a0-2b0c684-NOGIL/bm-20250612-vultr-x86_64-python-2b0c684e0759dc3fec0e-3.15.0a0-2b0c684-vs-base.md)[📈](results/bm-20250612-3.15.0a0-2b0c684-NOGIL/bm-20250612-vultr-x86_64-python-2b0c684e0759dc3fec0e-3.15.0a0-2b0c684-vs-base.svg)[🧠](results/bm-20250612-3.15.0a0-2b0c684-NOGIL/bm-20250612-vultr-x86_64-python-2b0c684e0759dc3fec0e-3.15.0a0-2b0c684-vs-base-mem.svg) |
| [2025-06-12](results/bm-20250612-3.15.0a0-2b0c684) | python/2b0c684e0759dc3fec0e | 2b0c684 | 1.107x ↑<br>[📄](results/bm-20250612-3.15.0a0-2b0c684/bm-20250612-vultr-x86_64-python-2b0c684e0759dc3fec0e-3.15.0a0-2b0c684-vs-3.12.6.md)[📈](results/bm-20250612-3.15.0a0-2b0c684/bm-20250612-vultr-x86_64-python-2b0c684e0759dc3fec0e-3.15.0a0-2b0c684-vs-3.12.6.svg) | 1.070x ↑<br>[📄](results/bm-20250612-3.15.0a0-2b0c684/bm-20250612-vultr-x86_64-python-2b0c684e0759dc3fec0e-3.15.0a0-2b0c684-vs-3.13.0rc2.md)[📈](results/bm-20250612-3.15.0a0-2b0c684/bm-20250612-vultr-x86_64-python-2b0c684e0759dc3fec0e-3.15.0a0-2b0c684-vs-3.13.0rc2.svg) |  |
| [2025-06-11](results/bm-20250611-3.15.0a0-6214373-NOGIL) | python/62143736b623fd0bcf99 | 6214373 (NOGIL) | 1.012x ↑<br>[📄](results/bm-20250611-3.15.0a0-6214373-NOGIL/bm-20250611-vultr-x86_64-python-62143736b623fd0bcf99-3.15.0a0-6214373-vs-3.12.6.md)[📈](results/bm-20250611-3.15.0a0-6214373-NOGIL/bm-20250611-vultr-x86_64-python-62143736b623fd0bcf99-3.15.0a0-6214373-vs-3.12.6.svg) | 1.023x ↓<br>[📄](results/bm-20250611-3.15.0a0-6214373-NOGIL/bm-20250611-vultr-x86_64-python-62143736b623fd0bcf99-3.15.0a0-6214373-vs-3.13.0rc2.md)[📈](results/bm-20250611-3.15.0a0-6214373-NOGIL/bm-20250611-vultr-x86_64-python-62143736b623fd0bcf99-3.15.0a0-6214373-vs-3.13.0rc2.svg) | 1.087x ↓<br>[📄](results/bm-20250611-3.15.0a0-6214373-NOGIL/bm-20250611-vultr-x86_64-python-62143736b623fd0bcf99-3.15.0a0-6214373-vs-base.md)[📈](results/bm-20250611-3.15.0a0-6214373-NOGIL/bm-20250611-vultr-x86_64-python-62143736b623fd0bcf99-3.15.0a0-6214373-vs-base.svg)[🧠](results/bm-20250611-3.15.0a0-6214373-NOGIL/bm-20250611-vultr-x86_64-python-62143736b623fd0bcf99-3.15.0a0-6214373-vs-base-mem.svg) |
| [2025-06-11](results/bm-20250611-3.15.0a0-6214373) | python/62143736b623fd0bcf99 | 6214373 | 1.102x ↑<br>[📄](results/bm-20250611-3.15.0a0-6214373/bm-20250611-vultr-x86_64-python-62143736b623fd0bcf99-3.15.0a0-6214373-vs-3.12.6.md)[📈](results/bm-20250611-3.15.0a0-6214373/bm-20250611-vultr-x86_64-python-62143736b623fd0bcf99-3.15.0a0-6214373-vs-3.12.6.svg) | 1.064x ↑<br>[📄](results/bm-20250611-3.15.0a0-6214373/bm-20250611-vultr-x86_64-python-62143736b623fd0bcf99-3.15.0a0-6214373-vs-3.13.0rc2.md)[📈](results/bm-20250611-3.15.0a0-6214373/bm-20250611-vultr-x86_64-python-62143736b623fd0bcf99-3.15.0a0-6214373-vs-3.13.0rc2.svg) |  |
| [2025-06-10](results/bm-20250610-3.15.0a0-0f866cb-NOGIL) | python/0f866cbfefd797b4dae2 | 0f866cb (NOGIL) | 1.017x ↑<br>[📄](results/bm-20250610-3.15.0a0-0f866cb-NOGIL/bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb-vs-3.12.6.md)[📈](results/bm-20250610-3.15.0a0-0f866cb-NOGIL/bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb-vs-3.12.6.svg) | 1.018x ↓<br>[📄](results/bm-20250610-3.15.0a0-0f866cb-NOGIL/bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb-vs-3.13.0rc2.md)[📈](results/bm-20250610-3.15.0a0-0f866cb-NOGIL/bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb-vs-3.13.0rc2.svg) | 1.088x ↓<br>[📄](results/bm-20250610-3.15.0a0-0f866cb-NOGIL/bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb-vs-base.md)[📈](results/bm-20250610-3.15.0a0-0f866cb-NOGIL/bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb-vs-base.svg)[🧠](results/bm-20250610-3.15.0a0-0f866cb-NOGIL/bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb-vs-base-mem.svg) |
| [2025-06-10](results/bm-20250610-3.15.0a0-0f866cb) | python/0f866cbfefd797b4dae2 | 0f866cb | 1.108x ↑<br>[📄](results/bm-20250610-3.15.0a0-0f866cb/bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb-vs-3.12.6.md)[📈](results/bm-20250610-3.15.0a0-0f866cb/bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb-vs-3.12.6.svg) | 1.071x ↑<br>[📄](results/bm-20250610-3.15.0a0-0f866cb/bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb-vs-3.13.0rc2.md)[📈](results/bm-20250610-3.15.0a0-0f866cb/bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb-vs-3.13.0rc2.svg) |  |

## darwin arm64 (macm4pro)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-06-13](results/bm-20250613-3.15.0a0-56eabea-NOGIL) | python/56eabea056ae1da49b55 | 56eabea (NOGIL) | 1.082x ↑<br>[📄](results/bm-20250613-3.15.0a0-56eabea-NOGIL/bm-20250613-macm4pro-arm64-python-56eabea056ae1da49b55-3.15.0a0-56eabea-vs-3.12.6.md)[📈](results/bm-20250613-3.15.0a0-56eabea-NOGIL/bm-20250613-macm4pro-arm64-python-56eabea056ae1da49b55-3.15.0a0-56eabea-vs-3.12.6.svg) | 1.004x ↑<br>[📄](results/bm-20250613-3.15.0a0-56eabea-NOGIL/bm-20250613-macm4pro-arm64-python-56eabea056ae1da49b55-3.15.0a0-56eabea-vs-3.13.0rc2.md)[📈](results/bm-20250613-3.15.0a0-56eabea-NOGIL/bm-20250613-macm4pro-arm64-python-56eabea056ae1da49b55-3.15.0a0-56eabea-vs-3.13.0rc2.svg) | 1.019x ↓<br>[📄](results/bm-20250613-3.15.0a0-56eabea-NOGIL/bm-20250613-macm4pro-arm64-python-56eabea056ae1da49b55-3.15.0a0-56eabea-vs-base.md)[📈](results/bm-20250613-3.15.0a0-56eabea-NOGIL/bm-20250613-macm4pro-arm64-python-56eabea056ae1da49b55-3.15.0a0-56eabea-vs-base.svg)[🧠](results/bm-20250613-3.15.0a0-56eabea-NOGIL/bm-20250613-macm4pro-arm64-python-56eabea056ae1da49b55-3.15.0a0-56eabea-vs-base-mem.svg) |
| [2025-06-13](results/bm-20250613-3.15.0a0-56eabea) | python/56eabea056ae1da49b55 | 56eabea | 1.102x ↑<br>[📄](results/bm-20250613-3.15.0a0-56eabea/bm-20250613-macm4pro-arm64-python-56eabea056ae1da49b55-3.15.0a0-56eabea-vs-3.12.6.md)[📈](results/bm-20250613-3.15.0a0-56eabea/bm-20250613-macm4pro-arm64-python-56eabea056ae1da49b55-3.15.0a0-56eabea-vs-3.12.6.svg) | 1.022x ↑<br>[📄](results/bm-20250613-3.15.0a0-56eabea/bm-20250613-macm4pro-arm64-python-56eabea056ae1da49b55-3.15.0a0-56eabea-vs-3.13.0rc2.md)[📈](results/bm-20250613-3.15.0a0-56eabea/bm-20250613-macm4pro-arm64-python-56eabea056ae1da49b55-3.15.0a0-56eabea-vs-3.13.0rc2.svg) |  |
| [2025-06-12](results/bm-20250612-3.15.0a0-2b0c684-NOGIL) | python/2b0c684e0759dc3fec0e | 2b0c684 (NOGIL) | 1.091x ↑<br>[📄](results/bm-20250612-3.15.0a0-2b0c684-NOGIL/bm-20250612-macm4pro-arm64-python-2b0c684e0759dc3fec0e-3.15.0a0-2b0c684-vs-3.12.6.md)[📈](results/bm-20250612-3.15.0a0-2b0c684-NOGIL/bm-20250612-macm4pro-arm64-python-2b0c684e0759dc3fec0e-3.15.0a0-2b0c684-vs-3.12.6.svg) | 1.011x ↑<br>[📄](results/bm-20250612-3.15.0a0-2b0c684-NOGIL/bm-20250612-macm4pro-arm64-python-2b0c684e0759dc3fec0e-3.15.0a0-2b0c684-vs-3.13.0rc2.md)[📈](results/bm-20250612-3.15.0a0-2b0c684-NOGIL/bm-20250612-macm4pro-arm64-python-2b0c684e0759dc3fec0e-3.15.0a0-2b0c684-vs-3.13.0rc2.svg) | 1.020x ↓<br>[📄](results/bm-20250612-3.15.0a0-2b0c684-NOGIL/bm-20250612-macm4pro-arm64-python-2b0c684e0759dc3fec0e-3.15.0a0-2b0c684-vs-base.md)[📈](results/bm-20250612-3.15.0a0-2b0c684-NOGIL/bm-20250612-macm4pro-arm64-python-2b0c684e0759dc3fec0e-3.15.0a0-2b0c684-vs-base.svg)[🧠](results/bm-20250612-3.15.0a0-2b0c684-NOGIL/bm-20250612-macm4pro-arm64-python-2b0c684e0759dc3fec0e-3.15.0a0-2b0c684-vs-base-mem.svg) |
| [2025-06-12](results/bm-20250612-3.15.0a0-2b0c684) | python/2b0c684e0759dc3fec0e | 2b0c684 | 1.110x ↑<br>[📄](results/bm-20250612-3.15.0a0-2b0c684/bm-20250612-macm4pro-arm64-python-2b0c684e0759dc3fec0e-3.15.0a0-2b0c684-vs-3.12.6.md)[📈](results/bm-20250612-3.15.0a0-2b0c684/bm-20250612-macm4pro-arm64-python-2b0c684e0759dc3fec0e-3.15.0a0-2b0c684-vs-3.12.6.svg) | 1.030x ↑<br>[📄](results/bm-20250612-3.15.0a0-2b0c684/bm-20250612-macm4pro-arm64-python-2b0c684e0759dc3fec0e-3.15.0a0-2b0c684-vs-3.13.0rc2.md)[📈](results/bm-20250612-3.15.0a0-2b0c684/bm-20250612-macm4pro-arm64-python-2b0c684e0759dc3fec0e-3.15.0a0-2b0c684-vs-3.13.0rc2.svg) |  |
| [2025-06-11](results/bm-20250611-3.15.0a0-6214373-NOGIL) | python/62143736b623fd0bcf99 | 6214373 (NOGIL) | 1.090x ↑<br>[📄](results/bm-20250611-3.15.0a0-6214373-NOGIL/bm-20250611-macm4pro-arm64-python-62143736b623fd0bcf99-3.15.0a0-6214373-vs-3.12.6.md)[📈](results/bm-20250611-3.15.0a0-6214373-NOGIL/bm-20250611-macm4pro-arm64-python-62143736b623fd0bcf99-3.15.0a0-6214373-vs-3.12.6.svg) | 1.010x ↑<br>[📄](results/bm-20250611-3.15.0a0-6214373-NOGIL/bm-20250611-macm4pro-arm64-python-62143736b623fd0bcf99-3.15.0a0-6214373-vs-3.13.0rc2.md)[📈](results/bm-20250611-3.15.0a0-6214373-NOGIL/bm-20250611-macm4pro-arm64-python-62143736b623fd0bcf99-3.15.0a0-6214373-vs-3.13.0rc2.svg) | 1.025x ↓<br>[📄](results/bm-20250611-3.15.0a0-6214373-NOGIL/bm-20250611-macm4pro-arm64-python-62143736b623fd0bcf99-3.15.0a0-6214373-vs-base.md)[📈](results/bm-20250611-3.15.0a0-6214373-NOGIL/bm-20250611-macm4pro-arm64-python-62143736b623fd0bcf99-3.15.0a0-6214373-vs-base.svg)[🧠](results/bm-20250611-3.15.0a0-6214373-NOGIL/bm-20250611-macm4pro-arm64-python-62143736b623fd0bcf99-3.15.0a0-6214373-vs-base-mem.svg) |
| [2025-06-11](results/bm-20250611-3.15.0a0-6214373) | python/62143736b623fd0bcf99 | 6214373 | 1.115x ↑<br>[📄](results/bm-20250611-3.15.0a0-6214373/bm-20250611-macm4pro-arm64-python-62143736b623fd0bcf99-3.15.0a0-6214373-vs-3.12.6.md)[📈](results/bm-20250611-3.15.0a0-6214373/bm-20250611-macm4pro-arm64-python-62143736b623fd0bcf99-3.15.0a0-6214373-vs-3.12.6.svg) | 1.034x ↑<br>[📄](results/bm-20250611-3.15.0a0-6214373/bm-20250611-macm4pro-arm64-python-62143736b623fd0bcf99-3.15.0a0-6214373-vs-3.13.0rc2.md)[📈](results/bm-20250611-3.15.0a0-6214373/bm-20250611-macm4pro-arm64-python-62143736b623fd0bcf99-3.15.0a0-6214373-vs-3.13.0rc2.svg) |  |
| [2025-06-10](results/bm-20250610-3.15.0a0-0f866cb-NOGIL) | python/0f866cbfefd797b4dae2 | 0f866cb (NOGIL) | 1.100x ↑<br>[📄](results/bm-20250610-3.15.0a0-0f866cb-NOGIL/bm-20250610-macm4pro-arm64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb-vs-3.12.6.md)[📈](results/bm-20250610-3.15.0a0-0f866cb-NOGIL/bm-20250610-macm4pro-arm64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb-vs-3.12.6.svg) | 1.020x ↑<br>[📄](results/bm-20250610-3.15.0a0-0f866cb-NOGIL/bm-20250610-macm4pro-arm64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb-vs-3.13.0rc2.md)[📈](results/bm-20250610-3.15.0a0-0f866cb-NOGIL/bm-20250610-macm4pro-arm64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb-vs-3.13.0rc2.svg) | 1.020x ↓<br>[📄](results/bm-20250610-3.15.0a0-0f866cb-NOGIL/bm-20250610-macm4pro-arm64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb-vs-base.md)[📈](results/bm-20250610-3.15.0a0-0f866cb-NOGIL/bm-20250610-macm4pro-arm64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb-vs-base.svg)[🧠](results/bm-20250610-3.15.0a0-0f866cb-NOGIL/bm-20250610-macm4pro-arm64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb-vs-base-mem.svg) |
| [2025-06-10](results/bm-20250610-3.15.0a0-0f866cb) | python/0f866cbfefd797b4dae2 | 0f866cb | 1.120x ↑<br>[📄](results/bm-20250610-3.15.0a0-0f866cb/bm-20250610-macm4pro-arm64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb-vs-3.12.6.md)[📈](results/bm-20250610-3.15.0a0-0f866cb/bm-20250610-macm4pro-arm64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb-vs-3.12.6.svg) | 1.039x ↑<br>[📄](results/bm-20250610-3.15.0a0-0f866cb/bm-20250610-macm4pro-arm64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb-vs-3.13.0rc2.md)[📈](results/bm-20250610-3.15.0a0-0f866cb/bm-20250610-macm4pro-arm64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb-vs-3.13.0rc2.svg) |  |


<!-- END table -->

`*` indicates that the exact same versions of pyperformance was not used.

![Longitudinal speed improvement](/longitudinal.svg)

Improvement of the geometric mean of key merged benchmarks, computed with `pyperf compare`.
The results have a resolution of 0.01 (1%).

![Configuration speed improvement](/configs.svg)

## Documentation

### Running benchmarks from the GitHub web UI

Visit the 🔒 [benchmark action](../../actions/workflows/benchmark.yml) and click the "Run Workflow" button.

The available parameters are:

- `fork`: The fork of CPython to benchmark.
  If benchmarking a pull request, this would normally be your GitHub username.
- `ref`: The branch, tag or commit SHA to benchmark.
  If a SHA, it must be the full SHA, since finding it by a prefix is not supported.
- `machine`: The machine to run on.
  One of `linux-amd64` (default), `windows-amd64`, `darwin-arm64` or `all`.
- `benchmark_base`: If checked, the base of the selected branch will also be benchmarked.
  The base is determined by running `git merge-base upstream/main $ref`.
- `pystats`: If checked, collect the pystats from running the benchmarks.

To watch the progress of the benchmark, select it from the 🔒 [benchmark action page](../../actions/workflows/benchmark.yml).
It may be canceled from there as well.
To show only your benchmark workflows, select your GitHub ID from the "Actor" dropdown.

When the benchmarking is complete, the results are published to this repository and will appear in the [complete table](RESULTS.md).
Each set of benchmarks will have:

- The raw `.json` results from pyperformance.
- Comparisons against important reference releases, as well as the merge base of the branch if `benchmark_base` was selected. These include
  - A markdown table produced by `pyperf compare_to`.
  - A set of "violin" plots showing the distribution of results for each benchmark.

The most convenient way to get results locally is to clone this repo and `git pull` from it.

### Running benchmarks from the GitHub CLI

To automate benchmarking runs, it may be more convenient to use the [GitHub CLI](https://cli.github.com/).
Once you have `gh` installed and configured, you can run benchmarks by cloning this repository and then from inside it:

```bash session
gh workflow run benchmark.yml -f fork=me -f ref=my_branch
```

Any of the parameters described above are available at the commandline using the `-f key=value` syntax.

### Collecting Linux perf profiling data

To collect Linux perf sampling profile data for a benchmarking run, run the `_benchmark` action and check the `perf` checkbox.
Follow this by a run of the `_generate` action to regenerate the plots.

## License

This repo is licensed under the BSD 3-Clause License, as found in the LICENSE file.
