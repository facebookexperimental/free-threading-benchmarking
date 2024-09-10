# Results vs. 3.12.5+

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 5a4fb7e
- commit date: 2024-09-06
- overall geometric mean: 1.41x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.32x slower
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240906-linux-x86_64-python-main-3.14.0a0-5a4fb7e |
|----------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 456 ms                                               | 682 ms: 1.50x slower                                  |
| docutils       | 4.05 sec                                             | 5.10 sec: 1.26x slower                                |
| html5lib       | 100 ms                                               | 147 ms: 1.47x slower                                  |
| tornado_http   | 261 ms                                               | 420 ms: 1.61x slower                                  |
| Geometric mean | (ref)                                                | 1.45x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240906-linux-x86_64-python-main-3.14.0a0-5a4fb7e |
|----------------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.87 sec                                             | 1.24 sec: 1.51x faster                                |
| async_tree_io              | 1.86 sec                                             | 1.32 sec: 1.40x faster                                |
| async_tree_memoization_tg  | 912 ms                                               | 674 ms: 1.35x faster                                  |
| async_tree_none            | 820 ms                                               | 607 ms: 1.35x faster                                  |
| async_tree_none_tg         | 726 ms                                               | 540 ms: 1.35x faster                                  |
| async_tree_memoization     | 975 ms                                               | 770 ms: 1.27x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.12 sec                                             | 885 ms: 1.26x faster                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                             | 937 ms: 1.22x faster                                  |
| asyncio_websockets         | 752 ms                                               | 818 ms: 1.09x slower                                  |
| async_generators           | 615 ms                                               | 723 ms: 1.18x slower                                  |
| asyncio_tcp                | 988 ms                                               | 1.22 sec: 1.23x slower                                |
| asyncio_tcp_ssl            | 2.82 sec                                             | 3.67 sec: 1.30x slower                                |
| coroutines                 | 30.6 ms                                              | 42.2 ms: 1.38x slower                                 |
| Geometric mean             | (ref)                                                | 1.10x faster                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240906-linux-x86_64-python-main-3.14.0a0-5a4fb7e |
|----------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| float          | 124 ms                                               | 203 ms: 1.63x slower                                  |
| nbody          | 117 ms                                               | 315 ms: 2.70x slower                                  |
| Geometric mean | (ref)                                                | 1.64x slower                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240906-linux-x86_64-python-main-3.14.0a0-5a4fb7e |
|----------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| regex_dna      | 268 ms                                               | 299 ms: 1.11x slower                                  |
| regex_v8       | 29.9 ms                                              | 37.6 ms: 1.26x slower                                 |
| regex_compile  | 186 ms                                               | 305 ms: 1.64x slower                                  |
| Geometric mean | (ref)                                                | 1.24x slower                                          |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240906-linux-x86_64-python-main-3.14.0a0-5a4fb7e |
|----------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| pickle               | 15.9 us                                              | 13.8 us: 1.15x faster                                 |
| pickle_list          | 7.01 us                                              | 6.51 us: 1.08x faster                                 |
| xml_etree_parse      | 244 ms                                               | 229 ms: 1.07x faster                                  |
| unpickle             | 21.6 us                                              | 23.1 us: 1.07x slower                                 |
| unpickle_list        | 6.83 us                                              | 7.45 us: 1.09x slower                                 |
| json_dumps           | 14.0 ms                                              | 18.0 ms: 1.29x slower                                 |
| xml_etree_generate   | 138 ms                                               | 179 ms: 1.30x slower                                  |
| json_loads           | 35.9 us                                              | 47.7 us: 1.33x slower                                 |
| tomli_loads          | 2.86 sec                                             | 4.37 sec: 1.53x slower                                |
| xml_etree_process    | 82.7 ms                                              | 136 ms: 1.64x slower                                  |
| pickle_pure_python   | 436 us                                               | 762 us: 1.75x slower                                  |
| unpickle_pure_python | 304 us                                               | 563 us: 1.85x slower                                  |
| Geometric mean       | (ref)                                                | 1.22x slower                                          |

Benchmark hidden because not significant (2): xml_etree_iterparse, pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240906-linux-x86_64-python-main-3.14.0a0-5a4fb7e |
|------------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 16.2 ms                                              | 24.3 ms: 1.50x slower                                 |
| python_startup         | 22.7 ms                                              | 37.1 ms: 1.63x slower                                 |
| Geometric mean         | (ref)                                                | 1.57x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240906-linux-x86_64-python-main-3.14.0a0-5a4fb7e |
|-----------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| django_template | 45.4 ms                                              | 83.6 ms: 1.84x slower                                 |
| genshi_text     | 30.3 ms                                              | 57.6 ms: 1.90x slower                                 |
| mako            | 16.1 ms                                              | 31.9 ms: 1.97x slower                                 |
| genshi_xml      | 69.1 ms                                              | 141 ms: 2.03x slower                                  |
| Geometric mean  | (ref)                                                | 1.94x slower                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240906-linux-x86_64-python-main-3.14.0a0-5a4fb7e |
|----------------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.87 sec                                             | 1.24 sec: 1.51x faster                                |
| async_tree_io              | 1.86 sec                                             | 1.32 sec: 1.40x faster                                |
| gc_traversal               | 6.42 ms                                              | 4.74 ms: 1.36x faster                                 |
| async_tree_memoization_tg  | 912 ms                                               | 674 ms: 1.35x faster                                  |
| async_tree_none            | 820 ms                                               | 607 ms: 1.35x faster                                  |
| async_tree_none_tg         | 726 ms                                               | 540 ms: 1.35x faster                                  |
| async_tree_memoization     | 975 ms                                               | 770 ms: 1.27x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.12 sec                                             | 885 ms: 1.26x faster                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                             | 937 ms: 1.22x faster                                  |
| pickle                     | 15.9 us                                              | 13.8 us: 1.15x faster                                 |
| bench_mp_pool              | 21.2 ms                                              | 19.4 ms: 1.09x faster                                 |
| pickle_list                | 7.01 us                                              | 6.51 us: 1.08x faster                                 |
| xml_etree_parse            | 244 ms                                               | 229 ms: 1.07x faster                                  |
| unpickle                   | 21.6 us                                              | 23.1 us: 1.07x slower                                 |
| asyncio_websockets         | 752 ms                                               | 818 ms: 1.09x slower                                  |
| unpickle_list              | 6.83 us                                              | 7.45 us: 1.09x slower                                 |
| regex_dna                  | 268 ms                                               | 299 ms: 1.11x slower                                  |
| sqlite_synth               | 3.77 us                                              | 4.25 us: 1.13x slower                                 |
| pathlib                    | 31.6 ms                                              | 36.2 ms: 1.15x slower                                 |
| async_generators           | 615 ms                                               | 723 ms: 1.18x slower                                  |
| asyncio_tcp                | 988 ms                                               | 1.22 sec: 1.23x slower                                |
| regex_v8                   | 29.9 ms                                              | 37.6 ms: 1.26x slower                                 |
| docutils                   | 4.05 sec                                             | 5.10 sec: 1.26x slower                                |
| json                       | 7.14 ms                                              | 9.01 ms: 1.26x slower                                 |
| generators                 | 44.7 ms                                              | 56.6 ms: 1.27x slower                                 |
| deepcopy                   | 486 us                                               | 617 us: 1.27x slower                                  |
| json_dumps                 | 14.0 ms                                              | 18.0 ms: 1.29x slower                                 |
| xml_etree_generate         | 138 ms                                               | 179 ms: 1.30x slower                                  |
| asyncio_tcp_ssl            | 2.82 sec                                             | 3.67 sec: 1.30x slower                                |
| scimark_sparse_mat_mult    | 6.94 ms                                              | 9.21 ms: 1.33x slower                                 |
| json_loads                 | 35.9 us                                              | 47.7 us: 1.33x slower                                 |
| pylint                     | 480 ms                                               | 641 ms: 1.33x slower                                  |
| meteor_contest             | 146 ms                                               | 196 ms: 1.34x slower                                  |
| mdp                        | 3.77 sec                                             | 5.07 sec: 1.34x slower                                |
| pycparser                  | 1.68 sec                                             | 2.29 sec: 1.37x slower                                |
| scimark_fft                | 481 ms                                               | 659 ms: 1.37x slower                                  |
| coroutines                 | 30.6 ms                                              | 42.2 ms: 1.38x slower                                 |
| dulwich_log                | 104 ms                                               | 143 ms: 1.38x slower                                  |
| deepcopy_reduce            | 4.18 us                                              | 5.81 us: 1.39x slower                                 |
| deepcopy_memo              | 51.0 us                                              | 71.0 us: 1.39x slower                                 |
| crypto_pyaes               | 110 ms                                               | 158 ms: 1.44x slower                                  |
| comprehensions             | 28.6 us                                              | 41.3 us: 1.44x slower                                 |
| nqueens                    | 116 ms                                               | 170 ms: 1.47x slower                                  |
| html5lib                   | 100 ms                                               | 147 ms: 1.47x slower                                  |
| coverage                   | 96.9 ms                                              | 144 ms: 1.49x slower                                  |
| 2to3                       | 456 ms                                               | 682 ms: 1.50x slower                                  |
| python_startup_no_site     | 16.2 ms                                              | 24.3 ms: 1.50x slower                                 |
| thrift                     | 1.10 ms                                              | 1.68 ms: 1.52x slower                                 |
| tomli_loads                | 2.86 sec                                             | 4.37 sec: 1.53x slower                                |
| fannkuch                   | 525 ms                                               | 807 ms: 1.54x slower                                  |
| sqlglot_optimize           | 80.2 ms                                              | 125 ms: 1.56x slower                                  |
| bench_thread_pool          | 3.42 ms                                              | 5.33 ms: 1.56x slower                                 |
| telco                      | 9.53 ms                                              | 14.9 ms: 1.56x slower                                 |
| bpe_tokeniser              | 6.76 sec                                             | 10.8 sec: 1.59x slower                                |
| typing_runtime_protocols   | 224 us                                               | 357 us: 1.59x slower                                  |
| tornado_http               | 261 ms                                               | 420 ms: 1.61x slower                                  |
| float                      | 124 ms                                               | 203 ms: 1.63x slower                                  |
| python_startup             | 22.7 ms                                              | 37.1 ms: 1.63x slower                                 |
| regex_compile              | 186 ms                                               | 305 ms: 1.64x slower                                  |
| xml_etree_process          | 82.7 ms                                              | 136 ms: 1.64x slower                                  |
| logging_simple             | 9.68 us                                              | 16.0 us: 1.65x slower                                 |
| pyflate                    | 664 ms                                               | 1.11 sec: 1.67x slower                                |
| richards                   | 62.8 ms                                              | 107 ms: 1.70x slower                                  |
| sympy_integrate            | 29.0 ms                                              | 49.3 ms: 1.70x slower                                 |
| pprint_safe_repr           | 972 ms                                               | 1.66 sec: 1.71x slower                                |
| sqlglot_normalize          | 144 ms                                               | 248 ms: 1.73x slower                                  |
| pickle_pure_python         | 436 us                                               | 762 us: 1.75x slower                                  |
| scimark_monte_carlo        | 96.8 ms                                              | 171 ms: 1.76x slower                                  |
| chaos                      | 92.1 ms                                              | 163 ms: 1.76x slower                                  |
| pprint_pformat             | 1.99 sec                                             | 3.55 sec: 1.79x slower                                |
| richards_super             | 69.7 ms                                              | 126 ms: 1.80x slower                                  |
| logging_format             | 9.56 us                                              | 17.5 us: 1.83x slower                                 |
| django_template            | 45.4 ms                                              | 83.6 ms: 1.84x slower                                 |
| unpickle_pure_python       | 304 us                                               | 563 us: 1.85x slower                                  |
| spectral_norm              | 136 ms                                               | 253 ms: 1.85x slower                                  |
| sympy_str                  | 379 ms                                               | 708 ms: 1.87x slower                                  |
| genshi_text                | 30.3 ms                                              | 57.6 ms: 1.90x slower                                 |
| logging_silent             | 139 ns                                               | 266 ns: 1.91x slower                                  |
| raytrace                   | 405 ms                                               | 798 ms: 1.97x slower                                  |
| mako                       | 16.1 ms                                              | 31.9 ms: 1.97x slower                                 |
| sqlglot_parse              | 1.85 ms                                              | 3.76 ms: 2.03x slower                                 |
| genshi_xml                 | 69.1 ms                                              | 141 ms: 2.03x slower                                  |
| sqlglot_transpile          | 2.32 ms                                              | 4.73 ms: 2.04x slower                                 |
| hexiom                     | 8.19 ms                                              | 17.1 ms: 2.09x slower                                 |
| scimark_lu                 | 155 ms                                               | 328 ms: 2.12x slower                                  |
| scimark_sor                | 170 ms                                               | 360 ms: 2.12x slower                                  |
| go                         | 173 ms                                               | 370 ms: 2.14x slower                                  |
| sympy_sum                  | 218 ms                                               | 472 ms: 2.16x slower                                  |
| sympy_expand               | 591 ms                                               | 1.32 sec: 2.23x slower                                |
| nbody                      | 117 ms                                               | 315 ms: 2.70x slower                                  |
| deltablue                  | 4.45 ms                                              | 12.2 ms: 2.73x slower                                 |
| unpack_sequence            | 70.8 ns                                              | 207 ns: 2.92x slower                                  |
| Geometric mean             | (ref)                                                | 1.41x slower                                          |

Benchmark hidden because not significant (5): xml_etree_iterparse, create_gc_cycles, pidigits, pickle_dict, regex_effbot
Ignored benchmarks (8) of results/bm-20240814-3.12.5+-9f153a2/bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.37x
- 95% likely to have a slowdown of 1.35x
- 99% likely to have a slowdown of 1.32x

# Memory
- memory change: 1.15x