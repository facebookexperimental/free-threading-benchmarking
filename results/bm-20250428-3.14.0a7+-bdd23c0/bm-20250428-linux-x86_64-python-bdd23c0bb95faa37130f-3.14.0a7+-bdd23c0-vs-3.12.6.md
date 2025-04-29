# Results vs. 3.12.6

- fork: python
- ref: bdd23c0bb95faa37130f
- machine: linux-x86_64
- commit hash: bdd23c0
- commit date: 2025-04-28
- overall geometric mean: 1.196x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 358 ms: 1.27x faster                                                   |
| docutils       | 4.00 sec                                               | 3.57 sec: 1.12x faster                                                 |
| html5lib       | 88.9 ms                                                | 76.3 ms: 1.17x faster                                                  |
| Geometric mean | (ref)                                                  | 1.19x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 829 ms: 2.33x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 424 ms: 2.30x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 820 ms: 2.25x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 443 ms: 2.10x faster                                                   |
| async_tree_none            | 741 ms                                                 | 359 ms: 2.07x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 341 ms: 2.07x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 638 ms: 1.73x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 640 ms: 1.68x faster                                                   |
| async_generators           | 589 ms                                                 | 498 ms: 1.18x faster                                                   |
| asyncio_websockets         | 748 ms                                                 | 660 ms: 1.13x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.73x faster                                                           |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 93.7 ms: 1.31x faster                                                  |
| pidigits       | 250 ms                                                 | 225 ms: 1.11x faster                                                   |
| Geometric mean | (ref)                                                  | 1.14x faster                                                           |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 3.86 ms: 1.33x faster                                                  |
| regex_v8       | 32.5 ms                                                | 26.9 ms: 1.21x faster                                                  |
| regex_compile  | 187 ms                                                 | 155 ms: 1.20x faster                                                   |
| regex_dna      | 278 ms                                                 | 253 ms: 1.10x faster                                                   |
| Geometric mean | (ref)                                                  | 1.21x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 241 ms                                                 | 191 ms: 1.26x faster                                                   |
| tomli_loads          | 2.88 sec                                               | 2.45 sec: 1.18x faster                                                 |
| xml_etree_iterparse  | 169 ms                                                 | 144 ms: 1.17x faster                                                   |
| pickle_pure_python   | 436 us                                                 | 391 us: 1.11x faster                                                   |
| xml_etree_generate   | 127 ms                                                 | 116 ms: 1.10x faster                                                   |
| unpickle_pure_python | 300 us                                                 | 274 us: 1.09x faster                                                   |
| xml_etree_process    | 83.7 ms                                                | 79.6 ms: 1.05x faster                                                  |
| Geometric mean       | (ref)                                                  | 1.10x faster                                                           |

Benchmark hidden because not significant (2): json_loads, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 11.6 ms: 1.51x faster                                                  |
| python_startup         | 23.7 ms                                                | 19.2 ms: 1.23x faster                                                  |
| Geometric mean         | (ref)                                                  | 1.37x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text    | 30.2 ms                                                | 26.3 ms: 1.15x faster                                                  |
| genshi_xml     | 67.6 ms                                                | 61.9 ms: 1.09x faster                                                  |
| mako           | 15.7 ms                                                | 16.8 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                  | 1.04x faster                                                           |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 829 ms: 2.33x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 424 ms: 2.30x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 820 ms: 2.25x faster                                                   |
| mdp                        | 3.97 sec                                               | 1.84 sec: 2.15x faster                                                 |
| async_tree_memoization_tg  | 930 ms                                                 | 443 ms: 2.10x faster                                                   |
| async_tree_none            | 741 ms                                                 | 359 ms: 2.07x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 341 ms: 2.07x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 638 ms: 1.73x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 640 ms: 1.68x faster                                                   |
| python_startup_no_site     | 17.6 ms                                                | 11.6 ms: 1.51x faster                                                  |
| deepcopy                   | 468 us                                                 | 324 us: 1.45x faster                                                   |
| deepcopy_memo              | 52.4 us                                                | 36.9 us: 1.42x faster                                                  |
| bench_thread_pool          | 3.48 ms                                                | 2.55 ms: 1.37x faster                                                  |
| dulwich_log                | 100 ms                                                 | 74.1 ms: 1.35x faster                                                  |
| regex_effbot               | 5.13 ms                                                | 3.86 ms: 1.33x faster                                                  |
| float                      | 123 ms                                                 | 93.7 ms: 1.31x faster                                                  |
| comprehensions             | 27.1 us                                                | 21.1 us: 1.28x faster                                                  |
| 2to3                       | 456 ms                                                 | 358 ms: 1.27x faster                                                   |
| pyflate                    | 727 ms                                                 | 573 ms: 1.27x faster                                                   |
| xml_etree_parse            | 241 ms                                                 | 191 ms: 1.26x faster                                                   |
| pathlib                    | 31.6 ms                                                | 25.1 ms: 1.26x faster                                                  |
| spectral_norm              | 156 ms                                                 | 125 ms: 1.25x faster                                                   |
| logging_simple             | 9.45 us                                                | 7.64 us: 1.24x faster                                                  |
| raytrace                   | 408 ms                                                 | 330 ms: 1.23x faster                                                   |
| python_startup             | 23.7 ms                                                | 19.2 ms: 1.23x faster                                                  |
| go                         | 172 ms                                                 | 140 ms: 1.23x faster                                                   |
| regex_v8                   | 32.5 ms                                                | 26.9 ms: 1.21x faster                                                  |
| pylint                     | 465 ms                                                 | 386 ms: 1.21x faster                                                   |
| regex_compile              | 187 ms                                                 | 155 ms: 1.20x faster                                                   |
| sympy_integrate            | 29.8 ms                                                | 24.7 ms: 1.20x faster                                                  |
| chaos                      | 84.9 ms                                                | 70.7 ms: 1.20x faster                                                  |
| scimark_monte_carlo        | 96.4 ms                                                | 80.3 ms: 1.20x faster                                                  |
| nqueens                    | 117 ms                                                 | 97.7 ms: 1.20x faster                                                  |
| crypto_pyaes               | 107 ms                                                 | 89.8 ms: 1.20x faster                                                  |
| pycparser                  | 1.79 sec                                               | 1.50 sec: 1.19x faster                                                 |
| bpe_tokeniser              | 6.59 sec                                               | 5.55 sec: 1.19x faster                                                 |
| deepcopy_reduce            | 4.04 us                                                | 3.41 us: 1.18x faster                                                  |
| sympy_sum                  | 222 ms                                                 | 187 ms: 1.18x faster                                                   |
| sqlite_synth               | 3.87 us                                                | 3.27 us: 1.18x faster                                                  |
| async_generators           | 589 ms                                                 | 498 ms: 1.18x faster                                                   |
| scimark_fft                | 500 ms                                                 | 424 ms: 1.18x faster                                                   |
| tomli_loads                | 2.88 sec                                               | 2.45 sec: 1.18x faster                                                 |
| xml_etree_iterparse        | 169 ms                                                 | 144 ms: 1.17x faster                                                   |
| sympy_str                  | 385 ms                                                 | 330 ms: 1.17x faster                                                   |
| html5lib                   | 88.9 ms                                                | 76.3 ms: 1.17x faster                                                  |
| scimark_sor                | 167 ms                                                 | 144 ms: 1.16x faster                                                   |
| richards_super             | 72.8 ms                                                | 63.0 ms: 1.16x faster                                                  |
| meteor_contest             | 146 ms                                                 | 127 ms: 1.15x faster                                                   |
| genshi_text                | 30.2 ms                                                | 26.3 ms: 1.15x faster                                                  |
| asyncio_websockets         | 748 ms                                                 | 660 ms: 1.13x faster                                                   |
| logging_format             | 9.59 us                                                | 8.49 us: 1.13x faster                                                  |
| typing_runtime_protocols   | 224 us                                                 | 200 us: 1.12x faster                                                   |
| docutils                   | 4.00 sec                                               | 3.57 sec: 1.12x faster                                                 |
| thrift                     | 1.06 ms                                                | 949 us: 1.12x faster                                                   |
| pickle_pure_python         | 436 us                                                 | 391 us: 1.11x faster                                                   |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 6.03 ms: 1.11x faster                                                  |
| pidigits                   | 250 ms                                                 | 225 ms: 1.11x faster                                                   |
| richards                   | 60.3 ms                                                | 54.6 ms: 1.11x faster                                                  |
| hexiom                     | 8.27 ms                                                | 7.49 ms: 1.10x faster                                                  |
| logging_silent             | 139 ns                                                 | 126 ns: 1.10x faster                                                   |
| xml_etree_generate         | 127 ms                                                 | 116 ms: 1.10x faster                                                   |
| regex_dna                  | 278 ms                                                 | 253 ms: 1.10x faster                                                   |
| unpickle_pure_python       | 300 us                                                 | 274 us: 1.09x faster                                                   |
| fannkuch                   | 540 ms                                                 | 495 ms: 1.09x faster                                                   |
| pprint_pformat             | 1.98 sec                                               | 1.81 sec: 1.09x faster                                                 |
| pprint_safe_repr           | 967 ms                                                 | 886 ms: 1.09x faster                                                   |
| genshi_xml                 | 67.6 ms                                                | 61.9 ms: 1.09x faster                                                  |
| xml_etree_process          | 83.7 ms                                                | 79.6 ms: 1.05x faster                                                  |
| sympy_expand               | 582 ms                                                 | 558 ms: 1.04x faster                                                   |
| scimark_lu                 | 152 ms                                                 | 147 ms: 1.04x faster                                                   |
| telco                      | 9.59 ms                                                | 9.25 ms: 1.04x faster                                                  |
| generators                 | 41.1 ms                                                | 39.8 ms: 1.03x faster                                                  |
| mako                       | 15.7 ms                                                | 16.8 ms: 1.07x slower                                                  |
| coverage                   | 95.4 ms                                                | 107 ms: 1.12x slower                                                   |
| gc_traversal               | 5.86 ms                                                | 7.85 ms: 1.34x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 3.53 ms: 1.82x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 75.9 ms: 3.67x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.19x faster                                                           |

Benchmark hidden because not significant (7): coroutines, django_template, nbody, json, json_loads, json_dumps, deltablue
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250428-3.14.0a7+-bdd23c0/bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.196x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.12x
- 95% likely to have a speedup of 1.11x
- 99% likely to have a speedup of 1.11x

# Memory
- memory change: 1.13x