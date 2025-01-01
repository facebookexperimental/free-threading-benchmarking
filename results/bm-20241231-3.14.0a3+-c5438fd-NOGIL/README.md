# Results

- fork: python/c5438fdf4706a70bdd19
- version: 3.14.0a3+
- config: NOGIL
- commit hash: [c5438fd](https://github.com/python/cpython/commit/c5438fd)
- commit date: 2024-12-31T23:22:33+02:00
- commit merge base: [e389d6c650ddacb55b08b657f1e4e9b1330f3455](https://github.com/python/cpython/commit/e389d6c650ddacb55b08b657f1e4e9b1330f3455)
- ref: c5438fdf4706a70bdd19

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12565348795)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20241231-linux-x86_64-python-c5438fdf4706a70bdd19-3.14.0a3%2B-c5438fd.json)

### vs. 3.12.6

- Geometric mean: 1.104x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241231-linux-x86_64-python-c5438fdf4706a70bdd19-3.14.0a3%2B-c5438fd-vs-3.12.6.md)
- [📈time plot](bm-20241231-linux-x86_64-python-c5438fdf4706a70bdd19-3.14.0a3%2B-c5438fd-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.136x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241231-linux-x86_64-python-c5438fdf4706a70bdd19-3.14.0a3%2B-c5438fd-vs-3.13.0rc2.md)
- [📈time plot](bm-20241231-linux-x86_64-python-c5438fdf4706a70bdd19-3.14.0a3%2B-c5438fd-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.214x slower (HPT: reliability of 100.00%, 1.20x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20241231-linux-x86_64-python-c5438fdf4706a70bdd19-3.14.0a3%2B-c5438fd-vs-base-mem.svg)
- [📄table](bm-20241231-linux-x86_64-python-c5438fdf4706a70bdd19-3.14.0a3%2B-c5438fd-vs-base.md)
- [📈time plot](bm-20241231-linux-x86_64-python-c5438fdf4706a70bdd19-3.14.0a3%2B-c5438fd-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12565348795)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241231-vultr-x86_64-python-c5438fdf4706a70bdd19-3.14.0a3%2B-c5438fd.json)

### vs. 3.12.6

- Geometric mean: 1.174x slower (HPT: reliability of 100.00%, 1.14x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241231-vultr-x86_64-python-c5438fdf4706a70bdd19-3.14.0a3%2B-c5438fd-vs-3.12.6.md)
- [📈time plot](bm-20241231-vultr-x86_64-python-c5438fdf4706a70bdd19-3.14.0a3%2B-c5438fd-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.201x slower (HPT: reliability of 100.00%, 1.15x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241231-vultr-x86_64-python-c5438fdf4706a70bdd19-3.14.0a3%2B-c5438fd-vs-3.13.0rc2.md)
- [📈time plot](bm-20241231-vultr-x86_64-python-c5438fdf4706a70bdd19-3.14.0a3%2B-c5438fd-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.244x slower (HPT: reliability of 100.00%, 1.25x slower at 99th %ile)
- Memory usage: 1.19x
- new benchmarks: html5lib
- [🧠memory plot](bm-20241231-vultr-x86_64-python-c5438fdf4706a70bdd19-3.14.0a3%2B-c5438fd-vs-base-mem.svg)
- [📄table](bm-20241231-vultr-x86_64-python-c5438fdf4706a70bdd19-3.14.0a3%2B-c5438fd-vs-base.md)
- [📈time plot](bm-20241231-vultr-x86_64-python-c5438fdf4706a70bdd19-3.14.0a3%2B-c5438fd-vs-base.svg)

