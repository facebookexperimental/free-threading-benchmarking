# Results

- fork: faster-cpython/use_stackrefs
- version: 3.14.0a5+
- config: NOGIL
- commit hash: [e2f1387](https://github.com/faster%2dcpython/cpython/commit/e2f1387)
- commit date: 2025-03-03T15:16:22+00:00
- commit merge base: [b3c18bfd828ba90b9c712da74095c4a052887655](https://github.com/python/cpython/commit/b3c18bfd828ba90b9c712da74095c4a052887655)
- ref: use_stackrefs

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13637467049)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250303-vultr-x86_64-faster%252dcpython-use_stackrefs-3.14.0a5%2B-e2f1387.json)

### vs. 3.12.6

- Geometric mean: 1.043x slower (HPT: reliability of 100.00%, 1.03x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250303-vultr-x86_64-faster%252dcpython-use_stackrefs-3.14.0a5%2B-e2f1387-vs-3.12.6.md)
- [📈time plot](bm-20250303-vultr-x86_64-faster%252dcpython-use_stackrefs-3.14.0a5%2B-e2f1387-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.075x slower (HPT: reliability of 99.99%, 1.05x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250303-vultr-x86_64-faster%252dcpython-use_stackrefs-3.14.0a5%2B-e2f1387-vs-3.13.0rc2.md)
- [📈time plot](bm-20250303-vultr-x86_64-faster%252dcpython-use_stackrefs-3.14.0a5%2B-e2f1387-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.000x slower (HPT: reliability of 76.19%, 1.00x slower at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20250303-vultr-x86_64-faster%252dcpython-use_stackrefs-3.14.0a5%2B-e2f1387-vs-base-mem.svg)
- [📄table](bm-20250303-vultr-x86_64-faster%252dcpython-use_stackrefs-3.14.0a5%2B-e2f1387-vs-base.md)
- [📈time plot](bm-20250303-vultr-x86_64-faster%252dcpython-use_stackrefs-3.14.0a5%2B-e2f1387-vs-base.svg)

