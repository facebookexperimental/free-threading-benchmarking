# Results

- fork: mpage
- version: 3.13.0rc2
- config: NOGIL
- commit hash: [4981ec5](https://github.com/mpage/cpython/commit/4981ec5)
- commit date: 2024-09-20T20:20:41-07:00
- ref: 4981ec59ded050919eb2

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/10969287788)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20240920-vultr-x86_64-mpage-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json)

### vs. 3.12.6

- Geometric mean: 1.315x slower (HPT: reliability of 100.00%, 1.32x slower at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: dask, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240920-vultr-x86_64-mpage-4981ec59ded050919eb2-3.13.0rc2-4981ec5-vs-3.12.6.md)
- [📈time plot](bm-20240920-vultr-x86_64-mpage-4981ec59ded050919eb2-3.13.0rc2-4981ec5-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.336x slower (HPT: reliability of 100.00%, 1.34x slower at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: dask
- [📄table](bm-20240920-vultr-x86_64-mpage-4981ec59ded050919eb2-3.13.0rc2-4981ec5-vs-3.13.0rc2.md)
- [📈time plot](bm-20240920-vultr-x86_64-mpage-4981ec59ded050919eb2-3.13.0rc2-4981ec5-vs-3.13.0rc2.svg)

