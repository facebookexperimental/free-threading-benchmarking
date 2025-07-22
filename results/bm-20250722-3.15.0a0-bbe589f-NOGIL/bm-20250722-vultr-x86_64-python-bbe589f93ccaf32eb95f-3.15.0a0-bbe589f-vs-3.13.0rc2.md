# Results vs. 3.13.0rc2

- fork: python
- ref: bbe589f93ccaf32eb95f
- machine: linux-x86_64
- commit hash: bbe589f
- commit date: 2025-07-22
- overall geometric mean: 1.056x slower
- HPT reliability: 97.12%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.38x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 284 ms: 1.09x slower                                                  |
| docutils       | 2.62 sec                                                     | 2.70 sec: 1.03x slower                                                |
| Geometric mean | (ref)                                                        | 1.04x slower                                                          |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 510 ms: 1.79x faster                                                  |
| async_tree_io              | 876 ms                                                       | 536 ms: 1.63x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 223 ms: 1.51x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 308 ms: 1.50x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 281 ms: 1.48x faster                                                  |
| async_tree_none            | 354 ms                                                       | 253 ms: 1.40x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 485 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 509 ms: 1.31x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 513 ms: 1.01x faster                                                  |
| async_generators           | 377 ms                                                       | 375 ms: 1.01x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 24.7 ms: 1.05x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.33x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 192 ms: 1.13x faster                                                  |
| float          | 77.5 ms                                                      | 69.1 ms: 1.12x faster                                                 |
| nbody          | 85.1 ms                                                      | 126 ms: 1.48x slower                                                  |
| Geometric mean | (ref)                                                        | 1.05x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.71 ms: 1.14x faster                                                 |
| regex_v8       | 22.7 ms                                                      | 20.7 ms: 1.10x faster                                                 |
| regex_dna      | 180 ms                                                       | 175 ms: 1.03x faster                                                  |
| regex_compile  | 132 ms                                                       | 143 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                        | 1.04x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 87.1 ms: 1.09x faster                                                 |
| xml_etree_parse      | 136 ms                                                       | 130 ms: 1.05x faster                                                  |
| tomli_loads          | 2.01 sec                                                     | 2.16 sec: 1.08x slower                                                |
| unpickle_pure_python | 210 us                                                       | 233 us: 1.11x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 96.5 ms: 1.13x slower                                                 |
| json_dumps           | 10.5 ms                                                      | 12.1 ms: 1.15x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 341 us: 1.16x slower                                                  |
| json_loads           | 27.0 us                                                      | 31.5 us: 1.17x slower                                                 |
| xml_etree_process    | 59.3 ms                                                      | 70.1 ms: 1.18x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.09x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.55 ms: 1.29x slower                                                 |
| python_startup         | 11.0 ms                                                      | 15.7 ms: 1.43x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.36x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 57.4 ms: 1.18x slower                                                 |
| django_template | 34.1 ms                                                      | 40.2 ms: 1.18x slower                                                 |
| genshi_text     | 21.5 ms                                                      | 26.7 ms: 1.24x slower                                                 |
| mako            | 11.3 ms                                                      | 15.7 ms: 1.38x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.24x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.31 sec: 1.80x faster                                                |
| async_tree_io_tg           | 913 ms                                                       | 510 ms: 1.79x faster                                                  |
| async_tree_io              | 876 ms                                                       | 536 ms: 1.63x faster                                                  |
| gc_traversal               | 3.14 ms                                                      | 1.95 ms: 1.61x faster                                                 |
| async_tree_none_tg         | 336 ms                                                       | 223 ms: 1.51x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 308 ms: 1.50x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 281 ms: 1.48x faster                                                  |
| async_tree_none            | 354 ms                                                       | 253 ms: 1.40x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 485 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 509 ms: 1.31x faster                                                  |
| deepcopy                   | 355 us                                                       | 298 us: 1.19x faster                                                  |
| go                         | 141 ms                                                       | 121 ms: 1.16x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.71 ms: 1.14x faster                                                 |
| pidigits                   | 217 ms                                                       | 192 ms: 1.13x faster                                                  |
| float                      | 77.5 ms                                                      | 69.1 ms: 1.12x faster                                                 |
| deepcopy_memo              | 39.1 us                                                      | 34.9 us: 1.12x faster                                                 |
| regex_v8                   | 22.7 ms                                                      | 20.7 ms: 1.10x faster                                                 |
| xml_etree_iterparse        | 94.9 ms                                                      | 87.1 ms: 1.09x faster                                                 |
| scimark_sor                | 134 ms                                                       | 124 ms: 1.09x faster                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.06 us: 1.07x faster                                                 |
| xml_etree_parse            | 136 ms                                                       | 130 ms: 1.05x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 71.5 ms: 1.05x faster                                                 |
| regex_dna                  | 180 ms                                                       | 175 ms: 1.03x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 3.05 us: 1.02x faster                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.37 sec: 1.02x faster                                                |
| asyncio_websockets         | 520 ms                                                       | 513 ms: 1.01x faster                                                  |
| async_generators           | 377 ms                                                       | 375 ms: 1.01x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 19.4 ms: 1.01x slower                                                 |
| logging_silent             | 103 ns                                                       | 104 ns: 1.01x slower                                                  |
| spectral_norm              | 111 ms                                                       | 113 ms: 1.02x slower                                                  |
| pycparser                  | 1.12 sec                                                     | 1.14 sec: 1.02x slower                                                |
| docutils                   | 2.62 sec                                                     | 2.70 sec: 1.03x slower                                                |
| pyflate                    | 449 ms                                                       | 464 ms: 1.03x slower                                                  |
| coroutines                 | 23.6 ms                                                      | 24.7 ms: 1.05x slower                                                 |
| scimark_fft                | 349 ms                                                       | 368 ms: 1.05x slower                                                  |
| generators                 | 28.8 ms                                                      | 30.5 ms: 1.06x slower                                                 |
| pprint_safe_repr           | 738 ms                                                       | 781 ms: 1.06x slower                                                  |
| hexiom                     | 5.99 ms                                                      | 6.38 ms: 1.07x slower                                                 |
| comprehensions             | 16.5 us                                                      | 17.6 us: 1.07x slower                                                 |
| tomli_loads                | 2.01 sec                                                     | 2.16 sec: 1.08x slower                                                |
| regex_compile              | 132 ms                                                       | 143 ms: 1.08x slower                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.62 sec: 1.08x slower                                                |
| json                       | 4.93 ms                                                      | 5.37 ms: 1.09x slower                                                 |
| 2to3                       | 260 ms                                                       | 284 ms: 1.09x slower                                                  |
| chaos                      | 57.3 ms                                                      | 63.5 ms: 1.11x slower                                                 |
| unpickle_pure_python       | 210 us                                                       | 233 us: 1.11x slower                                                  |
| sympy_integrate            | 19.8 ms                                                      | 22.1 ms: 1.11x slower                                                 |
| nqueens                    | 78.6 ms                                                      | 87.6 ms: 1.11x slower                                                 |
| logging_simple             | 6.16 us                                                      | 6.94 us: 1.13x slower                                                 |
| richards                   | 45.2 ms                                                      | 51.1 ms: 1.13x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 96.5 ms: 1.13x slower                                                 |
| thrift                     | 778 us                                                       | 881 us: 1.13x slower                                                  |
| sympy_str                  | 275 ms                                                       | 312 ms: 1.14x slower                                                  |
| richards_super             | 51.6 ms                                                      | 58.9 ms: 1.14x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.53 ms: 1.14x slower                                                 |
| sympy_expand               | 457 ms                                                       | 522 ms: 1.14x slower                                                  |
| json_dumps                 | 10.5 ms                                                      | 12.1 ms: 1.15x slower                                                 |
| scimark_lu                 | 113 ms                                                       | 130 ms: 1.16x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 341 us: 1.16x slower                                                  |
| sympy_sum                  | 156 ms                                                       | 180 ms: 1.16x slower                                                  |
| json_loads                 | 27.0 us                                                      | 31.5 us: 1.17x slower                                                 |
| meteor_contest             | 102 ms                                                       | 119 ms: 1.17x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 3.67 ms: 1.18x slower                                                 |
| genshi_xml                 | 48.8 ms                                                      | 57.4 ms: 1.18x slower                                                 |
| django_template            | 34.1 ms                                                      | 40.2 ms: 1.18x slower                                                 |
| xml_etree_process          | 59.3 ms                                                      | 70.1 ms: 1.18x slower                                                 |
| raytrace                   | 253 ms                                                       | 299 ms: 1.18x slower                                                  |
| logging_format             | 6.84 us                                                      | 8.10 us: 1.18x slower                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.62 ms: 1.19x slower                                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 78.8 ms: 1.21x slower                                                 |
| fannkuch                   | 370 ms                                                       | 455 ms: 1.23x slower                                                  |
| genshi_text                | 21.5 ms                                                      | 26.7 ms: 1.24x slower                                                 |
| typing_runtime_protocols   | 155 us                                                       | 192 us: 1.24x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 86.4 ms: 1.27x slower                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 9.55 ms: 1.29x slower                                                 |
| coverage                   | 83.0 ms                                                      | 111 ms: 1.34x slower                                                  |
| mako                       | 11.3 ms                                                      | 15.7 ms: 1.38x slower                                                 |
| python_startup             | 11.0 ms                                                      | 15.7 ms: 1.43x slower                                                 |
| nbody                      | 85.1 ms                                                      | 126 ms: 1.48x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 3.16 ms: 3.44x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 108 ms: 9.82x slower                                                  |
| telco                      | 7.82 ms                                                      | 176 ms: 22.43x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.10x slower                                                          |

Benchmark hidden because not significant (2): pylint, html5lib
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250722-3.15.0a0-bbe589f-NOGIL/bm-20250722-vultr-x86_64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.056x slower

# HPT report

- Reliability score: 97.12% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.38x