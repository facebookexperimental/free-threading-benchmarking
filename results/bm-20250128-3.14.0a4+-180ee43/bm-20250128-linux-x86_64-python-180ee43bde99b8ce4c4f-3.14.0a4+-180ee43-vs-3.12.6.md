# Results vs. 3.12.6

- fork: python
- ref: 180ee43bde99b8ce4c4f
- machine: linux-x86_64
- commit hash: 180ee43
- commit date: 2025-01-28
- overall geometric mean: 1.057x faster
- HPT reliability: 98.37%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250128-linux-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 529 ms: 1.16x slower                                                   |
| html5lib       | 88.9 ms                                                | 77.2 ms: 1.15x faster                                                  |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250128-linux-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 906 ms: 2.14x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 455 ms: 2.04x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 491 ms: 1.99x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 981 ms: 1.88x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 376 ms: 1.87x faster                                                   |
| async_tree_none            | 741 ms                                                 | 425 ms: 1.75x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 686 ms: 1.61x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 727 ms: 1.48x faster                                                   |
| asyncio_websockets         | 748 ms                                                 | 701 ms: 1.07x faster                                                   |
| async_generators           | 589 ms                                                 | 554 ms: 1.06x faster                                                   |
| coroutines                 | 29.5 ms                                                | 34.7 ms: 1.17x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.55x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250128-linux-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 117 ms: 1.05x faster                                                   |
| nbody          | 119 ms                                                 | 130 ms: 1.10x slower                                                   |
| Geometric mean | (ref)                                                  | 1.00x slower                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250128-linux-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.20 ms: 1.22x faster                                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                                           |

Benchmark hidden because not significant (3): regex_compile, regex_dna, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250128-linux-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_generate   | 127 ms                                                 | 109 ms: 1.16x faster                                                   |
| tomli_loads          | 2.88 sec                                               | 2.53 sec: 1.14x faster                                                 |
| xml_etree_process    | 83.7 ms                                                | 78.6 ms: 1.06x faster                                                  |
| pickle_pure_python   | 436 us                                                 | 469 us: 1.08x slower                                                   |
| json_loads           | 37.9 us                                                | 41.3 us: 1.09x slower                                                  |
| unpickle_pure_python | 300 us                                                 | 345 us: 1.15x slower                                                   |
| json_dumps           | 14.3 ms                                                | 16.5 ms: 1.15x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.01x slower                                                           |

Benchmark hidden because not significant (2): xml_etree_iterparse, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250128-linux-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup | 23.7 ms                                                | 29.7 ms: 1.25x slower                                                  |
| Geometric mean | (ref)                                                  | 1.10x slower                                                           |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250128-linux-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 44.9 ms                                                | 50.1 ms: 1.11x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.04x slower                                                           |

Benchmark hidden because not significant (3): genshi_text, mako, genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250128-linux-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 906 ms: 2.14x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 455 ms: 2.04x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 491 ms: 1.99x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 981 ms: 1.88x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 376 ms: 1.87x faster                                                   |
| async_tree_none            | 741 ms                                                 | 425 ms: 1.75x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 686 ms: 1.61x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 727 ms: 1.48x faster                                                   |
| comprehensions             | 27.1 us                                                | 21.0 us: 1.29x faster                                                  |
| deepcopy                   | 468 us                                                 | 363 us: 1.29x faster                                                   |
| regex_effbot               | 5.13 ms                                                | 4.20 ms: 1.22x faster                                                  |
| deepcopy_memo              | 52.4 us                                                | 43.2 us: 1.21x faster                                                  |
| raytrace                   | 408 ms                                                 | 341 ms: 1.20x faster                                                   |
| xml_etree_generate         | 127 ms                                                 | 109 ms: 1.16x faster                                                   |
| pylint                     | 465 ms                                                 | 399 ms: 1.16x faster                                                   |
| pycparser                  | 1.79 sec                                               | 1.54 sec: 1.16x faster                                                 |
| html5lib                   | 88.9 ms                                                | 77.2 ms: 1.15x faster                                                  |
| tomli_loads                | 2.88 sec                                               | 2.53 sec: 1.14x faster                                                 |
| pathlib                    | 31.6 ms                                                | 28.2 ms: 1.12x faster                                                  |
| spectral_norm              | 156 ms                                                 | 140 ms: 1.11x faster                                                   |
| deepcopy_reduce            | 4.04 us                                                | 3.63 us: 1.11x faster                                                  |
| sqlglot_normalize          | 157 ms                                                 | 143 ms: 1.10x faster                                                   |
| go                         | 172 ms                                                 | 158 ms: 1.09x faster                                                   |
| sqlite_synth               | 3.87 us                                                | 3.57 us: 1.09x faster                                                  |
| mdp                        | 3.97 sec                                               | 3.69 sec: 1.08x faster                                                 |
| bpe_tokeniser              | 6.59 sec                                               | 6.14 sec: 1.07x faster                                                 |
| pprint_safe_repr           | 967 ms                                                 | 904 ms: 1.07x faster                                                   |
| asyncio_websockets         | 748 ms                                                 | 701 ms: 1.07x faster                                                   |
| xml_etree_process          | 83.7 ms                                                | 78.6 ms: 1.06x faster                                                  |
| async_generators           | 589 ms                                                 | 554 ms: 1.06x faster                                                   |
| generators                 | 41.1 ms                                                | 39.0 ms: 1.05x faster                                                  |
| scimark_monte_carlo        | 96.4 ms                                                | 91.7 ms: 1.05x faster                                                  |
| float                      | 123 ms                                                 | 117 ms: 1.05x faster                                                   |
| typing_runtime_protocols   | 224 us                                                 | 214 us: 1.05x faster                                                   |
| sqlglot_parse              | 1.79 ms                                                | 1.86 ms: 1.04x slower                                                  |
| sympy_expand               | 582 ms                                                 | 612 ms: 1.05x slower                                                   |
| scimark_sor                | 167 ms                                                 | 177 ms: 1.06x slower                                                   |
| chaos                      | 84.9 ms                                                | 90.2 ms: 1.06x slower                                                  |
| meteor_contest             | 146 ms                                                 | 156 ms: 1.06x slower                                                   |
| thrift                     | 1.06 ms                                                | 1.13 ms: 1.07x slower                                                  |
| pickle_pure_python         | 436 us                                                 | 469 us: 1.08x slower                                                   |
| logging_silent             | 139 ns                                                 | 150 ns: 1.08x slower                                                   |
| json                       | 6.85 ms                                                | 7.43 ms: 1.08x slower                                                  |
| json_loads                 | 37.9 us                                                | 41.3 us: 1.09x slower                                                  |
| richards                   | 60.3 ms                                                | 65.9 ms: 1.09x slower                                                  |
| nbody                      | 119 ms                                                 | 130 ms: 1.10x slower                                                   |
| sqlglot_optimize           | 76.0 ms                                                | 84.3 ms: 1.11x slower                                                  |
| django_template            | 44.9 ms                                                | 50.1 ms: 1.11x slower                                                  |
| hexiom                     | 8.27 ms                                                | 9.34 ms: 1.13x slower                                                  |
| logging_format             | 9.59 us                                                | 11.0 us: 1.15x slower                                                  |
| unpickle_pure_python       | 300 us                                                 | 345 us: 1.15x slower                                                   |
| json_dumps                 | 14.3 ms                                                | 16.5 ms: 1.15x slower                                                  |
| 2to3                       | 456 ms                                                 | 529 ms: 1.16x slower                                                   |
| sympy_integrate            | 29.8 ms                                                | 34.8 ms: 1.17x slower                                                  |
| coroutines                 | 29.5 ms                                                | 34.7 ms: 1.17x slower                                                  |
| telco                      | 9.59 ms                                                | 11.9 ms: 1.24x slower                                                  |
| python_startup             | 23.7 ms                                                | 29.7 ms: 1.25x slower                                                  |
| coverage                   | 95.4 ms                                                | 127 ms: 1.33x slower                                                   |
| gc_traversal               | 5.86 ms                                                | 9.75 ms: 1.66x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 3.51 ms: 1.81x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 100 ms: 4.84x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.03x faster                                                           |

Benchmark hidden because not significant (29): bench_thread_pool, sympy_str, sqlalchemy_imperative, genshi_text, xml_etree_iterparse, sqlalchemy_declarative, pidigits, python_startup_no_site, pyflate, scimark_sparse_mat_mult, docutils, xml_etree_parse, dulwich_log, richards_super, sympy_sum, logging_simple, pprint_pformat, regex_compile, scimark_lu, crypto_pyaes, sqlglot_transpile, scimark_fft, deltablue, fannkuch, nqueens, regex_dna, mako, genshi_xml, regex_v8
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250128-3.14.0a4+-180ee43/bm-20250128-linux-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.057x faster

# HPT report

- Reliability score: 98.37% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.13x