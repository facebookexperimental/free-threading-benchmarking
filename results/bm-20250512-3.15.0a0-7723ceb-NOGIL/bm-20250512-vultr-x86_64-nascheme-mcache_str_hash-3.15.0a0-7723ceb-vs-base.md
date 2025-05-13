# Results vs. base

- fork: nascheme
- ref: mcache_str_hash
- machine: linux-x86_64
- commit hash: 7723ceb
- commit date: 2025-05-12
- overall geometric mean: 1.002x slower
- HPT reliability: 99.86%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250508-vultr-x86_64-python-9546eeea90c8deb8570a-3.15.0a0-9546eee | bm-20250512-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-7723ceb |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------:|
| docutils       | 2.71 sec                                                              | 2.69 sec: 1.01x faster                                             |
| Geometric mean | (ref)                                                                 | 1.00x faster                                                       |

Benchmark hidden because not significant (3): 2to3, html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250508-vultr-x86_64-python-9546eeea90c8deb8570a-3.15.0a0-9546eee | bm-20250512-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-7723ceb |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------:|
| coroutines                 | 23.5 ms                                                               | 23.1 ms: 1.02x faster                                              |
| async_tree_cpu_io_mixed    | 510 ms                                                                | 514 ms: 1.01x slower                                               |
| async_tree_cpu_io_mixed_tg | 484 ms                                                                | 487 ms: 1.01x slower                                               |
| async_generators           | 364 ms                                                                | 368 ms: 1.01x slower                                               |
| Geometric mean             | (ref)                                                                 | 1.00x slower                                                       |

Benchmark hidden because not significant (7): asyncio_websockets, async_tree_io_tg, async_tree_none_tg, async_tree_io, async_tree_memoization_tg, async_tree_memoization, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250508-vultr-x86_64-python-9546eeea90c8deb8570a-3.15.0a0-9546eee | bm-20250512-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-7723ceb |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------:|
| nbody          | 119 ms                                                                | 121 ms: 1.02x slower                                               |
| float          | 70.0 ms                                                               | 71.2 ms: 1.02x slower                                              |
| pidigits       | 198 ms                                                                | 207 ms: 1.04x slower                                               |
| Geometric mean | (ref)                                                                 | 1.02x slower                                                       |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250508-vultr-x86_64-python-9546eeea90c8deb8570a-3.15.0a0-9546eee | bm-20250512-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-7723ceb |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------:|
| regex_v8       | 21.2 ms                                                               | 20.8 ms: 1.02x faster                                              |
| regex_dna      | 180 ms                                                                | 178 ms: 1.01x faster                                               |
| regex_effbot   | 2.82 ms                                                               | 2.81 ms: 1.00x faster                                              |
| regex_compile  | 144 ms                                                                | 145 ms: 1.01x slower                                               |
| Geometric mean | (ref)                                                                 | 1.01x faster                                                       |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250508-vultr-x86_64-python-9546eeea90c8deb8570a-3.15.0a0-9546eee | bm-20250512-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-7723ceb |
|----------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------:|
| unpickle_pure_python | 234 us                                                                | 230 us: 1.02x faster                                               |
| xml_etree_parse      | 131 ms                                                                | 129 ms: 1.01x faster                                               |
| pickle_pure_python   | 339 us                                                                | 336 us: 1.01x faster                                               |
| xml_etree_iterparse  | 87.4 ms                                                               | 86.7 ms: 1.01x faster                                              |
| json_loads           | 30.5 us                                                               | 30.7 us: 1.01x slower                                              |
| xml_etree_generate   | 96.1 ms                                                               | 97.4 ms: 1.01x slower                                              |
| xml_etree_process    | 68.6 ms                                                               | 69.7 ms: 1.02x slower                                              |
| tomli_loads          | 2.12 sec                                                              | 2.16 sec: 1.02x slower                                             |
| Geometric mean       | (ref)                                                                 | 1.00x slower                                                       |

Benchmark hidden because not significant (1): json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20250508-vultr-x86_64-python-9546eeea90c8deb8570a-3.15.0a0-9546eee | bm-20250512-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-7723ceb |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------:|
| python_startup | 16.0 ms                                                               | 16.0 ms: 1.00x slower                                              |
| Geometric mean | (ref)                                                                 | 1.00x slower                                                       |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250508-vultr-x86_64-python-9546eeea90c8deb8570a-3.15.0a0-9546eee | bm-20250512-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-7723ceb |
|-----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------:|
| mako            | 16.0 ms                                                               | 16.0 ms: 1.00x slower                                              |
| django_template | 40.5 ms                                                               | 40.9 ms: 1.01x slower                                              |
| genshi_xml      | 54.9 ms                                                               | 55.5 ms: 1.01x slower                                              |
| Geometric mean  | (ref)                                                                 | 1.01x slower                                                       |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20250508-vultr-x86_64-python-9546eeea90c8deb8570a-3.15.0a0-9546eee | bm-20250512-vultr-x86_64-nascheme-mcache_str_hash-3.15.0a0-7723ceb |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------:|
| create_gc_cycles           | 1.51 ms                                                               | 1.46 ms: 1.03x faster                                              |
| regex_v8                   | 21.2 ms                                                               | 20.8 ms: 1.02x faster                                              |
| unpickle_pure_python       | 234 us                                                                | 230 us: 1.02x faster                                               |
| gc_traversal               | 1.93 ms                                                               | 1.89 ms: 1.02x faster                                              |
| coroutines                 | 23.5 ms                                                               | 23.1 ms: 1.02x faster                                              |
| typing_runtime_protocols   | 194 us                                                                | 191 us: 1.01x faster                                               |
| logging_format             | 8.76 us                                                               | 8.64 us: 1.01x faster                                              |
| xml_etree_parse            | 131 ms                                                                | 129 ms: 1.01x faster                                               |
| hexiom                     | 6.66 ms                                                               | 6.58 ms: 1.01x faster                                              |
| regex_dna                  | 180 ms                                                                | 178 ms: 1.01x faster                                               |
| pickle_pure_python         | 339 us                                                                | 336 us: 1.01x faster                                               |
| bench_mp_pool              | 104 ms                                                                | 103 ms: 1.01x faster                                               |
| chaos                      | 62.7 ms                                                               | 62.1 ms: 1.01x faster                                              |
| xml_etree_iterparse        | 87.4 ms                                                               | 86.7 ms: 1.01x faster                                              |
| docutils                   | 2.71 sec                                                              | 2.69 sec: 1.01x faster                                             |
| sqlglot_v2_normalize       | 116 ms                                                                | 115 ms: 1.01x faster                                               |
| scimark_fft                | 365 ms                                                                | 362 ms: 1.01x faster                                               |
| sqlglot_v2_optimize        | 57.9 ms                                                               | 57.6 ms: 1.01x faster                                              |
| pathlib                    | 19.7 ms                                                               | 19.6 ms: 1.00x faster                                              |
| regex_effbot               | 2.82 ms                                                               | 2.81 ms: 1.00x faster                                              |
| fannkuch                   | 471 ms                                                                | 470 ms: 1.00x faster                                               |
| python_startup             | 16.0 ms                                                               | 16.0 ms: 1.00x slower                                              |
| bpe_tokeniser              | 4.43 sec                                                              | 4.44 sec: 1.00x slower                                             |
| mako                       | 16.0 ms                                                               | 16.0 ms: 1.00x slower                                              |
| crypto_pyaes               | 85.5 ms                                                               | 85.8 ms: 1.00x slower                                              |
| nqueens                    | 87.9 ms                                                               | 88.2 ms: 1.00x slower                                              |
| k_core                     | 2.23 sec                                                              | 2.24 sec: 1.01x slower                                             |
| async_tree_cpu_io_mixed    | 510 ms                                                                | 514 ms: 1.01x slower                                               |
| regex_compile              | 144 ms                                                                | 145 ms: 1.01x slower                                               |
| async_tree_cpu_io_mixed_tg | 484 ms                                                                | 487 ms: 1.01x slower                                               |
| pprint_pformat             | 1.61 sec                                                              | 1.62 sec: 1.01x slower                                             |
| json_loads                 | 30.5 us                                                               | 30.7 us: 1.01x slower                                              |
| pprint_safe_repr           | 778 ms                                                                | 784 ms: 1.01x slower                                               |
| django_template            | 40.5 ms                                                               | 40.9 ms: 1.01x slower                                              |
| go                         | 123 ms                                                                | 124 ms: 1.01x slower                                               |
| telco                      | 8.62 ms                                                               | 8.69 ms: 1.01x slower                                              |
| sympy_sum                  | 178 ms                                                                | 180 ms: 1.01x slower                                               |
| logging_silent             | 533 ns                                                                | 538 ns: 1.01x slower                                               |
| sympy_expand               | 528 ms                                                                | 534 ms: 1.01x slower                                               |
| async_generators           | 364 ms                                                                | 368 ms: 1.01x slower                                               |
| scimark_sor                | 122 ms                                                                | 123 ms: 1.01x slower                                               |
| genshi_xml                 | 54.9 ms                                                               | 55.5 ms: 1.01x slower                                              |
| richards_super             | 57.6 ms                                                               | 58.2 ms: 1.01x slower                                              |
| comprehensions             | 19.2 us                                                               | 19.4 us: 1.01x slower                                              |
| raytrace                   | 296 ms                                                                | 300 ms: 1.01x slower                                               |
| deepcopy_reduce            | 3.02 us                                                               | 3.06 us: 1.01x slower                                              |
| xml_etree_generate         | 96.1 ms                                                               | 97.4 ms: 1.01x slower                                              |
| spectral_norm              | 108 ms                                                                | 109 ms: 1.01x slower                                               |
| deepcopy                   | 293 us                                                                | 297 us: 1.01x slower                                               |
| richards                   | 50.0 ms                                                               | 50.7 ms: 1.01x slower                                              |
| sqlglot_v2_transpile       | 1.77 ms                                                               | 1.80 ms: 1.01x slower                                              |
| nbody                      | 119 ms                                                                | 121 ms: 1.02x slower                                               |
| pyflate                    | 474 ms                                                                | 482 ms: 1.02x slower                                               |
| xml_etree_process          | 68.6 ms                                                               | 69.7 ms: 1.02x slower                                              |
| float                      | 70.0 ms                                                               | 71.2 ms: 1.02x slower                                              |
| tomli_loads                | 2.12 sec                                                              | 2.16 sec: 1.02x slower                                             |
| sqlglot_v2_parse           | 1.44 ms                                                               | 1.47 ms: 1.02x slower                                              |
| pidigits                   | 198 ms                                                                | 207 ms: 1.04x slower                                               |
| Geometric mean             | (ref)                                                                 | 1.00x slower                                                       |

Benchmark hidden because not significant (36): subparsers, meteor_contest, generators, pycparser, deepcopy_memo, scimark_lu, sqlite_synth, 2to3, bench_thread_pool, python_startup_no_site, connected_components, many_optionals, sympy_integrate, genshi_text, dulwich_log, asyncio_websockets, sphinx, shortest_path, thrift, mdp, async_tree_io_tg, sympy_str, logging_simple, async_tree_none_tg, scimark_monte_carlo, async_tree_io, json_dumps, async_tree_memoization_tg, async_tree_memoization, json, pylint, coverage, scimark_sparse_mat_mult, html5lib, async_tree_none, deltablue

- Geometric mean (including insignificant results): 1.002x slower

# HPT report

- Reliability score: 99.86% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x