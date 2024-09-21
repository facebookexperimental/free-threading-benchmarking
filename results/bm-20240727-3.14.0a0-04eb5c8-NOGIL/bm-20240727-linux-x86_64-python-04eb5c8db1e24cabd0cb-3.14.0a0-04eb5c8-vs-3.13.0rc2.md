# Results vs. 3.13.0rc2

- fork: python
- ref: 04eb5c8db1e24cabd0cb
- machine: linux-x86_64
- commit hash: 04eb5c8
- commit date: 2024-07-27
- overall geometric mean: 1.40x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.28x slower
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 647 ms: 1.45x slower                                                  |
| docutils       | 4.01 sec                                                     | 4.82 sec: 1.20x slower                                                |
| html5lib       | 92.6 ms                                                      | 141 ms: 1.52x slower                                                  |
| tornado_http   | 251 ms                                                       | 342 ms: 1.36x slower                                                  |
| Geometric mean | (ref)                                                        | 1.38x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 1.12 sec: 1.26x faster                                                |
| async_tree_io              | 1.39 sec                                                     | 1.23 sec: 1.13x faster                                                |
| async_tree_memoization_tg  | 670 ms                                                       | 632 ms: 1.06x faster                                                  |
| async_tree_none_tg         | 504 ms                                                       | 482 ms: 1.04x faster                                                  |
| asyncio_websockets         | 766 ms                                                       | 735 ms: 1.04x faster                                                  |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 820 ms: 1.04x faster                                                  |
| asyncio_tcp                | 948 ms                                                       | 1.02 sec: 1.08x slower                                                |
| asyncio_tcp_ssl            | 2.77 sec                                                     | 3.18 sec: 1.14x slower                                                |
| async_generators           | 567 ms                                                       | 723 ms: 1.27x slower                                                  |
| coroutines                 | 30.9 ms                                                      | 39.3 ms: 1.27x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.02x slower                                                          |

Benchmark hidden because not significant (3): async_tree_none, async_tree_memoization, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 116 ms                                                       | 193 ms: 1.67x slower                                                  |
| nbody          | 119 ms                                                       | 280 ms: 2.35x slower                                                  |
| Geometric mean | (ref)                                                        | 1.56x slower                                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 4.74 ms                                                      | 4.47 ms: 1.06x faster                                                 |
| regex_dna      | 282 ms                                                       | 295 ms: 1.05x slower                                                  |
| regex_v8       | 32.8 ms                                                      | 35.3 ms: 1.08x slower                                                 |
| regex_compile  | 182 ms                                                       | 293 ms: 1.61x slower                                                  |
| Geometric mean | (ref)                                                        | 1.14x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_parse      | 231 ms                                                       | 201 ms: 1.15x faster                                                  |
| xml_etree_iterparse  | 177 ms                                                       | 159 ms: 1.11x faster                                                  |
| pickle_dict          | 47.2 us                                                      | 44.0 us: 1.07x faster                                                 |
| pickle_list          | 6.86 us                                                      | 6.53 us: 1.05x faster                                                 |
| pickle               | 15.1 us                                                      | 14.5 us: 1.04x faster                                                 |
| unpickle             | 20.5 us                                                      | 22.0 us: 1.07x slower                                                 |
| unpickle_list        | 6.68 us                                                      | 7.76 us: 1.16x slower                                                 |
| json_dumps           | 14.1 ms                                                      | 17.8 ms: 1.26x slower                                                 |
| json_loads           | 34.3 us                                                      | 43.6 us: 1.27x slower                                                 |
| xml_etree_generate   | 122 ms                                                       | 160 ms: 1.31x slower                                                  |
| xml_etree_process    | 85.9 ms                                                      | 126 ms: 1.47x slower                                                  |
| tomli_loads          | 2.78 sec                                                     | 4.22 sec: 1.52x slower                                                |
| unpickle_pure_python | 290 us                                                       | 558 us: 1.92x slower                                                  |
| pickle_pure_python   | 416 us                                                       | 830 us: 1.99x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.21x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 19.5 ms: 1.27x slower                                                 |
| python_startup         | 22.4 ms                                                      | 28.9 ms: 1.29x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.28x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 120 ms: 1.66x slower                                                  |
| genshi_text     | 31.7 ms                                                      | 54.4 ms: 1.72x slower                                                 |
| django_template | 44.3 ms                                                      | 80.6 ms: 1.82x slower                                                 |
| mako            | 15.9 ms                                                      | 29.9 ms: 1.88x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.77x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240727-linux-x86_64-python-04eb5c8db1e24cabd0cb-3.14.0a0-04eb5c8 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| bench_mp_pool              | 18.7 ms                                                      | 13.6 ms: 1.37x faster                                                 |
| gc_traversal               | 5.70 ms                                                      | 4.28 ms: 1.33x faster                                                 |
| async_tree_io_tg           | 1.40 sec                                                     | 1.12 sec: 1.26x faster                                                |
| create_gc_cycles           | 2.41 ms                                                      | 1.95 ms: 1.24x faster                                                 |
| xml_etree_parse            | 231 ms                                                       | 201 ms: 1.15x faster                                                  |
| async_tree_io              | 1.39 sec                                                     | 1.23 sec: 1.13x faster                                                |
| xml_etree_iterparse        | 177 ms                                                       | 159 ms: 1.11x faster                                                  |
| pickle_dict                | 47.2 us                                                      | 44.0 us: 1.07x faster                                                 |
| async_tree_memoization_tg  | 670 ms                                                       | 632 ms: 1.06x faster                                                  |
| regex_effbot               | 4.74 ms                                                      | 4.47 ms: 1.06x faster                                                 |
| pickle_list                | 6.86 us                                                      | 6.53 us: 1.05x faster                                                 |
| async_tree_none_tg         | 504 ms                                                       | 482 ms: 1.04x faster                                                  |
| asyncio_websockets         | 766 ms                                                       | 735 ms: 1.04x faster                                                  |
| pickle                     | 15.1 us                                                      | 14.5 us: 1.04x faster                                                 |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 820 ms: 1.04x faster                                                  |
| regex_dna                  | 282 ms                                                       | 295 ms: 1.05x slower                                                  |
| unpickle                   | 20.5 us                                                      | 22.0 us: 1.07x slower                                                 |
| sqlite_synth               | 3.99 us                                                      | 4.28 us: 1.07x slower                                                 |
| regex_v8                   | 32.8 ms                                                      | 35.3 ms: 1.08x slower                                                 |
| asyncio_tcp                | 948 ms                                                       | 1.02 sec: 1.08x slower                                                |
| pathlib                    | 29.9 ms                                                      | 33.2 ms: 1.11x slower                                                 |
| asyncio_tcp_ssl            | 2.77 sec                                                     | 3.18 sec: 1.14x slower                                                |
| telco                      | 12.2 ms                                                      | 14.1 ms: 1.16x slower                                                 |
| unpickle_list              | 6.68 us                                                      | 7.76 us: 1.16x slower                                                 |
| json                       | 6.51 ms                                                      | 7.69 ms: 1.18x slower                                                 |
| pylint                     | 470 ms                                                       | 562 ms: 1.20x slower                                                  |
| docutils                   | 4.01 sec                                                     | 4.82 sec: 1.20x slower                                                |
| deepcopy                   | 498 us                                                       | 600 us: 1.21x slower                                                  |
| json_dumps                 | 14.1 ms                                                      | 17.8 ms: 1.26x slower                                                 |
| json_loads                 | 34.3 us                                                      | 43.6 us: 1.27x slower                                                 |
| async_generators           | 567 ms                                                       | 723 ms: 1.27x slower                                                  |
| python_startup_no_site     | 15.3 ms                                                      | 19.5 ms: 1.27x slower                                                 |
| coroutines                 | 30.9 ms                                                      | 39.3 ms: 1.27x slower                                                 |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 8.68 ms: 1.29x slower                                                 |
| python_startup             | 22.4 ms                                                      | 28.9 ms: 1.29x slower                                                 |
| xml_etree_generate         | 122 ms                                                       | 160 ms: 1.31x slower                                                  |
| coverage                   | 107 ms                                                       | 141 ms: 1.31x slower                                                  |
| mdp                        | 3.80 sec                                                     | 5.02 sec: 1.32x slower                                                |
| scimark_fft                | 473 ms                                                       | 641 ms: 1.35x slower                                                  |
| tornado_http               | 251 ms                                                       | 342 ms: 1.36x slower                                                  |
| generators                 | 40.0 ms                                                      | 54.8 ms: 1.37x slower                                                 |
| deepcopy_memo              | 50.1 us                                                      | 69.1 us: 1.38x slower                                                 |
| meteor_contest             | 150 ms                                                       | 208 ms: 1.38x slower                                                  |
| pycparser                  | 1.57 sec                                                     | 2.18 sec: 1.38x slower                                                |
| deepcopy_reduce            | 4.10 us                                                      | 5.73 us: 1.40x slower                                                 |
| fannkuch                   | 547 ms                                                       | 772 ms: 1.41x slower                                                  |
| sympy_integrate            | 30.2 ms                                                      | 42.8 ms: 1.41x slower                                                 |
| nqueens                    | 112 ms                                                       | 162 ms: 1.45x slower                                                  |
| 2to3                       | 445 ms                                                       | 647 ms: 1.45x slower                                                  |
| xml_etree_process          | 85.9 ms                                                      | 126 ms: 1.47x slower                                                  |
| bench_thread_pool          | 2.89 ms                                                      | 4.27 ms: 1.48x slower                                                 |
| tomli_loads                | 2.78 sec                                                     | 4.22 sec: 1.52x slower                                                |
| html5lib                   | 92.6 ms                                                      | 141 ms: 1.52x slower                                                  |
| spectral_norm              | 157 ms                                                       | 242 ms: 1.55x slower                                                  |
| thrift                     | 1.10 ms                                                      | 1.70 ms: 1.55x slower                                                 |
| bpe_tokeniser              | 6.28 sec                                                     | 9.90 sec: 1.58x slower                                                |
| crypto_pyaes               | 100 ms                                                       | 159 ms: 1.58x slower                                                  |
| typing_runtime_protocols   | 226 us                                                       | 362 us: 1.60x slower                                                  |
| regex_compile              | 182 ms                                                       | 293 ms: 1.61x slower                                                  |
| pyflate                    | 664 ms                                                       | 1.07 sec: 1.61x slower                                                |
| genshi_xml                 | 72.1 ms                                                      | 120 ms: 1.66x slower                                                  |
| float                      | 116 ms                                                       | 193 ms: 1.67x slower                                                  |
| richards                   | 65.5 ms                                                      | 111 ms: 1.70x slower                                                  |
| richards_super             | 73.2 ms                                                      | 125 ms: 1.71x slower                                                  |
| genshi_text                | 31.7 ms                                                      | 54.4 ms: 1.72x slower                                                 |
| comprehensions             | 22.2 us                                                      | 38.3 us: 1.72x slower                                                 |
| sympy_str                  | 379 ms                                                       | 663 ms: 1.75x slower                                                  |
| pprint_safe_repr           | 987 ms                                                       | 1.73 sec: 1.75x slower                                                |
| sqlglot_normalize          | 140 ms                                                       | 246 ms: 1.76x slower                                                  |
| sqlglot_optimize           | 74.7 ms                                                      | 133 ms: 1.78x slower                                                  |
| pprint_pformat             | 1.94 sec                                                     | 3.48 sec: 1.79x slower                                                |
| django_template            | 44.3 ms                                                      | 80.6 ms: 1.82x slower                                                 |
| logging_simple             | 8.56 us                                                      | 15.9 us: 1.86x slower                                                 |
| mako                       | 15.9 ms                                                      | 29.9 ms: 1.88x slower                                                 |
| scimark_monte_carlo        | 90.6 ms                                                      | 171 ms: 1.88x slower                                                  |
| logging_format             | 9.24 us                                                      | 17.6 us: 1.91x slower                                                 |
| unpickle_pure_python       | 290 us                                                       | 558 us: 1.92x slower                                                  |
| chaos                      | 83.6 ms                                                      | 163 ms: 1.95x slower                                                  |
| scimark_sor                | 179 ms                                                       | 351 ms: 1.96x slower                                                  |
| pickle_pure_python         | 416 us                                                       | 830 us: 1.99x slower                                                  |
| logging_silent             | 130 ns                                                       | 259 ns: 2.00x slower                                                  |
| sqlglot_transpile          | 2.20 ms                                                      | 4.53 ms: 2.06x slower                                                 |
| sympy_expand               | 601 ms                                                       | 1.27 sec: 2.11x slower                                                |
| go                         | 191 ms                                                       | 406 ms: 2.13x slower                                                  |
| scimark_lu                 | 146 ms                                                       | 313 ms: 2.14x slower                                                  |
| sqlglot_parse              | 1.76 ms                                                      | 3.76 ms: 2.14x slower                                                 |
| hexiom                     | 8.11 ms                                                      | 17.4 ms: 2.15x slower                                                 |
| raytrace                   | 344 ms                                                       | 806 ms: 2.34x slower                                                  |
| sympy_sum                  | 210 ms                                                       | 493 ms: 2.35x slower                                                  |
| nbody                      | 119 ms                                                       | 280 ms: 2.35x slower                                                  |
| deltablue                  | 4.44 ms                                                      | 11.7 ms: 2.62x slower                                                 |
| unpack_sequence            | 74.3 ns                                                      | 201 ns: 2.70x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.40x slower                                                          |

Benchmark hidden because not significant (4): pidigits, async_tree_none, async_tree_memoization, async_tree_cpu_io_mixed
Ignored benchmarks (6) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.32x
- 95% likely to have a slowdown of 1.32x
- 99% likely to have a slowdown of 1.28x

# Memory
- memory change: 1.16x