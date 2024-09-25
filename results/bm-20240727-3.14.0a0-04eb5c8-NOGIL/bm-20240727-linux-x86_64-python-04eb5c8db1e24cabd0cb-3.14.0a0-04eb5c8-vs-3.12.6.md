# Results vs. 3.12.6

- fork: python
- ref: 04eb5c8db1e24cabd0cb
- machine: linux-x86_64
- commit hash: 04eb5c8
- commit date: 2024-07-27
- overall geometric mean: 1.35x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.22x slower
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 647 ms: 1.42x slower                                                  |
| docutils       | 4.00 sec                                               | 4.82 sec: 1.21x slower                                                |
| html5lib       | 88.9 ms                                                | 141 ms: 1.59x slower                                                  |
| tornado_http   | 266 ms                                                 | 342 ms: 1.29x slower                                                  |
| Geometric mean | (ref)                                                  | 1.37x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.12 sec: 1.73x faster                                                |
| async_tree_io              | 1.85 sec                                               | 1.23 sec: 1.50x faster                                                |
| async_tree_memoization_tg  | 930 ms                                                 | 632 ms: 1.47x faster                                                  |
| async_tree_none_tg         | 704 ms                                                 | 482 ms: 1.46x faster                                                  |
| async_tree_memoization     | 977 ms                                                 | 721 ms: 1.36x faster                                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 820 ms: 1.34x faster                                                  |
| async_tree_none            | 741 ms                                                 | 566 ms: 1.31x faster                                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 913 ms: 1.18x faster                                                  |
| asyncio_tcp                | 923 ms                                                 | 1.02 sec: 1.11x slower                                                |
| asyncio_tcp_ssl            | 2.81 sec                                               | 3.18 sec: 1.13x slower                                                |
| async_generators           | 589 ms                                                 | 723 ms: 1.23x slower                                                  |
| coroutines                 | 29.5 ms                                                | 39.3 ms: 1.33x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.17x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 123 ms                                                 | 193 ms: 1.57x slower                                                  |
| nbody          | 119 ms                                                 | 280 ms: 2.35x slower                                                  |
| Geometric mean | (ref)                                                  | 1.53x slower                                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.47 ms: 1.15x faster                                                 |
| regex_dna      | 278 ms                                                 | 295 ms: 1.06x slower                                                  |
| regex_v8       | 32.5 ms                                                | 35.3 ms: 1.09x slower                                                 |
| regex_compile  | 187 ms                                                 | 293 ms: 1.57x slower                                                  |
| Geometric mean | (ref)                                                  | 1.12x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_parse      | 241 ms                                                 | 201 ms: 1.20x faster                                                  |
| pickle_dict          | 52.7 us                                                | 44.0 us: 1.20x faster                                                 |
| pickle               | 16.4 us                                                | 14.5 us: 1.13x faster                                                 |
| pickle_list          | 6.97 us                                                | 6.53 us: 1.07x faster                                                 |
| xml_etree_iterparse  | 169 ms                                                 | 159 ms: 1.06x faster                                                  |
| unpickle_list        | 6.83 us                                                | 7.76 us: 1.14x slower                                                 |
| json_loads           | 37.9 us                                                | 43.6 us: 1.15x slower                                                 |
| json_dumps           | 14.3 ms                                                | 17.8 ms: 1.24x slower                                                 |
| xml_etree_generate   | 127 ms                                                 | 160 ms: 1.26x slower                                                  |
| tomli_loads          | 2.88 sec                                               | 4.22 sec: 1.46x slower                                                |
| xml_etree_process    | 83.7 ms                                                | 126 ms: 1.51x slower                                                  |
| unpickle_pure_python | 300 us                                                 | 558 us: 1.86x slower                                                  |
| pickle_pure_python   | 436 us                                                 | 830 us: 1.90x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.17x slower                                                          |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 19.5 ms: 1.11x slower                                                 |
| python_startup         | 23.7 ms                                                | 28.9 ms: 1.22x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.16x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 67.6 ms                                                | 120 ms: 1.77x slower                                                  |
| django_template | 44.9 ms                                                | 80.6 ms: 1.79x slower                                                 |
| genshi_text     | 30.2 ms                                                | 54.4 ms: 1.80x slower                                                 |
| mako            | 15.7 ms                                                | 29.9 ms: 1.90x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.82x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.12 sec: 1.73x faster                                                |
| bench_mp_pool              | 20.7 ms                                                | 13.6 ms: 1.52x faster                                                 |
| async_tree_io              | 1.85 sec                                               | 1.23 sec: 1.50x faster                                                |
| async_tree_memoization_tg  | 930 ms                                                 | 632 ms: 1.47x faster                                                  |
| async_tree_none_tg         | 704 ms                                                 | 482 ms: 1.46x faster                                                  |
| gc_traversal               | 5.86 ms                                                | 4.28 ms: 1.37x faster                                                 |
| async_tree_memoization     | 977 ms                                                 | 721 ms: 1.36x faster                                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 820 ms: 1.34x faster                                                  |
| async_tree_none            | 741 ms                                                 | 566 ms: 1.31x faster                                                  |
| xml_etree_parse            | 241 ms                                                 | 201 ms: 1.20x faster                                                  |
| pickle_dict                | 52.7 us                                                | 44.0 us: 1.20x faster                                                 |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 913 ms: 1.18x faster                                                  |
| regex_effbot               | 5.13 ms                                                | 4.47 ms: 1.15x faster                                                 |
| pickle                     | 16.4 us                                                | 14.5 us: 1.13x faster                                                 |
| pickle_list                | 6.97 us                                                | 6.53 us: 1.07x faster                                                 |
| xml_etree_iterparse        | 169 ms                                                 | 159 ms: 1.06x faster                                                  |
| regex_dna                  | 278 ms                                                 | 295 ms: 1.06x slower                                                  |
| regex_v8                   | 32.5 ms                                                | 35.3 ms: 1.09x slower                                                 |
| sqlite_synth               | 3.87 us                                                | 4.28 us: 1.10x slower                                                 |
| asyncio_tcp                | 923 ms                                                 | 1.02 sec: 1.11x slower                                                |
| python_startup_no_site     | 17.6 ms                                                | 19.5 ms: 1.11x slower                                                 |
| json                       | 6.85 ms                                                | 7.69 ms: 1.12x slower                                                 |
| asyncio_tcp_ssl            | 2.81 sec                                               | 3.18 sec: 1.13x slower                                                |
| unpickle_list              | 6.83 us                                                | 7.76 us: 1.14x slower                                                 |
| json_loads                 | 37.9 us                                                | 43.6 us: 1.15x slower                                                 |
| docutils                   | 4.00 sec                                               | 4.82 sec: 1.21x slower                                                |
| pylint                     | 465 ms                                                 | 562 ms: 1.21x slower                                                  |
| pycparser                  | 1.79 sec                                               | 2.18 sec: 1.21x slower                                                |
| python_startup             | 23.7 ms                                                | 28.9 ms: 1.22x slower                                                 |
| bench_thread_pool          | 3.48 ms                                                | 4.27 ms: 1.23x slower                                                 |
| async_generators           | 589 ms                                                 | 723 ms: 1.23x slower                                                  |
| json_dumps                 | 14.3 ms                                                | 17.8 ms: 1.24x slower                                                 |
| xml_etree_generate         | 127 ms                                                 | 160 ms: 1.26x slower                                                  |
| mdp                        | 3.97 sec                                               | 5.02 sec: 1.26x slower                                                |
| scimark_fft                | 500 ms                                                 | 641 ms: 1.28x slower                                                  |
| deepcopy                   | 468 us                                                 | 600 us: 1.28x slower                                                  |
| tornado_http               | 266 ms                                                 | 342 ms: 1.29x slower                                                  |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 8.68 ms: 1.30x slower                                                 |
| deepcopy_memo              | 52.4 us                                                | 69.1 us: 1.32x slower                                                 |
| generators                 | 41.1 ms                                                | 54.8 ms: 1.33x slower                                                 |
| coroutines                 | 29.5 ms                                                | 39.3 ms: 1.33x slower                                                 |
| nqueens                    | 117 ms                                                 | 162 ms: 1.39x slower                                                  |
| comprehensions             | 27.1 us                                                | 38.3 us: 1.41x slower                                                 |
| 2to3                       | 456 ms                                                 | 647 ms: 1.42x slower                                                  |
| meteor_contest             | 146 ms                                                 | 208 ms: 1.42x slower                                                  |
| deepcopy_reduce            | 4.04 us                                                | 5.73 us: 1.42x slower                                                 |
| fannkuch                   | 540 ms                                                 | 772 ms: 1.43x slower                                                  |
| sympy_integrate            | 29.8 ms                                                | 42.8 ms: 1.44x slower                                                 |
| tomli_loads                | 2.88 sec                                               | 4.22 sec: 1.46x slower                                                |
| telco                      | 9.59 ms                                                | 14.1 ms: 1.47x slower                                                 |
| pyflate                    | 727 ms                                                 | 1.07 sec: 1.47x slower                                                |
| coverage                   | 95.4 ms                                                | 141 ms: 1.48x slower                                                  |
| crypto_pyaes               | 107 ms                                                 | 159 ms: 1.48x slower                                                  |
| bpe_tokeniser              | 6.59 sec                                               | 9.90 sec: 1.50x slower                                                |
| xml_etree_process          | 83.7 ms                                                | 126 ms: 1.51x slower                                                  |
| spectral_norm              | 156 ms                                                 | 242 ms: 1.56x slower                                                  |
| sqlglot_normalize          | 157 ms                                                 | 246 ms: 1.57x slower                                                  |
| regex_compile              | 187 ms                                                 | 293 ms: 1.57x slower                                                  |
| float                      | 123 ms                                                 | 193 ms: 1.57x slower                                                  |
| html5lib                   | 88.9 ms                                                | 141 ms: 1.59x slower                                                  |
| thrift                     | 1.06 ms                                                | 1.70 ms: 1.61x slower                                                 |
| typing_runtime_protocols   | 224 us                                                 | 362 us: 1.61x slower                                                  |
| logging_simple             | 9.45 us                                                | 15.9 us: 1.68x slower                                                 |
| sympy_str                  | 385 ms                                                 | 663 ms: 1.72x slower                                                  |
| richards_super             | 72.8 ms                                                | 125 ms: 1.72x slower                                                  |
| sqlglot_optimize           | 76.0 ms                                                | 133 ms: 1.75x slower                                                  |
| pprint_pformat             | 1.98 sec                                               | 3.48 sec: 1.76x slower                                                |
| scimark_monte_carlo        | 96.4 ms                                                | 171 ms: 1.77x slower                                                  |
| genshi_xml                 | 67.6 ms                                                | 120 ms: 1.77x slower                                                  |
| pprint_safe_repr           | 967 ms                                                 | 1.73 sec: 1.79x slower                                                |
| django_template            | 44.9 ms                                                | 80.6 ms: 1.79x slower                                                 |
| genshi_text                | 30.2 ms                                                | 54.4 ms: 1.80x slower                                                 |
| logging_format             | 9.59 us                                                | 17.6 us: 1.84x slower                                                 |
| richards                   | 60.3 ms                                                | 111 ms: 1.85x slower                                                  |
| logging_silent             | 139 ns                                                 | 259 ns: 1.86x slower                                                  |
| unpickle_pure_python       | 300 us                                                 | 558 us: 1.86x slower                                                  |
| mako                       | 15.7 ms                                                | 29.9 ms: 1.90x slower                                                 |
| pickle_pure_python         | 436 us                                                 | 830 us: 1.90x slower                                                  |
| chaos                      | 84.9 ms                                                | 163 ms: 1.92x slower                                                  |
| sqlglot_transpile          | 2.34 ms                                                | 4.53 ms: 1.94x slower                                                 |
| raytrace                   | 408 ms                                                 | 806 ms: 1.98x slower                                                  |
| scimark_lu                 | 152 ms                                                 | 313 ms: 2.06x slower                                                  |
| sqlglot_parse              | 1.79 ms                                                | 3.76 ms: 2.10x slower                                                 |
| scimark_sor                | 167 ms                                                 | 351 ms: 2.10x slower                                                  |
| hexiom                     | 8.27 ms                                                | 17.4 ms: 2.11x slower                                                 |
| sympy_expand               | 582 ms                                                 | 1.27 sec: 2.18x slower                                                |
| sympy_sum                  | 222 ms                                                 | 493 ms: 2.22x slower                                                  |
| nbody                      | 119 ms                                                 | 280 ms: 2.35x slower                                                  |
| go                         | 172 ms                                                 | 406 ms: 2.36x slower                                                  |
| deltablue                  | 4.27 ms                                                | 11.7 ms: 2.73x slower                                                 |
| unpack_sequence            | 60.2 ns                                                | 201 ns: 3.34x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.35x slower                                                          |

Benchmark hidden because not significant (5): pidigits, asyncio_websockets, create_gc_cycles, unpickle, pathlib
Ignored benchmarks (9) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.28x
- 95% likely to have a slowdown of 1.26x
- 99% likely to have a slowdown of 1.22x

# Memory
- memory change: 1.16x