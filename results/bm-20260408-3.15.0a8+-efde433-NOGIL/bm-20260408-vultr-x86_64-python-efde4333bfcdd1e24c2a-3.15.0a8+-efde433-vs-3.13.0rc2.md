# Results vs. 3.13.0rc2

- fork: python
- ref: efde4333bfcdd1e24c2a
- machine: linux-x86_64
- commit hash: efde433
- commit date: 2026-04-08
- overall geometric mean: 1.057x slower
- HPT reliability: 86.50%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.41x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 284 ms: 1.09x slower                                                   |
| docutils       | 2.62 sec                                                     | 2.63 sec: 1.00x slower                                                 |
| html5lib       | 67.0 ms                                                      | 65.7 ms: 1.02x faster                                                  |
| Geometric mean | (ref)                                                        | 1.03x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 612 ms: 1.49x faster                                                   |
| async_tree_io              | 876 ms                                                       | 638 ms: 1.37x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 357 ms: 1.29x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 262 ms: 1.28x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 325 ms: 1.27x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 511 ms: 1.25x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 538 ms: 1.24x faster                                                   |
| async_tree_none            | 354 ms                                                       | 292 ms: 1.21x faster                                                   |
| asyncio_websockets         | 520 ms                                                       | 508 ms: 1.02x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 23.3 ms: 1.01x faster                                                  |
| async_generators           | 377 ms                                                       | 380 ms: 1.01x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.21x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 192 ms: 1.13x faster                                                   |
| float          | 77.5 ms                                                      | 73.6 ms: 1.05x faster                                                  |
| nbody          | 85.1 ms                                                      | 123 ms: 1.44x slower                                                   |
| Geometric mean | (ref)                                                        | 1.07x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.74 ms: 1.13x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 21.0 ms: 1.08x faster                                                  |
| regex_dna      | 180 ms                                                       | 175 ms: 1.03x faster                                                   |
| regex_compile  | 132 ms                                                       | 141 ms: 1.06x slower                                                   |
| Geometric mean | (ref)                                                        | 1.04x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 87.3 ms: 1.09x faster                                                  |
| tomli_loads          | 2.01 sec                                                     | 1.92 sec: 1.04x faster                                                 |
| xml_etree_parse      | 136 ms                                                       | 131 ms: 1.04x faster                                                   |
| json_dumps           | 10.5 ms                                                      | 11.3 ms: 1.07x slower                                                  |
| json_loads           | 27.0 us                                                      | 29.3 us: 1.08x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 95.5 ms: 1.12x slower                                                  |
| unpickle_pure_python | 210 us                                                       | 237 us: 1.13x slower                                                   |
| pickle_pure_python   | 294 us                                                       | 338 us: 1.15x slower                                                   |
| xml_etree_process    | 59.3 ms                                                      | 68.4 ms: 1.15x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.06x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.93 ms: 1.34x slower                                                  |
| python_startup         | 11.0 ms                                                      | 16.2 ms: 1.47x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.41x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 54.0 ms: 1.11x slower                                                  |
| django_template | 34.1 ms                                                      | 39.2 ms: 1.15x slower                                                  |
| genshi_text     | 21.5 ms                                                      | 25.3 ms: 1.17x slower                                                  |
| mako            | 11.3 ms                                                      | 15.6 ms: 1.37x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.20x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.31 sec: 1.80x faster                                                 |
| gc_traversal               | 3.14 ms                                                      | 1.97 ms: 1.59x faster                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 7.05 ms: 1.56x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 612 ms: 1.49x faster                                                   |
| async_tree_io              | 876 ms                                                       | 638 ms: 1.37x faster                                                   |
| deepcopy                   | 355 us                                                       | 268 us: 1.33x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 357 ms: 1.29x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 262 ms: 1.28x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 325 ms: 1.27x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 31.2 us: 1.25x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 511 ms: 1.25x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 538 ms: 1.24x faster                                                   |
| async_tree_none            | 354 ms                                                       | 292 ms: 1.21x faster                                                   |
| go                         | 141 ms                                                       | 121 ms: 1.16x faster                                                   |
| sqlite_synth               | 2.21 us                                                      | 1.94 us: 1.14x faster                                                  |
| pidigits                   | 217 ms                                                       | 192 ms: 1.13x faster                                                   |
| regex_effbot               | 3.08 ms                                                      | 2.74 ms: 1.13x faster                                                  |
| scimark_sor                | 134 ms                                                       | 122 ms: 1.10x faster                                                   |
| xml_etree_iterparse        | 94.9 ms                                                      | 87.3 ms: 1.09x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 17.7 ms: 1.09x faster                                                  |
| regex_v8                   | 22.7 ms                                                      | 21.0 ms: 1.08x faster                                                  |
| pylint                     | 317 ms                                                       | 297 ms: 1.07x faster                                                   |
| dulwich_log                | 74.8 ms                                                      | 70.2 ms: 1.07x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.95 us: 1.06x faster                                                  |
| float                      | 77.5 ms                                                      | 73.6 ms: 1.05x faster                                                  |
| tomli_loads                | 2.01 sec                                                     | 1.92 sec: 1.04x faster                                                 |
| xml_etree_parse            | 136 ms                                                       | 131 ms: 1.04x faster                                                   |
| spectral_norm              | 111 ms                                                       | 107 ms: 1.04x faster                                                   |
| regex_dna                  | 180 ms                                                       | 175 ms: 1.03x faster                                                   |
| asyncio_websockets         | 520 ms                                                       | 508 ms: 1.02x faster                                                   |
| html5lib                   | 67.0 ms                                                      | 65.7 ms: 1.02x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.37 sec: 1.02x faster                                                 |
| coroutines                 | 23.6 ms                                                      | 23.3 ms: 1.01x faster                                                  |
| docutils                   | 2.62 sec                                                     | 2.63 sec: 1.00x slower                                                 |
| async_generators           | 377 ms                                                       | 380 ms: 1.01x slower                                                   |
| scimark_fft                | 349 ms                                                       | 353 ms: 1.01x slower                                                   |
| json                       | 4.93 ms                                                      | 5.06 ms: 1.03x slower                                                  |
| pyflate                    | 449 ms                                                       | 463 ms: 1.03x slower                                                   |
| regex_compile              | 132 ms                                                       | 141 ms: 1.06x slower                                                   |
| json_dumps                 | 10.5 ms                                                      | 11.3 ms: 1.07x slower                                                  |
| json_loads                 | 27.0 us                                                      | 29.3 us: 1.08x slower                                                  |
| pprint_safe_repr           | 738 ms                                                       | 800 ms: 1.09x slower                                                   |
| comprehensions             | 16.5 us                                                      | 17.9 us: 1.09x slower                                                  |
| chaos                      | 57.3 ms                                                      | 62.3 ms: 1.09x slower                                                  |
| 2to3                       | 260 ms                                                       | 284 ms: 1.09x slower                                                   |
| logging_simple             | 6.16 us                                                      | 6.74 us: 1.09x slower                                                  |
| sympy_integrate            | 19.8 ms                                                      | 21.7 ms: 1.09x slower                                                  |
| hexiom                     | 5.99 ms                                                      | 6.61 ms: 1.10x slower                                                  |
| genshi_xml                 | 48.8 ms                                                      | 54.0 ms: 1.11x slower                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.66 sec: 1.11x slower                                                 |
| deltablue                  | 3.12 ms                                                      | 3.47 ms: 1.11x slower                                                  |
| nqueens                    | 78.6 ms                                                      | 87.5 ms: 1.11x slower                                                  |
| scimark_lu                 | 113 ms                                                       | 126 ms: 1.11x slower                                                   |
| xml_etree_generate         | 85.4 ms                                                      | 95.5 ms: 1.12x slower                                                  |
| logging_format             | 6.84 us                                                      | 7.69 us: 1.12x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 237 us: 1.13x slower                                                   |
| sympy_str                  | 275 ms                                                       | 311 ms: 1.13x slower                                                   |
| richards_super             | 51.6 ms                                                      | 58.5 ms: 1.13x slower                                                  |
| richards                   | 45.2 ms                                                      | 51.4 ms: 1.14x slower                                                  |
| sympy_sum                  | 156 ms                                                       | 177 ms: 1.14x slower                                                   |
| thrift                     | 778 us                                                       | 890 us: 1.14x slower                                                   |
| generators                 | 28.8 ms                                                      | 33.0 ms: 1.14x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.53 ms: 1.15x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 338 us: 1.15x slower                                                   |
| django_template            | 34.1 ms                                                      | 39.2 ms: 1.15x slower                                                  |
| xml_etree_process          | 59.3 ms                                                      | 68.4 ms: 1.15x slower                                                  |
| sympy_expand               | 457 ms                                                       | 527 ms: 1.15x slower                                                   |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.44 ms: 1.15x slower                                                  |
| genshi_text                | 21.5 ms                                                      | 25.3 ms: 1.17x slower                                                  |
| raytrace                   | 253 ms                                                       | 302 ms: 1.19x slower                                                   |
| scimark_monte_carlo        | 65.4 ms                                                      | 78.8 ms: 1.21x slower                                                  |
| fannkuch                   | 370 ms                                                       | 457 ms: 1.24x slower                                                   |
| meteor_contest             | 102 ms                                                       | 126 ms: 1.24x slower                                                   |
| typing_runtime_protocols   | 155 us                                                       | 193 us: 1.25x slower                                                   |
| crypto_pyaes               | 67.9 ms                                                      | 88.3 ms: 1.30x slower                                                  |
| coverage                   | 83.0 ms                                                      | 111 ms: 1.34x slower                                                   |
| python_startup_no_site     | 7.39 ms                                                      | 9.93 ms: 1.34x slower                                                  |
| mako                       | 11.3 ms                                                      | 15.6 ms: 1.37x slower                                                  |
| nbody                      | 85.1 ms                                                      | 123 ms: 1.44x slower                                                   |
| python_startup             | 11.0 ms                                                      | 16.2 ms: 1.47x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.46 ms: 1.58x slower                                                  |
| telco                      | 7.82 ms                                                      | 171 ms: 21.83x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.06x slower                                                           |

Benchmark hidden because not significant (2): pycparser, logging_silent
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260408-3.15.0a8+-efde433-NOGIL/bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.057x slower

# HPT report

- Reliability score: 86.50% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.41x