# Results

- fork: python/bfb0788bfcaab7474c1b
- version: 3.14.0a2+
- config: NOGIL
- commit hash: [bfb0788](https://github.com/python/cpython/commit/bfb0788)
- commit date: 2024-12-03T07:30:24+08:00
- commit merge base: [edefb8678a11a20bdcdcbb8bb6a62ae22101bb51](https://github.com/python/cpython/commit/edefb8678a11a20bdcdcbb8bb6a62ae22101bb51)
- ref: bfb0788bfcaab7474c1b

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12130485954)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2%2B-bfb0788.json)

### vs. 3.12.6

- Geometric mean: 1.204x slower (HPT: reliability of 100.00%, 1.15x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2%2B-bfb0788-vs-3.12.6.md)
- [📈time plot](bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2%2B-bfb0788-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.231x slower (HPT: reliability of 100.00%, 1.19x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2%2B-bfb0788-vs-3.13.0rc2.md)
- [📈time plot](bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2%2B-bfb0788-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.277x slower (HPT: reliability of 100.00%, 1.28x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2%2B-bfb0788-vs-base-mem.svg)
- [📄table](bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2%2B-bfb0788-vs-base.md)
- [📈time plot](bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2%2B-bfb0788-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12130485954)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2%2B-bfb0788.json)

### vs. 3.12.6

- Geometric mean: 1.259x slower (HPT: reliability of 100.00%, 1.22x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2%2B-bfb0788-vs-3.12.6.md)
- [📈time plot](bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2%2B-bfb0788-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.283x slower (HPT: reliability of 100.00%, 1.24x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2%2B-bfb0788-vs-3.13.0rc2.md)
- [📈time plot](bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2%2B-bfb0788-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.295x slower (HPT: reliability of 100.00%, 1.31x slower at 99th %ile)
- Memory usage: 1.19x
- new benchmarks: html5lib
- [🧠memory plot](bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2%2B-bfb0788-vs-base-mem.svg)
- [📄table](bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2%2B-bfb0788-vs-base.md)
- [📈time plot](bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2%2B-bfb0788-vs-base.svg)

