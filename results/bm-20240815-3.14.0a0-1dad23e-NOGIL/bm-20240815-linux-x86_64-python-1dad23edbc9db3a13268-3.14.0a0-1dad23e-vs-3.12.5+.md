# Results vs. 3.12.5+

- fork: python
- ref: 1dad23edbc9db3a13268
- machine: linux-x86_64
- commit hash: 1dad23e
- commit date: 2024-08-15
- overall geometric mean: 1.40x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.30x slower
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e |
|----------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 456 ms                                               | 687 ms: 1.51x slower                                                  |
| docutils       | 4.05 sec                                             | 5.35 sec: 1.32x slower                                                |
| html5lib       | 100 ms                                               | 147 ms: 1.47x slower                                                  |
| tornado_http   | 261 ms                                               | 350 ms: 1.34x slower                                                  |
| Geometric mean | (ref)                                                | 1.41x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e |
|----------------------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.87 sec                                             | 1.14 sec: 1.64x faster                                                |
| async_tree_none_tg         | 726 ms                                               | 490 ms: 1.48x faster                                                  |
| async_tree_io              | 1.86 sec                                             | 1.28 sec: 1.46x faster                                                |
| async_tree_memoization_tg  | 912 ms                                               | 672 ms: 1.36x faster                                                  |
| async_tree_cpu_io_mixed_tg | 1.12 sec                                             | 836 ms: 1.34x faster                                                  |
| async_tree_none            | 820 ms                                               | 626 ms: 1.31x faster                                                  |
| async_tree_memoization     | 975 ms                                               | 774 ms: 1.26x faster                                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                             | 926 ms: 1.23x faster                                                  |
| asyncio_tcp                | 988 ms                                               | 1.16 sec: 1.17x slower                                                |
| async_generators           | 615 ms                                               | 731 ms: 1.19x slower                                                  |
| asyncio_tcp_ssl            | 2.82 sec                                             | 3.47 sec: 1.23x slower                                                |
| coroutines                 | 30.6 ms                                              | 42.9 ms: 1.40x slower                                                 |
| Geometric mean             | (ref)                                                | 1.14x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e |
|----------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 124 ms                                               | 195 ms: 1.57x slower                                                  |
| nbody          | 117 ms                                               | 307 ms: 2.63x slower                                                  |
| Geometric mean | (ref)                                                | 1.59x slower                                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e |
|----------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 268 ms                                               | 300 ms: 1.12x slower                                                  |
| regex_v8       | 29.9 ms                                              | 36.8 ms: 1.23x slower                                                 |
| regex_compile  | 186 ms                                               | 310 ms: 1.66x slower                                                  |
| Geometric mean | (ref)                                                | 1.23x slower                                                          |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e |
|----------------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle               | 15.9 us                                              | 13.8 us: 1.15x faster                                                 |
| pickle_dict          | 45.5 us                                              | 42.2 us: 1.08x faster                                                 |
| xml_etree_parse      | 244 ms                                               | 229 ms: 1.06x faster                                                  |
| unpickle             | 21.6 us                                              | 23.4 us: 1.08x slower                                                 |
| unpickle_list        | 6.83 us                                              | 7.89 us: 1.15x slower                                                 |
| xml_etree_generate   | 138 ms                                               | 167 ms: 1.21x slower                                                  |
| json_loads           | 35.9 us                                              | 44.8 us: 1.25x slower                                                 |
| json_dumps           | 14.0 ms                                              | 19.0 ms: 1.35x slower                                                 |
| tomli_loads          | 2.86 sec                                             | 4.23 sec: 1.48x slower                                                |
| xml_etree_process    | 82.7 ms                                              | 130 ms: 1.57x slower                                                  |
| pickle_pure_python   | 436 us                                               | 783 us: 1.79x slower                                                  |
| unpickle_pure_python | 304 us                                               | 578 us: 1.90x slower                                                  |
| Geometric mean       | (ref)                                                | 1.21x slower                                                          |

Benchmark hidden because not significant (2): pickle_list, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e |
|------------------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 16.2 ms                                              | 20.9 ms: 1.29x slower                                                 |
| python_startup         | 22.7 ms                                              | 30.8 ms: 1.36x slower                                                 |
| Geometric mean         | (ref)                                                | 1.33x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e |
|-----------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 69.1 ms                                              | 124 ms: 1.80x slower                                                  |
| genshi_text     | 30.3 ms                                              | 55.2 ms: 1.82x slower                                                 |
| django_template | 45.4 ms                                              | 87.7 ms: 1.93x slower                                                 |
| mako            | 16.1 ms                                              | 31.5 ms: 1.95x slower                                                 |
| Geometric mean  | (ref)                                                | 1.87x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e |
|----------------------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.87 sec                                             | 1.14 sec: 1.64x faster                                                |
| async_tree_none_tg         | 726 ms                                               | 490 ms: 1.48x faster                                                  |
| async_tree_io              | 1.86 sec                                             | 1.28 sec: 1.46x faster                                                |
| async_tree_memoization_tg  | 912 ms                                               | 672 ms: 1.36x faster                                                  |
| async_tree_cpu_io_mixed_tg | 1.12 sec                                             | 836 ms: 1.34x faster                                                  |
| async_tree_none            | 820 ms                                               | 626 ms: 1.31x faster                                                  |
| gc_traversal               | 6.42 ms                                              | 5.05 ms: 1.27x faster                                                 |
| async_tree_memoization     | 975 ms                                               | 774 ms: 1.26x faster                                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                             | 926 ms: 1.23x faster                                                  |
| bench_mp_pool              | 21.2 ms                                              | 18.5 ms: 1.15x faster                                                 |
| pickle                     | 15.9 us                                              | 13.8 us: 1.15x faster                                                 |
| pickle_dict                | 45.5 us                                              | 42.2 us: 1.08x faster                                                 |
| create_gc_cycles           | 2.00 ms                                              | 1.87 ms: 1.07x faster                                                 |
| xml_etree_parse            | 244 ms                                               | 229 ms: 1.06x faster                                                  |
| unpickle                   | 21.6 us                                              | 23.4 us: 1.08x slower                                                 |
| regex_dna                  | 268 ms                                               | 300 ms: 1.12x slower                                                  |
| sqlite_synth               | 3.77 us                                              | 4.29 us: 1.14x slower                                                 |
| unpickle_list              | 6.83 us                                              | 7.89 us: 1.15x slower                                                 |
| asyncio_tcp                | 988 ms                                               | 1.16 sec: 1.17x slower                                                |
| pathlib                    | 31.6 ms                                              | 37.4 ms: 1.18x slower                                                 |
| async_generators           | 615 ms                                               | 731 ms: 1.19x slower                                                  |
| json                       | 7.14 ms                                              | 8.59 ms: 1.20x slower                                                 |
| xml_etree_generate         | 138 ms                                               | 167 ms: 1.21x slower                                                  |
| regex_v8                   | 29.9 ms                                              | 36.8 ms: 1.23x slower                                                 |
| asyncio_tcp_ssl            | 2.82 sec                                             | 3.47 sec: 1.23x slower                                                |
| json_loads                 | 35.9 us                                              | 44.8 us: 1.25x slower                                                 |
| pylint                     | 480 ms                                               | 606 ms: 1.26x slower                                                  |
| deepcopy                   | 486 us                                               | 626 us: 1.29x slower                                                  |
| python_startup_no_site     | 16.2 ms                                              | 20.9 ms: 1.29x slower                                                 |
| generators                 | 44.7 ms                                              | 58.2 ms: 1.30x slower                                                 |
| docutils                   | 4.05 sec                                             | 5.35 sec: 1.32x slower                                                |
| pycparser                  | 1.68 sec                                             | 2.23 sec: 1.33x slower                                                |
| tornado_http               | 261 ms                                               | 350 ms: 1.34x slower                                                  |
| json_dumps                 | 14.0 ms                                              | 19.0 ms: 1.35x slower                                                 |
| python_startup             | 22.7 ms                                              | 30.8 ms: 1.36x slower                                                 |
| scimark_fft                | 481 ms                                               | 657 ms: 1.36x slower                                                  |
| scimark_sparse_mat_mult    | 6.94 ms                                              | 9.49 ms: 1.37x slower                                                 |
| comprehensions             | 28.6 us                                              | 39.2 us: 1.37x slower                                                 |
| meteor_contest             | 146 ms                                               | 202 ms: 1.38x slower                                                  |
| mdp                        | 3.77 sec                                             | 5.24 sec: 1.39x slower                                                |
| coroutines                 | 30.6 ms                                              | 42.9 ms: 1.40x slower                                                 |
| nqueens                    | 116 ms                                               | 164 ms: 1.42x slower                                                  |
| telco                      | 9.53 ms                                              | 13.7 ms: 1.44x slower                                                 |
| crypto_pyaes               | 110 ms                                               | 161 ms: 1.47x slower                                                  |
| html5lib                   | 100 ms                                               | 147 ms: 1.47x slower                                                  |
| tomli_loads                | 2.86 sec                                             | 4.23 sec: 1.48x slower                                                |
| 2to3                       | 456 ms                                               | 687 ms: 1.51x slower                                                  |
| thrift                     | 1.10 ms                                              | 1.66 ms: 1.51x slower                                                 |
| deepcopy_memo              | 51.0 us                                              | 77.4 us: 1.52x slower                                                 |
| sqlglot_optimize           | 80.2 ms                                              | 122 ms: 1.52x slower                                                  |
| typing_runtime_protocols   | 224 us                                               | 342 us: 1.53x slower                                                  |
| logging_simple             | 9.68 us                                              | 14.9 us: 1.54x slower                                                 |
| fannkuch                   | 525 ms                                               | 814 ms: 1.55x slower                                                  |
| bench_thread_pool          | 3.42 ms                                              | 5.33 ms: 1.56x slower                                                 |
| float                      | 124 ms                                               | 195 ms: 1.57x slower                                                  |
| sympy_integrate            | 29.0 ms                                              | 45.4 ms: 1.57x slower                                                 |
| xml_etree_process          | 82.7 ms                                              | 130 ms: 1.57x slower                                                  |
| bpe_tokeniser              | 6.76 sec                                             | 10.7 sec: 1.58x slower                                                |
| deepcopy_reduce            | 4.18 us                                              | 6.61 us: 1.58x slower                                                 |
| sqlglot_normalize          | 144 ms                                               | 235 ms: 1.63x slower                                                  |
| coverage                   | 96.9 ms                                              | 159 ms: 1.64x slower                                                  |
| regex_compile              | 186 ms                                               | 310 ms: 1.66x slower                                                  |
| scimark_monte_carlo        | 96.8 ms                                              | 161 ms: 1.66x slower                                                  |
| pyflate                    | 664 ms                                               | 1.12 sec: 1.69x slower                                                |
| richards                   | 62.8 ms                                              | 107 ms: 1.70x slower                                                  |
| pickle_pure_python         | 436 us                                               | 783 us: 1.79x slower                                                  |
| genshi_xml                 | 69.1 ms                                              | 124 ms: 1.80x slower                                                  |
| logging_format             | 9.56 us                                              | 17.3 us: 1.80x slower                                                 |
| spectral_norm              | 136 ms                                               | 247 ms: 1.81x slower                                                  |
| genshi_text                | 30.3 ms                                              | 55.2 ms: 1.82x slower                                                 |
| pprint_pformat             | 1.99 sec                                             | 3.62 sec: 1.82x slower                                                |
| sympy_str                  | 379 ms                                               | 697 ms: 1.84x slower                                                  |
| pprint_safe_repr           | 972 ms                                               | 1.80 sec: 1.85x slower                                                |
| unpickle_pure_python       | 304 us                                               | 578 us: 1.90x slower                                                  |
| logging_silent             | 139 ns                                               | 266 ns: 1.91x slower                                                  |
| richards_super             | 69.7 ms                                              | 133 ms: 1.92x slower                                                  |
| chaos                      | 92.1 ms                                              | 177 ms: 1.93x slower                                                  |
| django_template            | 45.4 ms                                              | 87.7 ms: 1.93x slower                                                 |
| raytrace                   | 405 ms                                               | 789 ms: 1.95x slower                                                  |
| mako                       | 16.1 ms                                              | 31.5 ms: 1.95x slower                                                 |
| sqlglot_transpile          | 2.32 ms                                              | 4.65 ms: 2.00x slower                                                 |
| sqlglot_parse              | 1.85 ms                                              | 3.77 ms: 2.03x slower                                                 |
| scimark_lu                 | 155 ms                                               | 319 ms: 2.06x slower                                                  |
| hexiom                     | 8.19 ms                                              | 16.9 ms: 2.07x slower                                                 |
| scimark_sor                | 170 ms                                               | 355 ms: 2.08x slower                                                  |
| sympy_sum                  | 218 ms                                               | 462 ms: 2.12x slower                                                  |
| sympy_expand               | 591 ms                                               | 1.26 sec: 2.13x slower                                                |
| go                         | 173 ms                                               | 440 ms: 2.54x slower                                                  |
| nbody                      | 117 ms                                               | 307 ms: 2.63x slower                                                  |
| deltablue                  | 4.45 ms                                              | 11.8 ms: 2.65x slower                                                 |
| unpack_sequence            | 70.8 ns                                              | 212 ns: 3.00x slower                                                  |
| Geometric mean             | (ref)                                                | 1.40x slower                                                          |

Benchmark hidden because not significant (5): pickle_list, pidigits, regex_effbot, xml_etree_iterparse, asyncio_websockets
Ignored benchmarks (9) of results/bm-20240814-3.12.5+-9f153a2/bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.35x
- 95% likely to have a slowdown of 1.33x
- 99% likely to have a slowdown of 1.30x

# Memory
- memory change: 1.16x