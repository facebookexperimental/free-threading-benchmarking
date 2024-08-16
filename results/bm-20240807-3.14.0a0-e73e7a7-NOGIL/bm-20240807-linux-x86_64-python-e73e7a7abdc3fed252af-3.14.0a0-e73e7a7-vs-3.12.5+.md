# Results vs. 3.12.5+

- fork: python
- ref: e73e7a7abdc3fed252af
- machine: linux-x86_64
- commit hash: e73e7a7
- commit date: 2024-08-07
- overall geometric mean: 1.34x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.23x slower
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|----------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 456 ms                                               | 651 ms: 1.43x slower                                                  |
| docutils       | 4.05 sec                                             | 4.92 sec: 1.21x slower                                                |
| html5lib       | 100 ms                                               | 137 ms: 1.37x slower                                                  |
| tornado_http   | 261 ms                                               | 319 ms: 1.22x slower                                                  |
| Geometric mean | (ref)                                                | 1.30x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|----------------------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.87 sec                                             | 1.12 sec: 1.67x faster                                                |
| async_tree_none_tg         | 726 ms                                               | 489 ms: 1.48x faster                                                  |
| async_tree_io              | 1.86 sec                                             | 1.25 sec: 1.48x faster                                                |
| async_tree_memoization_tg  | 912 ms                                               | 619 ms: 1.47x faster                                                  |
| async_tree_none            | 820 ms                                               | 584 ms: 1.40x faster                                                  |
| async_tree_memoization     | 975 ms                                               | 724 ms: 1.35x faster                                                  |
| async_tree_cpu_io_mixed_tg | 1.12 sec                                             | 874 ms: 1.28x faster                                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                             | 951 ms: 1.20x faster                                                  |
| asyncio_tcp                | 988 ms                                               | 1.09 sec: 1.10x slower                                                |
| asyncio_tcp_ssl            | 2.82 sec                                             | 3.34 sec: 1.18x slower                                                |
| async_generators           | 615 ms                                               | 747 ms: 1.21x slower                                                  |
| coroutines                 | 30.6 ms                                              | 42.7 ms: 1.40x slower                                                 |
| Geometric mean             | (ref)                                                | 1.16x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|----------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 256 ms                                               | 239 ms: 1.07x faster                                                  |
| float          | 124 ms                                               | 194 ms: 1.56x slower                                                  |
| nbody          | 117 ms                                               | 281 ms: 2.41x slower                                                  |
| Geometric mean | (ref)                                                | 1.52x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|----------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 268 ms                                               | 290 ms: 1.08x slower                                                  |
| regex_v8       | 29.9 ms                                              | 35.6 ms: 1.19x slower                                                 |
| regex_compile  | 186 ms                                               | 296 ms: 1.59x slower                                                  |
| Geometric mean | (ref)                                                | 1.19x slower                                                          |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|----------------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_parse      | 244 ms                                               | 218 ms: 1.12x faster                                                  |
| pickle               | 15.9 us                                              | 14.5 us: 1.10x faster                                                 |
| pickle_dict          | 45.5 us                                              | 43.1 us: 1.06x faster                                                 |
| unpickle_list        | 6.83 us                                              | 7.70 us: 1.13x slower                                                 |
| json_loads           | 35.9 us                                              | 41.2 us: 1.15x slower                                                 |
| xml_etree_generate   | 138 ms                                               | 159 ms: 1.16x slower                                                  |
| json_dumps           | 14.0 ms                                              | 18.0 ms: 1.28x slower                                                 |
| tomli_loads          | 2.86 sec                                             | 4.14 sec: 1.45x slower                                                |
| xml_etree_process    | 82.7 ms                                              | 127 ms: 1.54x slower                                                  |
| unpickle_pure_python | 304 us                                               | 544 us: 1.79x slower                                                  |
| pickle_pure_python   | 436 us                                               | 846 us: 1.94x slower                                                  |
| Geometric mean       | (ref)                                                | 1.19x slower                                                          |

Benchmark hidden because not significant (3): xml_etree_iterparse, pickle_list, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|------------------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 16.2 ms                                              | 19.4 ms: 1.19x slower                                                 |
| python_startup         | 22.7 ms                                              | 28.9 ms: 1.27x slower                                                 |
| Geometric mean         | (ref)                                                | 1.23x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|-----------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 69.1 ms                                              | 111 ms: 1.61x slower                                                  |
| django_template | 45.4 ms                                              | 79.6 ms: 1.75x slower                                                 |
| genshi_text     | 30.3 ms                                              | 53.4 ms: 1.76x slower                                                 |
| mako            | 16.1 ms                                              | 31.0 ms: 1.92x slower                                                 |
| Geometric mean  | (ref)                                                | 1.76x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|----------------------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.87 sec                                             | 1.12 sec: 1.67x faster                                                |
| gc_traversal               | 6.42 ms                                              | 4.19 ms: 1.53x faster                                                 |
| async_tree_none_tg         | 726 ms                                               | 489 ms: 1.48x faster                                                  |
| async_tree_io              | 1.86 sec                                             | 1.25 sec: 1.48x faster                                                |
| async_tree_memoization_tg  | 912 ms                                               | 619 ms: 1.47x faster                                                  |
| async_tree_none            | 820 ms                                               | 584 ms: 1.40x faster                                                  |
| async_tree_memoization     | 975 ms                                               | 724 ms: 1.35x faster                                                  |
| async_tree_cpu_io_mixed_tg | 1.12 sec                                             | 874 ms: 1.28x faster                                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                             | 951 ms: 1.20x faster                                                  |
| bench_mp_pool              | 21.2 ms                                              | 18.8 ms: 1.13x faster                                                 |
| xml_etree_parse            | 244 ms                                               | 218 ms: 1.12x faster                                                  |
| create_gc_cycles           | 2.00 ms                                              | 1.80 ms: 1.11x faster                                                 |
| pickle                     | 15.9 us                                              | 14.5 us: 1.10x faster                                                 |
| pidigits                   | 256 ms                                               | 239 ms: 1.07x faster                                                  |
| pickle_dict                | 45.5 us                                              | 43.1 us: 1.06x faster                                                 |
| regex_dna                  | 268 ms                                               | 290 ms: 1.08x slower                                                  |
| asyncio_tcp                | 988 ms                                               | 1.09 sec: 1.10x slower                                                |
| unpickle_list              | 6.83 us                                              | 7.70 us: 1.13x slower                                                 |
| json                       | 7.14 ms                                              | 8.10 ms: 1.13x slower                                                 |
| json_loads                 | 35.9 us                                              | 41.2 us: 1.15x slower                                                 |
| deepcopy                   | 486 us                                               | 560 us: 1.15x slower                                                  |
| xml_etree_generate         | 138 ms                                               | 159 ms: 1.16x slower                                                  |
| sqlite_synth               | 3.77 us                                              | 4.42 us: 1.17x slower                                                 |
| asyncio_tcp_ssl            | 2.82 sec                                             | 3.34 sec: 1.18x slower                                                |
| regex_v8                   | 29.9 ms                                              | 35.6 ms: 1.19x slower                                                 |
| python_startup_no_site     | 16.2 ms                                              | 19.4 ms: 1.19x slower                                                 |
| pylint                     | 480 ms                                               | 579 ms: 1.21x slower                                                  |
| async_generators           | 615 ms                                               | 747 ms: 1.21x slower                                                  |
| docutils                   | 4.05 sec                                             | 4.92 sec: 1.21x slower                                                |
| tornado_http               | 261 ms                                               | 319 ms: 1.22x slower                                                  |
| generators                 | 44.7 ms                                              | 55.0 ms: 1.23x slower                                                 |
| python_startup             | 22.7 ms                                              | 28.9 ms: 1.27x slower                                                 |
| scimark_sparse_mat_mult    | 6.94 ms                                              | 8.91 ms: 1.28x slower                                                 |
| json_dumps                 | 14.0 ms                                              | 18.0 ms: 1.28x slower                                                 |
| scimark_fft                | 481 ms                                               | 624 ms: 1.30x slower                                                  |
| deepcopy_memo              | 51.0 us                                              | 67.1 us: 1.31x slower                                                 |
| meteor_contest             | 146 ms                                               | 192 ms: 1.32x slower                                                  |
| pycparser                  | 1.68 sec                                             | 2.21 sec: 1.32x slower                                                |
| bench_thread_pool          | 3.42 ms                                              | 4.52 ms: 1.32x slower                                                 |
| nqueens                    | 116 ms                                               | 155 ms: 1.34x slower                                                  |
| comprehensions             | 28.6 us                                              | 38.7 us: 1.35x slower                                                 |
| mdp                        | 3.77 sec                                             | 5.13 sec: 1.36x slower                                                |
| deepcopy_reduce            | 4.18 us                                              | 5.70 us: 1.37x slower                                                 |
| html5lib                   | 100 ms                                               | 137 ms: 1.37x slower                                                  |
| coroutines                 | 30.6 ms                                              | 42.7 ms: 1.40x slower                                                 |
| crypto_pyaes               | 110 ms                                               | 156 ms: 1.42x slower                                                  |
| 2to3                       | 456 ms                                               | 651 ms: 1.43x slower                                                  |
| tomli_loads                | 2.86 sec                                             | 4.14 sec: 1.45x slower                                                |
| fannkuch                   | 525 ms                                               | 762 ms: 1.45x slower                                                  |
| typing_runtime_protocols   | 224 us                                               | 327 us: 1.46x slower                                                  |
| telco                      | 9.53 ms                                              | 14.0 ms: 1.47x slower                                                 |
| bpe_tokeniser              | 6.76 sec                                             | 10.1 sec: 1.50x slower                                                |
| coverage                   | 96.9 ms                                              | 146 ms: 1.51x slower                                                  |
| sqlglot_optimize           | 80.2 ms                                              | 121 ms: 1.51x slower                                                  |
| thrift                     | 1.10 ms                                              | 1.67 ms: 1.52x slower                                                 |
| xml_etree_process          | 82.7 ms                                              | 127 ms: 1.54x slower                                                  |
| sympy_integrate            | 29.0 ms                                              | 44.9 ms: 1.55x slower                                                 |
| float                      | 124 ms                                               | 194 ms: 1.56x slower                                                  |
| richards                   | 62.8 ms                                              | 99.2 ms: 1.58x slower                                                 |
| logging_simple             | 9.68 us                                              | 15.4 us: 1.59x slower                                                 |
| regex_compile              | 186 ms                                               | 296 ms: 1.59x slower                                                  |
| sqlglot_normalize          | 144 ms                                               | 229 ms: 1.59x slower                                                  |
| pyflate                    | 664 ms                                               | 1.07 sec: 1.61x slower                                                |
| genshi_xml                 | 69.1 ms                                              | 111 ms: 1.61x slower                                                  |
| scimark_monte_carlo        | 96.8 ms                                              | 159 ms: 1.64x slower                                                  |
| pprint_safe_repr           | 972 ms                                               | 1.65 sec: 1.70x slower                                                |
| pprint_pformat             | 1.99 sec                                             | 3.39 sec: 1.71x slower                                                |
| logging_format             | 9.56 us                                              | 16.4 us: 1.71x slower                                                 |
| django_template            | 45.4 ms                                              | 79.6 ms: 1.75x slower                                                 |
| genshi_text                | 30.3 ms                                              | 53.4 ms: 1.76x slower                                                 |
| sympy_str                  | 379 ms                                               | 675 ms: 1.78x slower                                                  |
| logging_silent             | 139 ns                                               | 249 ns: 1.79x slower                                                  |
| unpickle_pure_python       | 304 us                                               | 544 us: 1.79x slower                                                  |
| spectral_norm              | 136 ms                                               | 247 ms: 1.81x slower                                                  |
| richards_super             | 69.7 ms                                              | 127 ms: 1.82x slower                                                  |
| chaos                      | 92.1 ms                                              | 170 ms: 1.84x slower                                                  |
| sqlglot_transpile          | 2.32 ms                                              | 4.32 ms: 1.86x slower                                                 |
| mako                       | 16.1 ms                                              | 31.0 ms: 1.92x slower                                                 |
| pickle_pure_python         | 436 us                                               | 846 us: 1.94x slower                                                  |
| raytrace                   | 405 ms                                               | 801 ms: 1.98x slower                                                  |
| hexiom                     | 8.19 ms                                              | 16.3 ms: 1.99x slower                                                 |
| scimark_sor                | 170 ms                                               | 340 ms: 2.00x slower                                                  |
| scimark_lu                 | 155 ms                                               | 313 ms: 2.02x slower                                                  |
| sqlglot_parse              | 1.85 ms                                              | 3.76 ms: 2.03x slower                                                 |
| sympy_sum                  | 218 ms                                               | 443 ms: 2.03x slower                                                  |
| sympy_expand               | 591 ms                                               | 1.29 sec: 2.17x slower                                                |
| nbody                      | 117 ms                                               | 281 ms: 2.41x slower                                                  |
| go                         | 173 ms                                               | 434 ms: 2.51x slower                                                  |
| deltablue                  | 4.45 ms                                              | 11.6 ms: 2.60x slower                                                 |
| unpack_sequence            | 70.8 ns                                              | 190 ns: 2.68x slower                                                  |
| Geometric mean             | (ref)                                                | 1.34x slower                                                          |

Benchmark hidden because not significant (6): regex_effbot, xml_etree_iterparse, pickle_list, asyncio_websockets, unpickle, pathlib
Ignored benchmarks (9) of results/bm-20240814-3.12.5+-9f153a2/bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.31x
- 95% likely to have a slowdown of 1.29x
- 99% likely to have a slowdown of 1.23x

# Memory
- memory change: 1.15x