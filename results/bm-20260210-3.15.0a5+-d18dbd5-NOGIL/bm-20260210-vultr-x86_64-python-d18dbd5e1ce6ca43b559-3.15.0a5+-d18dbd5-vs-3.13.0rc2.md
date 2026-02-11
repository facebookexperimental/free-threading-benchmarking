# Results vs. 3.13.0rc2

- fork: python
- ref: d18dbd5e1ce6ca43b559
- machine: linux-x86_64
- commit hash: d18dbd5
- commit date: 2026-02-10
- overall geometric mean: 1.066x slower
- HPT reliability: 95.87%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.40x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260210-vultr-x86_64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 277 ms: 1.07x slower                                                   |
| docutils       | 2.62 sec                                                     | 2.72 sec: 1.04x slower                                                 |
| Geometric mean | (ref)                                                        | 1.03x slower                                                           |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260210-vultr-x86_64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 600 ms: 1.52x faster                                                   |
| async_tree_io              | 876 ms                                                       | 614 ms: 1.43x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 353 ms: 1.31x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 327 ms: 1.26x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 266 ms: 1.26x faster                                                   |
| async_tree_none            | 354 ms                                                       | 286 ms: 1.24x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 627 ms: 1.06x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 604 ms: 1.06x faster                                                   |
| asyncio_websockets         | 520 ms                                                       | 510 ms: 1.02x faster                                                   |
| async_generators           | 377 ms                                                       | 370 ms: 1.02x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 23.8 ms: 1.01x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.18x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260210-vultr-x86_64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 72.4 ms: 1.07x faster                                                  |
| pidigits       | 217 ms                                                       | 219 ms: 1.01x slower                                                   |
| nbody          | 85.1 ms                                                      | 121 ms: 1.42x slower                                                   |
| Geometric mean | (ref)                                                        | 1.10x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260210-vultr-x86_64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.68 ms: 1.15x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 20.9 ms: 1.09x faster                                                  |
| regex_dna      | 180 ms                                                       | 172 ms: 1.05x faster                                                   |
| regex_compile  | 132 ms                                                       | 140 ms: 1.06x slower                                                   |
| Geometric mean | (ref)                                                        | 1.05x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260210-vultr-x86_64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 88.4 ms: 1.07x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 132 ms: 1.03x faster                                                   |
| tomli_loads          | 2.01 sec                                                     | 1.97 sec: 1.02x faster                                                 |
| json_dumps           | 10.5 ms                                                      | 11.0 ms: 1.05x slower                                                  |
| unpickle_pure_python | 210 us                                                       | 236 us: 1.12x slower                                                   |
| pickle_pure_python   | 294 us                                                       | 331 us: 1.12x slower                                                   |
| xml_etree_generate   | 85.4 ms                                                      | 96.6 ms: 1.13x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 69.0 ms: 1.16x slower                                                  |
| json_loads           | 27.0 us                                                      | 32.3 us: 1.20x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.07x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260210-vultr-x86_64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.72 ms: 1.32x slower                                                  |
| python_startup         | 11.0 ms                                                      | 15.9 ms: 1.44x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.38x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260210-vultr-x86_64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 54.7 ms: 1.12x slower                                                  |
| django_template | 34.1 ms                                                      | 40.7 ms: 1.19x slower                                                  |
| genshi_text     | 21.5 ms                                                      | 25.9 ms: 1.20x slower                                                  |
| mako            | 11.3 ms                                                      | 15.7 ms: 1.39x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.22x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260210-vultr-x86_64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.31 sec: 1.80x faster                                                 |
| gc_traversal               | 3.14 ms                                                      | 1.96 ms: 1.60x faster                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 7.07 ms: 1.55x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 600 ms: 1.52x faster                                                   |
| async_tree_io              | 876 ms                                                       | 614 ms: 1.43x faster                                                   |
| deepcopy                   | 355 us                                                       | 268 us: 1.33x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 353 ms: 1.31x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 30.5 us: 1.28x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 327 ms: 1.26x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 266 ms: 1.26x faster                                                   |
| async_tree_none            | 354 ms                                                       | 286 ms: 1.24x faster                                                   |
| go                         | 141 ms                                                       | 120 ms: 1.17x faster                                                   |
| sqlite_synth               | 2.21 us                                                      | 1.91 us: 1.15x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.68 ms: 1.15x faster                                                  |
| scimark_sor                | 134 ms                                                       | 120 ms: 1.12x faster                                                   |
| regex_v8                   | 22.7 ms                                                      | 20.9 ms: 1.09x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 17.7 ms: 1.08x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.89 us: 1.08x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 88.4 ms: 1.07x faster                                                  |
| float                      | 77.5 ms                                                      | 72.4 ms: 1.07x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 627 ms: 1.06x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 604 ms: 1.06x faster                                                   |
| dulwich_log                | 74.8 ms                                                      | 71.3 ms: 1.05x faster                                                  |
| regex_dna                  | 180 ms                                                       | 172 ms: 1.05x faster                                                   |
| xml_etree_parse            | 136 ms                                                       | 132 ms: 1.03x faster                                                   |
| asyncio_websockets         | 520 ms                                                       | 510 ms: 1.02x faster                                                   |
| async_generators           | 377 ms                                                       | 370 ms: 1.02x faster                                                   |
| bpe_tokeniser              | 4.45 sec                                                     | 4.37 sec: 1.02x faster                                                 |
| tomli_loads                | 2.01 sec                                                     | 1.97 sec: 1.02x faster                                                 |
| scimark_fft                | 349 ms                                                       | 346 ms: 1.01x faster                                                   |
| spectral_norm              | 111 ms                                                       | 110 ms: 1.00x faster                                                   |
| logging_silent             | 103 ns                                                       | 104 ns: 1.01x slower                                                   |
| coroutines                 | 23.6 ms                                                      | 23.8 ms: 1.01x slower                                                  |
| pidigits                   | 217 ms                                                       | 219 ms: 1.01x slower                                                   |
| pycparser                  | 1.12 sec                                                     | 1.13 sec: 1.01x slower                                                 |
| pyflate                    | 449 ms                                                       | 460 ms: 1.03x slower                                                   |
| docutils                   | 2.62 sec                                                     | 2.72 sec: 1.04x slower                                                 |
| json_dumps                 | 10.5 ms                                                      | 11.0 ms: 1.05x slower                                                  |
| regex_compile              | 132 ms                                                       | 140 ms: 1.06x slower                                                   |
| pprint_safe_repr           | 738 ms                                                       | 785 ms: 1.06x slower                                                   |
| 2to3                       | 260 ms                                                       | 277 ms: 1.07x slower                                                   |
| pprint_pformat             | 1.50 sec                                                     | 1.62 sec: 1.08x slower                                                 |
| generators                 | 28.8 ms                                                      | 31.6 ms: 1.10x slower                                                  |
| chaos                      | 57.3 ms                                                      | 63.4 ms: 1.11x slower                                                  |
| hexiom                     | 5.99 ms                                                      | 6.64 ms: 1.11x slower                                                  |
| sympy_integrate            | 19.8 ms                                                      | 22.0 ms: 1.11x slower                                                  |
| json                       | 4.93 ms                                                      | 5.48 ms: 1.11x slower                                                  |
| scimark_lu                 | 113 ms                                                       | 126 ms: 1.12x slower                                                   |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.26 ms: 1.12x slower                                                  |
| genshi_xml                 | 48.8 ms                                                      | 54.7 ms: 1.12x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 236 us: 1.12x slower                                                   |
| pickle_pure_python         | 294 us                                                       | 331 us: 1.12x slower                                                   |
| comprehensions             | 16.5 us                                                      | 18.6 us: 1.13x slower                                                  |
| nqueens                    | 78.6 ms                                                      | 88.8 ms: 1.13x slower                                                  |
| logging_simple             | 6.16 us                                                      | 6.96 us: 1.13x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 96.6 ms: 1.13x slower                                                  |
| sympy_str                  | 275 ms                                                       | 312 ms: 1.14x slower                                                   |
| sympy_expand               | 457 ms                                                       | 521 ms: 1.14x slower                                                   |
| sympy_sum                  | 156 ms                                                       | 179 ms: 1.15x slower                                                   |
| thrift                     | 778 us                                                       | 895 us: 1.15x slower                                                   |
| deltablue                  | 3.12 ms                                                      | 3.60 ms: 1.15x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.55 ms: 1.16x slower                                                  |
| logging_format             | 6.84 us                                                      | 7.93 us: 1.16x slower                                                  |
| xml_etree_process          | 59.3 ms                                                      | 69.0 ms: 1.16x slower                                                  |
| raytrace                   | 253 ms                                                       | 297 ms: 1.17x slower                                                   |
| scimark_monte_carlo        | 65.4 ms                                                      | 77.6 ms: 1.19x slower                                                  |
| django_template            | 34.1 ms                                                      | 40.7 ms: 1.19x slower                                                  |
| json_loads                 | 27.0 us                                                      | 32.3 us: 1.20x slower                                                  |
| genshi_text                | 21.5 ms                                                      | 25.9 ms: 1.20x slower                                                  |
| richards_super             | 51.6 ms                                                      | 62.3 ms: 1.21x slower                                                  |
| richards                   | 45.2 ms                                                      | 54.7 ms: 1.21x slower                                                  |
| fannkuch                   | 370 ms                                                       | 455 ms: 1.23x slower                                                   |
| meteor_contest             | 102 ms                                                       | 125 ms: 1.23x slower                                                   |
| typing_runtime_protocols   | 155 us                                                       | 194 us: 1.26x slower                                                   |
| crypto_pyaes               | 67.9 ms                                                      | 86.1 ms: 1.27x slower                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 9.72 ms: 1.32x slower                                                  |
| coverage                   | 83.0 ms                                                      | 112 ms: 1.35x slower                                                   |
| mako                       | 11.3 ms                                                      | 15.7 ms: 1.39x slower                                                  |
| nbody                      | 85.1 ms                                                      | 121 ms: 1.42x slower                                                   |
| python_startup             | 11.0 ms                                                      | 15.9 ms: 1.44x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.46 ms: 1.59x slower                                                  |
| telco                      | 7.82 ms                                                      | 173 ms: 22.05x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.07x slower                                                           |

Benchmark hidden because not significant (2): pylint, html5lib
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260210-3.15.0a5+-d18dbd5-NOGIL/bm-20260210-vultr-x86_64-python-d18dbd5e1ce6ca43b559-3.15.0a5+-d18dbd5.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.066x slower

# HPT report

- Reliability score: 95.87% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.40x