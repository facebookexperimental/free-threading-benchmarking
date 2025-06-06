# Results

- fork: python/0ef4ffeefd1737c18dc9
- version: 3.14.0a5+
- config: NOGIL
- commit hash: [0ef4ffe](https://github.com/python/cpython/commit/0ef4ffe)
- commit date: 2025-02-25T23:04:27+02:00
- commit merge base: [2dad1e08ec9d5ddc798a313900613b3d1eeaff6b](https://github.com/python/cpython/commit/2dad1e08ec9d5ddc798a313900613b3d1eeaff6b)
- ref: 0ef4ffeefd1737c18dc9

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13533710040)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5%2B-0ef4ffe.json)

### vs. 3.12.6

- Geometric mean: 1.046x slower (HPT: reliability of 99.99%, 1.03x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5%2B-0ef4ffe-vs-3.12.6.md)
- [📈time plot](bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5%2B-0ef4ffe-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.079x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5%2B-0ef4ffe-vs-3.13.0rc2.md)
- [📈time plot](bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5%2B-0ef4ffe-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.132x slower (HPT: reliability of 100.00%, 1.14x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5%2B-0ef4ffe-vs-base-mem.svg)
- [📄table](bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5%2B-0ef4ffe-vs-base.md)
- [📈time plot](bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5%2B-0ef4ffe-vs-base.svg)

