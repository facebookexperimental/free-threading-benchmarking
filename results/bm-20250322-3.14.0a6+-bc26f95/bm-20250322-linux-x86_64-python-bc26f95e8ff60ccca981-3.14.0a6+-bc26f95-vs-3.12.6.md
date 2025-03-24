# Results vs. 3.12.6

- fork: python
- ref: bc26f95e8ff60ccca981
- machine: linux-x86_64
- commit hash: bc26f95
- commit date: 2025-03-22
- overall geometric mean: 1.145x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 404 ms: 1.13x faster                                                   |
| docutils       | 4.00 sec                                               | 3.55 sec: 1.12x faster                                                 |
| Geometric mean | (ref)                                                  | 1.13x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 877 ms: 2.21x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 854 ms: 2.16x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 461 ms: 2.12x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 440 ms: 2.11x faster                                                   |
| async_tree_none            | 741 ms                                                 | 369 ms: 2.01x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 359 ms: 1.96x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 665 ms: 1.66x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 664 ms: 1.62x faster                                                   |
| async_generators           | 589 ms                                                 | 479 ms: 1.23x faster                                                   |
| asyncio_tcp                | 923 ms                                                 | 853 ms: 1.08x faster                                                   |
| asyncio_websockets         | 748 ms                                                 | 714 ms: 1.05x faster                                                   |
| asyncio_tcp_ssl            | 2.81 sec                                               | 2.71 sec: 1.04x faster                                                 |
| coroutines                 | 29.5 ms                                                | 31.8 ms: 1.08x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.55x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 95.4 ms: 1.29x faster                                                  |
| pidigits       | 250 ms                                                 | 240 ms: 1.04x faster                                                   |
| nbody          | 119 ms                                                 | 129 ms: 1.08x slower                                                   |
| Geometric mean | (ref)                                                  | 1.07x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 3.99 ms: 1.29x faster                                                  |
| regex_v8       | 32.5 ms                                                | 30.2 ms: 1.08x faster                                                  |
| Geometric mean | (ref)                                                  | 1.10x faster                                                           |

Benchmark hidden because not significant (2): regex_compile, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|---------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse     | 241 ms                                                 | 186 ms: 1.29x faster                                                   |
| xml_etree_iterparse | 169 ms                                                 | 139 ms: 1.22x faster                                                   |
| tomli_loads         | 2.88 sec                                               | 2.43 sec: 1.19x faster                                                 |
| pickle_dict         | 52.7 us                                                | 45.6 us: 1.16x faster                                                  |
| unpickle            | 21.2 us                                                | 18.5 us: 1.15x faster                                                  |
| xml_etree_generate  | 127 ms                                                 | 113 ms: 1.12x faster                                                   |
| pickle_pure_python  | 436 us                                                 | 399 us: 1.09x faster                                                   |
| xml_etree_process   | 83.7 ms                                                | 77.6 ms: 1.08x faster                                                  |
| pickle_list         | 6.97 us                                                | 6.61 us: 1.06x faster                                                  |
| json_dumps          | 14.3 ms                                                | 15.1 ms: 1.06x slower                                                  |
| Geometric mean      | (ref)                                                  | 1.09x faster                                                           |

Benchmark hidden because not significant (4): unpickle_pure_python, pickle, json_loads, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 17.0 ms: 1.04x faster                                                  |
| python_startup         | 23.7 ms                                                | 28.8 ms: 1.21x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.08x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text    | 30.2 ms                                                | 27.0 ms: 1.12x faster                                                  |
| genshi_xml     | 67.6 ms                                                | 63.7 ms: 1.06x faster                                                  |
| Geometric mean | (ref)                                                  | 1.04x faster                                                           |

Benchmark hidden because not significant (2): django_template, mako

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 877 ms: 2.21x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 854 ms: 2.16x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 461 ms: 2.12x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 440 ms: 2.11x faster                                                   |
| async_tree_none            | 741 ms                                                 | 369 ms: 2.01x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 359 ms: 1.96x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 665 ms: 1.66x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 664 ms: 1.62x faster                                                   |
| deepcopy_memo              | 52.4 us                                                | 36.3 us: 1.44x faster                                                  |
| deepcopy                   | 468 us                                                 | 330 us: 1.42x faster                                                   |
| comprehensions             | 27.1 us                                                | 20.9 us: 1.30x faster                                                  |
| xml_etree_parse            | 241 ms                                                 | 186 ms: 1.29x faster                                                   |
| float                      | 123 ms                                                 | 95.4 ms: 1.29x faster                                                  |
| regex_effbot               | 5.13 ms                                                | 3.99 ms: 1.29x faster                                                  |
| sqlalchemy_declarative     | 218 ms                                                 | 173 ms: 1.25x faster                                                   |
| spectral_norm              | 156 ms                                                 | 125 ms: 1.24x faster                                                   |
| async_generators           | 589 ms                                                 | 479 ms: 1.23x faster                                                   |
| xml_etree_iterparse        | 169 ms                                                 | 139 ms: 1.22x faster                                                   |
| logging_simple             | 9.45 us                                                | 7.86 us: 1.20x faster                                                  |
| raytrace                   | 408 ms                                                 | 342 ms: 1.19x faster                                                   |
| pycparser                  | 1.79 sec                                               | 1.50 sec: 1.19x faster                                                 |
| pylint                     | 465 ms                                                 | 391 ms: 1.19x faster                                                   |
| logging_silent             | 139 ns                                                 | 117 ns: 1.19x faster                                                   |
| tomli_loads                | 2.88 sec                                               | 2.43 sec: 1.19x faster                                                 |
| pyflate                    | 727 ms                                                 | 620 ms: 1.17x faster                                                   |
| pickle_dict                | 52.7 us                                                | 45.6 us: 1.16x faster                                                  |
| crypto_pyaes               | 107 ms                                                 | 93.4 ms: 1.15x faster                                                  |
| unpickle                   | 21.2 us                                                | 18.5 us: 1.15x faster                                                  |
| mdp                        | 3.97 sec                                               | 3.46 sec: 1.15x faster                                                 |
| scimark_fft                | 500 ms                                                 | 438 ms: 1.14x faster                                                   |
| sympy_str                  | 385 ms                                                 | 338 ms: 1.14x faster                                                   |
| bpe_tokeniser              | 6.59 sec                                               | 5.81 sec: 1.13x faster                                                 |
| 2to3                       | 456 ms                                                 | 404 ms: 1.13x faster                                                   |
| sqlalchemy_imperative      | 24.7 ms                                                | 21.9 ms: 1.13x faster                                                  |
| docutils                   | 4.00 sec                                               | 3.55 sec: 1.12x faster                                                 |
| xml_etree_generate         | 127 ms                                                 | 113 ms: 1.12x faster                                                   |
| sympy_sum                  | 222 ms                                                 | 198 ms: 1.12x faster                                                   |
| dulwich_log                | 100 ms                                                 | 89.6 ms: 1.12x faster                                                  |
| genshi_text                | 30.2 ms                                                | 27.0 ms: 1.12x faster                                                  |
| sympy_integrate            | 29.8 ms                                                | 26.6 ms: 1.12x faster                                                  |
| pathlib                    | 31.6 ms                                                | 28.3 ms: 1.12x faster                                                  |
| scimark_monte_carlo        | 96.4 ms                                                | 86.9 ms: 1.11x faster                                                  |
| go                         | 172 ms                                                 | 156 ms: 1.10x faster                                                   |
| sqlite_synth               | 3.87 us                                                | 3.52 us: 1.10x faster                                                  |
| scimark_sor                | 167 ms                                                 | 152 ms: 1.10x faster                                                   |
| thrift                     | 1.06 ms                                                | 965 us: 1.10x faster                                                   |
| richards_super             | 72.8 ms                                                | 66.4 ms: 1.10x faster                                                  |
| nqueens                    | 117 ms                                                 | 107 ms: 1.09x faster                                                   |
| pickle_pure_python         | 436 us                                                 | 399 us: 1.09x faster                                                   |
| logging_format             | 9.59 us                                                | 8.82 us: 1.09x faster                                                  |
| asyncio_tcp                | 923 ms                                                 | 853 ms: 1.08x faster                                                   |
| chaos                      | 84.9 ms                                                | 78.6 ms: 1.08x faster                                                  |
| xml_etree_process          | 83.7 ms                                                | 77.6 ms: 1.08x faster                                                  |
| regex_v8                   | 32.5 ms                                                | 30.2 ms: 1.08x faster                                                  |
| deepcopy_reduce            | 4.04 us                                                | 3.75 us: 1.08x faster                                                  |
| generators                 | 41.1 ms                                                | 38.4 ms: 1.07x faster                                                  |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 6.32 ms: 1.06x faster                                                  |
| genshi_xml                 | 67.6 ms                                                | 63.7 ms: 1.06x faster                                                  |
| deltablue                  | 4.27 ms                                                | 4.04 ms: 1.06x faster                                                  |
| pickle_list                | 6.97 us                                                | 6.61 us: 1.06x faster                                                  |
| pprint_pformat             | 1.98 sec                                               | 1.88 sec: 1.05x faster                                                 |
| typing_runtime_protocols   | 224 us                                                 | 214 us: 1.05x faster                                                   |
| richards                   | 60.3 ms                                                | 57.6 ms: 1.05x faster                                                  |
| asyncio_websockets         | 748 ms                                                 | 714 ms: 1.05x faster                                                   |
| json                       | 6.85 ms                                                | 6.57 ms: 1.04x faster                                                  |
| pidigits                   | 250 ms                                                 | 240 ms: 1.04x faster                                                   |
| asyncio_tcp_ssl            | 2.81 sec                                               | 2.71 sec: 1.04x faster                                                 |
| python_startup_no_site     | 17.6 ms                                                | 17.0 ms: 1.04x faster                                                  |
| pprint_safe_repr           | 967 ms                                                 | 938 ms: 1.03x faster                                                   |
| unpack_sequence            | 60.2 ns                                                | 62.7 ns: 1.04x slower                                                  |
| json_dumps                 | 14.3 ms                                                | 15.1 ms: 1.06x slower                                                  |
| telco                      | 9.59 ms                                                | 10.2 ms: 1.06x slower                                                  |
| coroutines                 | 29.5 ms                                                | 31.8 ms: 1.08x slower                                                  |
| nbody                      | 119 ms                                                 | 129 ms: 1.08x slower                                                   |
| python_startup             | 23.7 ms                                                | 28.8 ms: 1.21x slower                                                  |
| coverage                   | 95.4 ms                                                | 122 ms: 1.28x slower                                                   |
| gc_traversal               | 5.86 ms                                                | 7.93 ms: 1.35x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 3.29 ms: 1.70x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 91.4 ms: 4.42x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.12x faster                                                           |

Benchmark hidden because not significant (14): bench_thread_pool, regex_compile, unpickle_pure_python, fannkuch, django_template, scimark_lu, sympy_expand, regex_dna, meteor_contest, pickle, json_loads, unpickle_list, hexiom, mako
Ignored benchmarks (12) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20250322-3.14.0a6+-bc26f95/bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.145x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.15x