# Results vs. base

- fork: colesbury
- ref: gh_142472_stackrefs
- machine: linux-x86_64
- commit hash: 7cfe81b
- commit date: 2025-12-11
- overall geometric mean: 1.002x slower
- HPT reliability: 96.18%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251211-vultr-x86_64-python-387f88cac1e911672f63-3.15.0a2+-387f88c | bm-20251211-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-7cfe81b |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 246 ms                                                                 | 248 ms: 1.01x slower                                                     |
| docutils       | 2.55 sec                                                               | 2.57 sec: 1.00x slower                                                   |
| html5lib       | 59.5 ms                                                                | 60.2 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20251211-vultr-x86_64-python-387f88cac1e911672f63-3.15.0a2+-387f88c | bm-20251211-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-7cfe81b |
|-------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_generators        | 344 ms                                                                 | 338 ms: 1.02x faster                                                     |
| coroutines              | 23.8 ms                                                                | 23.5 ms: 1.01x faster                                                    |
| async_tree_cpu_io_mixed | 481 ms                                                                 | 490 ms: 1.02x slower                                                     |
| Geometric mean          | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (8): async_tree_io, async_tree_none_tg, asyncio_websockets, async_tree_io_tg, async_tree_memoization_tg, async_tree_none, async_tree_memoization, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251211-vultr-x86_64-python-387f88cac1e911672f63-3.15.0a2+-387f88c | bm-20251211-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-7cfe81b |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 202 ms                                                                 | 206 ms: 1.02x slower                                                     |
| nbody          | 88.6 ms                                                                | 91.5 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                             |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251211-vultr-x86_64-python-387f88cac1e911672f63-3.15.0a2+-387f88c | bm-20251211-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-7cfe81b |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_dna      | 173 ms                                                                 | 169 ms: 1.03x faster                                                     |
| regex_effbot   | 2.80 ms                                                                | 2.75 ms: 1.02x faster                                                    |
| regex_v8       | 22.3 ms                                                                | 21.9 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20251211-vultr-x86_64-python-387f88cac1e911672f63-3.15.0a2+-387f88c | bm-20251211-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-7cfe81b |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse      | 133 ms                                                                 | 131 ms: 1.02x faster                                                     |
| unpickle_pure_python | 214 us                                                                 | 211 us: 1.01x faster                                                     |
| xml_etree_generate   | 82.8 ms                                                                | 82.2 ms: 1.01x faster                                                    |
| pickle_pure_python   | 306 us                                                                 | 307 us: 1.00x slower                                                     |
| json_loads           | 27.7 us                                                                | 27.9 us: 1.01x slower                                                    |
| json_dumps           | 9.93 ms                                                                | 10.0 ms: 1.01x slower                                                    |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (3): xml_etree_iterparse, xml_etree_process, tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251211-vultr-x86_64-python-387f88cac1e911672f63-3.15.0a2+-387f88c | bm-20251211-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-7cfe81b |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 12.5 ms                                                                | 12.5 ms: 1.00x slower                                                    |
| python_startup_no_site | 7.26 ms                                                                | 7.29 ms: 1.00x slower                                                    |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20251211-vultr-x86_64-python-387f88cac1e911672f63-3.15.0a2+-387f88c | bm-20251211-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-7cfe81b |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 20.6 ms                                                                | 20.6 ms: 1.00x faster                                                    |
| genshi_xml      | 48.2 ms                                                                | 48.5 ms: 1.01x slower                                                    |
| django_template | 34.7 ms                                                                | 35.0 ms: 1.01x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark               | bm-20251211-vultr-x86_64-python-387f88cac1e911672f63-3.15.0a2+-387f88c | bm-20251211-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-7cfe81b |
|-------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| bench_mp_pool           | 363 ms                                                                 | 315 ms: 1.15x faster                                                     |
| logging_format          | 6.83 us                                                                | 6.50 us: 1.05x faster                                                    |
| scimark_fft             | 309 ms                                                                 | 300 ms: 1.03x faster                                                     |
| logging_simple          | 5.93 us                                                                | 5.78 us: 1.03x faster                                                    |
| regex_dna               | 173 ms                                                                 | 169 ms: 1.03x faster                                                     |
| scimark_sparse_mat_mult | 4.38 ms                                                                | 4.28 ms: 1.02x faster                                                    |
| async_generators        | 344 ms                                                                 | 338 ms: 1.02x faster                                                     |
| regex_effbot            | 2.80 ms                                                                | 2.75 ms: 1.02x faster                                                    |
| xml_etree_parse         | 133 ms                                                                 | 131 ms: 1.02x faster                                                     |
| coverage                | 82.3 ms                                                                | 80.8 ms: 1.02x faster                                                    |
| pycparser               | 1.11 sec                                                               | 1.09 sec: 1.02x faster                                                   |
| regex_v8                | 22.3 ms                                                                | 21.9 ms: 1.02x faster                                                    |
| sympy_expand            | 476 ms                                                                 | 469 ms: 1.01x faster                                                     |
| coroutines              | 23.8 ms                                                                | 23.5 ms: 1.01x faster                                                    |
| sqlglot_v2_normalize    | 103 ms                                                                 | 102 ms: 1.01x faster                                                     |
| scimark_sor             | 108 ms                                                                 | 107 ms: 1.01x faster                                                     |
| unpickle_pure_python    | 214 us                                                                 | 211 us: 1.01x faster                                                     |
| logging_silent          | 99.9 ns                                                                | 98.9 ns: 1.01x faster                                                    |
| meteor_contest          | 101 ms                                                                 | 100 ms: 1.01x faster                                                     |
| xml_etree_generate      | 82.8 ms                                                                | 82.2 ms: 1.01x faster                                                    |
| sqlglot_v2_optimize     | 51.3 ms                                                                | 50.9 ms: 1.01x faster                                                    |
| mdp                     | 1.16 sec                                                               | 1.15 sec: 1.01x faster                                                   |
| hexiom                  | 5.76 ms                                                                | 5.73 ms: 1.01x faster                                                    |
| nqueens                 | 80.0 ms                                                                | 79.6 ms: 1.00x faster                                                    |
| genshi_text             | 20.6 ms                                                                | 20.6 ms: 1.00x faster                                                    |
| deltablue               | 3.31 ms                                                                | 3.30 ms: 1.00x faster                                                    |
| sympy_sum               | 154 ms                                                                 | 154 ms: 1.00x faster                                                     |
| python_startup          | 12.5 ms                                                                | 12.5 ms: 1.00x slower                                                    |
| python_startup_no_site  | 7.26 ms                                                                | 7.29 ms: 1.00x slower                                                    |
| bpe_tokeniser           | 4.19 sec                                                               | 4.21 sec: 1.00x slower                                                   |
| chaos                   | 56.5 ms                                                                | 56.7 ms: 1.00x slower                                                    |
| docutils                | 2.55 sec                                                               | 2.57 sec: 1.00x slower                                                   |
| pickle_pure_python      | 306 us                                                                 | 307 us: 1.00x slower                                                     |
| scimark_lu              | 108 ms                                                                 | 108 ms: 1.01x slower                                                     |
| 2to3                    | 246 ms                                                                 | 248 ms: 1.01x slower                                                     |
| deepcopy_reduce         | 2.63 us                                                                | 2.65 us: 1.01x slower                                                    |
| json_loads              | 27.7 us                                                                | 27.9 us: 1.01x slower                                                    |
| genshi_xml              | 48.2 ms                                                                | 48.5 ms: 1.01x slower                                                    |
| richards_super          | 47.6 ms                                                                | 48.0 ms: 1.01x slower                                                    |
| go                      | 105 ms                                                                 | 106 ms: 1.01x slower                                                     |
| raytrace                | 251 ms                                                                 | 253 ms: 1.01x slower                                                     |
| django_template         | 34.7 ms                                                                | 35.0 ms: 1.01x slower                                                    |
| shortest_path           | 431 ms                                                                 | 435 ms: 1.01x slower                                                     |
| subparsers              | 9.26 ms                                                                | 9.35 ms: 1.01x slower                                                    |
| json_dumps              | 9.93 ms                                                                | 10.0 ms: 1.01x slower                                                    |
| pyflate                 | 412 ms                                                                 | 417 ms: 1.01x slower                                                     |
| scimark_monte_carlo     | 62.8 ms                                                                | 63.5 ms: 1.01x slower                                                    |
| html5lib                | 59.5 ms                                                                | 60.2 ms: 1.01x slower                                                    |
| crypto_pyaes            | 69.0 ms                                                                | 69.9 ms: 1.01x slower                                                    |
| fannkuch                | 390 ms                                                                 | 395 ms: 1.01x slower                                                     |
| many_optionals          | 938 us                                                                 | 952 us: 1.01x slower                                                     |
| gc_traversal            | 4.32 ms                                                                | 4.39 ms: 1.02x slower                                                    |
| richards                | 41.6 ms                                                                | 42.2 ms: 1.02x slower                                                    |
| pidigits                | 202 ms                                                                 | 206 ms: 1.02x slower                                                     |
| connected_components    | 386 ms                                                                 | 393 ms: 1.02x slower                                                     |
| thrift                  | 757 us                                                                 | 770 us: 1.02x slower                                                     |
| deepcopy_memo           | 26.9 us                                                                | 27.4 us: 1.02x slower                                                    |
| async_tree_cpu_io_mixed | 481 ms                                                                 | 490 ms: 1.02x slower                                                     |
| pprint_safe_repr        | 696 ms                                                                 | 710 ms: 1.02x slower                                                     |
| comprehensions          | 15.8 us                                                                | 16.1 us: 1.02x slower                                                    |
| telco                   | 158 ms                                                                 | 162 ms: 1.02x slower                                                     |
| pprint_pformat          | 1.42 sec                                                               | 1.45 sec: 1.03x slower                                                   |
| pathlib                 | 17.4 ms                                                                | 17.9 ms: 1.03x slower                                                    |
| nbody                   | 88.6 ms                                                                | 91.5 ms: 1.03x slower                                                    |
| generators              | 27.1 ms                                                                | 28.8 ms: 1.06x slower                                                    |
| Geometric mean          | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (29): float, sqlite_synth, async_tree_io, sympy_str, sphinx, bench_thread_pool, sqlglot_v2_parse, pylint, xml_etree_iterparse, k_core, sympy_integrate, create_gc_cycles, dulwich_log, json, async_tree_none_tg, asyncio_websockets, typing_runtime_protocols, regex_compile, async_tree_io_tg, mako, sqlglot_v2_transpile, deepcopy, xml_etree_process, tomli_loads, async_tree_memoization_tg, spectral_norm, async_tree_none, async_tree_memoization, async_tree_cpu_io_mixed_tg

- Geometric mean (including insignificant results): 1.002x slower

# HPT report

- Reliability score: 96.18% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x