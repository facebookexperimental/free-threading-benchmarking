# Results

- fork: Yhg1s/more_spec
- version: 3.14.0a4+
- config: NOGIL
- commit hash: [c92089c](https://github.com/Yhg1s/cpython/commit/c92089c)
- commit date: 2025-01-27T17:18:29+01:00
- commit merge base: [a5075cd5bd0307d9c19a0e0d6fcf4b7ad3d5a915](https://github.com/python/cpython/commit/a5075cd5bd0307d9c19a0e0d6fcf4b7ad3d5a915)
- ref: more_spec

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12993576813)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250127-vultr-x86_64-Yhg1s-more_spec-3.14.0a4%2B-c92089c.json)

### vs. 3.12.6

- Geometric mean: 1.062x slower (HPT: reliability of 100.00%, 1.04x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250127-vultr-x86_64-Yhg1s-more_spec-3.14.0a4%2B-c92089c-vs-3.12.6.md)
- [📈time plot](bm-20250127-vultr-x86_64-Yhg1s-more_spec-3.14.0a4%2B-c92089c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.092x slower (HPT: reliability of 99.99%, 1.06x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250127-vultr-x86_64-Yhg1s-more_spec-3.14.0a4%2B-c92089c-vs-3.13.0rc2.md)
- [📈time plot](bm-20250127-vultr-x86_64-Yhg1s-more_spec-3.14.0a4%2B-c92089c-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.009x faster (HPT: reliability of 100.00%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250127-vultr-x86_64-Yhg1s-more_spec-3.14.0a4%2B-c92089c-vs-base-mem.svg)
- [📄table](bm-20250127-vultr-x86_64-Yhg1s-more_spec-3.14.0a4%2B-c92089c-vs-base.md)
- [📈time plot](bm-20250127-vultr-x86_64-Yhg1s-more_spec-3.14.0a4%2B-c92089c-vs-base.svg)

