# Results vs. 3.12.6

- fork: python
- ref: bca35f0e782848ae2acd
- machine: linux-x86_64
- commit hash: bca35f0
- commit date: 2025-01-20
- overall geometric mean: 1.072x faster
- HPT reliability: 99.81%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 514 ms: 1.13x slower                                                   |
| docutils       | 4.00 sec                                               | 4.17 sec: 1.04x slower                                                 |
| html5lib       | 88.9 ms                                                | 81.4 ms: 1.09x faster                                                  |
| Geometric mean | (ref)                                                  | 1.02x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 867 ms: 2.23x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 927 ms: 1.99x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 476 ms: 1.95x faster                                                   |
| async_tree_none            | 741 ms                                                 | 387 ms: 1.92x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 398 ms: 1.77x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 563 ms: 1.74x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 653 ms: 1.69x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 711 ms: 1.52x faster                                                   |
| async_generators           | 589 ms                                                 | 535 ms: 1.10x faster                                                   |
| coroutines                 | 29.5 ms                                                | 30.7 ms: 1.04x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.57x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 106 ms: 1.16x faster                                                   |
| pidigits       | 250 ms                                                 | 225 ms: 1.11x faster                                                   |
| nbody          | 119 ms                                                 | 126 ms: 1.06x slower                                                   |
| Geometric mean | (ref)                                                  | 1.07x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.52 ms: 1.14x faster                                                  |
| regex_compile  | 187 ms                                                 | 166 ms: 1.12x faster                                                   |
| regex_dna      | 278 ms                                                 | 296 ms: 1.07x slower                                                   |
| Geometric mean | (ref)                                                  | 1.03x faster                                                           |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0 |
|---------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse     | 241 ms                                                 | 188 ms: 1.28x faster                                                   |
| xml_etree_generate  | 127 ms                                                 | 112 ms: 1.13x faster                                                   |
| xml_etree_iterparse | 169 ms                                                 | 152 ms: 1.12x faster                                                   |
| tomli_loads         | 2.88 sec                                               | 2.58 sec: 1.12x faster                                                 |
| json_loads          | 37.9 us                                                | 39.5 us: 1.04x slower                                                  |
| json_dumps          | 14.3 ms                                                | 15.1 ms: 1.05x slower                                                  |
| pickle_pure_python  | 436 us                                                 | 489 us: 1.12x slower                                                   |
| Geometric mean      | (ref)                                                  | 1.04x faster                                                           |

Benchmark hidden because not significant (2): xml_etree_process, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup | 23.7 ms                                                | 30.7 ms: 1.30x slower                                                  |
| Geometric mean | (ref)                                                  | 1.13x slower                                                           |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 44.9 ms                                                | 50.2 ms: 1.12x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.03x slower                                                           |

Benchmark hidden because not significant (3): genshi_text, mako, genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 867 ms: 2.23x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 927 ms: 1.99x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 476 ms: 1.95x faster                                                   |
| async_tree_none            | 741 ms                                                 | 387 ms: 1.92x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 398 ms: 1.77x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 563 ms: 1.74x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 653 ms: 1.69x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 711 ms: 1.52x faster                                                   |
| xml_etree_parse            | 241 ms                                                 | 188 ms: 1.28x faster                                                   |
| deepcopy                   | 468 us                                                 | 381 us: 1.23x faster                                                   |
| pyflate                    | 727 ms                                                 | 604 ms: 1.20x faster                                                   |
| deepcopy_memo              | 52.4 us                                                | 44.4 us: 1.18x faster                                                  |
| raytrace                   | 408 ms                                                 | 346 ms: 1.18x faster                                                   |
| float                      | 123 ms                                                 | 106 ms: 1.16x faster                                                   |
| sqlalchemy_declarative     | 218 ms                                                 | 188 ms: 1.16x faster                                                   |
| pylint                     | 465 ms                                                 | 405 ms: 1.15x faster                                                   |
| spectral_norm              | 156 ms                                                 | 136 ms: 1.14x faster                                                   |
| scimark_monte_carlo        | 96.4 ms                                                | 84.8 ms: 1.14x faster                                                  |
| regex_effbot               | 5.13 ms                                                | 4.52 ms: 1.14x faster                                                  |
| bpe_tokeniser              | 6.59 sec                                               | 5.80 sec: 1.14x faster                                                 |
| xml_etree_generate         | 127 ms                                                 | 112 ms: 1.13x faster                                                   |
| nqueens                    | 117 ms                                                 | 104 ms: 1.13x faster                                                   |
| mdp                        | 3.97 sec                                               | 3.54 sec: 1.12x faster                                                 |
| regex_compile              | 187 ms                                                 | 166 ms: 1.12x faster                                                   |
| xml_etree_iterparse        | 169 ms                                                 | 152 ms: 1.12x faster                                                   |
| tomli_loads                | 2.88 sec                                               | 2.58 sec: 1.12x faster                                                 |
| richards                   | 60.3 ms                                                | 54.3 ms: 1.11x faster                                                  |
| pidigits                   | 250 ms                                                 | 225 ms: 1.11x faster                                                   |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 6.06 ms: 1.11x faster                                                  |
| logging_simple             | 9.45 us                                                | 8.56 us: 1.10x faster                                                  |
| async_generators           | 589 ms                                                 | 535 ms: 1.10x faster                                                   |
| html5lib                   | 88.9 ms                                                | 81.4 ms: 1.09x faster                                                  |
| richards_super             | 72.8 ms                                                | 66.7 ms: 1.09x faster                                                  |
| typing_runtime_protocols   | 224 us                                                 | 206 us: 1.09x faster                                                   |
| scimark_fft                | 500 ms                                                 | 460 ms: 1.09x faster                                                   |
| comprehensions             | 27.1 us                                                | 25.2 us: 1.07x faster                                                  |
| pycparser                  | 1.79 sec                                               | 1.68 sec: 1.07x faster                                                 |
| go                         | 172 ms                                                 | 163 ms: 1.06x faster                                                   |
| sqlglot_transpile          | 2.34 ms                                                | 2.22 ms: 1.05x faster                                                  |
| generators                 | 41.1 ms                                                | 39.3 ms: 1.05x faster                                                  |
| pprint_pformat             | 1.98 sec                                               | 1.89 sec: 1.05x faster                                                 |
| coroutines                 | 29.5 ms                                                | 30.7 ms: 1.04x slower                                                  |
| json_loads                 | 37.9 us                                                | 39.5 us: 1.04x slower                                                  |
| docutils                   | 4.00 sec                                               | 4.17 sec: 1.04x slower                                                 |
| json_dumps                 | 14.3 ms                                                | 15.1 ms: 1.05x slower                                                  |
| nbody                      | 119 ms                                                 | 126 ms: 1.06x slower                                                   |
| regex_dna                  | 278 ms                                                 | 296 ms: 1.07x slower                                                   |
| fannkuch                   | 540 ms                                                 | 577 ms: 1.07x slower                                                   |
| chaos                      | 84.9 ms                                                | 92.3 ms: 1.09x slower                                                  |
| django_template            | 44.9 ms                                                | 50.2 ms: 1.12x slower                                                  |
| meteor_contest             | 146 ms                                                 | 164 ms: 1.12x slower                                                   |
| telco                      | 9.59 ms                                                | 10.8 ms: 1.12x slower                                                  |
| pickle_pure_python         | 436 us                                                 | 489 us: 1.12x slower                                                   |
| 2to3                       | 456 ms                                                 | 514 ms: 1.13x slower                                                   |
| json                       | 6.85 ms                                                | 7.75 ms: 1.13x slower                                                  |
| bench_thread_pool          | 3.48 ms                                                | 3.96 ms: 1.14x slower                                                  |
| deltablue                  | 4.27 ms                                                | 5.14 ms: 1.20x slower                                                  |
| python_startup             | 23.7 ms                                                | 30.7 ms: 1.30x slower                                                  |
| coverage                   | 95.4 ms                                                | 134 ms: 1.40x slower                                                   |
| gc_traversal               | 5.86 ms                                                | 8.92 ms: 1.52x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 4.60 ms: 2.37x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 100 ms: 4.84x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                           |

Benchmark hidden because not significant (28): genshi_text, scimark_sor, pprint_safe_repr, python_startup_no_site, deepcopy_reduce, sympy_sum, xml_etree_process, sqlglot_normalize, asyncio_websockets, logging_silent, unpickle_pure_python, crypto_pyaes, sqlglot_optimize, pathlib, sqlalchemy_imperative, sympy_integrate, sqlglot_parse, dulwich_log, thrift, mako, logging_format, sympy_str, scimark_lu, sympy_expand, sqlite_synth, hexiom, genshi_xml, regex_v8
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250120-3.14.0a4+-bca35f0/bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.072x faster

# HPT report

- Reliability score: 99.81% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.13x