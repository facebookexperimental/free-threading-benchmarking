# Results vs. 3.13.0rc2

- fork: python
- ref: 87b120fdb58afd8f7cb7
- machine: linux-x86_64
- commit hash: 87b120f
- commit date: 2026-08-09
- overall geometric mean: 1.036x faster
- HPT reliability: 99.94%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260809-vultr-x86_64-python-87b120fdb58afd8f7cb7-3.16.0a0-87b120f |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 261 ms: 1.00x slower                                                  |
| docutils       | 2.62 sec                                                     | 2.37 sec: 1.11x faster                                                |
| html5lib       | 67.0 ms                                                      | 57.7 ms: 1.16x faster                                                 |
| Geometric mean | (ref)                                                        | 1.09x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260809-vultr-x86_64-python-87b120fdb58afd8f7cb7-3.16.0a0-87b120f |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 666 ms                                                       | 534 ms: 1.25x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 373 ms: 1.24x faster                                                  |
| async_tree_none            | 354 ms                                                       | 291 ms: 1.22x faster                                                  |
| async_tree_io              | 876 ms                                                       | 722 ms: 1.21x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 763 ms: 1.20x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 554 ms: 1.15x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 363 ms: 1.14x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 297 ms: 1.13x faster                                                  |
| async_generators           | 377 ms                                                       | 341 ms: 1.11x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 22.9 ms: 1.03x faster                                                 |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.04x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.14x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260809-vultr-x86_64-python-87b120fdb58afd8f7cb7-3.16.0a0-87b120f |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 188 ms: 1.16x faster                                                  |
| float          | 77.5 ms                                                      | 72.8 ms: 1.06x faster                                                 |
| nbody          | 85.1 ms                                                      | 92.6 ms: 1.09x slower                                                 |
| Geometric mean | (ref)                                                        | 1.04x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260809-vultr-x86_64-python-87b120fdb58afd8f7cb7-3.16.0a0-87b120f |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.56 ms: 1.20x faster                                                 |
| regex_v8       | 22.7 ms                                                      | 21.1 ms: 1.07x faster                                                 |
| regex_dna      | 180 ms                                                       | 176 ms: 1.03x faster                                                  |
| regex_compile  | 132 ms                                                       | 148 ms: 1.12x slower                                                  |
| Geometric mean | (ref)                                                        | 1.04x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260809-vultr-x86_64-python-87b120fdb58afd8f7cb7-3.16.0a0-87b120f |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                     | 1.79 sec: 1.12x faster                                                |
| json_dumps           | 10.5 ms                                                      | 9.94 ms: 1.06x faster                                                 |
| xml_etree_iterparse  | 94.9 ms                                                      | 91.7 ms: 1.04x faster                                                 |
| unpickle_pure_python | 210 us                                                       | 214 us: 1.02x slower                                                  |
| json_loads           | 27.0 us                                                      | 27.7 us: 1.02x slower                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 87.5 ms: 1.02x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 306 us: 1.04x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 62.3 ms: 1.05x slower                                                 |
| xml_etree_parse      | 136 ms                                                       | 143 ms: 1.05x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.00x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260809-vultr-x86_64-python-87b120fdb58afd8f7cb7-3.16.0a0-87b120f |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.08 ms: 1.04x faster                                                 |
| python_startup         | 11.0 ms                                                      | 12.6 ms: 1.15x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.05x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260809-vultr-x86_64-python-87b120fdb58afd8f7cb7-3.16.0a0-87b120f |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 11.3 ms                                                      | 11.8 ms: 1.04x slower                                                 |
| django_template | 34.1 ms                                                      | 36.5 ms: 1.07x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.06x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260809-vultr-x86_64-python-87b120fdb58afd8f7cb7-3.16.0a0-87b120f |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 317 ms                                                       | 114 ms: 2.77x faster                                                  |
| mdp                        | 2.36 sec                                                     | 1.12 sec: 2.10x faster                                                |
| deepcopy                   | 355 us                                                       | 233 us: 1.53x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 26.6 us: 1.47x faster                                                 |
| go                         | 141 ms                                                       | 105 ms: 1.34x faster                                                  |
| typing_runtime_protocols   | 155 us                                                       | 119 us: 1.30x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 534 ms: 1.25x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 373 ms: 1.24x faster                                                  |
| spectral_norm              | 111 ms                                                       | 90.9 ms: 1.22x faster                                                 |
| async_tree_none            | 354 ms                                                       | 291 ms: 1.22x faster                                                  |
| scimark_sor                | 134 ms                                                       | 111 ms: 1.22x faster                                                  |
| async_tree_io              | 876 ms                                                       | 722 ms: 1.21x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.58 us: 1.20x faster                                                 |
| regex_effbot               | 3.08 ms                                                      | 2.56 ms: 1.20x faster                                                 |
| async_tree_io_tg           | 913 ms                                                       | 763 ms: 1.20x faster                                                  |
| html5lib                   | 67.0 ms                                                      | 57.7 ms: 1.16x faster                                                 |
| pyflate                    | 449 ms                                                       | 388 ms: 1.16x faster                                                  |
| pidigits                   | 217 ms                                                       | 188 ms: 1.16x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 554 ms: 1.15x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 363 ms: 1.14x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 297 ms: 1.13x faster                                                  |
| scimark_fft                | 349 ms                                                       | 309 ms: 1.13x faster                                                  |
| tomli_loads                | 2.01 sec                                                     | 1.79 sec: 1.12x faster                                                |
| dulwich_log                | 74.8 ms                                                      | 67.0 ms: 1.12x faster                                                 |
| async_generators           | 377 ms                                                       | 341 ms: 1.11x faster                                                  |
| docutils                   | 2.62 sec                                                     | 2.37 sec: 1.11x faster                                                |
| nqueens                    | 78.6 ms                                                      | 73.1 ms: 1.08x faster                                                 |
| regex_v8                   | 22.7 ms                                                      | 21.1 ms: 1.07x faster                                                 |
| chaos                      | 57.3 ms                                                      | 53.7 ms: 1.07x faster                                                 |
| pathlib                    | 19.2 ms                                                      | 18.0 ms: 1.07x faster                                                 |
| float                      | 77.5 ms                                                      | 72.8 ms: 1.06x faster                                                 |
| json_dumps                 | 10.5 ms                                                      | 9.94 ms: 1.06x faster                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.23 sec: 1.05x faster                                                |
| hexiom                     | 5.99 ms                                                      | 5.72 ms: 1.05x faster                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 7.08 ms: 1.04x faster                                                 |
| comprehensions             | 16.5 us                                                      | 15.8 us: 1.04x faster                                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 62.9 ms: 1.04x faster                                                 |
| sympy_integrate            | 19.8 ms                                                      | 19.1 ms: 1.04x faster                                                 |
| xml_etree_iterparse        | 94.9 ms                                                      | 91.7 ms: 1.04x faster                                                 |
| generators                 | 28.8 ms                                                      | 27.9 ms: 1.03x faster                                                 |
| logging_silent             | 103 ns                                                       | 99.4 ns: 1.03x faster                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.58 ms: 1.03x faster                                                 |
| coroutines                 | 23.6 ms                                                      | 22.9 ms: 1.03x faster                                                 |
| regex_dna                  | 180 ms                                                       | 176 ms: 1.03x faster                                                  |
| richards                   | 45.2 ms                                                      | 44.4 ms: 1.02x faster                                                 |
| logging_simple             | 6.16 us                                                      | 6.05 us: 1.02x faster                                                 |
| richards_super             | 51.6 ms                                                      | 50.9 ms: 1.01x faster                                                 |
| logging_format             | 6.84 us                                                      | 6.76 us: 1.01x faster                                                 |
| pprint_pformat             | 1.50 sec                                                     | 1.48 sec: 1.01x faster                                                |
| pprint_safe_repr           | 738 ms                                                       | 730 ms: 1.01x faster                                                  |
| json                       | 4.93 ms                                                      | 4.88 ms: 1.01x faster                                                 |
| crypto_pyaes               | 67.9 ms                                                      | 67.3 ms: 1.01x faster                                                 |
| fannkuch                   | 370 ms                                                       | 370 ms: 1.00x slower                                                  |
| 2to3                       | 260 ms                                                       | 261 ms: 1.00x slower                                                  |
| meteor_contest             | 102 ms                                                       | 102 ms: 1.01x slower                                                  |
| coverage                   | 83.0 ms                                                      | 83.4 ms: 1.01x slower                                                 |
| pycparser                  | 1.12 sec                                                     | 1.13 sec: 1.01x slower                                                |
| raytrace                   | 253 ms                                                       | 255 ms: 1.01x slower                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.23 us: 1.01x slower                                                 |
| thrift                     | 778 us                                                       | 787 us: 1.01x slower                                                  |
| sympy_str                  | 275 ms                                                       | 279 ms: 1.02x slower                                                  |
| sympy_sum                  | 156 ms                                                       | 158 ms: 1.02x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 214 us: 1.02x slower                                                  |
| json_loads                 | 27.0 us                                                      | 27.7 us: 1.02x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 87.5 ms: 1.02x slower                                                 |
| scimark_lu                 | 113 ms                                                       | 116 ms: 1.03x slower                                                  |
| sympy_expand               | 457 ms                                                       | 473 ms: 1.04x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 306 us: 1.04x slower                                                  |
| mako                       | 11.3 ms                                                      | 11.8 ms: 1.04x slower                                                 |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.04x slower                                                  |
| xml_etree_process          | 59.3 ms                                                      | 62.3 ms: 1.05x slower                                                 |
| xml_etree_parse            | 136 ms                                                       | 143 ms: 1.05x slower                                                  |
| django_template            | 34.1 ms                                                      | 36.5 ms: 1.07x slower                                                 |
| nbody                      | 85.1 ms                                                      | 92.6 ms: 1.09x slower                                                 |
| deltablue                  | 3.12 ms                                                      | 3.40 ms: 1.09x slower                                                 |
| regex_compile              | 132 ms                                                       | 148 ms: 1.12x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 3.54 ms: 1.12x slower                                                 |
| python_startup             | 11.0 ms                                                      | 12.6 ms: 1.15x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.64 ms: 1.23x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 1.36 ms: 1.48x slower                                                 |
| telco                      | 7.82 ms                                                      | 159 ms: 20.38x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 227 ms: 20.60x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.01x slower                                                          |
Ignored benchmarks (20) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260809-3.16.0a0-87b120f/bm-20260809-vultr-x86_64-python-87b120fdb58afd8f7cb7-3.16.0a0-87b120f.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.036x faster

# HPT report

- Reliability score: 99.94% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.14x