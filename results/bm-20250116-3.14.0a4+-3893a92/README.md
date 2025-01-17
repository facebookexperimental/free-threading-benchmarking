# Results

- fork: python/3893a92d956363fa2443
- version: 3.14.0a4+
- config: 
- commit hash: [3893a92](https://github.com/python/cpython/commit/3893a92)
- commit date: 2025-01-16T15:22:13+00:00
- commit merge base: [e81fe940c9bd092f6de558fa965100502b78da0f](https://github.com/python/cpython/commit/e81fe940c9bd092f6de558fa965100502b78da0f)
- ref: 3893a92d956363fa2443

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12816549528)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20250116-vultr-x86_64-python-3893a92d956363fa2443-3.14.0a4%2B-3893a92.json)

### vs. 3.12.6

- Geometric mean: 1.099x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250116-vultr-x86_64-python-3893a92d956363fa2443-3.14.0a4%2B-3893a92-vs-3.12.6.md)
- [📈time plot](bm-20250116-vultr-x86_64-python-3893a92d956363fa2443-3.14.0a4%2B-3893a92-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.060x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250116-vultr-x86_64-python-3893a92d956363fa2443-3.14.0a4%2B-3893a92-vs-3.13.0rc2.md)
- [📈time plot](bm-20250116-vultr-x86_64-python-3893a92d956363fa2443-3.14.0a4%2B-3893a92-vs-3.13.0rc2.svg)

