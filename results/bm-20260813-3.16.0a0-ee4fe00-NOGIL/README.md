# Results

- fork: python/ee4fe00a8f72ea84a421
- version: 3.16.0a0
- config: NOGIL
- commit hash: [ee4fe00](https://github.com/python/cpython/commit/ee4fe00)
- commit date: 2026-08-13T00:12:39+00:00
- commit merge base: [bc31217fe432b5ede1485bec2b62b2c67a48eee4](https://github.com/python/cpython/commit/bc31217fe432b5ede1485bec2b62b2c67a48eee4)
- ref: ee4fe00a8f72ea84a421

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/31654608238)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260813-vultr-x86_64-python-ee4fe00a8f72ea84a421-3.16.0a0-ee4fe00.json)

### vs. 3.12.6

- Geometric mean: 1.037x slower (HPT: reliability of 86.72%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260813-vultr-x86_64-python-ee4fe00a8f72ea84a421-3.16.0a0-ee4fe00-vs-3.12.6.md)
- [📈time plot](bm-20260813-vultr-x86_64-python-ee4fe00a8f72ea84a421-3.16.0a0-ee4fe00-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.069x slower (HPT: reliability of 97.64%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260813-vultr-x86_64-python-ee4fe00a8f72ea84a421-3.16.0a0-ee4fe00-vs-3.13.0rc2.md)
- [📈time plot](bm-20260813-vultr-x86_64-python-ee4fe00a8f72ea84a421-3.16.0a0-ee4fe00-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.099x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20260813-vultr-x86_64-python-ee4fe00a8f72ea84a421-3.16.0a0-ee4fe00-vs-base-mem.svg)
- [📄table](bm-20260813-vultr-x86_64-python-ee4fe00a8f72ea84a421-3.16.0a0-ee4fe00-vs-base.md)
- [📈time plot](bm-20260813-vultr-x86_64-python-ee4fe00a8f72ea84a421-3.16.0a0-ee4fe00-vs-base.svg)

