# Results

- fork: nascheme/ft_gc_threshold_fix_
- version: 3.15.0a8+
- config: NOGIL
- commit hash: [ac09833](https://github.com/nascheme/cpython/commit/ac09833)
- commit date: 2026-04-23T18:39:45-07:00
- commit merge base: [448d7b96c181d13ca7f8977780e85b53b2716294](https://github.com/python/cpython/commit/448d7b96c181d13ca7f8977780e85b53b2716294)
- ref: ft_gc_threshold_fix_

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/24871430082)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260423-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8%2B-ac09833.json)

### vs. 3.12.6

- Geometric mean: 1.021x slower (HPT: reliability of 68.08%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260423-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8%2B-ac09833-vs-3.12.6.md)
- [📈time plot](bm-20260423-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8%2B-ac09833-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.054x slower (HPT: reliability of 89.64%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260423-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8%2B-ac09833-vs-3.13.0rc2.md)
- [📈time plot](bm-20260423-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8%2B-ac09833-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.007x slower (HPT: reliability of 64.96%, 1.00x slower at 99th %ile)
- Memory usage: 0.98x
- [🧠memory plot](bm-20260423-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8%2B-ac09833-vs-base-mem.svg)
- [📄table](bm-20260423-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8%2B-ac09833-vs-base.md)
- [📈time plot](bm-20260423-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8%2B-ac09833-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.101x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.19x
- [📄table](bm-20260423-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8%2B-ac09833-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20260423-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8%2B-ac09833-vs-default_base_vs_NOGIL.svg)

