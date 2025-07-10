# Results vs. 3.13.0rc2

- fork: python
- ref: 61dd9fdad729fe02d91c
- machine: linux-x86_64
- commit hash: 61dd9fd
- commit date: 2025-07-10
- overall geometric mean: 1.031x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 251 ms: 1.04x faster                                                  |
| docutils       | 2.62 sec                                                     | 2.55 sec: 1.02x faster                                                |
| html5lib       | 67.0 ms                                                      | 61.2 ms: 1.10x faster                                                 |
| Geometric mean | (ref)                                                        | 1.05x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 613 ms: 1.49x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 314 ms: 1.47x faster                                                  |
| async_tree_io              | 876 ms                                                       | 598 ms: 1.47x faster                                                  |
| async_tree_none            | 354 ms                                                       | 256 ms: 1.38x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 490 ms: 1.36x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 310 ms: 1.34x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 255 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 496 ms: 1.28x faster                                                  |
| async_generators           | 377 ms                                                       | 339 ms: 1.11x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 23.0 ms: 1.02x faster                                                 |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                  |
| Geometric mean             | (ref)                                                        | 1.28x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 195 ms: 1.11x faster                                                  |
| float          | 77.5 ms                                                      | 70.8 ms: 1.09x faster                                                 |
| nbody          | 85.1 ms                                                      | 93.6 ms: 1.10x slower                                                 |
| Geometric mean | (ref)                                                        | 1.03x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.72 ms: 1.13x faster                                                 |
| regex_compile  | 132 ms                                                       | 124 ms: 1.07x faster                                                  |
| regex_dna      | 180 ms                                                       | 176 ms: 1.03x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 23.1 ms: 1.02x slower                                                 |
| Geometric mean | (ref)                                                        | 1.05x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                     | 1.93 sec: 1.04x faster                                                |
| xml_etree_generate   | 85.4 ms                                                      | 82.7 ms: 1.03x faster                                                 |
| xml_etree_parse      | 136 ms                                                       | 132 ms: 1.03x faster                                                  |
| xml_etree_process    | 59.3 ms                                                      | 57.7 ms: 1.03x faster                                                 |
| xml_etree_iterparse  | 94.9 ms                                                      | 92.9 ms: 1.02x faster                                                 |
| unpickle_pure_python | 210 us                                                       | 211 us: 1.01x slower                                                  |
| json_dumps           | 10.5 ms                                                      | 10.9 ms: 1.04x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 309 us: 1.05x slower                                                  |
| json_loads           | 27.0 us                                                      | 28.7 us: 1.06x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.00x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.35 ms: 1.01x faster                                                 |
| python_startup         | 11.0 ms                                                      | 12.7 ms: 1.15x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.07x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text    | 21.5 ms                                                      | 20.6 ms: 1.05x faster                                                 |
| genshi_xml     | 48.8 ms                                                      | 48.4 ms: 1.01x faster                                                 |
| mako           | 11.3 ms                                                      | 11.5 ms: 1.02x slower                                                 |
| Geometric mean | (ref)                                                        | 1.01x faster                                                          |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.15 sec: 2.05x faster                                                |
| async_tree_io_tg           | 913 ms                                                       | 613 ms: 1.49x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 314 ms: 1.47x faster                                                  |
| async_tree_io              | 876 ms                                                       | 598 ms: 1.47x faster                                                  |
| deepcopy                   | 355 us                                                       | 251 us: 1.42x faster                                                  |
| async_tree_none            | 354 ms                                                       | 256 ms: 1.38x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 490 ms: 1.36x faster                                                  |
| go                         | 141 ms                                                       | 104 ms: 1.35x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 310 ms: 1.34x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 29.2 us: 1.34x faster                                                 |
| async_tree_none_tg         | 336 ms                                                       | 255 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 496 ms: 1.28x faster                                                  |
| scimark_sor                | 134 ms                                                       | 111 ms: 1.22x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.62 us: 1.19x faster                                                 |
| dulwich_log                | 74.8 ms                                                      | 65.8 ms: 1.14x faster                                                 |
| pylint                     | 317 ms                                                       | 279 ms: 1.14x faster                                                  |
| pyflate                    | 449 ms                                                       | 396 ms: 1.13x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.72 ms: 1.13x faster                                                 |
| spectral_norm              | 111 ms                                                       | 98.8 ms: 1.12x faster                                                 |
| async_generators           | 377 ms                                                       | 339 ms: 1.11x faster                                                  |
| pidigits                   | 217 ms                                                       | 195 ms: 1.11x faster                                                  |
| richards_super             | 51.6 ms                                                      | 46.6 ms: 1.11x faster                                                 |
| richards                   | 45.2 ms                                                      | 40.9 ms: 1.11x faster                                                 |
| html5lib                   | 67.0 ms                                                      | 61.2 ms: 1.10x faster                                                 |
| float                      | 77.5 ms                                                      | 70.8 ms: 1.09x faster                                                 |
| regex_compile              | 132 ms                                                       | 124 ms: 1.07x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.17 sec: 1.07x faster                                                |
| hexiom                     | 5.99 ms                                                      | 5.63 ms: 1.06x faster                                                 |
| pprint_safe_repr           | 738 ms                                                       | 695 ms: 1.06x faster                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.42 sec: 1.06x faster                                                |
| comprehensions             | 16.5 us                                                      | 15.6 us: 1.06x faster                                                 |
| sympy_integrate            | 19.8 ms                                                      | 18.8 ms: 1.05x faster                                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 62.3 ms: 1.05x faster                                                 |
| logging_simple             | 6.16 us                                                      | 5.88 us: 1.05x faster                                                 |
| genshi_text                | 21.5 ms                                                      | 20.6 ms: 1.05x faster                                                 |
| generators                 | 28.8 ms                                                      | 27.7 ms: 1.04x faster                                                 |
| tomli_loads                | 2.01 sec                                                     | 1.93 sec: 1.04x faster                                                |
| 2to3                       | 260 ms                                                       | 251 ms: 1.04x faster                                                  |
| logging_format             | 6.84 us                                                      | 6.61 us: 1.03x faster                                                 |
| scimark_fft                | 349 ms                                                       | 338 ms: 1.03x faster                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 82.7 ms: 1.03x faster                                                 |
| logging_silent             | 103 ns                                                       | 99.3 ns: 1.03x faster                                                 |
| xml_etree_parse            | 136 ms                                                       | 132 ms: 1.03x faster                                                  |
| meteor_contest             | 102 ms                                                       | 98.7 ms: 1.03x faster                                                 |
| chaos                      | 57.3 ms                                                      | 55.7 ms: 1.03x faster                                                 |
| xml_etree_process          | 59.3 ms                                                      | 57.7 ms: 1.03x faster                                                 |
| regex_dna                  | 180 ms                                                       | 176 ms: 1.03x faster                                                  |
| docutils                   | 2.62 sec                                                     | 2.55 sec: 1.02x faster                                                |
| coroutines                 | 23.6 ms                                                      | 23.0 ms: 1.02x faster                                                 |
| xml_etree_iterparse        | 94.9 ms                                                      | 92.9 ms: 1.02x faster                                                 |
| sympy_str                  | 275 ms                                                       | 269 ms: 1.02x faster                                                  |
| thrift                     | 778 us                                                       | 763 us: 1.02x faster                                                  |
| pycparser                  | 1.12 sec                                                     | 1.10 sec: 1.02x faster                                                |
| sympy_sum                  | 156 ms                                                       | 153 ms: 1.02x faster                                                  |
| typing_runtime_protocols   | 155 us                                                       | 152 us: 1.02x faster                                                  |
| coverage                   | 83.0 ms                                                      | 81.9 ms: 1.01x faster                                                 |
| genshi_xml                 | 48.8 ms                                                      | 48.4 ms: 1.01x faster                                                 |
| deltablue                  | 3.12 ms                                                      | 3.10 ms: 1.01x faster                                                 |
| nqueens                    | 78.6 ms                                                      | 78.1 ms: 1.01x faster                                                 |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 7.35 ms: 1.01x faster                                                 |
| crypto_pyaes               | 67.9 ms                                                      | 68.2 ms: 1.00x slower                                                 |
| raytrace                   | 253 ms                                                       | 254 ms: 1.01x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 211 us: 1.01x slower                                                  |
| pathlib                    | 19.2 ms                                                      | 19.3 ms: 1.01x slower                                                 |
| sqlite_synth               | 2.21 us                                                      | 2.24 us: 1.01x slower                                                 |
| mako                       | 11.3 ms                                                      | 11.5 ms: 1.02x slower                                                 |
| regex_v8                   | 22.7 ms                                                      | 23.1 ms: 1.02x slower                                                 |
| fannkuch                   | 370 ms                                                       | 380 ms: 1.03x slower                                                  |
| sympy_expand               | 457 ms                                                       | 471 ms: 1.03x slower                                                  |
| json_dumps                 | 10.5 ms                                                      | 10.9 ms: 1.04x slower                                                 |
| json                       | 4.93 ms                                                      | 5.15 ms: 1.05x slower                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.93 ms: 1.05x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 309 us: 1.05x slower                                                  |
| json_loads                 | 27.0 us                                                      | 28.7 us: 1.06x slower                                                 |
| nbody                      | 85.1 ms                                                      | 93.6 ms: 1.10x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 1.05 ms: 1.14x slower                                                 |
| python_startup             | 11.0 ms                                                      | 12.7 ms: 1.15x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 4.37 ms: 1.39x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.97 ms: 1.47x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 103 ms: 9.38x slower                                                  |
| telco                      | 7.82 ms                                                      | 160 ms: 20.40x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.00x faster                                                          |

Benchmark hidden because not significant (2): django_template, scimark_lu
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250710-3.15.0a0-61dd9fd/bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.031x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.15x