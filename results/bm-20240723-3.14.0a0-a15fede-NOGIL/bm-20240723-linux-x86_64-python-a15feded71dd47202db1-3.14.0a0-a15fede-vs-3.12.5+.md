# Results vs. 3.12.5+

- fork: python
- ref: a15feded71dd47202db1
- machine: linux-x86_64
- commit hash: a15fede
- commit date: 2024-07-23
- overall geometric mean: 1.37x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.27x slower
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede |
|----------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 456 ms                                               | 650 ms: 1.42x slower                                                  |
| docutils       | 4.05 sec                                             | 4.88 sec: 1.20x slower                                                |
| html5lib       | 100 ms                                               | 139 ms: 1.39x slower                                                  |
| tornado_http   | 261 ms                                               | 349 ms: 1.34x slower                                                  |
| Geometric mean | (ref)                                                | 1.34x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede |
|----------------------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.87 sec                                             | 1.16 sec: 1.60x faster                                                |
| async_tree_none_tg         | 726 ms                                               | 485 ms: 1.50x faster                                                  |
| async_tree_io              | 1.86 sec                                             | 1.30 sec: 1.43x faster                                                |
| async_tree_none            | 820 ms                                               | 588 ms: 1.39x faster                                                  |
| async_tree_cpu_io_mixed_tg | 1.12 sec                                             | 817 ms: 1.37x faster                                                  |
| async_tree_memoization_tg  | 912 ms                                               | 671 ms: 1.36x faster                                                  |
| async_tree_memoization     | 975 ms                                               | 721 ms: 1.35x faster                                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                             | 944 ms: 1.21x faster                                                  |
| asyncio_tcp                | 988 ms                                               | 1.12 sec: 1.13x slower                                                |
| asyncio_tcp_ssl            | 2.82 sec                                             | 3.36 sec: 1.19x slower                                                |
| async_generators           | 615 ms                                               | 739 ms: 1.20x slower                                                  |
| coroutines                 | 30.6 ms                                              | 43.2 ms: 1.41x slower                                                 |
| Geometric mean             | (ref)                                                | 1.15x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede |
|----------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 256 ms                                               | 243 ms: 1.06x faster                                                  |
| float          | 124 ms                                               | 202 ms: 1.62x slower                                                  |
| nbody          | 117 ms                                               | 288 ms: 2.47x slower                                                  |
| Geometric mean | (ref)                                                | 1.56x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede |
|----------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 5.02 ms                                              | 4.57 ms: 1.10x faster                                                 |
| regex_dna      | 268 ms                                               | 294 ms: 1.10x slower                                                  |
| regex_v8       | 29.9 ms                                              | 36.3 ms: 1.21x slower                                                 |
| regex_compile  | 186 ms                                               | 291 ms: 1.56x slower                                                  |
| Geometric mean | (ref)                                                | 1.17x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede |
|----------------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_list          | 7.01 us                                              | 6.30 us: 1.11x faster                                                 |
| pickle               | 15.9 us                                              | 14.5 us: 1.09x faster                                                 |
| pickle_dict          | 45.5 us                                              | 42.5 us: 1.07x faster                                                 |
| xml_etree_parse      | 244 ms                                               | 231 ms: 1.06x faster                                                  |
| xml_etree_generate   | 138 ms                                               | 162 ms: 1.18x slower                                                  |
| json_loads           | 35.9 us                                              | 42.7 us: 1.19x slower                                                 |
| unpickle_list        | 6.83 us                                              | 8.14 us: 1.19x slower                                                 |
| json_dumps           | 14.0 ms                                              | 19.0 ms: 1.36x slower                                                 |
| tomli_loads          | 2.86 sec                                             | 4.22 sec: 1.47x slower                                                |
| xml_etree_process    | 82.7 ms                                              | 127 ms: 1.53x slower                                                  |
| pickle_pure_python   | 436 us                                               | 805 us: 1.85x slower                                                  |
| unpickle_pure_python | 304 us                                               | 609 us: 2.01x slower                                                  |
| Geometric mean       | (ref)                                                | 1.21x slower                                                          |

Benchmark hidden because not significant (2): xml_etree_iterparse, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede |
|------------------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 16.2 ms                                              | 20.6 ms: 1.27x slower                                                 |
| python_startup         | 22.7 ms                                              | 29.7 ms: 1.31x slower                                                 |
| Geometric mean         | (ref)                                                | 1.29x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede |
|-----------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 69.1 ms                                              | 116 ms: 1.67x slower                                                  |
| django_template | 45.4 ms                                              | 80.4 ms: 1.77x slower                                                 |
| genshi_text     | 30.3 ms                                              | 54.9 ms: 1.81x slower                                                 |
| mako            | 16.1 ms                                              | 30.4 ms: 1.88x slower                                                 |
| Geometric mean  | (ref)                                                | 1.78x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede |
|----------------------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.87 sec                                             | 1.16 sec: 1.60x faster                                                |
| bench_mp_pool              | 21.2 ms                                              | 13.4 ms: 1.58x faster                                                 |
| async_tree_none_tg         | 726 ms                                               | 485 ms: 1.50x faster                                                  |
| async_tree_io              | 1.86 sec                                             | 1.30 sec: 1.43x faster                                                |
| async_tree_none            | 820 ms                                               | 588 ms: 1.39x faster                                                  |
| async_tree_cpu_io_mixed_tg | 1.12 sec                                             | 817 ms: 1.37x faster                                                  |
| async_tree_memoization_tg  | 912 ms                                               | 671 ms: 1.36x faster                                                  |
| async_tree_memoization     | 975 ms                                               | 721 ms: 1.35x faster                                                  |
| gc_traversal               | 6.42 ms                                              | 4.76 ms: 1.35x faster                                                 |
| async_tree_cpu_io_mixed    | 1.14 sec                                             | 944 ms: 1.21x faster                                                  |
| pickle_list                | 7.01 us                                              | 6.30 us: 1.11x faster                                                 |
| regex_effbot               | 5.02 ms                                              | 4.57 ms: 1.10x faster                                                 |
| pickle                     | 15.9 us                                              | 14.5 us: 1.09x faster                                                 |
| pickle_dict                | 45.5 us                                              | 42.5 us: 1.07x faster                                                 |
| xml_etree_parse            | 244 ms                                               | 231 ms: 1.06x faster                                                  |
| pidigits                   | 256 ms                                               | 243 ms: 1.06x faster                                                  |
| regex_dna                  | 268 ms                                               | 294 ms: 1.10x slower                                                  |
| pathlib                    | 31.6 ms                                              | 34.8 ms: 1.10x slower                                                 |
| json                       | 7.14 ms                                              | 7.98 ms: 1.12x slower                                                 |
| asyncio_tcp                | 988 ms                                               | 1.12 sec: 1.13x slower                                                |
| sqlite_synth               | 3.77 us                                              | 4.35 us: 1.15x slower                                                 |
| bench_thread_pool          | 3.42 ms                                              | 4.01 ms: 1.17x slower                                                 |
| xml_etree_generate         | 138 ms                                               | 162 ms: 1.18x slower                                                  |
| json_loads                 | 35.9 us                                              | 42.7 us: 1.19x slower                                                 |
| unpickle_list              | 6.83 us                                              | 8.14 us: 1.19x slower                                                 |
| asyncio_tcp_ssl            | 2.82 sec                                             | 3.36 sec: 1.19x slower                                                |
| async_generators           | 615 ms                                               | 739 ms: 1.20x slower                                                  |
| docutils                   | 4.05 sec                                             | 4.88 sec: 1.20x slower                                                |
| regex_v8                   | 29.9 ms                                              | 36.3 ms: 1.21x slower                                                 |
| deepcopy                   | 486 us                                               | 606 us: 1.25x slower                                                  |
| pylint                     | 480 ms                                               | 607 ms: 1.26x slower                                                  |
| python_startup_no_site     | 16.2 ms                                              | 20.6 ms: 1.27x slower                                                 |
| scimark_sparse_mat_mult    | 6.94 ms                                              | 8.89 ms: 1.28x slower                                                 |
| generators                 | 44.7 ms                                              | 58.0 ms: 1.30x slower                                                 |
| python_startup             | 22.7 ms                                              | 29.7 ms: 1.31x slower                                                 |
| scimark_fft                | 481 ms                                               | 633 ms: 1.32x slower                                                  |
| tornado_http               | 261 ms                                               | 349 ms: 1.34x slower                                                  |
| meteor_contest             | 146 ms                                               | 196 ms: 1.34x slower                                                  |
| json_dumps                 | 14.0 ms                                              | 19.0 ms: 1.36x slower                                                 |
| pycparser                  | 1.68 sec                                             | 2.28 sec: 1.36x slower                                                |
| nqueens                    | 116 ms                                               | 157 ms: 1.36x slower                                                  |
| mdp                        | 3.77 sec                                             | 5.14 sec: 1.36x slower                                                |
| comprehensions             | 28.6 us                                              | 39.2 us: 1.37x slower                                                 |
| telco                      | 9.53 ms                                              | 13.2 ms: 1.39x slower                                                 |
| html5lib                   | 100 ms                                               | 139 ms: 1.39x slower                                                  |
| dulwich_log                | 104 ms                                               | 146 ms: 1.41x slower                                                  |
| coroutines                 | 30.6 ms                                              | 43.2 ms: 1.41x slower                                                 |
| crypto_pyaes               | 110 ms                                               | 155 ms: 1.41x slower                                                  |
| 2to3                       | 456 ms                                               | 650 ms: 1.42x slower                                                  |
| deepcopy_memo              | 51.0 us                                              | 72.8 us: 1.43x slower                                                 |
| deepcopy_reduce            | 4.18 us                                              | 6.01 us: 1.44x slower                                                 |
| tomli_loads                | 2.86 sec                                             | 4.22 sec: 1.47x slower                                                |
| sympy_integrate            | 29.0 ms                                              | 43.3 ms: 1.49x slower                                                 |
| typing_runtime_protocols   | 224 us                                               | 339 us: 1.52x slower                                                  |
| xml_etree_process          | 82.7 ms                                              | 127 ms: 1.53x slower                                                  |
| bpe_tokeniser              | 6.76 sec                                             | 10.3 sec: 1.53x slower                                                |
| fannkuch                   | 525 ms                                               | 808 ms: 1.54x slower                                                  |
| coverage                   | 96.9 ms                                              | 150 ms: 1.54x slower                                                  |
| regex_compile              | 186 ms                                               | 291 ms: 1.56x slower                                                  |
| logging_simple             | 9.68 us                                              | 15.3 us: 1.58x slower                                                 |
| thrift                     | 1.10 ms                                              | 1.74 ms: 1.58x slower                                                 |
| sqlglot_optimize           | 80.2 ms                                              | 128 ms: 1.60x slower                                                  |
| float                      | 124 ms                                               | 202 ms: 1.62x slower                                                  |
| sqlglot_normalize          | 144 ms                                               | 238 ms: 1.65x slower                                                  |
| genshi_xml                 | 69.1 ms                                              | 116 ms: 1.67x slower                                                  |
| pyflate                    | 664 ms                                               | 1.13 sec: 1.70x slower                                                |
| pprint_safe_repr           | 972 ms                                               | 1.71 sec: 1.75x slower                                                |
| sympy_str                  | 379 ms                                               | 667 ms: 1.76x slower                                                  |
| django_template            | 45.4 ms                                              | 80.4 ms: 1.77x slower                                                 |
| scimark_monte_carlo        | 96.8 ms                                              | 171 ms: 1.77x slower                                                  |
| logging_silent             | 139 ns                                               | 251 ns: 1.80x slower                                                  |
| pprint_pformat             | 1.99 sec                                             | 3.58 sec: 1.80x slower                                                |
| spectral_norm              | 136 ms                                               | 246 ms: 1.80x slower                                                  |
| logging_format             | 9.56 us                                              | 17.3 us: 1.81x slower                                                 |
| genshi_text                | 30.3 ms                                              | 54.9 ms: 1.81x slower                                                 |
| richards                   | 62.8 ms                                              | 115 ms: 1.83x slower                                                  |
| pickle_pure_python         | 436 us                                               | 805 us: 1.85x slower                                                  |
| mako                       | 16.1 ms                                              | 30.4 ms: 1.88x slower                                                 |
| chaos                      | 92.1 ms                                              | 175 ms: 1.90x slower                                                  |
| richards_super             | 69.7 ms                                              | 136 ms: 1.95x slower                                                  |
| hexiom                     | 8.19 ms                                              | 16.2 ms: 1.97x slower                                                 |
| raytrace                   | 405 ms                                               | 802 ms: 1.98x slower                                                  |
| scimark_sor                | 170 ms                                               | 341 ms: 2.01x slower                                                  |
| unpickle_pure_python       | 304 us                                               | 609 us: 2.01x slower                                                  |
| sqlglot_transpile          | 2.32 ms                                              | 4.92 ms: 2.12x slower                                                 |
| sympy_expand               | 591 ms                                               | 1.25 sec: 2.12x slower                                                |
| sqlglot_parse              | 1.85 ms                                              | 3.96 ms: 2.14x slower                                                 |
| scimark_lu                 | 155 ms                                               | 332 ms: 2.14x slower                                                  |
| sympy_sum                  | 218 ms                                               | 477 ms: 2.19x slower                                                  |
| go                         | 173 ms                                               | 421 ms: 2.43x slower                                                  |
| nbody                      | 117 ms                                               | 288 ms: 2.47x slower                                                  |
| deltablue                  | 4.45 ms                                              | 11.7 ms: 2.62x slower                                                 |
| unpack_sequence            | 70.8 ns                                              | 210 ns: 2.96x slower                                                  |
| Geometric mean             | (ref)                                                | 1.37x slower                                                          |

Benchmark hidden because not significant (4): create_gc_cycles, xml_etree_iterparse, asyncio_websockets, unpickle
Ignored benchmarks (8) of results/bm-20240814-3.12.5+-9f153a2/bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.33x
- 95% likely to have a slowdown of 1.32x
- 99% likely to have a slowdown of 1.27x

# Memory
- memory change: 1.16x