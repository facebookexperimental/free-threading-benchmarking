# Results vs. 3.12.5+

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 5f68511
- commit date: 2024-08-13
- overall geometric mean: 1.39x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.28x slower
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511 |
|----------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 456 ms                                               | 661 ms: 1.45x slower                                  |
| docutils       | 4.05 sec                                             | 5.15 sec: 1.27x slower                                |
| html5lib       | 100 ms                                               | 145 ms: 1.44x slower                                  |
| tornado_http   | 261 ms                                               | 360 ms: 1.38x slower                                  |
| Geometric mean | (ref)                                                | 1.38x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511 |
|----------------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.87 sec                                             | 1.17 sec: 1.60x faster                                |
| async_tree_io              | 1.86 sec                                             | 1.30 sec: 1.43x faster                                |
| async_tree_none_tg         | 726 ms                                               | 521 ms: 1.39x faster                                  |
| async_tree_memoization_tg  | 912 ms                                               | 671 ms: 1.36x faster                                  |
| async_tree_none            | 820 ms                                               | 621 ms: 1.32x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.12 sec                                             | 849 ms: 1.32x faster                                  |
| async_tree_memoization     | 975 ms                                               | 787 ms: 1.24x faster                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                             | 945 ms: 1.21x faster                                  |
| asyncio_websockets         | 752 ms                                               | 788 ms: 1.05x slower                                  |
| asyncio_tcp                | 988 ms                                               | 1.17 sec: 1.18x slower                                |
| async_generators           | 615 ms                                               | 744 ms: 1.21x slower                                  |
| asyncio_tcp_ssl            | 2.82 sec                                             | 3.55 sec: 1.26x slower                                |
| coroutines                 | 30.6 ms                                              | 44.5 ms: 1.45x slower                                 |
| Geometric mean             | (ref)                                                | 1.11x faster                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511 |
|----------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| pidigits       | 256 ms                                               | 242 ms: 1.06x faster                                  |
| float          | 124 ms                                               | 206 ms: 1.66x slower                                  |
| nbody          | 117 ms                                               | 293 ms: 2.51x slower                                  |
| Geometric mean | (ref)                                                | 1.58x slower                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511 |
|----------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| regex_effbot   | 5.02 ms                                              | 4.62 ms: 1.09x faster                                 |
| regex_dna      | 268 ms                                               | 289 ms: 1.08x slower                                  |
| regex_v8       | 29.9 ms                                              | 36.7 ms: 1.23x slower                                 |
| regex_compile  | 186 ms                                               | 290 ms: 1.56x slower                                  |
| Geometric mean | (ref)                                                | 1.17x slower                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511 |
|----------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| pickle_list          | 7.01 us                                              | 6.17 us: 1.14x faster                                 |
| xml_etree_parse      | 244 ms                                               | 223 ms: 1.09x faster                                  |
| pickle               | 15.9 us                                              | 14.6 us: 1.08x faster                                 |
| xml_etree_generate   | 138 ms                                               | 159 ms: 1.15x slower                                  |
| json_loads           | 35.9 us                                              | 43.2 us: 1.20x slower                                 |
| unpickle_list        | 6.83 us                                              | 8.50 us: 1.24x slower                                 |
| json_dumps           | 14.0 ms                                              | 19.1 ms: 1.36x slower                                 |
| tomli_loads          | 2.86 sec                                             | 4.26 sec: 1.49x slower                                |
| xml_etree_process    | 82.7 ms                                              | 137 ms: 1.66x slower                                  |
| pickle_pure_python   | 436 us                                               | 803 us: 1.84x slower                                  |
| unpickle_pure_python | 304 us                                               | 619 us: 2.04x slower                                  |
| Geometric mean       | (ref)                                                | 1.22x slower                                          |

Benchmark hidden because not significant (3): xml_etree_iterparse, pickle_dict, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511 |
|------------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 16.2 ms                                              | 21.2 ms: 1.31x slower                                 |
| python_startup         | 22.7 ms                                              | 31.5 ms: 1.39x slower                                 |
| Geometric mean         | (ref)                                                | 1.35x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511 |
|-----------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| genshi_xml      | 69.1 ms                                              | 117 ms: 1.69x slower                                  |
| genshi_text     | 30.3 ms                                              | 55.9 ms: 1.84x slower                                 |
| django_template | 45.4 ms                                              | 85.9 ms: 1.89x slower                                 |
| mako            | 16.1 ms                                              | 32.0 ms: 1.98x slower                                 |
| Geometric mean  | (ref)                                                | 1.85x slower                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511 |
|----------------------------|:----------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.87 sec                                             | 1.17 sec: 1.60x faster                                |
| async_tree_io              | 1.86 sec                                             | 1.30 sec: 1.43x faster                                |
| async_tree_none_tg         | 726 ms                                               | 521 ms: 1.39x faster                                  |
| async_tree_memoization_tg  | 912 ms                                               | 671 ms: 1.36x faster                                  |
| async_tree_none            | 820 ms                                               | 621 ms: 1.32x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.12 sec                                             | 849 ms: 1.32x faster                                  |
| bench_mp_pool              | 21.2 ms                                              | 16.8 ms: 1.27x faster                                 |
| async_tree_memoization     | 975 ms                                               | 787 ms: 1.24x faster                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                             | 945 ms: 1.21x faster                                  |
| gc_traversal               | 6.42 ms                                              | 5.42 ms: 1.18x faster                                 |
| pickle_list                | 7.01 us                                              | 6.17 us: 1.14x faster                                 |
| xml_etree_parse            | 244 ms                                               | 223 ms: 1.09x faster                                  |
| regex_effbot               | 5.02 ms                                              | 4.62 ms: 1.09x faster                                 |
| pickle                     | 15.9 us                                              | 14.6 us: 1.08x faster                                 |
| pidigits                   | 256 ms                                               | 242 ms: 1.06x faster                                  |
| asyncio_websockets         | 752 ms                                               | 788 ms: 1.05x slower                                  |
| regex_dna                  | 268 ms                                               | 289 ms: 1.08x slower                                  |
| pathlib                    | 31.6 ms                                              | 34.5 ms: 1.09x slower                                 |
| xml_etree_generate         | 138 ms                                               | 159 ms: 1.15x slower                                  |
| sqlite_synth               | 3.77 us                                              | 4.38 us: 1.16x slower                                 |
| deepcopy                   | 486 us                                               | 571 us: 1.17x slower                                  |
| asyncio_tcp                | 988 ms                                               | 1.17 sec: 1.18x slower                                |
| json                       | 7.14 ms                                              | 8.55 ms: 1.20x slower                                 |
| json_loads                 | 35.9 us                                              | 43.2 us: 1.20x slower                                 |
| async_generators           | 615 ms                                               | 744 ms: 1.21x slower                                  |
| pylint                     | 480 ms                                               | 588 ms: 1.22x slower                                  |
| regex_v8                   | 29.9 ms                                              | 36.7 ms: 1.23x slower                                 |
| unpickle_list              | 6.83 us                                              | 8.50 us: 1.24x slower                                 |
| asyncio_tcp_ssl            | 2.82 sec                                             | 3.55 sec: 1.26x slower                                |
| docutils                   | 4.05 sec                                             | 5.15 sec: 1.27x slower                                |
| pycparser                  | 1.68 sec                                             | 2.18 sec: 1.30x slower                                |
| generators                 | 44.7 ms                                              | 58.3 ms: 1.30x slower                                 |
| scimark_fft                | 481 ms                                               | 628 ms: 1.30x slower                                  |
| python_startup_no_site     | 16.2 ms                                              | 21.2 ms: 1.31x slower                                 |
| json_dumps                 | 14.0 ms                                              | 19.1 ms: 1.36x slower                                 |
| tornado_http               | 261 ms                                               | 360 ms: 1.38x slower                                  |
| scimark_sparse_mat_mult    | 6.94 ms                                              | 9.62 ms: 1.39x slower                                 |
| python_startup             | 22.7 ms                                              | 31.5 ms: 1.39x slower                                 |
| mdp                        | 3.77 sec                                             | 5.24 sec: 1.39x slower                                |
| comprehensions             | 28.6 us                                              | 40.4 us: 1.41x slower                                 |
| bench_thread_pool          | 3.42 ms                                              | 4.83 ms: 1.41x slower                                 |
| deepcopy_memo              | 51.0 us                                              | 72.7 us: 1.43x slower                                 |
| crypto_pyaes               | 110 ms                                               | 157 ms: 1.43x slower                                  |
| meteor_contest             | 146 ms                                               | 210 ms: 1.43x slower                                  |
| html5lib                   | 100 ms                                               | 145 ms: 1.44x slower                                  |
| 2to3                       | 456 ms                                               | 661 ms: 1.45x slower                                  |
| coroutines                 | 30.6 ms                                              | 44.5 ms: 1.45x slower                                 |
| deepcopy_reduce            | 4.18 us                                              | 6.14 us: 1.47x slower                                 |
| nqueens                    | 116 ms                                               | 170 ms: 1.47x slower                                  |
| tomli_loads                | 2.86 sec                                             | 4.26 sec: 1.49x slower                                |
| coverage                   | 96.9 ms                                              | 146 ms: 1.50x slower                                  |
| fannkuch                   | 525 ms                                               | 804 ms: 1.53x slower                                  |
| sqlglot_optimize           | 80.2 ms                                              | 124 ms: 1.55x slower                                  |
| telco                      | 9.53 ms                                              | 14.8 ms: 1.55x slower                                 |
| regex_compile              | 186 ms                                               | 290 ms: 1.56x slower                                  |
| typing_runtime_protocols   | 224 us                                               | 350 us: 1.56x slower                                  |
| thrift                     | 1.10 ms                                              | 1.72 ms: 1.56x slower                                 |
| bpe_tokeniser              | 6.76 sec                                             | 10.6 sec: 1.56x slower                                |
| logging_simple             | 9.68 us                                              | 15.2 us: 1.57x slower                                 |
| sqlglot_normalize          | 144 ms                                               | 231 ms: 1.61x slower                                  |
| float                      | 124 ms                                               | 206 ms: 1.66x slower                                  |
| xml_etree_process          | 82.7 ms                                              | 137 ms: 1.66x slower                                  |
| genshi_xml                 | 69.1 ms                                              | 117 ms: 1.69x slower                                  |
| richards                   | 62.8 ms                                              | 106 ms: 1.69x slower                                  |
| pyflate                    | 664 ms                                               | 1.13 sec: 1.70x slower                                |
| pprint_safe_repr           | 972 ms                                               | 1.71 sec: 1.76x slower                                |
| pprint_pformat             | 1.99 sec                                             | 3.54 sec: 1.78x slower                                |
| sympy_integrate            | 29.0 ms                                              | 51.8 ms: 1.79x slower                                 |
| scimark_monte_carlo        | 96.8 ms                                              | 174 ms: 1.80x slower                                  |
| logging_format             | 9.56 us                                              | 17.5 us: 1.83x slower                                 |
| pickle_pure_python         | 436 us                                               | 803 us: 1.84x slower                                  |
| genshi_text                | 30.3 ms                                              | 55.9 ms: 1.84x slower                                 |
| sqlglot_transpile          | 2.32 ms                                              | 4.33 ms: 1.87x slower                                 |
| sympy_str                  | 379 ms                                               | 709 ms: 1.87x slower                                  |
| richards_super             | 69.7 ms                                              | 131 ms: 1.88x slower                                  |
| logging_silent             | 139 ns                                               | 262 ns: 1.88x slower                                  |
| spectral_norm              | 136 ms                                               | 258 ms: 1.89x slower                                  |
| django_template            | 45.4 ms                                              | 85.9 ms: 1.89x slower                                 |
| chaos                      | 92.1 ms                                              | 177 ms: 1.92x slower                                  |
| scimark_lu                 | 155 ms                                               | 305 ms: 1.97x slower                                  |
| mako                       | 16.1 ms                                              | 32.0 ms: 1.98x slower                                 |
| raytrace                   | 405 ms                                               | 804 ms: 1.99x slower                                  |
| unpickle_pure_python       | 304 us                                               | 619 us: 2.04x slower                                  |
| hexiom                     | 8.19 ms                                              | 16.8 ms: 2.05x slower                                 |
| sqlglot_parse              | 1.85 ms                                              | 3.84 ms: 2.07x slower                                 |
| scimark_sor                | 170 ms                                               | 368 ms: 2.16x slower                                  |
| sympy_sum                  | 218 ms                                               | 479 ms: 2.20x slower                                  |
| sympy_expand               | 591 ms                                               | 1.30 sec: 2.21x slower                                |
| nbody                      | 117 ms                                               | 293 ms: 2.51x slower                                  |
| unpack_sequence            | 70.8 ns                                              | 180 ns: 2.55x slower                                  |
| go                         | 173 ms                                               | 465 ms: 2.68x slower                                  |
| deltablue                  | 4.45 ms                                              | 12.0 ms: 2.70x slower                                 |
| Geometric mean             | (ref)                                                | 1.39x slower                                          |

Benchmark hidden because not significant (4): xml_etree_iterparse, pickle_dict, create_gc_cycles, unpickle
Ignored benchmarks (9) of results/bm-20240814-3.12.5+-9f153a2/bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.35x
- 95% likely to have a slowdown of 1.31x
- 99% likely to have a slowdown of 1.28x

# Memory
- memory change: 1.16x