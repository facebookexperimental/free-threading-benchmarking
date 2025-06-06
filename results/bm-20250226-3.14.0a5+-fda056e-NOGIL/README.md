# Results

- fork: python/fda056e64bdfcac3dd3d
- version: 3.14.0a5+
- config: NOGIL
- commit hash: [fda056e](https://github.com/python/cpython/commit/fda056e)
- commit date: 2025-02-26T21:44:48+00:00
- commit merge base: [959f43315e165a868888808d30025785d4ae3e7c](https://github.com/python/cpython/commit/959f43315e165a868888808d30025785d4ae3e7c)
- ref: fda056e64bdfcac3dd3d

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13556088922)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5%2B-fda056e.json)

### vs. 3.12.6

- Geometric mean: 1.042x slower (HPT: reliability of 99.99%, 1.03x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5%2B-fda056e-vs-3.12.6.md)
- [📈time plot](bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5%2B-fda056e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.074x slower (HPT: reliability of 99.99%, 1.04x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5%2B-fda056e-vs-3.13.0rc2.md)
- [📈time plot](bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5%2B-fda056e-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.130x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5%2B-fda056e-vs-base-mem.svg)
- [📄table](bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5%2B-fda056e-vs-base.md)
- [📈time plot](bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5%2B-fda056e-vs-base.svg)

