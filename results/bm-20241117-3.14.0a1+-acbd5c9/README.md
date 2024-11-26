# Results

- fork: python
- version: 3.14.0a1+
- config: 
- commit hash: [acbd5c9](https://github.com/python/cpython/commit/acbd5c9)
- commit date: 2024-11-17T00:07:25+00:00
- commit merge base: [ed81971e6b26c34445f06850192b34458b029337](https://github.com/python/cpython/commit/ed81971e6b26c34445f06850192b34458b029337)
- ref: acbd5c9c6c62dac34d2e

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11874309255)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1%2B-acbd5c9.json)

### vs. 3.12.6

- Geometric mean: 1.022x faster (HPT: reliability of 99.56%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- [📄table](bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1%2B-acbd5c9-vs-3.12.6.md)
- [📈time plot](bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1%2B-acbd5c9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.013x faster (HPT: reliability of 91.38%, 1.00x faster at 99th %ile)
- Memory usage: 1.01x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http
- [📄table](bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1%2B-acbd5c9-vs-3.13.0rc2.md)
- [📈time plot](bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1%2B-acbd5c9-vs-3.13.0rc2.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11874309255)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [pystats raw](bm-20241117-vultr-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1%2B-acbd5c9-pystats.json)
- [pystats table](bm-20241117-vultr-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1%2B-acbd5c9-pystats.md)
- [raw results](bm-20241117-vultr-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1%2B-acbd5c9.json)

### vs. 3.12.6

- Geometric mean: 1.021x faster (HPT: reliability of 99.25%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- [📄table](bm-20241117-vultr-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1%2B-acbd5c9-vs-3.12.6.md)
- [📈time plot](bm-20241117-vultr-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1%2B-acbd5c9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.005x faster (HPT: reliability of 70.14%, 1.00x slower at 99th %ile)
- Memory usage: 1.01x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http
- [📄table](bm-20241117-vultr-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1%2B-acbd5c9-vs-3.13.0rc2.md)
- [📈time plot](bm-20241117-vultr-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1%2B-acbd5c9-vs-3.13.0rc2.svg)

