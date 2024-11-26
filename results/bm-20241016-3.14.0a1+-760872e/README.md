# Results

- fork: python
- version: 3.14.0a1+
- config: 
- commit hash: [760872e](https://github.com/python/cpython/commit/760872e)
- commit date: 2024-10-16T11:39:17-04:00
- commit merge base: [d83fcf8371f2f33c7797bc8f5423a8bca8c46e5c](https://github.com/python/cpython/commit/d83fcf8371f2f33c7797bc8f5423a8bca8c46e5c)
- ref: 760872efecb95017db8e

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11372918029)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [pystats raw](bm-20241016-vultr-x86_64-python-760872efecb95017db8e-3.14.0a1%2B-760872e-pystats.json)
- [pystats table](bm-20241016-vultr-x86_64-python-760872efecb95017db8e-3.14.0a1%2B-760872e-pystats.md)
- [raw results](bm-20241016-vultr-x86_64-python-760872efecb95017db8e-3.14.0a1%2B-760872e.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 99.53%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20241016-vultr-x86_64-python-760872efecb95017db8e-3.14.0a1%2B-760872e-vs-3.12.6.md)
- [📈time plot](bm-20241016-vultr-x86_64-python-760872efecb95017db8e-3.14.0a1%2B-760872e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 86.22%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn
- [📄table](bm-20241016-vultr-x86_64-python-760872efecb95017db8e-3.14.0a1%2B-760872e-vs-3.13.0rc2.md)
- [📈time plot](bm-20241016-vultr-x86_64-python-760872efecb95017db8e-3.14.0a1%2B-760872e-vs-3.13.0rc2.svg)

