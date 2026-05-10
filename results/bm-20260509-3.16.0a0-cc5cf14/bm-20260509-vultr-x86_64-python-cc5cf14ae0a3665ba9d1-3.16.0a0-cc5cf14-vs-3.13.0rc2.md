# Results vs. 3.13.0rc2

- fork: python
- ref: cc5cf14ae0a3665ba9d1
- machine: linux-x86_64
- commit hash: cc5cf14
- commit date: 2026-05-09
- overall geometric mean: 1.023x faster
- HPT reliability: 99.91%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| docutils       | 2.62 sec                                                     | 2.41 sec: 1.09x faster                                                |
| html5lib       | 67.0 ms                                                      | 61.1 ms: 1.10x faster                                                 |
| Geometric mean | (ref)                                                        | 1.09x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 666 ms                                                       | 543 ms: 1.23x faster                                                  |
| async_tree_io              | 876 ms                                                       | 716 ms: 1.22x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 379 ms: 1.22x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 754 ms: 1.21x faster                                                  |
| async_tree_none            | 354 ms                                                       | 295 ms: 1.20x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 552 ms: 1.15x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 364 ms: 1.14x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 297 ms: 1.13x faster                                                  |
| asyncio_tcp                | 505 ms                                                       | 450 ms: 1.12x faster                                                  |
| async_generators           | 377 ms                                                       | 341 ms: 1.11x faster                                                  |
| asyncio_tcp_ssl            | 1.51 sec                                                     | 1.46 sec: 1.03x faster                                                |
| asyncio_websockets         | 520 ms                                                       | 543 ms: 1.04x slower                                                  |
| coroutines                 | 23.6 ms                                                      | 24.9 ms: 1.06x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.12x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 184 ms: 1.18x faster                                                  |
| float          | 77.5 ms                                                      | 75.2 ms: 1.03x faster                                                 |
| nbody          | 85.1 ms                                                      | 90.1 ms: 1.06x slower                                                 |
| Geometric mean | (ref)                                                        | 1.05x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 132 ms                                                       | 125 ms: 1.06x faster                                                  |
| regex_effbot   | 3.08 ms                                                      | 2.95 ms: 1.05x faster                                                 |
| regex_v8       | 22.7 ms                                                      | 21.7 ms: 1.04x faster                                                 |
| regex_dna      | 180 ms                                                       | 184 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                        | 1.03x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                     | 1.84 sec: 1.09x faster                                                |
| json_dumps           | 10.5 ms                                                      | 9.75 ms: 1.08x faster                                                 |
| xml_etree_iterparse  | 94.9 ms                                                      | 90.9 ms: 1.04x faster                                                 |
| json_loads           | 27.0 us                                                      | 27.4 us: 1.02x slower                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 86.9 ms: 1.02x slower                                                 |
| unpickle_pure_python | 210 us                                                       | 216 us: 1.03x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 61.2 ms: 1.03x slower                                                 |
| xml_etree_parse      | 136 ms                                                       | 142 ms: 1.05x slower                                                  |
| pickle_list          | 4.93 us                                                      | 5.18 us: 1.05x slower                                                 |
| pickle_dict          | 32.5 us                                                      | 34.3 us: 1.05x slower                                                 |
| unpickle             | 14.3 us                                                      | 15.2 us: 1.06x slower                                                 |
| unpickle_list        | 4.71 us                                                      | 5.06 us: 1.07x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 319 us: 1.08x slower                                                  |
| pickle               | 11.3 us                                                      | 13.1 us: 1.15x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.03x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.1 ms                                                      | 36.2 ms: 1.06x slower                                                 |
| mako            | 11.3 ms                                                      | 12.0 ms: 1.06x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.06x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 317 ms                                                       | 114 ms: 2.78x faster                                                  |
| mdp                        | 2.36 sec                                                     | 1.14 sec: 2.06x faster                                                |
| deepcopy                   | 355 us                                                       | 237 us: 1.50x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 27.7 us: 1.41x faster                                                 |
| go                         | 141 ms                                                       | 108 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 543 ms: 1.23x faster                                                  |
| async_tree_io              | 876 ms                                                       | 716 ms: 1.22x faster                                                  |
| scimark_sor                | 134 ms                                                       | 110 ms: 1.22x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 379 ms: 1.22x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.57 us: 1.21x faster                                                 |
| async_tree_io_tg           | 913 ms                                                       | 754 ms: 1.21x faster                                                  |
| async_tree_none            | 354 ms                                                       | 295 ms: 1.20x faster                                                  |
| pidigits                   | 217 ms                                                       | 184 ms: 1.18x faster                                                  |
| spectral_norm              | 111 ms                                                       | 94.6 ms: 1.17x faster                                                 |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 552 ms: 1.15x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 364 ms: 1.14x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 297 ms: 1.13x faster                                                  |
| pyflate                    | 449 ms                                                       | 399 ms: 1.12x faster                                                  |
| asyncio_tcp                | 505 ms                                                       | 450 ms: 1.12x faster                                                  |
| scimark_fft                | 349 ms                                                       | 316 ms: 1.11x faster                                                  |
| async_generators           | 377 ms                                                       | 341 ms: 1.11x faster                                                  |
| html5lib                   | 67.0 ms                                                      | 61.1 ms: 1.10x faster                                                 |
| pathlib                    | 19.2 ms                                                      | 17.6 ms: 1.09x faster                                                 |
| tomli_loads                | 2.01 sec                                                     | 1.84 sec: 1.09x faster                                                |
| dulwich_log                | 74.8 ms                                                      | 68.7 ms: 1.09x faster                                                 |
| docutils                   | 2.62 sec                                                     | 2.41 sec: 1.09x faster                                                |
| json_dumps                 | 10.5 ms                                                      | 9.75 ms: 1.08x faster                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.18 sec: 1.06x faster                                                |
| regex_compile              | 132 ms                                                       | 125 ms: 1.06x faster                                                  |
| logging_simple             | 6.16 us                                                      | 5.84 us: 1.05x faster                                                 |
| nqueens                    | 78.6 ms                                                      | 74.9 ms: 1.05x faster                                                 |
| regex_effbot               | 3.08 ms                                                      | 2.95 ms: 1.05x faster                                                 |
| generators                 | 28.8 ms                                                      | 27.5 ms: 1.05x faster                                                 |
| richards_super             | 51.6 ms                                                      | 49.4 ms: 1.05x faster                                                 |
| xml_etree_iterparse        | 94.9 ms                                                      | 90.9 ms: 1.04x faster                                                 |
| regex_v8                   | 22.7 ms                                                      | 21.7 ms: 1.04x faster                                                 |
| unpack_sequence            | 44.8 ns                                                      | 43.2 ns: 1.04x faster                                                 |
| richards                   | 45.2 ms                                                      | 43.7 ms: 1.04x faster                                                 |
| asyncio_tcp_ssl            | 1.51 sec                                                     | 1.46 sec: 1.03x faster                                                |
| float                      | 77.5 ms                                                      | 75.2 ms: 1.03x faster                                                 |
| sympy_integrate            | 19.8 ms                                                      | 19.2 ms: 1.03x faster                                                 |
| chaos                      | 57.3 ms                                                      | 55.6 ms: 1.03x faster                                                 |
| logging_format             | 6.84 us                                                      | 6.67 us: 1.03x faster                                                 |
| comprehensions             | 16.5 us                                                      | 16.0 us: 1.03x faster                                                 |
| hexiom                     | 5.99 ms                                                      | 5.89 ms: 1.02x faster                                                 |
| logging_silent             | 103 ns                                                       | 101 ns: 1.02x faster                                                  |
| meteor_contest             | 102 ms                                                       | 100 ms: 1.01x faster                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 64.8 ms: 1.01x faster                                                 |
| pprint_safe_repr           | 738 ms                                                       | 734 ms: 1.01x faster                                                  |
| sympy_str                  | 275 ms                                                       | 276 ms: 1.01x slower                                                  |
| sympy_sum                  | 156 ms                                                       | 157 ms: 1.01x slower                                                  |
| json_loads                 | 27.0 us                                                      | 27.4 us: 1.02x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 86.9 ms: 1.02x slower                                                 |
| json                       | 4.93 ms                                                      | 5.03 ms: 1.02x slower                                                 |
| regex_dna                  | 180 ms                                                       | 184 ms: 1.02x slower                                                  |
| raytrace                   | 253 ms                                                       | 259 ms: 1.02x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 69.6 ms: 1.03x slower                                                 |
| unpickle_pure_python       | 210 us                                                       | 216 us: 1.03x slower                                                  |
| fannkuch                   | 370 ms                                                       | 381 ms: 1.03x slower                                                  |
| xml_etree_process          | 59.3 ms                                                      | 61.2 ms: 1.03x slower                                                 |
| sympy_expand               | 457 ms                                                       | 472 ms: 1.03x slower                                                  |
| asyncio_websockets         | 520 ms                                                       | 543 ms: 1.04x slower                                                  |
| xml_etree_parse            | 136 ms                                                       | 142 ms: 1.05x slower                                                  |
| pickle_list                | 4.93 us                                                      | 5.18 us: 1.05x slower                                                 |
| typing_runtime_protocols   | 155 us                                                       | 163 us: 1.05x slower                                                  |
| pycparser                  | 1.12 sec                                                     | 1.18 sec: 1.05x slower                                                |
| pickle_dict                | 32.5 us                                                      | 34.3 us: 1.05x slower                                                 |
| coroutines                 | 23.6 ms                                                      | 24.9 ms: 1.06x slower                                                 |
| nbody                      | 85.1 ms                                                      | 90.1 ms: 1.06x slower                                                 |
| unpickle                   | 14.3 us                                                      | 15.2 us: 1.06x slower                                                 |
| django_template            | 34.1 ms                                                      | 36.2 ms: 1.06x slower                                                 |
| mako                       | 11.3 ms                                                      | 12.0 ms: 1.06x slower                                                 |
| unpickle_list              | 4.71 us                                                      | 5.06 us: 1.07x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 319 us: 1.08x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 3.39 ms: 1.09x slower                                                 |
| pickle                     | 11.3 us                                                      | 13.1 us: 1.15x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 4.19 ms: 1.33x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.82 ms: 1.36x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 1.34 ms: 1.46x slower                                                 |
| telco                      | 7.82 ms                                                      | 162 ms: 20.74x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 299 ms: 27.16x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.02x slower                                                          |

Benchmark hidden because not significant (6): sqlite_synth, scimark_sparse_mat_mult, pprint_pformat, coverage, scimark_lu, thrift
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: 2to3, aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, python_startup, python_startup_no_site, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20260509-3.16.0a0-cc5cf14/bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.023x faster

# HPT report

- Reliability score: 99.91% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.16x