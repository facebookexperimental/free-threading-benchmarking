# Results

- fork: python
- version: 3.13.0rc1+
- config: 
- commit hash: [79452b1](https://github.com/python/cpython/commit/79452b1)
- commit date: 2024-08-14T21:31:19+00:00
- ref: 3.13

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/10395537562)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1063-aws-x86_64-with-glibc2.31
- [raw results](bm-20240814-linux-x86_64-python-3.13-3.13.0rc1%2B-79452b1.json)

### vs. 3.12.0b1

- Geometric mean: 1.04x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.86x
- missing benchmarks: mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240814-linux-x86_64-python-3.13-3.13.0rc1%2B-79452b1-vs-3.12.0b1.md)
- [📈time plot](bm-20240814-linux-x86_64-python-3.13-3.13.0rc1%2B-79452b1-vs-3.12.0b1.svg)

### vs. 3.12.5+

- Geometric mean: 1.03x faster (HPT: reliability of 99.87%, 1.00x faster at 99th %ile)
- Memory usage: 1.01x
- missing benchmarks: mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240814-linux-x86_64-python-3.13-3.13.0rc1%2B-79452b1-vs-3.12.5%2B.md)
- [📈time plot](bm-20240814-linux-x86_64-python-3.13-3.13.0rc1%2B-79452b1-vs-3.12.5%2B.svg)

### vs. 3.13.0b1

- Geometric mean: 1.03x faster (HPT: reliability of 97.73%, 1.00x faster at 99th %ile)
- Memory usage: 1.01x
- [📄table](bm-20240814-linux-x86_64-python-3.13-3.13.0rc1%2B-79452b1-vs-3.13.0b1.md)
- [📈time plot](bm-20240814-linux-x86_64-python-3.13-3.13.0rc1%2B-79452b1-vs-3.13.0b1.svg)

