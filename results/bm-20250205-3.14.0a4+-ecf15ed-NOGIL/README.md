# Results

- fork: nascheme/ft_float_consume_inp
- version: 3.14.0a4+
- config: NOGIL
- commit hash: [ecf15ed](https://github.com/nascheme/cpython/commit/ecf15ed)
- commit date: 2025-02-05T14:20:50-08:00
- commit merge base: [7d9a22f50923309955a2caf7d57013f224071e6e](https://github.com/python/cpython/commit/7d9a22f50923309955a2caf7d57013f224071e6e)
- ref: ft_float_consume_inp

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13168056150)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250205-vultr-x86_64-nascheme-ft_float_consume_inp-3.14.0a4%2B-ecf15ed.json)

### vs. 3.12.6

- Geometric mean: 1.044x slower (HPT: reliability of 99.93%, 1.02x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250205-vultr-x86_64-nascheme-ft_float_consume_inp-3.14.0a4%2B-ecf15ed-vs-3.12.6.md)
- [📈time plot](bm-20250205-vultr-x86_64-nascheme-ft_float_consume_inp-3.14.0a4%2B-ecf15ed-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.075x slower (HPT: reliability of 99.97%, 1.04x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250205-vultr-x86_64-nascheme-ft_float_consume_inp-3.14.0a4%2B-ecf15ed-vs-3.13.0rc2.md)
- [📈time plot](bm-20250205-vultr-x86_64-nascheme-ft_float_consume_inp-3.14.0a4%2B-ecf15ed-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.002x faster (HPT: reliability of 60.44%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250205-vultr-x86_64-nascheme-ft_float_consume_inp-3.14.0a4%2B-ecf15ed-vs-base-mem.svg)
- [📄table](bm-20250205-vultr-x86_64-nascheme-ft_float_consume_inp-3.14.0a4%2B-ecf15ed-vs-base.md)
- [📈time plot](bm-20250205-vultr-x86_64-nascheme-ft_float_consume_inp-3.14.0a4%2B-ecf15ed-vs-base.svg)

