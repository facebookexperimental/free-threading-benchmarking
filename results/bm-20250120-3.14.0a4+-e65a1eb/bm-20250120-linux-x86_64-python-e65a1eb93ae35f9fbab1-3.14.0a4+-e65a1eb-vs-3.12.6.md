# Results vs. 3.12.6

- fork: python
- ref: e65a1eb93ae35f9fbab1
- machine: linux-x86_64
- commit hash: e65a1eb
- commit date: 2025-01-20
- overall geometric mean: 1.068x faster
- HPT reliability: 98.92%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| docutils       | 4.00 sec                                               | 3.71 sec: 1.08x faster                                                 |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (2): 2to3, html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 909 ms: 2.13x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 877 ms: 2.11x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 490 ms: 1.99x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 364 ms: 1.93x faster                                                   |
| async_tree_none            | 741 ms                                                 | 388 ms: 1.91x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 500 ms: 1.86x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 649 ms: 1.70x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 660 ms: 1.63x faster                                                   |
| async_generators           | 589 ms                                                 | 539 ms: 1.09x faster                                                   |
| asyncio_websockets         | 748 ms                                                 | 716 ms: 1.04x faster                                                   |
| coroutines                 | 29.5 ms                                                | 31.1 ms: 1.05x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.61x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 111 ms: 1.11x faster                                                   |
| nbody          | 119 ms                                                 | 129 ms: 1.09x slower                                                   |
| Geometric mean | (ref)                                                  | 1.00x slower                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.79 ms: 1.07x faster                                                  |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (3): regex_compile, regex_dna, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 241 ms                                                 | 215 ms: 1.12x faster                                                   |
| tomli_loads          | 2.88 sec                                               | 2.61 sec: 1.10x faster                                                 |
| xml_etree_iterparse  | 169 ms                                                 | 156 ms: 1.09x faster                                                   |
| unpickle_pure_python | 300 us                                                 | 316 us: 1.06x slower                                                   |
| xml_etree_process    | 83.7 ms                                                | 88.7 ms: 1.06x slower                                                  |
| json_dumps           | 14.3 ms                                                | 15.6 ms: 1.09x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (3): xml_etree_generate, pickle_pure_python, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 18.4 ms: 1.05x slower                                                  |
| python_startup         | 23.7 ms                                                | 30.3 ms: 1.28x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.16x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 30.2 ms                                                | 28.5 ms: 1.06x faster                                                  |
| django_template | 44.9 ms                                                | 49.7 ms: 1.11x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.02x slower                                                           |

Benchmark hidden because not significant (2): genshi_xml, mako

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 909 ms: 2.13x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 877 ms: 2.11x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 490 ms: 1.99x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 364 ms: 1.93x faster                                                   |
| async_tree_none            | 741 ms                                                 | 388 ms: 1.91x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 500 ms: 1.86x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 649 ms: 1.70x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 660 ms: 1.63x faster                                                   |
| sqlalchemy_declarative     | 218 ms                                                 | 164 ms: 1.32x faster                                                   |
| deepcopy_memo              | 52.4 us                                                | 40.1 us: 1.31x faster                                                  |
| deepcopy                   | 468 us                                                 | 360 us: 1.30x faster                                                   |
| comprehensions             | 27.1 us                                                | 22.1 us: 1.22x faster                                                  |
| deepcopy_reduce            | 4.04 us                                                | 3.38 us: 1.19x faster                                                  |
| pycparser                  | 1.79 sec                                               | 1.56 sec: 1.15x faster                                                 |
| go                         | 172 ms                                                 | 151 ms: 1.14x faster                                                   |
| sympy_sum                  | 222 ms                                                 | 197 ms: 1.13x faster                                                   |
| pylint                     | 465 ms                                                 | 413 ms: 1.12x faster                                                   |
| xml_etree_parse            | 241 ms                                                 | 215 ms: 1.12x faster                                                   |
| bpe_tokeniser              | 6.59 sec                                               | 5.89 sec: 1.12x faster                                                 |
| float                      | 123 ms                                                 | 111 ms: 1.11x faster                                                   |
| tomli_loads                | 2.88 sec                                               | 2.61 sec: 1.10x faster                                                 |
| scimark_fft                | 500 ms                                                 | 453 ms: 1.10x faster                                                   |
| async_generators           | 589 ms                                                 | 539 ms: 1.09x faster                                                   |
| richards_super             | 72.8 ms                                                | 66.8 ms: 1.09x faster                                                  |
| spectral_norm              | 156 ms                                                 | 143 ms: 1.09x faster                                                   |
| xml_etree_iterparse        | 169 ms                                                 | 156 ms: 1.09x faster                                                   |
| docutils                   | 4.00 sec                                               | 3.71 sec: 1.08x faster                                                 |
| crypto_pyaes               | 107 ms                                                 | 99.8 ms: 1.08x faster                                                  |
| pyflate                    | 727 ms                                                 | 678 ms: 1.07x faster                                                   |
| regex_effbot               | 5.13 ms                                                | 4.79 ms: 1.07x faster                                                  |
| raytrace                   | 408 ms                                                 | 383 ms: 1.07x faster                                                   |
| sqlglot_transpile          | 2.34 ms                                                | 2.20 ms: 1.06x faster                                                  |
| genshi_text                | 30.2 ms                                                | 28.5 ms: 1.06x faster                                                  |
| fannkuch                   | 540 ms                                                 | 514 ms: 1.05x faster                                                   |
| asyncio_websockets         | 748 ms                                                 | 716 ms: 1.04x faster                                                   |
| mdp                        | 3.97 sec                                               | 3.84 sec: 1.03x faster                                                 |
| pprint_pformat             | 1.98 sec                                               | 2.06 sec: 1.04x slower                                                 |
| python_startup_no_site     | 17.6 ms                                                | 18.4 ms: 1.05x slower                                                  |
| coroutines                 | 29.5 ms                                                | 31.1 ms: 1.05x slower                                                  |
| unpickle_pure_python       | 300 us                                                 | 316 us: 1.06x slower                                                   |
| xml_etree_process          | 83.7 ms                                                | 88.7 ms: 1.06x slower                                                  |
| pprint_safe_repr           | 967 ms                                                 | 1.02 sec: 1.06x slower                                                 |
| hexiom                     | 8.27 ms                                                | 8.85 ms: 1.07x slower                                                  |
| nbody                      | 119 ms                                                 | 129 ms: 1.09x slower                                                   |
| json_dumps                 | 14.3 ms                                                | 15.6 ms: 1.09x slower                                                  |
| bench_thread_pool          | 3.48 ms                                                | 3.81 ms: 1.09x slower                                                  |
| thrift                     | 1.06 ms                                                | 1.17 ms: 1.10x slower                                                  |
| django_template            | 44.9 ms                                                | 49.7 ms: 1.11x slower                                                  |
| sqlglot_optimize           | 76.0 ms                                                | 84.2 ms: 1.11x slower                                                  |
| json                       | 6.85 ms                                                | 7.94 ms: 1.16x slower                                                  |
| logging_format             | 9.59 us                                                | 11.2 us: 1.16x slower                                                  |
| typing_runtime_protocols   | 224 us                                                 | 263 us: 1.17x slower                                                   |
| telco                      | 9.59 ms                                                | 11.8 ms: 1.23x slower                                                  |
| coverage                   | 95.4 ms                                                | 120 ms: 1.26x slower                                                   |
| python_startup             | 23.7 ms                                                | 30.3 ms: 1.28x slower                                                  |
| gc_traversal               | 5.86 ms                                                | 9.71 ms: 1.66x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 3.93 ms: 2.03x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 102 ms: 4.94x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                           |

Benchmark hidden because not significant (32): pathlib, nqueens, sympy_integrate, logging_simple, sqlalchemy_imperative, regex_compile, xml_etree_generate, sqlglot_parse, sqlite_synth, meteor_contest, scimark_sparse_mat_mult, logging_silent, scimark_monte_carlo, deltablue, richards, pickle_pure_python, scimark_sor, html5lib, genshi_xml, regex_dna, sqlglot_normalize, mako, chaos, pidigits, scimark_lu, sympy_str, regex_v8, sympy_expand, generators, 2to3, dulwich_log, json_loads
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250120-3.14.0a4+-e65a1eb/bm-20250120-linux-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.068x faster

# HPT report

- Reliability score: 98.92% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.13x