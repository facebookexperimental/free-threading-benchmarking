# Results vs. 3.12.6

- fork: python
- ref: 9211b3dabeacb92713ac
- machine: linux-x86_64
- commit hash: 9211b3d
- commit date: 2025-02-28
- overall geometric mean: 1.126x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| docutils       | 4.00 sec                                               | 3.61 sec: 1.11x faster                                                 |
| html5lib       | 88.9 ms                                                | 84.6 ms: 1.05x faster                                                  |
| Geometric mean | (ref)                                                  | 1.07x faster                                                           |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 882 ms: 2.19x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 869 ms: 2.13x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 475 ms: 2.06x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 469 ms: 1.98x faster                                                   |
| async_tree_none            | 741 ms                                                 | 378 ms: 1.96x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 361 ms: 1.95x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 660 ms: 1.63x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 686 ms: 1.60x faster                                                   |
| async_generators           | 589 ms                                                 | 495 ms: 1.19x faster                                                   |
| asyncio_websockets         | 748 ms                                                 | 724 ms: 1.03x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.64x faster                                                           |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 106 ms: 1.16x faster                                                   |
| Geometric mean | (ref)                                                  | 1.05x faster                                                           |

Benchmark hidden because not significant (2): pidigits, nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.57 ms: 1.12x faster                                                  |
| regex_compile  | 187 ms                                                 | 174 ms: 1.07x faster                                                   |
| Geometric mean | (ref)                                                  | 1.03x faster                                                           |

Benchmark hidden because not significant (2): regex_dna, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 241 ms                                                 | 201 ms: 1.20x faster                                                   |
| xml_etree_iterparse  | 169 ms                                                 | 144 ms: 1.17x faster                                                   |
| tomli_loads          | 2.88 sec                                               | 2.53 sec: 1.14x faster                                                 |
| xml_etree_generate   | 127 ms                                                 | 115 ms: 1.10x faster                                                   |
| unpickle_pure_python | 300 us                                                 | 281 us: 1.07x faster                                                   |
| pickle_pure_python   | 436 us                                                 | 409 us: 1.06x faster                                                   |
| Geometric mean       | (ref)                                                  | 1.08x faster                                                           |

Benchmark hidden because not significant (3): xml_etree_process, json_loads, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 15.2 ms: 1.16x faster                                                  |
| python_startup         | 23.7 ms                                                | 26.0 ms: 1.10x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.03x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 44.9 ms                                                | 43.4 ms: 1.03x faster                                                  |
| Geometric mean  | (ref)                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (3): genshi_text, mako, genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 882 ms: 2.19x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 869 ms: 2.13x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 475 ms: 2.06x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 469 ms: 1.98x faster                                                   |
| async_tree_none            | 741 ms                                                 | 378 ms: 1.96x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 361 ms: 1.95x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 660 ms: 1.63x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 686 ms: 1.60x faster                                                   |
| deepcopy_memo              | 52.4 us                                                | 39.1 us: 1.34x faster                                                  |
| deepcopy                   | 468 us                                                 | 361 us: 1.29x faster                                                   |
| sqlalchemy_declarative     | 218 ms                                                 | 169 ms: 1.29x faster                                                   |
| comprehensions             | 27.1 us                                                | 21.5 us: 1.26x faster                                                  |
| logging_simple             | 9.45 us                                                | 7.64 us: 1.24x faster                                                  |
| pylint                     | 465 ms                                                 | 384 ms: 1.21x faster                                                   |
| spectral_norm              | 156 ms                                                 | 129 ms: 1.20x faster                                                   |
| pyflate                    | 727 ms                                                 | 606 ms: 1.20x faster                                                   |
| xml_etree_parse            | 241 ms                                                 | 201 ms: 1.20x faster                                                   |
| deepcopy_reduce            | 4.04 us                                                | 3.38 us: 1.19x faster                                                  |
| async_generators           | 589 ms                                                 | 495 ms: 1.19x faster                                                   |
| pycparser                  | 1.79 sec                                               | 1.53 sec: 1.17x faster                                                 |
| xml_etree_iterparse        | 169 ms                                                 | 144 ms: 1.17x faster                                                   |
| go                         | 172 ms                                                 | 147 ms: 1.17x faster                                                   |
| float                      | 123 ms                                                 | 106 ms: 1.16x faster                                                   |
| python_startup_no_site     | 17.6 ms                                                | 15.2 ms: 1.16x faster                                                  |
| bpe_tokeniser              | 6.59 sec                                               | 5.74 sec: 1.15x faster                                                 |
| thrift                     | 1.06 ms                                                | 927 us: 1.14x faster                                                   |
| tomli_loads                | 2.88 sec                                               | 2.53 sec: 1.14x faster                                                 |
| bench_thread_pool          | 3.48 ms                                                | 3.07 ms: 1.13x faster                                                  |
| sympy_sum                  | 222 ms                                                 | 198 ms: 1.12x faster                                                   |
| regex_effbot               | 5.13 ms                                                | 4.57 ms: 1.12x faster                                                  |
| richards                   | 60.3 ms                                                | 54.1 ms: 1.11x faster                                                  |
| sqlglot_normalize          | 157 ms                                                 | 142 ms: 1.11x faster                                                   |
| docutils                   | 4.00 sec                                               | 3.61 sec: 1.11x faster                                                 |
| raytrace                   | 408 ms                                                 | 369 ms: 1.10x faster                                                   |
| chaos                      | 84.9 ms                                                | 76.8 ms: 1.10x faster                                                  |
| xml_etree_generate         | 127 ms                                                 | 115 ms: 1.10x faster                                                   |
| scimark_monte_carlo        | 96.4 ms                                                | 87.4 ms: 1.10x faster                                                  |
| mdp                        | 3.97 sec                                               | 3.61 sec: 1.10x faster                                                 |
| scimark_fft                | 500 ms                                                 | 457 ms: 1.09x faster                                                   |
| sqlalchemy_imperative      | 24.7 ms                                                | 22.6 ms: 1.09x faster                                                  |
| pathlib                    | 31.6 ms                                                | 29.0 ms: 1.09x faster                                                  |
| dulwich_log                | 100 ms                                                 | 92.1 ms: 1.09x faster                                                  |
| crypto_pyaes               | 107 ms                                                 | 98.7 ms: 1.09x faster                                                  |
| hexiom                     | 8.27 ms                                                | 7.65 ms: 1.08x faster                                                  |
| sympy_str                  | 385 ms                                                 | 357 ms: 1.08x faster                                                   |
| pprint_pformat             | 1.98 sec                                               | 1.84 sec: 1.08x faster                                                 |
| regex_compile              | 187 ms                                                 | 174 ms: 1.07x faster                                                   |
| nqueens                    | 117 ms                                                 | 109 ms: 1.07x faster                                                   |
| unpickle_pure_python       | 300 us                                                 | 281 us: 1.07x faster                                                   |
| scimark_sor                | 167 ms                                                 | 156 ms: 1.07x faster                                                   |
| pickle_pure_python         | 436 us                                                 | 409 us: 1.06x faster                                                   |
| sqlite_synth               | 3.87 us                                                | 3.65 us: 1.06x faster                                                  |
| fannkuch                   | 540 ms                                                 | 510 ms: 1.06x faster                                                   |
| typing_runtime_protocols   | 224 us                                                 | 212 us: 1.06x faster                                                   |
| sqlglot_transpile          | 2.34 ms                                                | 2.21 ms: 1.06x faster                                                  |
| logging_format             | 9.59 us                                                | 9.08 us: 1.06x faster                                                  |
| pprint_safe_repr           | 967 ms                                                 | 916 ms: 1.06x faster                                                   |
| deltablue                  | 4.27 ms                                                | 4.06 ms: 1.05x faster                                                  |
| html5lib                   | 88.9 ms                                                | 84.6 ms: 1.05x faster                                                  |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 6.39 ms: 1.05x faster                                                  |
| django_template            | 44.9 ms                                                | 43.4 ms: 1.03x faster                                                  |
| asyncio_websockets         | 748 ms                                                 | 724 ms: 1.03x faster                                                   |
| scimark_lu                 | 152 ms                                                 | 158 ms: 1.04x slower                                                   |
| python_startup             | 23.7 ms                                                | 26.0 ms: 1.10x slower                                                  |
| coverage                   | 95.4 ms                                                | 111 ms: 1.16x slower                                                   |
| gc_traversal               | 5.86 ms                                                | 7.85 ms: 1.34x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 3.69 ms: 1.90x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 94.8 ms: 4.58x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.10x faster                                                           |

Benchmark hidden because not significant (22): 2to3, logging_silent, genshi_text, sympy_integrate, sqlglot_optimize, pidigits, meteor_contest, richards_super, sqlglot_parse, xml_etree_process, telco, json_loads, mako, genshi_xml, sympy_expand, json_dumps, nbody, generators, json, regex_dna, coroutines, regex_v8
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250228-3.14.0a5+-9211b3d/bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.126x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.13x