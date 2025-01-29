# Results

- fork: colesbury/gh_128563_revert
- version: 3.14.0a4+
- config: NOGIL
- commit hash: [8014514](https://github.com/colesbury/cpython/commit/8014514)
- commit date: 2025-01-29T18:37:46+00:00
- commit merge base: [99ed3025fe8fa9079b4c1eac01c5af62caa98c15](https://github.com/python/cpython/commit/99ed3025fe8fa9079b4c1eac01c5af62caa98c15)
- ref: gh_128563_revert

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13038129843)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250129-vultr-x86_64-colesbury-gh_128563_revert-3.14.0a4%2B-8014514.json)

### vs. 3.12.6

- Geometric mean: 1.042x slower (HPT: reliability of 99.95%, 1.02x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250129-vultr-x86_64-colesbury-gh_128563_revert-3.14.0a4%2B-8014514-vs-3.12.6.md)
- [📈time plot](bm-20250129-vultr-x86_64-colesbury-gh_128563_revert-3.14.0a4%2B-8014514-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.073x slower (HPT: reliability of 99.97%, 1.04x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250129-vultr-x86_64-colesbury-gh_128563_revert-3.14.0a4%2B-8014514-vs-3.13.0rc2.md)
- [📈time plot](bm-20250129-vultr-x86_64-colesbury-gh_128563_revert-3.14.0a4%2B-8014514-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.002x faster (HPT: reliability of 53.41%, 1.00x faster at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20250129-vultr-x86_64-colesbury-gh_128563_revert-3.14.0a4%2B-8014514-vs-base-mem.svg)
- [📄table](bm-20250129-vultr-x86_64-colesbury-gh_128563_revert-3.14.0a4%2B-8014514-vs-base.md)
- [📈time plot](bm-20250129-vultr-x86_64-colesbury-gh_128563_revert-3.14.0a4%2B-8014514-vs-base.svg)

