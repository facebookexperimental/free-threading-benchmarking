# Results vs. base

- fork: nascheme
- ref: mcache_str_hash
- machine: linux-x86_64
- commit hash: b6bca55
- commit date: 2025-05-08
- overall geometric mean: 1.002x slower
- HPT reliability: 97.46%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250508-vultr-x86_64-python-8679c8d5ccf657835a88-3.15.0a0-8679c8d | bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-b6bca55 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------:|
| 2to3           | 284 ms                                                                | 285 ms: 1.01x slower                                               |
| html5lib       | 65.7 ms                                                               | 67.4 ms: 1.03x slower                                              |
| Geometric mean | (ref)                                                                 | 1.01x slower                                                       |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250508-vultr-x86_64-python-8679c8d5ccf657835a88-3.15.0a0-8679c8d | bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-b6bca55 |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------:|
| asyncio_websockets         | 517 ms                                                                | 515 ms: 1.00x faster                                               |
| async_tree_memoization     | 310 ms                                                                | 312 ms: 1.01x slower                                               |
| async_tree_cpu_io_mixed_tg | 477 ms                                                                | 483 ms: 1.01x slower                                               |
| async_tree_cpu_io_mixed    | 503 ms                                                                | 512 ms: 1.02x slower                                               |
| coroutines                 | 22.6 ms                                                               | 23.3 ms: 1.03x slower                                              |
| Geometric mean             | (ref)                                                                 | 1.01x slower                                                       |

Benchmark hidden because not significant (6): async_tree_none_tg, async_tree_memoization_tg, async_generators, async_tree_io_tg, async_tree_none, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250508-vultr-x86_64-python-8679c8d5ccf657835a88-3.15.0a0-8679c8d | bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-b6bca55 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------:|
| float          | 70.4 ms                                                               | 69.9 ms: 1.01x faster                                              |
| pidigits       | 190 ms                                                                | 191 ms: 1.01x slower                                               |
| Geometric mean | (ref)                                                                 | 1.00x slower                                                       |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250508-vultr-x86_64-python-8679c8d5ccf657835a88-3.15.0a0-8679c8d | bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-b6bca55 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------:|
| regex_dna      | 184 ms                                                                | 181 ms: 1.02x faster                                               |
| regex_effbot   | 2.83 ms                                                               | 2.84 ms: 1.00x slower                                              |
| Geometric mean | (ref)                                                                 | 1.00x faster                                                       |

Benchmark hidden because not significant (2): regex_compile, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250508-vultr-x86_64-python-8679c8d5ccf657835a88-3.15.0a0-8679c8d | bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-b6bca55 |
|----------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------:|
| xml_etree_process    | 67.8 ms                                                               | 67.3 ms: 1.01x faster                                              |
| json_loads           | 30.8 us                                                               | 30.6 us: 1.01x faster                                              |
| pickle_pure_python   | 329 us                                                                | 328 us: 1.00x faster                                               |
| unpickle_pure_python | 226 us                                                                | 226 us: 1.00x faster                                               |
| tomli_loads          | 2.12 sec                                                              | 2.13 sec: 1.00x slower                                             |
| Geometric mean       | (ref)                                                                 | 1.00x faster                                                       |

Benchmark hidden because not significant (4): xml_etree_parse, json_dumps, xml_etree_iterparse, xml_etree_generate

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup, python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250508-vultr-x86_64-python-8679c8d5ccf657835a88-3.15.0a0-8679c8d | bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-b6bca55 |
|-----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------:|
| django_template | 40.4 ms                                                               | 39.8 ms: 1.02x faster                                              |
| genshi_xml      | 55.0 ms                                                               | 55.9 ms: 1.02x slower                                              |
| genshi_text     | 25.7 ms                                                               | 26.5 ms: 1.03x slower                                              |
| Geometric mean  | (ref)                                                                 | 1.01x slower                                                       |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                  | bm-20250508-vultr-x86_64-python-8679c8d5ccf657835a88-3.15.0a0-8679c8d | bm-20250508-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-b6bca55 |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------:|
| spectral_norm              | 112 ms                                                                | 109 ms: 1.03x faster                                               |
| scimark_sor                | 124 ms                                                                | 122 ms: 1.02x faster                                               |
| regex_dna                  | 184 ms                                                                | 181 ms: 1.02x faster                                               |
| generators                 | 29.8 ms                                                               | 29.3 ms: 1.02x faster                                              |
| deepcopy_memo              | 36.0 us                                                               | 35.4 us: 1.02x faster                                              |
| django_template            | 40.4 ms                                                               | 39.8 ms: 1.02x faster                                              |
| thrift                     | 886 us                                                                | 875 us: 1.01x faster                                               |
| dulwich_log                | 72.0 ms                                                               | 71.1 ms: 1.01x faster                                              |
| json                       | 5.23 ms                                                               | 5.18 ms: 1.01x faster                                              |
| coverage                   | 110 ms                                                                | 109 ms: 1.01x faster                                               |
| pathlib                    | 19.8 ms                                                               | 19.7 ms: 1.01x faster                                              |
| xml_etree_process          | 67.8 ms                                                               | 67.3 ms: 1.01x faster                                              |
| json_loads                 | 30.8 us                                                               | 30.6 us: 1.01x faster                                              |
| shortest_path              | 534 ms                                                                | 530 ms: 1.01x faster                                               |
| float                      | 70.4 ms                                                               | 69.9 ms: 1.01x faster                                              |
| gc_traversal               | 1.92 ms                                                               | 1.91 ms: 1.01x faster                                              |
| pprint_pformat             | 1.62 sec                                                              | 1.61 sec: 1.01x faster                                             |
| create_gc_cycles           | 1.49 ms                                                               | 1.49 ms: 1.01x faster                                              |
| k_core                     | 2.25 sec                                                              | 2.24 sec: 1.01x faster                                             |
| pickle_pure_python         | 329 us                                                                | 328 us: 1.00x faster                                               |
| asyncio_websockets         | 517 ms                                                                | 515 ms: 1.00x faster                                               |
| unpickle_pure_python       | 226 us                                                                | 226 us: 1.00x faster                                               |
| bench_thread_pool          | 3.13 ms                                                               | 3.13 ms: 1.00x faster                                              |
| regex_effbot               | 2.83 ms                                                               | 2.84 ms: 1.00x slower                                              |
| bpe_tokeniser              | 4.43 sec                                                              | 4.45 sec: 1.00x slower                                             |
| crypto_pyaes               | 86.1 ms                                                               | 86.4 ms: 1.00x slower                                              |
| tomli_loads                | 2.12 sec                                                              | 2.13 sec: 1.00x slower                                             |
| scimark_monte_carlo        | 76.6 ms                                                               | 77.0 ms: 1.01x slower                                              |
| richards_super             | 58.1 ms                                                               | 58.4 ms: 1.01x slower                                              |
| 2to3                       | 284 ms                                                                | 285 ms: 1.01x slower                                               |
| async_tree_memoization     | 310 ms                                                                | 312 ms: 1.01x slower                                               |
| pidigits                   | 190 ms                                                                | 191 ms: 1.01x slower                                               |
| mdp                        | 1.33 sec                                                              | 1.34 sec: 1.01x slower                                             |
| raytrace                   | 298 ms                                                                | 301 ms: 1.01x slower                                               |
| logging_simple             | 7.06 us                                                               | 7.13 us: 1.01x slower                                              |
| scimark_fft                | 363 ms                                                                | 366 ms: 1.01x slower                                               |
| sympy_expand               | 531 ms                                                                | 537 ms: 1.01x slower                                               |
| async_tree_cpu_io_mixed_tg | 477 ms                                                                | 483 ms: 1.01x slower                                               |
| comprehensions             | 19.2 us                                                               | 19.4 us: 1.01x slower                                              |
| scimark_lu                 | 130 ms                                                                | 132 ms: 1.01x slower                                               |
| sympy_str                  | 316 ms                                                                | 320 ms: 1.01x slower                                               |
| hexiom                     | 6.55 ms                                                               | 6.64 ms: 1.01x slower                                              |
| sqlite_synth               | 2.07 us                                                               | 2.10 us: 1.01x slower                                              |
| sympy_sum                  | 179 ms                                                                | 182 ms: 1.01x slower                                               |
| genshi_xml                 | 55.0 ms                                                               | 55.9 ms: 1.02x slower                                              |
| pyflate                    | 479 ms                                                                | 486 ms: 1.02x slower                                               |
| nqueens                    | 87.0 ms                                                               | 88.4 ms: 1.02x slower                                              |
| fannkuch                   | 467 ms                                                                | 476 ms: 1.02x slower                                               |
| async_tree_cpu_io_mixed    | 503 ms                                                                | 512 ms: 1.02x slower                                               |
| meteor_contest             | 129 ms                                                                | 131 ms: 1.02x slower                                               |
| chaos                      | 62.4 ms                                                               | 63.7 ms: 1.02x slower                                              |
| deepcopy_reduce            | 2.99 us                                                               | 3.05 us: 1.02x slower                                              |
| richards                   | 50.0 ms                                                               | 51.3 ms: 1.02x slower                                              |
| html5lib                   | 65.7 ms                                                               | 67.4 ms: 1.03x slower                                              |
| coroutines                 | 22.6 ms                                                               | 23.3 ms: 1.03x slower                                              |
| scimark_sparse_mat_mult    | 5.35 ms                                                               | 5.53 ms: 1.03x slower                                              |
| genshi_text                | 25.7 ms                                                               | 26.5 ms: 1.03x slower                                              |
| logging_silent             | 97.7 ns                                                               | 101 ns: 1.04x slower                                               |
| Geometric mean             | (ref)                                                                 | 1.00x slower                                                       |

Benchmark hidden because not significant (36): sqlglot_v2_transpile, async_tree_none_tg, subparsers, docutils, bench_mp_pool, connected_components, pprint_safe_repr, pycparser, xml_etree_parse, deepcopy, python_startup, json_dumps, python_startup_no_site, async_tree_memoization_tg, regex_compile, xml_etree_iterparse, async_generators, mako, sqlglot_v2_normalize, xml_etree_generate, sympy_integrate, async_tree_io_tg, telco, nbody, go, deltablue, async_tree_none, async_tree_io, sqlglot_v2_optimize, logging_format, regex_v8, sqlglot_v2_parse, sphinx, many_optionals, typing_runtime_protocols, pylint

- Geometric mean (including insignificant results): 1.002x slower

# HPT report

- Reliability score: 97.46% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x