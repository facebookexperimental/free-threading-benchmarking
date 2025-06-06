# Results

- fork: python/c9932a9ec8a3077933a8
- version: 3.14.0a5+
- config: NOGIL
- commit hash: [c9932a9](https://github.com/python/cpython/commit/c9932a9)
- commit date: 2025-03-01T21:25:38+00:00
- commit merge base: [a55dffd66dbddfd50c8f3de195218d041d26bd3c](https://github.com/python/cpython/commit/a55dffd66dbddfd50c8f3de195218d041d26bd3c)
- ref: c9932a9ec8a3077933a8

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13610155202)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250301-vultr-x86_64-python-c9932a9ec8a3077933a8-3.14.0a5%2B-c9932a9.json)

### vs. 3.12.6

- Geometric mean: 1.046x slower (HPT: reliability of 99.99%, 1.03x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250301-vultr-x86_64-python-c9932a9ec8a3077933a8-3.14.0a5%2B-c9932a9-vs-3.12.6.md)
- [📈time plot](bm-20250301-vultr-x86_64-python-c9932a9ec8a3077933a8-3.14.0a5%2B-c9932a9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.078x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250301-vultr-x86_64-python-c9932a9ec8a3077933a8-3.14.0a5%2B-c9932a9-vs-3.13.0rc2.md)
- [📈time plot](bm-20250301-vultr-x86_64-python-c9932a9ec8a3077933a8-3.14.0a5%2B-c9932a9-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.126x slower (HPT: reliability of 100.00%, 1.12x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250301-vultr-x86_64-python-c9932a9ec8a3077933a8-3.14.0a5%2B-c9932a9-vs-base-mem.svg)
- [📄table](bm-20250301-vultr-x86_64-python-c9932a9ec8a3077933a8-3.14.0a5%2B-c9932a9-vs-base.md)
- [📈time plot](bm-20250301-vultr-x86_64-python-c9932a9ec8a3077933a8-3.14.0a5%2B-c9932a9-vs-base.svg)

