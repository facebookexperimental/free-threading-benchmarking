# Results vs. 3.13.0rc2

- fork: python
- ref: efde4333bfcdd1e24c2a
- machine: linux-x86_64
- commit hash: efde433
- commit date: 2026-04-08
- overall geometric mean: 1.032x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 255 ms: 1.02x faster                                                   |
| docutils       | 2.62 sec                                                     | 2.50 sec: 1.05x faster                                                 |
| html5lib       | 67.0 ms                                                      | 60.1 ms: 1.12x faster                                                  |
| Geometric mean | (ref)                                                        | 1.06x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 597 ms: 1.53x faster                                                   |
| async_tree_io              | 876 ms                                                       | 585 ms: 1.50x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 315 ms: 1.46x faster                                                   |
| async_tree_none            | 354 ms                                                       | 246 ms: 1.44x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 490 ms: 1.36x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 307 ms: 1.35x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 253 ms: 1.33x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 488 ms: 1.31x faster                                                   |
| async_generators           | 377 ms                                                       | 342 ms: 1.10x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 23.3 ms: 1.01x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.29x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 187 ms: 1.16x faster                                                   |
| float          | 77.5 ms                                                      | 71.0 ms: 1.09x faster                                                  |
| nbody          | 85.1 ms                                                      | 92.8 ms: 1.09x slower                                                  |
| Geometric mean | (ref)                                                        | 1.05x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.87 ms: 1.07x faster                                                  |
| regex_compile  | 132 ms                                                       | 124 ms: 1.07x faster                                                   |
| regex_dna      | 180 ms                                                       | 172 ms: 1.05x faster                                                   |
| regex_v8       | 22.7 ms                                                      | 21.7 ms: 1.05x faster                                                  |
| Geometric mean | (ref)                                                        | 1.06x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 84.4 ms: 1.12x faster                                                  |
| tomli_loads          | 2.01 sec                                                     | 1.82 sec: 1.10x faster                                                 |
| json_dumps           | 10.5 ms                                                      | 9.80 ms: 1.07x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 132 ms: 1.03x faster                                                   |
| xml_etree_generate   | 85.4 ms                                                      | 85.2 ms: 1.00x faster                                                  |
| json_loads           | 27.0 us                                                      | 27.3 us: 1.01x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 60.2 ms: 1.01x slower                                                  |
| unpickle_pure_python | 210 us                                                       | 216 us: 1.03x slower                                                   |
| pickle_pure_python   | 294 us                                                       | 317 us: 1.08x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.02x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.49 ms: 1.01x slower                                                  |
| python_startup         | 11.0 ms                                                      | 12.7 ms: 1.16x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.08x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 21.7 ms: 1.01x slower                                                  |
| genshi_xml      | 48.8 ms                                                      | 50.8 ms: 1.04x slower                                                  |
| django_template | 34.1 ms                                                      | 35.7 ms: 1.04x slower                                                  |
| mako            | 11.3 ms                                                      | 12.2 ms: 1.08x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.04x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.15 sec: 2.05x faster                                                 |
| async_tree_io_tg           | 913 ms                                                       | 597 ms: 1.53x faster                                                   |
| async_tree_io              | 876 ms                                                       | 585 ms: 1.50x faster                                                   |
| deepcopy                   | 355 us                                                       | 239 us: 1.48x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 315 ms: 1.46x faster                                                   |
| async_tree_none            | 354 ms                                                       | 246 ms: 1.44x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 27.8 us: 1.40x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 490 ms: 1.36x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 307 ms: 1.35x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 253 ms: 1.33x faster                                                   |
| go                         | 141 ms                                                       | 106 ms: 1.32x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 488 ms: 1.31x faster                                                   |
| spectral_norm              | 111 ms                                                       | 90.9 ms: 1.22x faster                                                  |
| scimark_sor                | 134 ms                                                       | 111 ms: 1.21x faster                                                   |
| deepcopy_reduce            | 3.11 us                                                      | 2.62 us: 1.19x faster                                                  |
| pidigits                   | 217 ms                                                       | 187 ms: 1.16x faster                                                   |
| xml_etree_iterparse        | 94.9 ms                                                      | 84.4 ms: 1.12x faster                                                  |
| pylint                     | 317 ms                                                       | 283 ms: 1.12x faster                                                   |
| scimark_fft                | 349 ms                                                       | 313 ms: 1.12x faster                                                   |
| html5lib                   | 67.0 ms                                                      | 60.1 ms: 1.12x faster                                                  |
| async_generators           | 377 ms                                                       | 342 ms: 1.10x faster                                                   |
| pathlib                    | 19.2 ms                                                      | 17.4 ms: 1.10x faster                                                  |
| tomli_loads                | 2.01 sec                                                     | 1.82 sec: 1.10x faster                                                 |
| pyflate                    | 449 ms                                                       | 411 ms: 1.09x faster                                                   |
| float                      | 77.5 ms                                                      | 71.0 ms: 1.09x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 68.7 ms: 1.09x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.12 sec: 1.08x faster                                                 |
| json_dumps                 | 10.5 ms                                                      | 9.80 ms: 1.07x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.87 ms: 1.07x faster                                                  |
| regex_compile              | 132 ms                                                       | 124 ms: 1.07x faster                                                   |
| regex_dna                  | 180 ms                                                       | 172 ms: 1.05x faster                                                   |
| docutils                   | 2.62 sec                                                     | 2.50 sec: 1.05x faster                                                 |
| nqueens                    | 78.6 ms                                                      | 75.0 ms: 1.05x faster                                                  |
| regex_v8                   | 22.7 ms                                                      | 21.7 ms: 1.05x faster                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 62.5 ms: 1.05x faster                                                  |
| richards                   | 45.2 ms                                                      | 43.2 ms: 1.05x faster                                                  |
| scimark_lu                 | 113 ms                                                       | 108 ms: 1.05x faster                                                   |
| chaos                      | 57.3 ms                                                      | 54.9 ms: 1.04x faster                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.52 ms: 1.04x faster                                                  |
| richards_super             | 51.6 ms                                                      | 49.8 ms: 1.04x faster                                                  |
| logging_format             | 6.84 us                                                      | 6.60 us: 1.04x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 132 ms: 1.03x faster                                                   |
| logging_simple             | 6.16 us                                                      | 5.97 us: 1.03x faster                                                  |
| pycparser                  | 1.12 sec                                                     | 1.08 sec: 1.03x faster                                                 |
| sympy_integrate            | 19.8 ms                                                      | 19.2 ms: 1.03x faster                                                  |
| logging_silent             | 103 ns                                                       | 100 ns: 1.02x faster                                                   |
| sqlite_synth               | 2.21 us                                                      | 2.17 us: 1.02x faster                                                  |
| hexiom                     | 5.99 ms                                                      | 5.89 ms: 1.02x faster                                                  |
| 2to3                       | 260 ms                                                       | 255 ms: 1.02x faster                                                   |
| generators                 | 28.8 ms                                                      | 28.4 ms: 1.01x faster                                                  |
| thrift                     | 778 us                                                       | 769 us: 1.01x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 23.3 ms: 1.01x faster                                                  |
| pprint_safe_repr           | 738 ms                                                       | 730 ms: 1.01x faster                                                   |
| coverage                   | 83.0 ms                                                      | 82.3 ms: 1.01x faster                                                  |
| comprehensions             | 16.5 us                                                      | 16.3 us: 1.01x faster                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.49 sec: 1.00x faster                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 85.2 ms: 1.00x faster                                                  |
| genshi_text                | 21.5 ms                                                      | 21.7 ms: 1.01x slower                                                  |
| raytrace                   | 253 ms                                                       | 255 ms: 1.01x slower                                                   |
| json_loads                 | 27.0 us                                                      | 27.3 us: 1.01x slower                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 7.49 ms: 1.01x slower                                                  |
| xml_etree_process          | 59.3 ms                                                      | 60.2 ms: 1.01x slower                                                  |
| sympy_str                  | 275 ms                                                       | 279 ms: 1.02x slower                                                   |
| sympy_sum                  | 156 ms                                                       | 159 ms: 1.02x slower                                                   |
| json                       | 4.93 ms                                                      | 5.03 ms: 1.02x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 69.3 ms: 1.02x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 216 us: 1.03x slower                                                   |
| typing_runtime_protocols   | 155 us                                                       | 159 us: 1.03x slower                                                   |
| fannkuch                   | 370 ms                                                       | 383 ms: 1.04x slower                                                   |
| genshi_xml                 | 48.8 ms                                                      | 50.8 ms: 1.04x slower                                                  |
| django_template            | 34.1 ms                                                      | 35.7 ms: 1.04x slower                                                  |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                   |
| sympy_expand               | 457 ms                                                       | 480 ms: 1.05x slower                                                   |
| mako                       | 11.3 ms                                                      | 12.2 ms: 1.08x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 317 us: 1.08x slower                                                   |
| deltablue                  | 3.12 ms                                                      | 3.37 ms: 1.08x slower                                                  |
| nbody                      | 85.1 ms                                                      | 92.8 ms: 1.09x slower                                                  |
| python_startup             | 11.0 ms                                                      | 12.7 ms: 1.16x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 4.28 ms: 1.36x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.92 ms: 1.44x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.33 ms: 1.45x slower                                                  |
| telco                      | 7.82 ms                                                      | 159 ms: 20.32x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 235 ms: 21.36x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.01x slower                                                           |

Benchmark hidden because not significant (1): meteor_contest
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260408-3.15.0a8+-efde433/bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.032x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.17x