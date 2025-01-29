# Results vs. 3.13.0rc2

- fork: Yhg1s
- ref: load_const_defer
- machine: linux-x86_64
- commit hash: fcfb942
- commit date: 2025-01-29
- overall geometric mean: 1.109x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250129-vultr-x86_64-Yhg1s-load_const_defer-3.14.0a4+-fcfb942 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 311 ms: 1.20x slower                                              |
| docutils       | 2.62 sec                                                     | 2.84 sec: 1.09x slower                                            |
| html5lib       | 67.0 ms                                                      | 72.5 ms: 1.08x slower                                             |
| Geometric mean | (ref)                                                        | 1.12x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250129-vultr-x86_64-Yhg1s-load_const_defer-3.14.0a4+-fcfb942 |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 592 ms: 1.54x faster                                              |
| async_tree_io              | 876 ms                                                       | 617 ms: 1.42x faster                                              |
| async_tree_none_tg         | 336 ms                                                       | 258 ms: 1.30x faster                                              |
| async_tree_memoization     | 461 ms                                                       | 360 ms: 1.28x faster                                              |
| async_tree_memoization_tg  | 414 ms                                                       | 330 ms: 1.26x faster                                              |
| async_tree_none            | 354 ms                                                       | 295 ms: 1.20x faster                                              |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 629 ms: 1.06x faster                                              |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 604 ms: 1.06x faster                                              |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                              |
| async_generators           | 377 ms                                                       | 376 ms: 1.00x faster                                              |
| coroutines                 | 23.6 ms                                                      | 24.9 ms: 1.06x slower                                             |
| Geometric mean             | (ref)                                                        | 1.17x faster                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250129-vultr-x86_64-Yhg1s-load_const_defer-3.14.0a4+-fcfb942 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 78.1 ms: 1.01x slower                                             |
| pidigits       | 217 ms                                                       | 227 ms: 1.05x slower                                              |
| nbody          | 85.1 ms                                                      | 143 ms: 1.68x slower                                              |
| Geometric mean | (ref)                                                        | 1.21x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250129-vultr-x86_64-Yhg1s-load_const_defer-3.14.0a4+-fcfb942 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.84 ms: 1.09x faster                                             |
| regex_v8       | 22.7 ms                                                      | 23.5 ms: 1.03x slower                                             |
| regex_dna      | 180 ms                                                       | 188 ms: 1.04x slower                                              |
| regex_compile  | 132 ms                                                       | 156 ms: 1.18x slower                                              |
| Geometric mean | (ref)                                                        | 1.04x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250129-vultr-x86_64-Yhg1s-load_const_defer-3.14.0a4+-fcfb942 |
|----------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 89.0 ms: 1.07x faster                                             |
| xml_etree_parse      | 136 ms                                                       | 128 ms: 1.07x faster                                              |
| xml_etree_generate   | 85.4 ms                                                      | 97.5 ms: 1.14x slower                                             |
| json_loads           | 27.0 us                                                      | 30.9 us: 1.14x slower                                             |
| xml_etree_process    | 59.3 ms                                                      | 70.0 ms: 1.18x slower                                             |
| tomli_loads          | 2.01 sec                                                     | 2.41 sec: 1.20x slower                                            |
| unpickle_pure_python | 210 us                                                       | 258 us: 1.23x slower                                              |
| json_dumps           | 10.5 ms                                                      | 13.2 ms: 1.26x slower                                             |
| pickle_pure_python   | 294 us                                                       | 383 us: 1.30x slower                                              |
| Geometric mean       | (ref)                                                        | 1.14x slower                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250129-vultr-x86_64-Yhg1s-load_const_defer-3.14.0a4+-fcfb942 |
|------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.57 ms: 1.29x slower                                             |
| python_startup         | 11.0 ms                                                      | 15.2 ms: 1.39x slower                                             |
| Geometric mean         | (ref)                                                        | 1.34x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250129-vultr-x86_64-Yhg1s-load_const_defer-3.14.0a4+-fcfb942 |
|-----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 62.3 ms: 1.28x slower                                             |
| django_template | 34.1 ms                                                      | 43.7 ms: 1.28x slower                                             |
| genshi_text     | 21.5 ms                                                      | 28.7 ms: 1.33x slower                                             |
| mako            | 11.3 ms                                                      | 16.0 ms: 1.41x slower                                             |
| Geometric mean  | (ref)                                                        | 1.32x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250129-vultr-x86_64-Yhg1s-load_const_defer-3.14.0a4+-fcfb942 |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 592 ms: 1.54x faster                                              |
| async_tree_io              | 876 ms                                                       | 617 ms: 1.42x faster                                              |
| async_tree_none_tg         | 336 ms                                                       | 258 ms: 1.30x faster                                              |
| async_tree_memoization     | 461 ms                                                       | 360 ms: 1.28x faster                                              |
| async_tree_memoization_tg  | 414 ms                                                       | 330 ms: 1.26x faster                                              |
| async_tree_none            | 354 ms                                                       | 295 ms: 1.20x faster                                              |
| deepcopy                   | 355 us                                                       | 320 us: 1.11x faster                                              |
| regex_effbot               | 3.08 ms                                                      | 2.84 ms: 1.09x faster                                             |
| sqlite_synth               | 2.21 us                                                      | 2.05 us: 1.08x faster                                             |
| xml_etree_iterparse        | 94.9 ms                                                      | 89.0 ms: 1.07x faster                                             |
| xml_etree_parse            | 136 ms                                                       | 128 ms: 1.07x faster                                              |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 629 ms: 1.06x faster                                              |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 604 ms: 1.06x faster                                              |
| pathlib                    | 19.2 ms                                                      | 19.0 ms: 1.01x faster                                             |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                              |
| async_generators           | 377 ms                                                       | 376 ms: 1.00x faster                                              |
| float                      | 77.5 ms                                                      | 78.1 ms: 1.01x slower                                             |
| go                         | 141 ms                                                       | 143 ms: 1.02x slower                                              |
| spectral_norm              | 111 ms                                                       | 114 ms: 1.03x slower                                              |
| regex_v8                   | 22.7 ms                                                      | 23.5 ms: 1.03x slower                                             |
| scimark_sor                | 134 ms                                                       | 139 ms: 1.03x slower                                              |
| regex_dna                  | 180 ms                                                       | 188 ms: 1.04x slower                                              |
| pidigits                   | 217 ms                                                       | 227 ms: 1.05x slower                                              |
| bpe_tokeniser              | 4.45 sec                                                     | 4.66 sec: 1.05x slower                                            |
| coroutines                 | 23.6 ms                                                      | 24.9 ms: 1.06x slower                                             |
| deepcopy_reduce            | 3.11 us                                                      | 3.33 us: 1.07x slower                                             |
| gc_traversal               | 3.14 ms                                                      | 3.36 ms: 1.07x slower                                             |
| html5lib                   | 67.0 ms                                                      | 72.5 ms: 1.08x slower                                             |
| docutils                   | 2.62 sec                                                     | 2.84 sec: 1.09x slower                                            |
| pycparser                  | 1.12 sec                                                     | 1.21 sec: 1.09x slower                                            |
| json                       | 4.93 ms                                                      | 5.37 ms: 1.09x slower                                             |
| telco                      | 7.82 ms                                                      | 8.69 ms: 1.11x slower                                             |
| dulwich_log                | 74.8 ms                                                      | 83.6 ms: 1.12x slower                                             |
| pprint_safe_repr           | 738 ms                                                       | 830 ms: 1.13x slower                                              |
| pyflate                    | 449 ms                                                       | 507 ms: 1.13x slower                                              |
| mdp                        | 2.36 sec                                                     | 2.68 sec: 1.14x slower                                            |
| xml_etree_generate         | 85.4 ms                                                      | 97.5 ms: 1.14x slower                                             |
| scimark_fft                | 349 ms                                                       | 399 ms: 1.14x slower                                              |
| json_loads                 | 27.0 us                                                      | 30.9 us: 1.14x slower                                             |
| pprint_pformat             | 1.50 sec                                                     | 1.72 sec: 1.15x slower                                            |
| sqlglot_normalize          | 106 ms                                                       | 123 ms: 1.16x slower                                              |
| generators                 | 28.8 ms                                                      | 33.5 ms: 1.16x slower                                             |
| coverage                   | 83.0 ms                                                      | 97.7 ms: 1.18x slower                                             |
| xml_etree_process          | 59.3 ms                                                      | 70.0 ms: 1.18x slower                                             |
| regex_compile              | 132 ms                                                       | 156 ms: 1.18x slower                                              |
| sqlglot_optimize           | 52.7 ms                                                      | 62.5 ms: 1.19x slower                                             |
| 2to3                       | 260 ms                                                       | 311 ms: 1.20x slower                                              |
| logging_silent             | 103 ns                                                       | 123 ns: 1.20x slower                                              |
| thrift                     | 778 us                                                       | 935 us: 1.20x slower                                              |
| tomli_loads                | 2.01 sec                                                     | 2.41 sec: 1.20x slower                                            |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.67 ms: 1.20x slower                                             |
| sympy_sum                  | 156 ms                                                       | 190 ms: 1.22x slower                                              |
| comprehensions             | 16.5 us                                                      | 20.1 us: 1.22x slower                                             |
| logging_simple             | 6.16 us                                                      | 7.57 us: 1.23x slower                                             |
| unpickle_pure_python       | 210 us                                                       | 258 us: 1.23x slower                                              |
| sympy_expand               | 457 ms                                                       | 562 ms: 1.23x slower                                              |
| chaos                      | 57.3 ms                                                      | 71.2 ms: 1.24x slower                                             |
| sympy_integrate            | 19.8 ms                                                      | 24.6 ms: 1.24x slower                                             |
| nqueens                    | 78.6 ms                                                      | 97.6 ms: 1.24x slower                                             |
| sympy_str                  | 275 ms                                                       | 341 ms: 1.24x slower                                              |
| scimark_lu                 | 113 ms                                                       | 140 ms: 1.25x slower                                              |
| json_dumps                 | 10.5 ms                                                      | 13.2 ms: 1.26x slower                                             |
| logging_format             | 6.84 us                                                      | 8.63 us: 1.26x slower                                             |
| sqlglot_transpile          | 1.56 ms                                                      | 1.97 ms: 1.27x slower                                             |
| hexiom                     | 5.99 ms                                                      | 7.59 ms: 1.27x slower                                             |
| meteor_contest             | 102 ms                                                       | 130 ms: 1.28x slower                                              |
| genshi_xml                 | 48.8 ms                                                      | 62.3 ms: 1.28x slower                                             |
| django_template            | 34.1 ms                                                      | 43.7 ms: 1.28x slower                                             |
| python_startup_no_site     | 7.39 ms                                                      | 9.57 ms: 1.29x slower                                             |
| richards                   | 45.2 ms                                                      | 58.6 ms: 1.30x slower                                             |
| scimark_monte_carlo        | 65.4 ms                                                      | 84.9 ms: 1.30x slower                                             |
| pickle_pure_python         | 294 us                                                       | 383 us: 1.30x slower                                              |
| typing_runtime_protocols   | 155 us                                                       | 202 us: 1.30x slower                                              |
| crypto_pyaes               | 67.9 ms                                                      | 88.9 ms: 1.31x slower                                             |
| sqlglot_parse              | 1.25 ms                                                      | 1.64 ms: 1.31x slower                                             |
| fannkuch                   | 370 ms                                                       | 488 ms: 1.32x slower                                              |
| genshi_text                | 21.5 ms                                                      | 28.7 ms: 1.33x slower                                             |
| richards_super             | 51.6 ms                                                      | 69.0 ms: 1.34x slower                                             |
| raytrace                   | 253 ms                                                       | 342 ms: 1.35x slower                                              |
| python_startup             | 11.0 ms                                                      | 15.2 ms: 1.39x slower                                             |
| mako                       | 11.3 ms                                                      | 16.0 ms: 1.41x slower                                             |
| deltablue                  | 3.12 ms                                                      | 4.79 ms: 1.53x slower                                             |
| nbody                      | 85.1 ms                                                      | 143 ms: 1.68x slower                                              |
| bench_thread_pool          | 919 us                                                       | 3.33 ms: 3.62x slower                                             |
| bench_mp_pool              | 11.0 ms                                                      | 94.9 ms: 8.64x slower                                             |
| Geometric mean             | (ref)                                                        | 1.16x slower                                                      |

Benchmark hidden because not significant (3): deepcopy_memo, create_gc_cycles, pylint
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250129-3.14.0a4+-fcfb942-NOGIL/bm-20250129-vultr-x86_64-Yhg1s-load_const_defer-3.14.0a4+-fcfb942.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.109x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 1.34x