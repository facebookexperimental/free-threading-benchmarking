# Results

- fork: python/2ed5ee9a50454b3fce87
- version: 3.14.0a4+
- config: 
- commit hash: [2ed5ee9](https://github.com/python/cpython/commit/2ed5ee9)
- commit date: 2025-01-22T13:52:45+00:00
- commit merge base: [8e20e42cc63321dacc500d7670bfc225ca04e78b](https://github.com/python/cpython/commit/8e20e42cc63321dacc500d7670bfc225ca04e78b)
- ref: 2ed5ee9a50454b3fce87

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12914801800)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250122-vultr-x86_64-python-2ed5ee9a50454b3fce87-3.14.0a4%2B-2ed5ee9.json)

### vs. 3.12.6

- Geometric mean: 1.084x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250122-vultr-x86_64-python-2ed5ee9a50454b3fce87-3.14.0a4%2B-2ed5ee9-vs-3.12.6.md)
- [📈time plot](bm-20250122-vultr-x86_64-python-2ed5ee9a50454b3fce87-3.14.0a4%2B-2ed5ee9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.047x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250122-vultr-x86_64-python-2ed5ee9a50454b3fce87-3.14.0a4%2B-2ed5ee9-vs-3.13.0rc2.md)
- [📈time plot](bm-20250122-vultr-x86_64-python-2ed5ee9a50454b3fce87-3.14.0a4%2B-2ed5ee9-vs-3.13.0rc2.svg)

