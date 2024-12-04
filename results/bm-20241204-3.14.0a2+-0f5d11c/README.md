# Results

- fork: mpage
- version: 3.14.0a2+
- config: 
- commit hash: [0f5d11c](https://github.com/mpage/cpython/commit/0f5d11c)
- commit date: 2024-12-04T09:51:58-08:00
- commit merge base: [bfb0788bfcaab7474c1be0605552744e15082ee9](https://github.com/mpage/cpython/commit/bfb0788bfcaab7474c1be0605552744e15082ee9)
- ref: measure_gc_changes

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12165513391)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241204-vultr-x86_64-mpage-measure_gc_changes-3.14.0a2%2B-0f5d11c.json)

### vs. 3.12.6

- Geometric mean: 1.040x faster (HPT: reliability of 99.85%, 1.00x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241204-vultr-x86_64-mpage-measure_gc_changes-3.14.0a2%2B-0f5d11c-vs-3.12.6.md)
- [📈time plot](bm-20241204-vultr-x86_64-mpage-measure_gc_changes-3.14.0a2%2B-0f5d11c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.002x faster (HPT: reliability of 54.52%, 1.00x slower at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241204-vultr-x86_64-mpage-measure_gc_changes-3.14.0a2%2B-0f5d11c-vs-3.13.0rc2.md)
- [📈time plot](bm-20241204-vultr-x86_64-mpage-measure_gc_changes-3.14.0a2%2B-0f5d11c-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.019x slower (HPT: reliability of 74.19%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20241204-vultr-x86_64-mpage-measure_gc_changes-3.14.0a2%2B-0f5d11c-vs-base-mem.svg)
- [📄table](bm-20241204-vultr-x86_64-mpage-measure_gc_changes-3.14.0a2%2B-0f5d11c-vs-base.md)
- [📈time plot](bm-20241204-vultr-x86_64-mpage-measure_gc_changes-3.14.0a2%2B-0f5d11c-vs-base.svg)

