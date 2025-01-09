# Results vs. 3.13.0rc2

- fork: nascheme
- ref: nogil_gc_mark_alive
- machine: linux-x86_64
- commit hash: a111bff
- commit date: 2025-01-08
- overall geometric mean: 1.188x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.14x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250108-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 342 ms: 1.32x slower                                                    |
| docutils       | 2.62 sec                                                     | 3.00 sec: 1.15x slower                                                  |
| html5lib       | 67.0 ms                                                      | 89.1 ms: 1.33x slower                                                   |
| Geometric mean | (ref)                                                        | 1.26x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250108-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 734 ms: 1.24x faster                                                    |
| async_tree_io              | 876 ms                                                       | 762 ms: 1.15x faster                                                    |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 568 ms: 1.12x faster                                                    |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 597 ms: 1.12x faster                                                    |
| async_tree_memoization     | 461 ms                                                       | 429 ms: 1.08x faster                                                    |
| async_tree_none_tg         | 336 ms                                                       | 319 ms: 1.05x faster                                                    |
| async_tree_memoization_tg  | 414 ms                                                       | 402 ms: 1.03x faster                                                    |
| coroutines                 | 23.6 ms                                                      | 23.3 ms: 1.01x faster                                                   |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                    |
| async_generators           | 377 ms                                                       | 446 ms: 1.18x slower                                                    |
| Geometric mean             | (ref)                                                        | 1.06x faster                                                            |

Benchmark hidden because not significant (1): async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250108-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 198 ms: 1.10x faster                                                    |
| float          | 77.5 ms                                                      | 106 ms: 1.37x slower                                                    |
| nbody          | 85.1 ms                                                      | 131 ms: 1.54x slower                                                    |
| Geometric mean | (ref)                                                        | 1.24x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250108-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.83 ms: 1.09x faster                                                   |
| regex_dna      | 180 ms                                                       | 185 ms: 1.03x slower                                                    |
| regex_v8       | 22.7 ms                                                      | 24.6 ms: 1.08x slower                                                   |
| regex_compile  | 132 ms                                                       | 167 ms: 1.26x slower                                                    |
| Geometric mean | (ref)                                                        | 1.07x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250108-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff |
|----------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 89.7 ms: 1.06x faster                                                   |
| xml_etree_parse      | 136 ms                                                       | 129 ms: 1.06x faster                                                    |
| json_loads           | 27.0 us                                                      | 29.0 us: 1.07x slower                                                   |
| xml_etree_generate   | 85.4 ms                                                      | 98.8 ms: 1.16x slower                                                   |
| tomli_loads          | 2.01 sec                                                     | 2.35 sec: 1.17x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 73.1 ms: 1.23x slower                                                   |
| json_dumps           | 10.5 ms                                                      | 14.1 ms: 1.33x slower                                                   |
| unpickle_pure_python | 210 us                                                       | 323 us: 1.54x slower                                                    |
| pickle_pure_python   | 294 us                                                       | 491 us: 1.67x slower                                                    |
| Geometric mean       | (ref)                                                        | 1.21x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250108-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff |
|------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.72 ms: 1.31x slower                                                   |
| python_startup         | 11.0 ms                                                      | 15.5 ms: 1.41x slower                                                   |
| Geometric mean         | (ref)                                                        | 1.36x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250108-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff |
|-----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 63.0 ms: 1.29x slower                                                   |
| django_template | 34.1 ms                                                      | 48.5 ms: 1.42x slower                                                   |
| genshi_text     | 21.5 ms                                                      | 30.7 ms: 1.42x slower                                                   |
| mako            | 11.3 ms                                                      | 17.0 ms: 1.50x slower                                                   |
| Geometric mean  | (ref)                                                        | 1.41x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250108-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 734 ms: 1.24x faster                                                    |
| async_tree_io              | 876 ms                                                       | 762 ms: 1.15x faster                                                    |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 568 ms: 1.12x faster                                                    |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 597 ms: 1.12x faster                                                    |
| pidigits                   | 217 ms                                                       | 198 ms: 1.10x faster                                                    |
| deepcopy                   | 355 us                                                       | 325 us: 1.09x faster                                                    |
| regex_effbot               | 3.08 ms                                                      | 2.83 ms: 1.09x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 429 ms: 1.08x faster                                                    |
| xml_etree_iterparse        | 94.9 ms                                                      | 89.7 ms: 1.06x faster                                                   |
| xml_etree_parse            | 136 ms                                                       | 129 ms: 1.06x faster                                                    |
| sqlite_synth               | 2.21 us                                                      | 2.10 us: 1.05x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 319 ms: 1.05x faster                                                    |
| async_tree_memoization_tg  | 414 ms                                                       | 402 ms: 1.03x faster                                                    |
| spectral_norm              | 111 ms                                                       | 108 ms: 1.02x faster                                                    |
| coroutines                 | 23.6 ms                                                      | 23.3 ms: 1.01x faster                                                   |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                    |
| regex_dna                  | 180 ms                                                       | 185 ms: 1.03x slower                                                    |
| pathlib                    | 19.2 ms                                                      | 19.8 ms: 1.03x slower                                                   |
| deepcopy_memo              | 39.1 us                                                      | 40.7 us: 1.04x slower                                                   |
| json                       | 4.93 ms                                                      | 5.19 ms: 1.05x slower                                                   |
| pylint                     | 317 ms                                                       | 336 ms: 1.06x slower                                                    |
| create_gc_cycles           | 1.34 ms                                                      | 1.43 ms: 1.07x slower                                                   |
| json_loads                 | 27.0 us                                                      | 29.0 us: 1.07x slower                                                   |
| scimark_fft                | 349 ms                                                       | 378 ms: 1.08x slower                                                    |
| regex_v8                   | 22.7 ms                                                      | 24.6 ms: 1.08x slower                                                   |
| deepcopy_reduce            | 3.11 us                                                      | 3.41 us: 1.09x slower                                                   |
| telco                      | 7.82 ms                                                      | 8.68 ms: 1.11x slower                                                   |
| bpe_tokeniser              | 4.45 sec                                                     | 4.95 sec: 1.11x slower                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.36 ms: 1.14x slower                                                   |
| docutils                   | 2.62 sec                                                     | 3.00 sec: 1.15x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 98.8 ms: 1.16x slower                                                   |
| gc_traversal               | 3.14 ms                                                      | 3.67 ms: 1.17x slower                                                   |
| tomli_loads                | 2.01 sec                                                     | 2.35 sec: 1.17x slower                                                  |
| coverage                   | 83.0 ms                                                      | 97.2 ms: 1.17x slower                                                   |
| async_generators           | 377 ms                                                       | 446 ms: 1.18x slower                                                    |
| mdp                        | 2.36 sec                                                     | 2.79 sec: 1.18x slower                                                  |
| dulwich_log                | 74.8 ms                                                      | 89.7 ms: 1.20x slower                                                   |
| pycparser                  | 1.12 sec                                                     | 1.34 sec: 1.20x slower                                                  |
| nqueens                    | 78.6 ms                                                      | 96.1 ms: 1.22x slower                                                   |
| xml_etree_process          | 59.3 ms                                                      | 73.1 ms: 1.23x slower                                                   |
| sqlglot_optimize           | 52.7 ms                                                      | 65.5 ms: 1.24x slower                                                   |
| sqlglot_normalize          | 106 ms                                                       | 132 ms: 1.24x slower                                                    |
| sympy_sum                  | 156 ms                                                       | 194 ms: 1.25x slower                                                    |
| sympy_integrate            | 19.8 ms                                                      | 24.9 ms: 1.26x slower                                                   |
| regex_compile              | 132 ms                                                       | 167 ms: 1.26x slower                                                    |
| sympy_expand               | 457 ms                                                       | 579 ms: 1.27x slower                                                    |
| thrift                     | 778 us                                                       | 988 us: 1.27x slower                                                    |
| meteor_contest             | 102 ms                                                       | 130 ms: 1.28x slower                                                    |
| sympy_str                  | 275 ms                                                       | 351 ms: 1.28x slower                                                    |
| genshi_xml                 | 48.8 ms                                                      | 63.0 ms: 1.29x slower                                                   |
| fannkuch                   | 370 ms                                                       | 479 ms: 1.30x slower                                                    |
| typing_runtime_protocols   | 155 us                                                       | 201 us: 1.30x slower                                                    |
| pprint_safe_repr           | 738 ms                                                       | 969 ms: 1.31x slower                                                    |
| python_startup_no_site     | 7.39 ms                                                      | 9.72 ms: 1.31x slower                                                   |
| 2to3                       | 260 ms                                                       | 342 ms: 1.32x slower                                                    |
| crypto_pyaes               | 67.9 ms                                                      | 89.8 ms: 1.32x slower                                                   |
| html5lib                   | 67.0 ms                                                      | 89.1 ms: 1.33x slower                                                   |
| json_dumps                 | 10.5 ms                                                      | 14.1 ms: 1.33x slower                                                   |
| pprint_pformat             | 1.50 sec                                                     | 2.01 sec: 1.34x slower                                                  |
| generators                 | 28.8 ms                                                      | 39.4 ms: 1.37x slower                                                   |
| float                      | 77.5 ms                                                      | 106 ms: 1.37x slower                                                    |
| scimark_lu                 | 113 ms                                                       | 156 ms: 1.38x slower                                                    |
| pyflate                    | 449 ms                                                       | 627 ms: 1.40x slower                                                    |
| python_startup             | 11.0 ms                                                      | 15.5 ms: 1.41x slower                                                   |
| django_template            | 34.1 ms                                                      | 48.5 ms: 1.42x slower                                                   |
| genshi_text                | 21.5 ms                                                      | 30.7 ms: 1.42x slower                                                   |
| logging_simple             | 6.16 us                                                      | 8.81 us: 1.43x slower                                                   |
| logging_format             | 6.84 us                                                      | 10.1 us: 1.47x slower                                                   |
| richards                   | 45.2 ms                                                      | 66.6 ms: 1.47x slower                                                   |
| mako                       | 11.3 ms                                                      | 17.0 ms: 1.50x slower                                                   |
| richards_super             | 51.6 ms                                                      | 77.7 ms: 1.50x slower                                                   |
| scimark_sor                | 134 ms                                                       | 202 ms: 1.50x slower                                                    |
| nbody                      | 85.1 ms                                                      | 131 ms: 1.54x slower                                                    |
| unpickle_pure_python       | 210 us                                                       | 323 us: 1.54x slower                                                    |
| hexiom                     | 5.99 ms                                                      | 9.36 ms: 1.56x slower                                                   |
| scimark_monte_carlo        | 65.4 ms                                                      | 104 ms: 1.58x slower                                                    |
| comprehensions             | 16.5 us                                                      | 27.1 us: 1.65x slower                                                   |
| chaos                      | 57.3 ms                                                      | 94.9 ms: 1.66x slower                                                   |
| pickle_pure_python         | 294 us                                                       | 491 us: 1.67x slower                                                    |
| go                         | 141 ms                                                       | 236 ms: 1.68x slower                                                    |
| sqlglot_transpile          | 1.56 ms                                                      | 2.65 ms: 1.70x slower                                                   |
| logging_silent             | 103 ns                                                       | 180 ns: 1.76x slower                                                    |
| sqlglot_parse              | 1.25 ms                                                      | 2.26 ms: 1.81x slower                                                   |
| raytrace                   | 253 ms                                                       | 494 ms: 1.96x slower                                                    |
| deltablue                  | 3.12 ms                                                      | 7.25 ms: 2.32x slower                                                   |
| bench_thread_pool          | 919 us                                                       | 3.36 ms: 3.66x slower                                                   |
| bench_mp_pool              | 11.0 ms                                                      | 94.2 ms: 8.57x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.28x slower                                                            |

Benchmark hidden because not significant (1): async_tree_none
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250108-3.14.0a3+-a111bff-NOGIL/bm-20250108-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.188x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.17x
- 95% likely to have a slowdown of 1.16x
- 99% likely to have a slowdown of 1.14x

# Memory
- memory change: 1.33x