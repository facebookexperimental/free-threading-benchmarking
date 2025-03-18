# Results vs. 3.12.6

- fork: python
- ref: a936af924efc6e2fb59e
- machine: linux-x86_64
- commit hash: a936af9
- commit date: 2025-03-17
- overall geometric mean: 1.018x slower
- HPT reliability: 99.74%
- HPT 99th percentile: 1.02x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 540 ms: 1.18x slower                                                   |
| docutils       | 4.00 sec                                               | 4.13 sec: 1.03x slower                                                 |
| html5lib       | 88.9 ms                                                | 98.0 ms: 1.10x slower                                                  |
| Geometric mean | (ref)                                                  | 1.10x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 733 ms: 2.64x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 812 ms: 2.27x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 314 ms: 2.24x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 454 ms: 2.05x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 501 ms: 1.95x faster                                                   |
| async_tree_none            | 741 ms                                                 | 390 ms: 1.90x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 681 ms: 1.62x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 732 ms: 1.47x faster                                                   |
| asyncio_websockets         | 748 ms                                                 | 727 ms: 1.03x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.65x faster                                                           |

Benchmark hidden because not significant (2): async_generators, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 114 ms: 1.08x faster                                                   |
| pidigits       | 250 ms                                                 | 241 ms: 1.04x faster                                                   |
| nbody          | 119 ms                                                 | 172 ms: 1.45x slower                                                   |
| Geometric mean | (ref)                                                  | 1.09x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.25 ms: 1.21x faster                                                  |
| regex_dna      | 278 ms                                                 | 304 ms: 1.09x slower                                                   |
| regex_compile  | 187 ms                                                 | 212 ms: 1.14x slower                                                   |
| Geometric mean | (ref)                                                  | 1.00x slower                                                           |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 169 ms                                                 | 140 ms: 1.21x faster                                                   |
| xml_etree_parse      | 241 ms                                                 | 206 ms: 1.17x faster                                                   |
| tomli_loads          | 2.88 sec                                               | 3.09 sec: 1.07x slower                                                 |
| unpickle_pure_python | 300 us                                                 | 321 us: 1.07x slower                                                   |
| xml_etree_process    | 83.7 ms                                                | 92.3 ms: 1.10x slower                                                  |
| xml_etree_generate   | 127 ms                                                 | 145 ms: 1.14x slower                                                   |
| json_dumps           | 14.3 ms                                                | 16.8 ms: 1.17x slower                                                  |
| pickle_pure_python   | 436 us                                                 | 523 us: 1.20x slower                                                   |
| json_loads           | 37.9 us                                                | 47.8 us: 1.26x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.07x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 25.6 ms: 1.45x slower                                                  |
| python_startup         | 23.7 ms                                                | 34.9 ms: 1.47x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.46x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 44.9 ms                                                | 55.3 ms: 1.23x slower                                                  |
| genshi_xml      | 67.6 ms                                                | 87.3 ms: 1.29x slower                                                  |
| genshi_text     | 30.2 ms                                                | 39.5 ms: 1.31x slower                                                  |
| mako            | 15.7 ms                                                | 25.0 ms: 1.59x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.35x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 733 ms: 2.64x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 812 ms: 2.27x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 314 ms: 2.24x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 454 ms: 2.05x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 501 ms: 1.95x faster                                                   |
| async_tree_none            | 741 ms                                                 | 390 ms: 1.90x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 681 ms: 1.62x faster                                                   |
| gc_traversal               | 5.86 ms                                                | 3.97 ms: 1.48x faster                                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 732 ms: 1.47x faster                                                   |
| regex_effbot               | 5.13 ms                                                | 4.25 ms: 1.21x faster                                                  |
| xml_etree_iterparse        | 169 ms                                                 | 140 ms: 1.21x faster                                                   |
| deepcopy                   | 468 us                                                 | 395 us: 1.19x faster                                                   |
| xml_etree_parse            | 241 ms                                                 | 206 ms: 1.17x faster                                                   |
| dulwich_log                | 100 ms                                                 | 87.7 ms: 1.14x faster                                                  |
| pycparser                  | 1.79 sec                                               | 1.57 sec: 1.14x faster                                                 |
| sqlite_synth               | 3.87 us                                                | 3.57 us: 1.09x faster                                                  |
| deepcopy_memo              | 52.4 us                                                | 48.4 us: 1.08x faster                                                  |
| float                      | 123 ms                                                 | 114 ms: 1.08x faster                                                   |
| spectral_norm              | 156 ms                                                 | 147 ms: 1.06x faster                                                   |
| comprehensions             | 27.1 us                                                | 25.7 us: 1.06x faster                                                  |
| logging_silent             | 139 ns                                                 | 133 ns: 1.05x faster                                                   |
| pidigits                   | 250 ms                                                 | 241 ms: 1.04x faster                                                   |
| asyncio_websockets         | 748 ms                                                 | 727 ms: 1.03x faster                                                   |
| docutils                   | 4.00 sec                                               | 4.13 sec: 1.03x slower                                                 |
| scimark_sor                | 167 ms                                                 | 174 ms: 1.05x slower                                                   |
| raytrace                   | 408 ms                                                 | 430 ms: 1.06x slower                                                   |
| mdp                        | 3.97 sec                                               | 4.22 sec: 1.06x slower                                                 |
| scimark_fft                | 500 ms                                                 | 533 ms: 1.06x slower                                                   |
| crypto_pyaes               | 107 ms                                                 | 114 ms: 1.07x slower                                                   |
| tomli_loads                | 2.88 sec                                               | 3.09 sec: 1.07x slower                                                 |
| unpickle_pure_python       | 300 us                                                 | 321 us: 1.07x slower                                                   |
| json                       | 6.85 ms                                                | 7.34 ms: 1.07x slower                                                  |
| generators                 | 41.1 ms                                                | 44.2 ms: 1.08x slower                                                  |
| sqlglot_optimize           | 76.0 ms                                                | 82.4 ms: 1.09x slower                                                  |
| regex_dna                  | 278 ms                                                 | 304 ms: 1.09x slower                                                   |
| html5lib                   | 88.9 ms                                                | 98.0 ms: 1.10x slower                                                  |
| xml_etree_process          | 83.7 ms                                                | 92.3 ms: 1.10x slower                                                  |
| bench_thread_pool          | 3.48 ms                                                | 3.85 ms: 1.11x slower                                                  |
| nqueens                    | 117 ms                                                 | 130 ms: 1.11x slower                                                   |
| chaos                      | 84.9 ms                                                | 94.2 ms: 1.11x slower                                                  |
| scimark_monte_carlo        | 96.4 ms                                                | 107 ms: 1.11x slower                                                   |
| sympy_str                  | 385 ms                                                 | 429 ms: 1.11x slower                                                   |
| bpe_tokeniser              | 6.59 sec                                               | 7.38 sec: 1.12x slower                                                 |
| sqlglot_transpile          | 2.34 ms                                                | 2.62 ms: 1.12x slower                                                  |
| go                         | 172 ms                                                 | 194 ms: 1.13x slower                                                   |
| sympy_sum                  | 222 ms                                                 | 251 ms: 1.13x slower                                                   |
| regex_compile              | 187 ms                                                 | 212 ms: 1.14x slower                                                   |
| xml_etree_generate         | 127 ms                                                 | 145 ms: 1.14x slower                                                   |
| sympy_integrate            | 29.8 ms                                                | 34.0 ms: 1.14x slower                                                  |
| logging_format             | 9.59 us                                                | 11.1 us: 1.15x slower                                                  |
| pprint_safe_repr           | 967 ms                                                 | 1.12 sec: 1.16x slower                                                 |
| pprint_pformat             | 1.98 sec                                               | 2.29 sec: 1.16x slower                                                 |
| richards                   | 60.3 ms                                                | 70.1 ms: 1.16x slower                                                  |
| logging_simple             | 9.45 us                                                | 11.0 us: 1.16x slower                                                  |
| fannkuch                   | 540 ms                                                 | 631 ms: 1.17x slower                                                   |
| json_dumps                 | 14.3 ms                                                | 16.8 ms: 1.17x slower                                                  |
| 2to3                       | 456 ms                                                 | 540 ms: 1.18x slower                                                   |
| meteor_contest             | 146 ms                                                 | 174 ms: 1.19x slower                                                   |
| richards_super             | 72.8 ms                                                | 86.4 ms: 1.19x slower                                                  |
| deltablue                  | 4.27 ms                                                | 5.08 ms: 1.19x slower                                                  |
| sympy_expand               | 582 ms                                                 | 696 ms: 1.20x slower                                                   |
| thrift                     | 1.06 ms                                                | 1.27 ms: 1.20x slower                                                  |
| pickle_pure_python         | 436 us                                                 | 523 us: 1.20x slower                                                   |
| scimark_lu                 | 152 ms                                                 | 183 ms: 1.20x slower                                                   |
| hexiom                     | 8.27 ms                                                | 9.98 ms: 1.21x slower                                                  |
| typing_runtime_protocols   | 224 us                                                 | 275 us: 1.23x slower                                                   |
| django_template            | 44.9 ms                                                | 55.3 ms: 1.23x slower                                                  |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 8.25 ms: 1.23x slower                                                  |
| json_loads                 | 37.9 us                                                | 47.8 us: 1.26x slower                                                  |
| sqlalchemy_imperative      | 24.7 ms                                                | 31.2 ms: 1.26x slower                                                  |
| telco                      | 9.59 ms                                                | 12.2 ms: 1.27x slower                                                  |
| sqlglot_parse              | 1.79 ms                                                | 2.30 ms: 1.28x slower                                                  |
| genshi_xml                 | 67.6 ms                                                | 87.3 ms: 1.29x slower                                                  |
| genshi_text                | 30.2 ms                                                | 39.5 ms: 1.31x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 2.72 ms: 1.40x slower                                                  |
| nbody                      | 119 ms                                                 | 172 ms: 1.45x slower                                                   |
| python_startup_no_site     | 17.6 ms                                                | 25.6 ms: 1.45x slower                                                  |
| python_startup             | 23.7 ms                                                | 34.9 ms: 1.47x slower                                                  |
| coverage                   | 95.4 ms                                                | 141 ms: 1.48x slower                                                   |
| mako                       | 15.7 ms                                                | 25.0 ms: 1.59x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 84.8 ms: 4.10x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.04x slower                                                           |

Benchmark hidden because not significant (9): pylint, pyflate, regex_v8, pathlib, sqlglot_normalize, deepcopy_reduce, async_generators, coroutines, sqlalchemy_declarative
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250317-3.14.0a6+-a936af9-NOGIL/bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.018x slower

# HPT report

- Reliability score: 99.74% likely to be slow
- 90% likely to have a slowdown of 1.04x
- 95% likely to have a slowdown of 1.03x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: 1.36x