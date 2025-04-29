# Results vs. 3.13.0rc2

- fork: sergey-miryanov
- ref: gh_132042_precalc_mr
- machine: linux-x86_64
- commit hash: 39f987b
- commit date: 2025-04-29
- overall geometric mean: 1.143x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.09x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 362 ms: 1.23x faster                                                              |
| docutils       | 4.01 sec                                                     | 3.62 sec: 1.11x faster                                                            |
| html5lib       | 92.6 ms                                                      | 79.0 ms: 1.17x faster                                                             |
| Geometric mean | (ref)                                                        | 1.17x faster                                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| async_tree_io              | 1.39 sec                                                     | 823 ms: 1.69x faster                                                              |
| async_tree_io_tg           | 1.40 sec                                                     | 839 ms: 1.67x faster                                                              |
| async_tree_memoization     | 709 ms                                                       | 432 ms: 1.64x faster                                                              |
| async_tree_none            | 572 ms                                                       | 360 ms: 1.59x faster                                                              |
| async_tree_memoization_tg  | 670 ms                                                       | 449 ms: 1.49x faster                                                              |
| async_tree_none_tg         | 504 ms                                                       | 344 ms: 1.46x faster                                                              |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 654 ms: 1.36x faster                                                              |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 644 ms: 1.32x faster                                                              |
| async_generators           | 567 ms                                                       | 488 ms: 1.16x faster                                                              |
| asyncio_websockets         | 766 ms                                                       | 667 ms: 1.15x faster                                                              |
| Geometric mean             | (ref)                                                        | 1.40x faster                                                                      |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| float          | 116 ms                                                       | 93.8 ms: 1.23x faster                                                             |
| pidigits       | 251 ms                                                       | 236 ms: 1.06x faster                                                              |
| nbody          | 119 ms                                                       | 114 ms: 1.04x faster                                                              |
| Geometric mean | (ref)                                                        | 1.11x faster                                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| regex_effbot   | 4.74 ms                                                      | 3.82 ms: 1.24x faster                                                             |
| regex_v8       | 32.8 ms                                                      | 27.1 ms: 1.21x faster                                                             |
| regex_compile  | 182 ms                                                       | 152 ms: 1.20x faster                                                              |
| regex_dna      | 282 ms                                                       | 248 ms: 1.14x faster                                                              |
| Geometric mean | (ref)                                                        | 1.19x faster                                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 143 ms: 1.24x faster                                                              |
| xml_etree_parse      | 231 ms                                                       | 190 ms: 1.21x faster                                                              |
| tomli_loads          | 2.78 sec                                                     | 2.42 sec: 1.15x faster                                                            |
| xml_etree_process    | 85.9 ms                                                      | 79.2 ms: 1.08x faster                                                             |
| xml_etree_generate   | 122 ms                                                       | 115 ms: 1.06x faster                                                              |
| unpickle_pure_python | 290 us                                                       | 276 us: 1.05x faster                                                              |
| pickle_pure_python   | 416 us                                                       | 397 us: 1.05x faster                                                              |
| json_dumps           | 14.1 ms                                                      | 14.9 ms: 1.06x slower                                                             |
| json_loads           | 34.3 us                                                      | 39.3 us: 1.15x slower                                                             |
| Geometric mean       | (ref)                                                        | 1.07x faster                                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 11.6 ms: 1.32x faster                                                             |
| python_startup         | 22.4 ms                                                      | 19.0 ms: 1.18x faster                                                             |
| Geometric mean         | (ref)                                                        | 1.25x faster                                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| genshi_text     | 31.7 ms                                                      | 26.9 ms: 1.18x faster                                                             |
| genshi_xml      | 72.1 ms                                                      | 61.9 ms: 1.16x faster                                                             |
| django_template | 44.3 ms                                                      | 43.2 ms: 1.02x faster                                                             |
| mako            | 15.9 ms                                                      | 17.7 ms: 1.11x slower                                                             |
| Geometric mean  | (ref)                                                        | 1.06x faster                                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| mdp                        | 3.80 sec                                                     | 1.90 sec: 2.00x faster                                                            |
| async_tree_io              | 1.39 sec                                                     | 823 ms: 1.69x faster                                                              |
| async_tree_io_tg           | 1.40 sec                                                     | 839 ms: 1.67x faster                                                              |
| async_tree_memoization     | 709 ms                                                       | 432 ms: 1.64x faster                                                              |
| async_tree_none            | 572 ms                                                       | 360 ms: 1.59x faster                                                              |
| deepcopy                   | 498 us                                                       | 317 us: 1.57x faster                                                              |
| async_tree_memoization_tg  | 670 ms                                                       | 449 ms: 1.49x faster                                                              |
| async_tree_none_tg         | 504 ms                                                       | 344 ms: 1.46x faster                                                              |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 654 ms: 1.36x faster                                                              |
| deepcopy_memo              | 50.1 us                                                      | 37.1 us: 1.35x faster                                                             |
| go                         | 191 ms                                                       | 143 ms: 1.34x faster                                                              |
| telco                      | 12.2 ms                                                      | 9.19 ms: 1.32x faster                                                             |
| python_startup_no_site     | 15.3 ms                                                      | 11.6 ms: 1.32x faster                                                             |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 644 ms: 1.32x faster                                                              |
| dulwich_log                | 93.7 ms                                                      | 74.1 ms: 1.26x faster                                                             |
| xml_etree_iterparse        | 177 ms                                                       | 143 ms: 1.24x faster                                                              |
| regex_effbot               | 4.74 ms                                                      | 3.82 ms: 1.24x faster                                                             |
| deepcopy_reduce            | 4.10 us                                                      | 3.32 us: 1.23x faster                                                             |
| float                      | 116 ms                                                       | 93.8 ms: 1.23x faster                                                             |
| 2to3                       | 445 ms                                                       | 362 ms: 1.23x faster                                                              |
| pylint                     | 470 ms                                                       | 383 ms: 1.23x faster                                                              |
| spectral_norm              | 157 ms                                                       | 127 ms: 1.23x faster                                                              |
| scimark_sor                | 179 ms                                                       | 145 ms: 1.23x faster                                                              |
| sqlite_synth               | 3.99 us                                                      | 3.28 us: 1.22x faster                                                             |
| xml_etree_parse            | 231 ms                                                       | 190 ms: 1.21x faster                                                              |
| regex_v8                   | 32.8 ms                                                      | 27.1 ms: 1.21x faster                                                             |
| sympy_integrate            | 30.2 ms                                                      | 25.1 ms: 1.20x faster                                                             |
| regex_compile              | 182 ms                                                       | 152 ms: 1.20x faster                                                              |
| pathlib                    | 29.9 ms                                                      | 25.1 ms: 1.19x faster                                                             |
| chaos                      | 83.6 ms                                                      | 70.5 ms: 1.19x faster                                                             |
| richards                   | 65.5 ms                                                      | 55.4 ms: 1.18x faster                                                             |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 5.72 ms: 1.18x faster                                                             |
| python_startup             | 22.4 ms                                                      | 19.0 ms: 1.18x faster                                                             |
| genshi_text                | 31.7 ms                                                      | 26.9 ms: 1.18x faster                                                             |
| thrift                     | 1.10 ms                                                      | 936 us: 1.18x faster                                                              |
| html5lib                   | 92.6 ms                                                      | 79.0 ms: 1.17x faster                                                             |
| meteor_contest             | 150 ms                                                       | 128 ms: 1.17x faster                                                              |
| genshi_xml                 | 72.1 ms                                                      | 61.9 ms: 1.16x faster                                                             |
| async_generators           | 567 ms                                                       | 488 ms: 1.16x faster                                                              |
| sympy_str                  | 379 ms                                                       | 328 ms: 1.16x faster                                                              |
| richards_super             | 73.2 ms                                                      | 63.7 ms: 1.15x faster                                                             |
| asyncio_websockets         | 766 ms                                                       | 667 ms: 1.15x faster                                                              |
| tomli_loads                | 2.78 sec                                                     | 2.42 sec: 1.15x faster                                                            |
| regex_dna                  | 282 ms                                                       | 248 ms: 1.14x faster                                                              |
| typing_runtime_protocols   | 226 us                                                       | 199 us: 1.13x faster                                                              |
| bench_thread_pool          | 2.89 ms                                                      | 2.55 ms: 1.13x faster                                                             |
| pyflate                    | 664 ms                                                       | 587 ms: 1.13x faster                                                              |
| scimark_fft                | 473 ms                                                       | 419 ms: 1.13x faster                                                              |
| logging_simple             | 8.56 us                                                      | 7.60 us: 1.13x faster                                                             |
| sympy_sum                  | 210 ms                                                       | 187 ms: 1.12x faster                                                              |
| nqueens                    | 112 ms                                                       | 99.7 ms: 1.12x faster                                                             |
| crypto_pyaes               | 100 ms                                                       | 89.5 ms: 1.12x faster                                                             |
| bpe_tokeniser              | 6.28 sec                                                     | 5.63 sec: 1.12x faster                                                            |
| scimark_monte_carlo        | 90.6 ms                                                      | 81.2 ms: 1.12x faster                                                             |
| docutils                   | 4.01 sec                                                     | 3.62 sec: 1.11x faster                                                            |
| pprint_safe_repr           | 987 ms                                                       | 897 ms: 1.10x faster                                                              |
| sympy_expand               | 601 ms                                                       | 547 ms: 1.10x faster                                                              |
| xml_etree_process          | 85.9 ms                                                      | 79.2 ms: 1.08x faster                                                             |
| logging_format             | 9.24 us                                                      | 8.62 us: 1.07x faster                                                             |
| pprint_pformat             | 1.94 sec                                                     | 1.81 sec: 1.07x faster                                                            |
| hexiom                     | 8.11 ms                                                      | 7.59 ms: 1.07x faster                                                             |
| fannkuch                   | 547 ms                                                       | 512 ms: 1.07x faster                                                              |
| xml_etree_generate         | 122 ms                                                       | 115 ms: 1.06x faster                                                              |
| pidigits                   | 251 ms                                                       | 236 ms: 1.06x faster                                                              |
| comprehensions             | 22.2 us                                                      | 21.1 us: 1.05x faster                                                             |
| unpickle_pure_python       | 290 us                                                       | 276 us: 1.05x faster                                                              |
| pycparser                  | 1.57 sec                                                     | 1.50 sec: 1.05x faster                                                            |
| pickle_pure_python         | 416 us                                                       | 397 us: 1.05x faster                                                              |
| nbody                      | 119 ms                                                       | 114 ms: 1.04x faster                                                              |
| raytrace                   | 344 ms                                                       | 330 ms: 1.04x faster                                                              |
| django_template            | 44.3 ms                                                      | 43.2 ms: 1.02x faster                                                             |
| json                       | 6.51 ms                                                      | 6.86 ms: 1.05x slower                                                             |
| json_dumps                 | 14.1 ms                                                      | 14.9 ms: 1.06x slower                                                             |
| mako                       | 15.9 ms                                                      | 17.7 ms: 1.11x slower                                                             |
| json_loads                 | 34.3 us                                                      | 39.3 us: 1.15x slower                                                             |
| gc_traversal               | 5.70 ms                                                      | 8.40 ms: 1.47x slower                                                             |
| create_gc_cycles           | 2.41 ms                                                      | 4.09 ms: 1.70x slower                                                             |
| bench_mp_pool              | 18.7 ms                                                      | 77.2 ms: 4.13x slower                                                             |
| Geometric mean             | (ref)                                                        | 1.13x faster                                                                      |

Benchmark hidden because not significant (6): deltablue, coroutines, scimark_lu, coverage, logging_silent, generators
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250429-3.14.0a7+-39f987b/bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.143x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.11x
- 95% likely to have a speedup of 1.10x
- 99% likely to have a speedup of 1.09x

# Memory
- memory change: 1.13x