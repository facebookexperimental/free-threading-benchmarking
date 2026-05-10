# Results vs. 3.12.6

- fork: python
- ref: cc5cf14ae0a3665ba9d1
- machine: linux-x86_64
- commit hash: cc5cf14
- commit date: 2026-05-09
- overall geometric mean: 1.061x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| docutils       | 2.64 sec                                               | 2.41 sec: 1.10x faster                                                |
| html5lib       | 63.6 ms                                                | 61.1 ms: 1.04x faster                                                 |
| Geometric mean | (ref)                                                  | 1.07x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none            | 464 ms                                                 | 295 ms: 1.57x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 364 ms: 1.54x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 716 ms: 1.51x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 297 ms: 1.50x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 754 ms: 1.47x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 379 ms: 1.47x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 543 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 552 ms: 1.31x faster                                                  |
| asyncio_tcp                | 519 ms                                                 | 450 ms: 1.15x faster                                                  |
| async_generators           | 384 ms                                                 | 341 ms: 1.13x faster                                                  |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.46 sec: 1.03x faster                                                |
| coroutines                 | 23.9 ms                                                | 24.9 ms: 1.04x slower                                                 |
| asyncio_websockets         | 517 ms                                                 | 543 ms: 1.05x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.28x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 75.2 ms: 1.07x faster                                                 |
| pidigits       | 184 ms                                                 | 184 ms: 1.00x faster                                                  |
| nbody          | 89.3 ms                                                | 90.1 ms: 1.01x slower                                                 |
| Geometric mean | (ref)                                                  | 1.02x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 125 ms: 1.14x faster                                                  |
| regex_effbot   | 3.17 ms                                                | 2.95 ms: 1.07x faster                                                 |
| regex_v8       | 20.6 ms                                                | 21.7 ms: 1.06x slower                                                 |
| regex_dna      | 168 ms                                                 | 184 ms: 1.10x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.84 sec: 1.15x faster                                                |
| xml_etree_iterparse  | 96.7 ms                                                | 90.9 ms: 1.06x faster                                                 |
| json_dumps           | 10.4 ms                                                | 9.75 ms: 1.06x faster                                                 |
| unpickle_pure_python | 221 us                                                 | 216 us: 1.02x faster                                                  |
| xml_etree_generate   | 85.2 ms                                                | 86.9 ms: 1.02x slower                                                 |
| xml_etree_parse      | 139 ms                                                 | 142 ms: 1.03x slower                                                  |
| json_loads           | 26.5 us                                                | 27.4 us: 1.03x slower                                                 |
| pickle_pure_python   | 308 us                                                 | 319 us: 1.04x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 61.2 ms: 1.04x slower                                                 |
| pickle_dict          | 31.8 us                                                | 34.3 us: 1.08x slower                                                 |
| unpickle             | 14.1 us                                                | 15.2 us: 1.08x slower                                                 |
| unpickle_list        | 4.67 us                                                | 5.06 us: 1.08x slower                                                 |
| pickle_list          | 4.77 us                                                | 5.18 us: 1.09x slower                                                 |
| pickle               | 10.9 us                                                | 13.1 us: 1.19x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.03x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 36.2 ms: 1.04x slower                                                 |
| mako            | 11.0 ms                                                | 12.0 ms: 1.09x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.07x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 319 ms                                                 | 114 ms: 2.79x faster                                                  |
| mdp                        | 2.42 sec                                               | 1.14 sec: 2.12x faster                                                |
| async_tree_none            | 464 ms                                                 | 295 ms: 1.57x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 364 ms: 1.54x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 716 ms: 1.51x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 297 ms: 1.50x faster                                                  |
| deepcopy                   | 352 us                                                 | 237 us: 1.49x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 754 ms: 1.47x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 379 ms: 1.47x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 27.7 us: 1.45x faster                                                 |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 543 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 552 ms: 1.31x faster                                                  |
| go                         | 139 ms                                                 | 108 ms: 1.29x faster                                                  |
| comprehensions             | 19.8 us                                                | 16.0 us: 1.24x faster                                                 |
| pathlib                    | 21.5 ms                                                | 17.6 ms: 1.23x faster                                                 |
| unpack_sequence            | 52.1 ns                                                | 43.2 ns: 1.20x faster                                                 |
| deepcopy_reduce            | 3.08 us                                                | 2.57 us: 1.20x faster                                                 |
| scimark_sor                | 130 ms                                                 | 110 ms: 1.18x faster                                                  |
| generators                 | 32.2 ms                                                | 27.5 ms: 1.17x faster                                                 |
| spectral_norm              | 110 ms                                                 | 94.6 ms: 1.16x faster                                                 |
| raytrace                   | 299 ms                                                 | 259 ms: 1.16x faster                                                  |
| asyncio_tcp                | 519 ms                                                 | 450 ms: 1.15x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 68.7 ms: 1.15x faster                                                 |
| tomli_loads                | 2.11 sec                                               | 1.84 sec: 1.15x faster                                                |
| regex_compile              | 142 ms                                                 | 125 ms: 1.14x faster                                                  |
| logging_simple             | 6.63 us                                                | 5.84 us: 1.13x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.18 sec: 1.13x faster                                                |
| chaos                      | 62.8 ms                                                | 55.6 ms: 1.13x faster                                                 |
| async_generators           | 384 ms                                                 | 341 ms: 1.13x faster                                                  |
| pyflate                    | 448 ms                                                 | 399 ms: 1.12x faster                                                  |
| logging_format             | 7.35 us                                                | 6.67 us: 1.10x faster                                                 |
| crypto_pyaes               | 76.6 ms                                                | 69.6 ms: 1.10x faster                                                 |
| docutils                   | 2.64 sec                                               | 2.41 sec: 1.10x faster                                                |
| scimark_fft                | 342 ms                                                 | 316 ms: 1.08x faster                                                  |
| logging_silent             | 109 ns                                                 | 101 ns: 1.08x faster                                                  |
| float                      | 80.8 ms                                                | 75.2 ms: 1.07x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.95 ms: 1.07x faster                                                 |
| nqueens                    | 80.1 ms                                                | 74.9 ms: 1.07x faster                                                 |
| sympy_integrate            | 20.5 ms                                                | 19.2 ms: 1.07x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 90.9 ms: 1.06x faster                                                 |
| json_dumps                 | 10.4 ms                                                | 9.75 ms: 1.06x faster                                                 |
| sympy_sum                  | 166 ms                                                 | 157 ms: 1.06x faster                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 64.8 ms: 1.06x faster                                                 |
| sympy_str                  | 292 ms                                                 | 276 ms: 1.06x faster                                                  |
| richards                   | 45.9 ms                                                | 43.7 ms: 1.05x faster                                                 |
| richards_super             | 51.9 ms                                                | 49.4 ms: 1.05x faster                                                 |
| hexiom                     | 6.17 ms                                                | 5.89 ms: 1.05x faster                                                 |
| html5lib                   | 63.6 ms                                                | 61.1 ms: 1.04x faster                                                 |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.46 sec: 1.03x faster                                                |
| meteor_contest             | 104 ms                                                 | 100 ms: 1.03x faster                                                  |
| unpickle_pure_python       | 221 us                                                 | 216 us: 1.02x faster                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.49 sec: 1.02x faster                                                |
| deltablue                  | 3.45 ms                                                | 3.39 ms: 1.02x faster                                                 |
| pprint_safe_repr           | 743 ms                                                 | 734 ms: 1.01x faster                                                  |
| thrift                     | 791 us                                                 | 782 us: 1.01x faster                                                  |
| scimark_lu                 | 114 ms                                                 | 113 ms: 1.01x faster                                                  |
| pidigits                   | 184 ms                                                 | 184 ms: 1.00x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.18 sec: 1.01x slower                                                |
| nbody                      | 89.3 ms                                                | 90.1 ms: 1.01x slower                                                 |
| xml_etree_generate         | 85.2 ms                                                | 86.9 ms: 1.02x slower                                                 |
| fannkuch                   | 372 ms                                                 | 381 ms: 1.02x slower                                                  |
| xml_etree_parse            | 139 ms                                                 | 142 ms: 1.03x slower                                                  |
| json_loads                 | 26.5 us                                                | 27.4 us: 1.03x slower                                                 |
| pickle_pure_python         | 308 us                                                 | 319 us: 1.04x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 61.2 ms: 1.04x slower                                                 |
| coroutines                 | 23.9 ms                                                | 24.9 ms: 1.04x slower                                                 |
| django_template            | 34.7 ms                                                | 36.2 ms: 1.04x slower                                                 |
| asyncio_websockets         | 517 ms                                                 | 543 ms: 1.05x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 21.7 ms: 1.06x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.68 ms: 1.07x slower                                                 |
| pickle_dict                | 31.8 us                                                | 34.3 us: 1.08x slower                                                 |
| unpickle                   | 14.1 us                                                | 15.2 us: 1.08x slower                                                 |
| unpickle_list              | 4.67 us                                                | 5.06 us: 1.08x slower                                                 |
| pickle_list                | 4.77 us                                                | 5.18 us: 1.09x slower                                                 |
| mako                       | 11.0 ms                                                | 12.0 ms: 1.09x slower                                                 |
| regex_dna                  | 168 ms                                                 | 184 ms: 1.10x slower                                                  |
| coverage                   | 71.4 ms                                                | 82.8 ms: 1.16x slower                                                 |
| pickle                     | 10.9 us                                                | 13.1 us: 1.19x slower                                                 |
| gc_traversal               | 3.46 ms                                                | 4.19 ms: 1.21x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.34 ms: 1.43x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.82 ms: 1.67x slower                                                 |
| telco                      | 6.53 ms                                                | 162 ms: 24.86x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 299 ms: 27.65x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (4): sqlite_synth, typing_runtime_protocols, json, sympy_expand
Ignored benchmarks (18) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: 2to3, aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20260509-3.16.0a0-cc5cf14/bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.061x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.17x