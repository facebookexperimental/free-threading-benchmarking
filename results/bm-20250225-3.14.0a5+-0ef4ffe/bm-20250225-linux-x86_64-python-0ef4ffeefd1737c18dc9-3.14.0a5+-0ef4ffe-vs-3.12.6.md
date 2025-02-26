# Results vs. 3.12.6

- fork: python
- ref: 0ef4ffeefd1737c18dc9
- machine: linux-x86_64
- commit hash: 0ef4ffe
- commit date: 2025-02-25
- overall geometric mean: 1.105x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| docutils       | 4.00 sec                                               | 3.74 sec: 1.07x faster                                                 |
| html5lib       | 88.9 ms                                                | 83.7 ms: 1.06x faster                                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                                           |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.85 sec                                               | 885 ms: 2.09x faster                                                   |
| async_tree_io_tg           | 1.93 sec                                               | 967 ms: 2.00x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 502 ms: 1.95x faster                                                   |
| async_tree_none            | 741 ms                                                 | 383 ms: 1.94x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 485 ms: 1.92x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 368 ms: 1.91x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 667 ms: 1.65x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 675 ms: 1.60x faster                                                   |
| async_generators           | 589 ms                                                 | 507 ms: 1.16x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.60x faster                                                           |

Benchmark hidden because not significant (2): coroutines, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 103 ms: 1.19x faster                                                   |
| nbody          | 119 ms                                                 | 125 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                  | 1.05x faster                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 187 ms                                                 | 164 ms: 1.14x faster                                                   |
| regex_dna      | 278 ms                                                 | 291 ms: 1.04x slower                                                   |
| regex_v8       | 32.5 ms                                                | 37.0 ms: 1.14x slower                                                  |
| Geometric mean | (ref)                                                  | 1.00x slower                                                           |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe |
|---------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse     | 241 ms                                                 | 192 ms: 1.26x faster                                                   |
| tomli_loads         | 2.88 sec                                               | 2.51 sec: 1.15x faster                                                 |
| xml_etree_iterparse | 169 ms                                                 | 150 ms: 1.13x faster                                                   |
| xml_etree_generate  | 127 ms                                                 | 118 ms: 1.08x faster                                                   |
| json_dumps          | 14.3 ms                                                | 15.2 ms: 1.06x slower                                                  |
| json_loads          | 37.9 us                                                | 40.3 us: 1.06x slower                                                  |
| pickle_pure_python  | 436 us                                                 | 475 us: 1.09x slower                                                   |
| Geometric mean      | (ref)                                                  | 1.04x faster                                                           |

Benchmark hidden because not significant (2): unpickle_pure_python, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 16.1 ms: 1.09x faster                                                  |
| python_startup         | 23.7 ms                                                | 27.8 ms: 1.17x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.04x slower                                                           |

Benchmarks with tag 'template':
===============================

Benchmark hidden because not significant (4): django_template, mako, genshi_xml, genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.85 sec                                               | 885 ms: 2.09x faster                                                   |
| async_tree_io_tg           | 1.93 sec                                               | 967 ms: 2.00x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 502 ms: 1.95x faster                                                   |
| async_tree_none            | 741 ms                                                 | 383 ms: 1.94x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 485 ms: 1.92x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 368 ms: 1.91x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 667 ms: 1.65x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 675 ms: 1.60x faster                                                   |
| deepcopy                   | 468 us                                                 | 341 us: 1.37x faster                                                   |
| spectral_norm              | 156 ms                                                 | 123 ms: 1.27x faster                                                   |
| sqlalchemy_declarative     | 218 ms                                                 | 172 ms: 1.26x faster                                                   |
| xml_etree_parse            | 241 ms                                                 | 192 ms: 1.26x faster                                                   |
| logging_simple             | 9.45 us                                                | 7.65 us: 1.24x faster                                                  |
| pyflate                    | 727 ms                                                 | 599 ms: 1.21x faster                                                   |
| deepcopy_memo              | 52.4 us                                                | 43.2 us: 1.21x faster                                                  |
| comprehensions             | 27.1 us                                                | 22.8 us: 1.19x faster                                                  |
| float                      | 123 ms                                                 | 103 ms: 1.19x faster                                                   |
| raytrace                   | 408 ms                                                 | 346 ms: 1.18x faster                                                   |
| sqlglot_transpile          | 2.34 ms                                                | 2.00 ms: 1.17x faster                                                  |
| async_generators           | 589 ms                                                 | 507 ms: 1.16x faster                                                   |
| scimark_fft                | 500 ms                                                 | 431 ms: 1.16x faster                                                   |
| tomli_loads                | 2.88 sec                                               | 2.51 sec: 1.15x faster                                                 |
| pycparser                  | 1.79 sec                                               | 1.56 sec: 1.15x faster                                                 |
| scimark_monte_carlo        | 96.4 ms                                                | 84.1 ms: 1.15x faster                                                  |
| chaos                      | 84.9 ms                                                | 74.1 ms: 1.14x faster                                                  |
| crypto_pyaes               | 107 ms                                                 | 94.4 ms: 1.14x faster                                                  |
| regex_compile              | 187 ms                                                 | 164 ms: 1.14x faster                                                   |
| pylint                     | 465 ms                                                 | 410 ms: 1.13x faster                                                   |
| richards_super             | 72.8 ms                                                | 64.4 ms: 1.13x faster                                                  |
| xml_etree_iterparse        | 169 ms                                                 | 150 ms: 1.13x faster                                                   |
| sympy_sum                  | 222 ms                                                 | 197 ms: 1.12x faster                                                   |
| bpe_tokeniser              | 6.59 sec                                               | 5.86 sec: 1.12x faster                                                 |
| typing_runtime_protocols   | 224 us                                                 | 201 us: 1.12x faster                                                   |
| logging_format             | 9.59 us                                                | 8.69 us: 1.10x faster                                                  |
| go                         | 172 ms                                                 | 156 ms: 1.10x faster                                                   |
| bench_thread_pool          | 3.48 ms                                                | 3.17 ms: 1.10x faster                                                  |
| nqueens                    | 117 ms                                                 | 106 ms: 1.10x faster                                                   |
| mdp                        | 3.97 sec                                               | 3.62 sec: 1.10x faster                                                 |
| python_startup_no_site     | 17.6 ms                                                | 16.1 ms: 1.09x faster                                                  |
| sympy_integrate            | 29.8 ms                                                | 27.3 ms: 1.09x faster                                                  |
| xml_etree_generate         | 127 ms                                                 | 118 ms: 1.08x faster                                                   |
| sympy_str                  | 385 ms                                                 | 359 ms: 1.07x faster                                                   |
| docutils                   | 4.00 sec                                               | 3.74 sec: 1.07x faster                                                 |
| html5lib                   | 88.9 ms                                                | 83.7 ms: 1.06x faster                                                  |
| pprint_pformat             | 1.98 sec                                               | 1.87 sec: 1.06x faster                                                 |
| thrift                     | 1.06 ms                                                | 1.00 ms: 1.06x faster                                                  |
| deltablue                  | 4.27 ms                                                | 4.10 ms: 1.04x faster                                                  |
| pprint_safe_repr           | 967 ms                                                 | 931 ms: 1.04x faster                                                   |
| json                       | 6.85 ms                                                | 7.15 ms: 1.04x slower                                                  |
| regex_dna                  | 278 ms                                                 | 291 ms: 1.04x slower                                                   |
| nbody                      | 119 ms                                                 | 125 ms: 1.05x slower                                                   |
| json_dumps                 | 14.3 ms                                                | 15.2 ms: 1.06x slower                                                  |
| json_loads                 | 37.9 us                                                | 40.3 us: 1.06x slower                                                  |
| telco                      | 9.59 ms                                                | 10.2 ms: 1.07x slower                                                  |
| pickle_pure_python         | 436 us                                                 | 475 us: 1.09x slower                                                   |
| regex_v8                   | 32.5 ms                                                | 37.0 ms: 1.14x slower                                                  |
| python_startup             | 23.7 ms                                                | 27.8 ms: 1.17x slower                                                  |
| coverage                   | 95.4 ms                                                | 116 ms: 1.22x slower                                                   |
| gc_traversal               | 5.86 ms                                                | 7.80 ms: 1.33x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 4.16 ms: 2.14x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 96.3 ms: 4.65x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.08x faster                                                           |

Benchmark hidden because not significant (29): sqlglot_normalize, pathlib, sqlglot_parse, scimark_sor, regex_effbot, sqlalchemy_imperative, logging_silent, pidigits, fannkuch, generators, deepcopy_reduce, sqlglot_optimize, unpickle_pure_python, django_template, hexiom, xml_etree_process, scimark_lu, coroutines, sqlite_synth, mako, scimark_sparse_mat_mult, sympy_expand, genshi_xml, meteor_contest, 2to3, genshi_text, asyncio_websockets, richards, dulwich_log
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250225-3.14.0a5+-0ef4ffe/bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.105x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.14x