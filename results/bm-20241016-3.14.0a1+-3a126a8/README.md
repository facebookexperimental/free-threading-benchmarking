# Results

- fork: colesbury
- version: 3.14.0a1+
- config: 
- commit hash: [3a126a8](https://github.com/colesbury/cpython/commit/3a126a8)
- commit date: 2024-10-16T19:41:13+00:00
- commit merge base: [760872efecb95017db8e38a8eda614bf23d2a22c](https://github.com/colesbury/cpython/commit/760872efecb95017db8e38a8eda614bf23d2a22c)
- ref: gh_125610_STORE_ATTR

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11410719615)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [pystats raw](bm-20241016-vultr-x86_64-colesbury-gh_125610_STORE_ATTR-3.14.0a1%2B-3a126a8-pystats.json)
- [pystats table](bm-20241016-vultr-x86_64-colesbury-gh_125610_STORE_ATTR-3.14.0a1%2B-3a126a8-pystats.md)
- [raw results](bm-20241016-vultr-x86_64-colesbury-gh_125610_STORE_ATTR-3.14.0a1%2B-3a126a8.json)

### vs. 3.12.6

- Geometric mean: 1.00x faster (HPT: reliability of 99.29%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20241016-vultr-x86_64-colesbury-gh_125610_STORE_ATTR-3.14.0a1%2B-3a126a8-vs-3.12.6.md)
- [📈time plot](bm-20241016-vultr-x86_64-colesbury-gh_125610_STORE_ATTR-3.14.0a1%2B-3a126a8-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.01x slower (HPT: reliability of 64.44%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn
- [📄table](bm-20241016-vultr-x86_64-colesbury-gh_125610_STORE_ATTR-3.14.0a1%2B-3a126a8-vs-3.13.0rc2.md)
- [📈time plot](bm-20241016-vultr-x86_64-colesbury-gh_125610_STORE_ATTR-3.14.0a1%2B-3a126a8-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.00x slower (HPT: reliability of 98.84%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [pystats diff](bm-20241016-vultr-x86_64-colesbury-gh_125610_STORE_ATTR-3.14.0a1%2B-3a126a8-pystats-vs-base.md)
- [🧠memory plot](bm-20241016-vultr-x86_64-colesbury-gh_125610_STORE_ATTR-3.14.0a1%2B-3a126a8-vs-base-mem.svg)
- [📄table](bm-20241016-vultr-x86_64-colesbury-gh_125610_STORE_ATTR-3.14.0a1%2B-3a126a8-vs-base.md)
- [📈time plot](bm-20241016-vultr-x86_64-colesbury-gh_125610_STORE_ATTR-3.14.0a1%2B-3a126a8-vs-base.svg)

