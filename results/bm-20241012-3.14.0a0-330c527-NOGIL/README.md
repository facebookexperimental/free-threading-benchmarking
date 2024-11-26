# Results

- fork: python
- version: 3.14.0a0
- config: NOGIL
- commit hash: [330c527](https://github.com/python/cpython/commit/330c527)
- commit date: 2024-10-12T13:57:27-07:00
- commit merge base: [fa52b82c91a8e1a0971bd5fef656473ec93f41e3](https://github.com/python/cpython/commit/fa52b82c91a8e1a0971bd5fef656473ec93f41e3)
- ref: 330c527299a5380f39c6

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11309795576)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241012-vultr-x86_64-python-330c527299a5380f39c6-3.14.0a0-330c527.json)

### vs. 3.12.6

- Geometric mean: 1.351x slower (HPT: reliability of 100.00%, 1.39x slower at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20241012-vultr-x86_64-python-330c527299a5380f39c6-3.14.0a0-330c527-vs-3.12.6.md)
- [📈time plot](bm-20241012-vultr-x86_64-python-330c527299a5380f39c6-3.14.0a0-330c527-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.361x slower (HPT: reliability of 100.00%, 1.41x slower at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn
- [📄table](bm-20241012-vultr-x86_64-python-330c527299a5380f39c6-3.14.0a0-330c527-vs-3.13.0rc2.md)
- [📈time plot](bm-20241012-vultr-x86_64-python-330c527299a5380f39c6-3.14.0a0-330c527-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.363x slower (HPT: reliability of 100.00%, 1.41x slower at 99th %ile)
- Memory usage: 1.17x
- [🧠memory plot](bm-20241012-vultr-x86_64-python-330c527299a5380f39c6-3.14.0a0-330c527-vs-base-mem.svg)
- [📄table](bm-20241012-vultr-x86_64-python-330c527299a5380f39c6-3.14.0a0-330c527-vs-base.md)
- [📈time plot](bm-20241012-vultr-x86_64-python-330c527299a5380f39c6-3.14.0a0-330c527-vs-base.svg)

