# Results

- fork: mpage/63a53fd736f57fcf80df
- version: 3.14.0a3+
- config: 
- commit hash: [63a53fd](https://github.com/mpage/cpython/commit/63a53fd)
- commit date: 2024-12-20T20:09:39-08:00
- commit merge base: [2a66dd33dfc0b845042da9bb54aaa4e890733f54](https://github.com/python/cpython/commit/2a66dd33dfc0b845042da9bb54aaa4e890733f54)
- ref: 63a53fd736f57fcf80df

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12449611510)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241220-vultr-x86_64-mpage-63a53fd736f57fcf80df-3.14.0a3%2B-63a53fd.json)

### vs. 3.12.6

- Geometric mean: 1.085x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241220-vultr-x86_64-mpage-63a53fd736f57fcf80df-3.14.0a3%2B-63a53fd-vs-3.12.6.md)
- [📈time plot](bm-20241220-vultr-x86_64-mpage-63a53fd736f57fcf80df-3.14.0a3%2B-63a53fd-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.046x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241220-vultr-x86_64-mpage-63a53fd736f57fcf80df-3.14.0a3%2B-63a53fd-vs-3.13.0rc2.md)
- [📈time plot](bm-20241220-vultr-x86_64-mpage-63a53fd736f57fcf80df-3.14.0a3%2B-63a53fd-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.002x slower (HPT: reliability of 73.15%, 1.00x faster at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20241220-vultr-x86_64-mpage-63a53fd736f57fcf80df-3.14.0a3%2B-63a53fd-vs-base-mem.svg)
- [📄table](bm-20241220-vultr-x86_64-mpage-63a53fd736f57fcf80df-3.14.0a3%2B-63a53fd-vs-base.md)
- [📈time plot](bm-20241220-vultr-x86_64-mpage-63a53fd736f57fcf80df-3.14.0a3%2B-63a53fd-vs-base.svg)

