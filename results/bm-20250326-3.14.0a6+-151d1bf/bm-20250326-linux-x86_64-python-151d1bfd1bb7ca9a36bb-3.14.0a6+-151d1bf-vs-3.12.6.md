# Results vs. 3.12.6

- fork: python
- ref: 151d1bfd1bb7ca9a36bb
- machine: linux-x86_64
- commit hash: 151d1bf
- commit date: 2025-03-26
- overall geometric mean: 1.113x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| docutils       | 4.00 sec                                               | 3.58 sec: 1.12x faster                                                 |
| Geometric mean | (ref)                                                  | 1.04x faster                                                           |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 922 ms: 2.10x faster                                                   |
| async_tree_none            | 741 ms                                                 | 357 ms: 2.08x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 893 ms: 2.07x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 491 ms: 1.99x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 361 ms: 1.95x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 491 ms: 1.89x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 647 ms: 1.70x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 659 ms: 1.64x faster                                                   |
| async_generators           | 589 ms                                                 | 519 ms: 1.14x faster                                                   |
| coroutines                 | 29.5 ms                                                | 32.0 ms: 1.08x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.61x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 105 ms: 1.17x faster                                                   |
| pidigits       | 250 ms                                                 | 237 ms: 1.05x faster                                                   |
| nbody          | 119 ms                                                 | 126 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                  | 1.05x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 187 ms                                                 | 168 ms: 1.11x faster                                                   |
| regex_effbot   | 5.13 ms                                                | 4.70 ms: 1.09x faster                                                  |
| regex_v8       | 32.5 ms                                                | 30.8 ms: 1.05x faster                                                  |
| Geometric mean | (ref)                                                  | 1.05x faster                                                           |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|---------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse     | 241 ms                                                 | 207 ms: 1.16x faster                                                   |
| xml_etree_generate  | 127 ms                                                 | 111 ms: 1.14x faster                                                   |
| tomli_loads         | 2.88 sec                                               | 2.53 sec: 1.14x faster                                                 |
| xml_etree_iterparse | 169 ms                                                 | 157 ms: 1.08x faster                                                   |
| json_dumps          | 14.3 ms                                                | 15.4 ms: 1.08x slower                                                  |
| Geometric mean      | (ref)                                                  | 1.05x faster                                                           |

Benchmark hidden because not significant (4): unpickle_pure_python, pickle_pure_python, xml_etree_process, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup | 23.7 ms                                                | 29.9 ms: 1.26x slower                                                  |
| Geometric mean | (ref)                                                  | 1.14x slower                                                           |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 30.2 ms                                                | 28.6 ms: 1.06x faster                                                  |
| genshi_xml      | 67.6 ms                                                | 64.3 ms: 1.05x faster                                                  |
| django_template | 44.9 ms                                                | 43.4 ms: 1.04x faster                                                  |
| mako            | 15.7 ms                                                | 16.6 ms: 1.06x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.02x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 922 ms: 2.10x faster                                                   |
| async_tree_none            | 741 ms                                                 | 357 ms: 2.08x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 893 ms: 2.07x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 491 ms: 1.99x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 361 ms: 1.95x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 491 ms: 1.89x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 647 ms: 1.70x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 659 ms: 1.64x faster                                                   |
| deepcopy                   | 468 us                                                 | 330 us: 1.42x faster                                                   |
| deepcopy_memo              | 52.4 us                                                | 37.8 us: 1.39x faster                                                  |
| comprehensions             | 27.1 us                                                | 21.0 us: 1.29x faster                                                  |
| spectral_norm              | 156 ms                                                 | 129 ms: 1.21x faster                                                   |
| dulwich_log                | 100 ms                                                 | 85.2 ms: 1.18x faster                                                  |
| float                      | 123 ms                                                 | 105 ms: 1.17x faster                                                   |
| pyflate                    | 727 ms                                                 | 623 ms: 1.17x faster                                                   |
| xml_etree_parse            | 241 ms                                                 | 207 ms: 1.16x faster                                                   |
| raytrace                   | 408 ms                                                 | 351 ms: 1.16x faster                                                   |
| xml_etree_generate         | 127 ms                                                 | 111 ms: 1.14x faster                                                   |
| pathlib                    | 31.6 ms                                                | 27.6 ms: 1.14x faster                                                  |
| logging_simple             | 9.45 us                                                | 8.26 us: 1.14x faster                                                  |
| deepcopy_reduce            | 4.04 us                                                | 3.53 us: 1.14x faster                                                  |
| sqlalchemy_declarative     | 218 ms                                                 | 191 ms: 1.14x faster                                                   |
| tomli_loads                | 2.88 sec                                               | 2.53 sec: 1.14x faster                                                 |
| logging_silent             | 139 ns                                                 | 122 ns: 1.14x faster                                                   |
| async_generators           | 589 ms                                                 | 519 ms: 1.14x faster                                                   |
| sqlalchemy_imperative      | 24.7 ms                                                | 21.8 ms: 1.13x faster                                                  |
| pycparser                  | 1.79 sec                                               | 1.59 sec: 1.12x faster                                                 |
| pylint                     | 465 ms                                                 | 415 ms: 1.12x faster                                                   |
| docutils                   | 4.00 sec                                               | 3.58 sec: 1.12x faster                                                 |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 6.01 ms: 1.11x faster                                                  |
| scimark_fft                | 500 ms                                                 | 449 ms: 1.11x faster                                                   |
| mdp                        | 3.97 sec                                               | 3.57 sec: 1.11x faster                                                 |
| go                         | 172 ms                                                 | 155 ms: 1.11x faster                                                   |
| regex_compile              | 187 ms                                                 | 168 ms: 1.11x faster                                                   |
| scimark_sor                | 167 ms                                                 | 151 ms: 1.10x faster                                                   |
| chaos                      | 84.9 ms                                                | 77.3 ms: 1.10x faster                                                  |
| regex_effbot               | 5.13 ms                                                | 4.70 ms: 1.09x faster                                                  |
| sympy_sum                  | 222 ms                                                 | 204 ms: 1.09x faster                                                   |
| bpe_tokeniser              | 6.59 sec                                               | 6.06 sec: 1.09x faster                                                 |
| nqueens                    | 117 ms                                                 | 108 ms: 1.08x faster                                                   |
| sympy_integrate            | 29.8 ms                                                | 27.5 ms: 1.08x faster                                                  |
| xml_etree_iterparse        | 169 ms                                                 | 157 ms: 1.08x faster                                                   |
| crypto_pyaes               | 107 ms                                                 | 100 ms: 1.07x faster                                                   |
| sympy_str                  | 385 ms                                                 | 359 ms: 1.07x faster                                                   |
| scimark_monte_carlo        | 96.4 ms                                                | 90.3 ms: 1.07x faster                                                  |
| sqlite_synth               | 3.87 us                                                | 3.65 us: 1.06x faster                                                  |
| genshi_text                | 30.2 ms                                                | 28.6 ms: 1.06x faster                                                  |
| pidigits                   | 250 ms                                                 | 237 ms: 1.05x faster                                                   |
| regex_v8                   | 32.5 ms                                                | 30.8 ms: 1.05x faster                                                  |
| genshi_xml                 | 67.6 ms                                                | 64.3 ms: 1.05x faster                                                  |
| typing_runtime_protocols   | 224 us                                                 | 214 us: 1.05x faster                                                   |
| pprint_safe_repr           | 967 ms                                                 | 922 ms: 1.05x faster                                                   |
| pprint_pformat             | 1.98 sec                                               | 1.90 sec: 1.04x faster                                                 |
| deltablue                  | 4.27 ms                                                | 4.10 ms: 1.04x faster                                                  |
| django_template            | 44.9 ms                                                | 43.4 ms: 1.04x faster                                                  |
| sympy_expand               | 582 ms                                                 | 605 ms: 1.04x slower                                                   |
| nbody                      | 119 ms                                                 | 126 ms: 1.05x slower                                                   |
| mako                       | 15.7 ms                                                | 16.6 ms: 1.06x slower                                                  |
| json_dumps                 | 14.3 ms                                                | 15.4 ms: 1.08x slower                                                  |
| coroutines                 | 29.5 ms                                                | 32.0 ms: 1.08x slower                                                  |
| telco                      | 9.59 ms                                                | 10.7 ms: 1.12x slower                                                  |
| python_startup             | 23.7 ms                                                | 29.9 ms: 1.26x slower                                                  |
| coverage                   | 95.4 ms                                                | 127 ms: 1.33x slower                                                   |
| gc_traversal               | 5.86 ms                                                | 8.37 ms: 1.43x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 3.76 ms: 1.94x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 94.5 ms: 4.57x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.09x faster                                                           |

Benchmark hidden because not significant (19): logging_format, richards_super, thrift, unpickle_pure_python, meteor_contest, hexiom, richards, pickle_pure_python, xml_etree_process, generators, fannkuch, asyncio_websockets, json, json_loads, python_startup_no_site, bench_thread_pool, scimark_lu, 2to3, regex_dna
Ignored benchmarks (20) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250326-3.14.0a6+-151d1bf/bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.113x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.15x