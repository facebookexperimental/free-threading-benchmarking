# Results vs. 3.12.5+

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: e001027
- commit date: 2024-08-15
- overall geometric mean: 1.41x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.28x slower
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027 |
|----------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 456 ms                                               | 698 ms: 1.53x slower                                  |
| docutils       | 4.05 sec                                             | 5.02 sec: 1.24x slower                                |
| html5lib       | 100 ms                                               | 149 ms: 1.49x slower                                  |
| tornado_http   | 261 ms                                               | 429 ms: 1.64x slower                                  |
| Geometric mean | (ref)                                                | 1.47x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027 |
|----------------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.87 sec                                             | 1.19 sec: 1.57x faster                                |
| async_tree_none_tg         | 726 ms                                               | 510 ms: 1.42x faster                                  |
| async_tree_memoization_tg  | 912 ms                                               | 647 ms: 1.41x faster                                  |
| async_tree_io              | 1.86 sec                                             | 1.34 sec: 1.39x faster                                |
| async_tree_none            | 820 ms                                               | 614 ms: 1.33x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.12 sec                                             | 846 ms: 1.32x faster                                  |
| async_tree_memoization     | 975 ms                                               | 759 ms: 1.28x faster                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                             | 974 ms: 1.17x faster                                  |
| asyncio_websockets         | 752 ms                                               | 795 ms: 1.06x slower                                  |
| asyncio_tcp                | 988 ms                                               | 1.12 sec: 1.14x slower                                |
| asyncio_tcp_ssl            | 2.82 sec                                             | 3.41 sec: 1.21x slower                                |
| async_generators           | 615 ms                                               | 763 ms: 1.24x slower                                  |
| coroutines                 | 30.6 ms                                              | 43.6 ms: 1.42x slower                                 |
| Geometric mean             | (ref)                                                | 1.12x faster                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027 |
|----------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| pidigits       | 256 ms                                               | 275 ms: 1.07x slower                                  |
| float          | 124 ms                                               | 191 ms: 1.53x slower                                  |
| nbody          | 117 ms                                               | 317 ms: 2.72x slower                                  |
| Geometric mean | (ref)                                                | 1.65x slower                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027 |
|----------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| regex_effbot   | 5.02 ms                                              | 4.79 ms: 1.05x faster                                 |
| regex_dna      | 268 ms                                               | 297 ms: 1.11x slower                                  |
| regex_v8       | 29.9 ms                                              | 36.7 ms: 1.22x slower                                 |
| regex_compile  | 186 ms                                               | 303 ms: 1.63x slower                                  |
| Geometric mean | (ref)                                                | 1.20x slower                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027 |
|----------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| unpickle             | 21.6 us                                              | 23.1 us: 1.07x slower                                 |
| unpickle_list        | 6.83 us                                              | 7.97 us: 1.17x slower                                 |
| json_dumps           | 14.0 ms                                              | 17.9 ms: 1.28x slower                                 |
| xml_etree_generate   | 138 ms                                               | 180 ms: 1.31x slower                                  |
| json_loads           | 35.9 us                                              | 48.4 us: 1.35x slower                                 |
| tomli_loads          | 2.86 sec                                             | 4.36 sec: 1.53x slower                                |
| xml_etree_process    | 82.7 ms                                              | 133 ms: 1.61x slower                                  |
| unpickle_pure_python | 304 us                                               | 574 us: 1.89x slower                                  |
| pickle_pure_python   | 436 us                                               | 910 us: 2.09x slower                                  |
| Geometric mean       | (ref)                                                | 1.26x slower                                          |

Benchmark hidden because not significant (5): pickle_list, xml_etree_parse, pickle, pickle_dict, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027 |
|------------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| python_startup         | 22.7 ms                                              | 31.2 ms: 1.38x slower                                 |
| python_startup_no_site | 16.2 ms                                              | 22.7 ms: 1.40x slower                                 |
| Geometric mean         | (ref)                                                | 1.39x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027 |
|-----------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| genshi_xml      | 69.1 ms                                              | 118 ms: 1.71x slower                                  |
| django_template | 45.4 ms                                              | 80.8 ms: 1.78x slower                                 |
| mako            | 16.1 ms                                              | 30.6 ms: 1.89x slower                                 |
| genshi_text     | 30.3 ms                                              | 59.2 ms: 1.95x slower                                 |
| Geometric mean  | (ref)                                                | 1.83x slower                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027 |
|----------------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.87 sec                                             | 1.19 sec: 1.57x faster                                |
| async_tree_none_tg         | 726 ms                                               | 510 ms: 1.42x faster                                  |
| async_tree_memoization_tg  | 912 ms                                               | 647 ms: 1.41x faster                                  |
| async_tree_io              | 1.86 sec                                             | 1.34 sec: 1.39x faster                                |
| async_tree_none            | 820 ms                                               | 614 ms: 1.33x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.12 sec                                             | 846 ms: 1.32x faster                                  |
| async_tree_memoization     | 975 ms                                               | 759 ms: 1.28x faster                                  |
| bench_mp_pool              | 21.2 ms                                              | 17.0 ms: 1.25x faster                                 |
| gc_traversal               | 6.42 ms                                              | 5.18 ms: 1.24x faster                                 |
| async_tree_cpu_io_mixed    | 1.14 sec                                             | 974 ms: 1.17x faster                                  |
| regex_effbot               | 5.02 ms                                              | 4.79 ms: 1.05x faster                                 |
| asyncio_websockets         | 752 ms                                               | 795 ms: 1.06x slower                                  |
| unpickle                   | 21.6 us                                              | 23.1 us: 1.07x slower                                 |
| pidigits                   | 256 ms                                               | 275 ms: 1.07x slower                                  |
| regex_dna                  | 268 ms                                               | 297 ms: 1.11x slower                                  |
| asyncio_tcp                | 988 ms                                               | 1.12 sec: 1.14x slower                                |
| sqlite_synth               | 3.77 us                                              | 4.35 us: 1.15x slower                                 |
| unpickle_list              | 6.83 us                                              | 7.97 us: 1.17x slower                                 |
| generators                 | 44.7 ms                                              | 53.0 ms: 1.19x slower                                 |
| pathlib                    | 31.6 ms                                              | 37.5 ms: 1.19x slower                                 |
| asyncio_tcp_ssl            | 2.82 sec                                             | 3.41 sec: 1.21x slower                                |
| pylint                     | 480 ms                                               | 586 ms: 1.22x slower                                  |
| deepcopy                   | 486 us                                               | 596 us: 1.22x slower                                  |
| regex_v8                   | 29.9 ms                                              | 36.7 ms: 1.22x slower                                 |
| json                       | 7.14 ms                                              | 8.77 ms: 1.23x slower                                 |
| docutils                   | 4.05 sec                                             | 5.02 sec: 1.24x slower                                |
| async_generators           | 615 ms                                               | 763 ms: 1.24x slower                                  |
| json_dumps                 | 14.0 ms                                              | 17.9 ms: 1.28x slower                                 |
| xml_etree_generate         | 138 ms                                               | 180 ms: 1.31x slower                                  |
| scimark_sparse_mat_mult    | 6.94 ms                                              | 9.11 ms: 1.31x slower                                 |
| pycparser                  | 1.68 sec                                             | 2.21 sec: 1.32x slower                                |
| scimark_fft                | 481 ms                                               | 642 ms: 1.33x slower                                  |
| deepcopy_reduce            | 4.18 us                                              | 5.58 us: 1.34x slower                                 |
| json_loads                 | 35.9 us                                              | 48.4 us: 1.35x slower                                 |
| bench_thread_pool          | 3.42 ms                                              | 4.67 ms: 1.37x slower                                 |
| crypto_pyaes               | 110 ms                                               | 150 ms: 1.37x slower                                  |
| python_startup             | 22.7 ms                                              | 31.2 ms: 1.38x slower                                 |
| comprehensions             | 28.6 us                                              | 39.5 us: 1.38x slower                                 |
| meteor_contest             | 146 ms                                               | 203 ms: 1.39x slower                                  |
| deepcopy_memo              | 51.0 us                                              | 70.9 us: 1.39x slower                                 |
| python_startup_no_site     | 16.2 ms                                              | 22.7 ms: 1.40x slower                                 |
| mdp                        | 3.77 sec                                             | 5.29 sec: 1.40x slower                                |
| coroutines                 | 30.6 ms                                              | 43.6 ms: 1.42x slower                                 |
| telco                      | 9.53 ms                                              | 14.1 ms: 1.48x slower                                 |
| html5lib                   | 100 ms                                               | 149 ms: 1.49x slower                                  |
| fannkuch                   | 525 ms                                               | 786 ms: 1.50x slower                                  |
| nqueens                    | 116 ms                                               | 175 ms: 1.52x slower                                  |
| tomli_loads                | 2.86 sec                                             | 4.36 sec: 1.53x slower                                |
| bpe_tokeniser              | 6.76 sec                                             | 10.3 sec: 1.53x slower                                |
| 2to3                       | 456 ms                                               | 698 ms: 1.53x slower                                  |
| float                      | 124 ms                                               | 191 ms: 1.53x slower                                  |
| thrift                     | 1.10 ms                                              | 1.70 ms: 1.54x slower                                 |
| logging_simple             | 9.68 us                                              | 14.9 us: 1.54x slower                                 |
| coverage                   | 96.9 ms                                              | 152 ms: 1.57x slower                                  |
| typing_runtime_protocols   | 224 us                                               | 355 us: 1.59x slower                                  |
| sqlglot_optimize           | 80.2 ms                                              | 128 ms: 1.60x slower                                  |
| xml_etree_process          | 82.7 ms                                              | 133 ms: 1.61x slower                                  |
| regex_compile              | 186 ms                                               | 303 ms: 1.63x slower                                  |
| tornado_http               | 261 ms                                               | 429 ms: 1.64x slower                                  |
| sympy_integrate            | 29.0 ms                                              | 48.4 ms: 1.67x slower                                 |
| sqlglot_normalize          | 144 ms                                               | 240 ms: 1.67x slower                                  |
| genshi_xml                 | 69.1 ms                                              | 118 ms: 1.71x slower                                  |
| pyflate                    | 664 ms                                               | 1.13 sec: 1.71x slower                                |
| richards                   | 62.8 ms                                              | 107 ms: 1.71x slower                                  |
| scimark_monte_carlo        | 96.8 ms                                              | 170 ms: 1.76x slower                                  |
| django_template            | 45.4 ms                                              | 80.8 ms: 1.78x slower                                 |
| spectral_norm              | 136 ms                                               | 245 ms: 1.79x slower                                  |
| pprint_pformat             | 1.99 sec                                             | 3.57 sec: 1.80x slower                                |
| pprint_safe_repr           | 972 ms                                               | 1.77 sec: 1.82x slower                                |
| logging_format             | 9.56 us                                              | 17.9 us: 1.87x slower                                 |
| unpickle_pure_python       | 304 us                                               | 574 us: 1.89x slower                                  |
| mako                       | 16.1 ms                                              | 30.6 ms: 1.89x slower                                 |
| chaos                      | 92.1 ms                                              | 175 ms: 1.90x slower                                  |
| logging_silent             | 139 ns                                               | 267 ns: 1.91x slower                                  |
| sympy_str                  | 379 ms                                               | 730 ms: 1.93x slower                                  |
| sqlglot_transpile          | 2.32 ms                                              | 4.53 ms: 1.95x slower                                 |
| genshi_text                | 30.3 ms                                              | 59.2 ms: 1.95x slower                                 |
| richards_super             | 69.7 ms                                              | 137 ms: 1.96x slower                                  |
| hexiom                     | 8.19 ms                                              | 16.3 ms: 1.99x slower                                 |
| raytrace                   | 405 ms                                               | 816 ms: 2.02x slower                                  |
| sqlglot_parse              | 1.85 ms                                              | 3.81 ms: 2.05x slower                                 |
| scimark_sor                | 170 ms                                               | 354 ms: 2.08x slower                                  |
| pickle_pure_python         | 436 us                                               | 910 us: 2.09x slower                                  |
| scimark_lu                 | 155 ms                                               | 330 ms: 2.13x slower                                  |
| sympy_expand               | 591 ms                                               | 1.31 sec: 2.22x slower                                |
| sympy_sum                  | 218 ms                                               | 509 ms: 2.33x slower                                  |
| deltablue                  | 4.45 ms                                              | 11.3 ms: 2.54x slower                                 |
| go                         | 173 ms                                               | 452 ms: 2.61x slower                                  |
| unpack_sequence            | 70.8 ns                                              | 191 ns: 2.70x slower                                  |
| nbody                      | 117 ms                                               | 317 ms: 2.72x slower                                  |
| Geometric mean             | (ref)                                                | 1.41x slower                                          |

Benchmark hidden because not significant (6): pickle_list, xml_etree_parse, create_gc_cycles, pickle, pickle_dict, xml_etree_iterparse
Ignored benchmarks (9) of results/bm-20240814-3.12.5+-9f153a2/bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.36x
- 95% likely to have a slowdown of 1.33x
- 99% likely to have a slowdown of 1.28x

# Memory
- memory change: 1.15x