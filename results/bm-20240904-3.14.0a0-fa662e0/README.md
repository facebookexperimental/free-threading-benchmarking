# Results

- fork: mpage
- version: 3.14.0a0
- config: 
- commit hash: [fa662e0](https://github.com/mpage/cpython/commit/fa662e0)
- commit date: 2024-09-04T15:59:10-07:00
- commit merge base: [7e38e6745d2f9ee235d934ab7f3c6b3085be2b70](https://github.com/mpage/cpython/commit/7e38e6745d2f9ee235d934ab7f3c6b3085be2b70)
- ref: fa662e0b71a91c279cd2

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/10712985687)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1063-aws-x86_64-with-glibc2.31
- [raw results](bm-20240904-linux-x86_64-mpage-fa662e0b71a91c279cd2-3.14.0a0-fa662e0.json)

### vs. 3.12.0b1

- Geometric mean: 1.15x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.87x
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240904-linux-x86_64-mpage-fa662e0b71a91c279cd2-3.14.0a0-fa662e0-vs-3.12.0b1.md)
- [📈time plot](bm-20240904-linux-x86_64-mpage-fa662e0b71a91c279cd2-3.14.0a0-fa662e0-vs-3.12.0b1.svg)

### vs. 3.12.5+

- Geometric mean: 1.16x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.01x
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20240904-linux-x86_64-mpage-fa662e0b71a91c279cd2-3.14.0a0-fa662e0-vs-3.12.5%2B.md)
- [📈time plot](bm-20240904-linux-x86_64-mpage-fa662e0b71a91c279cd2-3.14.0a0-fa662e0-vs-3.12.5%2B.svg)

### vs. 3.13.0b1

- Geometric mean: 1.15x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn
- [📄table](bm-20240904-linux-x86_64-mpage-fa662e0b71a91c279cd2-3.14.0a0-fa662e0-vs-3.13.0b1.md)
- [📈time plot](bm-20240904-linux-x86_64-mpage-fa662e0b71a91c279cd2-3.14.0a0-fa662e0-vs-3.13.0b1.svg)

### vs. 3.13.0rc1+

- Geometric mean: 1.20x slower (HPT: reliability of 100.00%, 1.13x slower at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn
- [📄table](bm-20240904-linux-x86_64-mpage-fa662e0b71a91c279cd2-3.14.0a0-fa662e0-vs-3.13.0rc1%2B.md)
- [📈time plot](bm-20240904-linux-x86_64-mpage-fa662e0b71a91c279cd2-3.14.0a0-fa662e0-vs-3.13.0rc1%2B.svg)

