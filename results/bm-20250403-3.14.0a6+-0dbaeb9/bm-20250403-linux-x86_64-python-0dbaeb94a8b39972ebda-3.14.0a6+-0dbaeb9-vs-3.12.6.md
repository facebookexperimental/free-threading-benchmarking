# Results vs. 3.12.6

- fork: python
- ref: 0dbaeb94a8b39972ebda
- machine: linux-x86_64
- commit hash: 0dbaeb9
- commit date: 2025-04-03
- overall geometric mean: 1.115x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

Benchmark hidden because not significant (2): 2to3, docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250403-linux-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_memoization     | 977 ms                                                 | 478 ms: 2.04x faster                                                   |
| async_tree_io_tg           | 1.93 sec                                               | 952 ms: 2.03x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 939 ms: 1.97x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 486 ms: 1.91x faster                                                   |
| async_tree_none            | 741 ms                                                 | 389 ms: 1.91x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 384 ms: 1.84x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 693 ms: 1.59x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 714 ms: 1.51x faster                                                   |
| async_generators           | 589 ms                                                 | 525 ms: 1.12x faster                                                   |
| coroutines                 | 29.5 ms                                                | 31.5 ms: 1.07x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.57x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250403-linux-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 97.7 ms: 1.26x faster                                                  |
| pidigits       | 250 ms                                                 | 239 ms: 1.05x faster                                                   |
| nbody          | 119 ms                                                 | 129 ms: 1.08x slower                                                   |
| Geometric mean | (ref)                                                  | 1.07x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250403-linux-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.38 ms: 1.17x faster                                                  |
| regex_compile  | 187 ms                                                 | 167 ms: 1.12x faster                                                   |
| regex_v8       | 32.5 ms                                                | 29.2 ms: 1.11x faster                                                  |
| Geometric mean | (ref)                                                  | 1.09x faster                                                           |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark         | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250403-linux-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|-------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse   | 241 ms                                                 | 203 ms: 1.19x faster                                                   |
| tomli_loads       | 2.88 sec                                               | 2.52 sec: 1.14x faster                                                 |
| xml_etree_process | 83.7 ms                                                | 77.0 ms: 1.09x faster                                                  |
| json_loads        | 37.9 us                                                | 39.7 us: 1.05x slower                                                  |
| json_dumps        | 14.3 ms                                                | 15.6 ms: 1.09x slower                                                  |
| Geometric mean    | (ref)                                                  | 1.04x faster                                                           |

Benchmark hidden because not significant (4): xml_etree_generate, unpickle_pure_python, xml_etree_iterparse, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250403-linux-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 20.3 ms: 1.16x slower                                                  |
| python_startup         | 23.7 ms                                                | 31.8 ms: 1.34x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.25x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250403-linux-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 44.9 ms                                                | 47.1 ms: 1.05x slower                                                  |
| mako            | 15.7 ms                                                | 18.7 ms: 1.19x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.06x slower                                                           |

Benchmark hidden because not significant (2): genshi_text, genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250403-linux-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_memoization     | 977 ms                                                 | 478 ms: 2.04x faster                                                   |
| async_tree_io_tg           | 1.93 sec                                               | 952 ms: 2.03x faster                                                   |
| mdp                        | 3.97 sec                                               | 1.98 sec: 2.00x faster                                                 |
| async_tree_io              | 1.85 sec                                               | 939 ms: 1.97x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 486 ms: 1.91x faster                                                   |
| async_tree_none            | 741 ms                                                 | 389 ms: 1.91x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 384 ms: 1.84x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 693 ms: 1.59x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 714 ms: 1.51x faster                                                   |
| deepcopy                   | 468 us                                                 | 344 us: 1.36x faster                                                   |
| deepcopy_memo              | 52.4 us                                                | 39.0 us: 1.34x faster                                                  |
| float                      | 123 ms                                                 | 97.7 ms: 1.26x faster                                                  |
| comprehensions             | 27.1 us                                                | 21.9 us: 1.24x faster                                                  |
| spectral_norm              | 156 ms                                                 | 126 ms: 1.23x faster                                                   |
| raytrace                   | 408 ms                                                 | 335 ms: 1.22x faster                                                   |
| dulwich_log                | 100 ms                                                 | 83.0 ms: 1.21x faster                                                  |
| sqlalchemy_declarative     | 218 ms                                                 | 181 ms: 1.20x faster                                                   |
| pyflate                    | 727 ms                                                 | 606 ms: 1.20x faster                                                   |
| xml_etree_parse            | 241 ms                                                 | 203 ms: 1.19x faster                                                   |
| regex_effbot               | 5.13 ms                                                | 4.38 ms: 1.17x faster                                                  |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 5.75 ms: 1.17x faster                                                  |
| crypto_pyaes               | 107 ms                                                 | 93.0 ms: 1.15x faster                                                  |
| pylint                     | 465 ms                                                 | 405 ms: 1.15x faster                                                   |
| richards_super             | 72.8 ms                                                | 63.5 ms: 1.15x faster                                                  |
| pycparser                  | 1.79 sec                                               | 1.56 sec: 1.14x faster                                                 |
| tomli_loads                | 2.88 sec                                               | 2.52 sec: 1.14x faster                                                 |
| scimark_fft                | 500 ms                                                 | 438 ms: 1.14x faster                                                   |
| scimark_monte_carlo        | 96.4 ms                                                | 84.5 ms: 1.14x faster                                                  |
| chaos                      | 84.9 ms                                                | 74.4 ms: 1.14x faster                                                  |
| deepcopy_reduce            | 4.04 us                                                | 3.54 us: 1.14x faster                                                  |
| go                         | 172 ms                                                 | 153 ms: 1.13x faster                                                   |
| async_generators           | 589 ms                                                 | 525 ms: 1.12x faster                                                   |
| sympy_sum                  | 222 ms                                                 | 198 ms: 1.12x faster                                                   |
| regex_compile              | 187 ms                                                 | 167 ms: 1.12x faster                                                   |
| regex_v8                   | 32.5 ms                                                | 29.2 ms: 1.11x faster                                                  |
| sqlalchemy_imperative      | 24.7 ms                                                | 22.3 ms: 1.11x faster                                                  |
| nqueens                    | 117 ms                                                 | 107 ms: 1.10x faster                                                   |
| logging_silent             | 139 ns                                                 | 127 ns: 1.10x faster                                                   |
| xml_etree_process          | 83.7 ms                                                | 77.0 ms: 1.09x faster                                                  |
| scimark_sor                | 167 ms                                                 | 154 ms: 1.08x faster                                                   |
| bpe_tokeniser              | 6.59 sec                                               | 6.12 sec: 1.08x faster                                                 |
| sympy_integrate            | 29.8 ms                                                | 27.7 ms: 1.07x faster                                                  |
| pathlib                    | 31.6 ms                                                | 29.5 ms: 1.07x faster                                                  |
| fannkuch                   | 540 ms                                                 | 505 ms: 1.07x faster                                                   |
| sympy_str                  | 385 ms                                                 | 361 ms: 1.07x faster                                                   |
| logging_simple             | 9.45 us                                                | 8.89 us: 1.06x faster                                                  |
| pprint_pformat             | 1.98 sec                                               | 1.87 sec: 1.06x faster                                                 |
| pprint_safe_repr           | 967 ms                                                 | 920 ms: 1.05x faster                                                   |
| typing_runtime_protocols   | 224 us                                                 | 214 us: 1.05x faster                                                   |
| pidigits                   | 250 ms                                                 | 239 ms: 1.05x faster                                                   |
| json_loads                 | 37.9 us                                                | 39.7 us: 1.05x slower                                                  |
| django_template            | 44.9 ms                                                | 47.1 ms: 1.05x slower                                                  |
| sympy_expand               | 582 ms                                                 | 610 ms: 1.05x slower                                                   |
| generators                 | 41.1 ms                                                | 43.6 ms: 1.06x slower                                                  |
| deltablue                  | 4.27 ms                                                | 4.54 ms: 1.06x slower                                                  |
| coroutines                 | 29.5 ms                                                | 31.5 ms: 1.07x slower                                                  |
| logging_format             | 9.59 us                                                | 10.2 us: 1.07x slower                                                  |
| nbody                      | 119 ms                                                 | 129 ms: 1.08x slower                                                   |
| json_dumps                 | 14.3 ms                                                | 15.6 ms: 1.09x slower                                                  |
| telco                      | 9.59 ms                                                | 10.6 ms: 1.10x slower                                                  |
| bench_thread_pool          | 3.48 ms                                                | 3.88 ms: 1.11x slower                                                  |
| python_startup_no_site     | 17.6 ms                                                | 20.3 ms: 1.16x slower                                                  |
| coverage                   | 95.4 ms                                                | 112 ms: 1.18x slower                                                   |
| mako                       | 15.7 ms                                                | 18.7 ms: 1.19x slower                                                  |
| python_startup             | 23.7 ms                                                | 31.8 ms: 1.34x slower                                                  |
| gc_traversal               | 5.86 ms                                                | 8.37 ms: 1.43x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 4.09 ms: 2.11x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 95.9 ms: 4.63x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.09x faster                                                           |

Benchmark hidden because not significant (16): genshi_text, xml_etree_generate, unpickle_pure_python, hexiom, meteor_contest, scimark_lu, richards, asyncio_websockets, sqlite_synth, docutils, xml_etree_iterparse, pickle_pure_python, regex_dna, json, 2to3, genshi_xml
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250403-3.14.0a6+-0dbaeb9/bm-20250403-linux-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.115x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.14x