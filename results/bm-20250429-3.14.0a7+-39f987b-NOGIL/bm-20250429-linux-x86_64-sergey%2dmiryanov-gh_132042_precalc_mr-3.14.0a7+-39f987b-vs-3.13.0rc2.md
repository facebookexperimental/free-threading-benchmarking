# Results vs. 3.13.0rc2

- fork: sergey-miryanov
- ref: gh_132042_precalc_mr
- machine: linux-x86_64
- commit hash: 39f987b
- commit date: 2025-04-29
- overall geometric mean: 1.037x faster
- HPT reliability: 50.19%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 425 ms: 1.05x faster                                                              |
| docutils       | 4.01 sec                                                     | 3.92 sec: 1.02x faster                                                            |
| html5lib       | 92.6 ms                                                      | 83.2 ms: 1.11x faster                                                             |
| Geometric mean | (ref)                                                        | 1.06x faster                                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 708 ms: 1.98x faster                                                              |
| async_tree_io              | 1.39 sec                                                     | 740 ms: 1.87x faster                                                              |
| async_tree_none_tg         | 504 ms                                                       | 298 ms: 1.69x faster                                                              |
| async_tree_memoization_tg  | 670 ms                                                       | 403 ms: 1.66x faster                                                              |
| async_tree_none            | 572 ms                                                       | 348 ms: 1.64x faster                                                              |
| async_tree_memoization     | 709 ms                                                       | 452 ms: 1.57x faster                                                              |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 595 ms: 1.43x faster                                                              |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 638 ms: 1.39x faster                                                              |
| asyncio_websockets         | 766 ms                                                       | 690 ms: 1.11x faster                                                              |
| async_generators           | 567 ms                                                       | 542 ms: 1.05x faster                                                              |
| Geometric mean             | (ref)                                                        | 1.46x faster                                                                      |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| float          | 116 ms                                                       | 90.6 ms: 1.28x faster                                                             |
| pidigits       | 251 ms                                                       | 219 ms: 1.15x faster                                                              |
| nbody          | 119 ms                                                       | 148 ms: 1.25x slower                                                              |
| Geometric mean | (ref)                                                        | 1.05x faster                                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| regex_effbot   | 4.74 ms                                                      | 3.66 ms: 1.29x faster                                                             |
| regex_v8       | 32.8 ms                                                      | 29.1 ms: 1.13x faster                                                             |
| regex_dna      | 282 ms                                                       | 251 ms: 1.12x faster                                                              |
| Geometric mean | (ref)                                                        | 1.13x faster                                                                      |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 134 ms: 1.32x faster                                                              |
| xml_etree_parse      | 231 ms                                                       | 200 ms: 1.16x faster                                                              |
| pickle_pure_python   | 416 us                                                       | 432 us: 1.04x slower                                                              |
| tomli_loads          | 2.78 sec                                                     | 2.92 sec: 1.05x slower                                                            |
| unpickle_pure_python | 290 us                                                       | 305 us: 1.05x slower                                                              |
| xml_etree_process    | 85.9 ms                                                      | 95.0 ms: 1.11x slower                                                             |
| xml_etree_generate   | 122 ms                                                       | 139 ms: 1.14x slower                                                              |
| json_dumps           | 14.1 ms                                                      | 17.1 ms: 1.21x slower                                                             |
| json_loads           | 34.3 us                                                      | 42.1 us: 1.23x slower                                                             |
| Geometric mean       | (ref)                                                        | 1.04x slower                                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| python_startup | 22.4 ms                                                      | 25.9 ms: 1.15x slower                                                             |
| Geometric mean | (ref)                                                        | 1.08x slower                                                                      |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 75.8 ms: 1.05x slower                                                             |
| genshi_text     | 31.7 ms                                                      | 34.6 ms: 1.09x slower                                                             |
| django_template | 44.3 ms                                                      | 49.9 ms: 1.13x slower                                                             |
| mako            | 15.9 ms                                                      | 21.9 ms: 1.37x slower                                                             |
| Geometric mean  | (ref)                                                        | 1.15x slower                                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 708 ms: 1.98x faster                                                              |
| async_tree_io              | 1.39 sec                                                     | 740 ms: 1.87x faster                                                              |
| async_tree_none_tg         | 504 ms                                                       | 298 ms: 1.69x faster                                                              |
| async_tree_memoization_tg  | 670 ms                                                       | 403 ms: 1.66x faster                                                              |
| async_tree_none            | 572 ms                                                       | 348 ms: 1.64x faster                                                              |
| mdp                        | 3.80 sec                                                     | 2.31 sec: 1.64x faster                                                            |
| async_tree_memoization     | 709 ms                                                       | 452 ms: 1.57x faster                                                              |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 595 ms: 1.43x faster                                                              |
| gc_traversal               | 5.70 ms                                                      | 4.08 ms: 1.40x faster                                                             |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 638 ms: 1.39x faster                                                              |
| sqlite_synth               | 3.99 us                                                      | 3.01 us: 1.33x faster                                                             |
| xml_etree_iterparse        | 177 ms                                                       | 134 ms: 1.32x faster                                                              |
| deepcopy                   | 498 us                                                       | 379 us: 1.31x faster                                                              |
| regex_effbot               | 4.74 ms                                                      | 3.66 ms: 1.29x faster                                                             |
| float                      | 116 ms                                                       | 90.6 ms: 1.28x faster                                                             |
| spectral_norm              | 157 ms                                                       | 133 ms: 1.18x faster                                                              |
| dulwich_log                | 93.7 ms                                                      | 79.9 ms: 1.17x faster                                                             |
| xml_etree_parse            | 231 ms                                                       | 200 ms: 1.16x faster                                                              |
| pathlib                    | 29.9 ms                                                      | 26.0 ms: 1.15x faster                                                             |
| go                         | 191 ms                                                       | 167 ms: 1.15x faster                                                              |
| pidigits                   | 251 ms                                                       | 219 ms: 1.15x faster                                                              |
| telco                      | 12.2 ms                                                      | 10.8 ms: 1.13x faster                                                             |
| regex_v8                   | 32.8 ms                                                      | 29.1 ms: 1.13x faster                                                             |
| scimark_sor                | 179 ms                                                       | 159 ms: 1.12x faster                                                              |
| regex_dna                  | 282 ms                                                       | 251 ms: 1.12x faster                                                              |
| html5lib                   | 92.6 ms                                                      | 83.2 ms: 1.11x faster                                                             |
| asyncio_websockets         | 766 ms                                                       | 690 ms: 1.11x faster                                                              |
| deepcopy_memo              | 50.1 us                                                      | 45.7 us: 1.10x faster                                                             |
| pycparser                  | 1.57 sec                                                     | 1.47 sec: 1.07x faster                                                            |
| chaos                      | 83.6 ms                                                      | 79.6 ms: 1.05x faster                                                             |
| 2to3                       | 445 ms                                                       | 425 ms: 1.05x faster                                                              |
| async_generators           | 567 ms                                                       | 542 ms: 1.05x faster                                                              |
| deepcopy_reduce            | 4.10 us                                                      | 3.96 us: 1.04x faster                                                             |
| docutils                   | 4.01 sec                                                     | 3.92 sec: 1.02x faster                                                            |
| scimark_fft                | 473 ms                                                       | 464 ms: 1.02x faster                                                              |
| pickle_pure_python         | 416 us                                                       | 432 us: 1.04x slower                                                              |
| logging_simple             | 8.56 us                                                      | 8.95 us: 1.05x slower                                                             |
| tomli_loads                | 2.78 sec                                                     | 2.92 sec: 1.05x slower                                                            |
| unpickle_pure_python       | 290 us                                                       | 305 us: 1.05x slower                                                              |
| genshi_xml                 | 72.1 ms                                                      | 75.8 ms: 1.05x slower                                                             |
| thrift                     | 1.10 ms                                                      | 1.16 ms: 1.05x slower                                                             |
| richards                   | 65.5 ms                                                      | 69.5 ms: 1.06x slower                                                             |
| pprint_safe_repr           | 987 ms                                                       | 1.05 sec: 1.06x slower                                                            |
| logging_silent             | 130 ns                                                       | 140 ns: 1.08x slower                                                              |
| richards_super             | 73.2 ms                                                      | 78.9 ms: 1.08x slower                                                             |
| sympy_str                  | 379 ms                                                       | 408 ms: 1.08x slower                                                              |
| meteor_contest             | 150 ms                                                       | 163 ms: 1.08x slower                                                              |
| sympy_sum                  | 210 ms                                                       | 229 ms: 1.09x slower                                                              |
| json                       | 6.51 ms                                                      | 7.10 ms: 1.09x slower                                                             |
| scimark_monte_carlo        | 90.6 ms                                                      | 98.8 ms: 1.09x slower                                                             |
| genshi_text                | 31.7 ms                                                      | 34.6 ms: 1.09x slower                                                             |
| deltablue                  | 4.44 ms                                                      | 4.86 ms: 1.09x slower                                                             |
| crypto_pyaes               | 100 ms                                                       | 110 ms: 1.09x slower                                                              |
| fannkuch                   | 547 ms                                                       | 599 ms: 1.10x slower                                                              |
| xml_etree_process          | 85.9 ms                                                      | 95.0 ms: 1.11x slower                                                             |
| pprint_pformat             | 1.94 sec                                                     | 2.17 sec: 1.12x slower                                                            |
| logging_format             | 9.24 us                                                      | 10.3 us: 1.12x slower                                                             |
| raytrace                   | 344 ms                                                       | 384 ms: 1.12x slower                                                              |
| django_template            | 44.3 ms                                                      | 49.9 ms: 1.13x slower                                                             |
| sympy_expand               | 601 ms                                                       | 680 ms: 1.13x slower                                                              |
| create_gc_cycles           | 2.41 ms                                                      | 2.73 ms: 1.13x slower                                                             |
| xml_etree_generate         | 122 ms                                                       | 139 ms: 1.14x slower                                                              |
| scimark_lu                 | 146 ms                                                       | 167 ms: 1.14x slower                                                              |
| hexiom                     | 8.11 ms                                                      | 9.32 ms: 1.15x slower                                                             |
| python_startup             | 22.4 ms                                                      | 25.9 ms: 1.15x slower                                                             |
| typing_runtime_protocols   | 226 us                                                       | 261 us: 1.16x slower                                                              |
| comprehensions             | 22.2 us                                                      | 25.8 us: 1.16x slower                                                             |
| bpe_tokeniser              | 6.28 sec                                                     | 7.42 sec: 1.18x slower                                                            |
| generators                 | 40.0 ms                                                      | 47.3 ms: 1.18x slower                                                             |
| json_dumps                 | 14.1 ms                                                      | 17.1 ms: 1.21x slower                                                             |
| json_loads                 | 34.3 us                                                      | 42.1 us: 1.23x slower                                                             |
| nbody                      | 119 ms                                                       | 148 ms: 1.25x slower                                                              |
| coverage                   | 107 ms                                                       | 143 ms: 1.33x slower                                                              |
| mako                       | 15.9 ms                                                      | 21.9 ms: 1.37x slower                                                             |
| bench_mp_pool              | 18.7 ms                                                      | 75.9 ms: 4.06x slower                                                             |
| Geometric mean             | (ref)                                                        | 1.03x faster                                                                      |

Benchmark hidden because not significant (9): pylint, coroutines, scimark_sparse_mat_mult, regex_compile, nqueens, pyflate, python_startup_no_site, sympy_integrate, bench_thread_pool
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250429-3.14.0a7+-39f987b-NOGIL/bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.037x faster

# HPT report

- Reliability score: 50.19% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.35x