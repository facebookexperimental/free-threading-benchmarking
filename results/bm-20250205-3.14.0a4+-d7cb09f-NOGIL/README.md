# Results

- fork: wrongnull/ft_new_reference_dat
- version: 3.14.0a4+
- config: NOGIL
- commit hash: [d7cb09f](https://github.com/wrongnull/cpython/commit/d7cb09f)
- commit date: 2025-02-05T12:28:48+03:00
- commit merge base: [75b628adebd4594529da25ea9915600f2872fc2b](https://github.com/python/cpython/commit/75b628adebd4594529da25ea9915600f2872fc2b)
- ref: ft_new_reference_dat

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13185889281)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250205-vultr-x86_64-wrongnull-ft_new_reference_dat-3.14.0a4%2B-d7cb09f.json)

### vs. 3.12.6

- Geometric mean: 1.042x slower (HPT: reliability of 99.97%, 1.02x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250205-vultr-x86_64-wrongnull-ft_new_reference_dat-3.14.0a4%2B-d7cb09f-vs-3.12.6.md)
- [📈time plot](bm-20250205-vultr-x86_64-wrongnull-ft_new_reference_dat-3.14.0a4%2B-d7cb09f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.073x slower (HPT: reliability of 99.99%, 1.04x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250205-vultr-x86_64-wrongnull-ft_new_reference_dat-3.14.0a4%2B-d7cb09f-vs-3.13.0rc2.md)
- [📈time plot](bm-20250205-vultr-x86_64-wrongnull-ft_new_reference_dat-3.14.0a4%2B-d7cb09f-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.001x faster (HPT: reliability of 88.78%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250205-vultr-x86_64-wrongnull-ft_new_reference_dat-3.14.0a4%2B-d7cb09f-vs-base-mem.svg)
- [📄table](bm-20250205-vultr-x86_64-wrongnull-ft_new_reference_dat-3.14.0a4%2B-d7cb09f-vs-base.md)
- [📈time plot](bm-20250205-vultr-x86_64-wrongnull-ft_new_reference_dat-3.14.0a4%2B-d7cb09f-vs-base.svg)

