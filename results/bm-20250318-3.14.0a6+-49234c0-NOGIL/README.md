# Results

- fork: python/49234c065cf2b1ea32c5
- version: 3.14.0a6+
- config: NOGIL
- commit hash: [49234c0](https://github.com/python/cpython/commit/49234c0)
- commit date: 2025-03-18T14:31:13+01:00
- commit merge base: [8cb57dc3678a8b26772d0fffce525762fee4f234](https://github.com/python/cpython/commit/8cb57dc3678a8b26772d0fffce525762fee4f234)
- ref: 49234c065cf2b1ea32c5

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13925508624)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250318-vultr-x86_64-python-49234c065cf2b1ea32c5-3.14.0a6%2B-49234c0.json)

### vs. 3.12.6

- Geometric mean: 1.049x slower (HPT: reliability of 99.99%, 1.03x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250318-vultr-x86_64-python-49234c065cf2b1ea32c5-3.14.0a6%2B-49234c0-vs-3.12.6.md)
- [📈time plot](bm-20250318-vultr-x86_64-python-49234c065cf2b1ea32c5-3.14.0a6%2B-49234c0-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.081x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250318-vultr-x86_64-python-49234c065cf2b1ea32c5-3.14.0a6%2B-49234c0-vs-3.13.0rc2.md)
- [📈time plot](bm-20250318-vultr-x86_64-python-49234c065cf2b1ea32c5-3.14.0a6%2B-49234c0-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.105x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250318-vultr-x86_64-python-49234c065cf2b1ea32c5-3.14.0a6%2B-49234c0-vs-base-mem.svg)
- [📄table](bm-20250318-vultr-x86_64-python-49234c065cf2b1ea32c5-3.14.0a6%2B-49234c0-vs-base.md)
- [📈time plot](bm-20250318-vultr-x86_64-python-49234c065cf2b1ea32c5-3.14.0a6%2B-49234c0-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13925508624)
- cpu model: missing
- platform: macOS-15.3.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250318-macm4pro-arm64-python-49234c065cf2b1ea32c5-3.14.0a6%2B-49234c0.json)

### vs. 3.12.6

- Geometric mean: 1.030x slower (HPT: reliability of 99.94%, 1.02x slower at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, tornado_http
- [📄table](bm-20250318-macm4pro-arm64-python-49234c065cf2b1ea32c5-3.14.0a6%2B-49234c0-vs-3.12.6.md)
- [📈time plot](bm-20250318-macm4pro-arm64-python-49234c065cf2b1ea32c5-3.14.0a6%2B-49234c0-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.100x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, tornado_http
- [📄table](bm-20250318-macm4pro-arm64-python-49234c065cf2b1ea32c5-3.14.0a6%2B-49234c0-vs-3.13.0rc2.md)
- [📈time plot](bm-20250318-macm4pro-arm64-python-49234c065cf2b1ea32c5-3.14.0a6%2B-49234c0-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.084x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: 🔴 dask
- [🧠memory plot](bm-20250318-macm4pro-arm64-python-49234c065cf2b1ea32c5-3.14.0a6%2B-49234c0-vs-base-mem.svg)
- [📄table](bm-20250318-macm4pro-arm64-python-49234c065cf2b1ea32c5-3.14.0a6%2B-49234c0-vs-base.md)
- [📈time plot](bm-20250318-macm4pro-arm64-python-49234c065cf2b1ea32c5-3.14.0a6%2B-49234c0-vs-base.svg)

