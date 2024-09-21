# Results

- fork: python
- version: 3.14.0a0
- config: NOGIL
- commit hash: [540fcc6](https://github.com/python/cpython/commit/540fcc6)
- commit date: 2024-08-07T23:30:10+03:00
- commit merge base: [e73e7a7abdc3fed252affcb1629df1b3c8fff2ef](https://github.com/python/cpython/commit/e73e7a7abdc3fed252affcb1629df1b3c8fff2ef)
- ref: 540fcc62f5da982b7950

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/10315222935)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1063-aws-x86_64-with-glibc2.31
- [raw results](bm-20240807-linux-x86_64-python-540fcc62f5da982b7950-3.14.0a0-540fcc6.json)

### vs. 3.12.6

- Geometric mean: 1.35x slower (HPT: reliability of 100.00%, 1.23x slower at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240807-linux-x86_64-python-540fcc62f5da982b7950-3.14.0a0-540fcc6-vs-3.12.6.md)
- [📈time plot](bm-20240807-linux-x86_64-python-540fcc62f5da982b7950-3.14.0a0-540fcc6-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.40x slower (HPT: reliability of 100.00%, 1.27x slower at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn
- [📄table](bm-20240807-linux-x86_64-python-540fcc62f5da982b7950-3.14.0a0-540fcc6-vs-3.13.0rc2.md)
- [📈time plot](bm-20240807-linux-x86_64-python-540fcc62f5da982b7950-3.14.0a0-540fcc6-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.00x slower (HPT: reliability of 68.26%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240807-linux-x86_64-python-540fcc62f5da982b7950-3.14.0a0-540fcc6-vs-base-mem.svg)
- [📄table](bm-20240807-linux-x86_64-python-540fcc62f5da982b7950-3.14.0a0-540fcc6-vs-base.md)
- [📈time plot](bm-20240807-linux-x86_64-python-540fcc62f5da982b7950-3.14.0a0-540fcc6-vs-base.svg)

### vs. 3.12.0b1

- [📄table](bm-20240807-linux-x86_64-python-540fcc62f5da982b7950-3.14.0a0-540fcc6-vs-3.12.0b1.md)
- [📈time plot](bm-20240807-linux-x86_64-python-540fcc62f5da982b7950-3.14.0a0-540fcc6-vs-3.12.0b1.svg)

### vs. 3.12.5+

- [📄table](bm-20240807-linux-x86_64-python-540fcc62f5da982b7950-3.14.0a0-540fcc6-vs-3.12.5%2B.md)
- [📈time plot](bm-20240807-linux-x86_64-python-540fcc62f5da982b7950-3.14.0a0-540fcc6-vs-3.12.5%2B.svg)

### vs. 3.13.0b1

- [📄table](bm-20240807-linux-x86_64-python-540fcc62f5da982b7950-3.14.0a0-540fcc6-vs-3.13.0b1.md)
- [📈time plot](bm-20240807-linux-x86_64-python-540fcc62f5da982b7950-3.14.0a0-540fcc6-vs-3.13.0b1.svg)

### vs. 3.13.0rc1+

- [📄table](bm-20240807-linux-x86_64-python-540fcc62f5da982b7950-3.14.0a0-540fcc6-vs-3.13.0rc1%2B.md)
- [📈time plot](bm-20240807-linux-x86_64-python-540fcc62f5da982b7950-3.14.0a0-540fcc6-vs-3.13.0rc1%2B.svg)

