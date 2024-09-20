# Results vs. 3.12.5+

- fork: python
- ref: v3.13.0rc2
- machine: linux-x86_64
- commit hash: ec61006
- commit date: 2024-09-06
- overall geometric mean: 1.37x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.24x slower
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------|:----------------------------------------------------:|:------------------------------------------------------------:|
| 2to3           | 456 ms                                               | 648 ms: 1.42x slower                                         |
| chameleon      | 9.66 ms                                              | 18.1 ms: 1.87x slower                                        |
| docutils       | 4.05 sec                                             | 4.93 sec: 1.22x slower                                       |
| html5lib       | 100 ms                                               | 147 ms: 1.46x slower                                         |
| tornado_http   | 261 ms                                               | 356 ms: 1.36x slower                                         |
| Geometric mean | (ref)                                                | 1.45x slower                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------------------|:----------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_io_tg           | 1.87 sec                                             | 1.17 sec: 1.60x faster                                       |
| async_tree_io              | 1.86 sec                                             | 1.29 sec: 1.44x faster                                       |
| async_tree_memoization     | 975 ms                                               | 766 ms: 1.27x faster                                         |
| async_tree_none            | 820 ms                                               | 654 ms: 1.25x faster                                         |
| async_tree_memoization_tg  | 912 ms                                               | 729 ms: 1.25x faster                                         |
| async_tree_none_tg         | 726 ms                                               | 583 ms: 1.24x faster                                         |
| async_tree_cpu_io_mixed_tg | 1.12 sec                                             | 938 ms: 1.19x faster                                         |
| async_tree_cpu_io_mixed    | 1.14 sec                                             | 988 ms: 1.16x faster                                         |
| asyncio_websockets         | 752 ms                                               | 780 ms: 1.04x slower                                         |
| asyncio_tcp_ssl            | 2.82 sec                                             | 3.29 sec: 1.17x slower                                       |
| async_generators           | 615 ms                                               | 718 ms: 1.17x slower                                         |
| asyncio_tcp                | 988 ms                                               | 1.17 sec: 1.18x slower                                       |
| coroutines                 | 30.6 ms                                              | 42.2 ms: 1.38x slower                                        |
| Geometric mean             | (ref)                                                | 1.10x faster                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------|:----------------------------------------------------:|:------------------------------------------------------------:|
| float          | 124 ms                                               | 193 ms: 1.55x slower                                         |
| nbody          | 117 ms                                               | 267 ms: 2.29x slower                                         |
| Geometric mean | (ref)                                                | 1.51x slower                                                 |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------|:----------------------------------------------------:|:------------------------------------------------------------:|
| regex_dna      | 268 ms                                               | 312 ms: 1.16x slower                                         |
| regex_v8       | 29.9 ms                                              | 35.5 ms: 1.19x slower                                        |
| regex_compile  | 186 ms                                               | 271 ms: 1.46x slower                                         |
| Geometric mean | (ref)                                                | 1.20x slower                                                 |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------------|:----------------------------------------------------:|:------------------------------------------------------------:|
| xml_etree_parse      | 244 ms                                               | 200 ms: 1.22x faster                                         |
| pickle               | 15.9 us                                              | 14.4 us: 1.10x faster                                        |
| xml_etree_iterparse  | 173 ms                                               | 159 ms: 1.09x faster                                         |
| pickle_dict          | 45.5 us                                              | 43.3 us: 1.05x faster                                        |
| xml_etree_generate   | 138 ms                                               | 153 ms: 1.11x slower                                         |
| json_loads           | 35.9 us                                              | 42.7 us: 1.19x slower                                        |
| json_dumps           | 14.0 ms                                              | 18.0 ms: 1.28x slower                                        |
| tomli_loads          | 2.86 sec                                             | 4.19 sec: 1.46x slower                                       |
| xml_etree_process    | 82.7 ms                                              | 126 ms: 1.53x slower                                         |
| unpickle_pure_python | 304 us                                               | 515 us: 1.69x slower                                         |
| pickle_pure_python   | 436 us                                               | 872 us: 2.00x slower                                         |
| Geometric mean       | (ref)                                                | 1.16x slower                                                 |

Benchmark hidden because not significant (3): unpickle, pickle_list, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|------------------------|:----------------------------------------------------:|:------------------------------------------------------------:|
| python_startup_no_site | 16.2 ms                                              | 21.9 ms: 1.35x slower                                        |
| python_startup         | 22.7 ms                                              | 33.8 ms: 1.49x slower                                        |
| Geometric mean         | (ref)                                                | 1.42x slower                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|-----------------|:----------------------------------------------------:|:------------------------------------------------------------:|
| django_template | 45.4 ms                                              | 76.1 ms: 1.68x slower                                        |
| genshi_xml      | 69.1 ms                                              | 118 ms: 1.71x slower                                         |
| genshi_text     | 30.3 ms                                              | 54.3 ms: 1.79x slower                                        |
| mako            | 16.1 ms                                              | 29.9 ms: 1.85x slower                                        |
| Geometric mean  | (ref)                                                | 1.76x slower                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------------------|:----------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_io_tg           | 1.87 sec                                             | 1.17 sec: 1.60x faster                                       |
| bench_mp_pool              | 21.2 ms                                              | 13.3 ms: 1.59x faster                                        |
| gc_traversal               | 6.42 ms                                              | 4.47 ms: 1.44x faster                                        |
| async_tree_io              | 1.86 sec                                             | 1.29 sec: 1.44x faster                                       |
| async_tree_memoization     | 975 ms                                               | 766 ms: 1.27x faster                                         |
| async_tree_none            | 820 ms                                               | 654 ms: 1.25x faster                                         |
| async_tree_memoization_tg  | 912 ms                                               | 729 ms: 1.25x faster                                         |
| async_tree_none_tg         | 726 ms                                               | 583 ms: 1.24x faster                                         |
| xml_etree_parse            | 244 ms                                               | 200 ms: 1.22x faster                                         |
| async_tree_cpu_io_mixed_tg | 1.12 sec                                             | 938 ms: 1.19x faster                                         |
| async_tree_cpu_io_mixed    | 1.14 sec                                             | 988 ms: 1.16x faster                                         |
| pickle                     | 15.9 us                                              | 14.4 us: 1.10x faster                                        |
| xml_etree_iterparse        | 173 ms                                               | 159 ms: 1.09x faster                                         |
| pickle_dict                | 45.5 us                                              | 43.3 us: 1.05x faster                                        |
| asyncio_websockets         | 752 ms                                               | 780 ms: 1.04x slower                                         |
| xml_etree_generate         | 138 ms                                               | 153 ms: 1.11x slower                                         |
| json                       | 7.14 ms                                              | 7.98 ms: 1.12x slower                                        |
| bench_thread_pool          | 3.42 ms                                              | 3.85 ms: 1.12x slower                                        |
| sqlite_synth               | 3.77 us                                              | 4.31 us: 1.14x slower                                        |
| pathlib                    | 31.6 ms                                              | 36.1 ms: 1.14x slower                                        |
| regex_dna                  | 268 ms                                               | 312 ms: 1.16x slower                                         |
| asyncio_tcp_ssl            | 2.82 sec                                             | 3.29 sec: 1.17x slower                                       |
| async_generators           | 615 ms                                               | 718 ms: 1.17x slower                                         |
| asyncio_tcp                | 988 ms                                               | 1.17 sec: 1.18x slower                                       |
| regex_v8                   | 29.9 ms                                              | 35.5 ms: 1.19x slower                                        |
| json_loads                 | 35.9 us                                              | 42.7 us: 1.19x slower                                        |
| pylint                     | 480 ms                                               | 576 ms: 1.20x slower                                         |
| generators                 | 44.7 ms                                              | 54.0 ms: 1.21x slower                                        |
| scimark_sparse_mat_mult    | 6.94 ms                                              | 8.40 ms: 1.21x slower                                        |
| docutils                   | 4.05 sec                                             | 4.93 sec: 1.22x slower                                       |
| dulwich_log                | 104 ms                                               | 128 ms: 1.23x slower                                         |
| scimark_fft                | 481 ms                                               | 604 ms: 1.26x slower                                         |
| pycparser                  | 1.68 sec                                             | 2.13 sec: 1.27x slower                                       |
| json_dumps                 | 14.0 ms                                              | 18.0 ms: 1.28x slower                                        |
| comprehensions             | 28.6 us                                              | 36.9 us: 1.29x slower                                        |
| crypto_pyaes               | 110 ms                                               | 142 ms: 1.29x slower                                         |
| mdp                        | 3.77 sec                                             | 4.87 sec: 1.29x slower                                       |
| nqueens                    | 116 ms                                               | 151 ms: 1.31x slower                                         |
| gunicorn                   | 1.92 ms                                              | 2.53 ms: 1.32x slower                                        |
| python_startup_no_site     | 16.2 ms                                              | 21.9 ms: 1.35x slower                                        |
| meteor_contest             | 146 ms                                               | 198 ms: 1.36x slower                                         |
| tornado_http               | 261 ms                                               | 356 ms: 1.36x slower                                         |
| coroutines                 | 30.6 ms                                              | 42.2 ms: 1.38x slower                                        |
| fannkuch                   | 525 ms                                               | 738 ms: 1.41x slower                                         |
| 2to3                       | 456 ms                                               | 648 ms: 1.42x slower                                         |
| aiohttp                    | 2.05 ms                                              | 2.97 ms: 1.45x slower                                        |
| regex_compile              | 186 ms                                               | 271 ms: 1.46x slower                                         |
| tomli_loads                | 2.86 sec                                             | 4.19 sec: 1.46x slower                                       |
| html5lib                   | 100 ms                                               | 147 ms: 1.46x slower                                         |
| typing_runtime_protocols   | 224 us                                               | 329 us: 1.47x slower                                         |
| bpe_tokeniser              | 6.76 sec                                             | 9.94 sec: 1.47x slower                                       |
| python_startup             | 22.7 ms                                              | 33.8 ms: 1.49x slower                                        |
| thrift                     | 1.10 ms                                              | 1.65 ms: 1.49x slower                                        |
| telco                      | 9.53 ms                                              | 14.3 ms: 1.50x slower                                        |
| sympy_integrate            | 29.0 ms                                              | 43.4 ms: 1.50x slower                                        |
| sqlglot_optimize           | 80.2 ms                                              | 122 ms: 1.52x slower                                         |
| coverage                   | 96.9 ms                                              | 148 ms: 1.53x slower                                         |
| xml_etree_process          | 82.7 ms                                              | 126 ms: 1.53x slower                                         |
| deepcopy                   | 486 us                                               | 744 us: 1.53x slower                                         |
| float                      | 124 ms                                               | 193 ms: 1.55x slower                                         |
| pyflate                    | 664 ms                                               | 1.03 sec: 1.55x slower                                       |
| sqlglot_normalize          | 144 ms                                               | 225 ms: 1.57x slower                                         |
| deepcopy_memo              | 51.0 us                                              | 84.2 us: 1.65x slower                                        |
| logging_simple             | 9.68 us                                              | 16.1 us: 1.66x slower                                        |
| django_template            | 45.4 ms                                              | 76.1 ms: 1.68x slower                                        |
| deepcopy_reduce            | 4.18 us                                              | 7.05 us: 1.69x slower                                        |
| spectral_norm              | 136 ms                                               | 231 ms: 1.69x slower                                         |
| unpickle_pure_python       | 304 us                                               | 515 us: 1.69x slower                                         |
| genshi_xml                 | 69.1 ms                                              | 118 ms: 1.71x slower                                         |
| richards                   | 62.8 ms                                              | 108 ms: 1.72x slower                                         |
| pprint_pformat             | 1.99 sec                                             | 3.42 sec: 1.72x slower                                       |
| scimark_monte_carlo        | 96.8 ms                                              | 167 ms: 1.73x slower                                         |
| sympy_str                  | 379 ms                                               | 664 ms: 1.75x slower                                         |
| pprint_safe_repr           | 972 ms                                               | 1.74 sec: 1.79x slower                                       |
| genshi_text                | 30.3 ms                                              | 54.3 ms: 1.79x slower                                        |
| chaos                      | 92.1 ms                                              | 168 ms: 1.82x slower                                         |
| raytrace                   | 405 ms                                               | 740 ms: 1.83x slower                                         |
| sqlglot_transpile          | 2.32 ms                                              | 4.25 ms: 1.83x slower                                        |
| logging_format             | 9.56 us                                              | 17.6 us: 1.84x slower                                        |
| mako                       | 16.1 ms                                              | 29.9 ms: 1.85x slower                                        |
| richards_super             | 69.7 ms                                              | 130 ms: 1.87x slower                                         |
| chameleon                  | 9.66 ms                                              | 18.1 ms: 1.87x slower                                        |
| logging_silent             | 139 ns                                               | 262 ns: 1.88x slower                                         |
| hexiom                     | 8.19 ms                                              | 16.3 ms: 1.99x slower                                        |
| pickle_pure_python         | 436 us                                               | 872 us: 2.00x slower                                         |
| scimark_lu                 | 155 ms                                               | 313 ms: 2.02x slower                                         |
| scimark_sor                | 170 ms                                               | 345 ms: 2.03x slower                                         |
| sqlglot_parse              | 1.85 ms                                              | 3.76 ms: 2.03x slower                                        |
| sympy_expand               | 591 ms                                               | 1.24 sec: 2.10x slower                                       |
| sympy_sum                  | 218 ms                                               | 466 ms: 2.14x slower                                         |
| nbody                      | 117 ms                                               | 267 ms: 2.29x slower                                         |
| go                         | 173 ms                                               | 401 ms: 2.32x slower                                         |
| deltablue                  | 4.45 ms                                              | 10.7 ms: 2.40x slower                                        |
| flaskblogging              | 6.97 ms                                              | 17.1 ms: 2.46x slower                                        |
| unpack_sequence            | 70.8 ns                                              | 193 ns: 2.72x slower                                         |
| Geometric mean             | (ref)                                                | 1.37x slower                                                 |

Benchmark hidden because not significant (6): create_gc_cycles, pidigits, unpickle, pickle_list, unpickle_list, regex_effbot
Ignored benchmarks (4) of results/bm-20240814-3.12.5+-9f153a2/bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2.json: dask, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.30x
- 95% likely to have a slowdown of 1.28x
- 99% likely to have a slowdown of 1.24x

# Memory
- memory change: 1.15x