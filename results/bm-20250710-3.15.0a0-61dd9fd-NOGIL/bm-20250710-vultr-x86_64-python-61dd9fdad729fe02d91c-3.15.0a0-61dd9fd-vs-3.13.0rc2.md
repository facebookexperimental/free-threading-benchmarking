# Results vs. 3.13.0rc2

- fork: python
- ref: 61dd9fdad729fe02d91c
- machine: linux-x86_64
- commit hash: 61dd9fd
- commit date: 2025-07-10
- overall geometric mean: 1.059x slower
- HPT reliability: 97.80%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.38x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 283 ms: 1.09x slower                                                  |
| docutils       | 2.62 sec                                                     | 2.70 sec: 1.03x slower                                                |
| html5lib       | 67.0 ms                                                      | 66.0 ms: 1.02x faster                                                 |
| Geometric mean | (ref)                                                        | 1.03x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 523 ms: 1.75x faster                                                  |
| async_tree_io              | 876 ms                                                       | 549 ms: 1.60x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 228 ms: 1.48x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 314 ms: 1.47x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 286 ms: 1.45x faster                                                  |
| async_tree_none            | 354 ms                                                       | 258 ms: 1.37x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 490 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 517 ms: 1.29x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 512 ms: 1.02x faster                                                  |
| async_generators           | 377 ms                                                       | 372 ms: 1.01x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 24.9 ms: 1.06x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.31x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 70.4 ms: 1.10x faster                                                 |
| pidigits       | 217 ms                                                       | 204 ms: 1.06x faster                                                  |
| nbody          | 85.1 ms                                                      | 125 ms: 1.46x slower                                                  |
| Geometric mean | (ref)                                                        | 1.08x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.85 ms: 1.08x faster                                                 |
| regex_v8       | 22.7 ms                                                      | 21.5 ms: 1.05x faster                                                 |
| regex_compile  | 132 ms                                                       | 143 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                        | 1.01x faster                                                          |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 87.1 ms: 1.09x faster                                                 |
| xml_etree_parse      | 136 ms                                                       | 130 ms: 1.05x faster                                                  |
| tomli_loads          | 2.01 sec                                                     | 2.18 sec: 1.09x slower                                                |
| unpickle_pure_python | 210 us                                                       | 231 us: 1.10x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 96.2 ms: 1.13x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 339 us: 1.15x slower                                                  |
| json_loads           | 27.0 us                                                      | 31.2 us: 1.16x slower                                                 |
| json_dumps           | 10.5 ms                                                      | 12.2 ms: 1.16x slower                                                 |
| xml_etree_process    | 59.3 ms                                                      | 69.1 ms: 1.16x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.09x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.58 ms: 1.30x slower                                                 |
| python_startup         | 11.0 ms                                                      | 16.0 ms: 1.46x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.37x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.1 ms                                                      | 39.5 ms: 1.16x slower                                                 |
| genshi_xml      | 48.8 ms                                                      | 57.5 ms: 1.18x slower                                                 |
| genshi_text     | 21.5 ms                                                      | 26.9 ms: 1.25x slower                                                 |
| mako            | 11.3 ms                                                      | 15.8 ms: 1.40x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.24x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.33 sec: 1.78x faster                                                |
| async_tree_io_tg           | 913 ms                                                       | 523 ms: 1.75x faster                                                  |
| gc_traversal               | 3.14 ms                                                      | 1.90 ms: 1.66x faster                                                 |
| async_tree_io              | 876 ms                                                       | 549 ms: 1.60x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 228 ms: 1.48x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 314 ms: 1.47x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 286 ms: 1.45x faster                                                  |
| async_tree_none            | 354 ms                                                       | 258 ms: 1.37x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 490 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 517 ms: 1.29x faster                                                  |
| deepcopy                   | 355 us                                                       | 294 us: 1.21x faster                                                  |
| go                         | 141 ms                                                       | 121 ms: 1.16x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 34.7 us: 1.13x faster                                                 |
| float                      | 77.5 ms                                                      | 70.4 ms: 1.10x faster                                                 |
| xml_etree_iterparse        | 94.9 ms                                                      | 87.1 ms: 1.09x faster                                                 |
| regex_effbot               | 3.08 ms                                                      | 2.85 ms: 1.08x faster                                                 |
| scimark_sor                | 134 ms                                                       | 125 ms: 1.08x faster                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.05 us: 1.08x faster                                                 |
| pidigits                   | 217 ms                                                       | 204 ms: 1.06x faster                                                  |
| regex_v8                   | 22.7 ms                                                      | 21.5 ms: 1.05x faster                                                 |
| xml_etree_parse            | 136 ms                                                       | 130 ms: 1.05x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 72.4 ms: 1.03x faster                                                 |
| spectral_norm              | 111 ms                                                       | 109 ms: 1.02x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 512 ms: 1.02x faster                                                  |
| html5lib                   | 67.0 ms                                                      | 66.0 ms: 1.02x faster                                                 |
| async_generators           | 377 ms                                                       | 372 ms: 1.01x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.44 sec: 1.00x faster                                                |
| deepcopy_reduce            | 3.11 us                                                      | 3.12 us: 1.00x slower                                                 |
| pathlib                    | 19.2 ms                                                      | 19.3 ms: 1.00x slower                                                 |
| pycparser                  | 1.12 sec                                                     | 1.15 sec: 1.03x slower                                                |
| docutils                   | 2.62 sec                                                     | 2.70 sec: 1.03x slower                                                |
| pyflate                    | 449 ms                                                       | 467 ms: 1.04x slower                                                  |
| pprint_safe_repr           | 738 ms                                                       | 777 ms: 1.05x slower                                                  |
| hexiom                     | 5.99 ms                                                      | 6.34 ms: 1.06x slower                                                 |
| coroutines                 | 23.6 ms                                                      | 24.9 ms: 1.06x slower                                                 |
| comprehensions             | 16.5 us                                                      | 17.6 us: 1.07x slower                                                 |
| scimark_fft                | 349 ms                                                       | 374 ms: 1.07x slower                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.61 sec: 1.08x slower                                                |
| regex_compile              | 132 ms                                                       | 143 ms: 1.08x slower                                                  |
| json                       | 4.93 ms                                                      | 5.33 ms: 1.08x slower                                                 |
| tomli_loads                | 2.01 sec                                                     | 2.18 sec: 1.09x slower                                                |
| 2to3                       | 260 ms                                                       | 283 ms: 1.09x slower                                                  |
| generators                 | 28.8 ms                                                      | 31.5 ms: 1.09x slower                                                 |
| unpickle_pure_python       | 210 us                                                       | 231 us: 1.10x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.48 ms: 1.10x slower                                                 |
| chaos                      | 57.3 ms                                                      | 63.7 ms: 1.11x slower                                                 |
| sympy_integrate            | 19.8 ms                                                      | 22.1 ms: 1.11x slower                                                 |
| nqueens                    | 78.6 ms                                                      | 88.0 ms: 1.12x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 96.2 ms: 1.13x slower                                                 |
| thrift                     | 778 us                                                       | 878 us: 1.13x slower                                                  |
| logging_simple             | 6.16 us                                                      | 6.98 us: 1.13x slower                                                 |
| richards                   | 45.2 ms                                                      | 51.3 ms: 1.13x slower                                                 |
| deltablue                  | 3.12 ms                                                      | 3.56 ms: 1.14x slower                                                 |
| richards_super             | 51.6 ms                                                      | 58.8 ms: 1.14x slower                                                 |
| sympy_expand               | 457 ms                                                       | 522 ms: 1.14x slower                                                  |
| sympy_str                  | 275 ms                                                       | 314 ms: 1.14x slower                                                  |
| scimark_lu                 | 113 ms                                                       | 129 ms: 1.15x slower                                                  |
| logging_format             | 6.84 us                                                      | 7.88 us: 1.15x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 339 us: 1.15x slower                                                  |
| json_loads                 | 27.0 us                                                      | 31.2 us: 1.16x slower                                                 |
| meteor_contest             | 102 ms                                                       | 118 ms: 1.16x slower                                                  |
| django_template            | 34.1 ms                                                      | 39.5 ms: 1.16x slower                                                 |
| sympy_sum                  | 156 ms                                                       | 180 ms: 1.16x slower                                                  |
| json_dumps                 | 10.5 ms                                                      | 12.2 ms: 1.16x slower                                                 |
| xml_etree_process          | 59.3 ms                                                      | 69.1 ms: 1.16x slower                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.54 ms: 1.18x slower                                                 |
| genshi_xml                 | 48.8 ms                                                      | 57.5 ms: 1.18x slower                                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 78.5 ms: 1.20x slower                                                 |
| raytrace                   | 253 ms                                                       | 307 ms: 1.21x slower                                                  |
| typing_runtime_protocols   | 155 us                                                       | 188 us: 1.22x slower                                                  |
| genshi_text                | 21.5 ms                                                      | 26.9 ms: 1.25x slower                                                 |
| fannkuch                   | 370 ms                                                       | 463 ms: 1.25x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 85.7 ms: 1.26x slower                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 9.58 ms: 1.30x slower                                                 |
| coverage                   | 83.0 ms                                                      | 112 ms: 1.35x slower                                                  |
| mako                       | 11.3 ms                                                      | 15.8 ms: 1.40x slower                                                 |
| python_startup             | 11.0 ms                                                      | 16.0 ms: 1.46x slower                                                 |
| nbody                      | 85.1 ms                                                      | 125 ms: 1.46x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 3.15 ms: 3.43x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 108 ms: 9.85x slower                                                  |
| telco                      | 7.82 ms                                                      | 178 ms: 22.77x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.11x slower                                                          |

Benchmark hidden because not significant (3): pylint, logging_silent, regex_dna
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250710-3.15.0a0-61dd9fd-NOGIL/bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.059x slower

# HPT report

- Reliability score: 97.80% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.38x