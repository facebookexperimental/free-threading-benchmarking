# Results vs. 3.13.0rc2

- fork: python
- ref: f5dd52df16e1b3f3f8cc
- machine: linux-x86_64
- commit hash: f5dd52d
- commit date: 2026-09-11
- overall geometric mean: 1.085x slower
- HPT reliability: 99.67%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260911-vultr-x86_64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 298 ms: 1.15x slower                                                  |
| docutils       | 2.62 sec                                                     | 2.95 sec: 1.13x slower                                                |
| html5lib       | 67.0 ms                                                      | 68.1 ms: 1.02x slower                                                 |
| Geometric mean | (ref)                                                        | 1.10x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260911-vultr-x86_64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 706 ms: 1.29x faster                                                  |
| async_tree_io              | 876 ms                                                       | 728 ms: 1.20x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 587 ms: 1.09x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 614 ms: 1.08x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 507 ms: 1.03x faster                                                  |
| async_tree_none            | 354 ms                                                       | 375 ms: 1.06x slower                                                  |
| coroutines                 | 23.6 ms                                                      | 25.9 ms: 1.10x slower                                                 |
| async_generators           | 377 ms                                                       | 415 ms: 1.10x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.04x faster                                                          |

Benchmark hidden because not significant (3): async_tree_memoization_tg, async_tree_memoization, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260911-vultr-x86_64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 182 ms: 1.19x faster                                                  |
| float          | 77.5 ms                                                      | 85.1 ms: 1.10x slower                                                 |
| nbody          | 85.1 ms                                                      | 125 ms: 1.47x slower                                                  |
| Geometric mean | (ref)                                                        | 1.11x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260911-vultr-x86_64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 22.7 ms                                                      | 20.9 ms: 1.09x faster                                                 |
| regex_effbot   | 3.08 ms                                                      | 3.00 ms: 1.03x faster                                                 |
| regex_dna      | 180 ms                                                       | 187 ms: 1.04x slower                                                  |
| regex_compile  | 132 ms                                                       | 172 ms: 1.30x slower                                                  |
| Geometric mean | (ref)                                                        | 1.05x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260911-vultr-x86_64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 10.5 ms                                                      | 10.2 ms: 1.03x faster                                                 |
| tomli_loads          | 2.01 sec                                                     | 1.97 sec: 1.02x faster                                                |
| xml_etree_iterparse  | 94.9 ms                                                      | 96.6 ms: 1.02x slower                                                 |
| xml_etree_parse      | 136 ms                                                       | 143 ms: 1.05x slower                                                  |
| json_loads           | 27.0 us                                                      | 30.9 us: 1.15x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 339 us: 1.15x slower                                                  |
| unpickle_pure_python | 210 us                                                       | 243 us: 1.16x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 101 ms: 1.18x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 75.8 ms: 1.28x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.10x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260911-vultr-x86_64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.99 ms: 1.35x slower                                                 |
| python_startup         | 11.0 ms                                                      | 16.6 ms: 1.51x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.43x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260911-vultr-x86_64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.1 ms                                                      | 42.9 ms: 1.26x slower                                                 |
| mako            | 11.3 ms                                                      | 16.1 ms: 1.42x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.33x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260911-vultr-x86_64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 317 ms                                                       | 132 ms: 2.41x faster                                                  |
| mdp                        | 2.36 sec                                                     | 1.32 sec: 1.79x faster                                                |
| gc_traversal               | 3.14 ms                                                      | 1.80 ms: 1.75x faster                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 6.76 ms: 1.63x faster                                                 |
| deepcopy                   | 355 us                                                       | 272 us: 1.30x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 706 ms: 1.29x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 31.3 us: 1.25x faster                                                 |
| async_tree_io              | 876 ms                                                       | 728 ms: 1.20x faster                                                  |
| pidigits                   | 217 ms                                                       | 182 ms: 1.19x faster                                                  |
| go                         | 141 ms                                                       | 121 ms: 1.16x faster                                                  |
| sqlite_synth               | 2.21 us                                                      | 1.97 us: 1.12x faster                                                 |
| scimark_sor                | 134 ms                                                       | 123 ms: 1.10x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 587 ms: 1.09x faster                                                  |
| regex_v8                   | 22.7 ms                                                      | 20.9 ms: 1.09x faster                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 614 ms: 1.08x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 18.0 ms: 1.07x faster                                                 |
| dulwich_log                | 74.8 ms                                                      | 70.4 ms: 1.06x faster                                                 |
| typing_runtime_protocols   | 155 us                                                       | 147 us: 1.05x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 3.01 us: 1.03x faster                                                 |
| json_dumps                 | 10.5 ms                                                      | 10.2 ms: 1.03x faster                                                 |
| spectral_norm              | 111 ms                                                       | 108 ms: 1.03x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 3.00 ms: 1.03x faster                                                 |
| asyncio_websockets         | 520 ms                                                       | 507 ms: 1.03x faster                                                  |
| tomli_loads                | 2.01 sec                                                     | 1.97 sec: 1.02x faster                                                |
| bpe_tokeniser              | 4.45 sec                                                     | 4.40 sec: 1.01x faster                                                |
| scimark_fft                | 349 ms                                                       | 351 ms: 1.01x slower                                                  |
| html5lib                   | 67.0 ms                                                      | 68.1 ms: 1.02x slower                                                 |
| xml_etree_iterparse        | 94.9 ms                                                      | 96.6 ms: 1.02x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.38 ms: 1.03x slower                                                 |
| regex_dna                  | 180 ms                                                       | 187 ms: 1.04x slower                                                  |
| pyflate                    | 449 ms                                                       | 468 ms: 1.04x slower                                                  |
| xml_etree_parse            | 136 ms                                                       | 143 ms: 1.05x slower                                                  |
| pycparser                  | 1.12 sec                                                     | 1.17 sec: 1.05x slower                                                |
| logging_silent             | 103 ns                                                       | 108 ns: 1.05x slower                                                  |
| async_tree_none            | 354 ms                                                       | 375 ms: 1.06x slower                                                  |
| chaos                      | 57.3 ms                                                      | 61.8 ms: 1.08x slower                                                 |
| json                       | 4.93 ms                                                      | 5.40 ms: 1.10x slower                                                 |
| coroutines                 | 23.6 ms                                                      | 25.9 ms: 1.10x slower                                                 |
| pprint_safe_repr           | 738 ms                                                       | 810 ms: 1.10x slower                                                  |
| float                      | 77.5 ms                                                      | 85.1 ms: 1.10x slower                                                 |
| async_generators           | 377 ms                                                       | 415 ms: 1.10x slower                                                  |
| hexiom                     | 5.99 ms                                                      | 6.63 ms: 1.11x slower                                                 |
| comprehensions             | 16.5 us                                                      | 18.3 us: 1.11x slower                                                 |
| sympy_integrate            | 19.8 ms                                                      | 22.1 ms: 1.11x slower                                                 |
| docutils                   | 2.62 sec                                                     | 2.95 sec: 1.13x slower                                                |
| pprint_pformat             | 1.50 sec                                                     | 1.69 sec: 1.13x slower                                                |
| logging_simple             | 6.16 us                                                      | 7.01 us: 1.14x slower                                                 |
| json_loads                 | 27.0 us                                                      | 30.9 us: 1.15x slower                                                 |
| 2to3                       | 260 ms                                                       | 298 ms: 1.15x slower                                                  |
| nqueens                    | 78.6 ms                                                      | 90.5 ms: 1.15x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 339 us: 1.15x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 243 us: 1.16x slower                                                  |
| sympy_str                  | 275 ms                                                       | 319 ms: 1.16x slower                                                  |
| sympy_sum                  | 156 ms                                                       | 182 ms: 1.17x slower                                                  |
| sympy_expand               | 457 ms                                                       | 537 ms: 1.17x slower                                                  |
| logging_format             | 6.84 us                                                      | 8.04 us: 1.18x slower                                                 |
| richards                   | 45.2 ms                                                      | 53.3 ms: 1.18x slower                                                 |
| raytrace                   | 253 ms                                                       | 298 ms: 1.18x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 101 ms: 1.18x slower                                                  |
| richards_super             | 51.6 ms                                                      | 61.1 ms: 1.18x slower                                                 |
| scimark_lu                 | 113 ms                                                       | 134 ms: 1.19x slower                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.59 ms: 1.19x slower                                                 |
| generators                 | 28.8 ms                                                      | 34.3 ms: 1.19x slower                                                 |
| thrift                     | 778 us                                                       | 927 us: 1.19x slower                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 79.1 ms: 1.21x slower                                                 |
| deltablue                  | 3.12 ms                                                      | 3.79 ms: 1.21x slower                                                 |
| fannkuch                   | 370 ms                                                       | 462 ms: 1.25x slower                                                  |
| django_template            | 34.1 ms                                                      | 42.9 ms: 1.26x slower                                                 |
| meteor_contest             | 102 ms                                                       | 128 ms: 1.26x slower                                                  |
| xml_etree_process          | 59.3 ms                                                      | 75.8 ms: 1.28x slower                                                 |
| regex_compile              | 132 ms                                                       | 172 ms: 1.30x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 89.4 ms: 1.32x slower                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 9.99 ms: 1.35x slower                                                 |
| mako                       | 11.3 ms                                                      | 16.1 ms: 1.42x slower                                                 |
| coverage                   | 83.0 ms                                                      | 118 ms: 1.42x slower                                                  |
| nbody                      | 85.1 ms                                                      | 125 ms: 1.47x slower                                                  |
| python_startup             | 11.0 ms                                                      | 16.6 ms: 1.51x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 1.48 ms: 1.62x slower                                                 |
| telco                      | 7.82 ms                                                      | 178 ms: 22.77x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.09x slower                                                          |

Benchmark hidden because not significant (3): async_tree_memoization_tg, async_tree_memoization, async_tree_none_tg
Ignored benchmarks (20) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260911-3.16.0a0-f5dd52d-NOGIL/bm-20260911-vultr-x86_64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.085x slower

# HPT report

- Reliability score: 99.67% likely to be slow
- 90% likely to have a slowdown of 1.04x
- 95% likely to have a slowdown of 1.03x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.36x