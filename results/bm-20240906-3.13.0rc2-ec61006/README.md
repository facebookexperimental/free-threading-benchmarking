# Results

- fork: python/v3.13.0rc2
- version: 3.13.0rc2
- config: 
- commit hash: [ec61006](https://github.com/python/cpython/commit/ec61006)
- commit date: 2024-09-06T23:15:21+02:00
- ref: v3.13.0rc2

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/10965256084)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006-vs-3.12.6.md)
- [📈time plot](bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 98.90%, 1.00x slower at 99th %ile)
- Memory usage: 0.99x
- [📄table](bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006-vs-3.13.0rc2.md)
- [📈time plot](bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13924337418)
- cpu model: missing
- platform: macOS-15.3.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json)

### vs. 3.12.6

- Geometric mean: 1.077x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.06x
- [📄table](bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006-vs-3.12.6.md)
- [📈time plot](bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006-vs-3.12.6.svg)

