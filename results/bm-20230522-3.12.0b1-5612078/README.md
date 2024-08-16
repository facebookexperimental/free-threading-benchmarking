# Results

- fork: python
- version: 3.12.0b1
- config: 
- commit hash: [5612078](https://github.com/python/cpython/commit/5612078)
- commit date: 2023-05-22T14:07:36+02:00
- commit merge base: [5360cb3d5608ab375de6cd8c0b408459f3fa953a](https://github.com/python/cpython/commit/5360cb3d5608ab375de6cd8c0b408459f3fa953a)
- ref: 5612078f68e9688fbf3b

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/10395533870)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1063-aws-x86_64-with-glibc2.31
- [raw results](bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078.json)

### vs. 3.12.5+

- Geometric mean: 1.01x slower (HPT: reliability of 97.07%, 1.00x slower at 99th %ile)
- Memory usage: 0.59x
- [📄table](bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078-vs-3.12.5%2B.md)
- [📈time plot](bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078-vs-3.12.5%2B.svg)

### vs. 3.13.0b1

- Geometric mean: 1.01x slower (HPT: reliability of 100.00%, 1.00x slower at 99th %ile)
- Memory usage: 0.58x
- new benchmarks: mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078-vs-3.13.0b1.md)
- [📈time plot](bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078-vs-3.13.0b1.svg)

### vs. 3.13.0rc1+

- Geometric mean: 1.04x slower (HPT: reliability of 100.00%, 1.01x slower at 99th %ile)
- Memory usage: 0.58x
- new benchmarks: mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078-vs-3.13.0rc1%2B.md)
- [📈time plot](bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078-vs-3.13.0rc1%2B.svg)

