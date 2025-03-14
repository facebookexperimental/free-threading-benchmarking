# Results vs. 3.12.6

- fork: mpage
- ref: measure_lfb
- machine: linux-x86_64
- commit hash: 8ea82b5
- commit date: 2025-03-13
- overall geometric mean: 1.025x slower
- HPT reliability: 99.79%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250313-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-8ea82b5 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 290 ms: 1.10x slower                                         |
| docutils       | 2.64 sec                                               | 2.78 sec: 1.05x slower                                       |
| html5lib       | 63.6 ms                                                | 70.4 ms: 1.11x slower                                        |
| Geometric mean | (ref)                                                  | 1.09x slower                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250313-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-8ea82b5 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 538 ms: 2.06x faster                                         |
| async_tree_none_tg         | 446 ms                                                 | 230 ms: 1.94x faster                                         |
| async_tree_io              | 1.08 sec                                               | 573 ms: 1.89x faster                                         |
| async_tree_memoization_tg  | 560 ms                                                 | 298 ms: 1.88x faster                                         |
| async_tree_none            | 464 ms                                                 | 269 ms: 1.72x faster                                         |
| async_tree_memoization     | 555 ms                                                 | 330 ms: 1.68x faster                                         |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 563 ms: 1.28x faster                                         |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 595 ms: 1.20x faster                                         |
| async_generators           | 384 ms                                                 | 372 ms: 1.03x faster                                         |
| coroutines                 | 23.9 ms                                                | 23.5 ms: 1.02x faster                                        |
| asyncio_websockets         | 517 ms                                                 | 519 ms: 1.00x slower                                         |
| Geometric mean             | (ref)                                                  | 1.46x faster                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250313-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-8ea82b5 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| float          | 80.8 ms                                                | 71.2 ms: 1.13x faster                                        |
| pidigits       | 184 ms                                                 | 226 ms: 1.23x slower                                         |
| nbody          | 89.3 ms                                                | 118 ms: 1.33x slower                                         |
| Geometric mean | (ref)                                                  | 1.13x slower                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250313-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-8ea82b5 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.79 ms: 1.14x faster                                        |
| regex_compile  | 142 ms                                                 | 153 ms: 1.07x slower                                         |
| regex_dna      | 168 ms                                                 | 183 ms: 1.09x slower                                         |
| regex_v8       | 20.6 ms                                                | 24.2 ms: 1.17x slower                                        |
| Geometric mean | (ref)                                                  | 1.05x slower                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250313-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-8ea82b5 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.2 ms: 1.10x faster                                        |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.08x faster                                         |
| tomli_loads          | 2.11 sec                                               | 2.24 sec: 1.06x slower                                       |
| unpickle_pure_python | 221 us                                                 | 238 us: 1.08x slower                                         |
| json_loads           | 26.5 us                                                | 29.1 us: 1.10x slower                                        |
| pickle_pure_python   | 308 us                                                 | 340 us: 1.11x slower                                         |
| xml_etree_generate   | 85.2 ms                                                | 95.7 ms: 1.12x slower                                        |
| xml_etree_process    | 59.0 ms                                                | 68.7 ms: 1.17x slower                                        |
| json_dumps           | 10.4 ms                                                | 12.5 ms: 1.21x slower                                        |
| Geometric mean       | (ref)                                                  | 1.07x slower                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250313-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-8ea82b5 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 11.1 ms: 1.56x slower                                        |
| python_startup         | 9.93 ms                                                | 15.8 ms: 1.59x slower                                        |
| Geometric mean         | (ref)                                                  | 1.57x slower                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250313-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-8ea82b5 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 58.6 ms: 1.17x slower                                        |
| genshi_text     | 22.8 ms                                                | 26.8 ms: 1.18x slower                                        |
| django_template | 34.7 ms                                                | 41.8 ms: 1.20x slower                                        |
| mako            | 11.0 ms                                                | 15.5 ms: 1.41x slower                                        |
| Geometric mean  | (ref)                                                  | 1.23x slower                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250313-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-8ea82b5 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 538 ms: 2.06x faster                                         |
| gc_traversal               | 3.46 ms                                                | 1.74 ms: 1.99x faster                                        |
| async_tree_none_tg         | 446 ms                                                 | 230 ms: 1.94x faster                                         |
| async_tree_io              | 1.08 sec                                               | 573 ms: 1.89x faster                                         |
| async_tree_memoization_tg  | 560 ms                                                 | 298 ms: 1.88x faster                                         |
| async_tree_none            | 464 ms                                                 | 269 ms: 1.72x faster                                         |
| async_tree_memoization     | 555 ms                                                 | 330 ms: 1.68x faster                                         |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 563 ms: 1.28x faster                                         |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 595 ms: 1.20x faster                                         |
| deepcopy                   | 352 us                                                 | 300 us: 1.17x faster                                         |
| regex_effbot               | 3.17 ms                                                | 2.79 ms: 1.14x faster                                        |
| float                      | 80.8 ms                                                | 71.2 ms: 1.13x faster                                        |
| deepcopy_memo              | 40.3 us                                                | 35.7 us: 1.13x faster                                        |
| xml_etree_iterparse        | 96.7 ms                                                | 88.2 ms: 1.10x faster                                        |
| pathlib                    | 21.5 ms                                                | 19.8 ms: 1.09x faster                                        |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.08x faster                                         |
| go                         | 139 ms                                                 | 130 ms: 1.07x faster                                         |
| dulwich_log                | 78.9 ms                                                | 73.6 ms: 1.07x faster                                        |
| sqlite_synth               | 2.20 us                                                | 2.06 us: 1.07x faster                                        |
| logging_silent             | 109 ns                                                 | 104 ns: 1.05x faster                                         |
| async_generators           | 384 ms                                                 | 372 ms: 1.03x faster                                         |
| coroutines                 | 23.9 ms                                                | 23.5 ms: 1.02x faster                                        |
| scimark_sor                | 130 ms                                                 | 128 ms: 1.02x faster                                         |
| bpe_tokeniser              | 4.74 sec                                               | 4.70 sec: 1.01x faster                                       |
| spectral_norm              | 110 ms                                                 | 110 ms: 1.00x faster                                         |
| asyncio_websockets         | 517 ms                                                 | 519 ms: 1.00x slower                                         |
| raytrace                   | 299 ms                                                 | 302 ms: 1.01x slower                                         |
| comprehensions             | 19.8 us                                                | 20.3 us: 1.02x slower                                        |
| scimark_fft                | 342 ms                                                 | 357 ms: 1.04x slower                                         |
| docutils                   | 2.64 sec                                               | 2.78 sec: 1.05x slower                                       |
| chaos                      | 62.8 ms                                                | 66.3 ms: 1.06x slower                                        |
| deltablue                  | 3.45 ms                                                | 3.64 ms: 1.06x slower                                        |
| pyflate                    | 448 ms                                                 | 477 ms: 1.06x slower                                         |
| tomli_loads                | 2.11 sec                                               | 2.24 sec: 1.06x slower                                       |
| mdp                        | 2.42 sec                                               | 2.58 sec: 1.07x slower                                       |
| regex_compile              | 142 ms                                                 | 153 ms: 1.07x slower                                         |
| unpickle_pure_python       | 221 us                                                 | 238 us: 1.08x slower                                         |
| logging_simple             | 6.63 us                                                | 7.23 us: 1.09x slower                                        |
| pprint_safe_repr           | 743 ms                                                 | 811 ms: 1.09x slower                                         |
| regex_dna                  | 168 ms                                                 | 183 ms: 1.09x slower                                         |
| pprint_pformat             | 1.52 sec                                               | 1.66 sec: 1.09x slower                                       |
| json_loads                 | 26.5 us                                                | 29.1 us: 1.10x slower                                        |
| sqlglot_transpile          | 1.67 ms                                                | 1.83 ms: 1.10x slower                                        |
| thrift                     | 791 us                                                 | 869 us: 1.10x slower                                         |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.0 ms: 1.10x slower                                        |
| 2to3                       | 264 ms                                                 | 290 ms: 1.10x slower                                         |
| sqlalchemy_declarative     | 143 ms                                                 | 158 ms: 1.11x slower                                         |
| pickle_pure_python         | 308 us                                                 | 340 us: 1.11x slower                                         |
| html5lib                   | 63.6 ms                                                | 70.4 ms: 1.11x slower                                        |
| sqlglot_normalize          | 107 ms                                                 | 118 ms: 1.11x slower                                         |
| scimark_monte_carlo        | 68.4 ms                                                | 76.0 ms: 1.11x slower                                        |
| crypto_pyaes               | 76.6 ms                                                | 85.3 ms: 1.11x slower                                        |
| sqlglot_parse              | 1.36 ms                                                | 1.51 ms: 1.11x slower                                        |
| xml_etree_generate         | 85.2 ms                                                | 95.7 ms: 1.12x slower                                        |
| logging_format             | 7.35 us                                                | 8.26 us: 1.12x slower                                        |
| sympy_sum                  | 166 ms                                                 | 187 ms: 1.13x slower                                         |
| sqlglot_optimize           | 53.3 ms                                                | 60.0 ms: 1.13x slower                                        |
| sympy_str                  | 292 ms                                                 | 333 ms: 1.14x slower                                         |
| richards                   | 45.9 ms                                                | 53.3 ms: 1.16x slower                                        |
| sympy_integrate            | 20.5 ms                                                | 23.9 ms: 1.16x slower                                        |
| xml_etree_process          | 59.0 ms                                                | 68.7 ms: 1.17x slower                                        |
| sympy_expand               | 468 ms                                                 | 546 ms: 1.17x slower                                         |
| genshi_xml                 | 50.2 ms                                                | 58.6 ms: 1.17x slower                                        |
| regex_v8                   | 20.6 ms                                                | 24.2 ms: 1.17x slower                                        |
| genshi_text                | 22.8 ms                                                | 26.8 ms: 1.18x slower                                        |
| hexiom                     | 6.17 ms                                                | 7.27 ms: 1.18x slower                                        |
| typing_runtime_protocols   | 163 us                                                 | 193 us: 1.18x slower                                         |
| nqueens                    | 80.1 ms                                                | 94.6 ms: 1.18x slower                                        |
| richards_super             | 51.9 ms                                                | 61.4 ms: 1.18x slower                                        |
| scimark_lu                 | 114 ms                                                 | 135 ms: 1.18x slower                                         |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.25 ms: 1.19x slower                                        |
| django_template            | 34.7 ms                                                | 41.8 ms: 1.20x slower                                        |
| json_dumps                 | 10.4 ms                                                | 12.5 ms: 1.21x slower                                        |
| create_gc_cycles           | 1.09 ms                                                | 1.33 ms: 1.22x slower                                        |
| meteor_contest             | 104 ms                                                 | 127 ms: 1.22x slower                                         |
| pidigits                   | 184 ms                                                 | 226 ms: 1.23x slower                                         |
| fannkuch                   | 372 ms                                                 | 460 ms: 1.23x slower                                         |
| telco                      | 6.53 ms                                                | 8.59 ms: 1.32x slower                                        |
| nbody                      | 89.3 ms                                                | 118 ms: 1.33x slower                                         |
| coverage                   | 71.4 ms                                                | 96.2 ms: 1.35x slower                                        |
| mako                       | 11.0 ms                                                | 15.5 ms: 1.41x slower                                        |
| python_startup_no_site     | 7.16 ms                                                | 11.1 ms: 1.56x slower                                        |
| python_startup             | 9.93 ms                                                | 15.8 ms: 1.59x slower                                        |
| bench_thread_pool          | 941 us                                                 | 3.13 ms: 3.33x slower                                        |
| bench_mp_pool              | 10.8 ms                                                | 96.2 ms: 8.91x slower                                        |
| Geometric mean             | (ref)                                                  | 1.06x slower                                                 |

Benchmark hidden because not significant (5): pylint, generators, deepcopy_reduce, pycparser, json
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250313-3.14.0a5+-8ea82b5-NOGIL/bm-20250313-vultr-x86_64-mpage-measure_lfb-3.14.0a5+-8ea82b5.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.025x slower

# HPT report

- Reliability score: 99.79% likely to be slow
- 90% likely to have a slowdown of 1.04x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.36x