# Results

- fork: python/01bcf13a1c5bfca5124c
- version: 3.14.0a4+
- config: 
- commit hash: [01bcf13](https://github.com/python/cpython/commit/01bcf13)
- commit date: 2025-01-21T23:28:32+00:00
- commit merge base: [29caec62ee0650493c83c778ee2ea50b0501bc41](https://github.com/python/cpython/commit/29caec62ee0650493c83c778ee2ea50b0501bc41)
- fork: mpage/aa_test_6
- commit hash: [01bcf13](https://github.com/mpage/cpython/commit/01bcf13)
- ref: 01bcf13a1c5bfca5124c, aa_test_6

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12898483778)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4%2B-01bcf13.json)

### vs. 3.12.6

- Geometric mean: 1.048x faster (HPT: reliability of 98.46%, 1.00x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4%2B-01bcf13-vs-3.12.6.md)
- [📈time plot](bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4%2B-01bcf13-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.005x faster (HPT: reliability of 95.10%, 1.00x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4%2B-01bcf13-vs-3.13.0rc2.md)
- [📈time plot](bm-20250121-linux-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4%2B-01bcf13-vs-3.13.0rc2.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12898483778)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12903010477)
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250121-vultr-x86_64-mpage-aa_test_6-3.14.0a4%2B-01bcf13.json)
- [raw results](bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4%2B-01bcf13.json)

### vs. 3.12.6

- Geometric mean: 1.093x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- Geometric mean: 1.087x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- [📄table](bm-20250121-vultr-x86_64-mpage-aa_test_6-3.14.0a4%2B-01bcf13-vs-3.12.6.md)
- [📈time plot](bm-20250121-vultr-x86_64-mpage-aa_test_6-3.14.0a4%2B-01bcf13-vs-3.12.6.svg)
- [📄table](bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4%2B-01bcf13-vs-3.12.6.md)
- [📈time plot](bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4%2B-01bcf13-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.054x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- Geometric mean: 1.049x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- [📄table](bm-20250121-vultr-x86_64-mpage-aa_test_6-3.14.0a4%2B-01bcf13-vs-3.13.0rc2.md)
- [📈time plot](bm-20250121-vultr-x86_64-mpage-aa_test_6-3.14.0a4%2B-01bcf13-vs-3.13.0rc2.svg)
- [📄table](bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4%2B-01bcf13-vs-3.13.0rc2.md)
- [📈time plot](bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4%2B-01bcf13-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.002x slower (HPT: reliability of 83.49%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- Geometric mean: 1.006x slower (HPT: reliability of 100.00%, 1.00x slower at 99th %ile)
- [🧠memory plot](bm-20250121-vultr-x86_64-mpage-aa_test_6-3.14.0a4%2B-01bcf13-vs-base-mem.svg)
- [📄table](bm-20250121-vultr-x86_64-mpage-aa_test_6-3.14.0a4%2B-01bcf13-vs-base.md)
- [📈time plot](bm-20250121-vultr-x86_64-mpage-aa_test_6-3.14.0a4%2B-01bcf13-vs-base.svg)
- [🧠memory plot](bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4%2B-01bcf13-vs-base-mem.svg)
- [📄table](bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4%2B-01bcf13-vs-base.md)
- [📈time plot](bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4%2B-01bcf13-vs-base.svg)

