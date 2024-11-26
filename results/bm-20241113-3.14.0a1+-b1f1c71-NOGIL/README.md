# Results

- fork: corona10
- version: 3.14.0a1+
- config: NOGIL
- commit hash: [b1f1c71](https://github.com/corona10/cpython/commit/b1f1c71)
- commit date: 2024-11-13T00:01:14+09:00
- commit merge base: [6293d00e7201f3f28b1f4512e57dc4f03855cabd](https://github.com/corona10/cpython/commit/6293d00e7201f3f28b1f4512e57dc4f03855cabd)
- ref: gh_115999_bool

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11822600446)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241113-vultr-x86_64-corona10-gh_115999_bool-3.14.0a1%2B-b1f1c71.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.38x slower at 99th %ile)
- Memory usage: 1.23x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- [📄table](bm-20241113-vultr-x86_64-corona10-gh_115999_bool-3.14.0a1%2B-b1f1c71-vs-3.12.6.md)
- [📈time plot](bm-20241113-vultr-x86_64-corona10-gh_115999_bool-3.14.0a1%2B-b1f1c71-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.40x slower at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http
- [📄table](bm-20241113-vultr-x86_64-corona10-gh_115999_bool-3.14.0a1%2B-b1f1c71-vs-3.13.0rc2.md)
- [📈time plot](bm-20241113-vultr-x86_64-corona10-gh_115999_bool-3.14.0a1%2B-b1f1c71-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20241113-vultr-x86_64-corona10-gh_115999_bool-3.14.0a1%2B-b1f1c71-vs-base-mem.svg)
- [📄table](bm-20241113-vultr-x86_64-corona10-gh_115999_bool-3.14.0a1%2B-b1f1c71-vs-base.md)
- [📈time plot](bm-20241113-vultr-x86_64-corona10-gh_115999_bool-3.14.0a1%2B-b1f1c71-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.40x slower at 99th %ile)
- Memory usage: 1.20x
- [📄table](bm-20241113-vultr-x86_64-corona10-gh_115999_bool-3.14.0a1%2B-b1f1c71-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20241113-vultr-x86_64-corona10-gh_115999_bool-3.14.0a1%2B-b1f1c71-vs-default_base_vs_NOGIL.svg)

