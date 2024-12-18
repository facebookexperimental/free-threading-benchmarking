# Results

- fork: nascheme/gh_115999_specialize
- version: 3.14.0a2+
- config: 
- commit hash: [699f4e9](https://github.com/nascheme/cpython/commit/699f4e9)
- commit date: 2024-12-17T13:59:12-08:00
- commit merge base: [2de048ce79e621f5ae0574095b9600fe8595f607](https://github.com/python/cpython/commit/2de048ce79e621f5ae0574095b9600fe8595f607)
- ref: gh_115999_specialize

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12384451699)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-699f4e9.json)

### vs. 3.12.6

- Geometric mean: 1.079x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-699f4e9-vs-3.12.6.md)
- [📈time plot](bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-699f4e9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.040x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-699f4e9-vs-3.13.0rc2.md)
- [📈time plot](bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-699f4e9-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.005x slower (HPT: reliability of 97.76%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-699f4e9-vs-base-mem.svg)
- [📄table](bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-699f4e9-vs-base.md)
- [📈time plot](bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-699f4e9-vs-base.svg)

