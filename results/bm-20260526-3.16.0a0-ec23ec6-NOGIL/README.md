# Results

- fork: python/ec23ec6870373b64a760
- version: 3.16.0a0
- config: NOGIL
- commit hash: [ec23ec6](https://github.com/python/cpython/commit/ec23ec6)
- commit date: 2026-05-26T01:37:14+01:00
- commit merge base: [a5be25d3bdc1b3cbc9638a3249c0e3db5a97ebc6](https://github.com/python/cpython/commit/a5be25d3bdc1b3cbc9638a3249c0e3db5a97ebc6)
- ref: ec23ec6870373b64a760

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/26426274517)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260526-vultr-x86_64-python-ec23ec6870373b64a760-3.16.0a0-ec23ec6.json)

### vs. 3.12.6

- Geometric mean: 1.040x slower (HPT: reliability of 90.75%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260526-vultr-x86_64-python-ec23ec6870373b64a760-3.16.0a0-ec23ec6-vs-3.12.6.md)
- [📈time plot](bm-20260526-vultr-x86_64-python-ec23ec6870373b64a760-3.16.0a0-ec23ec6-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.076x slower (HPT: reliability of 99.73%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260526-vultr-x86_64-python-ec23ec6870373b64a760-3.16.0a0-ec23ec6-vs-3.13.0rc2.md)
- [📈time plot](bm-20260526-vultr-x86_64-python-ec23ec6870373b64a760-3.16.0a0-ec23ec6-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.100x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20260526-vultr-x86_64-python-ec23ec6870373b64a760-3.16.0a0-ec23ec6-vs-base-mem.svg)
- [📄table](bm-20260526-vultr-x86_64-python-ec23ec6870373b64a760-3.16.0a0-ec23ec6-vs-base.md)
- [📈time plot](bm-20260526-vultr-x86_64-python-ec23ec6870373b64a760-3.16.0a0-ec23ec6-vs-base.svg)

