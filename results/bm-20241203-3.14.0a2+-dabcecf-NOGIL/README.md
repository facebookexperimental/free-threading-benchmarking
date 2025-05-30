# Results

- fork: python/dabcecfd6dadb9430733
- version: 3.14.0a2+
- config: NOGIL
- commit hash: [dabcecf](https://github.com/python/cpython/commit/dabcecf)
- commit date: 2024-12-03T11:20:20-08:00
- commit merge base: [fc5a0dc22483a35068888e828c65796d7a792c14](https://github.com/python/cpython/commit/fc5a0dc22483a35068888e828c65796d7a792c14)
- ref: dabcecfd6dadb9430733

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12150668256)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241203-vultr-x86_64-python-dabcecfd6dadb9430733-3.14.0a2%2B-dabcecf.json)

### vs. 3.12.6

- Geometric mean: 1.231x slower (HPT: reliability of 100.00%, 1.18x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241203-vultr-x86_64-python-dabcecfd6dadb9430733-3.14.0a2%2B-dabcecf-vs-3.12.6.md)
- [📈time plot](bm-20241203-vultr-x86_64-python-dabcecfd6dadb9430733-3.14.0a2%2B-dabcecf-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.256x slower (HPT: reliability of 100.00%, 1.20x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241203-vultr-x86_64-python-dabcecfd6dadb9430733-3.14.0a2%2B-dabcecf-vs-3.13.0rc2.md)
- [📈time plot](bm-20241203-vultr-x86_64-python-dabcecfd6dadb9430733-3.14.0a2%2B-dabcecf-vs-3.13.0rc2.svg)

