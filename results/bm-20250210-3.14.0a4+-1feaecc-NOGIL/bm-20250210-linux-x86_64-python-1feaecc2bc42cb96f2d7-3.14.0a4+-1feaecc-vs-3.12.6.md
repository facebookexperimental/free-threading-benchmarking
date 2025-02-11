# Results vs. 3.12.6

- fork: python
- ref: 1feaecc2bc42cb96f2d7
- machine: linux-x86_64
- commit hash: 1feaecc
- commit date: 2025-02-10
- overall geometric mean: 1.034x slower
- HPT reliability: 99.61%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 542 ms: 1.19x slower                                                   |
| docutils       | 4.00 sec                                               | 4.14 sec: 1.04x slower                                                 |
| html5lib       | 88.9 ms                                                | 109 ms: 1.23x slower                                                   |
| Geometric mean | (ref)                                                  | 1.15x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 790 ms: 2.45x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 842 ms: 2.19x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 460 ms: 2.02x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 363 ms: 1.94x faster                                                   |
| async_tree_none            | 741 ms                                                 | 399 ms: 1.86x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 540 ms: 1.81x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 654 ms: 1.68x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 766 ms: 1.41x faster                                                   |
| async_generators           | 589 ms                                                 | 558 ms: 1.06x faster                                                   |
| coroutines                 | 29.5 ms                                                | 32.1 ms: 1.09x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.59x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 250 ms                                                 | 231 ms: 1.08x faster                                                   |
| float          | 123 ms                                                 | 114 ms: 1.08x faster                                                   |
| nbody          | 119 ms                                                 | 189 ms: 1.59x slower                                                   |
| Geometric mean | (ref)                                                  | 1.11x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.52 ms: 1.14x faster                                                  |
| regex_dna      | 278 ms                                                 | 269 ms: 1.04x faster                                                   |
| Geometric mean | (ref)                                                  | 1.03x faster                                                           |

Benchmark hidden because not significant (2): regex_compile, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 241 ms                                                 | 203 ms: 1.19x faster                                                   |
| xml_etree_iterparse  | 169 ms                                                 | 151 ms: 1.12x faster                                                   |
| tomli_loads          | 2.88 sec                                               | 3.03 sec: 1.05x slower                                                 |
| xml_etree_generate   | 127 ms                                                 | 140 ms: 1.10x slower                                                   |
| json_loads           | 37.9 us                                                | 42.9 us: 1.13x slower                                                  |
| xml_etree_process    | 83.7 ms                                                | 96.3 ms: 1.15x slower                                                  |
| unpickle_pure_python | 300 us                                                 | 361 us: 1.20x slower                                                   |
| json_dumps           | 14.3 ms                                                | 17.7 ms: 1.24x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.06x slower                                                           |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 20.8 ms: 1.18x slower                                                  |
| python_startup         | 23.7 ms                                                | 33.0 ms: 1.39x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.28x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 44.9 ms                                                | 56.4 ms: 1.26x slower                                                  |
| genshi_text     | 30.2 ms                                                | 39.0 ms: 1.29x slower                                                  |
| genshi_xml      | 67.6 ms                                                | 95.7 ms: 1.42x slower                                                  |
| mako            | 15.7 ms                                                | 25.2 ms: 1.60x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.38x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 790 ms: 2.45x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 842 ms: 2.19x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 460 ms: 2.02x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 363 ms: 1.94x faster                                                   |
| async_tree_none            | 741 ms                                                 | 399 ms: 1.86x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 540 ms: 1.81x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 654 ms: 1.68x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 766 ms: 1.41x faster                                                   |
| gc_traversal               | 5.86 ms                                                | 4.44 ms: 1.32x faster                                                  |
| deepcopy                   | 468 us                                                 | 387 us: 1.21x faster                                                   |
| xml_etree_parse            | 241 ms                                                 | 203 ms: 1.19x faster                                                   |
| regex_effbot               | 5.13 ms                                                | 4.52 ms: 1.14x faster                                                  |
| xml_etree_iterparse        | 169 ms                                                 | 151 ms: 1.12x faster                                                   |
| pycparser                  | 1.79 sec                                               | 1.64 sec: 1.09x faster                                                 |
| pidigits                   | 250 ms                                                 | 231 ms: 1.08x faster                                                   |
| float                      | 123 ms                                                 | 114 ms: 1.08x faster                                                   |
| comprehensions             | 27.1 us                                                | 25.5 us: 1.06x faster                                                  |
| async_generators           | 589 ms                                                 | 558 ms: 1.06x faster                                                   |
| regex_dna                  | 278 ms                                                 | 269 ms: 1.04x faster                                                   |
| docutils                   | 4.00 sec                                               | 4.14 sec: 1.04x slower                                                 |
| scimark_sor                | 167 ms                                                 | 174 ms: 1.04x slower                                                   |
| tomli_loads                | 2.88 sec                                               | 3.03 sec: 1.05x slower                                                 |
| mdp                        | 3.97 sec                                               | 4.20 sec: 1.06x slower                                                 |
| sympy_sum                  | 222 ms                                                 | 236 ms: 1.07x slower                                                   |
| logging_simple             | 9.45 us                                                | 10.1 us: 1.07x slower                                                  |
| raytrace                   | 408 ms                                                 | 437 ms: 1.07x slower                                                   |
| json                       | 6.85 ms                                                | 7.34 ms: 1.07x slower                                                  |
| coroutines                 | 29.5 ms                                                | 32.1 ms: 1.09x slower                                                  |
| go                         | 172 ms                                                 | 188 ms: 1.09x slower                                                   |
| scimark_fft                | 500 ms                                                 | 547 ms: 1.09x slower                                                   |
| xml_etree_generate         | 127 ms                                                 | 140 ms: 1.10x slower                                                   |
| crypto_pyaes               | 107 ms                                                 | 120 ms: 1.11x slower                                                   |
| bench_thread_pool          | 3.48 ms                                                | 3.89 ms: 1.12x slower                                                  |
| deepcopy_reduce            | 4.04 us                                                | 4.56 us: 1.13x slower                                                  |
| json_loads                 | 37.9 us                                                | 42.9 us: 1.13x slower                                                  |
| sympy_expand               | 582 ms                                                 | 663 ms: 1.14x slower                                                   |
| nqueens                    | 117 ms                                                 | 133 ms: 1.14x slower                                                   |
| xml_etree_process          | 83.7 ms                                                | 96.3 ms: 1.15x slower                                                  |
| bpe_tokeniser              | 6.59 sec                                               | 7.60 sec: 1.15x slower                                                 |
| pprint_pformat             | 1.98 sec                                               | 2.29 sec: 1.16x slower                                                 |
| fannkuch                   | 540 ms                                                 | 630 ms: 1.17x slower                                                   |
| sympy_integrate            | 29.8 ms                                                | 34.7 ms: 1.17x slower                                                  |
| chaos                      | 84.9 ms                                                | 99.1 ms: 1.17x slower                                                  |
| pprint_safe_repr           | 967 ms                                                 | 1.14 sec: 1.18x slower                                                 |
| sympy_str                  | 385 ms                                                 | 454 ms: 1.18x slower                                                   |
| scimark_lu                 | 152 ms                                                 | 179 ms: 1.18x slower                                                   |
| sqlglot_transpile          | 2.34 ms                                                | 2.76 ms: 1.18x slower                                                  |
| python_startup_no_site     | 17.6 ms                                                | 20.8 ms: 1.18x slower                                                  |
| 2to3                       | 456 ms                                                 | 542 ms: 1.19x slower                                                   |
| richards_super             | 72.8 ms                                                | 86.5 ms: 1.19x slower                                                  |
| hexiom                     | 8.27 ms                                                | 9.84 ms: 1.19x slower                                                  |
| thrift                     | 1.06 ms                                                | 1.27 ms: 1.20x slower                                                  |
| unpickle_pure_python       | 300 us                                                 | 361 us: 1.20x slower                                                   |
| generators                 | 41.1 ms                                                | 49.5 ms: 1.20x slower                                                  |
| richards                   | 60.3 ms                                                | 73.2 ms: 1.21x slower                                                  |
| sqlglot_parse              | 1.79 ms                                                | 2.17 ms: 1.21x slower                                                  |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 8.18 ms: 1.22x slower                                                  |
| meteor_contest             | 146 ms                                                 | 179 ms: 1.22x slower                                                   |
| html5lib                   | 88.9 ms                                                | 109 ms: 1.23x slower                                                   |
| logging_format             | 9.59 us                                                | 11.9 us: 1.24x slower                                                  |
| json_dumps                 | 14.3 ms                                                | 17.7 ms: 1.24x slower                                                  |
| django_template            | 44.9 ms                                                | 56.4 ms: 1.26x slower                                                  |
| scimark_monte_carlo        | 96.4 ms                                                | 124 ms: 1.28x slower                                                   |
| typing_runtime_protocols   | 224 us                                                 | 289 us: 1.29x slower                                                   |
| genshi_text                | 30.2 ms                                                | 39.0 ms: 1.29x slower                                                  |
| sqlalchemy_imperative      | 24.7 ms                                                | 32.5 ms: 1.31x slower                                                  |
| telco                      | 9.59 ms                                                | 12.9 ms: 1.35x slower                                                  |
| python_startup             | 23.7 ms                                                | 33.0 ms: 1.39x slower                                                  |
| genshi_xml                 | 67.6 ms                                                | 95.7 ms: 1.42x slower                                                  |
| coverage                   | 95.4 ms                                                | 140 ms: 1.47x slower                                                   |
| deltablue                  | 4.27 ms                                                | 6.45 ms: 1.51x slower                                                  |
| nbody                      | 119 ms                                                 | 189 ms: 1.59x slower                                                   |
| mako                       | 15.7 ms                                                | 25.2 ms: 1.60x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 3.11 ms: 1.60x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 87.5 ms: 4.23x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.06x slower                                                           |

Benchmark hidden because not significant (15): pathlib, asyncio_websockets, deepcopy_memo, pyflate, pylint, sqlalchemy_declarative, sqlglot_normalize, regex_compile, spectral_norm, logging_silent, pickle_pure_python, regex_v8, sqlglot_optimize, sqlite_synth, dulwich_log
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250210-3.14.0a4+-1feaecc-NOGIL/bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4+-1feaecc.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.034x slower

# HPT report

- Reliability score: 99.61% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.35x