# Results

- fork: python/v3.12.6
- version: 3.12.6
- config: 
- commit hash: [a4a2d2b](https://github.com/python/cpython/commit/a4a2d2b)
- commit date: 2024-09-06T21:03:47+02:00
- ref: v3.12.6

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/10967879382)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1063-aws-x86_64-with-glibc2.31
- [raw results](bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 99.79%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- new benchmarks: mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b-vs-3.13.0rc2.md)
- [📈time plot](bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b-vs-3.13.0rc2.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/10965245426)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.01x slower at 99th %ile)
- Memory usage: 0.99x
- new benchmarks: mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b-vs-3.13.0rc2.md)
- [📈time plot](bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13906391158)
- cpu model: missing
- platform: macOS-15.3.1-arm64-arm-64bit
- [raw results](bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json)

