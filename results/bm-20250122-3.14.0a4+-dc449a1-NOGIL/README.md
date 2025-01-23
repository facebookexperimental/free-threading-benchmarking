# Results

- fork: mpage/ft_aa_test_1
- version: 3.14.0a4+
- config: NOGIL
- commit hash: [dc449a1](https://github.com/mpage/cpython/commit/dc449a1)
- commit date: 2025-01-22T13:37:50-08:00
- commit merge base: [24c84d816f2f2ecb76b80328c3f1d8c05ead0b10](https://github.com/python/cpython/commit/24c84d816f2f2ecb76b80328c3f1d8c05ead0b10)
- ref: ft_aa_test_1

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12917634273)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250122-vultr-x86_64-mpage-ft_aa_test_1-3.14.0a4%2B-dc449a1.json)

### vs. 3.12.6

- Geometric mean: 1.079x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250122-vultr-x86_64-mpage-ft_aa_test_1-3.14.0a4%2B-dc449a1-vs-3.12.6.md)
- [📈time plot](bm-20250122-vultr-x86_64-mpage-ft_aa_test_1-3.14.0a4%2B-dc449a1-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.109x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250122-vultr-x86_64-mpage-ft_aa_test_1-3.14.0a4%2B-dc449a1-vs-3.13.0rc2.md)
- [📈time plot](bm-20250122-vultr-x86_64-mpage-ft_aa_test_1-3.14.0a4%2B-dc449a1-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.002x slower (HPT: reliability of 99.98%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250122-vultr-x86_64-mpage-ft_aa_test_1-3.14.0a4%2B-dc449a1-vs-base-mem.svg)
- [📄table](bm-20250122-vultr-x86_64-mpage-ft_aa_test_1-3.14.0a4%2B-dc449a1-vs-base.md)
- [📈time plot](bm-20250122-vultr-x86_64-mpage-ft_aa_test_1-3.14.0a4%2B-dc449a1-vs-base.svg)

