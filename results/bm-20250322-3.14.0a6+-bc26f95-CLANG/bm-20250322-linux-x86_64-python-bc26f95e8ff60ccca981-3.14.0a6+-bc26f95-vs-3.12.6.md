# Results vs. 3.12.6

- fork: python
- ref: bc26f95e8ff60ccca981
- machine: linux-x86_64
- commit hash: bc26f95
- commit date: 2025-03-22
- overall geometric mean: 1.119x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 487 ms: 1.07x slower                                                   |
| docutils       | 4.00 sec                                               | 3.52 sec: 1.14x faster                                                 |
| Geometric mean | (ref)                                                  | 1.03x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 942 ms: 2.05x faster                                                   |
| async_tree_none            | 741 ms                                                 | 363 ms: 2.04x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 910 ms: 2.03x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 489 ms: 1.90x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 375 ms: 1.88x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 521 ms: 1.88x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 716 ms: 1.50x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 782 ms: 1.41x faster                                                   |
| async_generators           | 589 ms                                                 | 542 ms: 1.09x faster                                                   |
| coroutines                 | 29.5 ms                                                | 27.2 ms: 1.09x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.46x faster                                                           |

Benchmark hidden because not significant (3): asyncio_tcp, asyncio_websockets, asyncio_tcp_ssl

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 107 ms: 1.15x faster                                                   |
| nbody          | 119 ms                                                 | 114 ms: 1.05x faster                                                   |
| pidigits       | 250 ms                                                 | 274 ms: 1.10x slower                                                   |
| Geometric mean | (ref)                                                  | 1.03x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.21 ms: 1.22x faster                                                  |
| regex_compile  | 187 ms                                                 | 165 ms: 1.13x faster                                                   |
| regex_v8       | 32.5 ms                                                | 28.9 ms: 1.12x faster                                                  |
| regex_dna      | 278 ms                                                 | 266 ms: 1.05x faster                                                   |
| Geometric mean | (ref)                                                  | 1.13x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|---------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_dict         | 52.7 us                                                | 44.9 us: 1.17x faster                                                  |
| tomli_loads         | 2.88 sec                                               | 2.50 sec: 1.16x faster                                                 |
| unpickle            | 21.2 us                                                | 19.3 us: 1.10x faster                                                  |
| xml_etree_iterparse | 169 ms                                                 | 154 ms: 1.10x faster                                                   |
| unpickle_list       | 6.83 us                                                | 6.24 us: 1.10x faster                                                  |
| pickle_list         | 6.97 us                                                | 7.37 us: 1.06x slower                                                  |
| pickle              | 16.4 us                                                | 18.4 us: 1.13x slower                                                  |
| json_dumps          | 14.3 ms                                                | 17.4 ms: 1.21x slower                                                  |
| Geometric mean      | (ref)                                                  | 1.02x faster                                                           |

Benchmark hidden because not significant (6): xml_etree_parse, json_loads, unpickle_pure_python, xml_etree_process, pickle_pure_python, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 19.4 ms: 1.10x slower                                                  |
| python_startup         | 23.7 ms                                                | 32.5 ms: 1.37x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.23x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 30.2 ms                                                | 27.9 ms: 1.08x faster                                                  |
| django_template | 44.9 ms                                                | 47.5 ms: 1.06x slower                                                  |
| genshi_xml      | 67.6 ms                                                | 71.9 ms: 1.06x slower                                                  |
| mako            | 15.7 ms                                                | 18.5 ms: 1.18x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.05x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 942 ms: 2.05x faster                                                   |
| async_tree_none            | 741 ms                                                 | 363 ms: 2.04x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 910 ms: 2.03x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 489 ms: 1.90x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 375 ms: 1.88x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 521 ms: 1.88x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 716 ms: 1.50x faster                                                   |
| spectral_norm              | 156 ms                                                 | 105 ms: 1.48x faster                                                   |
| deepcopy                   | 468 us                                                 | 319 us: 1.47x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 782 ms: 1.41x faster                                                   |
| comprehensions             | 27.1 us                                                | 19.9 us: 1.36x faster                                                  |
| deepcopy_memo              | 52.4 us                                                | 40.2 us: 1.30x faster                                                  |
| scimark_fft                | 500 ms                                                 | 390 ms: 1.28x faster                                                   |
| pyflate                    | 727 ms                                                 | 570 ms: 1.28x faster                                                   |
| regex_effbot               | 5.13 ms                                                | 4.21 ms: 1.22x faster                                                  |
| raytrace                   | 408 ms                                                 | 335 ms: 1.22x faster                                                   |
| pycparser                  | 1.79 sec                                               | 1.48 sec: 1.21x faster                                                 |
| scimark_sor                | 167 ms                                                 | 141 ms: 1.18x faster                                                   |
| scimark_monte_carlo        | 96.4 ms                                                | 81.9 ms: 1.18x faster                                                  |
| crypto_pyaes               | 107 ms                                                 | 91.2 ms: 1.18x faster                                                  |
| pylint                     | 465 ms                                                 | 396 ms: 1.17x faster                                                   |
| pickle_dict                | 52.7 us                                                | 44.9 us: 1.17x faster                                                  |
| dulwich_log                | 100 ms                                                 | 85.7 ms: 1.17x faster                                                  |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 5.73 ms: 1.17x faster                                                  |
| logging_simple             | 9.45 us                                                | 8.10 us: 1.17x faster                                                  |
| bpe_tokeniser              | 6.59 sec                                               | 5.65 sec: 1.17x faster                                                 |
| tomli_loads                | 2.88 sec                                               | 2.50 sec: 1.16x faster                                                 |
| richards_super             | 72.8 ms                                                | 63.0 ms: 1.16x faster                                                  |
| float                      | 123 ms                                                 | 107 ms: 1.15x faster                                                   |
| logging_silent             | 139 ns                                                 | 121 ns: 1.15x faster                                                   |
| sqlalchemy_declarative     | 218 ms                                                 | 191 ms: 1.14x faster                                                   |
| docutils                   | 4.00 sec                                               | 3.52 sec: 1.14x faster                                                 |
| richards                   | 60.3 ms                                                | 53.3 ms: 1.13x faster                                                  |
| regex_compile              | 187 ms                                                 | 165 ms: 1.13x faster                                                   |
| regex_v8                   | 32.5 ms                                                | 28.9 ms: 1.12x faster                                                  |
| pathlib                    | 31.6 ms                                                | 28.2 ms: 1.12x faster                                                  |
| sympy_str                  | 385 ms                                                 | 344 ms: 1.12x faster                                                   |
| deltablue                  | 4.27 ms                                                | 3.82 ms: 1.12x faster                                                  |
| typing_runtime_protocols   | 224 us                                                 | 202 us: 1.11x faster                                                   |
| deepcopy_reduce            | 4.04 us                                                | 3.65 us: 1.10x faster                                                  |
| unpickle                   | 21.2 us                                                | 19.3 us: 1.10x faster                                                  |
| sympy_sum                  | 222 ms                                                 | 202 ms: 1.10x faster                                                   |
| xml_etree_iterparse        | 169 ms                                                 | 154 ms: 1.10x faster                                                   |
| unpickle_list              | 6.83 us                                                | 6.24 us: 1.10x faster                                                  |
| hexiom                     | 8.27 ms                                                | 7.55 ms: 1.10x faster                                                  |
| async_generators           | 589 ms                                                 | 542 ms: 1.09x faster                                                   |
| coroutines                 | 29.5 ms                                                | 27.2 ms: 1.09x faster                                                  |
| chaos                      | 84.9 ms                                                | 78.2 ms: 1.08x faster                                                  |
| nqueens                    | 117 ms                                                 | 108 ms: 1.08x faster                                                   |
| genshi_text                | 30.2 ms                                                | 27.9 ms: 1.08x faster                                                  |
| generators                 | 41.1 ms                                                | 38.0 ms: 1.08x faster                                                  |
| thrift                     | 1.06 ms                                                | 983 us: 1.08x faster                                                   |
| mdp                        | 3.97 sec                                               | 3.71 sec: 1.07x faster                                                 |
| scimark_lu                 | 152 ms                                                 | 143 ms: 1.06x faster                                                   |
| go                         | 172 ms                                                 | 163 ms: 1.06x faster                                                   |
| regex_dna                  | 278 ms                                                 | 266 ms: 1.05x faster                                                   |
| nbody                      | 119 ms                                                 | 114 ms: 1.05x faster                                                   |
| django_template            | 44.9 ms                                                | 47.5 ms: 1.06x slower                                                  |
| pickle_list                | 6.97 us                                                | 7.37 us: 1.06x slower                                                  |
| genshi_xml                 | 67.6 ms                                                | 71.9 ms: 1.06x slower                                                  |
| 2to3                       | 456 ms                                                 | 487 ms: 1.07x slower                                                   |
| json                       | 6.85 ms                                                | 7.38 ms: 1.08x slower                                                  |
| coverage                   | 95.4 ms                                                | 104 ms: 1.09x slower                                                   |
| pidigits                   | 250 ms                                                 | 274 ms: 1.10x slower                                                   |
| python_startup_no_site     | 17.6 ms                                                | 19.4 ms: 1.10x slower                                                  |
| pickle                     | 16.4 us                                                | 18.4 us: 1.13x slower                                                  |
| mako                       | 15.7 ms                                                | 18.5 ms: 1.18x slower                                                  |
| unpack_sequence            | 60.2 ns                                                | 71.3 ns: 1.18x slower                                                  |
| json_dumps                 | 14.3 ms                                                | 17.4 ms: 1.21x slower                                                  |
| python_startup             | 23.7 ms                                                | 32.5 ms: 1.37x slower                                                  |
| gc_traversal               | 5.86 ms                                                | 9.28 ms: 1.58x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 4.37 ms: 2.25x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 91.9 ms: 4.44x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.09x faster                                                           |

Benchmark hidden because not significant (20): xml_etree_parse, sympy_integrate, json_loads, sqlalchemy_imperative, fannkuch, unpickle_pure_python, xml_etree_process, pprint_pformat, pprint_safe_repr, asyncio_tcp, logging_format, telco, bench_thread_pool, meteor_contest, pickle_pure_python, xml_etree_generate, asyncio_websockets, asyncio_tcp_ssl, sqlite_synth, sympy_expand
Ignored benchmarks (12) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20250322-3.14.0a6+-bc26f95-CLANG/bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.119x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.16x