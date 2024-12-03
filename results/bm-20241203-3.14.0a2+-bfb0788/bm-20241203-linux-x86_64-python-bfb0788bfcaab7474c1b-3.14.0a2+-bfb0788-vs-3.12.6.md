# Results vs. 3.12.6

- fork: python
- ref: bfb0788bfcaab7474c1b
- machine: linux-x86_64
- commit hash: bfb0788
- commit date: 2024-12-03
- overall geometric mean: 1.116x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| docutils       | 4.00 sec                                               | 3.56 sec: 1.12x faster                                                 |
| html5lib       | 88.9 ms                                                | 83.4 ms: 1.07x faster                                                  |
| Geometric mean | (ref)                                                  | 1.07x faster                                                           |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 879 ms: 2.20x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 864 ms: 2.14x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 483 ms: 2.02x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 469 ms: 1.99x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 355 ms: 1.98x faster                                                   |
| async_tree_none            | 741 ms                                                 | 426 ms: 1.74x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 680 ms: 1.62x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 682 ms: 1.58x faster                                                   |
| async_generators           | 589 ms                                                 | 546 ms: 1.08x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.60x faster                                                           |

Benchmark hidden because not significant (2): asyncio_websockets, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 108 ms: 1.13x faster                                                   |
| pidigits       | 250 ms                                                 | 234 ms: 1.07x faster                                                   |
| Geometric mean | (ref)                                                  | 1.06x faster                                                           |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.26 ms: 1.21x faster                                                  |
| regex_dna      | 278 ms                                                 | 268 ms: 1.04x faster                                                   |
| Geometric mean | (ref)                                                  | 1.06x faster                                                           |

Benchmark hidden because not significant (2): regex_compile, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 241 ms                                                 | 203 ms: 1.19x faster                                                   |
| json_loads           | 37.9 us                                                | 33.5 us: 1.13x faster                                                  |
| xml_etree_generate   | 127 ms                                                 | 114 ms: 1.12x faster                                                   |
| tomli_loads          | 2.88 sec                                               | 2.71 sec: 1.06x faster                                                 |
| unpickle_pure_python | 300 us                                                 | 285 us: 1.05x faster                                                   |
| xml_etree_process    | 83.7 ms                                                | 80.3 ms: 1.04x faster                                                  |
| json_dumps           | 14.3 ms                                                | 15.3 ms: 1.07x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.06x faster                                                           |

Benchmark hidden because not significant (2): xml_etree_iterparse, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 14.4 ms: 1.22x faster                                                  |
| Geometric mean         | (ref)                                                  | 1.10x faster                                                           |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text    | 30.2 ms                                                | 28.8 ms: 1.05x faster                                                  |
| Geometric mean | (ref)                                                  | 1.00x faster                                                           |

Benchmark hidden because not significant (3): genshi_xml, django_template, mako

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 879 ms: 2.20x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 864 ms: 2.14x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 483 ms: 2.02x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 469 ms: 1.99x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 355 ms: 1.98x faster                                                   |
| async_tree_none            | 741 ms                                                 | 426 ms: 1.74x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 680 ms: 1.62x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 682 ms: 1.58x faster                                                   |
| deepcopy                   | 468 us                                                 | 344 us: 1.36x faster                                                   |
| sqlalchemy_declarative     | 218 ms                                                 | 163 ms: 1.33x faster                                                   |
| deepcopy_memo              | 52.4 us                                                | 40.0 us: 1.31x faster                                                  |
| comprehensions             | 27.1 us                                                | 21.9 us: 1.24x faster                                                  |
| bench_thread_pool          | 3.48 ms                                                | 2.83 ms: 1.23x faster                                                  |
| python_startup_no_site     | 17.6 ms                                                | 14.4 ms: 1.22x faster                                                  |
| regex_effbot               | 5.13 ms                                                | 4.26 ms: 1.21x faster                                                  |
| logging_simple             | 9.45 us                                                | 7.91 us: 1.19x faster                                                  |
| xml_etree_parse            | 241 ms                                                 | 203 ms: 1.19x faster                                                   |
| pylint                     | 465 ms                                                 | 393 ms: 1.18x faster                                                   |
| raytrace                   | 408 ms                                                 | 348 ms: 1.17x faster                                                   |
| pathlib                    | 31.6 ms                                                | 27.1 ms: 1.17x faster                                                  |
| mdp                        | 3.97 sec                                               | 3.42 sec: 1.16x faster                                                 |
| bpe_tokeniser              | 6.59 sec                                               | 5.68 sec: 1.16x faster                                                 |
| logging_format             | 9.59 us                                                | 8.29 us: 1.16x faster                                                  |
| nqueens                    | 117 ms                                                 | 102 ms: 1.15x faster                                                   |
| pycparser                  | 1.79 sec                                               | 1.57 sec: 1.14x faster                                                 |
| sqlglot_optimize           | 76.0 ms                                                | 66.4 ms: 1.14x faster                                                  |
| sqlalchemy_imperative      | 24.7 ms                                                | 21.6 ms: 1.14x faster                                                  |
| float                      | 123 ms                                                 | 108 ms: 1.13x faster                                                   |
| json_loads                 | 37.9 us                                                | 33.5 us: 1.13x faster                                                  |
| deepcopy_reduce            | 4.04 us                                                | 3.58 us: 1.13x faster                                                  |
| sympy_sum                  | 222 ms                                                 | 197 ms: 1.12x faster                                                   |
| go                         | 172 ms                                                 | 154 ms: 1.12x faster                                                   |
| docutils                   | 4.00 sec                                               | 3.56 sec: 1.12x faster                                                 |
| xml_etree_generate         | 127 ms                                                 | 114 ms: 1.12x faster                                                   |
| pyflate                    | 727 ms                                                 | 656 ms: 1.11x faster                                                   |
| json                       | 6.85 ms                                                | 6.19 ms: 1.11x faster                                                  |
| crypto_pyaes               | 107 ms                                                 | 98.4 ms: 1.09x faster                                                  |
| scimark_monte_carlo        | 96.4 ms                                                | 89.1 ms: 1.08x faster                                                  |
| async_generators           | 589 ms                                                 | 546 ms: 1.08x faster                                                   |
| html5lib                   | 88.9 ms                                                | 83.4 ms: 1.07x faster                                                  |
| pidigits                   | 250 ms                                                 | 234 ms: 1.07x faster                                                   |
| pprint_pformat             | 1.98 sec                                               | 1.86 sec: 1.07x faster                                                 |
| chaos                      | 84.9 ms                                                | 79.8 ms: 1.06x faster                                                  |
| tomli_loads                | 2.88 sec                                               | 2.71 sec: 1.06x faster                                                 |
| dulwich_log                | 100 ms                                                 | 94.4 ms: 1.06x faster                                                  |
| scimark_sor                | 167 ms                                                 | 158 ms: 1.05x faster                                                   |
| sqlglot_transpile          | 2.34 ms                                                | 2.22 ms: 1.05x faster                                                  |
| unpickle_pure_python       | 300 us                                                 | 285 us: 1.05x faster                                                   |
| pprint_safe_repr           | 967 ms                                                 | 920 ms: 1.05x faster                                                   |
| genshi_text                | 30.2 ms                                                | 28.8 ms: 1.05x faster                                                  |
| generators                 | 41.1 ms                                                | 39.2 ms: 1.05x faster                                                  |
| sympy_str                  | 385 ms                                                 | 367 ms: 1.05x faster                                                   |
| richards_super             | 72.8 ms                                                | 69.6 ms: 1.05x faster                                                  |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 6.41 ms: 1.04x faster                                                  |
| scimark_fft                | 500 ms                                                 | 479 ms: 1.04x faster                                                   |
| xml_etree_process          | 83.7 ms                                                | 80.3 ms: 1.04x faster                                                  |
| regex_dna                  | 278 ms                                                 | 268 ms: 1.04x faster                                                   |
| richards                   | 60.3 ms                                                | 62.9 ms: 1.04x slower                                                  |
| sqlite_synth               | 3.87 us                                                | 4.04 us: 1.04x slower                                                  |
| telco                      | 9.59 ms                                                | 10.2 ms: 1.06x slower                                                  |
| json_dumps                 | 14.3 ms                                                | 15.3 ms: 1.07x slower                                                  |
| sqlglot_normalize          | 157 ms                                                 | 168 ms: 1.07x slower                                                   |
| coverage                   | 95.4 ms                                                | 102 ms: 1.07x slower                                                   |
| gc_traversal               | 5.86 ms                                                | 7.02 ms: 1.20x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 3.23 ms: 1.67x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 88.9 ms: 4.30x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.10x faster                                                           |

Benchmark hidden because not significant (24): xml_etree_iterparse, regex_compile, sympy_integrate, thrift, sqlglot_parse, genshi_xml, fannkuch, 2to3, meteor_contest, typing_runtime_protocols, asyncio_websockets, spectral_norm, scimark_lu, logging_silent, python_startup, pickle_pure_python, deltablue, nbody, django_template, coroutines, regex_v8, sympy_expand, hexiom, mako
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241203-3.14.0a2+-bfb0788/bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.116x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.13x