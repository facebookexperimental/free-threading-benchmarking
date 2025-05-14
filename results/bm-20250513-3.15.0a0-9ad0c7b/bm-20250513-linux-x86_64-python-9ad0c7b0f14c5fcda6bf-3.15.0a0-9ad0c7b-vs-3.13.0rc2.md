# Results vs. 3.13.0rc2

- fork: python
- ref: 9ad0c7b0f14c5fcda6bf
- machine: linux-x86_64
- commit hash: 9ad0c7b
- commit date: 2025-05-13
- overall geometric mean: 1.163x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.09x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 338 ms: 1.32x faster                                                  |
| docutils       | 4.01 sec                                                     | 3.39 sec: 1.18x faster                                                |
| html5lib       | 92.6 ms                                                      | 76.2 ms: 1.22x faster                                                 |
| Geometric mean | (ref)                                                        | 1.24x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io              | 1.39 sec                                                     | 801 ms: 1.73x faster                                                  |
| async_tree_memoization     | 709 ms                                                       | 412 ms: 1.72x faster                                                  |
| async_tree_io_tg           | 1.40 sec                                                     | 841 ms: 1.67x faster                                                  |
| async_tree_none            | 572 ms                                                       | 347 ms: 1.65x faster                                                  |
| async_tree_memoization_tg  | 670 ms                                                       | 416 ms: 1.61x faster                                                  |
| async_tree_none_tg         | 504 ms                                                       | 331 ms: 1.52x faster                                                  |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 618 ms: 1.44x faster                                                  |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 620 ms: 1.37x faster                                                  |
| asyncio_websockets         | 766 ms                                                       | 649 ms: 1.18x faster                                                  |
| async_generators           | 567 ms                                                       | 512 ms: 1.11x faster                                                  |
| Geometric mean             | (ref)                                                        | 1.44x faster                                                          |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 116 ms                                                       | 97.2 ms: 1.19x faster                                                 |
| pidigits       | 251 ms                                                       | 232 ms: 1.08x faster                                                  |
| nbody          | 119 ms                                                       | 123 ms: 1.04x slower                                                  |
| Geometric mean | (ref)                                                        | 1.08x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 4.74 ms                                                      | 3.74 ms: 1.27x faster                                                 |
| regex_compile  | 182 ms                                                       | 153 ms: 1.19x faster                                                  |
| regex_dna      | 282 ms                                                       | 237 ms: 1.19x faster                                                  |
| regex_v8       | 32.8 ms                                                      | 27.7 ms: 1.18x faster                                                 |
| Geometric mean | (ref)                                                        | 1.21x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 125 ms: 1.42x faster                                                  |
| xml_etree_parse      | 231 ms                                                       | 175 ms: 1.32x faster                                                  |
| xml_etree_process    | 85.9 ms                                                      | 75.2 ms: 1.14x faster                                                 |
| xml_etree_generate   | 122 ms                                                       | 110 ms: 1.12x faster                                                  |
| tomli_loads          | 2.78 sec                                                     | 2.50 sec: 1.11x faster                                                |
| unpickle_pure_python | 290 us                                                       | 269 us: 1.08x faster                                                  |
| pickle_pure_python   | 416 us                                                       | 390 us: 1.07x faster                                                  |
| json_dumps           | 14.1 ms                                                      | 13.8 ms: 1.03x faster                                                 |
| json_loads           | 34.3 us                                                      | 37.8 us: 1.10x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.12x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 10.4 ms: 1.47x faster                                                 |
| python_startup         | 22.4 ms                                                      | 17.6 ms: 1.27x faster                                                 |
| Geometric mean         | (ref)                                                        | 1.37x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 31.7 ms                                                      | 26.4 ms: 1.20x faster                                                 |
| genshi_xml      | 72.1 ms                                                      | 62.0 ms: 1.16x faster                                                 |
| django_template | 44.3 ms                                                      | 43.2 ms: 1.03x faster                                                 |
| Geometric mean  | (ref)                                                        | 1.09x faster                                                          |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 3.80 sec                                                     | 1.74 sec: 2.18x faster                                                |
| async_tree_io              | 1.39 sec                                                     | 801 ms: 1.73x faster                                                  |
| async_tree_memoization     | 709 ms                                                       | 412 ms: 1.72x faster                                                  |
| async_tree_io_tg           | 1.40 sec                                                     | 841 ms: 1.67x faster                                                  |
| async_tree_none            | 572 ms                                                       | 347 ms: 1.65x faster                                                  |
| bench_thread_pool          | 2.89 ms                                                      | 1.79 ms: 1.62x faster                                                 |
| async_tree_memoization_tg  | 670 ms                                                       | 416 ms: 1.61x faster                                                  |
| deepcopy                   | 498 us                                                       | 326 us: 1.53x faster                                                  |
| async_tree_none_tg         | 504 ms                                                       | 331 ms: 1.52x faster                                                  |
| python_startup_no_site     | 15.3 ms                                                      | 10.4 ms: 1.47x faster                                                 |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 618 ms: 1.44x faster                                                  |
| xml_etree_iterparse        | 177 ms                                                       | 125 ms: 1.42x faster                                                  |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 620 ms: 1.37x faster                                                  |
| go                         | 191 ms                                                       | 142 ms: 1.34x faster                                                  |
| deepcopy_memo              | 50.1 us                                                      | 37.4 us: 1.34x faster                                                 |
| xml_etree_parse            | 231 ms                                                       | 175 ms: 1.32x faster                                                  |
| 2to3                       | 445 ms                                                       | 338 ms: 1.32x faster                                                  |
| sympy_integrate            | 30.2 ms                                                      | 23.4 ms: 1.29x faster                                                 |
| telco                      | 12.2 ms                                                      | 9.45 ms: 1.29x faster                                                 |
| pylint                     | 470 ms                                                       | 365 ms: 1.29x faster                                                  |
| python_startup             | 22.4 ms                                                      | 17.6 ms: 1.27x faster                                                 |
| regex_effbot               | 4.74 ms                                                      | 3.74 ms: 1.27x faster                                                 |
| dulwich_log                | 93.7 ms                                                      | 74.3 ms: 1.26x faster                                                 |
| pathlib                    | 29.9 ms                                                      | 24.0 ms: 1.24x faster                                                 |
| sqlite_synth               | 3.99 us                                                      | 3.22 us: 1.24x faster                                                 |
| html5lib                   | 92.6 ms                                                      | 76.2 ms: 1.22x faster                                                 |
| richards                   | 65.5 ms                                                      | 54.0 ms: 1.21x faster                                                 |
| deepcopy_reduce            | 4.10 us                                                      | 3.40 us: 1.21x faster                                                 |
| scimark_sor                | 179 ms                                                       | 149 ms: 1.20x faster                                                  |
| genshi_text                | 31.7 ms                                                      | 26.4 ms: 1.20x faster                                                 |
| spectral_norm              | 157 ms                                                       | 131 ms: 1.19x faster                                                  |
| float                      | 116 ms                                                       | 97.2 ms: 1.19x faster                                                 |
| regex_compile              | 182 ms                                                       | 153 ms: 1.19x faster                                                  |
| regex_dna                  | 282 ms                                                       | 237 ms: 1.19x faster                                                  |
| pyflate                    | 664 ms                                                       | 559 ms: 1.19x faster                                                  |
| docutils                   | 4.01 sec                                                     | 3.39 sec: 1.18x faster                                                |
| regex_v8                   | 32.8 ms                                                      | 27.7 ms: 1.18x faster                                                 |
| asyncio_websockets         | 766 ms                                                       | 649 ms: 1.18x faster                                                  |
| richards_super             | 73.2 ms                                                      | 62.3 ms: 1.18x faster                                                 |
| sympy_str                  | 379 ms                                                       | 325 ms: 1.17x faster                                                  |
| thrift                     | 1.10 ms                                                      | 946 us: 1.16x faster                                                  |
| genshi_xml                 | 72.1 ms                                                      | 62.0 ms: 1.16x faster                                                 |
| meteor_contest             | 150 ms                                                       | 129 ms: 1.16x faster                                                  |
| sympy_sum                  | 210 ms                                                       | 183 ms: 1.15x faster                                                  |
| typing_runtime_protocols   | 226 us                                                       | 197 us: 1.15x faster                                                  |
| xml_etree_process          | 85.9 ms                                                      | 75.2 ms: 1.14x faster                                                 |
| bpe_tokeniser              | 6.28 sec                                                     | 5.52 sec: 1.14x faster                                                |
| chaos                      | 83.6 ms                                                      | 74.2 ms: 1.13x faster                                                 |
| nqueens                    | 112 ms                                                       | 99.3 ms: 1.13x faster                                                 |
| xml_etree_generate         | 122 ms                                                       | 110 ms: 1.12x faster                                                  |
| tomli_loads                | 2.78 sec                                                     | 2.50 sec: 1.11x faster                                                |
| async_generators           | 567 ms                                                       | 512 ms: 1.11x faster                                                  |
| sympy_expand               | 601 ms                                                       | 550 ms: 1.09x faster                                                  |
| pprint_safe_repr           | 987 ms                                                       | 909 ms: 1.09x faster                                                  |
| crypto_pyaes               | 100 ms                                                       | 92.3 ms: 1.08x faster                                                 |
| pidigits                   | 251 ms                                                       | 232 ms: 1.08x faster                                                  |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 6.25 ms: 1.08x faster                                                 |
| pycparser                  | 1.57 sec                                                     | 1.45 sec: 1.08x faster                                                |
| unpickle_pure_python       | 290 us                                                       | 269 us: 1.08x faster                                                  |
| scimark_monte_carlo        | 90.6 ms                                                      | 83.9 ms: 1.08x faster                                                 |
| pickle_pure_python         | 416 us                                                       | 390 us: 1.07x faster                                                  |
| hexiom                     | 8.11 ms                                                      | 7.59 ms: 1.07x faster                                                 |
| fannkuch                   | 547 ms                                                       | 512 ms: 1.07x faster                                                  |
| pprint_pformat             | 1.94 sec                                                     | 1.85 sec: 1.05x faster                                                |
| logging_simple             | 8.56 us                                                      | 8.20 us: 1.04x faster                                                 |
| comprehensions             | 22.2 us                                                      | 21.4 us: 1.04x faster                                                 |
| scimark_fft                | 473 ms                                                       | 456 ms: 1.04x faster                                                  |
| coverage                   | 107 ms                                                       | 105 ms: 1.03x faster                                                  |
| raytrace                   | 344 ms                                                       | 336 ms: 1.03x faster                                                  |
| django_template            | 44.3 ms                                                      | 43.2 ms: 1.03x faster                                                 |
| json_dumps                 | 14.1 ms                                                      | 13.8 ms: 1.03x faster                                                 |
| nbody                      | 119 ms                                                       | 123 ms: 1.04x slower                                                  |
| json                       | 6.51 ms                                                      | 6.97 ms: 1.07x slower                                                 |
| json_loads                 | 34.3 us                                                      | 37.8 us: 1.10x slower                                                 |
| gc_traversal               | 5.70 ms                                                      | 6.39 ms: 1.12x slower                                                 |
| create_gc_cycles           | 2.41 ms                                                      | 3.16 ms: 1.31x slower                                                 |
| bench_mp_pool              | 18.7 ms                                                      | 80.3 ms: 4.30x slower                                                 |
| logging_silent             | 130 ns                                                       | 615 ns: 4.73x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.14x faster                                                          |

Benchmark hidden because not significant (6): deltablue, coroutines, logging_format, generators, scimark_lu, mako
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250513-3.15.0a0-9ad0c7b/bm-20250513-linux-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.163x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.11x
- 95% likely to have a speedup of 1.10x
- 99% likely to have a speedup of 1.09x

# Memory
- memory change: 1.16x