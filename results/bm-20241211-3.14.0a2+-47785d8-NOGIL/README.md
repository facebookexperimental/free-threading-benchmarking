# Results

- fork: Yhg1s/compare_op
- version: 3.14.0a2+
- config: NOGIL
- commit hash: [47785d8](https://github.com/Yhg1s/cpython/commit/47785d8)
- commit date: 2024-12-11T15:13:24+01:00
- commit merge base: [359389ed51aecc107681e600b71852c0a97304e1](https://github.com/python/cpython/commit/359389ed51aecc107681e600b71852c0a97304e1)
- ref: compare_op

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12289005269)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2%2B-47785d8.json)

### vs. 3.12.6

- Geometric mean: 1.218x slower (HPT: reliability of 100.00%, 1.17x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2%2B-47785d8-vs-3.12.6.md)
- [📈time plot](bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2%2B-47785d8-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.243x slower (HPT: reliability of 100.00%, 1.18x slower at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2%2B-47785d8-vs-3.13.0rc2.md)
- [📈time plot](bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2%2B-47785d8-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.006x faster (HPT: reliability of 99.80%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2%2B-47785d8-vs-base-mem.svg)
- [📄table](bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2%2B-47785d8-vs-base.md)
- [📈time plot](bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2%2B-47785d8-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.272x slower (HPT: reliability of 100.00%, 1.27x slower at 99th %ile)
- Memory usage: 1.19x
- new benchmarks: html5lib
- [📄table](bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2%2B-47785d8-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2%2B-47785d8-vs-default_base_vs_NOGIL.svg)

