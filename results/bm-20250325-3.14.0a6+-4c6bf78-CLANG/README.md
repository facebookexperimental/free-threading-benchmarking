# Results

- fork: colesbury/gh_131586_lookup_spe
- version: 3.14.0a6+
- config: CLANG
- commit hash: [4c6bf78](https://github.com/colesbury/cpython/commit/4c6bf78)
- commit date: 2025-03-25T21:40:22+00:00
- commit merge base: [b92ee14b80cc8898f799aa8120ec99dd0c882339](https://github.com/python/cpython/commit/b92ee14b80cc8898f799aa8120ec99dd0c882339)
- ref: gh_131586_lookup_spe

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14084675330)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250325-vultr-x86_64-colesbury-gh_131586_lookup_spe-3.14.0a6%2B-4c6bf78.json)

### vs. 3.12.6

- Geometric mean: 1.142x faster (HPT: reliability of 100.00%, 1.08x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250325-vultr-x86_64-colesbury-gh_131586_lookup_spe-3.14.0a6%2B-4c6bf78-vs-3.12.6.md)
- [📈time plot](bm-20250325-vultr-x86_64-colesbury-gh_131586_lookup_spe-3.14.0a6%2B-4c6bf78-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.102x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250325-vultr-x86_64-colesbury-gh_131586_lookup_spe-3.14.0a6%2B-4c6bf78-vs-3.13.0rc2.md)
- [📈time plot](bm-20250325-vultr-x86_64-colesbury-gh_131586_lookup_spe-3.14.0a6%2B-4c6bf78-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.005x slower (HPT: reliability of 100.00%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250325-vultr-x86_64-colesbury-gh_131586_lookup_spe-3.14.0a6%2B-4c6bf78-vs-base-mem.svg)
- [📄table](bm-20250325-vultr-x86_64-colesbury-gh_131586_lookup_spe-3.14.0a6%2B-4c6bf78-vs-base.md)
- [📈time plot](bm-20250325-vultr-x86_64-colesbury-gh_131586_lookup_spe-3.14.0a6%2B-4c6bf78-vs-base.svg)

