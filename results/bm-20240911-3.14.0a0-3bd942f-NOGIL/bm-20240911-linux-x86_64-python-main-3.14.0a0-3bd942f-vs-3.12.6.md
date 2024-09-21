# Results vs. 3.12.6

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 3bd942f
- commit date: 2024-09-11
- overall geometric mean: 1.36x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.24x slower
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 456 ms                                                 | 626 ms: 1.37x slower                                  |
| docutils       | 4.00 sec                                               | 4.76 sec: 1.19x slower                                |
| html5lib       | 88.9 ms                                                | 141 ms: 1.58x slower                                  |
| tornado_http   | 266 ms                                                 | 352 ms: 1.32x slower                                  |
| Geometric mean | (ref)                                                  | 1.36x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.13 sec: 1.72x faster                                |
| async_tree_memoization_tg  | 930 ms                                                 | 653 ms: 1.42x faster                                  |
| async_tree_none_tg         | 704 ms                                                 | 495 ms: 1.42x faster                                  |
| async_tree_io              | 1.85 sec                                               | 1.31 sec: 1.41x faster                                |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 829 ms: 1.33x faster                                  |
| async_tree_memoization     | 977 ms                                                 | 748 ms: 1.31x faster                                  |
| async_tree_none            | 741 ms                                                 | 575 ms: 1.29x faster                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 980 ms: 1.10x faster                                  |
| asyncio_tcp_ssl            | 2.81 sec                                               | 3.27 sec: 1.16x slower                                |
| asyncio_tcp                | 923 ms                                                 | 1.09 sec: 1.18x slower                                |
| async_generators           | 589 ms                                                 | 712 ms: 1.21x slower                                  |
| coroutines                 | 29.5 ms                                                | 45.1 ms: 1.53x slower                                 |
| Geometric mean             | (ref)                                                  | 1.13x faster                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| float          | 123 ms                                                 | 201 ms: 1.63x slower                                  |
| nbody          | 119 ms                                                 | 312 ms: 2.62x slower                                  |
| Geometric mean | (ref)                                                  | 1.61x slower                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.56 ms: 1.13x faster                                 |
| regex_v8       | 32.5 ms                                                | 36.1 ms: 1.11x slower                                 |
| regex_compile  | 187 ms                                                 | 290 ms: 1.55x slower                                  |
| Geometric mean | (ref)                                                  | 1.12x slower                                          |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| pickle_dict          | 52.7 us                                                | 43.5 us: 1.21x faster                                 |
| pickle_list          | 6.97 us                                                | 6.36 us: 1.10x faster                                 |
| pickle               | 16.4 us                                                | 14.9 us: 1.10x faster                                 |
| unpickle             | 21.2 us                                                | 22.7 us: 1.07x slower                                 |
| unpickle_list        | 6.83 us                                                | 7.59 us: 1.11x slower                                 |
| json_loads           | 37.9 us                                                | 42.8 us: 1.13x slower                                 |
| xml_etree_generate   | 127 ms                                                 | 157 ms: 1.23x slower                                  |
| json_dumps           | 14.3 ms                                                | 18.9 ms: 1.32x slower                                 |
| xml_etree_process    | 83.7 ms                                                | 121 ms: 1.45x slower                                  |
| tomli_loads          | 2.88 sec                                               | 4.35 sec: 1.51x slower                                |
| unpickle_pure_python | 300 us                                                 | 547 us: 1.83x slower                                  |
| pickle_pure_python   | 436 us                                                 | 804 us: 1.85x slower                                  |
| Geometric mean       | (ref)                                                  | 1.19x slower                                          |

Benchmark hidden because not significant (2): xml_etree_parse, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 21.2 ms: 1.21x slower                                 |
| python_startup         | 23.7 ms                                                | 30.9 ms: 1.30x slower                                 |
| Geometric mean         | (ref)                                                  | 1.25x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_xml      | 67.6 ms                                                | 116 ms: 1.72x slower                                  |
| django_template | 44.9 ms                                                | 83.8 ms: 1.87x slower                                 |
| genshi_text     | 30.2 ms                                                | 58.2 ms: 1.93x slower                                 |
| mako            | 15.7 ms                                                | 31.2 ms: 1.98x slower                                 |
| Geometric mean  | (ref)                                                  | 1.87x slower                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.13 sec: 1.72x faster                                |
| async_tree_memoization_tg  | 930 ms                                                 | 653 ms: 1.42x faster                                  |
| async_tree_none_tg         | 704 ms                                                 | 495 ms: 1.42x faster                                  |
| async_tree_io              | 1.85 sec                                               | 1.31 sec: 1.41x faster                                |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 829 ms: 1.33x faster                                  |
| async_tree_memoization     | 977 ms                                                 | 748 ms: 1.31x faster                                  |
| gc_traversal               | 5.86 ms                                                | 4.51 ms: 1.30x faster                                 |
| async_tree_none            | 741 ms                                                 | 575 ms: 1.29x faster                                  |
| pickle_dict                | 52.7 us                                                | 43.5 us: 1.21x faster                                 |
| bench_mp_pool              | 20.7 ms                                                | 17.5 ms: 1.18x faster                                 |
| regex_effbot               | 5.13 ms                                                | 4.56 ms: 1.13x faster                                 |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 980 ms: 1.10x faster                                  |
| pickle_list                | 6.97 us                                                | 6.36 us: 1.10x faster                                 |
| pickle                     | 16.4 us                                                | 14.9 us: 1.10x faster                                 |
| create_gc_cycles           | 1.94 ms                                                | 1.83 ms: 1.06x faster                                 |
| unpickle                   | 21.2 us                                                | 22.7 us: 1.07x slower                                 |
| sqlite_synth               | 3.87 us                                                | 4.19 us: 1.08x slower                                 |
| regex_v8                   | 32.5 ms                                                | 36.1 ms: 1.11x slower                                 |
| unpickle_list              | 6.83 us                                                | 7.59 us: 1.11x slower                                 |
| json_loads                 | 37.9 us                                                | 42.8 us: 1.13x slower                                 |
| pathlib                    | 31.6 ms                                                | 36.6 ms: 1.16x slower                                 |
| asyncio_tcp_ssl            | 2.81 sec                                               | 3.27 sec: 1.16x slower                                |
| json                       | 6.85 ms                                                | 7.97 ms: 1.16x slower                                 |
| scimark_fft                | 500 ms                                                 | 587 ms: 1.17x slower                                  |
| asyncio_tcp                | 923 ms                                                 | 1.09 sec: 1.18x slower                                |
| docutils                   | 4.00 sec                                               | 4.76 sec: 1.19x slower                                |
| bench_thread_pool          | 3.48 ms                                                | 4.19 ms: 1.21x slower                                 |
| python_startup_no_site     | 17.6 ms                                                | 21.2 ms: 1.21x slower                                 |
| async_generators           | 589 ms                                                 | 712 ms: 1.21x slower                                  |
| xml_etree_generate         | 127 ms                                                 | 157 ms: 1.23x slower                                  |
| deepcopy                   | 468 us                                                 | 579 us: 1.24x slower                                  |
| pycparser                  | 1.79 sec                                               | 2.28 sec: 1.27x slower                                |
| meteor_contest             | 146 ms                                                 | 186 ms: 1.27x slower                                  |
| pylint                     | 465 ms                                                 | 593 ms: 1.28x slower                                  |
| mdp                        | 3.97 sec                                               | 5.11 sec: 1.29x slower                                |
| dulwich_log                | 100 ms                                                 | 130 ms: 1.29x slower                                  |
| python_startup             | 23.7 ms                                                | 30.9 ms: 1.30x slower                                 |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 8.77 ms: 1.31x slower                                 |
| json_dumps                 | 14.3 ms                                                | 18.9 ms: 1.32x slower                                 |
| tornado_http               | 266 ms                                                 | 352 ms: 1.32x slower                                  |
| generators                 | 41.1 ms                                                | 54.8 ms: 1.33x slower                                 |
| nqueens                    | 117 ms                                                 | 160 ms: 1.37x slower                                  |
| 2to3                       | 456 ms                                                 | 626 ms: 1.37x slower                                  |
| crypto_pyaes               | 107 ms                                                 | 151 ms: 1.41x slower                                  |
| deepcopy_memo              | 52.4 us                                                | 73.7 us: 1.41x slower                                 |
| comprehensions             | 27.1 us                                                | 38.4 us: 1.42x slower                                 |
| fannkuch                   | 540 ms                                                 | 767 ms: 1.42x slower                                  |
| xml_etree_process          | 83.7 ms                                                | 121 ms: 1.45x slower                                  |
| deepcopy_reduce            | 4.04 us                                                | 5.88 us: 1.46x slower                                 |
| telco                      | 9.59 ms                                                | 14.0 ms: 1.46x slower                                 |
| sympy_integrate            | 29.8 ms                                                | 43.8 ms: 1.47x slower                                 |
| pyflate                    | 727 ms                                                 | 1.08 sec: 1.48x slower                                |
| tomli_loads                | 2.88 sec                                               | 4.35 sec: 1.51x slower                                |
| bpe_tokeniser              | 6.59 sec                                               | 10.0 sec: 1.52x slower                                |
| coroutines                 | 29.5 ms                                                | 45.1 ms: 1.53x slower                                 |
| coverage                   | 95.4 ms                                                | 147 ms: 1.55x slower                                  |
| regex_compile              | 187 ms                                                 | 290 ms: 1.55x slower                                  |
| thrift                     | 1.06 ms                                                | 1.65 ms: 1.56x slower                                 |
| sqlglot_normalize          | 157 ms                                                 | 245 ms: 1.56x slower                                  |
| html5lib                   | 88.9 ms                                                | 141 ms: 1.58x slower                                  |
| logging_simple             | 9.45 us                                                | 15.0 us: 1.59x slower                                 |
| typing_runtime_protocols   | 224 us                                                 | 364 us: 1.62x slower                                  |
| scimark_monte_carlo        | 96.4 ms                                                | 157 ms: 1.63x slower                                  |
| float                      | 123 ms                                                 | 201 ms: 1.63x slower                                  |
| spectral_norm              | 156 ms                                                 | 254 ms: 1.63x slower                                  |
| sqlglot_optimize           | 76.0 ms                                                | 125 ms: 1.64x slower                                  |
| logging_format             | 9.59 us                                                | 16.0 us: 1.67x slower                                 |
| genshi_xml                 | 67.6 ms                                                | 116 ms: 1.72x slower                                  |
| richards                   | 60.3 ms                                                | 105 ms: 1.74x slower                                  |
| sympy_str                  | 385 ms                                                 | 672 ms: 1.75x slower                                  |
| pprint_safe_repr           | 967 ms                                                 | 1.69 sec: 1.75x slower                                |
| pprint_pformat             | 1.98 sec                                               | 3.52 sec: 1.78x slower                                |
| richards_super             | 72.8 ms                                                | 130 ms: 1.79x slower                                  |
| unpickle_pure_python       | 300 us                                                 | 547 us: 1.83x slower                                  |
| pickle_pure_python         | 436 us                                                 | 804 us: 1.85x slower                                  |
| django_template            | 44.9 ms                                                | 83.8 ms: 1.87x slower                                 |
| genshi_text                | 30.2 ms                                                | 58.2 ms: 1.93x slower                                 |
| hexiom                     | 8.27 ms                                                | 16.0 ms: 1.94x slower                                 |
| sqlglot_transpile          | 2.34 ms                                                | 4.53 ms: 1.94x slower                                 |
| raytrace                   | 408 ms                                                 | 791 ms: 1.94x slower                                  |
| logging_silent             | 139 ns                                                 | 272 ns: 1.96x slower                                  |
| sqlglot_parse              | 1.79 ms                                                | 3.50 ms: 1.96x slower                                 |
| chaos                      | 84.9 ms                                                | 168 ms: 1.98x slower                                  |
| mako                       | 15.7 ms                                                | 31.2 ms: 1.98x slower                                 |
| scimark_sor                | 167 ms                                                 | 337 ms: 2.02x slower                                  |
| scimark_lu                 | 152 ms                                                 | 309 ms: 2.03x slower                                  |
| sympy_sum                  | 222 ms                                                 | 464 ms: 2.09x slower                                  |
| go                         | 172 ms                                                 | 369 ms: 2.15x slower                                  |
| sympy_expand               | 582 ms                                                 | 1.36 sec: 2.33x slower                                |
| deltablue                  | 4.27 ms                                                | 10.9 ms: 2.55x slower                                 |
| nbody                      | 119 ms                                                 | 312 ms: 2.62x slower                                  |
| unpack_sequence            | 60.2 ns                                                | 187 ns: 3.11x slower                                  |
| Geometric mean             | (ref)                                                  | 1.36x slower                                          |

Benchmark hidden because not significant (5): pidigits, xml_etree_parse, asyncio_websockets, regex_dna, xml_etree_iterparse
Ignored benchmarks (8) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.28x
- 95% likely to have a slowdown of 1.27x
- 99% likely to have a slowdown of 1.24x

# Memory
- memory change: 1.15x