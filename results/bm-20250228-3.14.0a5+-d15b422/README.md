# Results

- fork: colesbury/gh_130382_reftracer_
- version: 3.14.0a5+
- config: 
- commit hash: [d15b422](https://github.com/colesbury/cpython/commit/d15b422)
- commit date: 2025-02-28T18:40:44+00:00
- commit merge base: [ab11c097052757b79060c75dd4835c2431e752b7](https://github.com/python/cpython/commit/ab11c097052757b79060c75dd4835c2431e752b7)
- ref: gh_130382_reftracer_

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13594439311)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250228-vultr-x86_64-colesbury-gh_130382_reftracer_-3.14.0a5%2B-d15b422.json)

### vs. 3.12.6

- Geometric mean: 1.108x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250228-vultr-x86_64-colesbury-gh_130382_reftracer_-3.14.0a5%2B-d15b422-vs-3.12.6.md)
- [📈time plot](bm-20250228-vultr-x86_64-colesbury-gh_130382_reftracer_-3.14.0a5%2B-d15b422-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.068x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250228-vultr-x86_64-colesbury-gh_130382_reftracer_-3.14.0a5%2B-d15b422-vs-3.13.0rc2.md)
- [📈time plot](bm-20250228-vultr-x86_64-colesbury-gh_130382_reftracer_-3.14.0a5%2B-d15b422-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.002x slower (HPT: reliability of 86.87%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250228-vultr-x86_64-colesbury-gh_130382_reftracer_-3.14.0a5%2B-d15b422-vs-base-mem.svg)
- [📄table](bm-20250228-vultr-x86_64-colesbury-gh_130382_reftracer_-3.14.0a5%2B-d15b422-vs-base.md)
- [📈time plot](bm-20250228-vultr-x86_64-colesbury-gh_130382_reftracer_-3.14.0a5%2B-d15b422-vs-base.svg)

