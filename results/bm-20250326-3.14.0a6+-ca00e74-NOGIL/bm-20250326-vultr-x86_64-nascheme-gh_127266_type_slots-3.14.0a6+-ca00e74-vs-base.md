# Results vs. base

- fork: nascheme
- ref: gh_127266_type_slots
- machine: linux-x86_64
- commit hash: ca00e74
- commit date: 2025-03-26
- overall geometric mean: 1.003x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250326-vultr-x86_64-python-898e6b395e63ad7f8bbe-3.14.0a6+-898e6b3 | bm-20250326-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-ca00e74 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 300 ms                                                                 | 299 ms: 1.00x faster                                                     |
| html5lib       | 69.9 ms                                                                | 72.3 ms: 1.03x slower                                                    |
| sphinx         | 1.10 sec                                                               | 1.09 sec: 1.01x faster                                                   |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                             |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250326-vultr-x86_64-python-898e6b395e63ad7f8bbe-3.14.0a6+-898e6b3 | bm-20250326-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-ca00e74 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| coroutines                 | 24.0 ms                                                                | 23.5 ms: 1.02x faster                                                    |
| async_tree_cpu_io_mixed_tg | 483 ms                                                                 | 476 ms: 1.01x faster                                                     |
| async_tree_cpu_io_mixed    | 519 ms                                                                 | 512 ms: 1.01x faster                                                     |
| async_tree_io              | 587 ms                                                                 | 583 ms: 1.01x faster                                                     |
| async_tree_memoization_tg  | 301 ms                                                                 | 298 ms: 1.01x faster                                                     |
| async_tree_memoization     | 333 ms                                                                 | 331 ms: 1.01x faster                                                     |
| async_generators           | 381 ms                                                                 | 383 ms: 1.01x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (4): async_tree_none_tg, async_tree_io_tg, async_tree_none, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250326-vultr-x86_64-python-898e6b395e63ad7f8bbe-3.14.0a6+-898e6b3 | bm-20250326-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-ca00e74 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 207 ms                                                                 | 204 ms: 1.02x faster                                                     |
| float          | 76.9 ms                                                                | 78.4 ms: 1.02x slower                                                    |
| nbody          | 131 ms                                                                 | 135 ms: 1.03x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250326-vultr-x86_64-python-898e6b395e63ad7f8bbe-3.14.0a6+-898e6b3 | bm-20250326-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-ca00e74 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 21.6 ms                                                                | 22.1 ms: 1.02x slower                                                    |
| regex_dna      | 169 ms                                                                 | 185 ms: 1.09x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                             |

Benchmark hidden because not significant (2): regex_effbot, regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250326-vultr-x86_64-python-898e6b395e63ad7f8bbe-3.14.0a6+-898e6b3 | bm-20250326-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-ca00e74 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_generate   | 97.4 ms                                                                | 94.8 ms: 1.03x faster                                                    |
| xml_etree_process    | 71.0 ms                                                                | 69.2 ms: 1.03x faster                                                    |
| xml_etree_iterparse  | 88.9 ms                                                                | 87.8 ms: 1.01x faster                                                    |
| unpickle_pure_python | 262 us                                                                 | 259 us: 1.01x faster                                                     |
| tomli_loads          | 2.38 sec                                                               | 2.37 sec: 1.01x faster                                                   |
| pickle_pure_python   | 365 us                                                                 | 363 us: 1.01x faster                                                     |
| json_loads           | 29.5 us                                                                | 30.5 us: 1.03x slower                                                    |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (2): xml_etree_parse, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250326-vultr-x86_64-python-898e6b395e63ad7f8bbe-3.14.0a6+-898e6b3 | bm-20250326-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-ca00e74 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 11.1 ms                                                                | 11.1 ms: 1.00x faster                                                    |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250326-vultr-x86_64-python-898e6b395e63ad7f8bbe-3.14.0a6+-898e6b3 | bm-20250326-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-ca00e74 |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| django_template | 43.1 ms                                                                | 42.5 ms: 1.01x faster                                                    |
| genshi_xml      | 60.2 ms                                                                | 59.9 ms: 1.01x faster                                                    |
| mako            | 16.1 ms                                                                | 16.1 ms: 1.00x faster                                                    |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20250326-vultr-x86_64-python-898e6b395e63ad7f8bbe-3.14.0a6+-898e6b3 | bm-20250326-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-ca00e74 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| scimark_lu                 | 145 ms                                                                 | 137 ms: 1.06x faster                                                     |
| sqlglot_v2_normalize       | 123 ms                                                                 | 119 ms: 1.03x faster                                                     |
| xml_etree_generate         | 97.4 ms                                                                | 94.8 ms: 1.03x faster                                                    |
| xml_etree_process          | 71.0 ms                                                                | 69.2 ms: 1.03x faster                                                    |
| richards                   | 55.6 ms                                                                | 54.2 ms: 1.02x faster                                                    |
| sqlite_synth               | 2.05 us                                                                | 2.00 us: 1.02x faster                                                    |
| logging_simple             | 7.44 us                                                                | 7.27 us: 1.02x faster                                                    |
| coroutines                 | 24.0 ms                                                                | 23.5 ms: 1.02x faster                                                    |
| deepcopy_reduce            | 3.25 us                                                                | 3.18 us: 1.02x faster                                                    |
| sqlglot_v2_optimize        | 61.5 ms                                                                | 60.3 ms: 1.02x faster                                                    |
| richards_super             | 64.4 ms                                                                | 63.2 ms: 1.02x faster                                                    |
| scimark_monte_carlo        | 84.9 ms                                                                | 83.4 ms: 1.02x faster                                                    |
| scimark_sparse_mat_mult    | 5.66 ms                                                                | 5.57 ms: 1.02x faster                                                    |
| typing_runtime_protocols   | 196 us                                                                 | 193 us: 1.02x faster                                                     |
| pidigits                   | 207 ms                                                                 | 204 ms: 1.02x faster                                                     |
| generators                 | 31.5 ms                                                                | 31.1 ms: 1.01x faster                                                    |
| async_tree_cpu_io_mixed_tg | 483 ms                                                                 | 476 ms: 1.01x faster                                                     |
| django_template            | 43.1 ms                                                                | 42.5 ms: 1.01x faster                                                    |
| comprehensions             | 21.0 us                                                                | 20.8 us: 1.01x faster                                                    |
| xml_etree_iterparse        | 88.9 ms                                                                | 87.8 ms: 1.01x faster                                                    |
| crypto_pyaes               | 88.4 ms                                                                | 87.2 ms: 1.01x faster                                                    |
| async_tree_cpu_io_mixed    | 519 ms                                                                 | 512 ms: 1.01x faster                                                     |
| unpickle_pure_python       | 262 us                                                                 | 259 us: 1.01x faster                                                     |
| deltablue                  | 3.92 ms                                                                | 3.88 ms: 1.01x faster                                                    |
| sympy_str                  | 338 ms                                                                 | 334 ms: 1.01x faster                                                     |
| sqlglot_v2_transpile       | 1.95 ms                                                                | 1.93 ms: 1.01x faster                                                    |
| pathlib                    | 19.9 ms                                                                | 19.7 ms: 1.01x faster                                                    |
| spectral_norm              | 114 ms                                                                 | 113 ms: 1.01x faster                                                     |
| scimark_sor                | 138 ms                                                                 | 137 ms: 1.01x faster                                                     |
| deepcopy                   | 315 us                                                                 | 312 us: 1.01x faster                                                     |
| sqlglot_v2_parse           | 1.61 ms                                                                | 1.59 ms: 1.01x faster                                                    |
| async_tree_io              | 587 ms                                                                 | 583 ms: 1.01x faster                                                     |
| sympy_expand               | 551 ms                                                                 | 547 ms: 1.01x faster                                                     |
| coverage                   | 109 ms                                                                 | 108 ms: 1.01x faster                                                     |
| async_tree_memoization_tg  | 301 ms                                                                 | 298 ms: 1.01x faster                                                     |
| mdp                        | 2.74 sec                                                               | 2.72 sec: 1.01x faster                                                   |
| go                         | 146 ms                                                                 | 145 ms: 1.01x faster                                                     |
| create_gc_cycles           | 1.38 ms                                                                | 1.37 ms: 1.01x faster                                                    |
| async_tree_memoization     | 333 ms                                                                 | 331 ms: 1.01x faster                                                     |
| tomli_loads                | 2.38 sec                                                               | 2.37 sec: 1.01x faster                                                   |
| sqlalchemy_declarative     | 159 ms                                                                 | 158 ms: 1.01x faster                                                     |
| genshi_xml                 | 60.2 ms                                                                | 59.9 ms: 1.01x faster                                                    |
| pickle_pure_python         | 365 us                                                                 | 363 us: 1.01x faster                                                     |
| sphinx                     | 1.10 sec                                                               | 1.09 sec: 1.01x faster                                                   |
| hexiom                     | 7.72 ms                                                                | 7.68 ms: 1.01x faster                                                    |
| pycparser                  | 1.20 sec                                                               | 1.19 sec: 1.00x faster                                                   |
| mako                       | 16.1 ms                                                                | 16.1 ms: 1.00x faster                                                    |
| pprint_pformat             | 1.74 sec                                                               | 1.73 sec: 1.00x faster                                                   |
| many_optionals             | 1.18 ms                                                                | 1.18 ms: 1.00x faster                                                    |
| raytrace                   | 328 ms                                                                 | 327 ms: 1.00x faster                                                     |
| 2to3                       | 300 ms                                                                 | 299 ms: 1.00x faster                                                     |
| python_startup_no_site     | 11.1 ms                                                                | 11.1 ms: 1.00x faster                                                    |
| chaos                      | 69.3 ms                                                                | 69.5 ms: 1.00x slower                                                    |
| async_generators           | 381 ms                                                                 | 383 ms: 1.01x slower                                                     |
| fannkuch                   | 499 ms                                                                 | 503 ms: 1.01x slower                                                     |
| bpe_tokeniser              | 4.85 sec                                                               | 4.88 sec: 1.01x slower                                                   |
| logging_silent             | 115 ns                                                                 | 116 ns: 1.01x slower                                                     |
| deepcopy_memo              | 39.2 us                                                                | 39.9 us: 1.02x slower                                                    |
| float                      | 76.9 ms                                                                | 78.4 ms: 1.02x slower                                                    |
| regex_v8                   | 21.6 ms                                                                | 22.1 ms: 1.02x slower                                                    |
| pyflate                    | 505 ms                                                                 | 518 ms: 1.03x slower                                                     |
| nbody                      | 131 ms                                                                 | 135 ms: 1.03x slower                                                     |
| json_loads                 | 29.5 us                                                                | 30.5 us: 1.03x slower                                                    |
| html5lib                   | 69.9 ms                                                                | 72.3 ms: 1.03x slower                                                    |
| json                       | 5.07 ms                                                                | 5.24 ms: 1.03x slower                                                    |
| regex_dna                  | 169 ms                                                                 | 185 ms: 1.09x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (30): async_tree_none_tg, connected_components, logging_format, subparsers, async_tree_io_tg, thrift, regex_effbot, pylint, xml_etree_parse, nqueens, telco, meteor_contest, async_tree_none, pprint_safe_repr, k_core, bench_thread_pool, docutils, scimark_fft, sympy_sum, bench_mp_pool, genshi_text, gc_traversal, asyncio_websockets, python_startup, regex_compile, dulwich_log, sympy_integrate, shortest_path, json_dumps, sqlalchemy_imperative

- Geometric mean (including insignificant results): 1.003x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.01x