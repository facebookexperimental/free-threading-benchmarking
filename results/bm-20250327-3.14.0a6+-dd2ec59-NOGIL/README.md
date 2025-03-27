# Results

- fork: Yhg1s/uniqref_critsection
- version: 3.14.0a6+
- config: NOGIL
- commit hash: [dd2ec59](https://github.com/Yhg1s/cpython/commit/dd2ec59)
- commit date: 2025-03-27T00:28:33+01:00
- commit merge base: [af29d5cfd19bf2656955b9bb782cc89c7aa7000f](https://github.com/python/cpython/commit/af29d5cfd19bf2656955b9bb782cc89c7aa7000f)
- ref: uniqref_critsection

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14095465549)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250327-vultr-x86_64-Yhg1s-uniqref_critsection-3.14.0a6%2B-dd2ec59.json)

### vs. 3.12.6

- Geometric mean: 1.053x slower (HPT: reliability of 99.99%, 1.03x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250327-vultr-x86_64-Yhg1s-uniqref_critsection-3.14.0a6%2B-dd2ec59-vs-3.12.6.md)
- [📈time plot](bm-20250327-vultr-x86_64-Yhg1s-uniqref_critsection-3.14.0a6%2B-dd2ec59-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.084x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250327-vultr-x86_64-Yhg1s-uniqref_critsection-3.14.0a6%2B-dd2ec59-vs-3.13.0rc2.md)
- [📈time plot](bm-20250327-vultr-x86_64-Yhg1s-uniqref_critsection-3.14.0a6%2B-dd2ec59-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.006x slower (HPT: reliability of 87.94%, 1.00x slower at 99th %ile)
- Memory usage: 0.99x
- [🧠memory plot](bm-20250327-vultr-x86_64-Yhg1s-uniqref_critsection-3.14.0a6%2B-dd2ec59-vs-base-mem.svg)
- [📄table](bm-20250327-vultr-x86_64-Yhg1s-uniqref_critsection-3.14.0a6%2B-dd2ec59-vs-base.md)
- [📈time plot](bm-20250327-vultr-x86_64-Yhg1s-uniqref_critsection-3.14.0a6%2B-dd2ec59-vs-base.svg)

