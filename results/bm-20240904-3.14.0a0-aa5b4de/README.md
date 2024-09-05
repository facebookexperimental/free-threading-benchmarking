# Results

- fork: mpage
- version: 3.14.0a0
- config: 
- commit hash: [aa5b4de](https://github.com/mpage/cpython/commit/aa5b4de)
- commit date: 2024-09-04T16:13:09-07:00
- commit merge base: [7e38e6745d2f9ee235d934ab7f3c6b3085be2b70](https://github.com/mpage/cpython/commit/7e38e6745d2f9ee235d934ab7f3c6b3085be2b70)
- ref: gh_115999_measure_sp

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/10709484612)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1063-aws-x86_64-with-glibc2.31
- [raw results](bm-20240904-linux-x86_64-mpage-gh_115999_measure_sp-3.14.0a0-aa5b4de.json)

### vs. 3.12.0b1

- Geometric mean: 1.18x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.87x
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240904-linux-x86_64-mpage-gh_115999_measure_sp-3.14.0a0-aa5b4de-vs-3.12.0b1.md)
- [📈time plot](bm-20240904-linux-x86_64-mpage-gh_115999_measure_sp-3.14.0a0-aa5b4de-vs-3.12.0b1.svg)

### vs. 3.12.5+

- Geometric mean: 1.19x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.01x
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240904-linux-x86_64-mpage-gh_115999_measure_sp-3.14.0a0-aa5b4de-vs-3.12.5%2B.md)
- [📈time plot](bm-20240904-linux-x86_64-mpage-gh_115999_measure_sp-3.14.0a0-aa5b4de-vs-3.12.5%2B.svg)

### vs. 3.13.0b1

- Geometric mean: 1.19x slower (HPT: reliability of 100.00%, 1.15x slower at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn
- [📄table](bm-20240904-linux-x86_64-mpage-gh_115999_measure_sp-3.14.0a0-aa5b4de-vs-3.13.0b1.md)
- [📈time plot](bm-20240904-linux-x86_64-mpage-gh_115999_measure_sp-3.14.0a0-aa5b4de-vs-3.13.0b1.svg)

### vs. 3.13.0rc1+

- Geometric mean: 1.23x slower (HPT: reliability of 100.00%, 1.15x slower at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn
- [📄table](bm-20240904-linux-x86_64-mpage-gh_115999_measure_sp-3.14.0a0-aa5b4de-vs-3.13.0rc1%2B.md)
- [📈time plot](bm-20240904-linux-x86_64-mpage-gh_115999_measure_sp-3.14.0a0-aa5b4de-vs-3.13.0rc1%2B.svg)

