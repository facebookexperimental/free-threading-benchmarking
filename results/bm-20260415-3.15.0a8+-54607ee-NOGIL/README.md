# Results

- fork: python/54607eec34b42d377a12
- version: 3.15.0a8+
- config: NOGIL
- commit hash: [54607ee](https://github.com/python/cpython/commit/54607ee)
- commit date: 2026-04-15T22:48:14+01:00
- commit merge base: [eb2f634b831ae235c2ebd4cbeab97a40e7d8724e](https://github.com/python/cpython/commit/eb2f634b831ae235c2ebd4cbeab97a40e7d8724e)
- ref: 54607eec34b42d377a12

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/24485999571)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260415-vultr-x86_64-python-54607eec34b42d377a12-3.15.0a8%2B-54607ee.json)

### vs. 3.12.6

- Geometric mean: 1.012x slower (HPT: reliability of 58.36%, 1.00x slower at 99th %ile)
- Memory usage: 1.44x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260415-vultr-x86_64-python-54607eec34b42d377a12-3.15.0a8%2B-54607ee-vs-3.12.6.md)
- [📈time plot](bm-20260415-vultr-x86_64-python-54607eec34b42d377a12-3.15.0a8%2B-54607ee-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.045x slower (HPT: reliability of 81.13%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260415-vultr-x86_64-python-54607eec34b42d377a12-3.15.0a8%2B-54607ee-vs-3.13.0rc2.md)
- [📈time plot](bm-20260415-vultr-x86_64-python-54607eec34b42d377a12-3.15.0a8%2B-54607ee-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.091x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20260415-vultr-x86_64-python-54607eec34b42d377a12-3.15.0a8%2B-54607ee-vs-base-mem.svg)
- [📄table](bm-20260415-vultr-x86_64-python-54607eec34b42d377a12-3.15.0a8%2B-54607ee-vs-base.md)
- [📈time plot](bm-20260415-vultr-x86_64-python-54607eec34b42d377a12-3.15.0a8%2B-54607ee-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/24485999571)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260415-macm4pro-arm64-python-54607eec34b42d377a12-3.15.0a8%2B-54607ee.json)

### vs. 3.12.6

- Geometric mean: 1.103x faster (HPT: reliability of 99.58%, 1.00x faster at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260415-macm4pro-arm64-python-54607eec34b42d377a12-3.15.0a8%2B-54607ee-vs-3.12.6.md)
- [📈time plot](bm-20260415-macm4pro-arm64-python-54607eec34b42d377a12-3.15.0a8%2B-54607ee-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.023x faster (HPT: reliability of 58.38%, 1.00x faster at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260415-macm4pro-arm64-python-54607eec34b42d377a12-3.15.0a8%2B-54607ee-vs-3.13.0rc2.md)
- [📈time plot](bm-20260415-macm4pro-arm64-python-54607eec34b42d377a12-3.15.0a8%2B-54607ee-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.056x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20260415-macm4pro-arm64-python-54607eec34b42d377a12-3.15.0a8%2B-54607ee-vs-base-mem.svg)
- [📄table](bm-20260415-macm4pro-arm64-python-54607eec34b42d377a12-3.15.0a8%2B-54607ee-vs-base.md)
- [📈time plot](bm-20260415-macm4pro-arm64-python-54607eec34b42d377a12-3.15.0a8%2B-54607ee-vs-base.svg)

