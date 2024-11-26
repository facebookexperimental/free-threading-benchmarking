# Results

- fork: nascheme
- version: 3.14.0a2+
- config: NOGIL
- commit hash: [a515a0d](https://github.com/nascheme/cpython/commit/a515a0d)
- commit date: 2024-11-25T11:22:18-08:00
- commit merge base: [09c240f20c47db126ad7e162df41e5c2596962d4](https://github.com/nascheme/cpython/commit/09c240f20c47db126ad7e162df41e5c2596962d4)
- ref: gh_115999_load_super

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12020600304)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2%2B-a515a0d.json)

### vs. 3.12.6

- Geometric mean: 1.411x slower (HPT: reliability of 100.00%, 1.43x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2%2B-a515a0d-vs-3.12.6.md)
- [📈time plot](bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2%2B-a515a0d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.431x slower (HPT: reliability of 100.00%, 1.48x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2%2B-a515a0d-vs-3.13.0rc2.md)
- [📈time plot](bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2%2B-a515a0d-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.175x slower (HPT: reliability of 99.99%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2%2B-a515a0d-vs-base-mem.svg)
- [📄table](bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2%2B-a515a0d-vs-base.md)
- [📈time plot](bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2%2B-a515a0d-vs-base.svg)

