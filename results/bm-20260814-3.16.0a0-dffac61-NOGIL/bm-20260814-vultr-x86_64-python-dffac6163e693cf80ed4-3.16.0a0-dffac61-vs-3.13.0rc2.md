# Results vs. 3.13.0rc2

- fork: python
- ref: dffac6163e693cf80ed4
- machine: linux-x86_64
- commit hash: dffac61
- commit date: 2026-08-14
- overall geometric mean: 1.063x slower
- HPT reliability: 95.06%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260814-vultr-x86_64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 297 ms: 1.15x slower                                                  |
| docutils       | 2.62 sec                                                     | 2.91 sec: 1.11x slower                                                |
| html5lib       | 67.0 ms                                                      | 65.7 ms: 1.02x faster                                                 |
| Geometric mean | (ref)                                                        | 1.08x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260814-vultr-x86_64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 693 ms: 1.32x faster                                                  |
| async_tree_io              | 876 ms                                                       | 704 ms: 1.24x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 602 ms: 1.11x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 583 ms: 1.09x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 425 ms: 1.09x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 401 ms: 1.03x faster                                                  |
| async_tree_none            | 354 ms                                                       | 345 ms: 1.02x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 511 ms: 1.02x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 23.9 ms: 1.01x slower                                                 |
| async_generators           | 377 ms                                                       | 394 ms: 1.04x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.07x faster                                                          |

Benchmark hidden because not significant (1): async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260814-vultr-x86_64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 180 ms: 1.20x faster                                                  |
| float          | 77.5 ms                                                      | 83.4 ms: 1.08x slower                                                 |
| nbody          | 85.1 ms                                                      | 120 ms: 1.41x slower                                                  |
| Geometric mean | (ref)                                                        | 1.08x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260814-vultr-x86_64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 22.7 ms                                                      | 20.1 ms: 1.13x faster                                                 |
| regex_effbot   | 3.08 ms                                                      | 2.88 ms: 1.07x faster                                                 |
| regex_dna      | 180 ms                                                       | 175 ms: 1.03x faster                                                  |
| regex_compile  | 132 ms                                                       | 169 ms: 1.28x slower                                                  |
| Geometric mean | (ref)                                                        | 1.01x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260814-vultr-x86_64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                     | 1.91 sec: 1.05x faster                                                |
| json_dumps           | 10.5 ms                                                      | 10.2 ms: 1.04x faster                                                 |
| xml_etree_parse      | 136 ms                                                       | 140 ms: 1.03x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 333 us: 1.13x slower                                                  |
| unpickle_pure_python | 210 us                                                       | 239 us: 1.14x slower                                                  |
| json_loads           | 27.0 us                                                      | 30.7 us: 1.14x slower                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 99.4 ms: 1.16x slower                                                 |
| xml_etree_process    | 59.3 ms                                                      | 75.1 ms: 1.27x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.08x slower                                                          |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260814-vultr-x86_64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.23 ms: 1.25x slower                                                 |
| python_startup         | 11.0 ms                                                      | 15.7 ms: 1.42x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.33x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260814-vultr-x86_64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.1 ms                                                      | 40.5 ms: 1.19x slower                                                 |
| mako            | 11.3 ms                                                      | 16.1 ms: 1.42x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.30x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260814-vultr-x86_64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 317 ms                                                       | 131 ms: 2.43x faster                                                  |
| mdp                        | 2.36 sec                                                     | 1.29 sec: 1.82x faster                                                |
| gc_traversal               | 3.14 ms                                                      | 1.78 ms: 1.77x faster                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 6.66 ms: 1.65x faster                                                 |
| deepcopy                   | 355 us                                                       | 266 us: 1.34x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 693 ms: 1.32x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 31.0 us: 1.26x faster                                                 |
| async_tree_io              | 876 ms                                                       | 704 ms: 1.24x faster                                                  |
| pidigits                   | 217 ms                                                       | 180 ms: 1.20x faster                                                  |
| go                         | 141 ms                                                       | 119 ms: 1.19x faster                                                  |
| sqlite_synth               | 2.21 us                                                      | 1.92 us: 1.15x faster                                                 |
| regex_v8                   | 22.7 ms                                                      | 20.1 ms: 1.13x faster                                                 |
| scimark_sor                | 134 ms                                                       | 120 ms: 1.12x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 602 ms: 1.11x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 583 ms: 1.09x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 425 ms: 1.09x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 17.7 ms: 1.08x faster                                                 |
| regex_effbot               | 3.08 ms                                                      | 2.88 ms: 1.07x faster                                                 |
| typing_runtime_protocols   | 155 us                                                       | 145 us: 1.06x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.93 us: 1.06x faster                                                 |
| tomli_loads                | 2.01 sec                                                     | 1.91 sec: 1.05x faster                                                |
| dulwich_log                | 74.8 ms                                                      | 71.6 ms: 1.05x faster                                                 |
| json_dumps                 | 10.5 ms                                                      | 10.2 ms: 1.04x faster                                                 |
| async_tree_memoization_tg  | 414 ms                                                       | 401 ms: 1.03x faster                                                  |
| regex_dna                  | 180 ms                                                       | 175 ms: 1.03x faster                                                  |
| async_tree_none            | 354 ms                                                       | 345 ms: 1.02x faster                                                  |
| html5lib                   | 67.0 ms                                                      | 65.7 ms: 1.02x faster                                                 |
| asyncio_websockets         | 520 ms                                                       | 511 ms: 1.02x faster                                                  |
| spectral_norm              | 111 ms                                                       | 109 ms: 1.02x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.37 sec: 1.02x faster                                                |
| scimark_fft                | 349 ms                                                       | 346 ms: 1.01x faster                                                  |
| logging_silent             | 103 ns                                                       | 103 ns: 1.00x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.35 ms: 1.01x slower                                                 |
| pyflate                    | 449 ms                                                       | 455 ms: 1.01x slower                                                  |
| coroutines                 | 23.6 ms                                                      | 23.9 ms: 1.01x slower                                                 |
| pycparser                  | 1.12 sec                                                     | 1.14 sec: 1.02x slower                                                |
| xml_etree_parse            | 136 ms                                                       | 140 ms: 1.03x slower                                                  |
| async_generators           | 377 ms                                                       | 394 ms: 1.04x slower                                                  |
| chaos                      | 57.3 ms                                                      | 60.1 ms: 1.05x slower                                                 |
| float                      | 77.5 ms                                                      | 83.4 ms: 1.08x slower                                                 |
| comprehensions             | 16.5 us                                                      | 17.8 us: 1.08x slower                                                 |
| hexiom                     | 5.99 ms                                                      | 6.51 ms: 1.09x slower                                                 |
| sympy_integrate            | 19.8 ms                                                      | 21.7 ms: 1.09x slower                                                 |
| pprint_safe_repr           | 738 ms                                                       | 808 ms: 1.10x slower                                                  |
| json                       | 4.93 ms                                                      | 5.40 ms: 1.10x slower                                                 |
| nqueens                    | 78.6 ms                                                      | 86.8 ms: 1.10x slower                                                 |
| generators                 | 28.8 ms                                                      | 32.0 ms: 1.11x slower                                                 |
| docutils                   | 2.62 sec                                                     | 2.91 sec: 1.11x slower                                                |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.25 ms: 1.11x slower                                                 |
| pprint_pformat             | 1.50 sec                                                     | 1.68 sec: 1.12x slower                                                |
| pickle_pure_python         | 294 us                                                       | 333 us: 1.13x slower                                                  |
| logging_simple             | 6.16 us                                                      | 7.00 us: 1.14x slower                                                 |
| unpickle_pure_python       | 210 us                                                       | 239 us: 1.14x slower                                                  |
| json_loads                 | 27.0 us                                                      | 30.7 us: 1.14x slower                                                 |
| richards                   | 45.2 ms                                                      | 51.5 ms: 1.14x slower                                                 |
| scimark_lu                 | 113 ms                                                       | 129 ms: 1.14x slower                                                  |
| 2to3                       | 260 ms                                                       | 297 ms: 1.15x slower                                                  |
| richards_super             | 51.6 ms                                                      | 59.2 ms: 1.15x slower                                                 |
| sympy_str                  | 275 ms                                                       | 315 ms: 1.15x slower                                                  |
| raytrace                   | 253 ms                                                       | 291 ms: 1.15x slower                                                  |
| sympy_sum                  | 156 ms                                                       | 180 ms: 1.15x slower                                                  |
| sympy_expand               | 457 ms                                                       | 531 ms: 1.16x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 99.4 ms: 1.16x slower                                                 |
| logging_format             | 6.84 us                                                      | 8.01 us: 1.17x slower                                                 |
| deltablue                  | 3.12 ms                                                      | 3.67 ms: 1.18x slower                                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 77.3 ms: 1.18x slower                                                 |
| django_template            | 34.1 ms                                                      | 40.5 ms: 1.19x slower                                                 |
| thrift                     | 778 us                                                       | 929 us: 1.19x slower                                                  |
| meteor_contest             | 102 ms                                                       | 124 ms: 1.22x slower                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 9.23 ms: 1.25x slower                                                 |
| fannkuch                   | 370 ms                                                       | 465 ms: 1.26x slower                                                  |
| xml_etree_process          | 59.3 ms                                                      | 75.1 ms: 1.27x slower                                                 |
| regex_compile              | 132 ms                                                       | 169 ms: 1.28x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 88.7 ms: 1.31x slower                                                 |
| coverage                   | 83.0 ms                                                      | 115 ms: 1.38x slower                                                  |
| nbody                      | 85.1 ms                                                      | 120 ms: 1.41x slower                                                  |
| mako                       | 11.3 ms                                                      | 16.1 ms: 1.42x slower                                                 |
| python_startup             | 11.0 ms                                                      | 15.7 ms: 1.42x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 1.48 ms: 1.61x slower                                                 |
| telco                      | 7.82 ms                                                      | 177 ms: 22.60x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.06x slower                                                          |

Benchmark hidden because not significant (2): async_tree_none_tg, xml_etree_iterparse
Ignored benchmarks (20) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260814-3.16.0a0-dffac61-NOGIL/bm-20260814-vultr-x86_64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.063x slower

# HPT report

- Reliability score: 95.06% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.36x