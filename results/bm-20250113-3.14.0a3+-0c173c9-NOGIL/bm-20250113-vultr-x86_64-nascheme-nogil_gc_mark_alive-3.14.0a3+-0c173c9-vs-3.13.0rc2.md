# Results vs. 3.13.0rc2

- fork: nascheme
- ref: nogil_gc_mark_alive
- machine: linux-x86_64
- commit hash: 0c173c9
- commit date: 2025-01-13
- overall geometric mean: 1.187x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.14x slower
- Memory change: 1.32x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250113-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-0c173c9 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 341 ms: 1.31x slower                                                    |
| docutils       | 2.62 sec                                                     | 2.98 sec: 1.14x slower                                                  |
| html5lib       | 67.0 ms                                                      | 88.8 ms: 1.33x slower                                                   |
| Geometric mean | (ref)                                                        | 1.26x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250113-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-0c173c9 |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 731 ms: 1.25x faster                                                    |
| async_tree_io              | 876 ms                                                       | 761 ms: 1.15x faster                                                    |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 567 ms: 1.13x faster                                                    |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 599 ms: 1.11x faster                                                    |
| async_tree_none_tg         | 336 ms                                                       | 312 ms: 1.08x faster                                                    |
| async_tree_memoization     | 461 ms                                                       | 431 ms: 1.07x faster                                                    |
| async_tree_memoization_tg  | 414 ms                                                       | 398 ms: 1.04x faster                                                    |
| asyncio_websockets         | 520 ms                                                       | 518 ms: 1.00x faster                                                    |
| coroutines                 | 23.6 ms                                                      | 23.7 ms: 1.01x slower                                                   |
| async_generators           | 377 ms                                                       | 448 ms: 1.19x slower                                                    |
| Geometric mean             | (ref)                                                        | 1.06x faster                                                            |

Benchmark hidden because not significant (1): async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250113-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-0c173c9 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 201 ms: 1.08x faster                                                    |
| float          | 77.5 ms                                                      | 106 ms: 1.37x slower                                                    |
| nbody          | 85.1 ms                                                      | 131 ms: 1.54x slower                                                    |
| Geometric mean | (ref)                                                        | 1.25x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250113-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-0c173c9 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.75 ms: 1.12x faster                                                   |
| regex_dna      | 180 ms                                                       | 188 ms: 1.04x slower                                                    |
| regex_v8       | 22.7 ms                                                      | 24.4 ms: 1.08x slower                                                   |
| regex_compile  | 132 ms                                                       | 165 ms: 1.25x slower                                                    |
| Geometric mean | (ref)                                                        | 1.06x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250113-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-0c173c9 |
|----------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 88.9 ms: 1.07x faster                                                   |
| xml_etree_parse      | 136 ms                                                       | 128 ms: 1.06x faster                                                    |
| json_loads           | 27.0 us                                                      | 29.2 us: 1.08x slower                                                   |
| xml_etree_generate   | 85.4 ms                                                      | 97.1 ms: 1.14x slower                                                   |
| tomli_loads          | 2.01 sec                                                     | 2.37 sec: 1.18x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 73.3 ms: 1.23x slower                                                   |
| json_dumps           | 10.5 ms                                                      | 13.7 ms: 1.30x slower                                                   |
| unpickle_pure_python | 210 us                                                       | 321 us: 1.53x slower                                                    |
| pickle_pure_python   | 294 us                                                       | 487 us: 1.65x slower                                                    |
| Geometric mean       | (ref)                                                        | 1.20x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250113-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-0c173c9 |
|------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.59 ms: 1.30x slower                                                   |
| python_startup         | 11.0 ms                                                      | 15.4 ms: 1.40x slower                                                   |
| Geometric mean         | (ref)                                                        | 1.35x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250113-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-0c173c9 |
|-----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 63.0 ms: 1.29x slower                                                   |
| genshi_text     | 21.5 ms                                                      | 30.4 ms: 1.41x slower                                                   |
| django_template | 34.1 ms                                                      | 49.9 ms: 1.46x slower                                                   |
| mako            | 11.3 ms                                                      | 17.0 ms: 1.50x slower                                                   |
| Geometric mean  | (ref)                                                        | 1.41x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250113-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-0c173c9 |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 731 ms: 1.25x faster                                                    |
| async_tree_io              | 876 ms                                                       | 761 ms: 1.15x faster                                                    |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 567 ms: 1.13x faster                                                    |
| regex_effbot               | 3.08 ms                                                      | 2.75 ms: 1.12x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 599 ms: 1.11x faster                                                    |
| deepcopy                   | 355 us                                                       | 325 us: 1.09x faster                                                    |
| async_tree_none_tg         | 336 ms                                                       | 312 ms: 1.08x faster                                                    |
| pidigits                   | 217 ms                                                       | 201 ms: 1.08x faster                                                    |
| async_tree_memoization     | 461 ms                                                       | 431 ms: 1.07x faster                                                    |
| xml_etree_iterparse        | 94.9 ms                                                      | 88.9 ms: 1.07x faster                                                   |
| xml_etree_parse            | 136 ms                                                       | 128 ms: 1.06x faster                                                    |
| async_tree_memoization_tg  | 414 ms                                                       | 398 ms: 1.04x faster                                                    |
| sqlite_synth               | 2.21 us                                                      | 2.12 us: 1.04x faster                                                   |
| spectral_norm              | 111 ms                                                       | 110 ms: 1.01x faster                                                    |
| asyncio_websockets         | 520 ms                                                       | 518 ms: 1.00x faster                                                    |
| coroutines                 | 23.6 ms                                                      | 23.7 ms: 1.01x slower                                                   |
| create_gc_cycles           | 1.34 ms                                                      | 1.36 ms: 1.02x slower                                                   |
| deepcopy_memo              | 39.1 us                                                      | 40.2 us: 1.03x slower                                                   |
| pathlib                    | 19.2 ms                                                      | 19.8 ms: 1.03x slower                                                   |
| regex_dna                  | 180 ms                                                       | 188 ms: 1.04x slower                                                    |
| json                       | 4.93 ms                                                      | 5.20 ms: 1.06x slower                                                   |
| pylint                     | 317 ms                                                       | 335 ms: 1.06x slower                                                    |
| regex_v8                   | 22.7 ms                                                      | 24.4 ms: 1.08x slower                                                   |
| json_loads                 | 27.0 us                                                      | 29.2 us: 1.08x slower                                                   |
| scimark_fft                | 349 ms                                                       | 384 ms: 1.10x slower                                                    |
| deepcopy_reduce            | 3.11 us                                                      | 3.43 us: 1.10x slower                                                   |
| telco                      | 7.82 ms                                                      | 8.68 ms: 1.11x slower                                                   |
| bpe_tokeniser              | 4.45 sec                                                     | 4.94 sec: 1.11x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 97.1 ms: 1.14x slower                                                   |
| docutils                   | 2.62 sec                                                     | 2.98 sec: 1.14x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 3.65 ms: 1.16x slower                                                   |
| mdp                        | 2.36 sec                                                     | 2.78 sec: 1.18x slower                                                  |
| tomli_loads                | 2.01 sec                                                     | 2.37 sec: 1.18x slower                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.57 ms: 1.18x slower                                                   |
| async_generators           | 377 ms                                                       | 448 ms: 1.19x slower                                                    |
| coverage                   | 83.0 ms                                                      | 99.0 ms: 1.19x slower                                                   |
| dulwich_log                | 74.8 ms                                                      | 89.6 ms: 1.20x slower                                                   |
| pycparser                  | 1.12 sec                                                     | 1.35 sec: 1.21x slower                                                  |
| xml_etree_process          | 59.3 ms                                                      | 73.3 ms: 1.23x slower                                                   |
| nqueens                    | 78.6 ms                                                      | 97.4 ms: 1.24x slower                                                   |
| sympy_sum                  | 156 ms                                                       | 194 ms: 1.25x slower                                                    |
| regex_compile              | 132 ms                                                       | 165 ms: 1.25x slower                                                    |
| sqlglot_normalize          | 106 ms                                                       | 133 ms: 1.25x slower                                                    |
| sqlglot_optimize           | 52.7 ms                                                      | 66.3 ms: 1.26x slower                                                   |
| sympy_integrate            | 19.8 ms                                                      | 25.2 ms: 1.27x slower                                                   |
| sympy_expand               | 457 ms                                                       | 584 ms: 1.28x slower                                                    |
| pprint_safe_repr           | 738 ms                                                       | 946 ms: 1.28x slower                                                    |
| thrift                     | 778 us                                                       | 1.00 ms: 1.29x slower                                                   |
| genshi_xml                 | 48.8 ms                                                      | 63.0 ms: 1.29x slower                                                   |
| meteor_contest             | 102 ms                                                       | 131 ms: 1.29x slower                                                    |
| sympy_str                  | 275 ms                                                       | 356 ms: 1.29x slower                                                    |
| python_startup_no_site     | 7.39 ms                                                      | 9.59 ms: 1.30x slower                                                   |
| json_dumps                 | 10.5 ms                                                      | 13.7 ms: 1.30x slower                                                   |
| pprint_pformat             | 1.50 sec                                                     | 1.96 sec: 1.31x slower                                                  |
| fannkuch                   | 370 ms                                                       | 485 ms: 1.31x slower                                                    |
| typing_runtime_protocols   | 155 us                                                       | 203 us: 1.31x slower                                                    |
| 2to3                       | 260 ms                                                       | 341 ms: 1.31x slower                                                    |
| html5lib                   | 67.0 ms                                                      | 88.8 ms: 1.33x slower                                                   |
| crypto_pyaes               | 67.9 ms                                                      | 90.2 ms: 1.33x slower                                                   |
| generators                 | 28.8 ms                                                      | 38.4 ms: 1.33x slower                                                   |
| float                      | 77.5 ms                                                      | 106 ms: 1.37x slower                                                    |
| scimark_lu                 | 113 ms                                                       | 156 ms: 1.39x slower                                                    |
| python_startup             | 11.0 ms                                                      | 15.4 ms: 1.40x slower                                                   |
| genshi_text                | 21.5 ms                                                      | 30.4 ms: 1.41x slower                                                   |
| richards                   | 45.2 ms                                                      | 65.0 ms: 1.44x slower                                                   |
| pyflate                    | 449 ms                                                       | 646 ms: 1.44x slower                                                    |
| logging_simple             | 6.16 us                                                      | 8.98 us: 1.46x slower                                                   |
| django_template            | 34.1 ms                                                      | 49.9 ms: 1.46x slower                                                   |
| logging_format             | 6.84 us                                                      | 10.1 us: 1.47x slower                                                   |
| richards_super             | 51.6 ms                                                      | 76.0 ms: 1.47x slower                                                   |
| mako                       | 11.3 ms                                                      | 17.0 ms: 1.50x slower                                                   |
| scimark_sor                | 134 ms                                                       | 203 ms: 1.51x slower                                                    |
| unpickle_pure_python       | 210 us                                                       | 321 us: 1.53x slower                                                    |
| nbody                      | 85.1 ms                                                      | 131 ms: 1.54x slower                                                    |
| hexiom                     | 5.99 ms                                                      | 9.24 ms: 1.54x slower                                                   |
| scimark_monte_carlo        | 65.4 ms                                                      | 102 ms: 1.56x slower                                                    |
| comprehensions             | 16.5 us                                                      | 26.7 us: 1.62x slower                                                   |
| go                         | 141 ms                                                       | 229 ms: 1.63x slower                                                    |
| pickle_pure_python         | 294 us                                                       | 487 us: 1.65x slower                                                    |
| chaos                      | 57.3 ms                                                      | 94.7 ms: 1.65x slower                                                   |
| sqlglot_transpile          | 1.56 ms                                                      | 2.63 ms: 1.69x slower                                                   |
| logging_silent             | 103 ns                                                       | 177 ns: 1.72x slower                                                    |
| sqlglot_parse              | 1.25 ms                                                      | 2.28 ms: 1.83x slower                                                   |
| raytrace                   | 253 ms                                                       | 489 ms: 1.93x slower                                                    |
| deltablue                  | 3.12 ms                                                      | 7.17 ms: 2.29x slower                                                   |
| bench_thread_pool          | 919 us                                                       | 3.37 ms: 3.67x slower                                                   |
| bench_mp_pool              | 11.0 ms                                                      | 97.3 ms: 8.85x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.28x slower                                                            |

Benchmark hidden because not significant (1): async_tree_none
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250113-3.14.0a3+-0c173c9-NOGIL/bm-20250113-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-0c173c9.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.187x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.18x
- 95% likely to have a slowdown of 1.17x
- 99% likely to have a slowdown of 1.14x

# Memory
- memory change: 1.32x