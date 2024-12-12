# Results

- fork: Yhg1s/compare_op
- version: 3.14.0a2+
- config: 
- commit hash: [47785d8](https://github.com/Yhg1s/cpython/commit/47785d8)
- commit date: 2024-12-11T15:13:24+01:00
- commit merge base: [359389ed51aecc107681e600b71852c0a97304e1](https://github.com/python/cpython/commit/359389ed51aecc107681e600b71852c0a97304e1)
- ref: compare_op

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12289007658)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2%2B-47785d8.json)

### vs. 3.12.6

- Geometric mean: 1.079x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2%2B-47785d8-vs-3.12.6.md)
- [📈time plot](bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2%2B-47785d8-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.040x faster (HPT: reliability of 100.00%, 1.00x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2%2B-47785d8-vs-3.13.0rc2.md)
- [📈time plot](bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2%2B-47785d8-vs-3.13.0rc2.svg)

