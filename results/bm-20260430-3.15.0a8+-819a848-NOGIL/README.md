# Results

- fork: nascheme/ft_gc_threshold_fix_
- version: 3.15.0a8+
- config: NOGIL
- commit hash: [819a848](https://github.com/nascheme/cpython/commit/819a848)
- commit date: 2026-04-30T08:19:56-07:00
- commit merge base: [8851a06e6e7ff23d91e5568df03a5ade570d4ab5](https://github.com/python/cpython/commit/8851a06e6e7ff23d91e5568df03a5ade570d4ab5)
- ref: ft_gc_threshold_fix_

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/25180073333)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260430-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8%2B-819a848.json)

### vs. 3.12.6

- Geometric mean: 1.021x slower (HPT: reliability of 61.84%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260430-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8%2B-819a848-vs-3.12.6.md)
- [📈time plot](bm-20260430-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8%2B-819a848-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.054x slower (HPT: reliability of 85.16%, 1.00x slower at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260430-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8%2B-819a848-vs-3.13.0rc2.md)
- [📈time plot](bm-20260430-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8%2B-819a848-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.006x slower (HPT: reliability of 72.82%, 1.00x slower at 99th %ile)
- Memory usage: 0.98x
- [🧠memory plot](bm-20260430-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8%2B-819a848-vs-base-mem.svg)
- [📄table](bm-20260430-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8%2B-819a848-vs-base.md)
- [📈time plot](bm-20260430-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8%2B-819a848-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.104x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.17x
- [📄table](bm-20260430-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8%2B-819a848-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20260430-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8%2B-819a848-vs-default_base_vs_NOGIL.svg)

