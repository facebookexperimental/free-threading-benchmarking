# Results vs. base

- fork: nascheme
- ref: gc_check_rss
- machine: linux-x86_64
- commit hash: aabe31d
- commit date: 2025-05-04
- overall geometric mean: 1.007x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250504-vultr-x86_64-python-af5799f3056b0eee61fc-3.14.0a7+-af5799f | bm-20250504-vultr-x86_64-nascheme-gc_check_rss-3.14.0a7+-aabe31d |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------:|
| 2to3           | 281 ms                                                                 | 278 ms: 1.01x faster                                             |
| html5lib       | 64.4 ms                                                                | 65.8 ms: 1.02x slower                                            |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                     |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250504-vultr-x86_64-python-af5799f3056b0eee61fc-3.14.0a7+-af5799f | bm-20250504-vultr-x86_64-nascheme-gc_check_rss-3.14.0a7+-aabe31d |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------:|
| coroutines                 | 22.9 ms                                                                | 22.5 ms: 1.02x faster                                            |
| async_tree_cpu_io_mixed_tg | 485 ms                                                                 | 482 ms: 1.01x faster                                             |
| async_tree_memoization_tg  | 285 ms                                                                 | 288 ms: 1.01x slower                                             |
| async_generators           | 367 ms                                                                 | 370 ms: 1.01x slower                                             |
| async_tree_io              | 548 ms                                                                 | 556 ms: 1.01x slower                                             |
| async_tree_none_tg         | 226 ms                                                                 | 229 ms: 1.02x slower                                             |
| async_tree_io_tg           | 519 ms                                                                 | 528 ms: 1.02x slower                                             |
| async_tree_memoization     | 313 ms                                                                 | 318 ms: 1.02x slower                                             |
| async_tree_none            | 257 ms                                                                 | 265 ms: 1.03x slower                                             |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                     |

Benchmark hidden because not significant (2): async_tree_cpu_io_mixed, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250504-vultr-x86_64-python-af5799f3056b0eee61fc-3.14.0a7+-af5799f | bm-20250504-vultr-x86_64-nascheme-gc_check_rss-3.14.0a7+-aabe31d |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------:|
| pidigits       | 190 ms                                                                 | 190 ms: 1.00x slower                                             |
| float          | 71.2 ms                                                                | 71.5 ms: 1.00x slower                                            |
| nbody          | 118 ms                                                                 | 121 ms: 1.03x slower                                             |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250504-vultr-x86_64-python-af5799f3056b0eee61fc-3.14.0a7+-af5799f | bm-20250504-vultr-x86_64-nascheme-gc_check_rss-3.14.0a7+-aabe31d |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------:|
| regex_compile  | 145 ms                                                                 | 146 ms: 1.00x slower                                             |
| regex_v8       | 21.0 ms                                                                | 21.7 ms: 1.03x slower                                            |
| regex_effbot   | 2.84 ms                                                                | 2.93 ms: 1.03x slower                                            |
| regex_dna      | 182 ms                                                                 | 189 ms: 1.04x slower                                             |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20250504-vultr-x86_64-python-af5799f3056b0eee61fc-3.14.0a7+-af5799f | bm-20250504-vultr-x86_64-nascheme-gc_check_rss-3.14.0a7+-aabe31d |
|---------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------:|
| json_loads          | 32.1 us                                                                | 31.0 us: 1.04x faster                                            |
| xml_etree_iterparse | 88.2 ms                                                                | 87.5 ms: 1.01x faster                                            |
| xml_etree_parse     | 132 ms                                                                 | 131 ms: 1.01x faster                                             |
| json_dumps          | 13.4 ms                                                                | 13.3 ms: 1.01x faster                                            |
| xml_etree_process   | 67.9 ms                                                                | 68.2 ms: 1.01x slower                                            |
| xml_etree_generate  | 94.6 ms                                                                | 95.3 ms: 1.01x slower                                            |
| tomli_loads         | 2.11 sec                                                               | 2.16 sec: 1.02x slower                                           |
| Geometric mean      | (ref)                                                                  | 1.00x faster                                                     |

Benchmark hidden because not significant (2): pickle_pure_python, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250504-vultr-x86_64-python-af5799f3056b0eee61fc-3.14.0a7+-af5799f | bm-20250504-vultr-x86_64-nascheme-gc_check_rss-3.14.0a7+-aabe31d |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------:|
| python_startup         | 15.7 ms                                                                | 15.9 ms: 1.01x slower                                            |
| python_startup_no_site | 9.33 ms                                                                | 9.48 ms: 1.02x slower                                            |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20250504-vultr-x86_64-python-af5799f3056b0eee61fc-3.14.0a7+-af5799f | bm-20250504-vultr-x86_64-nascheme-gc_check_rss-3.14.0a7+-aabe31d |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------:|
| mako           | 15.7 ms                                                                | 15.8 ms: 1.00x slower                                            |
| genshi_text    | 25.8 ms                                                                | 26.2 ms: 1.01x slower                                            |
| genshi_xml     | 54.5 ms                                                                | 55.5 ms: 1.02x slower                                            |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                     |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20250504-vultr-x86_64-python-af5799f3056b0eee61fc-3.14.0a7+-af5799f | bm-20250504-vultr-x86_64-nascheme-gc_check_rss-3.14.0a7+-aabe31d |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------:|
| bench_mp_pool              | 96.0 ms                                                                | 87.6 ms: 1.10x faster                                            |
| json                       | 5.41 ms                                                                | 5.19 ms: 1.04x faster                                            |
| json_loads                 | 32.1 us                                                                | 31.0 us: 1.04x faster                                            |
| generators                 | 30.5 ms                                                                | 29.6 ms: 1.03x faster                                            |
| deltablue                  | 3.50 ms                                                                | 3.43 ms: 1.02x faster                                            |
| coroutines                 | 22.9 ms                                                                | 22.5 ms: 1.02x faster                                            |
| comprehensions             | 19.6 us                                                                | 19.4 us: 1.01x faster                                            |
| sqlglot_v2_optimize        | 58.4 ms                                                                | 57.8 ms: 1.01x faster                                            |
| deepcopy_memo              | 35.9 us                                                                | 35.5 us: 1.01x faster                                            |
| 2to3                       | 281 ms                                                                 | 278 ms: 1.01x faster                                             |
| pycparser                  | 1.14 sec                                                               | 1.13 sec: 1.01x faster                                           |
| xml_etree_iterparse        | 88.2 ms                                                                | 87.5 ms: 1.01x faster                                            |
| xml_etree_parse            | 132 ms                                                                 | 131 ms: 1.01x faster                                             |
| json_dumps                 | 13.4 ms                                                                | 13.3 ms: 1.01x faster                                            |
| async_tree_cpu_io_mixed_tg | 485 ms                                                                 | 482 ms: 1.01x faster                                             |
| pidigits                   | 190 ms                                                                 | 190 ms: 1.00x slower                                             |
| mako                       | 15.7 ms                                                                | 15.8 ms: 1.00x slower                                            |
| chaos                      | 62.3 ms                                                                | 62.5 ms: 1.00x slower                                            |
| float                      | 71.2 ms                                                                | 71.5 ms: 1.00x slower                                            |
| hexiom                     | 6.68 ms                                                                | 6.71 ms: 1.00x slower                                            |
| regex_compile              | 145 ms                                                                 | 146 ms: 1.00x slower                                             |
| xml_etree_process          | 67.9 ms                                                                | 68.2 ms: 1.01x slower                                            |
| nqueens                    | 87.4 ms                                                                | 87.9 ms: 1.01x slower                                            |
| telco                      | 8.68 ms                                                                | 8.73 ms: 1.01x slower                                            |
| fannkuch                   | 465 ms                                                                 | 468 ms: 1.01x slower                                             |
| bpe_tokeniser              | 4.44 sec                                                               | 4.46 sec: 1.01x slower                                           |
| xml_etree_generate         | 94.6 ms                                                                | 95.3 ms: 1.01x slower                                            |
| async_tree_memoization_tg  | 285 ms                                                                 | 288 ms: 1.01x slower                                             |
| async_generators           | 367 ms                                                                 | 370 ms: 1.01x slower                                             |
| logging_silent             | 104 ns                                                                 | 104 ns: 1.01x slower                                             |
| coverage                   | 109 ms                                                                 | 110 ms: 1.01x slower                                             |
| scimark_monte_carlo        | 76.3 ms                                                                | 77.1 ms: 1.01x slower                                            |
| deepcopy                   | 294 us                                                                 | 297 us: 1.01x slower                                             |
| connected_components       | 486 ms                                                                 | 491 ms: 1.01x slower                                             |
| sqlglot_v2_normalize       | 116 ms                                                                 | 117 ms: 1.01x slower                                             |
| scimark_fft                | 366 ms                                                                 | 370 ms: 1.01x slower                                             |
| pprint_pformat             | 1.62 sec                                                               | 1.64 sec: 1.01x slower                                           |
| sympy_integrate            | 22.1 ms                                                                | 22.3 ms: 1.01x slower                                            |
| mdp                        | 1.32 sec                                                               | 1.34 sec: 1.01x slower                                           |
| python_startup             | 15.7 ms                                                                | 15.9 ms: 1.01x slower                                            |
| pprint_safe_repr           | 785 ms                                                                 | 795 ms: 1.01x slower                                             |
| genshi_text                | 25.8 ms                                                                | 26.2 ms: 1.01x slower                                            |
| sympy_str                  | 314 ms                                                                 | 318 ms: 1.01x slower                                             |
| crypto_pyaes               | 84.3 ms                                                                | 85.5 ms: 1.01x slower                                            |
| async_tree_io              | 548 ms                                                                 | 556 ms: 1.01x slower                                             |
| sqlglot_v2_parse           | 1.46 ms                                                                | 1.48 ms: 1.01x slower                                            |
| async_tree_none_tg         | 226 ms                                                                 | 229 ms: 1.02x slower                                             |
| python_startup_no_site     | 9.33 ms                                                                | 9.48 ms: 1.02x slower                                            |
| genshi_xml                 | 54.5 ms                                                                | 55.5 ms: 1.02x slower                                            |
| async_tree_io_tg           | 519 ms                                                                 | 528 ms: 1.02x slower                                             |
| async_tree_memoization     | 313 ms                                                                 | 318 ms: 1.02x slower                                             |
| sympy_expand               | 529 ms                                                                 | 539 ms: 1.02x slower                                             |
| typing_runtime_protocols   | 191 us                                                                 | 195 us: 1.02x slower                                             |
| scimark_sor                | 121 ms                                                                 | 124 ms: 1.02x slower                                             |
| html5lib                   | 64.4 ms                                                                | 65.8 ms: 1.02x slower                                            |
| tomli_loads                | 2.11 sec                                                               | 2.16 sec: 1.02x slower                                           |
| logging_format             | 7.78 us                                                                | 7.97 us: 1.02x slower                                            |
| sqlglot_v2_transpile       | 1.78 ms                                                                | 1.83 ms: 1.03x slower                                            |
| nbody                      | 118 ms                                                                 | 121 ms: 1.03x slower                                             |
| scimark_lu                 | 129 ms                                                                 | 133 ms: 1.03x slower                                             |
| regex_v8                   | 21.0 ms                                                                | 21.7 ms: 1.03x slower                                            |
| spectral_norm              | 106 ms                                                                 | 109 ms: 1.03x slower                                             |
| async_tree_none            | 257 ms                                                                 | 265 ms: 1.03x slower                                             |
| deepcopy_reduce            | 3.00 us                                                                | 3.09 us: 1.03x slower                                            |
| regex_effbot               | 2.84 ms                                                                | 2.93 ms: 1.03x slower                                            |
| richards_super             | 60.2 ms                                                                | 62.3 ms: 1.03x slower                                            |
| regex_dna                  | 182 ms                                                                 | 189 ms: 1.04x slower                                             |
| gc_traversal               | 1.78 ms                                                                | 1.86 ms: 1.04x slower                                            |
| scimark_sparse_mat_mult    | 5.23 ms                                                                | 5.48 ms: 1.05x slower                                            |
| create_gc_cycles           | 1.36 ms                                                                | 1.44 ms: 1.06x slower                                            |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                     |

Benchmark hidden because not significant (25): meteor_contest, pickle_pure_python, raytrace, docutils, unpickle_pure_python, sqlalchemy_imperative, bench_thread_pool, sphinx, django_template, async_tree_cpu_io_mixed, pylint, go, k_core, shortest_path, asyncio_websockets, pathlib, sqlalchemy_declarative, dulwich_log, sympy_sum, pyflate, logging_simple, sqlite_synth, many_optionals, richards, subparsers

- Geometric mean (including insignificant results): 1.007x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.03x