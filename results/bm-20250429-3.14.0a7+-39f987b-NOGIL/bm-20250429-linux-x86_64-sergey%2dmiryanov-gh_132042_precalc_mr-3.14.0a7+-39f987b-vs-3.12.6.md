# Results vs. 3.12.6

- fork: sergey-miryanov
- ref: gh_132042_precalc_mr
- machine: linux-x86_64
- commit hash: 39f987b
- commit date: 2025-04-29
- overall geometric mean: 1.079x faster
- HPT reliability: 71.43%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 425 ms: 1.07x faster                                                              |
| html5lib       | 88.9 ms                                                | 83.2 ms: 1.07x faster                                                             |
| Geometric mean | (ref)                                                  | 1.05x faster                                                                      |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 708 ms: 2.73x faster                                                              |
| async_tree_io              | 1.85 sec                                               | 740 ms: 2.50x faster                                                              |
| async_tree_none_tg         | 704 ms                                                 | 298 ms: 2.36x faster                                                              |
| async_tree_memoization_tg  | 930 ms                                                 | 403 ms: 2.31x faster                                                              |
| async_tree_memoization     | 977 ms                                                 | 452 ms: 2.16x faster                                                              |
| async_tree_none            | 741 ms                                                 | 348 ms: 2.13x faster                                                              |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 595 ms: 1.85x faster                                                              |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 638 ms: 1.69x faster                                                              |
| async_generators           | 589 ms                                                 | 542 ms: 1.09x faster                                                              |
| asyncio_websockets         | 748 ms                                                 | 690 ms: 1.08x faster                                                              |
| Geometric mean             | (ref)                                                  | 1.80x faster                                                                      |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| float          | 123 ms                                                 | 90.6 ms: 1.36x faster                                                             |
| pidigits       | 250 ms                                                 | 219 ms: 1.14x faster                                                              |
| nbody          | 119 ms                                                 | 148 ms: 1.25x slower                                                              |
| Geometric mean | (ref)                                                  | 1.08x faster                                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 3.66 ms: 1.40x faster                                                             |
| regex_v8       | 32.5 ms                                                | 29.1 ms: 1.12x faster                                                             |
| regex_dna      | 278 ms                                                 | 251 ms: 1.11x faster                                                              |
| Geometric mean | (ref)                                                  | 1.16x faster                                                                      |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|---------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| xml_etree_iterparse | 169 ms                                                 | 134 ms: 1.26x faster                                                              |
| xml_etree_parse     | 241 ms                                                 | 200 ms: 1.21x faster                                                              |
| xml_etree_generate  | 127 ms                                                 | 139 ms: 1.09x slower                                                              |
| json_loads          | 37.9 us                                                | 42.1 us: 1.11x slower                                                             |
| xml_etree_process   | 83.7 ms                                                | 95.0 ms: 1.13x slower                                                             |
| json_dumps          | 14.3 ms                                                | 17.1 ms: 1.20x slower                                                             |
| Geometric mean      | (ref)                                                  | 1.01x slower                                                                      |

Benchmark hidden because not significant (3): pickle_pure_python, tomli_loads, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 15.5 ms: 1.14x faster                                                             |
| python_startup         | 23.7 ms                                                | 25.9 ms: 1.09x slower                                                             |
| Geometric mean         | (ref)                                                  | 1.02x faster                                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| django_template | 44.9 ms                                                | 49.9 ms: 1.11x slower                                                             |
| genshi_xml      | 67.6 ms                                                | 75.8 ms: 1.12x slower                                                             |
| genshi_text     | 30.2 ms                                                | 34.6 ms: 1.14x slower                                                             |
| mako            | 15.7 ms                                                | 21.9 ms: 1.39x slower                                                             |
| Geometric mean  | (ref)                                                  | 1.19x slower                                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 708 ms: 2.73x faster                                                              |
| async_tree_io              | 1.85 sec                                               | 740 ms: 2.50x faster                                                              |
| async_tree_none_tg         | 704 ms                                                 | 298 ms: 2.36x faster                                                              |
| async_tree_memoization_tg  | 930 ms                                                 | 403 ms: 2.31x faster                                                              |
| async_tree_memoization     | 977 ms                                                 | 452 ms: 2.16x faster                                                              |
| async_tree_none            | 741 ms                                                 | 348 ms: 2.13x faster                                                              |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 595 ms: 1.85x faster                                                              |
| mdp                        | 3.97 sec                                               | 2.31 sec: 1.72x faster                                                            |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 638 ms: 1.69x faster                                                              |
| gc_traversal               | 5.86 ms                                                | 4.08 ms: 1.44x faster                                                             |
| regex_effbot               | 5.13 ms                                                | 3.66 ms: 1.40x faster                                                             |
| float                      | 123 ms                                                 | 90.6 ms: 1.36x faster                                                             |
| sqlite_synth               | 3.87 us                                                | 3.01 us: 1.29x faster                                                             |
| xml_etree_iterparse        | 169 ms                                                 | 134 ms: 1.26x faster                                                              |
| dulwich_log                | 100 ms                                                 | 79.9 ms: 1.25x faster                                                             |
| deepcopy                   | 468 us                                                 | 379 us: 1.23x faster                                                              |
| pycparser                  | 1.79 sec                                               | 1.47 sec: 1.22x faster                                                            |
| pathlib                    | 31.6 ms                                                | 26.0 ms: 1.22x faster                                                             |
| xml_etree_parse            | 241 ms                                                 | 200 ms: 1.21x faster                                                              |
| spectral_norm              | 156 ms                                                 | 133 ms: 1.17x faster                                                              |
| bench_thread_pool          | 3.48 ms                                                | 3.00 ms: 1.16x faster                                                             |
| deepcopy_memo              | 52.4 us                                                | 45.7 us: 1.15x faster                                                             |
| pidigits                   | 250 ms                                                 | 219 ms: 1.14x faster                                                              |
| python_startup_no_site     | 17.6 ms                                                | 15.5 ms: 1.14x faster                                                             |
| regex_v8                   | 32.5 ms                                                | 29.1 ms: 1.12x faster                                                             |
| regex_dna                  | 278 ms                                                 | 251 ms: 1.11x faster                                                              |
| pyflate                    | 727 ms                                                 | 666 ms: 1.09x faster                                                              |
| async_generators           | 589 ms                                                 | 542 ms: 1.09x faster                                                              |
| asyncio_websockets         | 748 ms                                                 | 690 ms: 1.08x faster                                                              |
| scimark_fft                | 500 ms                                                 | 464 ms: 1.08x faster                                                              |
| 2to3                       | 456 ms                                                 | 425 ms: 1.07x faster                                                              |
| html5lib                   | 88.9 ms                                                | 83.2 ms: 1.07x faster                                                             |
| chaos                      | 84.9 ms                                                | 79.6 ms: 1.07x faster                                                             |
| raytrace                   | 408 ms                                                 | 384 ms: 1.06x faster                                                              |
| logging_simple             | 9.45 us                                                | 8.95 us: 1.06x faster                                                             |
| comprehensions             | 27.1 us                                                | 25.8 us: 1.05x faster                                                             |
| scimark_sor                | 167 ms                                                 | 159 ms: 1.05x faster                                                              |
| nqueens                    | 117 ms                                                 | 112 ms: 1.05x faster                                                              |
| go                         | 172 ms                                                 | 167 ms: 1.03x faster                                                              |
| json                       | 6.85 ms                                                | 7.10 ms: 1.04x slower                                                             |
| sympy_str                  | 385 ms                                                 | 408 ms: 1.06x slower                                                              |
| logging_format             | 9.59 us                                                | 10.3 us: 1.08x slower                                                             |
| richards_super             | 72.8 ms                                                | 78.9 ms: 1.08x slower                                                             |
| pprint_safe_repr           | 967 ms                                                 | 1.05 sec: 1.08x slower                                                            |
| python_startup             | 23.7 ms                                                | 25.9 ms: 1.09x slower                                                             |
| thrift                     | 1.06 ms                                                | 1.16 ms: 1.09x slower                                                             |
| pprint_pformat             | 1.98 sec                                               | 2.17 sec: 1.09x slower                                                            |
| xml_etree_generate         | 127 ms                                                 | 139 ms: 1.09x slower                                                              |
| scimark_lu                 | 152 ms                                                 | 167 ms: 1.10x slower                                                              |
| fannkuch                   | 540 ms                                                 | 599 ms: 1.11x slower                                                              |
| json_loads                 | 37.9 us                                                | 42.1 us: 1.11x slower                                                             |
| meteor_contest             | 146 ms                                                 | 163 ms: 1.11x slower                                                              |
| django_template            | 44.9 ms                                                | 49.9 ms: 1.11x slower                                                             |
| genshi_xml                 | 67.6 ms                                                | 75.8 ms: 1.12x slower                                                             |
| telco                      | 9.59 ms                                                | 10.8 ms: 1.12x slower                                                             |
| bpe_tokeniser              | 6.59 sec                                               | 7.42 sec: 1.13x slower                                                            |
| hexiom                     | 8.27 ms                                                | 9.32 ms: 1.13x slower                                                             |
| xml_etree_process          | 83.7 ms                                                | 95.0 ms: 1.13x slower                                                             |
| deltablue                  | 4.27 ms                                                | 4.86 ms: 1.14x slower                                                             |
| genshi_text                | 30.2 ms                                                | 34.6 ms: 1.14x slower                                                             |
| generators                 | 41.1 ms                                                | 47.3 ms: 1.15x slower                                                             |
| richards                   | 60.3 ms                                                | 69.5 ms: 1.15x slower                                                             |
| typing_runtime_protocols   | 224 us                                                 | 261 us: 1.16x slower                                                              |
| sympy_expand               | 582 ms                                                 | 680 ms: 1.17x slower                                                              |
| json_dumps                 | 14.3 ms                                                | 17.1 ms: 1.20x slower                                                             |
| nbody                      | 119 ms                                                 | 148 ms: 1.25x slower                                                              |
| mako                       | 15.7 ms                                                | 21.9 ms: 1.39x slower                                                             |
| create_gc_cycles           | 1.94 ms                                                | 2.73 ms: 1.41x slower                                                             |
| coverage                   | 95.4 ms                                                | 143 ms: 1.50x slower                                                              |
| bench_mp_pool              | 20.7 ms                                                | 75.9 ms: 3.67x slower                                                             |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                                      |

Benchmark hidden because not significant (14): pylint, regex_compile, deepcopy_reduce, docutils, scimark_sparse_mat_mult, pickle_pure_python, logging_silent, coroutines, tomli_loads, unpickle_pure_python, crypto_pyaes, scimark_monte_carlo, sympy_sum, sympy_integrate
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250429-3.14.0a7+-39f987b-NOGIL/bm-20250429-linux-x86_64-sergey%2dmiryanov-gh_132042_precalc_mr-3.14.0a7+-39f987b.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.079x faster

# HPT report

- Reliability score: 71.43% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.36x