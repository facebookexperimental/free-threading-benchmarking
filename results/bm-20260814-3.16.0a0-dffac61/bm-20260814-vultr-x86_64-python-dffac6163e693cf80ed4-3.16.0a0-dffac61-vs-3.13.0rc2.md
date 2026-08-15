# Results vs. 3.13.0rc2

- fork: python
- ref: dffac6163e693cf80ed4
- machine: linux-x86_64
- commit hash: dffac61
- commit date: 2026-08-14
- overall geometric mean: 1.025x faster
- HPT reliability: 99.55%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260814-vultr-x86_64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 263 ms: 1.01x slower                                                  |
| docutils       | 2.62 sec                                                     | 2.40 sec: 1.09x faster                                                |
| html5lib       | 67.0 ms                                                      | 60.0 ms: 1.12x faster                                                 |
| Geometric mean | (ref)                                                        | 1.06x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260814-vultr-x86_64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 666 ms                                                       | 543 ms: 1.23x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 378 ms: 1.22x faster                                                  |
| async_tree_io              | 876 ms                                                       | 728 ms: 1.20x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 761 ms: 1.20x faster                                                  |
| async_tree_none            | 354 ms                                                       | 298 ms: 1.19x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 564 ms: 1.13x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 368 ms: 1.13x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 304 ms: 1.11x faster                                                  |
| async_generators           | 377 ms                                                       | 349 ms: 1.08x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 23.4 ms: 1.01x faster                                                 |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.04x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.13x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260814-vultr-x86_64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 187 ms: 1.16x faster                                                  |
| float          | 77.5 ms                                                      | 72.8 ms: 1.06x faster                                                 |
| nbody          | 85.1 ms                                                      | 88.1 ms: 1.04x slower                                                 |
| Geometric mean | (ref)                                                        | 1.06x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260814-vultr-x86_64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.88 ms: 1.07x faster                                                 |
| regex_v8       | 22.7 ms                                                      | 21.9 ms: 1.03x faster                                                 |
| regex_dna      | 180 ms                                                       | 192 ms: 1.07x slower                                                  |
| regex_compile  | 132 ms                                                       | 149 ms: 1.13x slower                                                  |
| Geometric mean | (ref)                                                        | 1.02x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260814-vultr-x86_64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 10.5 ms                                                      | 9.29 ms: 1.13x faster                                                 |
| tomli_loads          | 2.01 sec                                                     | 1.81 sec: 1.11x faster                                                |
| xml_etree_iterparse  | 94.9 ms                                                      | 91.5 ms: 1.04x faster                                                 |
| json_loads           | 27.0 us                                                      | 27.3 us: 1.01x slower                                                 |
| unpickle_pure_python | 210 us                                                       | 213 us: 1.01x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 88.5 ms: 1.04x slower                                                 |
| xml_etree_parse      | 136 ms                                                       | 143 ms: 1.05x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 62.5 ms: 1.05x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 312 us: 1.06x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.01x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260814-vultr-x86_64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.06 ms: 1.05x faster                                                 |
| python_startup         | 11.0 ms                                                      | 12.6 ms: 1.15x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.05x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260814-vultr-x86_64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.1 ms                                                      | 36.6 ms: 1.07x slower                                                 |
| mako            | 11.3 ms                                                      | 12.3 ms: 1.08x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.08x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260814-vultr-x86_64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 317 ms                                                       | 115 ms: 2.76x faster                                                  |
| mdp                        | 2.36 sec                                                     | 1.13 sec: 2.08x faster                                                |
| deepcopy                   | 355 us                                                       | 237 us: 1.50x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 26.7 us: 1.46x faster                                                 |
| go                         | 141 ms                                                       | 106 ms: 1.33x faster                                                  |
| typing_runtime_protocols   | 155 us                                                       | 122 us: 1.27x faster                                                  |
| scimark_sor                | 134 ms                                                       | 109 ms: 1.24x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 543 ms: 1.23x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 378 ms: 1.22x faster                                                  |
| spectral_norm              | 111 ms                                                       | 91.1 ms: 1.22x faster                                                 |
| async_tree_io              | 876 ms                                                       | 728 ms: 1.20x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 761 ms: 1.20x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.61 us: 1.19x faster                                                 |
| async_tree_none            | 354 ms                                                       | 298 ms: 1.19x faster                                                  |
| pyflate                    | 449 ms                                                       | 387 ms: 1.16x faster                                                  |
| pidigits                   | 217 ms                                                       | 187 ms: 1.16x faster                                                  |
| json_dumps                 | 10.5 ms                                                      | 9.29 ms: 1.13x faster                                                 |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 564 ms: 1.13x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 368 ms: 1.13x faster                                                  |
| html5lib                   | 67.0 ms                                                      | 60.0 ms: 1.12x faster                                                 |
| scimark_fft                | 349 ms                                                       | 314 ms: 1.11x faster                                                  |
| tomli_loads                | 2.01 sec                                                     | 1.81 sec: 1.11x faster                                                |
| async_tree_none_tg         | 336 ms                                                       | 304 ms: 1.11x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 67.8 ms: 1.10x faster                                                 |
| docutils                   | 2.62 sec                                                     | 2.40 sec: 1.09x faster                                                |
| async_generators           | 377 ms                                                       | 349 ms: 1.08x faster                                                  |
| nqueens                    | 78.6 ms                                                      | 73.4 ms: 1.07x faster                                                 |
| regex_effbot               | 3.08 ms                                                      | 2.88 ms: 1.07x faster                                                 |
| pathlib                    | 19.2 ms                                                      | 17.9 ms: 1.07x faster                                                 |
| float                      | 77.5 ms                                                      | 72.8 ms: 1.06x faster                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.20 sec: 1.06x faster                                                |
| chaos                      | 57.3 ms                                                      | 54.2 ms: 1.06x faster                                                 |
| hexiom                     | 5.99 ms                                                      | 5.69 ms: 1.05x faster                                                 |
| comprehensions             | 16.5 us                                                      | 15.7 us: 1.05x faster                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 7.06 ms: 1.05x faster                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.52 ms: 1.04x faster                                                 |
| logging_silent             | 103 ns                                                       | 98.7 ns: 1.04x faster                                                 |
| xml_etree_iterparse        | 94.9 ms                                                      | 91.5 ms: 1.04x faster                                                 |
| regex_v8                   | 22.7 ms                                                      | 21.9 ms: 1.03x faster                                                 |
| sympy_integrate            | 19.8 ms                                                      | 19.2 ms: 1.03x faster                                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 63.5 ms: 1.03x faster                                                 |
| json                       | 4.93 ms                                                      | 4.86 ms: 1.01x faster                                                 |
| coroutines                 | 23.6 ms                                                      | 23.4 ms: 1.01x faster                                                 |
| sqlite_synth               | 2.21 us                                                      | 2.19 us: 1.01x faster                                                 |
| pprint_safe_repr           | 738 ms                                                       | 732 ms: 1.01x faster                                                  |
| richards_super             | 51.6 ms                                                      | 51.5 ms: 1.00x faster                                                 |
| fannkuch                   | 370 ms                                                       | 369 ms: 1.00x faster                                                  |
| raytrace                   | 253 ms                                                       | 254 ms: 1.01x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 68.3 ms: 1.01x slower                                                 |
| thrift                     | 778 us                                                       | 783 us: 1.01x slower                                                  |
| pycparser                  | 1.12 sec                                                     | 1.13 sec: 1.01x slower                                                |
| json_loads                 | 27.0 us                                                      | 27.3 us: 1.01x slower                                                 |
| logging_simple             | 6.16 us                                                      | 6.23 us: 1.01x slower                                                 |
| 2to3                       | 260 ms                                                       | 263 ms: 1.01x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 213 us: 1.01x slower                                                  |
| meteor_contest             | 102 ms                                                       | 103 ms: 1.01x slower                                                  |
| sympy_sum                  | 156 ms                                                       | 159 ms: 1.02x slower                                                  |
| sympy_str                  | 275 ms                                                       | 280 ms: 1.02x slower                                                  |
| nbody                      | 85.1 ms                                                      | 88.1 ms: 1.04x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 88.5 ms: 1.04x slower                                                 |
| generators                 | 28.8 ms                                                      | 29.9 ms: 1.04x slower                                                 |
| logging_format             | 6.84 us                                                      | 7.12 us: 1.04x slower                                                 |
| sympy_expand               | 457 ms                                                       | 477 ms: 1.04x slower                                                  |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.04x slower                                                  |
| xml_etree_parse            | 136 ms                                                       | 143 ms: 1.05x slower                                                  |
| xml_etree_process          | 59.3 ms                                                      | 62.5 ms: 1.05x slower                                                 |
| scimark_lu                 | 113 ms                                                       | 119 ms: 1.06x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 312 us: 1.06x slower                                                  |
| regex_dna                  | 180 ms                                                       | 192 ms: 1.07x slower                                                  |
| django_template            | 34.1 ms                                                      | 36.6 ms: 1.07x slower                                                 |
| mako                       | 11.3 ms                                                      | 12.3 ms: 1.08x slower                                                 |
| deltablue                  | 3.12 ms                                                      | 3.41 ms: 1.09x slower                                                 |
| regex_compile              | 132 ms                                                       | 149 ms: 1.13x slower                                                  |
| python_startup             | 11.0 ms                                                      | 12.6 ms: 1.15x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.65 ms: 1.24x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 4.03 ms: 1.28x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 1.35 ms: 1.47x slower                                                 |
| telco                      | 7.82 ms                                                      | 164 ms: 20.90x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 249 ms: 22.68x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.02x slower                                                          |

Benchmark hidden because not significant (3): pprint_pformat, richards, coverage
Ignored benchmarks (20) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260814-3.16.0a0-dffac61/bm-20260814-vultr-x86_64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.025x faster

# HPT report

- Reliability score: 99.55% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.14x