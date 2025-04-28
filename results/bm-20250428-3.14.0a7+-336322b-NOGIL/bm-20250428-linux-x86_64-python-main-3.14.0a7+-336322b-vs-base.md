# Results vs. base

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 336322b
- commit date: 2025-04-28
- overall geometric mean: 1.000x slower
- HPT reliability: 88.59%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250428-linux-x86_64-python-606003ffa9e400cc22cc-3.14.0a7+-606003f | bm-20250428-linux-x86_64-python-main-3.14.0a7+-336322b |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 417 ms                                                                 | 404 ms: 1.03x faster                                   |
| docutils       | 3.94 sec                                                               | 3.87 sec: 1.02x faster                                 |
| sphinx         | 1.57 sec                                                               | 1.51 sec: 1.04x faster                                 |
| Geometric mean | (ref)                                                                  | 1.02x faster                                           |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250428-linux-x86_64-python-606003ffa9e400cc22cc-3.14.0a7+-606003f | bm-20250428-linux-x86_64-python-main-3.14.0a7+-336322b |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------:|
| async_tree_io_tg           | 684 ms                                                                 | 670 ms: 1.02x faster                                   |
| async_tree_cpu_io_mixed_tg | 589 ms                                                                 | 578 ms: 1.02x faster                                   |
| async_tree_cpu_io_mixed    | 639 ms                                                                 | 629 ms: 1.02x faster                                   |
| async_tree_none            | 347 ms                                                                 | 342 ms: 1.02x faster                                   |
| async_tree_io              | 733 ms                                                                 | 723 ms: 1.01x faster                                   |
| async_generators           | 546 ms                                                                 | 538 ms: 1.01x faster                                   |
| asyncio_websockets         | 684 ms                                                                 | 689 ms: 1.01x slower                                   |
| coroutines                 | 29.6 ms                                                                | 30.3 ms: 1.02x slower                                  |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                           |

Benchmark hidden because not significant (3): async_tree_none_tg, async_tree_memoization, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250428-linux-x86_64-python-606003ffa9e400cc22cc-3.14.0a7+-606003f | bm-20250428-linux-x86_64-python-main-3.14.0a7+-336322b |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------:|
| nbody          | 147 ms                                                                 | 150 ms: 1.02x slower                                   |
| pidigits       | 218 ms                                                                 | 225 ms: 1.03x slower                                   |
| Geometric mean | (ref)                                                                  | 1.02x slower                                           |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250428-linux-x86_64-python-606003ffa9e400cc22cc-3.14.0a7+-606003f | bm-20250428-linux-x86_64-python-main-3.14.0a7+-336322b |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------:|
| regex_effbot   | 3.91 ms                                                                | 3.77 ms: 1.04x faster                                  |
| regex_compile  | 179 ms                                                                 | 180 ms: 1.00x slower                                   |
| regex_v8       | 26.2 ms                                                                | 26.3 ms: 1.01x slower                                  |
| Geometric mean | (ref)                                                                  | 1.01x faster                                           |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250428-linux-x86_64-python-606003ffa9e400cc22cc-3.14.0a7+-606003f | bm-20250428-linux-x86_64-python-main-3.14.0a7+-336322b |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------:|
| xml_etree_parse      | 196 ms                                                                 | 187 ms: 1.05x faster                                   |
| xml_etree_iterparse  | 130 ms                                                                 | 125 ms: 1.04x faster                                   |
| xml_etree_generate   | 135 ms                                                                 | 131 ms: 1.04x faster                                   |
| xml_etree_process    | 93.6 ms                                                                | 91.7 ms: 1.02x faster                                  |
| unpickle_pure_python | 302 us                                                                 | 297 us: 1.02x faster                                   |
| json_loads           | 40.7 us                                                                | 41.0 us: 1.01x slower                                  |
| pickle_pure_python   | 437 us                                                                 | 447 us: 1.02x slower                                   |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                           |

Benchmark hidden because not significant (2): tomli_loads, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20250428-linux-x86_64-python-606003ffa9e400cc22cc-3.14.0a7+-606003f | bm-20250428-linux-x86_64-python-main-3.14.0a7+-336322b |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------:|
| python_startup | 24.5 ms                                                                | 24.0 ms: 1.02x faster                                  |
| Geometric mean | (ref)                                                                  | 1.01x faster                                           |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20250428-linux-x86_64-python-606003ffa9e400cc22cc-3.14.0a7+-606003f | bm-20250428-linux-x86_64-python-main-3.14.0a7+-336322b |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------:|
| genshi_xml     | 73.4 ms                                                                | 76.1 ms: 1.04x slower                                  |
| mako           | 20.8 ms                                                                | 22.4 ms: 1.08x slower                                  |
| Geometric mean | (ref)                                                                  | 1.03x slower                                           |

Benchmark hidden because not significant (2): django_template, genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20250428-linux-x86_64-python-606003ffa9e400cc22cc-3.14.0a7+-606003f | bm-20250428-linux-x86_64-python-main-3.14.0a7+-336322b |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------:|
| bench_thread_pool          | 3.09 ms                                                                | 2.50 ms: 1.24x faster                                  |
| xml_etree_parse            | 196 ms                                                                 | 187 ms: 1.05x faster                                   |
| xml_etree_iterparse        | 130 ms                                                                 | 125 ms: 1.04x faster                                   |
| sympy_integrate            | 31.2 ms                                                                | 30.0 ms: 1.04x faster                                  |
| sphinx                     | 1.57 sec                                                               | 1.51 sec: 1.04x faster                                 |
| regex_effbot               | 3.91 ms                                                                | 3.77 ms: 1.04x faster                                  |
| xml_etree_generate         | 135 ms                                                                 | 131 ms: 1.04x faster                                   |
| 2to3                       | 417 ms                                                                 | 404 ms: 1.03x faster                                   |
| sympy_sum                  | 229 ms                                                                 | 223 ms: 1.03x faster                                   |
| sqlglot_v2_transpile       | 2.49 ms                                                                | 2.43 ms: 1.03x faster                                  |
| sympy_expand               | 673 ms                                                                 | 658 ms: 1.02x faster                                   |
| python_startup             | 24.5 ms                                                                | 24.0 ms: 1.02x faster                                  |
| async_tree_io_tg           | 684 ms                                                                 | 670 ms: 1.02x faster                                   |
| xml_etree_process          | 93.6 ms                                                                | 91.7 ms: 1.02x faster                                  |
| subparsers                 | 32.9 ms                                                                | 32.3 ms: 1.02x faster                                  |
| typing_runtime_protocols   | 251 us                                                                 | 246 us: 1.02x faster                                   |
| sqlglot_v2_normalize       | 149 ms                                                                 | 146 ms: 1.02x faster                                   |
| async_tree_cpu_io_mixed_tg | 589 ms                                                                 | 578 ms: 1.02x faster                                   |
| docutils                   | 3.94 sec                                                               | 3.87 sec: 1.02x faster                                 |
| pycparser                  | 1.49 sec                                                               | 1.46 sec: 1.02x faster                                 |
| unpickle_pure_python       | 302 us                                                                 | 297 us: 1.02x faster                                   |
| create_gc_cycles           | 2.42 ms                                                                | 2.38 ms: 1.02x faster                                  |
| async_tree_cpu_io_mixed    | 639 ms                                                                 | 629 ms: 1.02x faster                                   |
| async_tree_none            | 347 ms                                                                 | 342 ms: 1.02x faster                                   |
| async_tree_io              | 733 ms                                                                 | 723 ms: 1.01x faster                                   |
| async_generators           | 546 ms                                                                 | 538 ms: 1.01x faster                                   |
| many_optionals             | 1.33 ms                                                                | 1.32 ms: 1.01x faster                                  |
| deltablue                  | 4.77 ms                                                                | 4.72 ms: 1.01x faster                                  |
| thrift                     | 1.10 ms                                                                | 1.09 ms: 1.01x faster                                  |
| comprehensions             | 25.6 us                                                                | 25.3 us: 1.01x faster                                  |
| chaos                      | 81.4 ms                                                                | 80.7 ms: 1.01x faster                                  |
| meteor_contest             | 161 ms                                                                 | 160 ms: 1.01x faster                                   |
| coverage                   | 144 ms                                                                 | 143 ms: 1.01x faster                                   |
| scimark_sor                | 159 ms                                                                 | 158 ms: 1.01x faster                                   |
| bpe_tokeniser              | 7.33 sec                                                               | 7.29 sec: 1.01x faster                                 |
| regex_compile              | 179 ms                                                                 | 180 ms: 1.00x slower                                   |
| scimark_monte_carlo        | 97.6 ms                                                                | 98.1 ms: 1.01x slower                                  |
| json_loads                 | 40.7 us                                                                | 41.0 us: 1.01x slower                                  |
| regex_v8                   | 26.2 ms                                                                | 26.3 ms: 1.01x slower                                  |
| asyncio_websockets         | 684 ms                                                                 | 689 ms: 1.01x slower                                   |
| deepcopy_reduce            | 3.90 us                                                                | 3.94 us: 1.01x slower                                  |
| pprint_pformat             | 2.08 sec                                                               | 2.10 sec: 1.01x slower                                 |
| scimark_lu                 | 167 ms                                                                 | 168 ms: 1.01x slower                                   |
| richards                   | 66.5 ms                                                                | 67.1 ms: 1.01x slower                                  |
| logging_silent             | 138 ns                                                                 | 140 ns: 1.01x slower                                   |
| go                         | 164 ms                                                                 | 166 ms: 1.01x slower                                   |
| crypto_pyaes               | 110 ms                                                                 | 111 ms: 1.01x slower                                   |
| scimark_fft                | 456 ms                                                                 | 463 ms: 1.02x slower                                   |
| nbody                      | 147 ms                                                                 | 150 ms: 1.02x slower                                   |
| logging_format             | 9.68 us                                                                | 9.85 us: 1.02x slower                                  |
| nqueens                    | 111 ms                                                                 | 113 ms: 1.02x slower                                   |
| fannkuch                   | 587 ms                                                                 | 601 ms: 1.02x slower                                   |
| pickle_pure_python         | 437 us                                                                 | 447 us: 1.02x slower                                   |
| coroutines                 | 29.6 ms                                                                | 30.3 ms: 1.02x slower                                  |
| mdp                        | 2.23 sec                                                               | 2.29 sec: 1.03x slower                                 |
| scimark_sparse_mat_mult    | 6.85 ms                                                                | 7.06 ms: 1.03x slower                                  |
| pidigits                   | 218 ms                                                                 | 225 ms: 1.03x slower                                   |
| pyflate                    | 644 ms                                                                 | 667 ms: 1.04x slower                                   |
| spectral_norm              | 138 ms                                                                 | 143 ms: 1.04x slower                                   |
| pprint_safe_repr           | 1.01 sec                                                               | 1.05 sec: 1.04x slower                                 |
| genshi_xml                 | 73.4 ms                                                                | 76.1 ms: 1.04x slower                                  |
| pathlib                    | 26.1 ms                                                                | 27.1 ms: 1.04x slower                                  |
| shortest_path              | 934 ms                                                                 | 975 ms: 1.04x slower                                   |
| connected_components       | 851 ms                                                                 | 897 ms: 1.05x slower                                   |
| gc_traversal               | 3.38 ms                                                                | 3.58 ms: 1.06x slower                                  |
| mako                       | 20.8 ms                                                                | 22.4 ms: 1.08x slower                                  |
| k_core                     | 3.89 sec                                                               | 4.24 sec: 1.09x slower                                 |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                           |

Benchmark hidden because not significant (27): bench_mp_pool, sqlglot_v2_parse, sqlglot_v2_optimize, hexiom, sympy_str, sqlite_synth, async_tree_none_tg, async_tree_memoization, richards_super, django_template, async_tree_memoization_tg, raytrace, dulwich_log, regex_dna, tomli_loads, python_startup_no_site, generators, float, genshi_text, deepcopy, deepcopy_memo, html5lib, telco, logging_simple, json_dumps, json, pylint

- Geometric mean (including insignificant results): 1.000x slower

# HPT report

- Reliability score: 88.59% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x