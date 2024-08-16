# Results

- fork: python
- version: 3.13.0b1
- config: 
- commit hash: [2268289](https://github.com/python/cpython/commit/2268289)
- commit date: 2024-05-08T11:21:00+02:00
- commit merge base: [c4f9823be277b2e3de2315526612276626217743](https://github.com/python/cpython/commit/c4f9823be277b2e3de2315526612276626217743)
- ref: 2268289a47c6e3c9a220

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/10395537562)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1063-aws-x86_64-with-glibc2.31
- [raw results](bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289.json)

### vs. 3.12.0b1

- Geometric mean: 1.01x faster (HPT: reliability of 100.00%, 1.00x faster at 99th %ile)
- Memory usage: 1.85x
- missing benchmarks: mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289-vs-3.12.0b1.md)
- [📈time plot](bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289-vs-3.12.0b1.svg)

### vs. 3.12.5+

- Geometric mean: 1.00x slower (HPT: reliability of 96.89%, 1.00x faster at 99th %ile)
- Memory usage: 1.01x
- missing benchmarks: mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289-vs-3.12.5%2B.md)
- [📈time plot](bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289-vs-3.12.5%2B.svg)

### vs. 3.13.0rc1+

- Geometric mean: 1.03x slower (HPT: reliability of 97.73%, 1.00x slower at 99th %ile)
- Memory usage: 0.99x
- [📄table](bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289-vs-3.13.0rc1%2B.md)
- [📈time plot](bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289-vs-3.13.0rc1%2B.svg)

