# Results

- fork: python
- version: 3.13.0rc2
- config: NOGIL
- commit hash: [ec61006](https://github.com/python/cpython/commit/ec61006)
- commit date: 2024-09-06T23:15:21+02:00
- ref: v3.13.0rc2

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/10947089461)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1063-aws-x86_64-with-glibc2.31
- [raw results](bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json)

### vs. 3.12.6

- Geometric mean: 1.37x slower (HPT: reliability of 100.00%, 1.24x slower at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: dask, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006-vs-3.12.6.md)
- [📈time plot](bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.42x slower (HPT: reliability of 100.00%, 1.29x slower at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: dask
- [📄table](bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006-vs-3.13.0rc2.md)
- [📈time plot](bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.42x slower (HPT: reliability of 100.00%, 1.29x slower at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: 🔴 dask
- [🧠memory plot](bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006-vs-base-mem.svg)
- [📄table](bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006-vs-base.md)
- [📈time plot](bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006-vs-base.svg)

### vs. 3.12.0b1

- [📄table](bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006-vs-3.12.0b1.md)
- [📈time plot](bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006-vs-3.12.0b1.svg)

### vs. 3.12.5+

- [📄table](bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006-vs-3.12.5%2B.md)
- [📈time plot](bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006-vs-3.12.5%2B.svg)

### vs. 3.13.0b1

- [📄table](bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006-vs-3.13.0b1.md)
- [📈time plot](bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006-vs-3.13.0b1.svg)

### vs. 3.13.0rc1+

- [📄table](bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006-vs-3.13.0rc1%2B.md)
- [📈time plot](bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006-vs-3.13.0rc1%2B.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/10966676301)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json)

### vs. 3.12.6

- Geometric mean: 1.45x slower (HPT: reliability of 100.00%, 1.31x slower at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: dask, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006-vs-3.12.6.md)
- [📈time plot](bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.49x slower (HPT: reliability of 100.00%, 1.32x slower at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: dask
- [📄table](bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006-vs-3.13.0rc2.md)
- [📈time plot](bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.49x slower (HPT: reliability of 100.00%, 1.32x slower at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: 🔴 dask
- [🧠memory plot](bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006-vs-base-mem.svg)
- [📄table](bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006-vs-base.md)
- [📈time plot](bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006-vs-base.svg)

