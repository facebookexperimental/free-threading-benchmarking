# Results vs. 3.12.6

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: d9efa45
- commit date: 2024-07-25
- overall geometric mean: 1.37x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.26x slower
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240725-linux-x86_64-python-main-3.14.0a0-d9efa45 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 456 ms                                                 | 690 ms: 1.51x slower                                  |
| docutils       | 4.00 sec                                               | 5.03 sec: 1.26x slower                                |
| html5lib       | 88.9 ms                                                | 138 ms: 1.55x slower                                  |
| tornado_http   | 266 ms                                                 | 358 ms: 1.35x slower                                  |
| Geometric mean | (ref)                                                  | 1.41x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240725-linux-x86_64-python-main-3.14.0a0-d9efa45 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.19 sec: 1.62x faster                                |
| async_tree_none_tg         | 704 ms                                                 | 471 ms: 1.49x faster                                  |
| async_tree_memoization_tg  | 930 ms                                                 | 641 ms: 1.45x faster                                  |
| async_tree_io              | 1.85 sec                                               | 1.28 sec: 1.45x faster                                |
| async_tree_memoization     | 977 ms                                                 | 744 ms: 1.31x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 843 ms: 1.31x faster                                  |
| async_tree_none            | 741 ms                                                 | 600 ms: 1.24x faster                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 975 ms: 1.11x faster                                  |
| asyncio_tcp                | 923 ms                                                 | 1.10 sec: 1.19x slower                                |
| asyncio_tcp_ssl            | 2.81 sec                                               | 3.42 sec: 1.22x slower                                |
| async_generators           | 589 ms                                                 | 741 ms: 1.26x slower                                  |
| coroutines                 | 29.5 ms                                                | 42.7 ms: 1.45x slower                                 |
| Geometric mean             | (ref)                                                  | 1.12x faster                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240725-linux-x86_64-python-main-3.14.0a0-d9efa45 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| float          | 123 ms                                                 | 201 ms: 1.64x slower                                  |
| nbody          | 119 ms                                                 | 291 ms: 2.44x slower                                  |
| Geometric mean | (ref)                                                  | 1.58x slower                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240725-linux-x86_64-python-main-3.14.0a0-d9efa45 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.78 ms: 1.07x faster                                 |
| regex_dna      | 278 ms                                                 | 289 ms: 1.04x slower                                  |
| regex_v8       | 32.5 ms                                                | 36.8 ms: 1.13x slower                                 |
| regex_compile  | 187 ms                                                 | 292 ms: 1.57x slower                                  |
| Geometric mean | (ref)                                                  | 1.14x slower                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240725-linux-x86_64-python-main-3.14.0a0-d9efa45 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| pickle_dict          | 52.7 us                                                | 44.3 us: 1.19x faster                                 |
| pickle               | 16.4 us                                                | 14.4 us: 1.14x faster                                 |
| xml_etree_parse      | 241 ms                                                 | 213 ms: 1.13x faster                                  |
| pickle_list          | 6.97 us                                                | 6.46 us: 1.08x faster                                 |
| json_loads           | 37.9 us                                                | 44.5 us: 1.17x slower                                 |
| xml_etree_generate   | 127 ms                                                 | 163 ms: 1.28x slower                                  |
| json_dumps           | 14.3 ms                                                | 18.3 ms: 1.28x slower                                 |
| tomli_loads          | 2.88 sec                                               | 4.33 sec: 1.50x slower                                |
| xml_etree_process    | 83.7 ms                                                | 137 ms: 1.64x slower                                  |
| pickle_pure_python   | 436 us                                                 | 768 us: 1.76x slower                                  |
| unpickle_pure_python | 300 us                                                 | 573 us: 1.91x slower                                  |
| Geometric mean       | (ref)                                                  | 1.18x slower                                          |

Benchmark hidden because not significant (3): unpickle_list, unpickle, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240725-linux-x86_64-python-main-3.14.0a0-d9efa45 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 19.9 ms: 1.13x slower                                 |
| python_startup         | 23.7 ms                                                | 29.3 ms: 1.24x slower                                 |
| Geometric mean         | (ref)                                                  | 1.18x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240725-linux-x86_64-python-main-3.14.0a0-d9efa45 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_xml      | 67.6 ms                                                | 117 ms: 1.73x slower                                  |
| django_template | 44.9 ms                                                | 81.6 ms: 1.82x slower                                 |
| mako            | 15.7 ms                                                | 29.5 ms: 1.88x slower                                 |
| genshi_text     | 30.2 ms                                                | 57.9 ms: 1.92x slower                                 |
| Geometric mean  | (ref)                                                  | 1.83x slower                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240725-linux-x86_64-python-main-3.14.0a0-d9efa45 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.19 sec: 1.62x faster                                |
| async_tree_none_tg         | 704 ms                                                 | 471 ms: 1.49x faster                                  |
| async_tree_memoization_tg  | 930 ms                                                 | 641 ms: 1.45x faster                                  |
| async_tree_io              | 1.85 sec                                               | 1.28 sec: 1.45x faster                                |
| async_tree_memoization     | 977 ms                                                 | 744 ms: 1.31x faster                                  |
| bench_mp_pool              | 20.7 ms                                                | 15.8 ms: 1.31x faster                                 |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 843 ms: 1.31x faster                                  |
| gc_traversal               | 5.86 ms                                                | 4.66 ms: 1.26x faster                                 |
| async_tree_none            | 741 ms                                                 | 600 ms: 1.24x faster                                  |
| pickle_dict                | 52.7 us                                                | 44.3 us: 1.19x faster                                 |
| pickle                     | 16.4 us                                                | 14.4 us: 1.14x faster                                 |
| xml_etree_parse            | 241 ms                                                 | 213 ms: 1.13x faster                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 975 ms: 1.11x faster                                  |
| pickle_list                | 6.97 us                                                | 6.46 us: 1.08x faster                                 |
| regex_effbot               | 5.13 ms                                                | 4.78 ms: 1.07x faster                                 |
| regex_dna                  | 278 ms                                                 | 289 ms: 1.04x slower                                  |
| sqlite_synth               | 3.87 us                                                | 4.23 us: 1.09x slower                                 |
| pathlib                    | 31.6 ms                                                | 35.5 ms: 1.12x slower                                 |
| python_startup_no_site     | 17.6 ms                                                | 19.9 ms: 1.13x slower                                 |
| regex_v8                   | 32.5 ms                                                | 36.8 ms: 1.13x slower                                 |
| bench_thread_pool          | 3.48 ms                                                | 3.97 ms: 1.14x slower                                 |
| json_loads                 | 37.9 us                                                | 44.5 us: 1.17x slower                                 |
| asyncio_tcp                | 923 ms                                                 | 1.10 sec: 1.19x slower                                |
| deepcopy                   | 468 us                                                 | 566 us: 1.21x slower                                  |
| asyncio_tcp_ssl            | 2.81 sec                                               | 3.42 sec: 1.22x slower                                |
| pycparser                  | 1.79 sec                                               | 2.21 sec: 1.23x slower                                |
| python_startup             | 23.7 ms                                                | 29.3 ms: 1.24x slower                                 |
| json                       | 6.85 ms                                                | 8.50 ms: 1.24x slower                                 |
| scimark_fft                | 500 ms                                                 | 621 ms: 1.24x slower                                  |
| docutils                   | 4.00 sec                                               | 5.03 sec: 1.26x slower                                |
| async_generators           | 589 ms                                                 | 741 ms: 1.26x slower                                  |
| xml_etree_generate         | 127 ms                                                 | 163 ms: 1.28x slower                                  |
| pylint                     | 465 ms                                                 | 595 ms: 1.28x slower                                  |
| json_dumps                 | 14.3 ms                                                | 18.3 ms: 1.28x slower                                 |
| mdp                        | 3.97 sec                                               | 5.12 sec: 1.29x slower                                |
| nqueens                    | 117 ms                                                 | 151 ms: 1.29x slower                                  |
| deepcopy_memo              | 52.4 us                                                | 67.8 us: 1.29x slower                                 |
| tornado_http               | 266 ms                                                 | 358 ms: 1.35x slower                                  |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 9.05 ms: 1.35x slower                                 |
| crypto_pyaes               | 107 ms                                                 | 149 ms: 1.39x slower                                  |
| generators                 | 41.1 ms                                                | 57.4 ms: 1.40x slower                                 |
| meteor_contest             | 146 ms                                                 | 206 ms: 1.41x slower                                  |
| telco                      | 9.59 ms                                                | 13.8 ms: 1.44x slower                                 |
| comprehensions             | 27.1 us                                                | 39.2 us: 1.45x slower                                 |
| coroutines                 | 29.5 ms                                                | 42.7 ms: 1.45x slower                                 |
| fannkuch                   | 540 ms                                                 | 802 ms: 1.48x slower                                  |
| sqlglot_normalize          | 157 ms                                                 | 233 ms: 1.49x slower                                  |
| sympy_integrate            | 29.8 ms                                                | 44.3 ms: 1.49x slower                                 |
| deepcopy_reduce            | 4.04 us                                                | 6.02 us: 1.49x slower                                 |
| tomli_loads                | 2.88 sec                                               | 4.33 sec: 1.50x slower                                |
| pyflate                    | 727 ms                                                 | 1.09 sec: 1.51x slower                                |
| bpe_tokeniser              | 6.59 sec                                               | 9.93 sec: 1.51x slower                                |
| 2to3                       | 456 ms                                                 | 690 ms: 1.51x slower                                  |
| html5lib                   | 88.9 ms                                                | 138 ms: 1.55x slower                                  |
| spectral_norm              | 156 ms                                                 | 244 ms: 1.57x slower                                  |
| regex_compile              | 187 ms                                                 | 292 ms: 1.57x slower                                  |
| coverage                   | 95.4 ms                                                | 149 ms: 1.57x slower                                  |
| sqlglot_optimize           | 76.0 ms                                                | 123 ms: 1.62x slower                                  |
| float                      | 123 ms                                                 | 201 ms: 1.64x slower                                  |
| xml_etree_process          | 83.7 ms                                                | 137 ms: 1.64x slower                                  |
| thrift                     | 1.06 ms                                                | 1.77 ms: 1.67x slower                                 |
| logging_simple             | 9.45 us                                                | 15.9 us: 1.68x slower                                 |
| typing_runtime_protocols   | 224 us                                                 | 377 us: 1.68x slower                                  |
| genshi_xml                 | 67.6 ms                                                | 117 ms: 1.73x slower                                  |
| richards                   | 60.3 ms                                                | 105 ms: 1.73x slower                                  |
| scimark_monte_carlo        | 96.4 ms                                                | 168 ms: 1.75x slower                                  |
| pickle_pure_python         | 436 us                                                 | 768 us: 1.76x slower                                  |
| pprint_safe_repr           | 967 ms                                                 | 1.74 sec: 1.80x slower                                |
| django_template            | 44.9 ms                                                | 81.6 ms: 1.82x slower                                 |
| pprint_pformat             | 1.98 sec                                               | 3.60 sec: 1.82x slower                                |
| richards_super             | 72.8 ms                                                | 134 ms: 1.84x slower                                  |
| sympy_str                  | 385 ms                                                 | 713 ms: 1.85x slower                                  |
| logging_silent             | 139 ns                                                 | 259 ns: 1.86x slower                                  |
| mako                       | 15.7 ms                                                | 29.5 ms: 1.88x slower                                 |
| logging_format             | 9.59 us                                                | 18.2 us: 1.90x slower                                 |
| unpickle_pure_python       | 300 us                                                 | 573 us: 1.91x slower                                  |
| genshi_text                | 30.2 ms                                                | 57.9 ms: 1.92x slower                                 |
| raytrace                   | 408 ms                                                 | 805 ms: 1.97x slower                                  |
| hexiom                     | 8.27 ms                                                | 16.3 ms: 1.98x slower                                 |
| sqlglot_transpile          | 2.34 ms                                                | 4.65 ms: 1.99x slower                                 |
| scimark_sor                | 167 ms                                                 | 342 ms: 2.06x slower                                  |
| chaos                      | 84.9 ms                                                | 175 ms: 2.06x slower                                  |
| scimark_lu                 | 152 ms                                                 | 323 ms: 2.12x slower                                  |
| sqlglot_parse              | 1.79 ms                                                | 3.81 ms: 2.13x slower                                 |
| sympy_sum                  | 222 ms                                                 | 487 ms: 2.20x slower                                  |
| sympy_expand               | 582 ms                                                 | 1.29 sec: 2.23x slower                                |
| go                         | 172 ms                                                 | 405 ms: 2.35x slower                                  |
| nbody                      | 119 ms                                                 | 291 ms: 2.44x slower                                  |
| deltablue                  | 4.27 ms                                                | 12.1 ms: 2.84x slower                                 |
| unpack_sequence            | 60.2 ns                                                | 190 ns: 3.16x slower                                  |
| Geometric mean             | (ref)                                                  | 1.37x slower                                          |

Benchmark hidden because not significant (6): create_gc_cycles, pidigits, unpickle_list, asyncio_websockets, unpickle, xml_etree_iterparse
Ignored benchmarks (9) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.31x
- 95% likely to have a slowdown of 1.28x
- 99% likely to have a slowdown of 1.26x

# Memory
- memory change: 1.16x