# Results

- fork: Fidget-Spinner/resume_tracing
- version: 3.15.0a3+
- config: JIT
- commit hash: [564677c](https://github.com/Fidget%2dSpinner/cpython/commit/564677c)
- commit date: 2025-12-31T16:22:40Z
- commit merge base: [6cb245d26086369bb075858501405865fc255a10](https://github.com/python/cpython/commit/6cb245d26086369bb075858501405865fc255a10)
- commit date: 2025-12-31T16:22:40+00:00
- ref: resume_tracing

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20623347206)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20251231-vultr-x86_64-Fidget%252dSpinner-resume_tracing-3.15.0a3%2B-564677c.json)

### vs. 3.12.6

- Geometric mean: 1.123x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251231-vultr-x86_64-Fidget%252dSpinner-resume_tracing-3.15.0a3%2B-564677c-vs-3.12.6.md)
- [📈time plot](bm-20251231-vultr-x86_64-Fidget%252dSpinner-resume_tracing-3.15.0a3%2B-564677c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.085x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251231-vultr-x86_64-Fidget%252dSpinner-resume_tracing-3.15.0a3%2B-564677c-vs-3.13.0rc2.md)
- [📈time plot](bm-20251231-vultr-x86_64-Fidget%252dSpinner-resume_tracing-3.15.0a3%2B-564677c-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.002x faster (HPT: reliability of 71.13%, 1.00x faster at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20251231-vultr-x86_64-Fidget%252dSpinner-resume_tracing-3.15.0a3%2B-564677c-vs-base-mem.svg)
- [📄table](bm-20251231-vultr-x86_64-Fidget%252dSpinner-resume_tracing-3.15.0a3%2B-564677c-vs-base.md)
- [📈time plot](bm-20251231-vultr-x86_64-Fidget%252dSpinner-resume_tracing-3.15.0a3%2B-564677c-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20623347206)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251231-macm4pro-arm64-Fidget%252dSpinner-resume_tracing-3.15.0a3%2B-564677c.json)

### vs. 3.12.6

- Geometric mean: 1.247x faster (HPT: reliability of 100.00%, 1.12x faster at 99th %ile)
- Memory usage: 1.24x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251231-macm4pro-arm64-Fidget%252dSpinner-resume_tracing-3.15.0a3%2B-564677c-vs-3.12.6.md)
- [📈time plot](bm-20251231-macm4pro-arm64-Fidget%252dSpinner-resume_tracing-3.15.0a3%2B-564677c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.156x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251231-macm4pro-arm64-Fidget%252dSpinner-resume_tracing-3.15.0a3%2B-564677c-vs-3.13.0rc2.md)
- [📈time plot](bm-20251231-macm4pro-arm64-Fidget%252dSpinner-resume_tracing-3.15.0a3%2B-564677c-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.004x slower (HPT: reliability of 77.56%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- new benchmarks: asyncio_websockets
- [🧠memory plot](bm-20251231-macm4pro-arm64-Fidget%252dSpinner-resume_tracing-3.15.0a3%2B-564677c-vs-base-mem.svg)
- [📄table](bm-20251231-macm4pro-arm64-Fidget%252dSpinner-resume_tracing-3.15.0a3%2B-564677c-vs-base.md)
- [📈time plot](bm-20251231-macm4pro-arm64-Fidget%252dSpinner-resume_tracing-3.15.0a3%2B-564677c-vs-base.svg)

