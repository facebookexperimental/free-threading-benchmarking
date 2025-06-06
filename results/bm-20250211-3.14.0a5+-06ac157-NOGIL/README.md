# Results

- fork: python/06ac157c53046f4fcad3
- version: 3.14.0a5+
- config: NOGIL
- commit hash: [06ac157](https://github.com/python/cpython/commit/06ac157)
- commit date: 2025-02-11T23:59:09+00:00
- commit merge base: [a7427f2db937adb4c787754deb4c337f1894fe86](https://github.com/python/cpython/commit/a7427f2db937adb4c787754deb4c337f1894fe86)
- ref: 06ac157c53046f4fcad3

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13275213571)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250211-vultr-x86_64-python-06ac157c53046f4fcad3-3.14.0a5%2B-06ac157.json)

### vs. 3.12.6

- Geometric mean: 1.046x slower (HPT: reliability of 99.95%, 1.02x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250211-vultr-x86_64-python-06ac157c53046f4fcad3-3.14.0a5%2B-06ac157-vs-3.12.6.md)
- [📈time plot](bm-20250211-vultr-x86_64-python-06ac157c53046f4fcad3-3.14.0a5%2B-06ac157-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.077x slower (HPT: reliability of 99.97%, 1.04x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250211-vultr-x86_64-python-06ac157c53046f4fcad3-3.14.0a5%2B-06ac157-vs-3.13.0rc2.md)
- [📈time plot](bm-20250211-vultr-x86_64-python-06ac157c53046f4fcad3-3.14.0a5%2B-06ac157-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.127x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20250211-vultr-x86_64-python-06ac157c53046f4fcad3-3.14.0a5%2B-06ac157-vs-base-mem.svg)
- [📄table](bm-20250211-vultr-x86_64-python-06ac157c53046f4fcad3-3.14.0a5%2B-06ac157-vs-base.md)
- [📈time plot](bm-20250211-vultr-x86_64-python-06ac157c53046f4fcad3-3.14.0a5%2B-06ac157-vs-base.svg)

