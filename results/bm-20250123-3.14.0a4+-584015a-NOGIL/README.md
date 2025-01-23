# Results

- fork: faster-cpython/remove_most_conditio
- version: 3.14.0a4+
- config: NOGIL
- commit hash: [584015a](https://github.com/faster%2dcpython/cpython/commit/584015a)
- commit date: 2025-01-23T14:48:17+00:00
- commit merge base: [a10f99375e7912df863cf101a38e9703cfcd72f1](https://github.com/python/cpython/commit/a10f99375e7912df863cf101a38e9703cfcd72f1)
- ref: remove_most_conditio

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12933465070)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250123-vultr-x86_64-faster%252dcpython-remove_most_conditio-3.14.0a4%2B-584015a.json)

### vs. 3.12.6

- Geometric mean: 1.057x slower (HPT: reliability of 99.97%, 1.03x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250123-vultr-x86_64-faster%252dcpython-remove_most_conditio-3.14.0a4%2B-584015a-vs-3.12.6.md)
- [📈time plot](bm-20250123-vultr-x86_64-faster%252dcpython-remove_most_conditio-3.14.0a4%2B-584015a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.087x slower (HPT: reliability of 99.99%, 1.05x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250123-vultr-x86_64-faster%252dcpython-remove_most_conditio-3.14.0a4%2B-584015a-vs-3.13.0rc2.md)
- [📈time plot](bm-20250123-vultr-x86_64-faster%252dcpython-remove_most_conditio-3.14.0a4%2B-584015a-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.006x faster (HPT: reliability of 99.90%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250123-vultr-x86_64-faster%252dcpython-remove_most_conditio-3.14.0a4%2B-584015a-vs-base-mem.svg)
- [📄table](bm-20250123-vultr-x86_64-faster%252dcpython-remove_most_conditio-3.14.0a4%2B-584015a-vs-base.md)
- [📈time plot](bm-20250123-vultr-x86_64-faster%252dcpython-remove_most_conditio-3.14.0a4%2B-584015a-vs-base.svg)

