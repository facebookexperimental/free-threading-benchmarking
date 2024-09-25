# Results vs. 3.12.5+

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: a9bb3c7
- commit date: 2024-07-23
- overall geometric mean: 1.32x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.22x slower
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 456 ms                                               | 661 ms: 1.45x slower                                  |
| docutils       | 4.05 sec                                             | 4.69 sec: 1.16x slower                                |
| html5lib       | 100 ms                                               | 135 ms: 1.35x slower                                  |
| tornado_http   | 261 ms                                               | 320 ms: 1.23x slower                                  |
| Geometric mean | (ref)                                                | 1.29x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.87 sec                                             | 1.15 sec: 1.62x faster                                |
| async_tree_none_tg         | 726 ms                                               | 479 ms: 1.52x faster                                  |
| async_tree_io              | 1.86 sec                                             | 1.25 sec: 1.49x faster                                |
| async_tree_memoization_tg  | 912 ms                                               | 632 ms: 1.44x faster                                  |
| async_tree_none            | 820 ms                                               | 578 ms: 1.42x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.12 sec                                             | 806 ms: 1.39x faster                                  |
| async_tree_memoization     | 975 ms                                               | 728 ms: 1.34x faster                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                             | 926 ms: 1.23x faster                                  |
| asyncio_websockets         | 752 ms                                               | 714 ms: 1.05x faster                                  |
| asyncio_tcp                | 988 ms                                               | 1.05 sec: 1.06x slower                                |
| asyncio_tcp_ssl            | 2.82 sec                                             | 3.12 sec: 1.11x slower                                |
| async_generators           | 615 ms                                               | 739 ms: 1.20x slower                                  |
| coroutines                 | 30.6 ms                                              | 40.7 ms: 1.33x slower                                 |
| Geometric mean             | (ref)                                                | 1.19x faster                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| pidigits       | 256 ms                                               | 241 ms: 1.06x faster                                  |
| float          | 124 ms                                               | 199 ms: 1.60x slower                                  |
| nbody          | 117 ms                                               | 284 ms: 2.43x slower                                  |
| Geometric mean | (ref)                                                | 1.54x slower                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| regex_effbot   | 5.02 ms                                              | 4.60 ms: 1.09x faster                                 |
| regex_dna      | 268 ms                                               | 285 ms: 1.06x slower                                  |
| regex_v8       | 29.9 ms                                              | 35.5 ms: 1.18x slower                                 |
| regex_compile  | 186 ms                                               | 287 ms: 1.54x slower                                  |
| Geometric mean | (ref)                                                | 1.15x slower                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| xml_etree_parse      | 244 ms                                               | 203 ms: 1.20x faster                                  |
| xml_etree_iterparse  | 173 ms                                               | 152 ms: 1.14x faster                                  |
| pickle_dict          | 45.5 us                                              | 40.4 us: 1.13x faster                                 |
| pickle               | 15.9 us                                              | 14.4 us: 1.10x faster                                 |
| pickle_list          | 7.01 us                                              | 6.56 us: 1.07x faster                                 |
| unpickle_list        | 6.83 us                                              | 7.37 us: 1.08x slower                                 |
| xml_etree_generate   | 138 ms                                               | 160 ms: 1.16x slower                                  |
| json_loads           | 35.9 us                                              | 41.9 us: 1.17x slower                                 |
| json_dumps           | 14.0 ms                                              | 18.2 ms: 1.30x slower                                 |
| xml_etree_process    | 82.7 ms                                              | 119 ms: 1.44x slower                                  |
| tomli_loads          | 2.86 sec                                             | 4.17 sec: 1.46x slower                                |
| unpickle_pure_python | 304 us                                               | 526 us: 1.73x slower                                  |
| pickle_pure_python   | 436 us                                               | 792 us: 1.82x slower                                  |
| Geometric mean       | (ref)                                                | 1.15x slower                                          |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|------------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 16.2 ms                                              | 18.6 ms: 1.15x slower                                 |
| python_startup         | 22.7 ms                                              | 27.3 ms: 1.20x slower                                 |
| Geometric mean         | (ref)                                                | 1.17x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|-----------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| genshi_xml      | 69.1 ms                                              | 117 ms: 1.69x slower                                  |
| django_template | 45.4 ms                                              | 80.7 ms: 1.78x slower                                 |
| genshi_text     | 30.3 ms                                              | 54.8 ms: 1.81x slower                                 |
| mako            | 16.1 ms                                              | 29.7 ms: 1.84x slower                                 |
| Geometric mean  | (ref)                                                | 1.78x slower                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| bench_mp_pool              | 21.2 ms                                              | 12.0 ms: 1.77x faster                                 |
| async_tree_io_tg           | 1.87 sec                                             | 1.15 sec: 1.62x faster                                |
| gc_traversal               | 6.42 ms                                              | 4.22 ms: 1.52x faster                                 |
| async_tree_none_tg         | 726 ms                                               | 479 ms: 1.52x faster                                  |
| async_tree_io              | 1.86 sec                                             | 1.25 sec: 1.49x faster                                |
| async_tree_memoization_tg  | 912 ms                                               | 632 ms: 1.44x faster                                  |
| async_tree_none            | 820 ms                                               | 578 ms: 1.42x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.12 sec                                             | 806 ms: 1.39x faster                                  |
| async_tree_memoization     | 975 ms                                               | 728 ms: 1.34x faster                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                             | 926 ms: 1.23x faster                                  |
| xml_etree_parse            | 244 ms                                               | 203 ms: 1.20x faster                                  |
| xml_etree_iterparse        | 173 ms                                               | 152 ms: 1.14x faster                                  |
| create_gc_cycles           | 2.00 ms                                              | 1.77 ms: 1.13x faster                                 |
| pickle_dict                | 45.5 us                                              | 40.4 us: 1.13x faster                                 |
| pickle                     | 15.9 us                                              | 14.4 us: 1.10x faster                                 |
| regex_effbot               | 5.02 ms                                              | 4.60 ms: 1.09x faster                                 |
| pickle_list                | 7.01 us                                              | 6.56 us: 1.07x faster                                 |
| pidigits                   | 256 ms                                               | 241 ms: 1.06x faster                                  |
| asyncio_websockets         | 752 ms                                               | 714 ms: 1.05x faster                                  |
| asyncio_tcp                | 988 ms                                               | 1.05 sec: 1.06x slower                                |
| regex_dna                  | 268 ms                                               | 285 ms: 1.06x slower                                  |
| unpickle_list              | 6.83 us                                              | 7.37 us: 1.08x slower                                 |
| bench_thread_pool          | 3.42 ms                                              | 3.73 ms: 1.09x slower                                 |
| asyncio_tcp_ssl            | 2.82 sec                                             | 3.12 sec: 1.11x slower                                |
| json                       | 7.14 ms                                              | 8.04 ms: 1.13x slower                                 |
| sqlite_synth               | 3.77 us                                              | 4.31 us: 1.14x slower                                 |
| python_startup_no_site     | 16.2 ms                                              | 18.6 ms: 1.15x slower                                 |
| pylint                     | 480 ms                                               | 554 ms: 1.15x slower                                  |
| docutils                   | 4.05 sec                                             | 4.69 sec: 1.16x slower                                |
| xml_etree_generate         | 138 ms                                               | 160 ms: 1.16x slower                                  |
| json_loads                 | 35.9 us                                              | 41.9 us: 1.17x slower                                 |
| generators                 | 44.7 ms                                              | 52.7 ms: 1.18x slower                                 |
| regex_v8                   | 29.9 ms                                              | 35.5 ms: 1.18x slower                                 |
| python_startup             | 22.7 ms                                              | 27.3 ms: 1.20x slower                                 |
| async_generators           | 615 ms                                               | 739 ms: 1.20x slower                                  |
| tornado_http               | 261 ms                                               | 320 ms: 1.23x slower                                  |
| deepcopy                   | 486 us                                               | 608 us: 1.25x slower                                  |
| scimark_fft                | 481 ms                                               | 616 ms: 1.28x slower                                  |
| pycparser                  | 1.68 sec                                             | 2.15 sec: 1.28x slower                                |
| json_dumps                 | 14.0 ms                                              | 18.2 ms: 1.30x slower                                 |
| scimark_sparse_mat_mult    | 6.94 ms                                              | 9.03 ms: 1.30x slower                                 |
| dulwich_log                | 104 ms                                               | 135 ms: 1.30x slower                                  |
| nqueens                    | 116 ms                                               | 153 ms: 1.32x slower                                  |
| coroutines                 | 30.6 ms                                              | 40.7 ms: 1.33x slower                                 |
| meteor_contest             | 146 ms                                               | 196 ms: 1.34x slower                                  |
| mdp                        | 3.77 sec                                             | 5.07 sec: 1.35x slower                                |
| html5lib                   | 100 ms                                               | 135 ms: 1.35x slower                                  |
| deepcopy_memo              | 51.0 us                                              | 69.3 us: 1.36x slower                                 |
| crypto_pyaes               | 110 ms                                               | 150 ms: 1.37x slower                                  |
| telco                      | 9.53 ms                                              | 13.2 ms: 1.38x slower                                 |
| xml_etree_process          | 82.7 ms                                              | 119 ms: 1.44x slower                                  |
| deepcopy_reduce            | 4.18 us                                              | 6.01 us: 1.44x slower                                 |
| bpe_tokeniser              | 6.76 sec                                             | 9.73 sec: 1.44x slower                                |
| 2to3                       | 456 ms                                               | 661 ms: 1.45x slower                                  |
| tomli_loads                | 2.86 sec                                             | 4.17 sec: 1.46x slower                                |
| comprehensions             | 28.6 us                                              | 42.1 us: 1.47x slower                                 |
| sympy_integrate            | 29.0 ms                                              | 43.4 ms: 1.50x slower                                 |
| sqlglot_optimize           | 80.2 ms                                              | 121 ms: 1.50x slower                                  |
| typing_runtime_protocols   | 224 us                                               | 337 us: 1.50x slower                                  |
| fannkuch                   | 525 ms                                               | 794 ms: 1.51x slower                                  |
| coverage                   | 96.9 ms                                              | 149 ms: 1.54x slower                                  |
| regex_compile              | 186 ms                                               | 287 ms: 1.54x slower                                  |
| thrift                     | 1.10 ms                                              | 1.71 ms: 1.55x slower                                 |
| richards                   | 62.8 ms                                              | 99.0 ms: 1.58x slower                                 |
| float                      | 124 ms                                               | 199 ms: 1.60x slower                                  |
| logging_simple             | 9.68 us                                              | 15.5 us: 1.60x slower                                 |
| pyflate                    | 664 ms                                               | 1.08 sec: 1.63x slower                                |
| sqlglot_normalize          | 144 ms                                               | 235 ms: 1.63x slower                                  |
| genshi_xml                 | 69.1 ms                                              | 117 ms: 1.69x slower                                  |
| scimark_monte_carlo        | 96.8 ms                                              | 165 ms: 1.70x slower                                  |
| logging_silent             | 139 ns                                               | 240 ns: 1.72x slower                                  |
| unpickle_pure_python       | 304 us                                               | 526 us: 1.73x slower                                  |
| sympy_str                  | 379 ms                                               | 664 ms: 1.75x slower                                  |
| richards_super             | 69.7 ms                                              | 122 ms: 1.76x slower                                  |
| pprint_safe_repr           | 972 ms                                               | 1.71 sec: 1.76x slower                                |
| logging_format             | 9.56 us                                              | 16.8 us: 1.76x slower                                 |
| pprint_pformat             | 1.99 sec                                             | 3.50 sec: 1.76x slower                                |
| django_template            | 45.4 ms                                              | 80.7 ms: 1.78x slower                                 |
| chaos                      | 92.1 ms                                              | 165 ms: 1.79x slower                                  |
| spectral_norm              | 136 ms                                               | 245 ms: 1.79x slower                                  |
| genshi_text                | 30.3 ms                                              | 54.8 ms: 1.81x slower                                 |
| pickle_pure_python         | 436 us                                               | 792 us: 1.82x slower                                  |
| mako                       | 16.1 ms                                              | 29.7 ms: 1.84x slower                                 |
| sqlglot_transpile          | 2.32 ms                                              | 4.33 ms: 1.87x slower                                 |
| raytrace                   | 405 ms                                               | 784 ms: 1.94x slower                                  |
| scimark_sor                | 170 ms                                               | 337 ms: 1.98x slower                                  |
| hexiom                     | 8.19 ms                                              | 16.5 ms: 2.01x slower                                 |
| sqlglot_parse              | 1.85 ms                                              | 3.77 ms: 2.04x slower                                 |
| scimark_lu                 | 155 ms                                               | 326 ms: 2.10x slower                                  |
| sympy_sum                  | 218 ms                                               | 460 ms: 2.11x slower                                  |
| sympy_expand               | 591 ms                                               | 1.27 sec: 2.14x slower                                |
| go                         | 173 ms                                               | 395 ms: 2.28x slower                                  |
| deltablue                  | 4.45 ms                                              | 10.8 ms: 2.43x slower                                 |
| nbody                      | 117 ms                                               | 284 ms: 2.43x slower                                  |
| unpack_sequence            | 70.8 ns                                              | 191 ns: 2.69x slower                                  |
| Geometric mean             | (ref)                                                | 1.32x slower                                          |

Benchmark hidden because not significant (2): unpickle, pathlib
Ignored benchmarks (8) of results/bm-20240814-3.12.5+-9f153a2/bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.28x
- 95% likely to have a slowdown of 1.26x
- 99% likely to have a slowdown of 1.22x

# Memory
- memory change: 1.16x