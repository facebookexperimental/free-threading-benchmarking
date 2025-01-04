# Results

- fork: mpage/gh_115999_integrate
- version: 3.14.0a3+
- config: NOGIL
- commit hash: [33deca3](https://github.com/mpage/cpython/commit/33deca3)
- commit date: 2025-01-03T14:03:19-08:00
- commit merge base: [f1574859d7d6cd259f867194762f04b72ef2c340](https://github.com/python/cpython/commit/f1574859d7d6cd259f867194762f04b72ef2c340)
- ref: gh_115999_integrate

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12604534528)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20250103-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a3%2B-33deca3.json)

### vs. 3.12.6

- Geometric mean: 1.059x slower (HPT: reliability of 100.00%, 1.04x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250103-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a3%2B-33deca3-vs-3.12.6.md)
- [📈time plot](bm-20250103-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a3%2B-33deca3-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.089x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250103-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a3%2B-33deca3-vs-3.13.0rc2.md)
- [📈time plot](bm-20250103-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a3%2B-33deca3-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.126x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20250103-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a3%2B-33deca3-vs-base-mem.svg)
- [📄table](bm-20250103-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a3%2B-33deca3-vs-base.md)
- [📈time plot](bm-20250103-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a3%2B-33deca3-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.136x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [📄table](bm-20250103-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a3%2B-33deca3-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20250103-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a3%2B-33deca3-vs-default_base_vs_NOGIL.svg)

