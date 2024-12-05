# Results

- fork: python/d6bcc154e93a0a20ab97
- version: 3.14.0a1+
- config: NOGIL
- commit hash: [d6bcc15](https://github.com/python/cpython/commit/d6bcc15)
- commit date: 2024-11-15T18:09:05-05:00
- commit merge base: [94a7a4e22fb8f567090514785c69e65298acca42](https://github.com/python/cpython/commit/94a7a4e22fb8f567090514785c69e65298acca42)
- ref: d6bcc154e93a0a20ab97

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11865458454)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20241115-linux-x86_64-python-d6bcc154e93a0a20ab97-3.14.0a1%2B-d6bcc15.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.35x slower at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- [📄table](bm-20241115-linux-x86_64-python-d6bcc154e93a0a20ab97-3.14.0a1%2B-d6bcc15-vs-3.12.6.md)
- [📈time plot](bm-20241115-linux-x86_64-python-d6bcc154e93a0a20ab97-3.14.0a1%2B-d6bcc15-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.39x slower at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http
- [📄table](bm-20241115-linux-x86_64-python-d6bcc154e93a0a20ab97-3.14.0a1%2B-d6bcc15-vs-3.13.0rc2.md)
- [📈time plot](bm-20241115-linux-x86_64-python-d6bcc154e93a0a20ab97-3.14.0a1%2B-d6bcc15-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.38x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20241115-linux-x86_64-python-d6bcc154e93a0a20ab97-3.14.0a1%2B-d6bcc15-vs-base-mem.svg)
- [📄table](bm-20241115-linux-x86_64-python-d6bcc154e93a0a20ab97-3.14.0a1%2B-d6bcc15-vs-base.md)
- [📈time plot](bm-20241115-linux-x86_64-python-d6bcc154e93a0a20ab97-3.14.0a1%2B-d6bcc15-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11865458454)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241115-vultr-x86_64-python-d6bcc154e93a0a20ab97-3.14.0a1%2B-d6bcc15.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.39x slower at 99th %ile)
- Memory usage: 1.23x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- [📄table](bm-20241115-vultr-x86_64-python-d6bcc154e93a0a20ab97-3.14.0a1%2B-d6bcc15-vs-3.12.6.md)
- [📈time plot](bm-20241115-vultr-x86_64-python-d6bcc154e93a0a20ab97-3.14.0a1%2B-d6bcc15-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.41x slower at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http
- [📄table](bm-20241115-vultr-x86_64-python-d6bcc154e93a0a20ab97-3.14.0a1%2B-d6bcc15-vs-3.13.0rc2.md)
- [📈time plot](bm-20241115-vultr-x86_64-python-d6bcc154e93a0a20ab97-3.14.0a1%2B-d6bcc15-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.41x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20241115-vultr-x86_64-python-d6bcc154e93a0a20ab97-3.14.0a1%2B-d6bcc15-vs-base-mem.svg)
- [📄table](bm-20241115-vultr-x86_64-python-d6bcc154e93a0a20ab97-3.14.0a1%2B-d6bcc15-vs-base.md)
- [📈time plot](bm-20241115-vultr-x86_64-python-d6bcc154e93a0a20ab97-3.14.0a1%2B-d6bcc15-vs-base.svg)

