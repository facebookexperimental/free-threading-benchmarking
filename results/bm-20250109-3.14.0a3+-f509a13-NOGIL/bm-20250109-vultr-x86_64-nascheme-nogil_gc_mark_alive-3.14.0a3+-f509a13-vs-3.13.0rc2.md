# Results vs. 3.13.0rc2

- fork: nascheme
- ref: nogil_gc_mark_alive
- machine: linux-x86_64
- commit hash: f509a13
- commit date: 2025-01-09
- overall geometric mean: 1.184x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.14x slower
- Memory change: 1.32x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250109-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 341 ms: 1.31x slower                                                    |
| docutils       | 2.62 sec                                                     | 2.98 sec: 1.14x slower                                                  |
| html5lib       | 67.0 ms                                                      | 87.9 ms: 1.31x slower                                                   |
| Geometric mean | (ref)                                                        | 1.25x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250109-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13 |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 727 ms: 1.26x faster                                                    |
| async_tree_io              | 876 ms                                                       | 754 ms: 1.16x faster                                                    |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 567 ms: 1.12x faster                                                    |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 594 ms: 1.12x faster                                                    |
| async_tree_memoization     | 461 ms                                                       | 425 ms: 1.09x faster                                                    |
| async_tree_none_tg         | 336 ms                                                       | 313 ms: 1.07x faster                                                    |
| async_tree_memoization_tg  | 414 ms                                                       | 398 ms: 1.04x faster                                                    |
| coroutines                 | 23.6 ms                                                      | 23.1 ms: 1.02x faster                                                   |
| async_tree_none            | 354 ms                                                       | 349 ms: 1.01x faster                                                    |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                    |
| async_generators           | 377 ms                                                       | 446 ms: 1.18x slower                                                    |
| Geometric mean             | (ref)                                                        | 1.06x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250109-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 192 ms: 1.13x faster                                                    |
| float          | 77.5 ms                                                      | 106 ms: 1.37x slower                                                    |
| nbody          | 85.1 ms                                                      | 127 ms: 1.50x slower                                                    |
| Geometric mean | (ref)                                                        | 1.22x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250109-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.77 ms: 1.11x faster                                                   |
| regex_dna      | 180 ms                                                       | 176 ms: 1.03x faster                                                    |
| regex_v8       | 22.7 ms                                                      | 23.8 ms: 1.05x slower                                                   |
| regex_compile  | 132 ms                                                       | 166 ms: 1.25x slower                                                    |
| Geometric mean | (ref)                                                        | 1.04x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250109-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13 |
|----------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 88.7 ms: 1.07x faster                                                   |
| xml_etree_parse      | 136 ms                                                       | 129 ms: 1.06x faster                                                    |
| json_loads           | 27.0 us                                                      | 29.2 us: 1.08x slower                                                   |
| xml_etree_generate   | 85.4 ms                                                      | 97.1 ms: 1.14x slower                                                   |
| tomli_loads          | 2.01 sec                                                     | 2.36 sec: 1.18x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 73.1 ms: 1.23x slower                                                   |
| json_dumps           | 10.5 ms                                                      | 13.9 ms: 1.32x slower                                                   |
| unpickle_pure_python | 210 us                                                       | 323 us: 1.54x slower                                                    |
| pickle_pure_python   | 294 us                                                       | 492 us: 1.67x slower                                                    |
| Geometric mean       | (ref)                                                        | 1.20x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250109-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13 |
|------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.67 ms: 1.31x slower                                                   |
| python_startup         | 11.0 ms                                                      | 15.5 ms: 1.41x slower                                                   |
| Geometric mean         | (ref)                                                        | 1.36x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250109-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13 |
|-----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 62.5 ms: 1.28x slower                                                   |
| genshi_text     | 21.5 ms                                                      | 30.6 ms: 1.42x slower                                                   |
| django_template | 34.1 ms                                                      | 48.9 ms: 1.43x slower                                                   |
| mako            | 11.3 ms                                                      | 17.2 ms: 1.52x slower                                                   |
| Geometric mean  | (ref)                                                        | 1.41x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250109-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13 |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 727 ms: 1.26x faster                                                    |
| async_tree_io              | 876 ms                                                       | 754 ms: 1.16x faster                                                    |
| pidigits                   | 217 ms                                                       | 192 ms: 1.13x faster                                                    |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 567 ms: 1.12x faster                                                    |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 594 ms: 1.12x faster                                                    |
| regex_effbot               | 3.08 ms                                                      | 2.77 ms: 1.11x faster                                                   |
| deepcopy                   | 355 us                                                       | 325 us: 1.09x faster                                                    |
| async_tree_memoization     | 461 ms                                                       | 425 ms: 1.09x faster                                                    |
| async_tree_none_tg         | 336 ms                                                       | 313 ms: 1.07x faster                                                    |
| xml_etree_iterparse        | 94.9 ms                                                      | 88.7 ms: 1.07x faster                                                   |
| xml_etree_parse            | 136 ms                                                       | 129 ms: 1.06x faster                                                    |
| sqlite_synth               | 2.21 us                                                      | 2.10 us: 1.05x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 398 ms: 1.04x faster                                                    |
| regex_dna                  | 180 ms                                                       | 176 ms: 1.03x faster                                                    |
| coroutines                 | 23.6 ms                                                      | 23.1 ms: 1.02x faster                                                   |
| async_tree_none            | 354 ms                                                       | 349 ms: 1.01x faster                                                    |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                    |
| pathlib                    | 19.2 ms                                                      | 19.5 ms: 1.02x slower                                                   |
| spectral_norm              | 111 ms                                                       | 115 ms: 1.03x slower                                                    |
| deepcopy_memo              | 39.1 us                                                      | 40.7 us: 1.04x slower                                                   |
| regex_v8                   | 22.7 ms                                                      | 23.8 ms: 1.05x slower                                                   |
| gc_traversal               | 3.14 ms                                                      | 3.33 ms: 1.06x slower                                                   |
| pylint                     | 317 ms                                                       | 337 ms: 1.06x slower                                                    |
| json                       | 4.93 ms                                                      | 5.24 ms: 1.06x slower                                                   |
| create_gc_cycles           | 1.34 ms                                                      | 1.43 ms: 1.07x slower                                                   |
| json_loads                 | 27.0 us                                                      | 29.2 us: 1.08x slower                                                   |
| scimark_fft                | 349 ms                                                       | 383 ms: 1.10x slower                                                    |
| deepcopy_reduce            | 3.11 us                                                      | 3.43 us: 1.10x slower                                                   |
| telco                      | 7.82 ms                                                      | 8.65 ms: 1.11x slower                                                   |
| bpe_tokeniser              | 4.45 sec                                                     | 4.99 sec: 1.12x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 97.1 ms: 1.14x slower                                                   |
| docutils                   | 2.62 sec                                                     | 2.98 sec: 1.14x slower                                                  |
| tomli_loads                | 2.01 sec                                                     | 2.36 sec: 1.18x slower                                                  |
| async_generators           | 377 ms                                                       | 446 ms: 1.18x slower                                                    |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.59 ms: 1.19x slower                                                   |
| coverage                   | 83.0 ms                                                      | 98.8 ms: 1.19x slower                                                   |
| dulwich_log                | 74.8 ms                                                      | 89.8 ms: 1.20x slower                                                   |
| pycparser                  | 1.12 sec                                                     | 1.35 sec: 1.21x slower                                                  |
| mdp                        | 2.36 sec                                                     | 2.88 sec: 1.22x slower                                                  |
| xml_etree_process          | 59.3 ms                                                      | 73.1 ms: 1.23x slower                                                   |
| sqlglot_optimize           | 52.7 ms                                                      | 65.4 ms: 1.24x slower                                                   |
| sqlglot_normalize          | 106 ms                                                       | 132 ms: 1.25x slower                                                    |
| sympy_sum                  | 156 ms                                                       | 194 ms: 1.25x slower                                                    |
| nqueens                    | 78.6 ms                                                      | 98.0 ms: 1.25x slower                                                   |
| regex_compile              | 132 ms                                                       | 166 ms: 1.25x slower                                                    |
| sympy_integrate            | 19.8 ms                                                      | 24.9 ms: 1.25x slower                                                   |
| sympy_expand               | 457 ms                                                       | 578 ms: 1.26x slower                                                    |
| meteor_contest             | 102 ms                                                       | 129 ms: 1.27x slower                                                    |
| pprint_safe_repr           | 738 ms                                                       | 939 ms: 1.27x slower                                                    |
| genshi_xml                 | 48.8 ms                                                      | 62.5 ms: 1.28x slower                                                   |
| sympy_str                  | 275 ms                                                       | 352 ms: 1.28x slower                                                    |
| thrift                     | 778 us                                                       | 1.00 ms: 1.29x slower                                                   |
| pprint_pformat             | 1.50 sec                                                     | 1.96 sec: 1.31x slower                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 9.67 ms: 1.31x slower                                                   |
| fannkuch                   | 370 ms                                                       | 484 ms: 1.31x slower                                                    |
| typing_runtime_protocols   | 155 us                                                       | 203 us: 1.31x slower                                                    |
| html5lib                   | 67.0 ms                                                      | 87.9 ms: 1.31x slower                                                   |
| 2to3                       | 260 ms                                                       | 341 ms: 1.31x slower                                                    |
| crypto_pyaes               | 67.9 ms                                                      | 89.5 ms: 1.32x slower                                                   |
| json_dumps                 | 10.5 ms                                                      | 13.9 ms: 1.32x slower                                                   |
| generators                 | 28.8 ms                                                      | 38.5 ms: 1.34x slower                                                   |
| float                      | 77.5 ms                                                      | 106 ms: 1.37x slower                                                    |
| scimark_lu                 | 113 ms                                                       | 155 ms: 1.38x slower                                                    |
| python_startup             | 11.0 ms                                                      | 15.5 ms: 1.41x slower                                                   |
| pyflate                    | 449 ms                                                       | 635 ms: 1.42x slower                                                    |
| genshi_text                | 21.5 ms                                                      | 30.6 ms: 1.42x slower                                                   |
| django_template            | 34.1 ms                                                      | 48.9 ms: 1.43x slower                                                   |
| logging_format             | 6.84 us                                                      | 9.84 us: 1.44x slower                                                   |
| logging_simple             | 6.16 us                                                      | 8.90 us: 1.44x slower                                                   |
| richards                   | 45.2 ms                                                      | 66.0 ms: 1.46x slower                                                   |
| richards_super             | 51.6 ms                                                      | 77.0 ms: 1.49x slower                                                   |
| nbody                      | 85.1 ms                                                      | 127 ms: 1.50x slower                                                    |
| scimark_sor                | 134 ms                                                       | 202 ms: 1.50x slower                                                    |
| mako                       | 11.3 ms                                                      | 17.2 ms: 1.52x slower                                                   |
| hexiom                     | 5.99 ms                                                      | 9.18 ms: 1.53x slower                                                   |
| unpickle_pure_python       | 210 us                                                       | 323 us: 1.54x slower                                                    |
| scimark_monte_carlo        | 65.4 ms                                                      | 103 ms: 1.57x slower                                                    |
| chaos                      | 57.3 ms                                                      | 93.5 ms: 1.63x slower                                                   |
| go                         | 141 ms                                                       | 230 ms: 1.63x slower                                                    |
| comprehensions             | 16.5 us                                                      | 27.4 us: 1.66x slower                                                   |
| pickle_pure_python         | 294 us                                                       | 492 us: 1.67x slower                                                    |
| sqlglot_transpile          | 1.56 ms                                                      | 2.62 ms: 1.68x slower                                                   |
| logging_silent             | 103 ns                                                       | 183 ns: 1.79x slower                                                    |
| sqlglot_parse              | 1.25 ms                                                      | 2.24 ms: 1.79x slower                                                   |
| raytrace                   | 253 ms                                                       | 489 ms: 1.94x slower                                                    |
| deltablue                  | 3.12 ms                                                      | 7.31 ms: 2.34x slower                                                   |
| bench_thread_pool          | 919 us                                                       | 3.38 ms: 3.68x slower                                                   |
| bench_mp_pool              | 11.0 ms                                                      | 94.3 ms: 8.58x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.27x slower                                                            |
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250109-3.14.0a3+-f509a13-NOGIL/bm-20250109-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.184x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.18x
- 95% likely to have a slowdown of 1.17x
- 99% likely to have a slowdown of 1.14x

# Memory
- memory change: 1.32x