# Results

- fork: Yhg1s/bb495b05f9c1a3d5224b
- version: 3.14.0a3+
- config: NOGIL
- commit hash: [bb495b0](https://github.com/Yhg1s/cpython/commit/bb495b0)
- commit date: 2025-01-21T16:05:24+01:00
- commit merge base: [7dc41ad6a7826ffc675f088972de96624917696e](https://github.com/python/cpython/commit/7dc41ad6a7826ffc675f088972de96624917696e)
- ref: bb495b05f9c1a3d5224b

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12889916385)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20250121-vultr-x86_64-Yhg1s-bb495b05f9c1a3d5224b-3.14.0a3%2B-bb495b0.json)

### vs. 3.12.6

- Geometric mean: 1.166x slower (HPT: reliability of 100.00%, 1.12x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250121-vultr-x86_64-Yhg1s-bb495b05f9c1a3d5224b-3.14.0a3%2B-bb495b0-vs-3.12.6.md)
- [📈time plot](bm-20250121-vultr-x86_64-Yhg1s-bb495b05f9c1a3d5224b-3.14.0a3%2B-bb495b0-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.193x slower (HPT: reliability of 100.00%, 1.15x slower at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250121-vultr-x86_64-Yhg1s-bb495b05f9c1a3d5224b-3.14.0a3%2B-bb495b0-vs-3.13.0rc2.md)
- [📈time plot](bm-20250121-vultr-x86_64-Yhg1s-bb495b05f9c1a3d5224b-3.14.0a3%2B-bb495b0-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.001x slower (HPT: reliability of 94.52%, 1.00x slower at 99th %ile)
- Memory usage: 1.04x
- [🧠memory plot](bm-20250121-vultr-x86_64-Yhg1s-bb495b05f9c1a3d5224b-3.14.0a3%2B-bb495b0-vs-base-mem.svg)
- [📄table](bm-20250121-vultr-x86_64-Yhg1s-bb495b05f9c1a3d5224b-3.14.0a3%2B-bb495b0-vs-base.md)
- [📈time plot](bm-20250121-vultr-x86_64-Yhg1s-bb495b05f9c1a3d5224b-3.14.0a3%2B-bb495b0-vs-base.svg)

