# Results vs. 3.12.6

- fork: sergey-miryanov
- ref: gh_132042_precalc_mr
- machine: linux-x86_64
- commit hash: 39f987b
- commit date: 2025-04-29
- overall geometric mean: 1.187x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 362 ms: 1.26x faster                                                              |
| docutils       | 4.00 sec                                               | 3.62 sec: 1.10x faster                                                            |
| html5lib       | 88.9 ms                                                | 79.0 ms: 1.13x faster                                                             |
| Geometric mean | (ref)                                                  | 1.16x faster                                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 839 ms: 2.31x faster                                                              |
| async_tree_memoization     | 977 ms                                                 | 432 ms: 2.26x faster                                                              |
| async_tree_io              | 1.85 sec                                               | 823 ms: 2.25x faster                                                              |
| async_tree_memoization_tg  | 930 ms                                                 | 449 ms: 2.07x faster                                                              |
| async_tree_none            | 741 ms                                                 | 360 ms: 2.06x faster                                                              |
| async_tree_none_tg         | 704 ms                                                 | 344 ms: 2.05x faster                                                              |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 644 ms: 1.71x faster                                                              |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 654 ms: 1.65x faster                                                              |
| async_generators           | 589 ms                                                 | 488 ms: 1.21x faster                                                              |
| asyncio_websockets         | 748 ms                                                 | 667 ms: 1.12x faster                                                              |
| Geometric mean             | (ref)                                                  | 1.72x faster                                                                      |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| float          | 123 ms                                                 | 93.8 ms: 1.31x faster                                                             |
| pidigits       | 250 ms                                                 | 236 ms: 1.06x faster                                                              |
| nbody          | 119 ms                                                 | 114 ms: 1.05x faster                                                              |
| Geometric mean | (ref)                                                  | 1.13x faster                                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 3.82 ms: 1.34x faster                                                             |
| regex_compile  | 187 ms                                                 | 152 ms: 1.23x faster                                                              |
| regex_v8       | 32.5 ms                                                | 27.1 ms: 1.20x faster                                                             |
| regex_dna      | 278 ms                                                 | 248 ms: 1.12x faster                                                              |
| Geometric mean | (ref)                                                  | 1.22x faster                                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| xml_etree_parse      | 241 ms                                                 | 190 ms: 1.26x faster                                                              |
| tomli_loads          | 2.88 sec                                               | 2.42 sec: 1.19x faster                                                            |
| xml_etree_iterparse  | 169 ms                                                 | 143 ms: 1.19x faster                                                              |
| xml_etree_generate   | 127 ms                                                 | 115 ms: 1.11x faster                                                              |
| pickle_pure_python   | 436 us                                                 | 397 us: 1.10x faster                                                              |
| unpickle_pure_python | 300 us                                                 | 276 us: 1.08x faster                                                              |
| xml_etree_process    | 83.7 ms                                                | 79.2 ms: 1.06x faster                                                             |
| json_loads           | 37.9 us                                                | 39.3 us: 1.04x slower                                                             |
| json_dumps           | 14.3 ms                                                | 14.9 ms: 1.04x slower                                                             |
| Geometric mean       | (ref)                                                  | 1.10x faster                                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 11.6 ms: 1.52x faster                                                             |
| python_startup         | 23.7 ms                                                | 19.0 ms: 1.25x faster                                                             |
| Geometric mean         | (ref)                                                  | 1.38x faster                                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| genshi_text     | 30.2 ms                                                | 26.9 ms: 1.12x faster                                                             |
| genshi_xml      | 67.6 ms                                                | 61.9 ms: 1.09x faster                                                             |
| django_template | 44.9 ms                                                | 43.2 ms: 1.04x faster                                                             |
| mako            | 15.7 ms                                                | 17.7 ms: 1.13x slower                                                             |
| Geometric mean  | (ref)                                                  | 1.03x faster                                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 839 ms: 2.31x faster                                                              |
| async_tree_memoization     | 977 ms                                                 | 432 ms: 2.26x faster                                                              |
| async_tree_io              | 1.85 sec                                               | 823 ms: 2.25x faster                                                              |
| mdp                        | 3.97 sec                                               | 1.90 sec: 2.09x faster                                                            |
| async_tree_memoization_tg  | 930 ms                                                 | 449 ms: 2.07x faster                                                              |
| async_tree_none            | 741 ms                                                 | 360 ms: 2.06x faster                                                              |
| async_tree_none_tg         | 704 ms                                                 | 344 ms: 2.05x faster                                                              |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 644 ms: 1.71x faster                                                              |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 654 ms: 1.65x faster                                                              |
| python_startup_no_site     | 17.6 ms                                                | 11.6 ms: 1.52x faster                                                             |
| deepcopy                   | 468 us                                                 | 317 us: 1.48x faster                                                              |
| deepcopy_memo              | 52.4 us                                                | 37.1 us: 1.41x faster                                                             |
| bench_thread_pool          | 3.48 ms                                                | 2.55 ms: 1.36x faster                                                             |
| dulwich_log                | 100 ms                                                 | 74.1 ms: 1.35x faster                                                             |
| regex_effbot               | 5.13 ms                                                | 3.82 ms: 1.34x faster                                                             |
| float                      | 123 ms                                                 | 93.8 ms: 1.31x faster                                                             |
| comprehensions             | 27.1 us                                                | 21.1 us: 1.28x faster                                                             |
| xml_etree_parse            | 241 ms                                                 | 190 ms: 1.26x faster                                                              |
| pathlib                    | 31.6 ms                                                | 25.1 ms: 1.26x faster                                                             |
| 2to3                       | 456 ms                                                 | 362 ms: 1.26x faster                                                              |
| python_startup             | 23.7 ms                                                | 19.0 ms: 1.25x faster                                                             |
| logging_simple             | 9.45 us                                                | 7.60 us: 1.24x faster                                                             |
| pyflate                    | 727 ms                                                 | 587 ms: 1.24x faster                                                              |
| raytrace                   | 408 ms                                                 | 330 ms: 1.24x faster                                                              |
| regex_compile              | 187 ms                                                 | 152 ms: 1.23x faster                                                              |
| spectral_norm              | 156 ms                                                 | 127 ms: 1.22x faster                                                              |
| deepcopy_reduce            | 4.04 us                                                | 3.32 us: 1.22x faster                                                             |
| pylint                     | 465 ms                                                 | 383 ms: 1.21x faster                                                              |
| go                         | 172 ms                                                 | 143 ms: 1.21x faster                                                              |
| async_generators           | 589 ms                                                 | 488 ms: 1.21x faster                                                              |
| chaos                      | 84.9 ms                                                | 70.5 ms: 1.20x faster                                                             |
| crypto_pyaes               | 107 ms                                                 | 89.5 ms: 1.20x faster                                                             |
| regex_v8                   | 32.5 ms                                                | 27.1 ms: 1.20x faster                                                             |
| pycparser                  | 1.79 sec                                               | 1.50 sec: 1.20x faster                                                            |
| scimark_fft                | 500 ms                                                 | 419 ms: 1.19x faster                                                              |
| tomli_loads                | 2.88 sec                                               | 2.42 sec: 1.19x faster                                                            |
| xml_etree_iterparse        | 169 ms                                                 | 143 ms: 1.19x faster                                                              |
| scimark_monte_carlo        | 96.4 ms                                                | 81.2 ms: 1.19x faster                                                             |
| sympy_sum                  | 222 ms                                                 | 187 ms: 1.19x faster                                                              |
| sympy_integrate            | 29.8 ms                                                | 25.1 ms: 1.18x faster                                                             |
| sqlite_synth               | 3.87 us                                                | 3.28 us: 1.18x faster                                                             |
| sympy_str                  | 385 ms                                                 | 328 ms: 1.17x faster                                                              |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 5.72 ms: 1.17x faster                                                             |
| nqueens                    | 117 ms                                                 | 99.7 ms: 1.17x faster                                                             |
| bpe_tokeniser              | 6.59 sec                                               | 5.63 sec: 1.17x faster                                                            |
| scimark_sor                | 167 ms                                                 | 145 ms: 1.15x faster                                                              |
| richards_super             | 72.8 ms                                                | 63.7 ms: 1.14x faster                                                             |
| meteor_contest             | 146 ms                                                 | 128 ms: 1.14x faster                                                              |
| thrift                     | 1.06 ms                                                | 936 us: 1.13x faster                                                              |
| html5lib                   | 88.9 ms                                                | 79.0 ms: 1.13x faster                                                             |
| typing_runtime_protocols   | 224 us                                                 | 199 us: 1.13x faster                                                              |
| genshi_text                | 30.2 ms                                                | 26.9 ms: 1.12x faster                                                             |
| regex_dna                  | 278 ms                                                 | 248 ms: 1.12x faster                                                              |
| asyncio_websockets         | 748 ms                                                 | 667 ms: 1.12x faster                                                              |
| logging_format             | 9.59 us                                                | 8.62 us: 1.11x faster                                                             |
| xml_etree_generate         | 127 ms                                                 | 115 ms: 1.11x faster                                                              |
| docutils                   | 4.00 sec                                               | 3.62 sec: 1.10x faster                                                            |
| pickle_pure_python         | 436 us                                                 | 397 us: 1.10x faster                                                              |
| genshi_xml                 | 67.6 ms                                                | 61.9 ms: 1.09x faster                                                             |
| pprint_pformat             | 1.98 sec                                               | 1.81 sec: 1.09x faster                                                            |
| hexiom                     | 8.27 ms                                                | 7.59 ms: 1.09x faster                                                             |
| richards                   | 60.3 ms                                                | 55.4 ms: 1.09x faster                                                             |
| unpickle_pure_python       | 300 us                                                 | 276 us: 1.08x faster                                                              |
| pprint_safe_repr           | 967 ms                                                 | 897 ms: 1.08x faster                                                              |
| logging_silent             | 139 ns                                                 | 131 ns: 1.07x faster                                                              |
| sympy_expand               | 582 ms                                                 | 547 ms: 1.06x faster                                                              |
| pidigits                   | 250 ms                                                 | 236 ms: 1.06x faster                                                              |
| xml_etree_process          | 83.7 ms                                                | 79.2 ms: 1.06x faster                                                             |
| fannkuch                   | 540 ms                                                 | 512 ms: 1.05x faster                                                              |
| nbody                      | 119 ms                                                 | 114 ms: 1.05x faster                                                              |
| telco                      | 9.59 ms                                                | 9.19 ms: 1.04x faster                                                             |
| django_template            | 44.9 ms                                                | 43.2 ms: 1.04x faster                                                             |
| scimark_lu                 | 152 ms                                                 | 146 ms: 1.04x faster                                                              |
| json_loads                 | 37.9 us                                                | 39.3 us: 1.04x slower                                                             |
| json_dumps                 | 14.3 ms                                                | 14.9 ms: 1.04x slower                                                             |
| coverage                   | 95.4 ms                                                | 108 ms: 1.13x slower                                                              |
| mako                       | 15.7 ms                                                | 17.7 ms: 1.13x slower                                                             |
| gc_traversal               | 5.86 ms                                                | 8.40 ms: 1.43x slower                                                             |
| create_gc_cycles           | 1.94 ms                                                | 4.09 ms: 2.11x slower                                                             |
| bench_mp_pool              | 20.7 ms                                                | 77.2 ms: 3.73x slower                                                             |
| Geometric mean             | (ref)                                                  | 1.18x faster                                                                      |

Benchmark hidden because not significant (4): generators, json, deltablue, coroutines
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250429-3.14.0a7+-39f987b/bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.187x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.12x
- 95% likely to have a speedup of 1.11x
- 99% likely to have a speedup of 1.10x

# Memory
- memory change: 1.13x