# Results

- fork: python/c5438fdf4706a70bdd19
- version: 3.14.0a3+
- config: 
- commit hash: [c5438fd](https://github.com/python/cpython/commit/c5438fd)
- commit date: 2024-12-31T23:22:33+02:00
- commit merge base: [e389d6c650ddacb55b08b657f1e4e9b1330f3455](https://github.com/python/cpython/commit/e389d6c650ddacb55b08b657f1e4e9b1330f3455)
- ref: c5438fdf4706a70bdd19

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12565348795)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241231-vultr-x86_64-python-c5438fdf4706a70bdd19-3.14.0a3%2B-c5438fd.json)

### vs. 3.12.6

- Geometric mean: 1.101x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241231-vultr-x86_64-python-c5438fdf4706a70bdd19-3.14.0a3%2B-c5438fd-vs-3.12.6.md)
- [📈time plot](bm-20241231-vultr-x86_64-python-c5438fdf4706a70bdd19-3.14.0a3%2B-c5438fd-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.062x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241231-vultr-x86_64-python-c5438fdf4706a70bdd19-3.14.0a3%2B-c5438fd-vs-3.13.0rc2.md)
- [📈time plot](bm-20241231-vultr-x86_64-python-c5438fdf4706a70bdd19-3.14.0a3%2B-c5438fd-vs-3.13.0rc2.svg)

