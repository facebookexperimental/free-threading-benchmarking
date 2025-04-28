# Results vs. 3.13.0rc2

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 336322b
- commit date: 2025-04-28
- overall geometric mean: 1.056x faster
- HPT reliability: 57.61%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250428-linux-x86_64-python-main-3.14.0a7+-336322b |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 404 ms: 1.10x faster                                   |
| docutils       | 4.01 sec                                                     | 3.87 sec: 1.04x faster                                 |
| html5lib       | 92.6 ms                                                      | 85.7 ms: 1.08x faster                                  |
| Geometric mean | (ref)                                                        | 1.07x faster                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250428-linux-x86_64-python-main-3.14.0a7+-336322b |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 670 ms: 2.09x faster                                   |
| async_tree_io              | 1.39 sec                                                     | 723 ms: 1.92x faster                                   |
| async_tree_none_tg         | 504 ms                                                       | 294 ms: 1.72x faster                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 395 ms: 1.70x faster                                   |
| async_tree_none            | 572 ms                                                       | 342 ms: 1.67x faster                                   |
| async_tree_memoization     | 709 ms                                                       | 440 ms: 1.61x faster                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 578 ms: 1.47x faster                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 629 ms: 1.41x faster                                   |
| asyncio_websockets         | 766 ms                                                       | 689 ms: 1.11x faster                                   |
| async_generators           | 567 ms                                                       | 538 ms: 1.05x faster                                   |
| Geometric mean             | (ref)                                                        | 1.49x faster                                           |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250428-linux-x86_64-python-main-3.14.0a7+-336322b |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------:|
| float          | 116 ms                                                       | 91.2 ms: 1.27x faster                                  |
| pidigits       | 251 ms                                                       | 225 ms: 1.12x faster                                   |
| nbody          | 119 ms                                                       | 150 ms: 1.26x slower                                   |
| Geometric mean | (ref)                                                        | 1.04x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250428-linux-x86_64-python-main-3.14.0a7+-336322b |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------:|
| regex_effbot   | 4.74 ms                                                      | 3.77 ms: 1.26x faster                                  |
| regex_v8       | 32.8 ms                                                      | 26.3 ms: 1.25x faster                                  |
| regex_dna      | 282 ms                                                       | 248 ms: 1.14x faster                                   |
| Geometric mean | (ref)                                                        | 1.16x faster                                           |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250428-linux-x86_64-python-main-3.14.0a7+-336322b |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 125 ms: 1.42x faster                                   |
| xml_etree_parse      | 231 ms                                                       | 187 ms: 1.23x faster                                   |
| unpickle_pure_python | 290 us                                                       | 297 us: 1.02x slower                                   |
| xml_etree_generate   | 122 ms                                                       | 131 ms: 1.07x slower                                   |
| xml_etree_process    | 85.9 ms                                                      | 91.7 ms: 1.07x slower                                  |
| pickle_pure_python   | 416 us                                                       | 447 us: 1.07x slower                                   |
| json_loads           | 34.3 us                                                      | 41.0 us: 1.20x slower                                  |
| json_dumps           | 14.1 ms                                                      | 17.0 ms: 1.20x slower                                  |
| Geometric mean       | (ref)                                                        | 1.00x slower                                           |

Benchmark hidden because not significant (1): tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250428-linux-x86_64-python-main-3.14.0a7+-336322b |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 14.8 ms: 1.03x faster                                  |
| python_startup         | 22.4 ms                                                      | 24.0 ms: 1.07x slower                                  |
| Geometric mean         | (ref)                                                        | 1.02x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250428-linux-x86_64-python-main-3.14.0a7+-336322b |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 76.1 ms: 1.06x slower                                  |
| genshi_text     | 31.7 ms                                                      | 34.1 ms: 1.08x slower                                  |
| django_template | 44.3 ms                                                      | 48.8 ms: 1.10x slower                                  |
| mako            | 15.9 ms                                                      | 22.4 ms: 1.40x slower                                  |
| Geometric mean  | (ref)                                                        | 1.15x slower                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250428-linux-x86_64-python-main-3.14.0a7+-336322b |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 670 ms: 2.09x faster                                   |
| async_tree_io              | 1.39 sec                                                     | 723 ms: 1.92x faster                                   |
| async_tree_none_tg         | 504 ms                                                       | 294 ms: 1.72x faster                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 395 ms: 1.70x faster                                   |
| async_tree_none            | 572 ms                                                       | 342 ms: 1.67x faster                                   |
| mdp                        | 3.80 sec                                                     | 2.29 sec: 1.66x faster                                 |
| async_tree_memoization     | 709 ms                                                       | 440 ms: 1.61x faster                                   |
| gc_traversal               | 5.70 ms                                                      | 3.58 ms: 1.59x faster                                  |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 578 ms: 1.47x faster                                   |
| xml_etree_iterparse        | 177 ms                                                       | 125 ms: 1.42x faster                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 629 ms: 1.41x faster                                   |
| sqlite_synth               | 3.99 us                                                      | 2.95 us: 1.35x faster                                  |
| deepcopy                   | 498 us                                                       | 377 us: 1.32x faster                                   |
| float                      | 116 ms                                                       | 91.2 ms: 1.27x faster                                  |
| regex_effbot               | 4.74 ms                                                      | 3.77 ms: 1.26x faster                                  |
| regex_v8                   | 32.8 ms                                                      | 26.3 ms: 1.25x faster                                  |
| xml_etree_parse            | 231 ms                                                       | 187 ms: 1.23x faster                                   |
| dulwich_log                | 93.7 ms                                                      | 79.8 ms: 1.17x faster                                  |
| telco                      | 12.2 ms                                                      | 10.5 ms: 1.16x faster                                  |
| bench_thread_pool          | 2.89 ms                                                      | 2.50 ms: 1.15x faster                                  |
| go                         | 191 ms                                                       | 166 ms: 1.15x faster                                   |
| regex_dna                  | 282 ms                                                       | 248 ms: 1.14x faster                                   |
| scimark_sor                | 179 ms                                                       | 158 ms: 1.13x faster                                   |
| pidigits                   | 251 ms                                                       | 225 ms: 1.12x faster                                   |
| asyncio_websockets         | 766 ms                                                       | 689 ms: 1.11x faster                                   |
| pathlib                    | 29.9 ms                                                      | 27.1 ms: 1.11x faster                                  |
| 2to3                       | 445 ms                                                       | 404 ms: 1.10x faster                                   |
| spectral_norm              | 157 ms                                                       | 143 ms: 1.10x faster                                   |
| deepcopy_memo              | 50.1 us                                                      | 45.8 us: 1.09x faster                                  |
| pylint                     | 470 ms                                                       | 433 ms: 1.08x faster                                   |
| html5lib                   | 92.6 ms                                                      | 85.7 ms: 1.08x faster                                  |
| pycparser                  | 1.57 sec                                                     | 1.46 sec: 1.07x faster                                 |
| async_generators           | 567 ms                                                       | 538 ms: 1.05x faster                                   |
| deepcopy_reduce            | 4.10 us                                                      | 3.94 us: 1.04x faster                                  |
| docutils                   | 4.01 sec                                                     | 3.87 sec: 1.04x faster                                 |
| python_startup_no_site     | 15.3 ms                                                      | 14.8 ms: 1.03x faster                                  |
| scimark_fft                | 473 ms                                                       | 463 ms: 1.02x faster                                   |
| unpickle_pure_python       | 290 us                                                       | 297 us: 1.02x slower                                   |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 7.06 ms: 1.04x slower                                  |
| richards_super             | 73.2 ms                                                      | 76.8 ms: 1.05x slower                                  |
| genshi_xml                 | 72.1 ms                                                      | 76.1 ms: 1.06x slower                                  |
| sympy_str                  | 379 ms                                                       | 401 ms: 1.06x slower                                   |
| sympy_sum                  | 210 ms                                                       | 223 ms: 1.06x slower                                   |
| pprint_safe_repr           | 987 ms                                                       | 1.05 sec: 1.06x slower                                 |
| deltablue                  | 4.44 ms                                                      | 4.72 ms: 1.06x slower                                  |
| meteor_contest             | 150 ms                                                       | 160 ms: 1.07x slower                                   |
| logging_format             | 9.24 us                                                      | 9.85 us: 1.07x slower                                  |
| xml_etree_generate         | 122 ms                                                       | 131 ms: 1.07x slower                                   |
| xml_etree_process          | 85.9 ms                                                      | 91.7 ms: 1.07x slower                                  |
| python_startup             | 22.4 ms                                                      | 24.0 ms: 1.07x slower                                  |
| pickle_pure_python         | 416 us                                                       | 447 us: 1.07x slower                                   |
| logging_silent             | 130 ns                                                       | 140 ns: 1.08x slower                                   |
| genshi_text                | 31.7 ms                                                      | 34.1 ms: 1.08x slower                                  |
| pprint_pformat             | 1.94 sec                                                     | 2.10 sec: 1.08x slower                                 |
| scimark_monte_carlo        | 90.6 ms                                                      | 98.1 ms: 1.08x slower                                  |
| hexiom                     | 8.11 ms                                                      | 8.84 ms: 1.09x slower                                  |
| typing_runtime_protocols   | 226 us                                                       | 246 us: 1.09x slower                                   |
| json                       | 6.51 ms                                                      | 7.13 ms: 1.09x slower                                  |
| sympy_expand               | 601 ms                                                       | 658 ms: 1.09x slower                                   |
| fannkuch                   | 547 ms                                                       | 601 ms: 1.10x slower                                   |
| django_template            | 44.3 ms                                                      | 48.8 ms: 1.10x slower                                  |
| raytrace                   | 344 ms                                                       | 381 ms: 1.11x slower                                   |
| crypto_pyaes               | 100 ms                                                       | 111 ms: 1.11x slower                                   |
| generators                 | 40.0 ms                                                      | 44.4 ms: 1.11x slower                                  |
| comprehensions             | 22.2 us                                                      | 25.3 us: 1.14x slower                                  |
| scimark_lu                 | 146 ms                                                       | 168 ms: 1.15x slower                                   |
| bpe_tokeniser              | 6.28 sec                                                     | 7.29 sec: 1.16x slower                                 |
| json_loads                 | 34.3 us                                                      | 41.0 us: 1.20x slower                                  |
| json_dumps                 | 14.1 ms                                                      | 17.0 ms: 1.20x slower                                  |
| nbody                      | 119 ms                                                       | 150 ms: 1.26x slower                                   |
| coverage                   | 107 ms                                                       | 143 ms: 1.33x slower                                   |
| mako                       | 15.9 ms                                                      | 22.4 ms: 1.40x slower                                  |
| bench_mp_pool              | 18.7 ms                                                      | 75.4 ms: 4.04x slower                                  |
| Geometric mean             | (ref)                                                        | 1.05x faster                                           |

Benchmark hidden because not significant (11): chaos, coroutines, create_gc_cycles, regex_compile, thrift, sympy_integrate, tomli_loads, pyflate, nqueens, richards, logging_simple
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250428-3.14.0a7+-336322b-NOGIL/bm-20250428-linux-x86_64-python-main-3.14.0a7+-336322b.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.056x faster

# HPT report

- Reliability score: 57.61% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.35x