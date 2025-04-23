# Results vs. base

- fork: nascheme
- ref: gh_127266_type_slots
- machine: linux-x86_64
- commit hash: 986f23a
- commit date: 2025-04-22
- overall geometric mean: 1.002x faster
- HPT reliability: 65.97%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250422-vultr-x86_64-python-b5bf8c80a921679b2354-3.14.0a7+-b5bf8c8 | bm-20250422-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-986f23a |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 280 ms                                                                 | 281 ms: 1.00x slower                                                     |
| docutils       | 2.68 sec                                                               | 2.70 sec: 1.01x slower                                                   |
| html5lib       | 64.4 ms                                                                | 67.0 ms: 1.04x slower                                                    |
| sphinx         | 1.06 sec                                                               | 1.07 sec: 1.00x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250422-vultr-x86_64-python-b5bf8c80a921679b2354-3.14.0a7+-b5bf8c8 | bm-20250422-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-986f23a |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_generators           | 364 ms                                                                 | 358 ms: 1.02x faster                                                     |
| async_tree_cpu_io_mixed_tg | 475 ms                                                                 | 468 ms: 1.02x faster                                                     |
| async_tree_cpu_io_mixed    | 501 ms                                                                 | 494 ms: 1.01x faster                                                     |
| async_tree_io_tg           | 524 ms                                                                 | 519 ms: 1.01x faster                                                     |
| coroutines                 | 22.5 ms                                                                | 22.8 ms: 1.01x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (6): async_tree_memoization_tg, async_tree_none_tg, async_tree_memoization, asyncio_websockets, async_tree_io, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250422-vultr-x86_64-python-b5bf8c80a921679b2354-3.14.0a7+-b5bf8c8 | bm-20250422-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-986f23a |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 199 ms                                                                 | 186 ms: 1.07x faster                                                     |
| float          | 68.3 ms                                                                | 67.2 ms: 1.02x faster                                                    |
| nbody          | 110 ms                                                                 | 110 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250422-vultr-x86_64-python-b5bf8c80a921679b2354-3.14.0a7+-b5bf8c8 | bm-20250422-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-986f23a |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 21.2 ms                                                                | 21.0 ms: 1.01x faster                                                    |
| regex_effbot   | 2.79 ms                                                                | 2.78 ms: 1.00x faster                                                    |
| regex_compile  | 143 ms                                                                 | 143 ms: 1.00x slower                                                     |
| regex_dna      | 179 ms                                                                 | 180 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250422-vultr-x86_64-python-b5bf8c80a921679b2354-3.14.0a7+-b5bf8c8 | bm-20250422-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-986f23a |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 88.1 ms                                                                | 86.8 ms: 1.01x faster                                                    |
| tomli_loads          | 2.08 sec                                                               | 2.07 sec: 1.01x faster                                                   |
| unpickle_pure_python | 226 us                                                                 | 228 us: 1.01x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (6): xml_etree_generate, json_dumps, xml_etree_process, pickle_pure_python, xml_etree_parse, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250422-vultr-x86_64-python-b5bf8c80a921679b2354-3.14.0a7+-b5bf8c8 | bm-20250422-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-986f23a |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 15.8 ms                                                                | 15.8 ms: 1.00x faster                                                    |
| python_startup_no_site | 11.1 ms                                                                | 11.1 ms: 1.00x faster                                                    |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250422-vultr-x86_64-python-b5bf8c80a921679b2354-3.14.0a7+-b5bf8c8 | bm-20250422-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-986f23a |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 15.1 ms                                                                | 15.2 ms: 1.01x slower                                                    |
| genshi_xml      | 54.7 ms                                                                | 55.4 ms: 1.01x slower                                                    |
| django_template | 39.4 ms                                                                | 40.4 ms: 1.03x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.01x slower                                                             |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20250422-vultr-x86_64-python-b5bf8c80a921679b2354-3.14.0a7+-b5bf8c8 | bm-20250422-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-986f23a |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits                   | 199 ms                                                                 | 186 ms: 1.07x faster                                                     |
| generators                 | 32.2 ms                                                                | 30.1 ms: 1.07x faster                                                    |
| scimark_fft                | 349 ms                                                                 | 335 ms: 1.04x faster                                                     |
| crypto_pyaes               | 83.4 ms                                                                | 81.8 ms: 1.02x faster                                                    |
| logging_format             | 7.93 us                                                                | 7.78 us: 1.02x faster                                                    |
| richards_super             | 58.4 ms                                                                | 57.3 ms: 1.02x faster                                                    |
| async_generators           | 364 ms                                                                 | 358 ms: 1.02x faster                                                     |
| async_tree_cpu_io_mixed_tg | 475 ms                                                                 | 468 ms: 1.02x faster                                                     |
| float                      | 68.3 ms                                                                | 67.2 ms: 1.02x faster                                                    |
| scimark_sparse_mat_mult    | 5.08 ms                                                                | 5.01 ms: 1.02x faster                                                    |
| xml_etree_iterparse        | 88.1 ms                                                                | 86.8 ms: 1.01x faster                                                    |
| async_tree_cpu_io_mixed    | 501 ms                                                                 | 494 ms: 1.01x faster                                                     |
| regex_v8                   | 21.2 ms                                                                | 21.0 ms: 1.01x faster                                                    |
| typing_runtime_protocols   | 191 us                                                                 | 188 us: 1.01x faster                                                     |
| async_tree_io_tg           | 524 ms                                                                 | 519 ms: 1.01x faster                                                     |
| richards                   | 50.2 ms                                                                | 49.7 ms: 1.01x faster                                                    |
| sqlite_synth               | 2.00 us                                                                | 1.99 us: 1.01x faster                                                    |
| scimark_monte_carlo        | 74.0 ms                                                                | 73.4 ms: 1.01x faster                                                    |
| hexiom                     | 6.60 ms                                                                | 6.55 ms: 1.01x faster                                                    |
| connected_components       | 482 ms                                                                 | 479 ms: 1.01x faster                                                     |
| nbody                      | 110 ms                                                                 | 110 ms: 1.01x faster                                                     |
| tomli_loads                | 2.08 sec                                                               | 2.07 sec: 1.01x faster                                                   |
| mdp                        | 1.31 sec                                                               | 1.31 sec: 1.01x faster                                                   |
| logging_simple             | 7.00 us                                                                | 6.96 us: 1.01x faster                                                    |
| bpe_tokeniser              | 4.36 sec                                                               | 4.34 sec: 1.00x faster                                                   |
| gc_traversal               | 1.80 ms                                                                | 1.79 ms: 1.00x faster                                                    |
| regex_effbot               | 2.79 ms                                                                | 2.78 ms: 1.00x faster                                                    |
| python_startup             | 15.8 ms                                                                | 15.8 ms: 1.00x faster                                                    |
| python_startup_no_site     | 11.1 ms                                                                | 11.1 ms: 1.00x faster                                                    |
| 2to3                       | 280 ms                                                                 | 281 ms: 1.00x slower                                                     |
| pprint_safe_repr           | 762 ms                                                                 | 764 ms: 1.00x slower                                                     |
| sympy_integrate            | 22.0 ms                                                                | 22.1 ms: 1.00x slower                                                    |
| deepcopy_memo              | 34.6 us                                                                | 34.8 us: 1.00x slower                                                    |
| many_optionals             | 1.10 ms                                                                | 1.11 ms: 1.00x slower                                                    |
| chaos                      | 60.7 ms                                                                | 61.0 ms: 1.00x slower                                                    |
| regex_compile              | 143 ms                                                                 | 143 ms: 1.00x slower                                                     |
| pyflate                    | 457 ms                                                                 | 459 ms: 1.00x slower                                                     |
| deepcopy_reduce            | 3.00 us                                                                | 3.02 us: 1.00x slower                                                    |
| sphinx                     | 1.06 sec                                                               | 1.07 sec: 1.00x slower                                                   |
| nqueens                    | 86.8 ms                                                                | 87.2 ms: 1.00x slower                                                    |
| regex_dna                  | 179 ms                                                                 | 180 ms: 1.01x slower                                                     |
| pycparser                  | 1.13 sec                                                               | 1.13 sec: 1.01x slower                                                   |
| raytrace                   | 287 ms                                                                 | 288 ms: 1.01x slower                                                     |
| docutils                   | 2.68 sec                                                               | 2.70 sec: 1.01x slower                                                   |
| go                         | 123 ms                                                                 | 124 ms: 1.01x slower                                                     |
| spectral_norm              | 101 ms                                                                 | 102 ms: 1.01x slower                                                     |
| unpickle_pure_python       | 226 us                                                                 | 228 us: 1.01x slower                                                     |
| mako                       | 15.1 ms                                                                | 15.2 ms: 1.01x slower                                                    |
| scimark_lu                 | 128 ms                                                                 | 130 ms: 1.01x slower                                                     |
| genshi_xml                 | 54.7 ms                                                                | 55.4 ms: 1.01x slower                                                    |
| telco                      | 8.39 ms                                                                | 8.49 ms: 1.01x slower                                                    |
| logging_silent             | 100 ns                                                                 | 102 ns: 1.01x slower                                                     |
| coroutines                 | 22.5 ms                                                                | 22.8 ms: 1.01x slower                                                    |
| pprint_pformat             | 1.57 sec                                                               | 1.59 sec: 1.01x slower                                                   |
| subparsers                 | 24.2 ms                                                                | 24.6 ms: 1.02x slower                                                    |
| django_template            | 39.4 ms                                                                | 40.4 ms: 1.03x slower                                                    |
| html5lib                   | 64.4 ms                                                                | 67.0 ms: 1.04x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (38): async_tree_memoization_tg, shortest_path, sympy_expand, create_gc_cycles, pathlib, dulwich_log, sympy_sum, k_core, sqlglot_v2_parse, sympy_str, xml_etree_generate, json_dumps, xml_etree_process, sqlglot_v2_transpile, pylint, json, async_tree_none_tg, coverage, deepcopy, meteor_contest, fannkuch, bench_thread_pool, comprehensions, async_tree_memoization, sqlalchemy_imperative, sqlglot_v2_optimize, genshi_text, asyncio_websockets, bench_mp_pool, scimark_sor, sqlalchemy_declarative, deltablue, pickle_pure_python, xml_etree_parse, json_loads, async_tree_io, async_tree_none, sqlglot_v2_normalize

- Geometric mean (including insignificant results): 1.002x faster

# HPT report

- Reliability score: 65.97% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x