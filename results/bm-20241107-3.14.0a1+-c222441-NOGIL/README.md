# Results

- fork: python/c222441fa7f89d448e47
- version: 3.14.0a1+
- config: NOGIL
- commit hash: [c222441](https://github.com/python/cpython/commit/c222441)
- commit date: 2024-11-07T23:03:11+00:00
- commit merge base: [bbe9b21d06c192a616bc1720ec8f7d4ccc16cab8](https://github.com/python/cpython/commit/bbe9b21d06c192a616bc1720ec8f7d4ccc16cab8)
- ref: c222441fa7f89d448e47

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11733653393)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20241107-linux-x86_64-python-c222441fa7f89d448e47-3.14.0a1%2B-c222441.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.31x slower at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- [📄table](bm-20241107-linux-x86_64-python-c222441fa7f89d448e47-3.14.0a1%2B-c222441-vs-3.12.6.md)
- [📈time plot](bm-20241107-linux-x86_64-python-c222441fa7f89d448e47-3.14.0a1%2B-c222441-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.34x slower at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http
- [📄table](bm-20241107-linux-x86_64-python-c222441fa7f89d448e47-3.14.0a1%2B-c222441-vs-3.13.0rc2.md)
- [📈time plot](bm-20241107-linux-x86_64-python-c222441fa7f89d448e47-3.14.0a1%2B-c222441-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.35x slower at 99th %ile)
- Memory usage: 1.17x
- [🧠memory plot](bm-20241107-linux-x86_64-python-c222441fa7f89d448e47-3.14.0a1%2B-c222441-vs-base-mem.svg)
- [📄table](bm-20241107-linux-x86_64-python-c222441fa7f89d448e47-3.14.0a1%2B-c222441-vs-base.md)
- [📈time plot](bm-20241107-linux-x86_64-python-c222441fa7f89d448e47-3.14.0a1%2B-c222441-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11733653393)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241107-vultr-x86_64-python-c222441fa7f89d448e47-3.14.0a1%2B-c222441.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.39x slower at 99th %ile)
- Memory usage: 1.23x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- [📄table](bm-20241107-vultr-x86_64-python-c222441fa7f89d448e47-3.14.0a1%2B-c222441-vs-3.12.6.md)
- [📈time plot](bm-20241107-vultr-x86_64-python-c222441fa7f89d448e47-3.14.0a1%2B-c222441-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.41x slower at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http
- [📄table](bm-20241107-vultr-x86_64-python-c222441fa7f89d448e47-3.14.0a1%2B-c222441-vs-3.13.0rc2.md)
- [📈time plot](bm-20241107-vultr-x86_64-python-c222441fa7f89d448e47-3.14.0a1%2B-c222441-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.40x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20241107-vultr-x86_64-python-c222441fa7f89d448e47-3.14.0a1%2B-c222441-vs-base-mem.svg)
- [📄table](bm-20241107-vultr-x86_64-python-c222441fa7f89d448e47-3.14.0a1%2B-c222441-vs-base.md)
- [📈time plot](bm-20241107-vultr-x86_64-python-c222441fa7f89d448e47-3.14.0a1%2B-c222441-vs-base.svg)

