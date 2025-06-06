# Results

- fork: python/b52de22ac345ad8583bc
- version: 3.14.0a4+
- config: NOGIL
- commit hash: [b52de22](https://github.com/python/cpython/commit/b52de22)
- commit date: 2025-01-15T01:17:11+02:00
- commit merge base: [f7ceb317aec498823555885a4b7fed5e0244f300](https://github.com/python/cpython/commit/f7ceb317aec498823555885a4b7fed5e0244f300)
- ref: b52de22ac345ad8583bc

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12778887140)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20250115-vultr-x86_64-python-b52de22ac345ad8583bc-3.14.0a4%2B-b52de22.json)

### vs. 3.12.6

- Geometric mean: 1.066x slower (HPT: reliability of 99.99%, 1.04x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250115-vultr-x86_64-python-b52de22ac345ad8583bc-3.14.0a4%2B-b52de22-vs-3.12.6.md)
- [📈time plot](bm-20250115-vultr-x86_64-python-b52de22ac345ad8583bc-3.14.0a4%2B-b52de22-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.096x slower (HPT: reliability of 99.99%, 1.06x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250115-vultr-x86_64-python-b52de22ac345ad8583bc-3.14.0a4%2B-b52de22-vs-3.13.0rc2.md)
- [📈time plot](bm-20250115-vultr-x86_64-python-b52de22ac345ad8583bc-3.14.0a4%2B-b52de22-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.156x slower (HPT: reliability of 100.00%, 1.14x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250115-vultr-x86_64-python-b52de22ac345ad8583bc-3.14.0a4%2B-b52de22-vs-base-mem.svg)
- [📄table](bm-20250115-vultr-x86_64-python-b52de22ac345ad8583bc-3.14.0a4%2B-b52de22-vs-base.md)
- [📈time plot](bm-20250115-vultr-x86_64-python-b52de22ac345ad8583bc-3.14.0a4%2B-b52de22-vs-base.svg)

