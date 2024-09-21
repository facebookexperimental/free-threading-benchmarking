# Results vs. 3.12.6

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 8145ebe
- commit date: 2024-09-12
- overall geometric mean: 1.37x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.26x slower
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240912-linux-x86_64-python-main-3.14.0a0-8145ebe |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 456 ms                                                 | 669 ms: 1.47x slower                                  |
| docutils       | 4.00 sec                                               | 4.89 sec: 1.22x slower                                |
| html5lib       | 88.9 ms                                                | 133 ms: 1.50x slower                                  |
| tornado_http   | 266 ms                                                 | 374 ms: 1.41x slower                                  |
| Geometric mean | (ref)                                                  | 1.39x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240912-linux-x86_64-python-main-3.14.0a0-8145ebe |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.17 sec: 1.66x faster                                |
| async_tree_io              | 1.85 sec                                               | 1.24 sec: 1.49x faster                                |
| async_tree_memoization_tg  | 930 ms                                                 | 651 ms: 1.43x faster                                  |
| async_tree_none_tg         | 704 ms                                                 | 497 ms: 1.42x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 844 ms: 1.30x faster                                  |
| async_tree_memoization     | 977 ms                                                 | 751 ms: 1.30x faster                                  |
| async_tree_none            | 741 ms                                                 | 609 ms: 1.22x faster                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 948 ms: 1.14x faster                                  |
| asyncio_websockets         | 748 ms                                                 | 802 ms: 1.07x slower                                  |
| asyncio_tcp_ssl            | 2.81 sec                                               | 3.36 sec: 1.19x slower                                |
| asyncio_tcp                | 923 ms                                                 | 1.10 sec: 1.20x slower                                |
| async_generators           | 589 ms                                                 | 742 ms: 1.26x slower                                  |
| coroutines                 | 29.5 ms                                                | 44.4 ms: 1.50x slower                                 |
| Geometric mean             | (ref)                                                  | 1.11x faster                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240912-linux-x86_64-python-main-3.14.0a0-8145ebe |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| float          | 123 ms                                                 | 196 ms: 1.59x slower                                  |
| nbody          | 119 ms                                                 | 281 ms: 2.36x slower                                  |
| Geometric mean | (ref)                                                  | 1.55x slower                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240912-linux-x86_64-python-main-3.14.0a0-8145ebe |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.42 ms: 1.16x faster                                 |
| regex_v8       | 32.5 ms                                                | 37.2 ms: 1.15x slower                                 |
| regex_compile  | 187 ms                                                 | 288 ms: 1.54x slower                                  |
| Geometric mean | (ref)                                                  | 1.12x slower                                          |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240912-linux-x86_64-python-main-3.14.0a0-8145ebe |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| pickle_dict          | 52.7 us                                                | 45.4 us: 1.16x faster                                 |
| pickle               | 16.4 us                                                | 14.9 us: 1.10x faster                                 |
| xml_etree_parse      | 241 ms                                                 | 224 ms: 1.07x faster                                  |
| json_loads           | 37.9 us                                                | 41.7 us: 1.10x slower                                 |
| unpickle_list        | 6.83 us                                                | 7.64 us: 1.12x slower                                 |
| json_dumps           | 14.3 ms                                                | 17.8 ms: 1.24x slower                                 |
| xml_etree_generate   | 127 ms                                                 | 170 ms: 1.33x slower                                  |
| tomli_loads          | 2.88 sec                                               | 4.34 sec: 1.51x slower                                |
| xml_etree_process    | 83.7 ms                                                | 126 ms: 1.51x slower                                  |
| unpickle_pure_python | 300 us                                                 | 516 us: 1.72x slower                                  |
| pickle_pure_python   | 436 us                                                 | 847 us: 1.94x slower                                  |
| Geometric mean       | (ref)                                                  | 1.19x slower                                          |

Benchmark hidden because not significant (3): pickle_list, xml_etree_iterparse, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240912-linux-x86_64-python-main-3.14.0a0-8145ebe |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 21.3 ms: 1.21x slower                                 |
| python_startup         | 23.7 ms                                                | 32.2 ms: 1.36x slower                                 |
| Geometric mean         | (ref)                                                  | 1.28x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240912-linux-x86_64-python-main-3.14.0a0-8145ebe |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_xml      | 67.6 ms                                                | 118 ms: 1.75x slower                                  |
| django_template | 44.9 ms                                                | 85.0 ms: 1.89x slower                                 |
| mako            | 15.7 ms                                                | 31.6 ms: 2.01x slower                                 |
| genshi_text     | 30.2 ms                                                | 60.8 ms: 2.01x slower                                 |
| Geometric mean  | (ref)                                                  | 1.91x slower                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240912-linux-x86_64-python-main-3.14.0a0-8145ebe |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.17 sec: 1.66x faster                                |
| async_tree_io              | 1.85 sec                                               | 1.24 sec: 1.49x faster                                |
| async_tree_memoization_tg  | 930 ms                                                 | 651 ms: 1.43x faster                                  |
| async_tree_none_tg         | 704 ms                                                 | 497 ms: 1.42x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 844 ms: 1.30x faster                                  |
| async_tree_memoization     | 977 ms                                                 | 751 ms: 1.30x faster                                  |
| async_tree_none            | 741 ms                                                 | 609 ms: 1.22x faster                                  |
| gc_traversal               | 5.86 ms                                                | 4.89 ms: 1.20x faster                                 |
| pickle_dict                | 52.7 us                                                | 45.4 us: 1.16x faster                                 |
| regex_effbot               | 5.13 ms                                                | 4.42 ms: 1.16x faster                                 |
| bench_mp_pool              | 20.7 ms                                                | 17.9 ms: 1.15x faster                                 |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 948 ms: 1.14x faster                                  |
| pickle                     | 16.4 us                                                | 14.9 us: 1.10x faster                                 |
| xml_etree_parse            | 241 ms                                                 | 224 ms: 1.07x faster                                  |
| asyncio_websockets         | 748 ms                                                 | 802 ms: 1.07x slower                                  |
| json_loads                 | 37.9 us                                                | 41.7 us: 1.10x slower                                 |
| pathlib                    | 31.6 ms                                                | 35.3 ms: 1.12x slower                                 |
| unpickle_list              | 6.83 us                                                | 7.64 us: 1.12x slower                                 |
| sqlite_synth               | 3.87 us                                                | 4.43 us: 1.14x slower                                 |
| regex_v8                   | 32.5 ms                                                | 37.2 ms: 1.15x slower                                 |
| json                       | 6.85 ms                                                | 8.00 ms: 1.17x slower                                 |
| asyncio_tcp_ssl            | 2.81 sec                                               | 3.36 sec: 1.19x slower                                |
| asyncio_tcp                | 923 ms                                                 | 1.10 sec: 1.20x slower                                |
| python_startup_no_site     | 17.6 ms                                                | 21.3 ms: 1.21x slower                                 |
| docutils                   | 4.00 sec                                               | 4.89 sec: 1.22x slower                                |
| deepcopy                   | 468 us                                                 | 581 us: 1.24x slower                                  |
| json_dumps                 | 14.3 ms                                                | 17.8 ms: 1.24x slower                                 |
| pycparser                  | 1.79 sec                                               | 2.24 sec: 1.25x slower                                |
| async_generators           | 589 ms                                                 | 742 ms: 1.26x slower                                  |
| scimark_fft                | 500 ms                                                 | 631 ms: 1.26x slower                                  |
| generators                 | 41.1 ms                                                | 52.8 ms: 1.28x slower                                 |
| mdp                        | 3.97 sec                                               | 5.21 sec: 1.31x slower                                |
| pylint                     | 465 ms                                                 | 610 ms: 1.31x slower                                  |
| deepcopy_memo              | 52.4 us                                                | 68.8 us: 1.31x slower                                 |
| nqueens                    | 117 ms                                                 | 155 ms: 1.33x slower                                  |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 8.92 ms: 1.33x slower                                 |
| xml_etree_generate         | 127 ms                                                 | 170 ms: 1.33x slower                                  |
| python_startup             | 23.7 ms                                                | 32.2 ms: 1.36x slower                                 |
| bench_thread_pool          | 3.48 ms                                                | 4.74 ms: 1.36x slower                                 |
| comprehensions             | 27.1 us                                                | 37.2 us: 1.37x slower                                 |
| crypto_pyaes               | 107 ms                                                 | 151 ms: 1.40x slower                                  |
| tornado_http               | 266 ms                                                 | 374 ms: 1.41x slower                                  |
| meteor_contest             | 146 ms                                                 | 208 ms: 1.42x slower                                  |
| fannkuch                   | 540 ms                                                 | 767 ms: 1.42x slower                                  |
| pyflate                    | 727 ms                                                 | 1.04 sec: 1.43x slower                                |
| telco                      | 9.59 ms                                                | 13.9 ms: 1.45x slower                                 |
| deepcopy_reduce            | 4.04 us                                                | 5.91 us: 1.46x slower                                 |
| 2to3                       | 456 ms                                                 | 669 ms: 1.47x slower                                  |
| typing_runtime_protocols   | 224 us                                                 | 334 us: 1.49x slower                                  |
| html5lib                   | 88.9 ms                                                | 133 ms: 1.50x slower                                  |
| coroutines                 | 29.5 ms                                                | 44.4 ms: 1.50x slower                                 |
| tomli_loads                | 2.88 sec                                               | 4.34 sec: 1.51x slower                                |
| xml_etree_process          | 83.7 ms                                                | 126 ms: 1.51x slower                                  |
| regex_compile              | 187 ms                                                 | 288 ms: 1.54x slower                                  |
| sqlglot_optimize           | 76.0 ms                                                | 117 ms: 1.54x slower                                  |
| bpe_tokeniser              | 6.59 sec                                               | 10.2 sec: 1.56x slower                                |
| sympy_integrate            | 29.8 ms                                                | 46.3 ms: 1.56x slower                                 |
| spectral_norm              | 156 ms                                                 | 245 ms: 1.58x slower                                  |
| dulwich_log                | 100 ms                                                 | 159 ms: 1.58x slower                                  |
| sqlglot_normalize          | 157 ms                                                 | 250 ms: 1.59x slower                                  |
| float                      | 123 ms                                                 | 196 ms: 1.59x slower                                  |
| logging_simple             | 9.45 us                                                | 15.2 us: 1.61x slower                                 |
| thrift                     | 1.06 ms                                                | 1.71 ms: 1.61x slower                                 |
| coverage                   | 95.4 ms                                                | 156 ms: 1.64x slower                                  |
| richards_super             | 72.8 ms                                                | 123 ms: 1.69x slower                                  |
| logging_format             | 9.59 us                                                | 16.3 us: 1.70x slower                                 |
| unpickle_pure_python       | 300 us                                                 | 516 us: 1.72x slower                                  |
| scimark_monte_carlo        | 96.4 ms                                                | 166 ms: 1.73x slower                                  |
| pprint_safe_repr           | 967 ms                                                 | 1.69 sec: 1.75x slower                                |
| genshi_xml                 | 67.6 ms                                                | 118 ms: 1.75x slower                                  |
| pprint_pformat             | 1.98 sec                                               | 3.52 sec: 1.78x slower                                |
| sympy_str                  | 385 ms                                                 | 687 ms: 1.78x slower                                  |
| richards                   | 60.3 ms                                                | 108 ms: 1.79x slower                                  |
| logging_silent             | 139 ns                                                 | 256 ns: 1.84x slower                                  |
| chaos                      | 84.9 ms                                                | 159 ms: 1.88x slower                                  |
| raytrace                   | 408 ms                                                 | 766 ms: 1.88x slower                                  |
| sqlglot_transpile          | 2.34 ms                                                | 4.40 ms: 1.89x slower                                 |
| django_template            | 44.9 ms                                                | 85.0 ms: 1.89x slower                                 |
| hexiom                     | 8.27 ms                                                | 16.0 ms: 1.93x slower                                 |
| pickle_pure_python         | 436 us                                                 | 847 us: 1.94x slower                                  |
| mako                       | 15.7 ms                                                | 31.6 ms: 2.01x slower                                 |
| genshi_text                | 30.2 ms                                                | 60.8 ms: 2.01x slower                                 |
| scimark_lu                 | 152 ms                                                 | 307 ms: 2.02x slower                                  |
| scimark_sor                | 167 ms                                                 | 345 ms: 2.07x slower                                  |
| go                         | 172 ms                                                 | 361 ms: 2.10x slower                                  |
| sqlglot_parse              | 1.79 ms                                                | 3.90 ms: 2.18x slower                                 |
| sympy_sum                  | 222 ms                                                 | 491 ms: 2.21x slower                                  |
| sympy_expand               | 582 ms                                                 | 1.33 sec: 2.28x slower                                |
| nbody                      | 119 ms                                                 | 281 ms: 2.36x slower                                  |
| deltablue                  | 4.27 ms                                                | 11.6 ms: 2.73x slower                                 |
| unpack_sequence            | 60.2 ns                                                | 201 ns: 3.34x slower                                  |
| Geometric mean             | (ref)                                                  | 1.37x slower                                          |

Benchmark hidden because not significant (6): pickle_list, pidigits, regex_dna, xml_etree_iterparse, unpickle, create_gc_cycles
Ignored benchmarks (8) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.32x
- 95% likely to have a slowdown of 1.29x
- 99% likely to have a slowdown of 1.26x

# Memory
- memory change: 1.15x