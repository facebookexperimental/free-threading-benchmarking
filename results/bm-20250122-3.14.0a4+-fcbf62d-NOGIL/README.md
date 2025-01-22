# Results

- fork: mpage/ft_aa_test_0
- version: 3.14.0a4+
- config: NOGIL
- commit hash: [fcbf62d](https://github.com/mpage/cpython/commit/fcbf62d)
- commit date: 2025-01-22T13:37:21-08:00
- commit merge base: [2ed5ee9a50454b3fce87b26be5838ca7127b2ff9](https://github.com/python/cpython/commit/2ed5ee9a50454b3fce87b26be5838ca7127b2ff9)
- ref: ft_aa_test_0

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12917630928)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250122-vultr-x86_64-mpage-ft_aa_test_0-3.14.0a4%2B-fcbf62d.json)

### vs. 3.12.6

- Geometric mean: 1.081x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250122-vultr-x86_64-mpage-ft_aa_test_0-3.14.0a4%2B-fcbf62d-vs-3.12.6.md)
- [📈time plot](bm-20250122-vultr-x86_64-mpage-ft_aa_test_0-3.14.0a4%2B-fcbf62d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.111x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250122-vultr-x86_64-mpage-ft_aa_test_0-3.14.0a4%2B-fcbf62d-vs-3.13.0rc2.md)
- [📈time plot](bm-20250122-vultr-x86_64-mpage-ft_aa_test_0-3.14.0a4%2B-fcbf62d-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.001x slower (HPT: reliability of 93.21%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250122-vultr-x86_64-mpage-ft_aa_test_0-3.14.0a4%2B-fcbf62d-vs-base-mem.svg)
- [📄table](bm-20250122-vultr-x86_64-mpage-ft_aa_test_0-3.14.0a4%2B-fcbf62d-vs-base.md)
- [📈time plot](bm-20250122-vultr-x86_64-mpage-ft_aa_test_0-3.14.0a4%2B-fcbf62d-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.152x slower (HPT: reliability of 100.00%, 1.13x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [📄table](bm-20250122-vultr-x86_64-mpage-ft_aa_test_0-3.14.0a4%2B-fcbf62d-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20250122-vultr-x86_64-mpage-ft_aa_test_0-3.14.0a4%2B-fcbf62d-vs-default_base_vs_NOGIL.svg)

