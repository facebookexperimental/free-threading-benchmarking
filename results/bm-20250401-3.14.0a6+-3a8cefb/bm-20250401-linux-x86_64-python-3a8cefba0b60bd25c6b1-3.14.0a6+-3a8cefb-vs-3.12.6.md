# Results vs. 3.12.6

- fork: python
- ref: 3a8cefba0b60bd25c6b1
- machine: linux-x86_64
- commit hash: 3a8cefb
- commit date: 2025-04-01
- overall geometric mean: 1.128x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| docutils       | 4.00 sec                                               | 3.68 sec: 1.09x faster                                                 |
| Geometric mean | (ref)                                                  | 1.04x faster                                                           |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_memoization     | 977 ms                                                 | 449 ms: 2.18x faster                                                   |
| async_tree_io_tg           | 1.93 sec                                               | 890 ms: 2.17x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 883 ms: 2.09x faster                                                   |
| async_tree_none            | 741 ms                                                 | 374 ms: 1.98x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 482 ms: 1.93x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 384 ms: 1.83x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 674 ms: 1.63x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 674 ms: 1.60x faster                                                   |
| async_generators           | 589 ms                                                 | 535 ms: 1.10x faster                                                   |
| coroutines                 | 29.5 ms                                                | 32.8 ms: 1.11x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.61x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 95.2 ms: 1.29x faster                                                  |
| pidigits       | 250 ms                                                 | 237 ms: 1.05x faster                                                   |
| nbody          | 119 ms                                                 | 128 ms: 1.08x slower                                                   |
| Geometric mean | (ref)                                                  | 1.08x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.39 ms: 1.17x faster                                                  |
| regex_compile  | 187 ms                                                 | 169 ms: 1.11x faster                                                   |
| Geometric mean | (ref)                                                  | 1.06x faster                                                           |

Benchmark hidden because not significant (2): regex_v8, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|---------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse     | 241 ms                                                 | 202 ms: 1.19x faster                                                   |
| tomli_loads         | 2.88 sec                                               | 2.46 sec: 1.17x faster                                                 |
| xml_etree_iterparse | 169 ms                                                 | 145 ms: 1.17x faster                                                   |
| xml_etree_process   | 83.7 ms                                                | 80.4 ms: 1.04x faster                                                  |
| json_loads          | 37.9 us                                                | 36.5 us: 1.04x faster                                                  |
| json_dumps          | 14.3 ms                                                | 16.4 ms: 1.14x slower                                                  |
| Geometric mean      | (ref)                                                  | 1.06x faster                                                           |

Benchmark hidden because not significant (3): xml_etree_generate, unpickle_pure_python, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup | 23.7 ms                                                | 29.8 ms: 1.26x slower                                                  |
| Geometric mean | (ref)                                                  | 1.12x slower                                                           |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 44.9 ms                                                | 43.0 ms: 1.04x faster                                                  |
| mako            | 15.7 ms                                                | 16.5 ms: 1.05x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.00x slower                                                           |

Benchmark hidden because not significant (2): genshi_xml, genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_memoization     | 977 ms                                                 | 449 ms: 2.18x faster                                                   |
| async_tree_io_tg           | 1.93 sec                                               | 890 ms: 2.17x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 883 ms: 2.09x faster                                                   |
| mdp                        | 3.97 sec                                               | 1.94 sec: 2.04x faster                                                 |
| async_tree_none            | 741 ms                                                 | 374 ms: 1.98x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 482 ms: 1.93x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 384 ms: 1.83x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 674 ms: 1.63x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 674 ms: 1.60x faster                                                   |
| deepcopy_memo              | 52.4 us                                                | 36.7 us: 1.43x faster                                                  |
| deepcopy                   | 468 us                                                 | 333 us: 1.40x faster                                                   |
| float                      | 123 ms                                                 | 95.2 ms: 1.29x faster                                                  |
| comprehensions             | 27.1 us                                                | 22.2 us: 1.22x faster                                                  |
| chaos                      | 84.9 ms                                                | 69.9 ms: 1.21x faster                                                  |
| raytrace                   | 408 ms                                                 | 336 ms: 1.21x faster                                                   |
| pyflate                    | 727 ms                                                 | 605 ms: 1.20x faster                                                   |
| sqlalchemy_declarative     | 218 ms                                                 | 183 ms: 1.19x faster                                                   |
| xml_etree_parse            | 241 ms                                                 | 202 ms: 1.19x faster                                                   |
| tomli_loads                | 2.88 sec                                               | 2.46 sec: 1.17x faster                                                 |
| xml_etree_iterparse        | 169 ms                                                 | 145 ms: 1.17x faster                                                   |
| regex_effbot               | 5.13 ms                                                | 4.39 ms: 1.17x faster                                                  |
| dulwich_log                | 100 ms                                                 | 86.0 ms: 1.17x faster                                                  |
| spectral_norm              | 156 ms                                                 | 134 ms: 1.16x faster                                                   |
| pylint                     | 465 ms                                                 | 403 ms: 1.15x faster                                                   |
| scimark_fft                | 500 ms                                                 | 438 ms: 1.14x faster                                                   |
| go                         | 172 ms                                                 | 152 ms: 1.14x faster                                                   |
| richards_super             | 72.8 ms                                                | 64.4 ms: 1.13x faster                                                  |
| logging_simple             | 9.45 us                                                | 8.37 us: 1.13x faster                                                  |
| pycparser                  | 1.79 sec                                               | 1.59 sec: 1.12x faster                                                 |
| pathlib                    | 31.6 ms                                                | 28.2 ms: 1.12x faster                                                  |
| sqlite_synth               | 3.87 us                                                | 3.47 us: 1.12x faster                                                  |
| regex_compile              | 187 ms                                                 | 169 ms: 1.11x faster                                                   |
| bpe_tokeniser              | 6.59 sec                                               | 5.97 sec: 1.10x faster                                                 |
| scimark_sor                | 167 ms                                                 | 151 ms: 1.10x faster                                                   |
| async_generators           | 589 ms                                                 | 535 ms: 1.10x faster                                                   |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 6.12 ms: 1.09x faster                                                  |
| deepcopy_reduce            | 4.04 us                                                | 3.69 us: 1.09x faster                                                  |
| logging_silent             | 139 ns                                                 | 127 ns: 1.09x faster                                                   |
| pprint_pformat             | 1.98 sec                                               | 1.82 sec: 1.09x faster                                                 |
| docutils                   | 4.00 sec                                               | 3.68 sec: 1.09x faster                                                 |
| typing_runtime_protocols   | 224 us                                                 | 207 us: 1.08x faster                                                   |
| sympy_sum                  | 222 ms                                                 | 207 ms: 1.07x faster                                                   |
| pprint_safe_repr           | 967 ms                                                 | 905 ms: 1.07x faster                                                   |
| sympy_integrate            | 29.8 ms                                                | 27.9 ms: 1.07x faster                                                  |
| fannkuch                   | 540 ms                                                 | 511 ms: 1.06x faster                                                   |
| crypto_pyaes               | 107 ms                                                 | 102 ms: 1.06x faster                                                   |
| pidigits                   | 250 ms                                                 | 237 ms: 1.05x faster                                                   |
| sympy_str                  | 385 ms                                                 | 367 ms: 1.05x faster                                                   |
| django_template            | 44.9 ms                                                | 43.0 ms: 1.04x faster                                                  |
| xml_etree_process          | 83.7 ms                                                | 80.4 ms: 1.04x faster                                                  |
| json_loads                 | 37.9 us                                                | 36.5 us: 1.04x faster                                                  |
| deltablue                  | 4.27 ms                                                | 4.42 ms: 1.04x slower                                                  |
| generators                 | 41.1 ms                                                | 43.0 ms: 1.04x slower                                                  |
| mako                       | 15.7 ms                                                | 16.5 ms: 1.05x slower                                                  |
| nbody                      | 119 ms                                                 | 128 ms: 1.08x slower                                                   |
| json                       | 6.85 ms                                                | 7.54 ms: 1.10x slower                                                  |
| coroutines                 | 29.5 ms                                                | 32.8 ms: 1.11x slower                                                  |
| coverage                   | 95.4 ms                                                | 107 ms: 1.12x slower                                                   |
| json_dumps                 | 14.3 ms                                                | 16.4 ms: 1.14x slower                                                  |
| python_startup             | 23.7 ms                                                | 29.8 ms: 1.26x slower                                                  |
| gc_traversal               | 5.86 ms                                                | 7.62 ms: 1.30x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 3.64 ms: 1.88x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 96.7 ms: 4.67x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.10x faster                                                           |

Benchmark hidden because not significant (21): xml_etree_generate, scimark_monte_carlo, logging_format, nqueens, genshi_xml, sqlalchemy_imperative, asyncio_websockets, unpickle_pure_python, 2to3, pickle_pure_python, regex_v8, sympy_expand, python_startup_no_site, hexiom, regex_dna, scimark_lu, richards, meteor_contest, bench_thread_pool, telco, genshi_text
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250401-3.14.0a6+-3a8cefb/bm-20250401-linux-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.128x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.16x