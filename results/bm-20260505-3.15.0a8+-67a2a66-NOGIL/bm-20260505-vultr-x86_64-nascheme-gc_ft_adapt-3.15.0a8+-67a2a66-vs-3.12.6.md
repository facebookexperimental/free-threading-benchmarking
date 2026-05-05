# Results vs. 3.12.6

- fork: nascheme
- ref: gc_ft_adapt
- machine: linux-x86_64
- commit hash: 67a2a66
- commit date: 2026-05-05
- overall geometric mean: 1.023x slower
- HPT reliability: 86.05%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.40x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260505-vultr-x86_64-nascheme-gc_ft_adapt-3.15.0a8+-67a2a66 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------:|
| docutils       | 2.64 sec                                               | 2.95 sec: 1.12x slower                                          |
| html5lib       | 63.6 ms                                                | 70.1 ms: 1.10x slower                                           |
| Geometric mean | (ref)                                                  | 1.11x slower                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260505-vultr-x86_64-nascheme-gc_ft_adapt-3.15.0a8+-67a2a66 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 601 ms: 1.85x faster                                            |
| async_tree_io              | 1.08 sec                                               | 630 ms: 1.72x faster                                            |
| async_tree_memoization_tg  | 560 ms                                                 | 328 ms: 1.71x faster                                            |
| async_tree_none_tg         | 446 ms                                                 | 275 ms: 1.62x faster                                            |
| async_tree_none            | 464 ms                                                 | 294 ms: 1.58x faster                                            |
| async_tree_memoization     | 555 ms                                                 | 368 ms: 1.51x faster                                            |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 522 ms: 1.38x faster                                            |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 557 ms: 1.28x faster                                            |
| asyncio_websockets         | 517 ms                                                 | 510 ms: 1.01x faster                                            |
| async_generators           | 384 ms                                                 | 394 ms: 1.02x slower                                            |
| coroutines                 | 23.9 ms                                                | 24.7 ms: 1.03x slower                                           |
| Geometric mean             | (ref)                                                  | 1.38x faster                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260505-vultr-x86_64-nascheme-gc_ft_adapt-3.15.0a8+-67a2a66 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------:|
| float          | 80.8 ms                                                | 78.7 ms: 1.03x faster                                           |
| pidigits       | 184 ms                                                 | 188 ms: 1.02x slower                                            |
| nbody          | 89.3 ms                                                | 126 ms: 1.41x slower                                            |
| Geometric mean | (ref)                                                  | 1.12x slower                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260505-vultr-x86_64-nascheme-gc_ft_adapt-3.15.0a8+-67a2a66 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 3.09 ms: 1.03x faster                                           |
| regex_v8       | 20.6 ms                                                | 20.4 ms: 1.01x faster                                           |
| regex_compile  | 142 ms                                                 | 144 ms: 1.01x slower                                            |
| regex_dna      | 168 ms                                                 | 176 ms: 1.05x slower                                            |
| Geometric mean | (ref)                                                  | 1.01x slower                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260505-vultr-x86_64-nascheme-gc_ft_adapt-3.15.0a8+-67a2a66 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.98 sec: 1.07x faster                                          |
| xml_etree_iterparse  | 96.7 ms                                                | 91.7 ms: 1.05x faster                                           |
| xml_etree_parse      | 139 ms                                                 | 136 ms: 1.02x faster                                            |
| json_dumps           | 10.4 ms                                                | 10.9 ms: 1.05x slower                                           |
| unpickle_pure_python | 221 us                                                 | 241 us: 1.09x slower                                            |
| pickle_pure_python   | 308 us                                                 | 347 us: 1.13x slower                                            |
| xml_etree_generate   | 85.2 ms                                                | 99.2 ms: 1.16x slower                                           |
| json_loads           | 26.5 us                                                | 31.0 us: 1.17x slower                                           |
| xml_etree_process    | 59.0 ms                                                | 70.2 ms: 1.19x slower                                           |
| Geometric mean       | (ref)                                                  | 1.07x slower                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260505-vultr-x86_64-nascheme-gc_ft_adapt-3.15.0a8+-67a2a66 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 40.1 ms: 1.16x slower                                           |
| mako            | 11.0 ms                                                | 16.4 ms: 1.49x slower                                           |
| Geometric mean  | (ref)                                                  | 1.31x slower                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260505-vultr-x86_64-nascheme-gc_ft_adapt-3.15.0a8+-67a2a66 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------:|
| pylint                     | 319 ms                                                 | 131 ms: 2.43x faster                                            |
| async_tree_io_tg           | 1.11 sec                                               | 601 ms: 1.85x faster                                            |
| gc_traversal               | 3.46 ms                                                | 1.89 ms: 1.83x faster                                           |
| mdp                        | 2.42 sec                                               | 1.33 sec: 1.82x faster                                          |
| async_tree_io              | 1.08 sec                                               | 630 ms: 1.72x faster                                            |
| async_tree_memoization_tg  | 560 ms                                                 | 328 ms: 1.71x faster                                            |
| async_tree_none_tg         | 446 ms                                                 | 275 ms: 1.62x faster                                            |
| async_tree_none            | 464 ms                                                 | 294 ms: 1.58x faster                                            |
| bench_mp_pool              | 10.8 ms                                                | 6.99 ms: 1.55x faster                                           |
| async_tree_memoization     | 555 ms                                                 | 368 ms: 1.51x faster                                            |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 522 ms: 1.38x faster                                            |
| deepcopy                   | 352 us                                                 | 270 us: 1.30x faster                                            |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 557 ms: 1.28x faster                                            |
| deepcopy_memo              | 40.3 us                                                | 31.6 us: 1.27x faster                                           |
| pathlib                    | 21.5 ms                                                | 17.9 ms: 1.20x faster                                           |
| go                         | 139 ms                                                 | 121 ms: 1.15x faster                                            |
| sqlite_synth               | 2.20 us                                                | 1.94 us: 1.13x faster                                           |
| comprehensions             | 19.8 us                                                | 18.1 us: 1.10x faster                                           |
| dulwich_log                | 78.9 ms                                                | 72.3 ms: 1.09x faster                                           |
| bpe_tokeniser              | 4.74 sec                                               | 4.42 sec: 1.07x faster                                          |
| tomli_loads                | 2.11 sec                                               | 1.98 sec: 1.07x faster                                          |
| xml_etree_iterparse        | 96.7 ms                                                | 91.7 ms: 1.05x faster                                           |
| scimark_sor                | 130 ms                                                 | 123 ms: 1.05x faster                                            |
| logging_silent             | 109 ns                                                 | 105 ns: 1.04x faster                                            |
| deepcopy_reduce            | 3.08 us                                                | 3.00 us: 1.03x faster                                           |
| regex_effbot               | 3.17 ms                                                | 3.09 ms: 1.03x faster                                           |
| float                      | 80.8 ms                                                | 78.7 ms: 1.03x faster                                           |
| pycparser                  | 1.17 sec                                               | 1.14 sec: 1.02x faster                                          |
| xml_etree_parse            | 139 ms                                                 | 136 ms: 1.02x faster                                            |
| asyncio_websockets         | 517 ms                                                 | 510 ms: 1.01x faster                                            |
| regex_v8                   | 20.6 ms                                                | 20.4 ms: 1.01x faster                                           |
| regex_compile              | 142 ms                                                 | 144 ms: 1.01x slower                                            |
| chaos                      | 62.8 ms                                                | 63.4 ms: 1.01x slower                                           |
| generators                 | 32.2 ms                                                | 32.6 ms: 1.01x slower                                           |
| pidigits                   | 184 ms                                                 | 188 ms: 1.02x slower                                            |
| async_generators           | 384 ms                                                 | 394 ms: 1.02x slower                                            |
| raytrace                   | 299 ms                                                 | 307 ms: 1.03x slower                                            |
| coroutines                 | 23.9 ms                                                | 24.7 ms: 1.03x slower                                           |
| pyflate                    | 448 ms                                                 | 464 ms: 1.04x slower                                            |
| spectral_norm              | 110 ms                                                 | 115 ms: 1.05x slower                                            |
| regex_dna                  | 168 ms                                                 | 176 ms: 1.05x slower                                            |
| json_dumps                 | 10.4 ms                                                | 10.9 ms: 1.05x slower                                           |
| logging_simple             | 6.63 us                                                | 6.98 us: 1.05x slower                                           |
| scimark_fft                | 342 ms                                                 | 360 ms: 1.05x slower                                            |
| json                       | 5.02 ms                                                | 5.34 ms: 1.06x slower                                           |
| sympy_integrate            | 20.5 ms                                                | 22.0 ms: 1.07x slower                                           |
| hexiom                     | 6.17 ms                                                | 6.62 ms: 1.07x slower                                           |
| logging_format             | 7.35 us                                                | 7.94 us: 1.08x slower                                           |
| sympy_sum                  | 166 ms                                                 | 180 ms: 1.08x slower                                            |
| deltablue                  | 3.45 ms                                                | 3.74 ms: 1.08x slower                                           |
| sympy_str                  | 292 ms                                                 | 316 ms: 1.09x slower                                            |
| unpickle_pure_python       | 221 us                                                 | 241 us: 1.09x slower                                            |
| html5lib                   | 63.6 ms                                                | 70.1 ms: 1.10x slower                                           |
| pprint_safe_repr           | 743 ms                                                 | 825 ms: 1.11x slower                                            |
| nqueens                    | 80.1 ms                                                | 89.4 ms: 1.12x slower                                           |
| pprint_pformat             | 1.52 sec                                               | 1.70 sec: 1.12x slower                                          |
| richards                   | 45.9 ms                                                | 51.4 ms: 1.12x slower                                           |
| docutils                   | 2.64 sec                                               | 2.95 sec: 1.12x slower                                          |
| pickle_pure_python         | 308 us                                                 | 347 us: 1.13x slower                                            |
| sympy_expand               | 468 ms                                                 | 530 ms: 1.13x slower                                            |
| richards_super             | 51.9 ms                                                | 58.8 ms: 1.13x slower                                           |
| thrift                     | 791 us                                                 | 906 us: 1.15x slower                                            |
| scimark_lu                 | 114 ms                                                 | 131 ms: 1.15x slower                                            |
| django_template            | 34.7 ms                                                | 40.1 ms: 1.16x slower                                           |
| xml_etree_generate         | 85.2 ms                                                | 99.2 ms: 1.16x slower                                           |
| json_loads                 | 26.5 us                                                | 31.0 us: 1.17x slower                                           |
| crypto_pyaes               | 76.6 ms                                                | 89.6 ms: 1.17x slower                                           |
| scimark_monte_carlo        | 68.4 ms                                                | 81.0 ms: 1.18x slower                                           |
| xml_etree_process          | 59.0 ms                                                | 70.2 ms: 1.19x slower                                           |
| meteor_contest             | 104 ms                                                 | 125 ms: 1.21x slower                                            |
| typing_runtime_protocols   | 163 us                                                 | 199 us: 1.22x slower                                            |
| fannkuch                   | 372 ms                                                 | 464 ms: 1.25x slower                                            |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.77 ms: 1.31x slower                                           |
| create_gc_cycles           | 1.09 ms                                                | 1.48 ms: 1.36x slower                                           |
| nbody                      | 89.3 ms                                                | 126 ms: 1.41x slower                                            |
| mako                       | 11.0 ms                                                | 16.4 ms: 1.49x slower                                           |
| bench_thread_pool          | 941 us                                                 | 1.48 ms: 1.57x slower                                           |
| coverage                   | 71.4 ms                                                | 117 ms: 1.63x slower                                            |
| telco                      | 6.53 ms                                                | 175 ms: 26.80x slower                                           |
| Geometric mean             | (ref)                                                  | 1.02x slower                                                    |
Ignored benchmarks (26) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260505-3.15.0a8+-67a2a66-NOGIL/bm-20260505-vultr-x86_64-nascheme-gc_ft_adapt-3.15.0a8+-67a2a66.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.023x slower

# HPT report

- Reliability score: 86.05% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.40x