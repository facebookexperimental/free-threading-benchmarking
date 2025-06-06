# Results

- fork: python/cf4c4ecc26c7e3b89f2e
- version: 3.14.0a4+
- config: 
- commit hash: [cf4c4ec](https://github.com/python/cpython/commit/cf4c4ec)
- commit date: 2025-02-01T18:49:45+02:00
- commit merge base: [71ae93374defd192e5e88fe0912eff4f8e56f286](https://github.com/python/cpython/commit/71ae93374defd192e5e88fe0912eff4f8e56f286)
- ref: cf4c4ecc26c7e3b89f2e

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13093724822)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4%2B-cf4c4ec.json)

### vs. 3.12.6

- Geometric mean: 1.104x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4%2B-cf4c4ec-vs-3.12.6.md)
- [📈time plot](bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4%2B-cf4c4ec-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.065x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, html5lib, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4%2B-cf4c4ec-vs-3.13.0rc2.md)
- [📈time plot](bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4%2B-cf4c4ec-vs-3.13.0rc2.svg)

