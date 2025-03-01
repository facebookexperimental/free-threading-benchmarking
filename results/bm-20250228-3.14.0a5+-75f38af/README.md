# Results

- fork: python/75f38af7810af1c3ca56
- version: 3.14.0a5+
- config: 
- commit hash: [75f38af](https://github.com/python/cpython/commit/75f38af)
- commit date: 2025-02-28T16:57:48-05:00
- commit merge base: [da4899b94a9a9083fed4972b2473546e0d997727](https://github.com/python/cpython/commit/da4899b94a9a9083fed4972b2473546e0d997727)
- ref: 75f38af7810af1c3ca56

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13598883760)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250228-linux-x86_64-python-75f38af7810af1c3ca56-3.14.0a5%2B-75f38af.json)

### vs. 3.12.6

- Geometric mean: 1.120x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250228-linux-x86_64-python-75f38af7810af1c3ca56-3.14.0a5%2B-75f38af-vs-3.12.6.md)
- [📈time plot](bm-20250228-linux-x86_64-python-75f38af7810af1c3ca56-3.14.0a5%2B-75f38af-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.077x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250228-linux-x86_64-python-75f38af7810af1c3ca56-3.14.0a5%2B-75f38af-vs-3.13.0rc2.md)
- [📈time plot](bm-20250228-linux-x86_64-python-75f38af7810af1c3ca56-3.14.0a5%2B-75f38af-vs-3.13.0rc2.svg)

