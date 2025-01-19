# Results

- fork: mpage/aa_test_3
- version: 3.14.0a4+
- config: 
- commit hash: [278858b](https://github.com/mpage/cpython/commit/278858b)
- commit date: 2025-01-18T14:29:44-08:00
- commit merge base: [61b35f74aa4a6ac606635e245147ff3658628d99](https://github.com/python/cpython/commit/61b35f74aa4a6ac606635e245147ff3658628d99)
- ref: aa_test_3

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12847968539)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20250118-vultr-x86_64-mpage-aa_test_3-3.14.0a4%2B-278858b.json)

### vs. 3.12.6

- Geometric mean: 1.083x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250118-vultr-x86_64-mpage-aa_test_3-3.14.0a4%2B-278858b-vs-3.12.6.md)
- [📈time plot](bm-20250118-vultr-x86_64-mpage-aa_test_3-3.14.0a4%2B-278858b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.044x faster (HPT: reliability of 99.99%, 1.00x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250118-vultr-x86_64-mpage-aa_test_3-3.14.0a4%2B-278858b-vs-3.13.0rc2.md)
- [📈time plot](bm-20250118-vultr-x86_64-mpage-aa_test_3-3.14.0a4%2B-278858b-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.007x slower (HPT: reliability of 100.00%, 1.00x slower at 99th %ile)
- Memory usage: 0.98x
- [🧠memory plot](bm-20250118-vultr-x86_64-mpage-aa_test_3-3.14.0a4%2B-278858b-vs-base-mem.svg)
- [📄table](bm-20250118-vultr-x86_64-mpage-aa_test_3-3.14.0a4%2B-278858b-vs-base.md)
- [📈time plot](bm-20250118-vultr-x86_64-mpage-aa_test_3-3.14.0a4%2B-278858b-vs-base.svg)

