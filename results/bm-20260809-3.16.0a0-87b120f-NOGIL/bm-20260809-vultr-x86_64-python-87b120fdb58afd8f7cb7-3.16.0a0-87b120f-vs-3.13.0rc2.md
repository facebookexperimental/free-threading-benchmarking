# Results vs. 3.13.0rc2

- fork: python
- ref: 87b120fdb58afd8f7cb7
- machine: linux-x86_64
- commit hash: 87b120f
- commit date: 2026-08-09
- overall geometric mean: 1.069x slower
- HPT reliability: 97.91%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260809-vultr-x86_64-python-87b120fdb58afd8f7cb7-3.16.0a0-87b120f |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 298 ms: 1.15x slower                                                  |
| docutils       | 2.62 sec                                                     | 2.93 sec: 1.12x slower                                                |
| Geometric mean | (ref)                                                        | 1.09x slower                                                          |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260809-vultr-x86_64-python-87b120fdb58afd8f7cb7-3.16.0a0-87b120f |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 678 ms: 1.35x faster                                                  |
| async_tree_io              | 876 ms                                                       | 696 ms: 1.26x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 575 ms: 1.11x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 602 ms: 1.11x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 419 ms: 1.10x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 393 ms: 1.06x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 321 ms: 1.05x faster                                                  |
| async_tree_none            | 354 ms                                                       | 342 ms: 1.04x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 512 ms: 1.02x faster                                                  |
| async_generators           | 377 ms                                                       | 387 ms: 1.03x slower                                                  |
| coroutines                 | 23.6 ms                                                      | 24.2 ms: 1.03x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.09x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260809-vultr-x86_64-python-87b120fdb58afd8f7cb7-3.16.0a0-87b120f |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 181 ms: 1.20x faster                                                  |
| float          | 77.5 ms                                                      | 84.2 ms: 1.09x slower                                                 |
| nbody          | 85.1 ms                                                      | 120 ms: 1.41x slower                                                  |
| Geometric mean | (ref)                                                        | 1.09x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260809-vultr-x86_64-python-87b120fdb58afd8f7cb7-3.16.0a0-87b120f |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 22.7 ms                                                      | 20.5 ms: 1.11x faster                                                 |
| regex_effbot   | 3.08 ms                                                      | 3.01 ms: 1.02x faster                                                 |
| regex_dna      | 180 ms                                                       | 183 ms: 1.01x slower                                                  |
| regex_compile  | 132 ms                                                       | 169 ms: 1.28x slower                                                  |
| Geometric mean | (ref)                                                        | 1.03x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260809-vultr-x86_64-python-87b120fdb58afd8f7cb7-3.16.0a0-87b120f |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                     | 1.97 sec: 1.02x faster                                                |
| json_dumps           | 10.5 ms                                                      | 10.7 ms: 1.01x slower                                                 |
| xml_etree_parse      | 136 ms                                                       | 140 ms: 1.03x slower                                                  |
| unpickle_pure_python | 210 us                                                       | 238 us: 1.13x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 333 us: 1.13x slower                                                  |
| json_loads           | 27.0 us                                                      | 30.7 us: 1.14x slower                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 101 ms: 1.18x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 74.7 ms: 1.26x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.09x slower                                                          |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260809-vultr-x86_64-python-87b120fdb58afd8f7cb7-3.16.0a0-87b120f |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.26 ms: 1.25x slower                                                 |
| python_startup         | 11.0 ms                                                      | 15.7 ms: 1.43x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.34x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260809-vultr-x86_64-python-87b120fdb58afd8f7cb7-3.16.0a0-87b120f |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.1 ms                                                      | 41.4 ms: 1.21x slower                                                 |
| mako            | 11.3 ms                                                      | 15.7 ms: 1.39x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.30x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260809-vultr-x86_64-python-87b120fdb58afd8f7cb7-3.16.0a0-87b120f |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 317 ms                                                       | 131 ms: 2.43x faster                                                  |
| mdp                        | 2.36 sec                                                     | 1.31 sec: 1.80x faster                                                |
| gc_traversal               | 3.14 ms                                                      | 1.77 ms: 1.78x faster                                                 |
| async_tree_io_tg           | 913 ms                                                       | 678 ms: 1.35x faster                                                  |
| deepcopy                   | 355 us                                                       | 271 us: 1.31x faster                                                  |
| async_tree_io              | 876 ms                                                       | 696 ms: 1.26x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 32.0 us: 1.22x faster                                                 |
| pidigits                   | 217 ms                                                       | 181 ms: 1.20x faster                                                  |
| go                         | 141 ms                                                       | 121 ms: 1.17x faster                                                  |
| sqlite_synth               | 2.21 us                                                      | 1.92 us: 1.15x faster                                                 |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 575 ms: 1.11x faster                                                  |
| regex_v8                   | 22.7 ms                                                      | 20.5 ms: 1.11x faster                                                 |
| scimark_sor                | 134 ms                                                       | 122 ms: 1.11x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 602 ms: 1.11x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 419 ms: 1.10x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 69.5 ms: 1.08x faster                                                 |
| deepcopy_reduce            | 3.11 us                                                      | 2.92 us: 1.07x faster                                                 |
| typing_runtime_protocols   | 155 us                                                       | 145 us: 1.06x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 18.0 ms: 1.06x faster                                                 |
| async_tree_memoization_tg  | 414 ms                                                       | 393 ms: 1.06x faster                                                  |
| spectral_norm              | 111 ms                                                       | 105 ms: 1.05x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 321 ms: 1.05x faster                                                  |
| async_tree_none            | 354 ms                                                       | 342 ms: 1.04x faster                                                  |
| scimark_fft                | 349 ms                                                       | 338 ms: 1.03x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 3.01 ms: 1.02x faster                                                 |
| tomli_loads                | 2.01 sec                                                     | 1.97 sec: 1.02x faster                                                |
| bpe_tokeniser              | 4.45 sec                                                     | 4.36 sec: 1.02x faster                                                |
| asyncio_websockets         | 520 ms                                                       | 512 ms: 1.02x faster                                                  |
| regex_dna                  | 180 ms                                                       | 183 ms: 1.01x slower                                                  |
| json_dumps                 | 10.5 ms                                                      | 10.7 ms: 1.01x slower                                                 |
| xml_etree_parse            | 136 ms                                                       | 140 ms: 1.03x slower                                                  |
| async_generators           | 377 ms                                                       | 387 ms: 1.03x slower                                                  |
| coroutines                 | 23.6 ms                                                      | 24.2 ms: 1.03x slower                                                 |
| logging_silent             | 103 ns                                                       | 106 ns: 1.03x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.39 ms: 1.04x slower                                                 |
| pyflate                    | 449 ms                                                       | 465 ms: 1.04x slower                                                  |
| pycparser                  | 1.12 sec                                                     | 1.17 sec: 1.05x slower                                                |
| chaos                      | 57.3 ms                                                      | 60.8 ms: 1.06x slower                                                 |
| hexiom                     | 5.99 ms                                                      | 6.49 ms: 1.08x slower                                                 |
| float                      | 77.5 ms                                                      | 84.2 ms: 1.09x slower                                                 |
| comprehensions             | 16.5 us                                                      | 17.9 us: 1.09x slower                                                 |
| json                       | 4.93 ms                                                      | 5.39 ms: 1.09x slower                                                 |
| sympy_integrate            | 19.8 ms                                                      | 21.7 ms: 1.10x slower                                                 |
| pprint_safe_repr           | 738 ms                                                       | 826 ms: 1.12x slower                                                  |
| docutils                   | 2.62 sec                                                     | 2.93 sec: 1.12x slower                                                |
| nqueens                    | 78.6 ms                                                      | 88.3 ms: 1.12x slower                                                 |
| unpickle_pure_python       | 210 us                                                       | 238 us: 1.13x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 333 us: 1.13x slower                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.33 ms: 1.13x slower                                                 |
| json_loads                 | 27.0 us                                                      | 30.7 us: 1.14x slower                                                 |
| logging_simple             | 6.16 us                                                      | 7.02 us: 1.14x slower                                                 |
| pprint_pformat             | 1.50 sec                                                     | 1.71 sec: 1.14x slower                                                |
| 2to3                       | 260 ms                                                       | 298 ms: 1.15x slower                                                  |
| generators                 | 28.8 ms                                                      | 33.0 ms: 1.15x slower                                                 |
| scimark_lu                 | 113 ms                                                       | 130 ms: 1.15x slower                                                  |
| sympy_str                  | 275 ms                                                       | 316 ms: 1.15x slower                                                  |
| sympy_sum                  | 156 ms                                                       | 180 ms: 1.16x slower                                                  |
| sympy_expand               | 457 ms                                                       | 531 ms: 1.16x slower                                                  |
| raytrace                   | 253 ms                                                       | 294 ms: 1.17x slower                                                  |
| richards                   | 45.2 ms                                                      | 52.9 ms: 1.17x slower                                                 |
| richards_super             | 51.6 ms                                                      | 60.5 ms: 1.17x slower                                                 |
| deltablue                  | 3.12 ms                                                      | 3.68 ms: 1.18x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 101 ms: 1.18x slower                                                  |
| thrift                     | 778 us                                                       | 924 us: 1.19x slower                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 78.0 ms: 1.19x slower                                                 |
| logging_format             | 6.84 us                                                      | 8.20 us: 1.20x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 13.2 ms: 1.20x slower                                                 |
| django_template            | 34.1 ms                                                      | 41.4 ms: 1.21x slower                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 9.26 ms: 1.25x slower                                                 |
| xml_etree_process          | 59.3 ms                                                      | 74.7 ms: 1.26x slower                                                 |
| meteor_contest             | 102 ms                                                       | 128 ms: 1.26x slower                                                  |
| fannkuch                   | 370 ms                                                       | 468 ms: 1.26x slower                                                  |
| regex_compile              | 132 ms                                                       | 169 ms: 1.28x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 89.2 ms: 1.31x slower                                                 |
| coverage                   | 83.0 ms                                                      | 114 ms: 1.37x slower                                                  |
| mako                       | 11.3 ms                                                      | 15.7 ms: 1.39x slower                                                 |
| nbody                      | 85.1 ms                                                      | 120 ms: 1.41x slower                                                  |
| python_startup             | 11.0 ms                                                      | 15.7 ms: 1.43x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 1.49 ms: 1.62x slower                                                 |
| telco                      | 7.82 ms                                                      | 175 ms: 22.38x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.08x slower                                                          |

Benchmark hidden because not significant (2): xml_etree_iterparse, html5lib
Ignored benchmarks (20) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260809-3.16.0a0-87b120f-NOGIL/bm-20260809-vultr-x86_64-python-87b120fdb58afd8f7cb7-3.16.0a0-87b120f.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.069x slower

# HPT report

- Reliability score: 97.91% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.36x