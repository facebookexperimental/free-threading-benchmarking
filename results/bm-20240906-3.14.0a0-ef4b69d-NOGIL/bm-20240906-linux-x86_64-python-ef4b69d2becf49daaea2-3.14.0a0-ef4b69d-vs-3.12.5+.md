# Results vs. 3.12.5+

- fork: python
- ref: ef4b69d2becf49daaea2
- machine: linux-x86_64
- commit hash: ef4b69d
- commit date: 2024-09-06
- overall geometric mean: 1.39x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.27x slower
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 456 ms                                               | 719 ms: 1.58x slower                                                  |
| docutils       | 4.05 sec                                             | 4.96 sec: 1.23x slower                                                |
| html5lib       | 100 ms                                               | 139 ms: 1.39x slower                                                  |
| tornado_http   | 261 ms                                               | 350 ms: 1.34x slower                                                  |
| Geometric mean | (ref)                                                | 1.38x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.87 sec                                             | 1.17 sec: 1.59x faster                                                |
| async_tree_none_tg         | 726 ms                                               | 514 ms: 1.41x faster                                                  |
| async_tree_io              | 1.86 sec                                             | 1.34 sec: 1.38x faster                                                |
| async_tree_memoization_tg  | 912 ms                                               | 660 ms: 1.38x faster                                                  |
| async_tree_none            | 820 ms                                               | 610 ms: 1.34x faster                                                  |
| async_tree_memoization     | 975 ms                                               | 747 ms: 1.31x faster                                                  |
| async_tree_cpu_io_mixed_tg | 1.12 sec                                             | 863 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                             | 952 ms: 1.20x faster                                                  |
| async_generators           | 615 ms                                               | 734 ms: 1.19x slower                                                  |
| asyncio_tcp                | 988 ms                                               | 1.22 sec: 1.23x slower                                                |
| asyncio_tcp_ssl            | 2.82 sec                                             | 3.56 sec: 1.26x slower                                                |
| coroutines                 | 30.6 ms                                              | 41.7 ms: 1.36x slower                                                 |
| Geometric mean             | (ref)                                                | 1.13x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 124 ms                                               | 204 ms: 1.64x slower                                                  |
| nbody          | 117 ms                                               | 300 ms: 2.58x slower                                                  |
| Geometric mean | (ref)                                                | 1.60x slower                                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 268 ms                                               | 294 ms: 1.10x slower                                                  |
| regex_v8       | 29.9 ms                                              | 37.7 ms: 1.26x slower                                                 |
| regex_compile  | 186 ms                                               | 284 ms: 1.52x slower                                                  |
| Geometric mean | (ref)                                                | 1.19x slower                                                          |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_parse      | 244 ms                                               | 215 ms: 1.13x faster                                                  |
| pickle_dict          | 45.5 us                                              | 40.9 us: 1.11x faster                                                 |
| unpickle_list        | 6.83 us                                              | 7.20 us: 1.05x slower                                                 |
| xml_etree_generate   | 138 ms                                               | 163 ms: 1.18x slower                                                  |
| json_loads           | 35.9 us                                              | 44.0 us: 1.23x slower                                                 |
| json_dumps           | 14.0 ms                                              | 18.1 ms: 1.29x slower                                                 |
| tomli_loads          | 2.86 sec                                             | 4.30 sec: 1.50x slower                                                |
| xml_etree_process    | 82.7 ms                                              | 128 ms: 1.55x slower                                                  |
| unpickle_pure_python | 304 us                                               | 550 us: 1.81x slower                                                  |
| pickle_pure_python   | 436 us                                               | 870 us: 1.99x slower                                                  |
| Geometric mean       | (ref)                                                | 1.19x slower                                                          |

Benchmark hidden because not significant (4): pickle_list, pickle, xml_etree_iterparse, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|------------------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 16.2 ms                                              | 21.5 ms: 1.33x slower                                                 |
| python_startup         | 22.7 ms                                              | 32.8 ms: 1.45x slower                                                 |
| Geometric mean         | (ref)                                                | 1.39x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|-----------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 30.3 ms                                              | 55.1 ms: 1.82x slower                                                 |
| mako            | 16.1 ms                                              | 30.1 ms: 1.86x slower                                                 |
| genshi_xml      | 69.1 ms                                              | 129 ms: 1.87x slower                                                  |
| django_template | 45.4 ms                                              | 85.9 ms: 1.89x slower                                                 |
| Geometric mean  | (ref)                                                | 1.86x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------------------|:----------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.87 sec                                             | 1.17 sec: 1.59x faster                                                |
| async_tree_none_tg         | 726 ms                                               | 514 ms: 1.41x faster                                                  |
| gc_traversal               | 6.42 ms                                              | 4.60 ms: 1.39x faster                                                 |
| async_tree_io              | 1.86 sec                                             | 1.34 sec: 1.38x faster                                                |
| async_tree_memoization_tg  | 912 ms                                               | 660 ms: 1.38x faster                                                  |
| async_tree_none            | 820 ms                                               | 610 ms: 1.34x faster                                                  |
| async_tree_memoization     | 975 ms                                               | 747 ms: 1.31x faster                                                  |
| async_tree_cpu_io_mixed_tg | 1.12 sec                                             | 863 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                             | 952 ms: 1.20x faster                                                  |
| xml_etree_parse            | 244 ms                                               | 215 ms: 1.13x faster                                                  |
| pickle_dict                | 45.5 us                                              | 40.9 us: 1.11x faster                                                 |
| unpickle_list              | 6.83 us                                              | 7.20 us: 1.05x slower                                                 |
| regex_dna                  | 268 ms                                               | 294 ms: 1.10x slower                                                  |
| json                       | 7.14 ms                                              | 8.10 ms: 1.13x slower                                                 |
| deepcopy                   | 486 us                                               | 568 us: 1.17x slower                                                  |
| pathlib                    | 31.6 ms                                              | 37.2 ms: 1.18x slower                                                 |
| xml_etree_generate         | 138 ms                                               | 163 ms: 1.18x slower                                                  |
| async_generators           | 615 ms                                               | 734 ms: 1.19x slower                                                  |
| sqlite_synth               | 3.77 us                                              | 4.60 us: 1.22x slower                                                 |
| generators                 | 44.7 ms                                              | 54.6 ms: 1.22x slower                                                 |
| docutils                   | 4.05 sec                                             | 4.96 sec: 1.23x slower                                                |
| json_loads                 | 35.9 us                                              | 44.0 us: 1.23x slower                                                 |
| asyncio_tcp                | 988 ms                                               | 1.22 sec: 1.23x slower                                                |
| regex_v8                   | 29.9 ms                                              | 37.7 ms: 1.26x slower                                                 |
| asyncio_tcp_ssl            | 2.82 sec                                             | 3.56 sec: 1.26x slower                                                |
| scimark_sparse_mat_mult    | 6.94 ms                                              | 8.80 ms: 1.27x slower                                                 |
| json_dumps                 | 14.0 ms                                              | 18.1 ms: 1.29x slower                                                 |
| pylint                     | 480 ms                                               | 625 ms: 1.30x slower                                                  |
| pycparser                  | 1.68 sec                                             | 2.18 sec: 1.30x slower                                                |
| comprehensions             | 28.6 us                                              | 37.3 us: 1.30x slower                                                 |
| deepcopy_memo              | 51.0 us                                              | 67.4 us: 1.32x slower                                                 |
| python_startup_no_site     | 16.2 ms                                              | 21.5 ms: 1.33x slower                                                 |
| tornado_http               | 261 ms                                               | 350 ms: 1.34x slower                                                  |
| scimark_fft                | 481 ms                                               | 652 ms: 1.36x slower                                                  |
| meteor_contest             | 146 ms                                               | 199 ms: 1.36x slower                                                  |
| coroutines                 | 30.6 ms                                              | 41.7 ms: 1.36x slower                                                 |
| mdp                        | 3.77 sec                                             | 5.18 sec: 1.37x slower                                                |
| html5lib                   | 100 ms                                               | 139 ms: 1.39x slower                                                  |
| crypto_pyaes               | 110 ms                                               | 156 ms: 1.42x slower                                                  |
| deepcopy_reduce            | 4.18 us                                              | 5.97 us: 1.43x slower                                                 |
| python_startup             | 22.7 ms                                              | 32.8 ms: 1.45x slower                                                 |
| dulwich_log                | 104 ms                                               | 152 ms: 1.47x slower                                                  |
| tomli_loads                | 2.86 sec                                             | 4.30 sec: 1.50x slower                                                |
| nqueens                    | 116 ms                                               | 174 ms: 1.51x slower                                                  |
| bpe_tokeniser              | 6.76 sec                                             | 10.2 sec: 1.52x slower                                                |
| regex_compile              | 186 ms                                               | 284 ms: 1.52x slower                                                  |
| telco                      | 9.53 ms                                              | 14.7 ms: 1.54x slower                                                 |
| thrift                     | 1.10 ms                                              | 1.70 ms: 1.54x slower                                                 |
| xml_etree_process          | 82.7 ms                                              | 128 ms: 1.55x slower                                                  |
| typing_runtime_protocols   | 224 us                                               | 353 us: 1.57x slower                                                  |
| 2to3                       | 456 ms                                               | 719 ms: 1.58x slower                                                  |
| fannkuch                   | 525 ms                                               | 831 ms: 1.58x slower                                                  |
| bench_thread_pool          | 3.42 ms                                              | 5.45 ms: 1.59x slower                                                 |
| coverage                   | 96.9 ms                                              | 157 ms: 1.62x slower                                                  |
| logging_format             | 9.56 us                                              | 15.5 us: 1.62x slower                                                 |
| sqlglot_optimize           | 80.2 ms                                              | 130 ms: 1.62x slower                                                  |
| pyflate                    | 664 ms                                               | 1.08 sec: 1.62x slower                                                |
| float                      | 124 ms                                               | 204 ms: 1.64x slower                                                  |
| scimark_monte_carlo        | 96.8 ms                                              | 160 ms: 1.65x slower                                                  |
| sympy_integrate            | 29.0 ms                                              | 48.3 ms: 1.67x slower                                                 |
| sqlglot_normalize          | 144 ms                                               | 240 ms: 1.67x slower                                                  |
| pprint_safe_repr           | 972 ms                                               | 1.68 sec: 1.73x slower                                                |
| pprint_pformat             | 1.99 sec                                             | 3.48 sec: 1.75x slower                                                |
| richards_super             | 69.7 ms                                              | 123 ms: 1.77x slower                                                  |
| unpickle_pure_python       | 304 us                                               | 550 us: 1.81x slower                                                  |
| genshi_text                | 30.3 ms                                              | 55.1 ms: 1.82x slower                                                 |
| spectral_norm              | 136 ms                                               | 249 ms: 1.82x slower                                                  |
| richards                   | 62.8 ms                                              | 114 ms: 1.82x slower                                                  |
| logging_simple             | 9.68 us                                              | 17.7 us: 1.83x slower                                                 |
| sympy_str                  | 379 ms                                               | 696 ms: 1.84x slower                                                  |
| raytrace                   | 405 ms                                               | 751 ms: 1.86x slower                                                  |
| logging_silent             | 139 ns                                               | 260 ns: 1.86x slower                                                  |
| mako                       | 16.1 ms                                              | 30.1 ms: 1.86x slower                                                 |
| genshi_xml                 | 69.1 ms                                              | 129 ms: 1.87x slower                                                  |
| django_template            | 45.4 ms                                              | 85.9 ms: 1.89x slower                                                 |
| sqlglot_transpile          | 2.32 ms                                              | 4.43 ms: 1.91x slower                                                 |
| chaos                      | 92.1 ms                                              | 176 ms: 1.91x slower                                                  |
| scimark_lu                 | 155 ms                                               | 305 ms: 1.97x slower                                                  |
| pickle_pure_python         | 436 us                                               | 870 us: 1.99x slower                                                  |
| scimark_sor                | 170 ms                                               | 340 ms: 2.00x slower                                                  |
| hexiom                     | 8.19 ms                                              | 16.4 ms: 2.00x slower                                                 |
| sqlglot_parse              | 1.85 ms                                              | 3.72 ms: 2.01x slower                                                 |
| go                         | 173 ms                                               | 361 ms: 2.08x slower                                                  |
| sympy_expand               | 591 ms                                               | 1.33 sec: 2.25x slower                                                |
| sympy_sum                  | 218 ms                                               | 492 ms: 2.26x slower                                                  |
| unpack_sequence            | 70.8 ns                                              | 180 ns: 2.54x slower                                                  |
| deltablue                  | 4.45 ms                                              | 11.3 ms: 2.55x slower                                                 |
| nbody                      | 117 ms                                               | 300 ms: 2.58x slower                                                  |
| Geometric mean             | (ref)                                                | 1.39x slower                                                          |

Benchmark hidden because not significant (9): pickle_list, pidigits, pickle, regex_effbot, xml_etree_iterparse, asyncio_websockets, unpickle, create_gc_cycles, bench_mp_pool
Ignored benchmarks (8) of results/bm-20240814-3.12.5+-9f153a2/bm-20240814-linux-x86_64-python-3.12-3.12.5+-9f153a2.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.34x
- 95% likely to have a slowdown of 1.32x
- 99% likely to have a slowdown of 1.27x

# Memory
- memory change: 1.15x