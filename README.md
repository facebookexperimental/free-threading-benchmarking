# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
- [Most recent  pystats on main (4f18916)](results/bm-20250426-3.14.0a7%2B-4f18916/bm-20250426-linux-x86_64-python-4f18916c5c28321f363e-3.14.0a7%2B-4f18916-pystats.md)
- [Most recent PYTHON_UOPS pystats on main (4f18916)](results/bm-20250426-3.14.0a7%2B-4f18916-PYTHON_UOPS/bm-20250426-linux-x86_64-python-4f18916c5c28321f363e-3.14.0a7%2B-4f18916-pystats.md)

## linux x86_64 (linux)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-04-22](results/bm-20250422-3.14.0a7%2B-b5bf8c8-NOGIL) | python/b5bf8c80a921679b2354 | b5bf8c8 (NOGIL) | 1.133x ↑<br>[📄](results/bm-20250422-3.14.0a7%2B-b5bf8c8-NOGIL/bm-20250422-linux-x86_64-python-b5bf8c80a921679b2354-3.14.0a7%2B-b5bf8c8-vs-3.12.6.md)[📈](results/bm-20250422-3.14.0a7%2B-b5bf8c8-NOGIL/bm-20250422-linux-x86_64-python-b5bf8c80a921679b2354-3.14.0a7%2B-b5bf8c8-vs-3.12.6.svg) | 1.092x ↑<br>[📄](results/bm-20250422-3.14.0a7%2B-b5bf8c8-NOGIL/bm-20250422-linux-x86_64-python-b5bf8c80a921679b2354-3.14.0a7%2B-b5bf8c8-vs-3.13.0rc2.md)[📈](results/bm-20250422-3.14.0a7%2B-b5bf8c8-NOGIL/bm-20250422-linux-x86_64-python-b5bf8c80a921679b2354-3.14.0a7%2B-b5bf8c8-vs-3.13.0rc2.svg) | 1.083x ↓<br>[📄](results/bm-20250422-3.14.0a7%2B-b5bf8c8-NOGIL/bm-20250422-linux-x86_64-python-b5bf8c80a921679b2354-3.14.0a7%2B-b5bf8c8-vs-base.md)[📈](results/bm-20250422-3.14.0a7%2B-b5bf8c8-NOGIL/bm-20250422-linux-x86_64-python-b5bf8c80a921679b2354-3.14.0a7%2B-b5bf8c8-vs-base.svg)[🧠](results/bm-20250422-3.14.0a7%2B-b5bf8c8-NOGIL/bm-20250422-linux-x86_64-python-b5bf8c80a921679b2354-3.14.0a7%2B-b5bf8c8-vs-base-mem.svg) |
| [2025-04-22](results/bm-20250422-3.14.0a7%2B-b5bf8c8) | python/b5bf8c80a921679b2354 | b5bf8c8 | 1.227x ↑<br>[📄](results/bm-20250422-3.14.0a7%2B-b5bf8c8/bm-20250422-linux-x86_64-python-b5bf8c80a921679b2354-3.14.0a7%2B-b5bf8c8-vs-3.12.6.md)[📈](results/bm-20250422-3.14.0a7%2B-b5bf8c8/bm-20250422-linux-x86_64-python-b5bf8c80a921679b2354-3.14.0a7%2B-b5bf8c8-vs-3.12.6.svg) | 1.179x ↑<br>[📄](results/bm-20250422-3.14.0a7%2B-b5bf8c8/bm-20250422-linux-x86_64-python-b5bf8c80a921679b2354-3.14.0a7%2B-b5bf8c8-vs-3.13.0rc2.md)[📈](results/bm-20250422-3.14.0a7%2B-b5bf8c8/bm-20250422-linux-x86_64-python-b5bf8c80a921679b2354-3.14.0a7%2B-b5bf8c8-vs-3.13.0rc2.svg) |  |
| [2025-04-21](results/bm-20250421-3.14.0a7%2B-3cfab44-NOGIL) | python/3cfab449ab1e3c1472d2 | 3cfab44 (NOGIL) | 1.132x ↑<br>[📄](results/bm-20250421-3.14.0a7%2B-3cfab44-NOGIL/bm-20250421-linux-x86_64-python-3cfab449ab1e3c1472d2-3.14.0a7%2B-3cfab44-vs-3.12.6.md)[📈](results/bm-20250421-3.14.0a7%2B-3cfab44-NOGIL/bm-20250421-linux-x86_64-python-3cfab449ab1e3c1472d2-3.14.0a7%2B-3cfab44-vs-3.12.6.svg) | 1.094x ↑<br>[📄](results/bm-20250421-3.14.0a7%2B-3cfab44-NOGIL/bm-20250421-linux-x86_64-python-3cfab449ab1e3c1472d2-3.14.0a7%2B-3cfab44-vs-3.13.0rc2.md)[📈](results/bm-20250421-3.14.0a7%2B-3cfab44-NOGIL/bm-20250421-linux-x86_64-python-3cfab449ab1e3c1472d2-3.14.0a7%2B-3cfab44-vs-3.13.0rc2.svg) | 1.085x ↓<br>[📄](results/bm-20250421-3.14.0a7%2B-3cfab44-NOGIL/bm-20250421-linux-x86_64-python-3cfab449ab1e3c1472d2-3.14.0a7%2B-3cfab44-vs-base.md)[📈](results/bm-20250421-3.14.0a7%2B-3cfab44-NOGIL/bm-20250421-linux-x86_64-python-3cfab449ab1e3c1472d2-3.14.0a7%2B-3cfab44-vs-base.svg)[🧠](results/bm-20250421-3.14.0a7%2B-3cfab44-NOGIL/bm-20250421-linux-x86_64-python-3cfab449ab1e3c1472d2-3.14.0a7%2B-3cfab44-vs-base-mem.svg) |

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-04-28](results/bm-20250428-3.14.0a7%2B-1b7470f-NOGIL) | python/1b7470f8cbff4bb9e58e | 1b7470f (NOGIL) | 1.026x ↑<br>[📄](results/bm-20250428-3.14.0a7%2B-1b7470f-NOGIL/bm-20250428-vultr-x86_64-python-1b7470f8cbff4bb9e58e-3.14.0a7%2B-1b7470f-vs-3.12.6.md)[📈](results/bm-20250428-3.14.0a7%2B-1b7470f-NOGIL/bm-20250428-vultr-x86_64-python-1b7470f8cbff4bb9e58e-3.14.0a7%2B-1b7470f-vs-3.12.6.svg) | 1.007x ↓<br>[📄](results/bm-20250428-3.14.0a7%2B-1b7470f-NOGIL/bm-20250428-vultr-x86_64-python-1b7470f8cbff4bb9e58e-3.14.0a7%2B-1b7470f-vs-3.13.0rc2.md)[📈](results/bm-20250428-3.14.0a7%2B-1b7470f-NOGIL/bm-20250428-vultr-x86_64-python-1b7470f8cbff4bb9e58e-3.14.0a7%2B-1b7470f-vs-3.13.0rc2.svg) | 1.086x ↓<br>[📄](results/bm-20250428-3.14.0a7%2B-1b7470f-NOGIL/bm-20250428-vultr-x86_64-python-1b7470f8cbff4bb9e58e-3.14.0a7%2B-1b7470f-vs-base.md)[📈](results/bm-20250428-3.14.0a7%2B-1b7470f-NOGIL/bm-20250428-vultr-x86_64-python-1b7470f8cbff4bb9e58e-3.14.0a7%2B-1b7470f-vs-base.svg)[🧠](results/bm-20250428-3.14.0a7%2B-1b7470f-NOGIL/bm-20250428-vultr-x86_64-python-1b7470f8cbff4bb9e58e-3.14.0a7%2B-1b7470f-vs-base-mem.svg) |
| [2025-04-28](results/bm-20250428-3.14.0a7%2B-1b7470f) | python/1b7470f8cbff4bb9e58e | 1b7470f | 1.116x ↑<br>[📄](results/bm-20250428-3.14.0a7%2B-1b7470f/bm-20250428-vultr-x86_64-python-1b7470f8cbff4bb9e58e-3.14.0a7%2B-1b7470f-vs-3.12.6.md)[📈](results/bm-20250428-3.14.0a7%2B-1b7470f/bm-20250428-vultr-x86_64-python-1b7470f8cbff4bb9e58e-3.14.0a7%2B-1b7470f-vs-3.12.6.svg) | 1.076x ↑<br>[📄](results/bm-20250428-3.14.0a7%2B-1b7470f/bm-20250428-vultr-x86_64-python-1b7470f8cbff4bb9e58e-3.14.0a7%2B-1b7470f-vs-3.13.0rc2.md)[📈](results/bm-20250428-3.14.0a7%2B-1b7470f/bm-20250428-vultr-x86_64-python-1b7470f8cbff4bb9e58e-3.14.0a7%2B-1b7470f-vs-3.13.0rc2.svg) |  |
| [2025-04-26](results/bm-20250426-3.14.0a7%2B-4f18916-NOGIL) | python/4f18916c5c28321f363e | 4f18916 (NOGIL) | 1.023x ↑<br>[📄](results/bm-20250426-3.14.0a7%2B-4f18916-NOGIL/bm-20250426-vultr-x86_64-python-4f18916c5c28321f363e-3.14.0a7%2B-4f18916-vs-3.12.6.md)[📈](results/bm-20250426-3.14.0a7%2B-4f18916-NOGIL/bm-20250426-vultr-x86_64-python-4f18916c5c28321f363e-3.14.0a7%2B-4f18916-vs-3.12.6.svg) | 1.010x ↓<br>[📄](results/bm-20250426-3.14.0a7%2B-4f18916-NOGIL/bm-20250426-vultr-x86_64-python-4f18916c5c28321f363e-3.14.0a7%2B-4f18916-vs-3.13.0rc2.md)[📈](results/bm-20250426-3.14.0a7%2B-4f18916-NOGIL/bm-20250426-vultr-x86_64-python-4f18916c5c28321f363e-3.14.0a7%2B-4f18916-vs-3.13.0rc2.svg) | 1.090x ↓<br>[📄](results/bm-20250426-3.14.0a7%2B-4f18916-NOGIL/bm-20250426-vultr-x86_64-python-4f18916c5c28321f363e-3.14.0a7%2B-4f18916-vs-base.md)[📈](results/bm-20250426-3.14.0a7%2B-4f18916-NOGIL/bm-20250426-vultr-x86_64-python-4f18916c5c28321f363e-3.14.0a7%2B-4f18916-vs-base.svg)[🧠](results/bm-20250426-3.14.0a7%2B-4f18916-NOGIL/bm-20250426-vultr-x86_64-python-4f18916c5c28321f363e-3.14.0a7%2B-4f18916-vs-base-mem.svg) |
| [2025-04-26](results/bm-20250426-3.14.0a7%2B-4f18916-JIT) | python/4f18916c5c28321f363e | 4f18916 (JIT) | 1.116x ↑<br>[📄](results/bm-20250426-3.14.0a7%2B-4f18916-JIT/bm-20250426-vultr-x86_64-python-4f18916c5c28321f363e-3.14.0a7%2B-4f18916-vs-3.12.6.md)[📈](results/bm-20250426-3.14.0a7%2B-4f18916-JIT/bm-20250426-vultr-x86_64-python-4f18916c5c28321f363e-3.14.0a7%2B-4f18916-vs-3.12.6.svg) | 1.076x ↑<br>[📄](results/bm-20250426-3.14.0a7%2B-4f18916-JIT/bm-20250426-vultr-x86_64-python-4f18916c5c28321f363e-3.14.0a7%2B-4f18916-vs-3.13.0rc2.md)[📈](results/bm-20250426-3.14.0a7%2B-4f18916-JIT/bm-20250426-vultr-x86_64-python-4f18916c5c28321f363e-3.14.0a7%2B-4f18916-vs-3.13.0rc2.svg) | 1.001x ↓<br>[📄](results/bm-20250426-3.14.0a7%2B-4f18916-JIT/bm-20250426-vultr-x86_64-python-4f18916c5c28321f363e-3.14.0a7%2B-4f18916-vs-base.md)[📈](results/bm-20250426-3.14.0a7%2B-4f18916-JIT/bm-20250426-vultr-x86_64-python-4f18916c5c28321f363e-3.14.0a7%2B-4f18916-vs-base.svg)[🧠](results/bm-20250426-3.14.0a7%2B-4f18916-JIT/bm-20250426-vultr-x86_64-python-4f18916c5c28321f363e-3.14.0a7%2B-4f18916-vs-base-mem.svg) |
| [2025-04-26](results/bm-20250426-3.14.0a7%2B-4f18916-CLANG) | python/4f18916c5c28321f363e | 4f18916 (CLANG) | 1.174x ↑<br>[📄](results/bm-20250426-3.14.0a7%2B-4f18916-CLANG/bm-20250426-vultr-x86_64-python-4f18916c5c28321f363e-3.14.0a7%2B-4f18916-vs-3.12.6.md)[📈](results/bm-20250426-3.14.0a7%2B-4f18916-CLANG/bm-20250426-vultr-x86_64-python-4f18916c5c28321f363e-3.14.0a7%2B-4f18916-vs-3.12.6.svg) | 1.133x ↑<br>[📄](results/bm-20250426-3.14.0a7%2B-4f18916-CLANG/bm-20250426-vultr-x86_64-python-4f18916c5c28321f363e-3.14.0a7%2B-4f18916-vs-3.13.0rc2.md)[📈](results/bm-20250426-3.14.0a7%2B-4f18916-CLANG/bm-20250426-vultr-x86_64-python-4f18916c5c28321f363e-3.14.0a7%2B-4f18916-vs-3.13.0rc2.svg) | 1.049x ↑<br>[📄](results/bm-20250426-3.14.0a7%2B-4f18916-CLANG/bm-20250426-vultr-x86_64-python-4f18916c5c28321f363e-3.14.0a7%2B-4f18916-vs-base.md)[📈](results/bm-20250426-3.14.0a7%2B-4f18916-CLANG/bm-20250426-vultr-x86_64-python-4f18916c5c28321f363e-3.14.0a7%2B-4f18916-vs-base.svg)[🧠](results/bm-20250426-3.14.0a7%2B-4f18916-CLANG/bm-20250426-vultr-x86_64-python-4f18916c5c28321f363e-3.14.0a7%2B-4f18916-vs-base-mem.svg) |
| [2025-04-26](results/bm-20250426-3.14.0a7%2B-4f18916) | python/4f18916c5c28321f363e | 4f18916 | 1.117x ↑<br>[📄](results/bm-20250426-3.14.0a7%2B-4f18916/bm-20250426-vultr-x86_64-python-4f18916c5c28321f363e-3.14.0a7%2B-4f18916-vs-3.12.6.md)[📈](results/bm-20250426-3.14.0a7%2B-4f18916/bm-20250426-vultr-x86_64-python-4f18916c5c28321f363e-3.14.0a7%2B-4f18916-vs-3.12.6.svg) | 1.077x ↑<br>[📄](results/bm-20250426-3.14.0a7%2B-4f18916/bm-20250426-vultr-x86_64-python-4f18916c5c28321f363e-3.14.0a7%2B-4f18916-vs-3.13.0rc2.md)[📈](results/bm-20250426-3.14.0a7%2B-4f18916/bm-20250426-vultr-x86_64-python-4f18916c5c28321f363e-3.14.0a7%2B-4f18916-vs-3.13.0rc2.svg) |  |
| [2025-04-25](results/bm-20250425-3.14.0a7%2B-8a4d4f3-NOGIL) | python/8a4d4f37abb9fa639fdc | 8a4d4f3 (NOGIL) | 1.027x ↑<br>[📄](results/bm-20250425-3.14.0a7%2B-8a4d4f3-NOGIL/bm-20250425-vultr-x86_64-python-8a4d4f37abb9fa639fdc-3.14.0a7%2B-8a4d4f3-vs-3.12.6.md)[📈](results/bm-20250425-3.14.0a7%2B-8a4d4f3-NOGIL/bm-20250425-vultr-x86_64-python-8a4d4f37abb9fa639fdc-3.14.0a7%2B-8a4d4f3-vs-3.12.6.svg) | 1.006x ↓<br>[📄](results/bm-20250425-3.14.0a7%2B-8a4d4f3-NOGIL/bm-20250425-vultr-x86_64-python-8a4d4f37abb9fa639fdc-3.14.0a7%2B-8a4d4f3-vs-3.13.0rc2.md)[📈](results/bm-20250425-3.14.0a7%2B-8a4d4f3-NOGIL/bm-20250425-vultr-x86_64-python-8a4d4f37abb9fa639fdc-3.14.0a7%2B-8a4d4f3-vs-3.13.0rc2.svg) | 1.083x ↓<br>[📄](results/bm-20250425-3.14.0a7%2B-8a4d4f3-NOGIL/bm-20250425-vultr-x86_64-python-8a4d4f37abb9fa639fdc-3.14.0a7%2B-8a4d4f3-vs-base.md)[📈](results/bm-20250425-3.14.0a7%2B-8a4d4f3-NOGIL/bm-20250425-vultr-x86_64-python-8a4d4f37abb9fa639fdc-3.14.0a7%2B-8a4d4f3-vs-base.svg)[🧠](results/bm-20250425-3.14.0a7%2B-8a4d4f3-NOGIL/bm-20250425-vultr-x86_64-python-8a4d4f37abb9fa639fdc-3.14.0a7%2B-8a4d4f3-vs-base-mem.svg) |
| [2025-04-25](results/bm-20250425-3.14.0a7%2B-8a4d4f3) | python/8a4d4f37abb9fa639fdc | 8a4d4f3 | 1.114x ↑<br>[📄](results/bm-20250425-3.14.0a7%2B-8a4d4f3/bm-20250425-vultr-x86_64-python-8a4d4f37abb9fa639fdc-3.14.0a7%2B-8a4d4f3-vs-3.12.6.md)[📈](results/bm-20250425-3.14.0a7%2B-8a4d4f3/bm-20250425-vultr-x86_64-python-8a4d4f37abb9fa639fdc-3.14.0a7%2B-8a4d4f3-vs-3.12.6.svg) | 1.074x ↑<br>[📄](results/bm-20250425-3.14.0a7%2B-8a4d4f3/bm-20250425-vultr-x86_64-python-8a4d4f37abb9fa639fdc-3.14.0a7%2B-8a4d4f3-vs-3.13.0rc2.md)[📈](results/bm-20250425-3.14.0a7%2B-8a4d4f3/bm-20250425-vultr-x86_64-python-8a4d4f37abb9fa639fdc-3.14.0a7%2B-8a4d4f3-vs-3.13.0rc2.svg) |  |
| [2025-04-24](results/bm-20250424-3.14.0a7%2B-e54e828-NOGIL) | python/e54e8288521c1bd5fa49 | e54e828 (NOGIL) | 1.025x ↑<br>[📄](results/bm-20250424-3.14.0a7%2B-e54e828-NOGIL/bm-20250424-vultr-x86_64-python-e54e8288521c1bd5fa49-3.14.0a7%2B-e54e828-vs-3.12.6.md)[📈](results/bm-20250424-3.14.0a7%2B-e54e828-NOGIL/bm-20250424-vultr-x86_64-python-e54e8288521c1bd5fa49-3.14.0a7%2B-e54e828-vs-3.12.6.svg) | 1.009x ↓<br>[📄](results/bm-20250424-3.14.0a7%2B-e54e828-NOGIL/bm-20250424-vultr-x86_64-python-e54e8288521c1bd5fa49-3.14.0a7%2B-e54e828-vs-3.13.0rc2.md)[📈](results/bm-20250424-3.14.0a7%2B-e54e828-NOGIL/bm-20250424-vultr-x86_64-python-e54e8288521c1bd5fa49-3.14.0a7%2B-e54e828-vs-3.13.0rc2.svg) | 1.086x ↓<br>[📄](results/bm-20250424-3.14.0a7%2B-e54e828-NOGIL/bm-20250424-vultr-x86_64-python-e54e8288521c1bd5fa49-3.14.0a7%2B-e54e828-vs-base.md)[📈](results/bm-20250424-3.14.0a7%2B-e54e828-NOGIL/bm-20250424-vultr-x86_64-python-e54e8288521c1bd5fa49-3.14.0a7%2B-e54e828-vs-base.svg)[🧠](results/bm-20250424-3.14.0a7%2B-e54e828-NOGIL/bm-20250424-vultr-x86_64-python-e54e8288521c1bd5fa49-3.14.0a7%2B-e54e828-vs-base-mem.svg) |
| [2025-04-24](results/bm-20250424-3.14.0a7%2B-e54e828) | python/e54e8288521c1bd5fa49 | e54e828 | 1.113x ↑<br>[📄](results/bm-20250424-3.14.0a7%2B-e54e828/bm-20250424-vultr-x86_64-python-e54e8288521c1bd5fa49-3.14.0a7%2B-e54e828-vs-3.12.6.md)[📈](results/bm-20250424-3.14.0a7%2B-e54e828/bm-20250424-vultr-x86_64-python-e54e8288521c1bd5fa49-3.14.0a7%2B-e54e828-vs-3.12.6.svg) | 1.074x ↑<br>[📄](results/bm-20250424-3.14.0a7%2B-e54e828/bm-20250424-vultr-x86_64-python-e54e8288521c1bd5fa49-3.14.0a7%2B-e54e828-vs-3.13.0rc2.md)[📈](results/bm-20250424-3.14.0a7%2B-e54e828/bm-20250424-vultr-x86_64-python-e54e8288521c1bd5fa49-3.14.0a7%2B-e54e828-vs-3.13.0rc2.svg) |  |

## darwin arm64 (macm4pro)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-04-28](results/bm-20250428-3.14.0a7%2B-b739ec5-NOGIL) | python/main | b739ec5 (NOGIL) | 1.082x ↑<br>[📄](results/bm-20250428-3.14.0a7%2B-b739ec5-NOGIL/bm-20250428-macm4pro-arm64-python-main-3.14.0a7%2B-b739ec5-vs-3.12.6.md)[📈](results/bm-20250428-3.14.0a7%2B-b739ec5-NOGIL/bm-20250428-macm4pro-arm64-python-main-3.14.0a7%2B-b739ec5-vs-3.12.6.svg) | 1.003x ↑<br>[📄](results/bm-20250428-3.14.0a7%2B-b739ec5-NOGIL/bm-20250428-macm4pro-arm64-python-main-3.14.0a7%2B-b739ec5-vs-3.13.0rc2.md)[📈](results/bm-20250428-3.14.0a7%2B-b739ec5-NOGIL/bm-20250428-macm4pro-arm64-python-main-3.14.0a7%2B-b739ec5-vs-3.13.0rc2.svg) | 1.001x ↑<br>[📄](results/bm-20250428-3.14.0a7%2B-b739ec5-NOGIL/bm-20250428-macm4pro-arm64-python-main-3.14.0a7%2B-b739ec5-vs-base.md)[📈](results/bm-20250428-3.14.0a7%2B-b739ec5-NOGIL/bm-20250428-macm4pro-arm64-python-main-3.14.0a7%2B-b739ec5-vs-base.svg)[🧠](results/bm-20250428-3.14.0a7%2B-b739ec5-NOGIL/bm-20250428-macm4pro-arm64-python-main-3.14.0a7%2B-b739ec5-vs-base-mem.svg) |
| [2025-04-28](results/bm-20250428-3.14.0a7%2B-58567cc-NOGIL) | python/58567cc18c5b048e0830 | 58567cc (NOGIL) | 1.081x ↑<br>[📄](results/bm-20250428-3.14.0a7%2B-58567cc-NOGIL/bm-20250428-macm4pro-arm64-python-58567cc18c5b048e0830-3.14.0a7%2B-58567cc-vs-3.12.6.md)[📈](results/bm-20250428-3.14.0a7%2B-58567cc-NOGIL/bm-20250428-macm4pro-arm64-python-58567cc18c5b048e0830-3.14.0a7%2B-58567cc-vs-3.12.6.svg) | 1.003x ↑<br>[📄](results/bm-20250428-3.14.0a7%2B-58567cc-NOGIL/bm-20250428-macm4pro-arm64-python-58567cc18c5b048e0830-3.14.0a7%2B-58567cc-vs-3.13.0rc2.md)[📈](results/bm-20250428-3.14.0a7%2B-58567cc-NOGIL/bm-20250428-macm4pro-arm64-python-58567cc18c5b048e0830-3.14.0a7%2B-58567cc-vs-3.13.0rc2.svg) |  |
| [2025-04-24](results/bm-20250424-3.14.0a7%2B-e54e828-NOGIL) | python/e54e8288521c1bd5fa49 | e54e828 (NOGIL) | 1.104x ↑<br>[📄](results/bm-20250424-3.14.0a7%2B-e54e828-NOGIL/bm-20250424-macm4pro-arm64-python-e54e8288521c1bd5fa49-3.14.0a7%2B-e54e828-vs-3.12.6.md)[📈](results/bm-20250424-3.14.0a7%2B-e54e828-NOGIL/bm-20250424-macm4pro-arm64-python-e54e8288521c1bd5fa49-3.14.0a7%2B-e54e828-vs-3.12.6.svg) | 1.024x ↑<br>[📄](results/bm-20250424-3.14.0a7%2B-e54e828-NOGIL/bm-20250424-macm4pro-arm64-python-e54e8288521c1bd5fa49-3.14.0a7%2B-e54e828-vs-3.13.0rc2.md)[📈](results/bm-20250424-3.14.0a7%2B-e54e828-NOGIL/bm-20250424-macm4pro-arm64-python-e54e8288521c1bd5fa49-3.14.0a7%2B-e54e828-vs-3.13.0rc2.svg) | 1.020x ↓<br>[📄](results/bm-20250424-3.14.0a7%2B-e54e828-NOGIL/bm-20250424-macm4pro-arm64-python-e54e8288521c1bd5fa49-3.14.0a7%2B-e54e828-vs-base.md)[📈](results/bm-20250424-3.14.0a7%2B-e54e828-NOGIL/bm-20250424-macm4pro-arm64-python-e54e8288521c1bd5fa49-3.14.0a7%2B-e54e828-vs-base.svg)[🧠](results/bm-20250424-3.14.0a7%2B-e54e828-NOGIL/bm-20250424-macm4pro-arm64-python-e54e8288521c1bd5fa49-3.14.0a7%2B-e54e828-vs-base-mem.svg) |
| [2025-04-24](results/bm-20250424-3.14.0a7%2B-e54e828) | python/e54e8288521c1bd5fa49 | e54e828 | 1.124x ↑<br>[📄](results/bm-20250424-3.14.0a7%2B-e54e828/bm-20250424-macm4pro-arm64-python-e54e8288521c1bd5fa49-3.14.0a7%2B-e54e828-vs-3.12.6.md)[📈](results/bm-20250424-3.14.0a7%2B-e54e828/bm-20250424-macm4pro-arm64-python-e54e8288521c1bd5fa49-3.14.0a7%2B-e54e828-vs-3.12.6.svg) | 1.042x ↑<br>[📄](results/bm-20250424-3.14.0a7%2B-e54e828/bm-20250424-macm4pro-arm64-python-e54e8288521c1bd5fa49-3.14.0a7%2B-e54e828-vs-3.13.0rc2.md)[📈](results/bm-20250424-3.14.0a7%2B-e54e828/bm-20250424-macm4pro-arm64-python-e54e8288521c1bd5fa49-3.14.0a7%2B-e54e828-vs-3.13.0rc2.svg) |  |


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
