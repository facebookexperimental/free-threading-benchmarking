# Results vs. 3.13.0rc2

- fork: python
- ref: 0ac40acec045c4ce780c
- machine: linux-x86_64
- commit hash: 0ac40ac
- commit date: 2024-12-14
- overall geometric mean: 1.185x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.15x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 577 ms: 1.30x slower                                                   |
| docutils       | 4.01 sec                                                     | 4.38 sec: 1.09x slower                                                 |
| html5lib       | 92.6 ms                                                      | 120 ms: 1.30x slower                                                   |
| Geometric mean | (ref)                                                        | 1.22x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 1.01 sec: 1.39x faster                                                 |
| async_tree_io              | 1.39 sec                                                     | 1.08 sec: 1.29x faster                                                 |
| async_tree_memoization_tg  | 670 ms                                                       | 585 ms: 1.15x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 451 ms: 1.12x faster                                                   |
| async_tree_none            | 572 ms                                                       | 513 ms: 1.12x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 772 ms: 1.10x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 644 ms: 1.10x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 850 ms: 1.04x faster                                                   |
| asyncio_websockets         | 766 ms                                                       | 735 ms: 1.04x faster                                                   |
| coroutines                 | 30.9 ms                                                      | 35.3 ms: 1.14x slower                                                  |
| async_generators           | 567 ms                                                       | 659 ms: 1.16x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.09x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 251 ms                                                       | 238 ms: 1.05x faster                                                   |
| nbody          | 119 ms                                                       | 167 ms: 1.41x slower                                                   |
| float          | 116 ms                                                       | 168 ms: 1.45x slower                                                   |
| Geometric mean | (ref)                                                        | 1.25x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 4.74 ms                                                      | 4.51 ms: 1.05x faster                                                  |
| regex_dna      | 282 ms                                                       | 290 ms: 1.03x slower                                                   |
| regex_compile  | 182 ms                                                       | 235 ms: 1.29x slower                                                   |
| Geometric mean | (ref)                                                        | 1.06x slower                                                           |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 137 ms: 1.29x faster                                                   |
| xml_etree_parse      | 231 ms                                                       | 204 ms: 1.13x faster                                                   |
| json_loads           | 34.3 us                                                      | 35.7 us: 1.04x slower                                                  |
| xml_etree_generate   | 122 ms                                                       | 135 ms: 1.10x slower                                                   |
| tomli_loads          | 2.78 sec                                                     | 3.36 sec: 1.21x slower                                                 |
| xml_etree_process    | 85.9 ms                                                      | 104 ms: 1.21x slower                                                   |
| json_dumps           | 14.1 ms                                                      | 17.3 ms: 1.22x slower                                                  |
| unpickle_pure_python | 290 us                                                       | 411 us: 1.42x slower                                                   |
| pickle_pure_python   | 416 us                                                       | 615 us: 1.48x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.13x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 19.4 ms: 1.26x slower                                                  |
| python_startup         | 22.4 ms                                                      | 31.5 ms: 1.41x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.33x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 89.0 ms: 1.24x slower                                                  |
| genshi_text     | 31.7 ms                                                      | 41.0 ms: 1.29x slower                                                  |
| django_template | 44.3 ms                                                      | 61.0 ms: 1.38x slower                                                  |
| mako            | 15.9 ms                                                      | 26.3 ms: 1.65x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.38x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 1.01 sec: 1.39x faster                                                 |
| xml_etree_iterparse        | 177 ms                                                       | 137 ms: 1.29x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 1.08 sec: 1.29x faster                                                 |
| deepcopy                   | 498 us                                                       | 408 us: 1.22x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 585 ms: 1.15x faster                                                   |
| xml_etree_parse            | 231 ms                                                       | 204 ms: 1.13x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 451 ms: 1.12x faster                                                   |
| async_tree_none            | 572 ms                                                       | 513 ms: 1.12x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 772 ms: 1.10x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 644 ms: 1.10x faster                                                   |
| sqlite_synth               | 3.99 us                                                      | 3.66 us: 1.09x faster                                                  |
| pidigits                   | 251 ms                                                       | 238 ms: 1.05x faster                                                   |
| regex_effbot               | 4.74 ms                                                      | 4.51 ms: 1.05x faster                                                  |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 850 ms: 1.04x faster                                                   |
| asyncio_websockets         | 766 ms                                                       | 735 ms: 1.04x faster                                                   |
| regex_dna                  | 282 ms                                                       | 290 ms: 1.03x slower                                                   |
| json_loads                 | 34.3 us                                                      | 35.7 us: 1.04x slower                                                  |
| json                       | 6.51 ms                                                      | 6.83 ms: 1.05x slower                                                  |
| deepcopy_reduce            | 4.10 us                                                      | 4.30 us: 1.05x slower                                                  |
| pathlib                    | 29.9 ms                                                      | 31.7 ms: 1.06x slower                                                  |
| docutils                   | 4.01 sec                                                     | 4.38 sec: 1.09x slower                                                 |
| xml_etree_generate         | 122 ms                                                       | 135 ms: 1.10x slower                                                   |
| coroutines                 | 30.9 ms                                                      | 35.3 ms: 1.14x slower                                                  |
| meteor_contest             | 150 ms                                                       | 173 ms: 1.15x slower                                                   |
| nqueens                    | 112 ms                                                       | 130 ms: 1.16x slower                                                   |
| mdp                        | 3.80 sec                                                     | 4.41 sec: 1.16x slower                                                 |
| scimark_fft                | 473 ms                                                       | 550 ms: 1.16x slower                                                   |
| async_generators           | 567 ms                                                       | 659 ms: 1.16x slower                                                   |
| bpe_tokeniser              | 6.28 sec                                                     | 7.46 sec: 1.19x slower                                                 |
| gc_traversal               | 5.70 ms                                                      | 6.80 ms: 1.19x slower                                                  |
| fannkuch                   | 547 ms                                                       | 653 ms: 1.19x slower                                                   |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 8.07 ms: 1.19x slower                                                  |
| tomli_loads                | 2.78 sec                                                     | 3.36 sec: 1.21x slower                                                 |
| sqlglot_normalize          | 140 ms                                                       | 169 ms: 1.21x slower                                                   |
| typing_runtime_protocols   | 226 us                                                       | 274 us: 1.21x slower                                                   |
| xml_etree_process          | 85.9 ms                                                      | 104 ms: 1.21x slower                                                   |
| sqlglot_optimize           | 74.7 ms                                                      | 90.9 ms: 1.22x slower                                                  |
| json_dumps                 | 14.1 ms                                                      | 17.3 ms: 1.22x slower                                                  |
| pycparser                  | 1.57 sec                                                     | 1.93 sec: 1.23x slower                                                 |
| crypto_pyaes               | 100 ms                                                       | 123 ms: 1.23x slower                                                   |
| genshi_xml                 | 72.1 ms                                                      | 89.0 ms: 1.24x slower                                                  |
| dulwich_log                | 93.7 ms                                                      | 117 ms: 1.25x slower                                                   |
| python_startup_no_site     | 15.3 ms                                                      | 19.4 ms: 1.26x slower                                                  |
| regex_compile              | 182 ms                                                       | 235 ms: 1.29x slower                                                   |
| genshi_text                | 31.7 ms                                                      | 41.0 ms: 1.29x slower                                                  |
| 2to3                       | 445 ms                                                       | 577 ms: 1.30x slower                                                   |
| html5lib                   | 92.6 ms                                                      | 120 ms: 1.30x slower                                                   |
| sympy_integrate            | 30.2 ms                                                      | 39.4 ms: 1.30x slower                                                  |
| thrift                     | 1.10 ms                                                      | 1.43 ms: 1.30x slower                                                  |
| bench_thread_pool          | 2.89 ms                                                      | 3.76 ms: 1.30x slower                                                  |
| coverage                   | 107 ms                                                       | 141 ms: 1.31x slower                                                   |
| generators                 | 40.0 ms                                                      | 52.5 ms: 1.31x slower                                                  |
| pprint_safe_repr           | 987 ms                                                       | 1.30 sec: 1.31x slower                                                 |
| create_gc_cycles           | 2.41 ms                                                      | 3.28 ms: 1.36x slower                                                  |
| django_template            | 44.3 ms                                                      | 61.0 ms: 1.38x slower                                                  |
| pprint_pformat             | 1.94 sec                                                     | 2.71 sec: 1.39x slower                                                 |
| nbody                      | 119 ms                                                       | 167 ms: 1.41x slower                                                   |
| python_startup             | 22.4 ms                                                      | 31.5 ms: 1.41x slower                                                  |
| logging_simple             | 8.56 us                                                      | 12.1 us: 1.41x slower                                                  |
| pyflate                    | 664 ms                                                       | 939 ms: 1.42x slower                                                   |
| unpickle_pure_python       | 290 us                                                       | 411 us: 1.42x slower                                                   |
| richards_super             | 73.2 ms                                                      | 106 ms: 1.45x slower                                                   |
| float                      | 116 ms                                                       | 168 ms: 1.45x slower                                                   |
| chaos                      | 83.6 ms                                                      | 123 ms: 1.47x slower                                                   |
| richards                   | 65.5 ms                                                      | 96.2 ms: 1.47x slower                                                  |
| logging_format             | 9.24 us                                                      | 13.6 us: 1.47x slower                                                  |
| pickle_pure_python         | 416 us                                                       | 615 us: 1.48x slower                                                   |
| comprehensions             | 22.2 us                                                      | 34.7 us: 1.56x slower                                                  |
| hexiom                     | 8.11 ms                                                      | 12.7 ms: 1.57x slower                                                  |
| sympy_str                  | 379 ms                                                       | 600 ms: 1.58x slower                                                   |
| go                         | 191 ms                                                       | 303 ms: 1.59x slower                                                   |
| scimark_lu                 | 146 ms                                                       | 232 ms: 1.59x slower                                                   |
| scimark_sor                | 179 ms                                                       | 291 ms: 1.63x slower                                                   |
| mako                       | 15.9 ms                                                      | 26.3 ms: 1.65x slower                                                  |
| scimark_monte_carlo        | 90.6 ms                                                      | 151 ms: 1.67x slower                                                   |
| logging_silent             | 130 ns                                                       | 220 ns: 1.69x slower                                                   |
| sqlglot_transpile          | 2.20 ms                                                      | 3.81 ms: 1.73x slower                                                  |
| sqlglot_parse              | 1.76 ms                                                      | 3.05 ms: 1.74x slower                                                  |
| raytrace                   | 344 ms                                                       | 620 ms: 1.80x slower                                                   |
| sympy_expand               | 601 ms                                                       | 1.11 sec: 1.85x slower                                                 |
| sympy_sum                  | 210 ms                                                       | 424 ms: 2.02x slower                                                   |
| deltablue                  | 4.44 ms                                                      | 11.3 ms: 2.54x slower                                                  |
| bench_mp_pool              | 18.7 ms                                                      | 90.5 ms: 4.84x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.25x slower                                                           |

Benchmark hidden because not significant (5): regex_v8, telco, deepcopy_memo, spectral_norm, pylint
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241214-3.14.0a2+-0ac40ac-NOGIL/bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.185x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.17x
- 95% likely to have a slowdown of 1.16x
- 99% likely to have a slowdown of 1.15x

# Memory
- memory change: 1.33x