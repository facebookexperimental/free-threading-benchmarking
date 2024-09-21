# Results vs. 3.12.6

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 4767a6e
- commit date: 2024-08-06
- overall geometric mean: 1.39x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.25x slower
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240806-linux-x86_64-python-main-3.14.0a0-4767a6e |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 456 ms                                                 | 666 ms: 1.46x slower                                  |
| docutils       | 4.00 sec                                               | 5.00 sec: 1.25x slower                                |
| html5lib       | 88.9 ms                                                | 162 ms: 1.82x slower                                  |
| tornado_http   | 266 ms                                                 | 337 ms: 1.27x slower                                  |
| Geometric mean | (ref)                                                  | 1.43x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240806-linux-x86_64-python-main-3.14.0a0-4767a6e |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.14 sec: 1.70x faster                                |
| async_tree_io              | 1.85 sec                                               | 1.24 sec: 1.49x faster                                |
| async_tree_memoization_tg  | 930 ms                                                 | 634 ms: 1.47x faster                                  |
| async_tree_none_tg         | 704 ms                                                 | 483 ms: 1.46x faster                                  |
| async_tree_memoization     | 977 ms                                                 | 744 ms: 1.31x faster                                  |
| async_tree_none            | 741 ms                                                 | 607 ms: 1.22x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 909 ms: 1.21x faster                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 961 ms: 1.12x faster                                  |
| asyncio_tcp_ssl            | 2.81 sec                                               | 3.33 sec: 1.18x slower                                |
| asyncio_tcp                | 923 ms                                                 | 1.11 sec: 1.20x slower                                |
| async_generators           | 589 ms                                                 | 740 ms: 1.26x slower                                  |
| coroutines                 | 29.5 ms                                                | 43.8 ms: 1.48x slower                                 |
| Geometric mean             | (ref)                                                  | 1.12x faster                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240806-linux-x86_64-python-main-3.14.0a0-4767a6e |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| pidigits       | 250 ms                                                 | 267 ms: 1.07x slower                                  |
| float          | 123 ms                                                 | 190 ms: 1.55x slower                                  |
| nbody          | 119 ms                                                 | 309 ms: 2.59x slower                                  |
| Geometric mean | (ref)                                                  | 1.62x slower                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240806-linux-x86_64-python-main-3.14.0a0-4767a6e |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| regex_dna      | 278 ms                                                 | 304 ms: 1.09x slower                                  |
| regex_v8       | 32.5 ms                                                | 36.9 ms: 1.14x slower                                 |
| regex_compile  | 187 ms                                                 | 288 ms: 1.54x slower                                  |
| Geometric mean | (ref)                                                  | 1.17x slower                                          |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240806-linux-x86_64-python-main-3.14.0a0-4767a6e |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| pickle_dict          | 52.7 us                                                | 42.8 us: 1.23x faster                                 |
| pickle               | 16.4 us                                                | 14.1 us: 1.16x faster                                 |
| xml_etree_parse      | 241 ms                                                 | 222 ms: 1.08x faster                                  |
| pickle_list          | 6.97 us                                                | 6.56 us: 1.06x faster                                 |
| unpickle_list        | 6.83 us                                                | 7.55 us: 1.11x slower                                 |
| unpickle             | 21.2 us                                                | 24.7 us: 1.16x slower                                 |
| json_loads           | 37.9 us                                                | 45.4 us: 1.20x slower                                 |
| xml_etree_generate   | 127 ms                                                 | 162 ms: 1.27x slower                                  |
| json_dumps           | 14.3 ms                                                | 18.6 ms: 1.30x slower                                 |
| tomli_loads          | 2.88 sec                                               | 4.21 sec: 1.46x slower                                |
| xml_etree_process    | 83.7 ms                                                | 132 ms: 1.58x slower                                  |
| pickle_pure_python   | 436 us                                                 | 764 us: 1.75x slower                                  |
| unpickle_pure_python | 300 us                                                 | 537 us: 1.79x slower                                  |
| Geometric mean       | (ref)                                                  | 1.19x slower                                          |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240806-linux-x86_64-python-main-3.14.0a0-4767a6e |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 19.2 ms: 1.09x slower                                 |
| python_startup         | 23.7 ms                                                | 29.3 ms: 1.24x slower                                 |
| Geometric mean         | (ref)                                                  | 1.16x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240806-linux-x86_64-python-main-3.14.0a0-4767a6e |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_xml      | 67.6 ms                                                | 123 ms: 1.82x slower                                  |
| django_template | 44.9 ms                                                | 81.9 ms: 1.82x slower                                 |
| genshi_text     | 30.2 ms                                                | 56.5 ms: 1.87x slower                                 |
| mako            | 15.7 ms                                                | 30.3 ms: 1.93x slower                                 |
| Geometric mean  | (ref)                                                  | 1.86x slower                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240806-linux-x86_64-python-main-3.14.0a0-4767a6e |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.14 sec: 1.70x faster                                |
| async_tree_io              | 1.85 sec                                               | 1.24 sec: 1.49x faster                                |
| async_tree_memoization_tg  | 930 ms                                                 | 634 ms: 1.47x faster                                  |
| async_tree_none_tg         | 704 ms                                                 | 483 ms: 1.46x faster                                  |
| async_tree_memoization     | 977 ms                                                 | 744 ms: 1.31x faster                                  |
| bench_mp_pool              | 20.7 ms                                                | 16.0 ms: 1.30x faster                                 |
| pickle_dict                | 52.7 us                                                | 42.8 us: 1.23x faster                                 |
| async_tree_none            | 741 ms                                                 | 607 ms: 1.22x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 909 ms: 1.21x faster                                  |
| gc_traversal               | 5.86 ms                                                | 5.03 ms: 1.17x faster                                 |
| pickle                     | 16.4 us                                                | 14.1 us: 1.16x faster                                 |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 961 ms: 1.12x faster                                  |
| xml_etree_parse            | 241 ms                                                 | 222 ms: 1.08x faster                                  |
| pickle_list                | 6.97 us                                                | 6.56 us: 1.06x faster                                 |
| pathlib                    | 31.6 ms                                                | 33.6 ms: 1.06x slower                                 |
| pidigits                   | 250 ms                                                 | 267 ms: 1.07x slower                                  |
| python_startup_no_site     | 17.6 ms                                                | 19.2 ms: 1.09x slower                                 |
| sqlite_synth               | 3.87 us                                                | 4.22 us: 1.09x slower                                 |
| regex_dna                  | 278 ms                                                 | 304 ms: 1.09x slower                                  |
| unpickle_list              | 6.83 us                                                | 7.55 us: 1.11x slower                                 |
| regex_v8                   | 32.5 ms                                                | 36.9 ms: 1.14x slower                                 |
| unpickle                   | 21.2 us                                                | 24.7 us: 1.16x slower                                 |
| asyncio_tcp_ssl            | 2.81 sec                                               | 3.33 sec: 1.18x slower                                |
| json_loads                 | 37.9 us                                                | 45.4 us: 1.20x slower                                 |
| asyncio_tcp                | 923 ms                                                 | 1.11 sec: 1.20x slower                                |
| python_startup             | 23.7 ms                                                | 29.3 ms: 1.24x slower                                 |
| pycparser                  | 1.79 sec                                               | 2.23 sec: 1.24x slower                                |
| docutils                   | 4.00 sec                                               | 5.00 sec: 1.25x slower                                |
| async_generators           | 589 ms                                                 | 740 ms: 1.26x slower                                  |
| mdp                        | 3.97 sec                                               | 5.00 sec: 1.26x slower                                |
| tornado_http               | 266 ms                                                 | 337 ms: 1.27x slower                                  |
| pylint                     | 465 ms                                                 | 591 ms: 1.27x slower                                  |
| xml_etree_generate         | 127 ms                                                 | 162 ms: 1.27x slower                                  |
| bench_thread_pool          | 3.48 ms                                                | 4.44 ms: 1.28x slower                                 |
| deepcopy                   | 468 us                                                 | 602 us: 1.29x slower                                  |
| json_dumps                 | 14.3 ms                                                | 18.6 ms: 1.30x slower                                 |
| scimark_fft                | 500 ms                                                 | 651 ms: 1.30x slower                                  |
| json                       | 6.85 ms                                                | 8.93 ms: 1.30x slower                                 |
| generators                 | 41.1 ms                                                | 53.8 ms: 1.31x slower                                 |
| deepcopy_memo              | 52.4 us                                                | 72.1 us: 1.38x slower                                 |
| nqueens                    | 117 ms                                                 | 161 ms: 1.38x slower                                  |
| crypto_pyaes               | 107 ms                                                 | 154 ms: 1.43x slower                                  |
| meteor_contest             | 146 ms                                                 | 212 ms: 1.45x slower                                  |
| 2to3                       | 456 ms                                                 | 666 ms: 1.46x slower                                  |
| tomli_loads                | 2.88 sec                                               | 4.21 sec: 1.46x slower                                |
| bpe_tokeniser              | 6.59 sec                                               | 9.70 sec: 1.47x slower                                |
| deepcopy_reduce            | 4.04 us                                                | 5.96 us: 1.48x slower                                 |
| coroutines                 | 29.5 ms                                                | 43.8 ms: 1.48x slower                                 |
| sympy_integrate            | 29.8 ms                                                | 44.2 ms: 1.49x slower                                 |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 9.98 ms: 1.49x slower                                 |
| fannkuch                   | 540 ms                                                 | 806 ms: 1.49x slower                                  |
| sqlglot_normalize          | 157 ms                                                 | 237 ms: 1.51x slower                                  |
| pyflate                    | 727 ms                                                 | 1.10 sec: 1.51x slower                                |
| telco                      | 9.59 ms                                                | 14.8 ms: 1.54x slower                                 |
| regex_compile              | 187 ms                                                 | 288 ms: 1.54x slower                                  |
| comprehensions             | 27.1 us                                                | 41.9 us: 1.55x slower                                 |
| float                      | 123 ms                                                 | 190 ms: 1.55x slower                                  |
| xml_etree_process          | 83.7 ms                                                | 132 ms: 1.58x slower                                  |
| spectral_norm              | 156 ms                                                 | 247 ms: 1.59x slower                                  |
| logging_simple             | 9.45 us                                                | 15.1 us: 1.60x slower                                 |
| sqlglot_optimize           | 76.0 ms                                                | 122 ms: 1.60x slower                                  |
| coverage                   | 95.4 ms                                                | 157 ms: 1.65x slower                                  |
| thrift                     | 1.06 ms                                                | 1.78 ms: 1.68x slower                                 |
| typing_runtime_protocols   | 224 us                                                 | 383 us: 1.71x slower                                  |
| pprint_safe_repr           | 967 ms                                                 | 1.65 sec: 1.71x slower                                |
| pprint_pformat             | 1.98 sec                                               | 3.44 sec: 1.74x slower                                |
| richards_super             | 72.8 ms                                                | 127 ms: 1.74x slower                                  |
| scimark_monte_carlo        | 96.4 ms                                                | 168 ms: 1.74x slower                                  |
| pickle_pure_python         | 436 us                                                 | 764 us: 1.75x slower                                  |
| unpickle_pure_python       | 300 us                                                 | 537 us: 1.79x slower                                  |
| sympy_str                  | 385 ms                                                 | 698 ms: 1.81x slower                                  |
| html5lib                   | 88.9 ms                                                | 162 ms: 1.82x slower                                  |
| genshi_xml                 | 67.6 ms                                                | 123 ms: 1.82x slower                                  |
| django_template            | 44.9 ms                                                | 81.9 ms: 1.82x slower                                 |
| genshi_text                | 30.2 ms                                                | 56.5 ms: 1.87x slower                                 |
| logging_silent             | 139 ns                                                 | 267 ns: 1.92x slower                                  |
| richards                   | 60.3 ms                                                | 116 ms: 1.92x slower                                  |
| mako                       | 15.7 ms                                                | 30.3 ms: 1.93x slower                                 |
| hexiom                     | 8.27 ms                                                | 16.2 ms: 1.96x slower                                 |
| logging_format             | 9.59 us                                                | 18.8 us: 1.96x slower                                 |
| raytrace                   | 408 ms                                                 | 800 ms: 1.96x slower                                  |
| sqlglot_transpile          | 2.34 ms                                                | 4.65 ms: 1.99x slower                                 |
| scimark_sor                | 167 ms                                                 | 347 ms: 2.09x slower                                  |
| chaos                      | 84.9 ms                                                | 179 ms: 2.11x slower                                  |
| sqlglot_parse              | 1.79 ms                                                | 3.79 ms: 2.12x slower                                 |
| sympy_sum                  | 222 ms                                                 | 470 ms: 2.12x slower                                  |
| scimark_lu                 | 152 ms                                                 | 336 ms: 2.21x slower                                  |
| sympy_expand               | 582 ms                                                 | 1.30 sec: 2.23x slower                                |
| nbody                      | 119 ms                                                 | 309 ms: 2.59x slower                                  |
| go                         | 172 ms                                                 | 457 ms: 2.65x slower                                  |
| deltablue                  | 4.27 ms                                                | 11.9 ms: 2.78x slower                                 |
| unpack_sequence            | 60.2 ns                                                | 217 ns: 3.60x slower                                  |
| Geometric mean             | (ref)                                                  | 1.39x slower                                          |

Benchmark hidden because not significant (4): regex_effbot, asyncio_websockets, xml_etree_iterparse, create_gc_cycles
Ignored benchmarks (9) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.29x
- 95% likely to have a slowdown of 1.27x
- 99% likely to have a slowdown of 1.25x

# Memory
- memory change: 1.15x