# Results

- fork: mpage/measure_lfb
- version: 3.14.0a5+
- config: 
- commit hash: [76fc3d1](https://github.com/mpage/cpython/commit/76fc3d1)
- commit date: 2025-03-14T15:59:18-07:00
- commit merge base: [1a8e5742cdcf3dba7fc592d036adab49877c42ba](https://github.com/python/cpython/commit/1a8e5742cdcf3dba7fc592d036adab49877c42ba)
- ref: measure_lfb

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13867391541)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250314-vultr-x86_64-mpage-measure_lfb-3.14.0a5%2B-76fc3d1.json)

### vs. 3.12.6

- Geometric mean: 1.089x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250314-vultr-x86_64-mpage-measure_lfb-3.14.0a5%2B-76fc3d1-vs-3.12.6.md)
- [📈time plot](bm-20250314-vultr-x86_64-mpage-measure_lfb-3.14.0a5%2B-76fc3d1-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.050x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250314-vultr-x86_64-mpage-measure_lfb-3.14.0a5%2B-76fc3d1-vs-3.13.0rc2.md)
- [📈time plot](bm-20250314-vultr-x86_64-mpage-measure_lfb-3.14.0a5%2B-76fc3d1-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.027x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250314-vultr-x86_64-mpage-measure_lfb-3.14.0a5%2B-76fc3d1-vs-base-mem.svg)
- [📄table](bm-20250314-vultr-x86_64-mpage-measure_lfb-3.14.0a5%2B-76fc3d1-vs-base.md)
- [📈time plot](bm-20250314-vultr-x86_64-mpage-measure_lfb-3.14.0a5%2B-76fc3d1-vs-base.svg)

