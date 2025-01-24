# Results

- fork: nascheme/7f51104490216a377c74
- version: 3.14.0a4+
- config: NOGIL
- commit hash: [7f51104](https://github.com/nascheme/cpython/commit/7f51104)
- commit date: 2025-01-23T22:58:55-08:00
- commit merge base: [3829104ab412a47bf3f36b8c133c886d2cc9a6d4](https://github.com/python/cpython/commit/3829104ab412a47bf3f36b8c133c886d2cc9a6d4)
- ref: 7f51104490216a377c74

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12945841469)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250123-vultr-x86_64-nascheme-7f51104490216a377c74-3.14.0a4%2B-7f51104.json)

### vs. 3.12.6

- Geometric mean: 1.056x slower (HPT: reliability of 99.97%, 1.03x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list, xml_etree_generate, xml_etree_iterparse, xml_etree_parse, xml_etree_process
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250123-vultr-x86_64-nascheme-7f51104490216a377c74-3.14.0a4%2B-7f51104-vs-3.12.6.md)
- [📈time plot](bm-20250123-vultr-x86_64-nascheme-7f51104490216a377c74-3.14.0a4%2B-7f51104-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.087x slower (HPT: reliability of 99.99%, 1.05x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list, xml_etree_generate, xml_etree_iterparse, xml_etree_parse, xml_etree_process
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250123-vultr-x86_64-nascheme-7f51104490216a377c74-3.14.0a4%2B-7f51104-vs-3.13.0rc2.md)
- [📈time plot](bm-20250123-vultr-x86_64-nascheme-7f51104490216a377c74-3.14.0a4%2B-7f51104-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.006x faster (HPT: reliability of 100.00%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: 🔴 xml_etree_generate, xml_etree_iterparse, xml_etree_parse, xml_etree_process
- [🧠memory plot](bm-20250123-vultr-x86_64-nascheme-7f51104490216a377c74-3.14.0a4%2B-7f51104-vs-base-mem.svg)
- [📄table](bm-20250123-vultr-x86_64-nascheme-7f51104490216a377c74-3.14.0a4%2B-7f51104-vs-base.md)
- [📈time plot](bm-20250123-vultr-x86_64-nascheme-7f51104490216a377c74-3.14.0a4%2B-7f51104-vs-base.svg)

