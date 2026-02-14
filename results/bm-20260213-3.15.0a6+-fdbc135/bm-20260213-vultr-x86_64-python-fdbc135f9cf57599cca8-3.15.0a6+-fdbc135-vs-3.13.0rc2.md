# Results vs. 3.13.0rc2

- fork: python
- ref: fdbc135f9cf57599cca8
- machine: linux-x86_64
- commit hash: fdbc135
- commit date: 2026-02-13
- overall geometric mean: 1.043x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260213-vultr-x86_64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 249 ms: 1.04x faster                                                   |
| docutils       | 2.62 sec                                                     | 2.55 sec: 1.03x faster                                                 |
| html5lib       | 67.0 ms                                                      | 58.9 ms: 1.14x faster                                                  |
| Geometric mean | (ref)                                                        | 1.07x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260213-vultr-x86_64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 558 ms: 1.64x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 300 ms: 1.54x faster                                                   |
| async_tree_io              | 876 ms                                                       | 580 ms: 1.51x faster                                                   |
| async_tree_none            | 354 ms                                                       | 247 ms: 1.43x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 294 ms: 1.41x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 486 ms: 1.37x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 248 ms: 1.36x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 494 ms: 1.29x faster                                                   |
| async_generators           | 377 ms                                                       | 340 ms: 1.11x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 23.3 ms: 1.01x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.31x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260213-vultr-x86_64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 193 ms: 1.12x faster                                                   |
| float          | 77.5 ms                                                      | 69.6 ms: 1.11x faster                                                  |
| nbody          | 85.1 ms                                                      | 88.2 ms: 1.04x slower                                                  |
| Geometric mean | (ref)                                                        | 1.06x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260213-vultr-x86_64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 132 ms                                                       | 121 ms: 1.09x faster                                                   |
| regex_effbot   | 3.08 ms                                                      | 2.92 ms: 1.05x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 23.1 ms: 1.02x slower                                                  |
| regex_dna      | 180 ms                                                       | 185 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                        | 1.03x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260213-vultr-x86_64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 84.5 ms: 1.12x faster                                                  |
| tomli_loads          | 2.01 sec                                                     | 1.86 sec: 1.08x faster                                                 |
| json_dumps           | 10.5 ms                                                      | 9.88 ms: 1.07x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 130 ms: 1.05x faster                                                   |
| xml_etree_generate   | 85.4 ms                                                      | 84.7 ms: 1.01x faster                                                  |
| xml_etree_process    | 59.3 ms                                                      | 58.9 ms: 1.01x faster                                                  |
| unpickle_pure_python | 210 us                                                       | 209 us: 1.00x faster                                                   |
| pickle_pure_python   | 294 us                                                       | 309 us: 1.05x slower                                                   |
| json_loads           | 27.0 us                                                      | 28.6 us: 1.06x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.02x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260213-vultr-x86_64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.34 ms: 1.01x faster                                                  |
| python_startup         | 11.0 ms                                                      | 12.5 ms: 1.14x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.06x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260213-vultr-x86_64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 20.9 ms: 1.03x faster                                                  |
| genshi_xml      | 48.8 ms                                                      | 49.5 ms: 1.02x slower                                                  |
| mako            | 11.3 ms                                                      | 11.6 ms: 1.02x slower                                                  |
| django_template | 34.1 ms                                                      | 34.8 ms: 1.02x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.01x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260213-vultr-x86_64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.14 sec: 2.07x faster                                                 |
| async_tree_io_tg           | 913 ms                                                       | 558 ms: 1.64x faster                                                   |
| deepcopy                   | 355 us                                                       | 230 us: 1.54x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 300 ms: 1.54x faster                                                   |
| async_tree_io              | 876 ms                                                       | 580 ms: 1.51x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 26.2 us: 1.49x faster                                                  |
| async_tree_none            | 354 ms                                                       | 247 ms: 1.43x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 294 ms: 1.41x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 486 ms: 1.37x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 248 ms: 1.36x faster                                                   |
| go                         | 141 ms                                                       | 104 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 494 ms: 1.29x faster                                                   |
| scimark_sor                | 134 ms                                                       | 107 ms: 1.26x faster                                                   |
| deepcopy_reduce            | 3.11 us                                                      | 2.52 us: 1.23x faster                                                  |
| spectral_norm              | 111 ms                                                       | 94.5 ms: 1.18x faster                                                  |
| scimark_fft                | 349 ms                                                       | 304 ms: 1.15x faster                                                   |
| html5lib                   | 67.0 ms                                                      | 58.9 ms: 1.14x faster                                                  |
| pylint                     | 317 ms                                                       | 282 ms: 1.12x faster                                                   |
| xml_etree_iterparse        | 94.9 ms                                                      | 84.5 ms: 1.12x faster                                                  |
| pidigits                   | 217 ms                                                       | 193 ms: 1.12x faster                                                   |
| float                      | 77.5 ms                                                      | 69.6 ms: 1.11x faster                                                  |
| async_generators           | 377 ms                                                       | 340 ms: 1.11x faster                                                   |
| dulwich_log                | 74.8 ms                                                      | 67.8 ms: 1.10x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 17.4 ms: 1.10x faster                                                  |
| regex_compile              | 132 ms                                                       | 121 ms: 1.09x faster                                                   |
| pyflate                    | 449 ms                                                       | 412 ms: 1.09x faster                                                   |
| richards                   | 45.2 ms                                                      | 41.8 ms: 1.08x faster                                                  |
| richards_super             | 51.6 ms                                                      | 47.8 ms: 1.08x faster                                                  |
| tomli_loads                | 2.01 sec                                                     | 1.86 sec: 1.08x faster                                                 |
| logging_silent             | 103 ns                                                       | 96.0 ns: 1.07x faster                                                  |
| pprint_safe_repr           | 738 ms                                                       | 691 ms: 1.07x faster                                                   |
| hexiom                     | 5.99 ms                                                      | 5.62 ms: 1.07x faster                                                  |
| json_dumps                 | 10.5 ms                                                      | 9.88 ms: 1.07x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.17 sec: 1.07x faster                                                 |
| pprint_pformat             | 1.50 sec                                                     | 1.41 sec: 1.06x faster                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.44 ms: 1.06x faster                                                  |
| scimark_lu                 | 113 ms                                                       | 107 ms: 1.06x faster                                                   |
| regex_effbot               | 3.08 ms                                                      | 2.92 ms: 1.05x faster                                                  |
| logging_simple             | 6.16 us                                                      | 5.86 us: 1.05x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 130 ms: 1.05x faster                                                   |
| scimark_monte_carlo        | 65.4 ms                                                      | 62.4 ms: 1.05x faster                                                  |
| 2to3                       | 260 ms                                                       | 249 ms: 1.04x faster                                                   |
| chaos                      | 57.3 ms                                                      | 55.1 ms: 1.04x faster                                                  |
| logging_format             | 6.84 us                                                      | 6.58 us: 1.04x faster                                                  |
| sympy_integrate            | 19.8 ms                                                      | 19.1 ms: 1.04x faster                                                  |
| generators                 | 28.8 ms                                                      | 27.9 ms: 1.03x faster                                                  |
| genshi_text                | 21.5 ms                                                      | 20.9 ms: 1.03x faster                                                  |
| docutils                   | 2.62 sec                                                     | 2.55 sec: 1.03x faster                                                 |
| comprehensions             | 16.5 us                                                      | 16.1 us: 1.02x faster                                                  |
| pycparser                  | 1.12 sec                                                     | 1.09 sec: 1.02x faster                                                 |
| coverage                   | 83.0 ms                                                      | 81.4 ms: 1.02x faster                                                  |
| thrift                     | 778 us                                                       | 770 us: 1.01x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 23.3 ms: 1.01x faster                                                  |
| meteor_contest             | 102 ms                                                       | 101 ms: 1.01x faster                                                   |
| xml_etree_generate         | 85.4 ms                                                      | 84.7 ms: 1.01x faster                                                  |
| raytrace                   | 253 ms                                                       | 251 ms: 1.01x faster                                                   |
| python_startup_no_site     | 7.39 ms                                                      | 7.34 ms: 1.01x faster                                                  |
| xml_etree_process          | 59.3 ms                                                      | 58.9 ms: 1.01x faster                                                  |
| unpickle_pure_python       | 210 us                                                       | 209 us: 1.00x faster                                                   |
| crypto_pyaes               | 67.9 ms                                                      | 68.2 ms: 1.00x slower                                                  |
| nqueens                    | 78.6 ms                                                      | 79.1 ms: 1.01x slower                                                  |
| sympy_sum                  | 156 ms                                                       | 157 ms: 1.01x slower                                                   |
| typing_runtime_protocols   | 155 us                                                       | 157 us: 1.01x slower                                                   |
| genshi_xml                 | 48.8 ms                                                      | 49.5 ms: 1.02x slower                                                  |
| regex_v8                   | 22.7 ms                                                      | 23.1 ms: 1.02x slower                                                  |
| mako                       | 11.3 ms                                                      | 11.6 ms: 1.02x slower                                                  |
| django_template            | 34.1 ms                                                      | 34.8 ms: 1.02x slower                                                  |
| regex_dna                  | 180 ms                                                       | 185 ms: 1.02x slower                                                   |
| nbody                      | 85.1 ms                                                      | 88.2 ms: 1.04x slower                                                  |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                   |
| pickle_pure_python         | 294 us                                                       | 309 us: 1.05x slower                                                   |
| fannkuch                   | 370 ms                                                       | 388 ms: 1.05x slower                                                   |
| deltablue                  | 3.12 ms                                                      | 3.29 ms: 1.05x slower                                                  |
| sympy_expand               | 457 ms                                                       | 482 ms: 1.06x slower                                                   |
| json                       | 4.93 ms                                                      | 5.20 ms: 1.06x slower                                                  |
| json_loads                 | 27.0 us                                                      | 28.6 us: 1.06x slower                                                  |
| python_startup             | 11.0 ms                                                      | 12.5 ms: 1.14x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 4.25 ms: 1.35x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.84 ms: 1.38x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.31 ms: 1.42x slower                                                  |
| telco                      | 7.82 ms                                                      | 157 ms: 20.04x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 285 ms: 25.88x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.00x slower                                                           |

Benchmark hidden because not significant (2): sympy_str, sqlite_synth
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260213-3.15.0a6+-fdbc135/bm-20260213-vultr-x86_64-python-fdbc135f9cf57599cca8-3.15.0a6+-fdbc135.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.043x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.16x