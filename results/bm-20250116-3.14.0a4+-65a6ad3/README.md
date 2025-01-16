# Results

- fork: mpage/gh_115999_specialize
- version: 3.14.0a4+
- config: 
- commit hash: [65a6ad3](https://github.com/mpage/cpython/commit/65a6ad3)
- commit date: 2025-01-16T08:54:16-08:00
- commit merge base: [211f41316b7f205d18eb65c1ececd7f7fb30b02d](https://github.com/python/cpython/commit/211f41316b7f205d18eb65c1ececd7f7fb30b02d)
- ref: gh_115999_specialize

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12813755305)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-65a6ad3.json)

### vs. 3.12.6

- Geometric mean: 1.088x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-65a6ad3-vs-3.12.6.md)
- [📈time plot](bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-65a6ad3-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.050x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-65a6ad3-vs-3.13.0rc2.md)
- [📈time plot](bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-65a6ad3-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.001x slower (HPT: reliability of 97.72%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-65a6ad3-vs-base-mem.svg)
- [📄table](bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-65a6ad3-vs-base.md)
- [📈time plot](bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-65a6ad3-vs-base.svg)

