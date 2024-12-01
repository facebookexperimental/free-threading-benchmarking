# Results

- fork: corona10
- version: 3.14.0a2+
- config: NOGIL
- commit hash: [0637d48](https://github.com/corona10/cpython/commit/0637d48)
- commit date: 2024-11-30T21:56:55+09:00
- commit merge base: [58e334e1431b2ed6b70ee42501ea73e08084e769](https://github.com/corona10/cpython/commit/58e334e1431b2ed6b70ee42501ea73e08084e769)
- ref: gh_115999_binary_sub

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12101364156)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241130-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2%2B-0637d48.json)

### vs. 3.12.6

- Geometric mean: 1.254x slower (HPT: reliability of 100.00%, 1.21x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241130-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2%2B-0637d48-vs-3.12.6.md)
- [📈time plot](bm-20241130-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2%2B-0637d48-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.280x slower (HPT: reliability of 100.00%, 1.23x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241130-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2%2B-0637d48-vs-3.13.0rc2.md)
- [📈time plot](bm-20241130-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2%2B-0637d48-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.012x faster (HPT: reliability of 100.00%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20241130-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2%2B-0637d48-vs-base-mem.svg)
- [📄table](bm-20241130-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2%2B-0637d48-vs-base.md)
- [📈time plot](bm-20241130-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2%2B-0637d48-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.271x slower (HPT: reliability of 100.00%, 1.23x slower at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative
- new benchmarks: html5lib
- [📄table](bm-20241130-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2%2B-0637d48-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20241130-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2%2B-0637d48-vs-default_base_vs_NOGIL.svg)

