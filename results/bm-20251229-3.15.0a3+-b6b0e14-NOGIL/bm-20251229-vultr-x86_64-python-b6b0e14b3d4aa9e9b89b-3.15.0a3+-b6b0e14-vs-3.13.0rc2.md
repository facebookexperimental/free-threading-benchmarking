# Results vs. 3.13.0rc2

- fork: python
- ref: b6b0e14b3d4aa9e9b89b
- machine: linux-x86_64
- commit hash: b6b0e14
- commit date: 2025-12-29
- overall geometric mean: 1.064x slower
- HPT reliability: 95.05%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.39x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251229-vultr-x86_64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 275 ms: 1.06x slower                                                   |
| docutils       | 2.62 sec                                                     | 2.73 sec: 1.04x slower                                                 |
| html5lib       | 67.0 ms                                                      | 65.9 ms: 1.02x faster                                                  |
| Geometric mean | (ref)                                                        | 1.03x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251229-vultr-x86_64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 612 ms: 1.49x faster                                                   |
| async_tree_io              | 876 ms                                                       | 614 ms: 1.43x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 351 ms: 1.31x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 262 ms: 1.28x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 323 ms: 1.28x faster                                                   |
| async_tree_none            | 354 ms                                                       | 286 ms: 1.24x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 523 ms: 1.22x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 550 ms: 1.21x faster                                                   |
| asyncio_websockets         | 520 ms                                                       | 511 ms: 1.02x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 24.2 ms: 1.03x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.21x faster                                                           |

Benchmark hidden because not significant (1): async_generators

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251229-vultr-x86_64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 192 ms: 1.13x faster                                                   |
| float          | 77.5 ms                                                      | 73.2 ms: 1.06x faster                                                  |
| nbody          | 85.1 ms                                                      | 125 ms: 1.47x slower                                                   |
| Geometric mean | (ref)                                                        | 1.07x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251229-vultr-x86_64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.88 ms: 1.07x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 21.4 ms: 1.06x faster                                                  |
| regex_dna      | 180 ms                                                       | 174 ms: 1.03x faster                                                   |
| regex_compile  | 132 ms                                                       | 141 ms: 1.06x slower                                                   |
| Geometric mean | (ref)                                                        | 1.02x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251229-vultr-x86_64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 88.3 ms: 1.08x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 131 ms: 1.04x faster                                                   |
| json_dumps           | 10.5 ms                                                      | 11.2 ms: 1.07x slower                                                  |
| unpickle_pure_python | 210 us                                                       | 236 us: 1.12x slower                                                   |
| pickle_pure_python   | 294 us                                                       | 333 us: 1.13x slower                                                   |
| tomli_loads          | 2.01 sec                                                     | 2.27 sec: 1.13x slower                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 97.0 ms: 1.14x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 69.6 ms: 1.17x slower                                                  |
| json_loads           | 27.0 us                                                      | 32.3 us: 1.20x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.09x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251229-vultr-x86_64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.61 ms: 1.30x slower                                                  |
| python_startup         | 11.0 ms                                                      | 15.7 ms: 1.43x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.36x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251229-vultr-x86_64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 57.7 ms: 1.18x slower                                                  |
| django_template | 34.1 ms                                                      | 40.6 ms: 1.19x slower                                                  |
| genshi_text     | 21.5 ms                                                      | 26.8 ms: 1.25x slower                                                  |
| mako            | 11.3 ms                                                      | 15.3 ms: 1.35x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.24x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251229-vultr-x86_64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.31 sec: 1.79x faster                                                 |
| gc_traversal               | 3.14 ms                                                      | 1.87 ms: 1.68x faster                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 7.11 ms: 1.55x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 612 ms: 1.49x faster                                                   |
| async_tree_io              | 876 ms                                                       | 614 ms: 1.43x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 351 ms: 1.31x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 30.0 us: 1.30x faster                                                  |
| deepcopy                   | 355 us                                                       | 276 us: 1.29x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 262 ms: 1.28x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 323 ms: 1.28x faster                                                   |
| async_tree_none            | 354 ms                                                       | 286 ms: 1.24x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 523 ms: 1.22x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 550 ms: 1.21x faster                                                   |
| go                         | 141 ms                                                       | 120 ms: 1.18x faster                                                   |
| pidigits                   | 217 ms                                                       | 192 ms: 1.13x faster                                                   |
| scimark_sor                | 134 ms                                                       | 122 ms: 1.10x faster                                                   |
| xml_etree_iterparse        | 94.9 ms                                                      | 88.3 ms: 1.08x faster                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.06 us: 1.07x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.88 ms: 1.07x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 18.0 ms: 1.07x faster                                                  |
| regex_v8                   | 22.7 ms                                                      | 21.4 ms: 1.06x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 70.7 ms: 1.06x faster                                                  |
| float                      | 77.5 ms                                                      | 73.2 ms: 1.06x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.94 us: 1.06x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 131 ms: 1.04x faster                                                   |
| regex_dna                  | 180 ms                                                       | 174 ms: 1.03x faster                                                   |
| asyncio_websockets         | 520 ms                                                       | 511 ms: 1.02x faster                                                   |
| html5lib                   | 67.0 ms                                                      | 65.9 ms: 1.02x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.38 sec: 1.02x faster                                                 |
| scimark_fft                | 349 ms                                                       | 345 ms: 1.01x faster                                                   |
| spectral_norm              | 111 ms                                                       | 110 ms: 1.01x faster                                                   |
| pycparser                  | 1.12 sec                                                     | 1.14 sec: 1.02x slower                                                 |
| coroutines                 | 23.6 ms                                                      | 24.2 ms: 1.03x slower                                                  |
| pprint_safe_repr           | 738 ms                                                       | 763 ms: 1.03x slower                                                   |
| pyflate                    | 449 ms                                                       | 468 ms: 1.04x slower                                                   |
| docutils                   | 2.62 sec                                                     | 2.73 sec: 1.04x slower                                                 |
| pprint_pformat             | 1.50 sec                                                     | 1.58 sec: 1.06x slower                                                 |
| 2to3                       | 260 ms                                                       | 275 ms: 1.06x slower                                                   |
| regex_compile              | 132 ms                                                       | 141 ms: 1.06x slower                                                   |
| json_dumps                 | 10.5 ms                                                      | 11.2 ms: 1.07x slower                                                  |
| hexiom                     | 5.99 ms                                                      | 6.40 ms: 1.07x slower                                                  |
| comprehensions             | 16.5 us                                                      | 17.7 us: 1.08x slower                                                  |
| chaos                      | 57.3 ms                                                      | 62.8 ms: 1.10x slower                                                  |
| sympy_integrate            | 19.8 ms                                                      | 21.8 ms: 1.10x slower                                                  |
| generators                 | 28.8 ms                                                      | 32.2 ms: 1.12x slower                                                  |
| json                       | 4.93 ms                                                      | 5.51 ms: 1.12x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.50 ms: 1.12x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 236 us: 1.12x slower                                                   |
| thrift                     | 778 us                                                       | 878 us: 1.13x slower                                                   |
| pickle_pure_python         | 294 us                                                       | 333 us: 1.13x slower                                                   |
| sympy_str                  | 275 ms                                                       | 311 ms: 1.13x slower                                                   |
| tomli_loads                | 2.01 sec                                                     | 2.27 sec: 1.13x slower                                                 |
| logging_simple             | 6.16 us                                                      | 6.98 us: 1.13x slower                                                  |
| richards                   | 45.2 ms                                                      | 51.3 ms: 1.13x slower                                                  |
| sympy_sum                  | 156 ms                                                       | 177 ms: 1.14x slower                                                   |
| xml_etree_generate         | 85.4 ms                                                      | 97.0 ms: 1.14x slower                                                  |
| sympy_expand               | 457 ms                                                       | 519 ms: 1.14x slower                                                   |
| nqueens                    | 78.6 ms                                                      | 89.4 ms: 1.14x slower                                                  |
| richards_super             | 51.6 ms                                                      | 58.9 ms: 1.14x slower                                                  |
| scimark_lu                 | 113 ms                                                       | 130 ms: 1.15x slower                                                   |
| logging_format             | 6.84 us                                                      | 7.90 us: 1.16x slower                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.45 ms: 1.16x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 3.62 ms: 1.16x slower                                                  |
| xml_etree_process          | 59.3 ms                                                      | 69.6 ms: 1.17x slower                                                  |
| raytrace                   | 253 ms                                                       | 298 ms: 1.18x slower                                                   |
| genshi_xml                 | 48.8 ms                                                      | 57.7 ms: 1.18x slower                                                  |
| django_template            | 34.1 ms                                                      | 40.6 ms: 1.19x slower                                                  |
| json_loads                 | 27.0 us                                                      | 32.3 us: 1.20x slower                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 78.8 ms: 1.21x slower                                                  |
| meteor_contest             | 102 ms                                                       | 123 ms: 1.21x slower                                                   |
| fannkuch                   | 370 ms                                                       | 457 ms: 1.24x slower                                                   |
| typing_runtime_protocols   | 155 us                                                       | 192 us: 1.24x slower                                                   |
| genshi_text                | 21.5 ms                                                      | 26.8 ms: 1.25x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 86.7 ms: 1.28x slower                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 9.61 ms: 1.30x slower                                                  |
| mako                       | 11.3 ms                                                      | 15.3 ms: 1.35x slower                                                  |
| coverage                   | 83.0 ms                                                      | 113 ms: 1.36x slower                                                   |
| python_startup             | 11.0 ms                                                      | 15.7 ms: 1.43x slower                                                  |
| nbody                      | 85.1 ms                                                      | 125 ms: 1.47x slower                                                   |
| bench_thread_pool          | 919 us                                                       | 1.47 ms: 1.60x slower                                                  |
| telco                      | 7.82 ms                                                      | 175 ms: 22.37x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.06x slower                                                           |

Benchmark hidden because not significant (3): pylint, async_generators, logging_silent
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251229-3.15.0a3+-b6b0e14-NOGIL/bm-20251229-vultr-x86_64-python-b6b0e14b3d4aa9e9b89b-3.15.0a3+-b6b0e14.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.064x slower

# HPT report

- Reliability score: 95.05% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.39x