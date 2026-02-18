# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: no_invalidate_func
- machine: linux-x86_64
- commit hash: 170839d
- commit date: 2026-02-18
- overall geometric mean: 1.093x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260218-vultr-x86_64-Fidget%2dSpinner-no_invalidate_func-3.15.0a6+-170839d |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 250 ms: 1.04x faster                                                           |
| docutils       | 2.62 sec                                                     | 2.77 sec: 1.06x slower                                                         |
| html5lib       | 67.0 ms                                                      | 63.6 ms: 1.05x faster                                                          |
| Geometric mean | (ref)                                                        | 1.01x faster                                                                   |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260218-vultr-x86_64-Fidget%2dSpinner-no_invalidate_func-3.15.0a6+-170839d |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 560 ms: 1.63x faster                                                           |
| async_tree_memoization     | 461 ms                                                       | 291 ms: 1.58x faster                                                           |
| async_tree_io              | 876 ms                                                       | 591 ms: 1.48x faster                                                           |
| async_tree_none            | 354 ms                                                       | 240 ms: 1.47x faster                                                           |
| async_tree_memoization_tg  | 414 ms                                                       | 293 ms: 1.41x faster                                                           |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 472 ms: 1.41x faster                                                           |
| async_tree_none_tg         | 336 ms                                                       | 245 ms: 1.37x faster                                                           |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 483 ms: 1.32x faster                                                           |
| async_generators           | 377 ms                                                       | 366 ms: 1.03x faster                                                           |
| coroutines                 | 23.6 ms                                                      | 24.4 ms: 1.03x slower                                                          |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                           |
| Geometric mean             | (ref)                                                        | 1.31x faster                                                                   |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260218-vultr-x86_64-Fidget%2dSpinner-no_invalidate_func-3.15.0a6+-170839d |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 60.8 ms: 1.27x faster                                                          |
| nbody          | 85.1 ms                                                      | 74.2 ms: 1.15x faster                                                          |
| pidigits       | 217 ms                                                       | 202 ms: 1.07x faster                                                           |
| Geometric mean | (ref)                                                        | 1.16x faster                                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260218-vultr-x86_64-Fidget%2dSpinner-no_invalidate_func-3.15.0a6+-170839d |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.89 ms: 1.07x faster                                                          |
| regex_compile  | 132 ms                                                       | 125 ms: 1.05x faster                                                           |
| regex_v8       | 22.7 ms                                                      | 22.0 ms: 1.03x faster                                                          |
| regex_dna      | 180 ms                                                       | 185 ms: 1.02x slower                                                           |
| Geometric mean | (ref)                                                        | 1.03x faster                                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260218-vultr-x86_64-Fidget%2dSpinner-no_invalidate_func-3.15.0a6+-170839d |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                     | 1.57 sec: 1.28x faster                                                         |
| json_dumps           | 10.5 ms                                                      | 8.96 ms: 1.18x faster                                                          |
| xml_etree_iterparse  | 94.9 ms                                                      | 84.1 ms: 1.13x faster                                                          |
| xml_etree_generate   | 85.4 ms                                                      | 77.6 ms: 1.10x faster                                                          |
| xml_etree_process    | 59.3 ms                                                      | 54.1 ms: 1.10x faster                                                          |
| unpickle_pure_python | 210 us                                                       | 200 us: 1.05x faster                                                           |
| xml_etree_parse      | 136 ms                                                       | 132 ms: 1.03x faster                                                           |
| pickle_pure_python   | 294 us                                                       | 311 us: 1.06x slower                                                           |
| json_loads           | 27.0 us                                                      | 28.8 us: 1.07x slower                                                          |
| Geometric mean       | (ref)                                                        | 1.08x faster                                                                   |

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260218-vultr-x86_64-Fidget%2dSpinner-no_invalidate_func-3.15.0a6+-170839d |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| python_startup | 11.0 ms                                                      | 12.6 ms: 1.15x slower                                                          |
| Geometric mean | (ref)                                                        | 1.07x slower                                                                   |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260218-vultr-x86_64-Fidget%2dSpinner-no_invalidate_func-3.15.0a6+-170839d |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| mako            | 11.3 ms                                                      | 10.5 ms: 1.08x faster                                                          |
| django_template | 34.1 ms                                                      | 36.0 ms: 1.05x slower                                                          |
| Geometric mean  | (ref)                                                        | 1.01x faster                                                                   |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260218-vultr-x86_64-Fidget%2dSpinner-no_invalidate_func-3.15.0a6+-170839d |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| richards                   | 45.2 ms                                                      | 18.4 ms: 2.45x faster                                                          |
| richards_super             | 51.6 ms                                                      | 22.4 ms: 2.31x faster                                                          |
| mdp                        | 2.36 sec                                                     | 1.21 sec: 1.95x faster                                                         |
| deepcopy_memo              | 39.1 us                                                      | 23.0 us: 1.70x faster                                                          |
| async_tree_io_tg           | 913 ms                                                       | 560 ms: 1.63x faster                                                           |
| async_tree_memoization     | 461 ms                                                       | 291 ms: 1.58x faster                                                           |
| deepcopy                   | 355 us                                                       | 228 us: 1.56x faster                                                           |
| scimark_sor                | 134 ms                                                       | 87.0 ms: 1.55x faster                                                          |
| async_tree_io              | 876 ms                                                       | 591 ms: 1.48x faster                                                           |
| async_tree_none            | 354 ms                                                       | 240 ms: 1.47x faster                                                           |
| go                         | 141 ms                                                       | 99.3 ms: 1.42x faster                                                          |
| async_tree_memoization_tg  | 414 ms                                                       | 293 ms: 1.41x faster                                                           |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 472 ms: 1.41x faster                                                           |
| scimark_lu                 | 113 ms                                                       | 80.6 ms: 1.40x faster                                                          |
| async_tree_none_tg         | 336 ms                                                       | 245 ms: 1.37x faster                                                           |
| scimark_fft                | 349 ms                                                       | 259 ms: 1.35x faster                                                           |
| spectral_norm              | 111 ms                                                       | 82.7 ms: 1.34x faster                                                          |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 483 ms: 1.32x faster                                                           |
| deepcopy_reduce            | 3.11 us                                                      | 2.41 us: 1.29x faster                                                          |
| tomli_loads                | 2.01 sec                                                     | 1.57 sec: 1.28x faster                                                         |
| float                      | 77.5 ms                                                      | 60.8 ms: 1.27x faster                                                          |
| scimark_monte_carlo        | 65.4 ms                                                      | 52.7 ms: 1.24x faster                                                          |
| pyflate                    | 449 ms                                                       | 370 ms: 1.21x faster                                                           |
| logging_silent             | 103 ns                                                       | 84.8 ns: 1.21x faster                                                          |
| json_dumps                 | 10.5 ms                                                      | 8.96 ms: 1.18x faster                                                          |
| pprint_safe_repr           | 738 ms                                                       | 637 ms: 1.16x faster                                                           |
| nbody                      | 85.1 ms                                                      | 74.2 ms: 1.15x faster                                                          |
| pprint_pformat             | 1.50 sec                                                     | 1.31 sec: 1.14x faster                                                         |
| xml_etree_iterparse        | 94.9 ms                                                      | 84.1 ms: 1.13x faster                                                          |
| comprehensions             | 16.5 us                                                      | 14.6 us: 1.12x faster                                                          |
| deltablue                  | 3.12 ms                                                      | 2.81 ms: 1.11x faster                                                          |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.26 ms: 1.11x faster                                                          |
| bpe_tokeniser              | 4.45 sec                                                     | 4.02 sec: 1.11x faster                                                         |
| pathlib                    | 19.2 ms                                                      | 17.4 ms: 1.10x faster                                                          |
| xml_etree_generate         | 85.4 ms                                                      | 77.6 ms: 1.10x faster                                                          |
| xml_etree_process          | 59.3 ms                                                      | 54.1 ms: 1.10x faster                                                          |
| pylint                     | 317 ms                                                       | 292 ms: 1.09x faster                                                           |
| mako                       | 11.3 ms                                                      | 10.5 ms: 1.08x faster                                                          |
| pidigits                   | 217 ms                                                       | 202 ms: 1.07x faster                                                           |
| regex_effbot               | 3.08 ms                                                      | 2.89 ms: 1.07x faster                                                          |
| regex_compile              | 132 ms                                                       | 125 ms: 1.05x faster                                                           |
| html5lib                   | 67.0 ms                                                      | 63.6 ms: 1.05x faster                                                          |
| fannkuch                   | 370 ms                                                       | 352 ms: 1.05x faster                                                           |
| unpickle_pure_python       | 210 us                                                       | 200 us: 1.05x faster                                                           |
| chaos                      | 57.3 ms                                                      | 54.7 ms: 1.05x faster                                                          |
| logging_simple             | 6.16 us                                                      | 5.89 us: 1.05x faster                                                          |
| hexiom                     | 5.99 ms                                                      | 5.76 ms: 1.04x faster                                                          |
| 2to3                       | 260 ms                                                       | 250 ms: 1.04x faster                                                           |
| dulwich_log                | 74.8 ms                                                      | 72.1 ms: 1.04x faster                                                          |
| logging_format             | 6.84 us                                                      | 6.62 us: 1.03x faster                                                          |
| xml_etree_parse            | 136 ms                                                       | 132 ms: 1.03x faster                                                           |
| async_generators           | 377 ms                                                       | 366 ms: 1.03x faster                                                           |
| regex_v8                   | 22.7 ms                                                      | 22.0 ms: 1.03x faster                                                          |
| crypto_pyaes               | 67.9 ms                                                      | 66.0 ms: 1.03x faster                                                          |
| meteor_contest             | 102 ms                                                       | 99.4 ms: 1.02x faster                                                          |
| sqlite_synth               | 2.21 us                                                      | 2.16 us: 1.02x faster                                                          |
| sympy_integrate            | 19.8 ms                                                      | 19.6 ms: 1.01x faster                                                          |
| coverage                   | 83.0 ms                                                      | 82.3 ms: 1.01x faster                                                          |
| generators                 | 28.8 ms                                                      | 29.1 ms: 1.01x slower                                                          |
| pycparser                  | 1.12 sec                                                     | 1.13 sec: 1.01x slower                                                         |
| json                       | 4.93 ms                                                      | 5.02 ms: 1.02x slower                                                          |
| regex_dna                  | 180 ms                                                       | 185 ms: 1.02x slower                                                           |
| coroutines                 | 23.6 ms                                                      | 24.4 ms: 1.03x slower                                                          |
| sympy_sum                  | 156 ms                                                       | 161 ms: 1.04x slower                                                           |
| typing_runtime_protocols   | 155 us                                                       | 160 us: 1.04x slower                                                           |
| thrift                     | 778 us                                                       | 808 us: 1.04x slower                                                           |
| sympy_str                  | 275 ms                                                       | 286 ms: 1.04x slower                                                           |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                           |
| django_template            | 34.1 ms                                                      | 36.0 ms: 1.05x slower                                                          |
| pickle_pure_python         | 294 us                                                       | 311 us: 1.06x slower                                                           |
| docutils                   | 2.62 sec                                                     | 2.77 sec: 1.06x slower                                                         |
| json_loads                 | 27.0 us                                                      | 28.8 us: 1.07x slower                                                          |
| sympy_expand               | 457 ms                                                       | 491 ms: 1.07x slower                                                           |
| raytrace                   | 253 ms                                                       | 288 ms: 1.14x slower                                                           |
| python_startup             | 11.0 ms                                                      | 12.6 ms: 1.15x slower                                                          |
| gc_traversal               | 3.14 ms                                                      | 4.16 ms: 1.32x slower                                                          |
| create_gc_cycles           | 1.34 ms                                                      | 1.83 ms: 1.37x slower                                                          |
| bench_thread_pool          | 919 us                                                       | 1.31 ms: 1.42x slower                                                          |
| bench_mp_pool              | 11.0 ms                                                      | 214 ms: 19.49x slower                                                          |
| telco                      | 7.82 ms                                                      | 160 ms: 20.50x slower                                                          |
| Geometric mean             | (ref)                                                        | 1.05x faster                                                                   |

Benchmark hidden because not significant (2): nqueens, python_startup_no_site
Ignored benchmarks (20) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260218-3.15.0a6+-170839d-JIT/bm-20260218-vultr-x86_64-Fidget%2dSpinner-no_invalidate_func-3.15.0a6+-170839d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.093x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.21x