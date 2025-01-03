# Results vs. 3.13.0rc2

- fork: python
- ref: 8eebe4e6d02bb4ad3f1c
- machine: linux-x86_64
- commit hash: 8eebe4e
- commit date: 2025-01-02
- overall geometric mean: 1.148x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250102-linux-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 602 ms: 1.35x slower                                                   |
| docutils       | 4.01 sec                                                     | 4.33 sec: 1.08x slower                                                 |
| html5lib       | 92.6 ms                                                      | 120 ms: 1.30x slower                                                   |
| Geometric mean | (ref)                                                        | 1.24x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250102-linux-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 918 ms: 1.53x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 989 ms: 1.40x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 410 ms: 1.23x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 567 ms: 1.18x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 601 ms: 1.18x faster                                                   |
| async_tree_none            | 572 ms                                                       | 493 ms: 1.16x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 738 ms: 1.15x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 834 ms: 1.07x faster                                                   |
| coroutines                 | 30.9 ms                                                      | 33.0 ms: 1.07x slower                                                  |
| async_generators           | 567 ms                                                       | 642 ms: 1.13x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.14x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250102-linux-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 116 ms                                                       | 142 ms: 1.23x slower                                                   |
| nbody          | 119 ms                                                       | 170 ms: 1.43x slower                                                   |
| Geometric mean | (ref)                                                        | 1.19x slower                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250102-linux-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 4.74 ms                                                      | 4.55 ms: 1.04x faster                                                  |
| regex_dna      | 282 ms                                                       | 293 ms: 1.04x slower                                                   |
| regex_compile  | 182 ms                                                       | 211 ms: 1.16x slower                                                   |
| Geometric mean | (ref)                                                        | 1.04x slower                                                           |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250102-linux-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 128 ms: 1.39x faster                                                   |
| xml_etree_parse      | 231 ms                                                       | 208 ms: 1.11x faster                                                   |
| xml_etree_generate   | 122 ms                                                       | 131 ms: 1.07x slower                                                   |
| json_loads           | 34.3 us                                                      | 39.5 us: 1.15x slower                                                  |
| tomli_loads          | 2.78 sec                                                     | 3.27 sec: 1.17x slower                                                 |
| json_dumps           | 14.1 ms                                                      | 17.1 ms: 1.21x slower                                                  |
| xml_etree_process    | 85.9 ms                                                      | 106 ms: 1.23x slower                                                   |
| unpickle_pure_python | 290 us                                                       | 416 us: 1.43x slower                                                   |
| pickle_pure_python   | 416 us                                                       | 614 us: 1.47x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.13x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250102-linux-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 19.6 ms: 1.28x slower                                                  |
| python_startup         | 22.4 ms                                                      | 30.4 ms: 1.36x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.32x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250102-linux-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 85.7 ms: 1.19x slower                                                  |
| genshi_text     | 31.7 ms                                                      | 42.0 ms: 1.33x slower                                                  |
| django_template | 44.3 ms                                                      | 65.0 ms: 1.47x slower                                                  |
| mako            | 15.9 ms                                                      | 27.2 ms: 1.71x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.41x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250102-linux-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 918 ms: 1.53x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 989 ms: 1.40x faster                                                   |
| xml_etree_iterparse        | 177 ms                                                       | 128 ms: 1.39x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 410 ms: 1.23x faster                                                   |
| deepcopy                   | 498 us                                                       | 414 us: 1.20x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 567 ms: 1.18x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 601 ms: 1.18x faster                                                   |
| async_tree_none            | 572 ms                                                       | 493 ms: 1.16x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 738 ms: 1.15x faster                                                   |
| xml_etree_parse            | 231 ms                                                       | 208 ms: 1.11x faster                                                   |
| sqlite_synth               | 3.99 us                                                      | 3.71 us: 1.07x faster                                                  |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 834 ms: 1.07x faster                                                   |
| telco                      | 12.2 ms                                                      | 11.5 ms: 1.06x faster                                                  |
| regex_effbot               | 4.74 ms                                                      | 4.55 ms: 1.04x faster                                                  |
| regex_dna                  | 282 ms                                                       | 293 ms: 1.04x slower                                                   |
| deepcopy_memo              | 50.1 us                                                      | 52.6 us: 1.05x slower                                                  |
| gc_traversal               | 5.70 ms                                                      | 6.06 ms: 1.06x slower                                                  |
| coroutines                 | 30.9 ms                                                      | 33.0 ms: 1.07x slower                                                  |
| xml_etree_generate         | 122 ms                                                       | 131 ms: 1.07x slower                                                   |
| docutils                   | 4.01 sec                                                     | 4.33 sec: 1.08x slower                                                 |
| deepcopy_reduce            | 4.10 us                                                      | 4.43 us: 1.08x slower                                                  |
| json                       | 6.51 ms                                                      | 7.05 ms: 1.08x slower                                                  |
| scimark_fft                | 473 ms                                                       | 522 ms: 1.10x slower                                                   |
| async_generators           | 567 ms                                                       | 642 ms: 1.13x slower                                                   |
| mdp                        | 3.80 sec                                                     | 4.33 sec: 1.14x slower                                                 |
| json_loads                 | 34.3 us                                                      | 39.5 us: 1.15x slower                                                  |
| nqueens                    | 112 ms                                                       | 129 ms: 1.15x slower                                                   |
| sympy_integrate            | 30.2 ms                                                      | 35.0 ms: 1.16x slower                                                  |
| regex_compile              | 182 ms                                                       | 211 ms: 1.16x slower                                                   |
| sympy_sum                  | 210 ms                                                       | 244 ms: 1.16x slower                                                   |
| thrift                     | 1.10 ms                                                      | 1.29 ms: 1.17x slower                                                  |
| sympy_str                  | 379 ms                                                       | 443 ms: 1.17x slower                                                   |
| pycparser                  | 1.57 sec                                                     | 1.84 sec: 1.17x slower                                                 |
| richards_super             | 73.2 ms                                                      | 85.9 ms: 1.17x slower                                                  |
| tomli_loads                | 2.78 sec                                                     | 3.27 sec: 1.17x slower                                                 |
| meteor_contest             | 150 ms                                                       | 177 ms: 1.18x slower                                                   |
| genshi_xml                 | 72.1 ms                                                      | 85.7 ms: 1.19x slower                                                  |
| sqlglot_optimize           | 74.7 ms                                                      | 89.1 ms: 1.19x slower                                                  |
| sympy_expand               | 601 ms                                                       | 717 ms: 1.19x slower                                                   |
| fannkuch                   | 547 ms                                                       | 654 ms: 1.20x slower                                                   |
| richards                   | 65.5 ms                                                      | 78.8 ms: 1.20x slower                                                  |
| typing_runtime_protocols   | 226 us                                                       | 272 us: 1.21x slower                                                   |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 8.15 ms: 1.21x slower                                                  |
| dulwich_log                | 93.7 ms                                                      | 113 ms: 1.21x slower                                                   |
| sqlglot_normalize          | 140 ms                                                       | 169 ms: 1.21x slower                                                   |
| json_dumps                 | 14.1 ms                                                      | 17.1 ms: 1.21x slower                                                  |
| crypto_pyaes               | 100 ms                                                       | 122 ms: 1.22x slower                                                   |
| float                      | 116 ms                                                       | 142 ms: 1.23x slower                                                   |
| xml_etree_process          | 85.9 ms                                                      | 106 ms: 1.23x slower                                                   |
| bpe_tokeniser              | 6.28 sec                                                     | 7.88 sec: 1.25x slower                                                 |
| pprint_safe_repr           | 987 ms                                                       | 1.24 sec: 1.25x slower                                                 |
| coverage                   | 107 ms                                                       | 137 ms: 1.27x slower                                                   |
| python_startup_no_site     | 15.3 ms                                                      | 19.6 ms: 1.28x slower                                                  |
| html5lib                   | 92.6 ms                                                      | 120 ms: 1.30x slower                                                   |
| pprint_pformat             | 1.94 sec                                                     | 2.56 sec: 1.32x slower                                                 |
| genshi_text                | 31.7 ms                                                      | 42.0 ms: 1.33x slower                                                  |
| scimark_lu                 | 146 ms                                                       | 195 ms: 1.33x slower                                                   |
| 2to3                       | 445 ms                                                       | 602 ms: 1.35x slower                                                   |
| logging_format             | 9.24 us                                                      | 12.5 us: 1.36x slower                                                  |
| python_startup             | 22.4 ms                                                      | 30.4 ms: 1.36x slower                                                  |
| generators                 | 40.0 ms                                                      | 54.5 ms: 1.36x slower                                                  |
| pyflate                    | 664 ms                                                       | 905 ms: 1.36x slower                                                   |
| create_gc_cycles           | 2.41 ms                                                      | 3.32 ms: 1.38x slower                                                  |
| logging_simple             | 8.56 us                                                      | 12.0 us: 1.41x slower                                                  |
| unpickle_pure_python       | 290 us                                                       | 416 us: 1.43x slower                                                   |
| nbody                      | 119 ms                                                       | 170 ms: 1.43x slower                                                   |
| chaos                      | 83.6 ms                                                      | 122 ms: 1.46x slower                                                   |
| django_template            | 44.3 ms                                                      | 65.0 ms: 1.47x slower                                                  |
| pickle_pure_python         | 416 us                                                       | 614 us: 1.47x slower                                                   |
| hexiom                     | 8.11 ms                                                      | 12.0 ms: 1.48x slower                                                  |
| bench_thread_pool          | 2.89 ms                                                      | 4.33 ms: 1.50x slower                                                  |
| go                         | 191 ms                                                       | 288 ms: 1.50x slower                                                   |
| comprehensions             | 22.2 us                                                      | 33.6 us: 1.51x slower                                                  |
| scimark_monte_carlo        | 90.6 ms                                                      | 138 ms: 1.52x slower                                                   |
| scimark_sor                | 179 ms                                                       | 275 ms: 1.54x slower                                                   |
| sqlglot_transpile          | 2.20 ms                                                      | 3.43 ms: 1.56x slower                                                  |
| raytrace                   | 344 ms                                                       | 584 ms: 1.70x slower                                                   |
| mako                       | 15.9 ms                                                      | 27.2 ms: 1.71x slower                                                  |
| sqlglot_parse              | 1.76 ms                                                      | 3.03 ms: 1.72x slower                                                  |
| logging_silent             | 130 ns                                                       | 230 ns: 1.77x slower                                                   |
| deltablue                  | 4.44 ms                                                      | 10.4 ms: 2.35x slower                                                  |
| bench_mp_pool              | 18.7 ms                                                      | 94.2 ms: 5.04x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.20x slower                                                           |

Benchmark hidden because not significant (6): pidigits, asyncio_websockets, regex_v8, pathlib, pylint, spectral_norm
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250102-3.14.0a3+-8eebe4e-NOGIL/bm-20250102-linux-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.148x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.14x
- 95% likely to have a slowdown of 1.13x
- 99% likely to have a slowdown of 1.11x

# Memory
- memory change: 1.33x