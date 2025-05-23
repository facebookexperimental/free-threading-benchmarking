# Results

- fork: mpage/aa_test_2
- version: 3.14.0a4+
- config: 
- commit hash: [f1b75b3](https://github.com/mpage/cpython/commit/f1b75b3)
- commit date: 2025-01-16T11:51:21-08:00
- commit merge base: [3893a92d956363fa2443bc5e47d4bae3deddacef](https://github.com/python/cpython/commit/3893a92d956363fa2443bc5e47d4bae3deddacef)
- ref: aa_test_2

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12816549528)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20250116-vultr-x86_64-mpage-aa_test_2-3.14.0a4%2B-f1b75b3.json)

### vs. 3.12.6

- Geometric mean: 1.084x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250116-vultr-x86_64-mpage-aa_test_2-3.14.0a4%2B-f1b75b3-vs-3.12.6.md)
- [📈time plot](bm-20250116-vultr-x86_64-mpage-aa_test_2-3.14.0a4%2B-f1b75b3-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.046x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250116-vultr-x86_64-mpage-aa_test_2-3.14.0a4%2B-f1b75b3-vs-3.13.0rc2.md)
- [📈time plot](bm-20250116-vultr-x86_64-mpage-aa_test_2-3.14.0a4%2B-f1b75b3-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.013x slower (HPT: reliability of 100.00%, 1.00x slower at 99th %ile)
- Memory usage: 0.99x
- [🧠memory plot](bm-20250116-vultr-x86_64-mpage-aa_test_2-3.14.0a4%2B-f1b75b3-vs-base-mem.svg)
- [📄table](bm-20250116-vultr-x86_64-mpage-aa_test_2-3.14.0a4%2B-f1b75b3-vs-base.md)
- [📈time plot](bm-20250116-vultr-x86_64-mpage-aa_test_2-3.14.0a4%2B-f1b75b3-vs-base.svg)

