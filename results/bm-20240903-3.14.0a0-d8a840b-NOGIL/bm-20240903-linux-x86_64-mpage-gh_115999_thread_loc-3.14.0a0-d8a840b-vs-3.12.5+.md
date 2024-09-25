# Results vs. 3.12.5+

- fork: mpage
- ref: gh_115999_thread_loc
- machine: linux-x86_64
- commit hash: d8a840b
- commit date: 2024-09-03
- overall geometric mean: 1.38x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.23x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b |
|----------------|:----------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 456 ms                                               | 698 ms: 1.53x slower                                                 |
| docutils       | 4.05 sec                                             | 4.84 sec: 1.19x slower                                               |
| html5lib       | 100 ms                                               | 142 ms: 1.42x slower                                                 |
| tornado_http   | 261 ms                                               | 399 ms: 1.53x slower                                                 |
| Geometric mean | (ref)                                                | 1.41x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b |
|----------------------------|:----------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 1.87 sec                                             | 1.15 sec: 1.62x faster                                               |
| async_tree_none_tg         | 726 ms                                               | 505 ms: 1.44x faster                                                 |
| async_tree_io              | 1.86 sec                                             | 1.30 sec: 1.43x faster                                               |
| async_tree_none            | 820 ms                                               | 581 ms: 1.41x faster                                                 |
| async_tree_memoization_tg  | 912 ms                                               | 676 ms: 1.35x faster                                                 |
| async_tree_memoization     | 975 ms                                               | 727 ms: 1.34x faster                                                 |
| async_tree_cpu_io_mixed_tg | 1.12 sec                                             | 851 ms: 1.32x faster                                                 |
| async_tree_cpu_io_mixed    | 1.14 sec                                             | 974 ms: 1.17x faster                                                 |
| asyncio_tcp                | 988 ms                                               | 1.12 sec: 1.13x slower                                               |
| async_generators           | 615 ms                                               | 712 ms: 1.16x slower                                                 |
| asyncio_tcp_ssl            | 2.82 sec                                             | 3.41 sec: 1.21x slower                                               |
| coroutines                 | 30.6 ms                                              | 41.6 ms: 1.36x slower                                                |
| Geometric mean             | (ref)                                                | 1.15x faster                                                         |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b |
|----------------|:----------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 124 ms                                               | 192 ms: 1.54x slower                                                 |
| nbody          | 117 ms                                               | 271 ms: 2.33x slower                                                 |
| Geometric mean | (ref)                                                | 1.51x slower                                                         |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b |
|----------------|:----------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 5.02 ms                                              | 4.57 ms: 1.10x faster                                                |
| regex_dna      | 268 ms                                               | 297 ms: 1.11x slower                                                 |
| regex_v8       | 29.9 ms                                              | 35.5 ms: 1.19x slower                                                |
| regex_compile  | 186 ms                                               | 312 ms: 1.68x slower                                                 |
| Geometric mean | (ref)                                                | 1.19x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b |
|----------------------|:----------------------------------------------------:|:--------------------------------------------------------------------:|
| pickle               | 15.9 us                                              | 13.8 us: 1.15x faster                                                |
| unpickle             | 21.6 us                                              | 22.9 us: 1.06x slower                                                |
| xml_etree_generate   | 138 ms                                               | 166 ms: 1.21x slower                                                 |
| unpickle_list        | 6.83 us                                              | 8.26 us: 1.21x slower                                                |
| json_loads           | 35.9 us                                              | 43.5 us: 1.21x slower                                                |
| json_dumps           | 14.0 ms                                              | 17.3 ms: 1.23x slower                                                |
| tomli_loads          | 2.86 sec                                             | 4.40 sec: 1.54x slower                                               |
| xml_etree_process    | 82.7 ms                                              | 131 ms: 1.59x slower                                                 |
| pickle_pure_python   | 436 us                                               | 812 us: 1.86x slower                                                 |
| unpickle_pure_python | 304 us                                               | 597 us: 1.96x slower                                                 |
| Geometric mean       | (ref)                                                | 1.23x slower                                                         |

Benchmark hidden because not significant (4): pickle_dict, xml_etree_parse, xml_etree_iterparse, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b |
|------------------------|:----------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 16.2 ms                                              | 21.7 ms: 1.34x slower                                                |
| python_startup         | 22.7 ms                                              | 35.2 ms: 1.55x slower                                                |
| Geometric mean         | (ref)                                                | 1.44x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b |
|-----------------|:----------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 69.1 ms                                              | 120 ms: 1.73x slower                                                 |
| django_template | 45.4 ms                                              | 82.3 ms: 1.81x slower                                                |
| genshi_text     | 30.3 ms                                              | 55.2 ms: 1.82x slower                                                |
| mako            | 16.1 ms                                              | 32.1 ms: 1.99x slower                                                |
| Geometric mean  | (ref)                                                | 1.83x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b |
|----------------------------|:----------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 1.87 sec                                             | 1.15 sec: 1.62x faster                                               |
| async_tree_none_tg         | 726 ms                                               | 505 ms: 1.44x faster                                                 |
| async_tree_io              | 1.86 sec                                             | 1.30 sec: 1.43x faster                                               |
| async_tree_none            | 820 ms                                               | 581 ms: 1.41x faster                                                 |
| async_tree_memoization_tg  | 912 ms                                               | 676 ms: 1.35x faster                                                 |
| async_tree_memoization     | 975 ms                                               | 727 ms: 1.34x faster                                                 |
| async_tree_cpu_io_mixed_tg | 1.12 sec                                             | 851 ms: 1.32x faster                                                 |
| gc_traversal               | 6.42 ms                                              | 5.05 ms: 1.27x faster                                                |
| async_tree_cpu_io_mixed    | 1.14 sec                                             | 974 ms: 1.17x faster                                                 |
| bench_mp_pool              | 21.2 ms                                              | 18.2 ms: 1.17x faster                                                |
| pickle                     | 15.9 us                                              | 13.8 us: 1.15x faster                                                |
| regex_effbot               | 5.02 ms                                              | 4.57 ms: 1.10x faster                                                |
| create_gc_cycles           | 2.00 ms                                              | 1.85 ms: 1.08x faster                                                |
| unpickle                   | 21.6 us                                              | 22.9 us: 1.06x slower                                                |
| regex_dna                  | 268 ms                                               | 297 ms: 1.11x slower                                                 |
| scimark_fft                | 481 ms                                               | 539 ms: 1.12x slower                                                 |
| asyncio_tcp                | 988 ms                                               | 1.12 sec: 1.13x slower                                               |
| pathlib                    | 31.6 ms                                              | 36.3 ms: 1.15x slower                                                |
| async_generators           | 615 ms                                               | 712 ms: 1.16x slower                                                 |
| deepcopy                   | 486 us                                               | 564 us: 1.16x slower                                                 |
| scimark_sparse_mat_mult    | 6.94 ms                                              | 8.22 ms: 1.18x slower                                                |
| regex_v8                   | 29.9 ms                                              | 35.5 ms: 1.19x slower                                                |
| docutils                   | 4.05 sec                                             | 4.84 sec: 1.19x slower                                               |
| generators                 | 44.7 ms                                              | 53.5 ms: 1.20x slower                                                |
| json                       | 7.14 ms                                              | 8.56 ms: 1.20x slower                                                |
| xml_etree_generate         | 138 ms                                               | 166 ms: 1.21x slower                                                 |
| asyncio_tcp_ssl            | 2.82 sec                                             | 3.41 sec: 1.21x slower                                               |
| unpickle_list              | 6.83 us                                              | 8.26 us: 1.21x slower                                                |
| json_loads                 | 35.9 us                                              | 43.5 us: 1.21x slower                                                |
| sqlite_synth               | 3.77 us                                              | 4.64 us: 1.23x slower                                                |
| json_dumps                 | 14.0 ms                                              | 17.3 ms: 1.23x slower                                                |
| pylint                     | 480 ms                                               | 609 ms: 1.27x slower                                                 |
| mdp                        | 3.77 sec                                             | 4.90 sec: 1.30x slower                                               |
| pycparser                  | 1.68 sec                                             | 2.20 sec: 1.31x slower                                               |
| bench_thread_pool          | 3.42 ms                                              | 4.51 ms: 1.32x slower                                                |
| meteor_contest             | 146 ms                                               | 195 ms: 1.33x slower                                                 |
| python_startup_no_site     | 16.2 ms                                              | 21.7 ms: 1.34x slower                                                |
| comprehensions             | 28.6 us                                              | 38.6 us: 1.35x slower                                                |
| coroutines                 | 30.6 ms                                              | 41.6 ms: 1.36x slower                                                |
| nqueens                    | 116 ms                                               | 160 ms: 1.39x slower                                                 |
| deepcopy_memo              | 51.0 us                                              | 72.1 us: 1.41x slower                                                |
| html5lib                   | 100 ms                                               | 142 ms: 1.42x slower                                                 |
| crypto_pyaes               | 110 ms                                               | 156 ms: 1.43x slower                                                 |
| fannkuch                   | 525 ms                                               | 761 ms: 1.45x slower                                                 |
| bpe_tokeniser              | 6.76 sec                                             | 9.87 sec: 1.46x slower                                               |
| telco                      | 9.53 ms                                              | 14.0 ms: 1.47x slower                                                |
| sqlglot_optimize           | 80.2 ms                                              | 119 ms: 1.49x slower                                                 |
| coverage                   | 96.9 ms                                              | 144 ms: 1.49x slower                                                 |
| deepcopy_reduce            | 4.18 us                                              | 6.24 us: 1.49x slower                                                |
| tornado_http               | 261 ms                                               | 399 ms: 1.53x slower                                                 |
| 2to3                       | 456 ms                                               | 698 ms: 1.53x slower                                                 |
| tomli_loads                | 2.86 sec                                             | 4.40 sec: 1.54x slower                                               |
| float                      | 124 ms                                               | 192 ms: 1.54x slower                                                 |
| python_startup             | 22.7 ms                                              | 35.2 ms: 1.55x slower                                                |
| pyflate                    | 664 ms                                               | 1.04 sec: 1.57x slower                                               |
| thrift                     | 1.10 ms                                              | 1.73 ms: 1.57x slower                                                |
| xml_etree_process          | 82.7 ms                                              | 131 ms: 1.59x slower                                                 |
| spectral_norm              | 136 ms                                               | 224 ms: 1.64x slower                                                 |
| scimark_monte_carlo        | 96.8 ms                                              | 160 ms: 1.66x slower                                                 |
| chaos                      | 92.1 ms                                              | 154 ms: 1.68x slower                                                 |
| regex_compile              | 186 ms                                               | 312 ms: 1.68x slower                                                 |
| richards                   | 62.8 ms                                              | 107 ms: 1.70x slower                                                 |
| typing_runtime_protocols   | 224 us                                               | 381 us: 1.70x slower                                                 |
| logging_simple             | 9.68 us                                              | 16.6 us: 1.72x slower                                                |
| genshi_xml                 | 69.1 ms                                              | 120 ms: 1.73x slower                                                 |
| sqlglot_normalize          | 144 ms                                               | 249 ms: 1.73x slower                                                 |
| pprint_pformat             | 1.99 sec                                             | 3.47 sec: 1.75x slower                                               |
| sympy_integrate            | 29.0 ms                                              | 51.4 ms: 1.78x slower                                                |
| django_template            | 45.4 ms                                              | 82.3 ms: 1.81x slower                                                |
| pprint_safe_repr           | 972 ms                                               | 1.77 sec: 1.82x slower                                               |
| genshi_text                | 30.3 ms                                              | 55.2 ms: 1.82x slower                                                |
| sympy_str                  | 379 ms                                               | 698 ms: 1.84x slower                                                 |
| pickle_pure_python         | 436 us                                               | 812 us: 1.86x slower                                                 |
| logging_silent             | 139 ns                                               | 262 ns: 1.88x slower                                                 |
| hexiom                     | 8.19 ms                                              | 15.8 ms: 1.93x slower                                                |
| scimark_sor                | 170 ms                                               | 331 ms: 1.94x slower                                                 |
| raytrace                   | 405 ms                                               | 788 ms: 1.95x slower                                                 |
| richards_super             | 69.7 ms                                              | 137 ms: 1.96x slower                                                 |
| unpickle_pure_python       | 304 us                                               | 597 us: 1.96x slower                                                 |
| mako                       | 16.1 ms                                              | 32.1 ms: 1.99x slower                                                |
| logging_format             | 9.56 us                                              | 19.1 us: 1.99x slower                                                |
| sqlglot_transpile          | 2.32 ms                                              | 4.66 ms: 2.01x slower                                                |
| scimark_lu                 | 155 ms                                               | 317 ms: 2.05x slower                                                 |
| go                         | 173 ms                                               | 370 ms: 2.14x slower                                                 |
| sqlglot_parse              | 1.85 ms                                              | 4.06 ms: 2.19x slower                                                |
| sympy_expand               | 591 ms                                               | 1.35 sec: 2.28x slower                                               |
| nbody                      | 117 ms                                               | 271 ms: 2.33x slower                                                 |
| sympy_sum                  | 218 ms                                               | 512 ms: 2.35x slower                                                 |
| deltablue                  | 4.45 ms                                              | 11.5 ms: 2.58x slower                                                |
| unpack_sequence            | 70.8 ns                                              | 191 ns: 2.70x slower                                                 |
| Geometric mean             | (ref)                                                | 1.38x slower                                                         |

Benchmark hidden because not significant (6): pidigits, pickle_dict, asyncio_websockets, xml_etree_parse, xml_etree_iterparse, pickle_list
Ignored benchmarks (9) of results/bm-20240814-3.12.5+-9f153a2/bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.30x
- 95% likely to have a slowdown of 1.28x
- 99% likely to have a slowdown of 1.23x

# Memory
- memory change: 1.18x