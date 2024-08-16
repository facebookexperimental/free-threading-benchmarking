# Results

- fork: python
- version: 3.12.5+
- config: 
- commit hash: [9f153a2](https://github.com/python/cpython/commit/9f153a2)
- commit date: 2024-08-14T22:30:44+01:00
- ref: 3.12

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/10395533870)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1063-aws-x86_64-with-glibc2.31
- [raw results](bm-20240814-linux-x86_64-python-3.12-3.12.5%2B-9f153a2.json)

### vs. 3.12.0b1

- Geometric mean: 1.01x faster (HPT: reliability of 97.07%, 1.00x faster at 99th %ile)
- Memory usage: 1.84x
- [📄table](bm-20240814-linux-x86_64-python-3.12-3.12.5%2B-9f153a2-vs-3.12.0b1.md)
- [📈time plot](bm-20240814-linux-x86_64-python-3.12-3.12.5%2B-9f153a2-vs-3.12.0b1.svg)

### vs. 3.13.0b1

- Geometric mean: 1.00x faster (HPT: reliability of 96.89%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- new benchmarks: mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240814-linux-x86_64-python-3.12-3.12.5%2B-9f153a2-vs-3.13.0b1.md)
- [📈time plot](bm-20240814-linux-x86_64-python-3.12-3.12.5%2B-9f153a2-vs-3.13.0b1.svg)

### vs. 3.13.0rc1+

- Geometric mean: 1.03x slower (HPT: reliability of 99.87%, 1.00x slower at 99th %ile)
- Memory usage: 0.99x
- new benchmarks: mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240814-linux-x86_64-python-3.12-3.12.5%2B-9f153a2-vs-3.13.0rc1%2B.md)
- [📈time plot](bm-20240814-linux-x86_64-python-3.12-3.12.5%2B-9f153a2-vs-3.13.0rc1%2B.svg)

