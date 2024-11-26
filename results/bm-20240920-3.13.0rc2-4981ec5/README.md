# Results

- fork: mpage
- version: 3.13.0rc2
- config: 
- commit hash: [4981ec5](https://github.com/mpage/cpython/commit/4981ec5)
- commit date: 2024-09-20T20:20:41-07:00
- fork: python
- commit hash: [4981ec5](https://github.com/python/cpython/commit/4981ec5)
- ref: 4981ec59ded050919eb2

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/10970087024)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1063-aws-x86_64-with-glibc2.31
- [raw results](bm-20240920-linux-x86_64-mpage-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 97.26%, 1.00x faster at 99th %ile)
- Memory usage: 1.01x
- missing benchmarks: mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240920-linux-x86_64-mpage-4981ec59ded050919eb2-3.13.0rc2-4981ec5-vs-3.12.6.md)
- [📈time plot](bm-20240920-linux-x86_64-mpage-4981ec59ded050919eb2-3.13.0rc2-4981ec5-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 55.77%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [📄table](bm-20240920-linux-x86_64-mpage-4981ec59ded050919eb2-3.13.0rc2-4981ec5-vs-3.13.0rc2.md)
- [📈time plot](bm-20240920-linux-x86_64-mpage-4981ec59ded050919eb2-3.13.0rc2-4981ec5-vs-3.13.0rc2.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/10969281961)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5-vs-3.12.6.md)
- [📈time plot](bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 98.90%, 1.00x faster at 99th %ile)
- Memory usage: 1.01x
- [📄table](bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5-vs-3.13.0rc2.md)
- [📈time plot](bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5-vs-3.13.0rc2.svg)

