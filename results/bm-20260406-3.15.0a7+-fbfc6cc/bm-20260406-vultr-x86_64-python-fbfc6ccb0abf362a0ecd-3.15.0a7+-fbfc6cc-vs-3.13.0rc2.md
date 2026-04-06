# Results vs. 3.13.0rc2

- fork: python
- ref: fbfc6ccb0abf362a0ecd
- machine: linux-x86_64
- commit hash: fbfc6cc
- commit date: 2026-04-06
- overall geometric mean: 1.031x faster
- HPT reliability: 99.98%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260406-vultr-x86_64-python-fbfc6ccb0abf362a0ecd-3.15.0a7+-fbfc6cc |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 252 ms: 1.03x faster                                                   |
| docutils       | 2.62 sec                                                     | 2.48 sec: 1.05x faster                                                 |
| html5lib       | 67.0 ms                                                      | 59.6 ms: 1.12x faster                                                  |
| Geometric mean | (ref)                                                        | 1.07x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260406-vultr-x86_64-python-fbfc6ccb0abf362a0ecd-3.15.0a7+-fbfc6cc |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 579 ms: 1.58x faster                                                   |
| async_tree_io              | 876 ms                                                       | 597 ms: 1.47x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 314 ms: 1.47x faster                                                   |
| async_tree_none            | 354 ms                                                       | 252 ms: 1.40x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 483 ms: 1.38x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 247 ms: 1.36x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 306 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 484 ms: 1.32x faster                                                   |
| async_generators           | 377 ms                                                       | 344 ms: 1.10x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 24.0 ms: 1.02x slower                                                  |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.29x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260406-vultr-x86_64-python-fbfc6ccb0abf362a0ecd-3.15.0a7+-fbfc6cc |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 184 ms: 1.17x faster                                                   |
| float          | 77.5 ms                                                      | 71.2 ms: 1.09x faster                                                  |
| nbody          | 85.1 ms                                                      | 95.6 ms: 1.12x slower                                                  |
| Geometric mean | (ref)                                                        | 1.04x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260406-vultr-x86_64-python-fbfc6ccb0abf362a0ecd-3.15.0a7+-fbfc6cc |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.89 ms: 1.07x faster                                                  |
| regex_compile  | 132 ms                                                       | 125 ms: 1.06x faster                                                   |
| regex_dna      | 180 ms                                                       | 178 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                        | 1.03x faster                                                           |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260406-vultr-x86_64-python-fbfc6ccb0abf362a0ecd-3.15.0a7+-fbfc6cc |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 84.7 ms: 1.12x faster                                                  |
| tomli_loads          | 2.01 sec                                                     | 1.84 sec: 1.09x faster                                                 |
| json_dumps           | 10.5 ms                                                      | 9.85 ms: 1.07x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 131 ms: 1.04x faster                                                   |
| xml_etree_generate   | 85.4 ms                                                      | 84.4 ms: 1.01x faster                                                  |
| xml_etree_process    | 59.3 ms                                                      | 60.2 ms: 1.01x slower                                                  |
| json_loads           | 27.0 us                                                      | 27.8 us: 1.03x slower                                                  |
| unpickle_pure_python | 210 us                                                       | 217 us: 1.03x slower                                                   |
| pickle_pure_python   | 294 us                                                       | 316 us: 1.07x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.02x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260406-vultr-x86_64-python-fbfc6ccb0abf362a0ecd-3.15.0a7+-fbfc6cc |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.47 ms: 1.01x slower                                                  |
| python_startup         | 11.0 ms                                                      | 12.7 ms: 1.16x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.08x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260406-vultr-x86_64-python-fbfc6ccb0abf362a0ecd-3.15.0a7+-fbfc6cc |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 20.9 ms: 1.03x faster                                                  |
| genshi_xml      | 48.8 ms                                                      | 49.3 ms: 1.01x slower                                                  |
| django_template | 34.1 ms                                                      | 35.7 ms: 1.04x slower                                                  |
| mako            | 11.3 ms                                                      | 12.1 ms: 1.07x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.02x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260406-vultr-x86_64-python-fbfc6ccb0abf362a0ecd-3.15.0a7+-fbfc6cc |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.16 sec: 2.03x faster                                                 |
| async_tree_io_tg           | 913 ms                                                       | 579 ms: 1.58x faster                                                   |
| deepcopy                   | 355 us                                                       | 241 us: 1.47x faster                                                   |
| async_tree_io              | 876 ms                                                       | 597 ms: 1.47x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 314 ms: 1.47x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 27.7 us: 1.41x faster                                                  |
| async_tree_none            | 354 ms                                                       | 252 ms: 1.40x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 483 ms: 1.38x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 247 ms: 1.36x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 306 ms: 1.35x faster                                                   |
| go                         | 141 ms                                                       | 104 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 484 ms: 1.32x faster                                                   |
| scimark_sor                | 134 ms                                                       | 110 ms: 1.22x faster                                                   |
| deepcopy_reduce            | 3.11 us                                                      | 2.62 us: 1.19x faster                                                  |
| spectral_norm              | 111 ms                                                       | 94.0 ms: 1.18x faster                                                  |
| pidigits                   | 217 ms                                                       | 184 ms: 1.17x faster                                                   |
| html5lib                   | 67.0 ms                                                      | 59.6 ms: 1.12x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 84.7 ms: 1.12x faster                                                  |
| pylint                     | 317 ms                                                       | 283 ms: 1.12x faster                                                   |
| scimark_fft                | 349 ms                                                       | 312 ms: 1.12x faster                                                   |
| dulwich_log                | 74.8 ms                                                      | 67.4 ms: 1.11x faster                                                  |
| async_generators           | 377 ms                                                       | 344 ms: 1.10x faster                                                   |
| tomli_loads                | 2.01 sec                                                     | 1.84 sec: 1.09x faster                                                 |
| float                      | 77.5 ms                                                      | 71.2 ms: 1.09x faster                                                  |
| pyflate                    | 449 ms                                                       | 414 ms: 1.08x faster                                                   |
| pathlib                    | 19.2 ms                                                      | 17.8 ms: 1.08x faster                                                  |
| json_dumps                 | 10.5 ms                                                      | 9.85 ms: 1.07x faster                                                  |
| chaos                      | 57.3 ms                                                      | 53.7 ms: 1.07x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.89 ms: 1.07x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.18 sec: 1.06x faster                                                 |
| richards                   | 45.2 ms                                                      | 42.6 ms: 1.06x faster                                                  |
| regex_compile              | 132 ms                                                       | 125 ms: 1.06x faster                                                   |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.45 ms: 1.06x faster                                                  |
| docutils                   | 2.62 sec                                                     | 2.48 sec: 1.05x faster                                                 |
| richards_super             | 51.6 ms                                                      | 49.1 ms: 1.05x faster                                                  |
| logging_silent             | 103 ns                                                       | 98.0 ns: 1.05x faster                                                  |
| scimark_lu                 | 113 ms                                                       | 108 ms: 1.05x faster                                                   |
| xml_etree_parse            | 136 ms                                                       | 131 ms: 1.04x faster                                                   |
| logging_simple             | 6.16 us                                                      | 5.93 us: 1.04x faster                                                  |
| nqueens                    | 78.6 ms                                                      | 75.9 ms: 1.04x faster                                                  |
| hexiom                     | 5.99 ms                                                      | 5.80 ms: 1.03x faster                                                  |
| 2to3                       | 260 ms                                                       | 252 ms: 1.03x faster                                                   |
| scimark_monte_carlo        | 65.4 ms                                                      | 63.5 ms: 1.03x faster                                                  |
| genshi_text                | 21.5 ms                                                      | 20.9 ms: 1.03x faster                                                  |
| sympy_integrate            | 19.8 ms                                                      | 19.3 ms: 1.03x faster                                                  |
| logging_format             | 6.84 us                                                      | 6.69 us: 1.02x faster                                                  |
| thrift                     | 778 us                                                       | 765 us: 1.02x faster                                                   |
| pprint_safe_repr           | 738 ms                                                       | 726 ms: 1.02x faster                                                   |
| pprint_pformat             | 1.50 sec                                                     | 1.48 sec: 1.01x faster                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 84.4 ms: 1.01x faster                                                  |
| coverage                   | 83.0 ms                                                      | 82.1 ms: 1.01x faster                                                  |
| regex_dna                  | 180 ms                                                       | 178 ms: 1.01x faster                                                   |
| raytrace                   | 253 ms                                                       | 253 ms: 1.00x slower                                                   |
| comprehensions             | 16.5 us                                                      | 16.6 us: 1.01x slower                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 7.47 ms: 1.01x slower                                                  |
| genshi_xml                 | 48.8 ms                                                      | 49.3 ms: 1.01x slower                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.23 us: 1.01x slower                                                  |
| xml_etree_process          | 59.3 ms                                                      | 60.2 ms: 1.01x slower                                                  |
| coroutines                 | 23.6 ms                                                      | 24.0 ms: 1.02x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 69.1 ms: 1.02x slower                                                  |
| sympy_str                  | 275 ms                                                       | 280 ms: 1.02x slower                                                   |
| sympy_sum                  | 156 ms                                                       | 159 ms: 1.02x slower                                                   |
| json_loads                 | 27.0 us                                                      | 27.8 us: 1.03x slower                                                  |
| typing_runtime_protocols   | 155 us                                                       | 159 us: 1.03x slower                                                   |
| unpickle_pure_python       | 210 us                                                       | 217 us: 1.03x slower                                                   |
| json                       | 4.93 ms                                                      | 5.11 ms: 1.04x slower                                                  |
| django_template            | 34.1 ms                                                      | 35.7 ms: 1.04x slower                                                  |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                   |
| sympy_expand               | 457 ms                                                       | 480 ms: 1.05x slower                                                   |
| deltablue                  | 3.12 ms                                                      | 3.29 ms: 1.05x slower                                                  |
| fannkuch                   | 370 ms                                                       | 390 ms: 1.06x slower                                                   |
| mako                       | 11.3 ms                                                      | 12.1 ms: 1.07x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 316 us: 1.07x slower                                                   |
| nbody                      | 85.1 ms                                                      | 95.6 ms: 1.12x slower                                                  |
| python_startup             | 11.0 ms                                                      | 12.7 ms: 1.16x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 4.30 ms: 1.37x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.88 ms: 1.41x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.33 ms: 1.45x slower                                                  |
| telco                      | 7.82 ms                                                      | 159 ms: 20.31x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 278 ms: 25.26x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.01x slower                                                           |

Benchmark hidden because not significant (4): regex_v8, generators, meteor_contest, pycparser
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260406-3.15.0a7+-fbfc6cc/bm-20260406-vultr-x86_64-python-fbfc6ccb0abf362a0ecd-3.15.0a7+-fbfc6cc.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.031x faster

# HPT report

- Reliability score: 99.98% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.16x