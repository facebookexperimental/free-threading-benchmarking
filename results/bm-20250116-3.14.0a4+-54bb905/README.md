# Results

- fork: mpage/aa_test_0
- version: 3.14.0a4+
- config: 
- commit hash: [54bb905](https://github.com/mpage/cpython/commit/54bb905)
- commit date: 2025-01-16T11:46:12-08:00
- commit merge base: [211f41316b7f205d18eb65c1ececd7f7fb30b02d](https://github.com/python/cpython/commit/211f41316b7f205d18eb65c1ececd7f7fb30b02d)
- ref: aa_test_0

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12816541437)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20250116-vultr-x86_64-mpage-aa_test_0-3.14.0a4%2B-54bb905.json)

### vs. 3.12.6

- Geometric mean: 1.080x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250116-vultr-x86_64-mpage-aa_test_0-3.14.0a4%2B-54bb905-vs-3.12.6.md)
- [📈time plot](bm-20250116-vultr-x86_64-mpage-aa_test_0-3.14.0a4%2B-54bb905-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.042x faster (HPT: reliability of 99.98%, 1.00x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250116-vultr-x86_64-mpage-aa_test_0-3.14.0a4%2B-54bb905-vs-3.13.0rc2.md)
- [📈time plot](bm-20250116-vultr-x86_64-mpage-aa_test_0-3.14.0a4%2B-54bb905-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.007x slower (HPT: reliability of 99.89%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250116-vultr-x86_64-mpage-aa_test_0-3.14.0a4%2B-54bb905-vs-base-mem.svg)
- [📄table](bm-20250116-vultr-x86_64-mpage-aa_test_0-3.14.0a4%2B-54bb905-vs-base.md)
- [📈time plot](bm-20250116-vultr-x86_64-mpage-aa_test_0-3.14.0a4%2B-54bb905-vs-base.svg)

