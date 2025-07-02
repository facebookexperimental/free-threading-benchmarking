# Results vs. base

- fork: Fidget-Spinner
- ref: tos_caching_rebased
- machine: linux-x86_64
- commit hash: 50081dc
- commit date: 2025-06-24
- overall geometric mean: 1.005x faster
- HPT reliability: 99.80%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250624-vultr-x86_64-python-bda121862e7d7f4684d9-3.15.0a0-bda1218 | bm-20250624-vultr-x86_64-Fidget%2dSpinner-tos_caching_rebased-3.15.0a0-50081dc |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| docutils       | 2.59 sec                                                              | 2.58 sec: 1.01x faster                                                         |
| html5lib       | 62.3 ms                                                               | 61.6 ms: 1.01x faster                                                          |
| sphinx         | 991 ms                                                                | 979 ms: 1.01x faster                                                           |
| Geometric mean | (ref)                                                                 | 1.01x faster                                                                   |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250624-vultr-x86_64-python-bda121862e7d7f4684d9-3.15.0a0-bda1218 | bm-20250624-vultr-x86_64-Fidget%2dSpinner-tos_caching_rebased-3.15.0a0-50081dc |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 506 ms                                                                | 498 ms: 1.02x faster                                                           |
| async_tree_cpu_io_mixed    | 505 ms                                                                | 498 ms: 1.01x faster                                                           |
| async_generators           | 352 ms                                                                | 351 ms: 1.00x faster                                                           |
| async_tree_none_tg         | 255 ms                                                                | 258 ms: 1.01x slower                                                           |
| Geometric mean             | (ref)                                                                 | 1.00x faster                                                                   |

Benchmark hidden because not significant (7): async_tree_io_tg, async_tree_io, coroutines, asyncio_websockets, async_tree_memoization_tg, async_tree_memoization, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250624-vultr-x86_64-python-bda121862e7d7f4684d9-3.15.0a0-bda1218 | bm-20250624-vultr-x86_64-Fidget%2dSpinner-tos_caching_rebased-3.15.0a0-50081dc |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| nbody          | 90.0 ms                                                               | 76.1 ms: 1.18x faster                                                          |
| float          | 65.2 ms                                                               | 64.5 ms: 1.01x faster                                                          |
| pidigits       | 203 ms                                                                | 209 ms: 1.03x slower                                                           |
| Geometric mean | (ref)                                                                 | 1.05x faster                                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250624-vultr-x86_64-python-bda121862e7d7f4684d9-3.15.0a0-bda1218 | bm-20250624-vultr-x86_64-Fidget%2dSpinner-tos_caching_rebased-3.15.0a0-50081dc |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| regex_effbot   | 2.89 ms                                                               | 2.62 ms: 1.10x faster                                                          |
| regex_v8       | 23.0 ms                                                               | 20.9 ms: 1.10x faster                                                          |
| regex_dna      | 178 ms                                                                | 171 ms: 1.04x faster                                                           |
| Geometric mean | (ref)                                                                 | 1.06x faster                                                                   |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250624-vultr-x86_64-python-bda121862e7d7f4684d9-3.15.0a0-bda1218 | bm-20250624-vultr-x86_64-Fidget%2dSpinner-tos_caching_rebased-3.15.0a0-50081dc |
|----------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| xml_etree_parse      | 130 ms                                                                | 128 ms: 1.02x faster                                                           |
| xml_etree_process    | 55.2 ms                                                               | 54.7 ms: 1.01x faster                                                          |
| tomli_loads          | 1.78 sec                                                              | 1.77 sec: 1.01x faster                                                         |
| json_loads           | 27.8 us                                                               | 28.0 us: 1.00x slower                                                          |
| unpickle_pure_python | 191 us                                                                | 194 us: 1.02x slower                                                           |
| Geometric mean       | (ref)                                                                 | 1.00x faster                                                                   |

Benchmark hidden because not significant (4): pickle_pure_python, json_dumps, xml_etree_iterparse, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250624-vultr-x86_64-python-bda121862e7d7f4684d9-3.15.0a0-bda1218 | bm-20250624-vultr-x86_64-Fidget%2dSpinner-tos_caching_rebased-3.15.0a0-50081dc |
|------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| python_startup_no_site | 7.33 ms                                                               | 7.35 ms: 1.00x slower                                                          |
| Geometric mean         | (ref)                                                                 | 1.00x slower                                                                   |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250624-vultr-x86_64-python-bda121862e7d7f4684d9-3.15.0a0-bda1218 | bm-20250624-vultr-x86_64-Fidget%2dSpinner-tos_caching_rebased-3.15.0a0-50081dc |
|-----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| genshi_xml      | 49.8 ms                                                               | 48.6 ms: 1.02x faster                                                          |
| django_template | 34.3 ms                                                               | 34.8 ms: 1.01x slower                                                          |
| mako            | 11.2 ms                                                               | 11.5 ms: 1.03x slower                                                          |
| Geometric mean  | (ref)                                                                 | 1.00x slower                                                                   |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20250624-vultr-x86_64-python-bda121862e7d7f4684d9-3.15.0a0-bda1218 | bm-20250624-vultr-x86_64-Fidget%2dSpinner-tos_caching_rebased-3.15.0a0-50081dc |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| nbody                      | 90.0 ms                                                               | 76.1 ms: 1.18x faster                                                          |
| regex_effbot               | 2.89 ms                                                               | 2.62 ms: 1.10x faster                                                          |
| regex_v8                   | 23.0 ms                                                               | 20.9 ms: 1.10x faster                                                          |
| regex_dna                  | 178 ms                                                                | 171 ms: 1.04x faster                                                           |
| scimark_lu                 | 111 ms                                                                | 108 ms: 1.03x faster                                                           |
| logging_format             | 7.44 us                                                               | 7.23 us: 1.03x faster                                                          |
| pycparser                  | 1.17 sec                                                              | 1.14 sec: 1.03x faster                                                         |
| telco                      | 7.25 ms                                                               | 7.06 ms: 1.03x faster                                                          |
| logging_simple             | 6.65 us                                                               | 6.47 us: 1.03x faster                                                          |
| generators                 | 28.6 ms                                                               | 27.9 ms: 1.03x faster                                                          |
| genshi_xml                 | 49.8 ms                                                               | 48.6 ms: 1.02x faster                                                          |
| fannkuch                   | 371 ms                                                                | 362 ms: 1.02x faster                                                           |
| scimark_fft                | 285 ms                                                                | 279 ms: 1.02x faster                                                           |
| xml_etree_parse            | 130 ms                                                                | 128 ms: 1.02x faster                                                           |
| create_gc_cycles           | 1.93 ms                                                               | 1.89 ms: 1.02x faster                                                          |
| async_tree_cpu_io_mixed_tg | 506 ms                                                                | 498 ms: 1.02x faster                                                           |
| richards                   | 31.5 ms                                                               | 31.0 ms: 1.02x faster                                                          |
| deepcopy_reduce            | 2.66 us                                                               | 2.62 us: 1.02x faster                                                          |
| async_tree_cpu_io_mixed    | 505 ms                                                                | 498 ms: 1.01x faster                                                           |
| bpe_tokeniser              | 4.04 sec                                                              | 3.98 sec: 1.01x faster                                                         |
| html5lib                   | 62.3 ms                                                               | 61.6 ms: 1.01x faster                                                          |
| nqueens                    | 76.5 ms                                                               | 75.5 ms: 1.01x faster                                                          |
| subparsers                 | 25.4 ms                                                               | 25.1 ms: 1.01x faster                                                          |
| scimark_monte_carlo        | 60.4 ms                                                               | 59.7 ms: 1.01x faster                                                          |
| deepcopy                   | 254 us                                                                | 251 us: 1.01x faster                                                           |
| sphinx                     | 991 ms                                                                | 979 ms: 1.01x faster                                                           |
| xml_etree_process          | 55.2 ms                                                               | 54.7 ms: 1.01x faster                                                          |
| float                      | 65.2 ms                                                               | 64.5 ms: 1.01x faster                                                          |
| sqlglot_v2_parse           | 1.24 ms                                                               | 1.23 ms: 1.01x faster                                                          |
| sqlglot_v2_transpile       | 1.55 ms                                                               | 1.53 ms: 1.01x faster                                                          |
| logging_silent             | 470 ns                                                                | 466 ns: 1.01x faster                                                           |
| sqlglot_v2_normalize       | 100 ms                                                                | 99.7 ms: 1.01x faster                                                          |
| pyflate                    | 389 ms                                                                | 386 ms: 1.01x faster                                                           |
| tomli_loads                | 1.78 sec                                                              | 1.77 sec: 1.01x faster                                                         |
| docutils                   | 2.59 sec                                                              | 2.58 sec: 1.01x faster                                                         |
| sympy_expand               | 474 ms                                                                | 471 ms: 1.01x faster                                                           |
| sqlglot_v2_optimize        | 50.4 ms                                                               | 50.2 ms: 1.00x faster                                                          |
| mdp                        | 1.16 sec                                                              | 1.16 sec: 1.00x faster                                                         |
| async_generators           | 352 ms                                                                | 351 ms: 1.00x faster                                                           |
| deepcopy_memo              | 28.6 us                                                               | 28.5 us: 1.00x faster                                                          |
| scimark_sparse_mat_mult    | 4.50 ms                                                               | 4.51 ms: 1.00x slower                                                          |
| python_startup_no_site     | 7.33 ms                                                               | 7.35 ms: 1.00x slower                                                          |
| sympy_integrate            | 19.2 ms                                                               | 19.3 ms: 1.00x slower                                                          |
| sympy_sum                  | 155 ms                                                                | 156 ms: 1.00x slower                                                           |
| json_loads                 | 27.8 us                                                               | 28.0 us: 1.00x slower                                                          |
| bench_mp_pool              | 98.5 ms                                                               | 99.2 ms: 1.01x slower                                                          |
| go                         | 117 ms                                                                | 118 ms: 1.01x slower                                                           |
| deltablue                  | 2.86 ms                                                               | 2.90 ms: 1.01x slower                                                          |
| django_template            | 34.3 ms                                                               | 34.8 ms: 1.01x slower                                                          |
| async_tree_none_tg         | 255 ms                                                                | 258 ms: 1.01x slower                                                           |
| comprehensions             | 16.6 us                                                               | 16.9 us: 1.02x slower                                                          |
| unpickle_pure_python       | 191 us                                                                | 194 us: 1.02x slower                                                           |
| scimark_sor                | 107 ms                                                                | 109 ms: 1.02x slower                                                           |
| typing_runtime_protocols   | 155 us                                                                | 158 us: 1.02x slower                                                           |
| connected_components       | 392 ms                                                                | 399 ms: 1.02x slower                                                           |
| mako                       | 11.2 ms                                                               | 11.5 ms: 1.03x slower                                                          |
| pprint_pformat             | 1.70 sec                                                              | 1.75 sec: 1.03x slower                                                         |
| pidigits                   | 203 ms                                                                | 209 ms: 1.03x slower                                                           |
| pprint_safe_repr           | 815 ms                                                                | 843 ms: 1.03x slower                                                           |
| hexiom                     | 6.06 ms                                                               | 6.29 ms: 1.04x slower                                                          |
| gc_traversal               | 4.39 ms                                                               | 4.65 ms: 1.06x slower                                                          |
| Geometric mean             | (ref)                                                                 | 1.01x faster                                                                   |

Benchmark hidden because not significant (33): spectral_norm, richards_super, pickle_pure_python, async_tree_io_tg, async_tree_io, raytrace, json_dumps, pathlib, json, sympy_str, regex_compile, meteor_contest, coroutines, pylint, dulwich_log, bench_thread_pool, 2to3, asyncio_websockets, async_tree_memoization_tg, python_startup, shortest_path, many_optionals, xml_etree_iterparse, coverage, genshi_text, async_tree_memoization, k_core, xml_etree_generate, crypto_pyaes, chaos, thrift, sqlite_synth, async_tree_none

- Geometric mean (including insignificant results): 1.005x faster

# HPT report

- Reliability score: 99.80% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.01x