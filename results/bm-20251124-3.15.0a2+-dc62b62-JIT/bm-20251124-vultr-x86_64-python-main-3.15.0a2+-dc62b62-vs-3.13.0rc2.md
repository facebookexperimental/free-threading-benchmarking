# Results vs. 3.13.0rc2

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: dc62b62
- commit date: 2025-11-24
- overall geometric mean: 1.064x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251124-vultr-x86_64-python-main-3.15.0a2+-dc62b62 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 249 ms: 1.04x faster                                   |
| docutils       | 2.62 sec                                                     | 2.75 sec: 1.05x slower                                 |
| html5lib       | 67.0 ms                                                      | 67.6 ms: 1.01x slower                                  |
| Geometric mean | (ref)                                                        | 1.01x slower                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251124-vultr-x86_64-python-main-3.15.0a2+-dc62b62 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------:|
| async_tree_io              | 876 ms                                                       | 563 ms: 1.56x faster                                   |
| async_tree_io_tg           | 913 ms                                                       | 595 ms: 1.53x faster                                   |
| async_tree_memoization     | 461 ms                                                       | 311 ms: 1.48x faster                                   |
| async_tree_none            | 354 ms                                                       | 248 ms: 1.43x faster                                   |
| async_tree_none_tg         | 336 ms                                                       | 246 ms: 1.36x faster                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 490 ms: 1.36x faster                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 310 ms: 1.34x faster                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 489 ms: 1.30x faster                                   |
| async_generators           | 377 ms                                                       | 360 ms: 1.05x faster                                   |
| coroutines                 | 23.6 ms                                                      | 24.3 ms: 1.03x slower                                  |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                   |
| Geometric mean             | (ref)                                                        | 1.29x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251124-vultr-x86_64-python-main-3.15.0a2+-dc62b62 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------:|
| float          | 77.5 ms                                                      | 59.9 ms: 1.29x faster                                  |
| pidigits       | 217 ms                                                       | 195 ms: 1.11x faster                                   |
| nbody          | 85.1 ms                                                      | 88.0 ms: 1.03x slower                                  |
| Geometric mean | (ref)                                                        | 1.11x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251124-vultr-x86_64-python-main-3.15.0a2+-dc62b62 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.67 ms: 1.15x faster                                  |
| regex_compile  | 132 ms                                                       | 125 ms: 1.05x faster                                   |
| regex_dna      | 180 ms                                                       | 176 ms: 1.03x faster                                   |
| Geometric mean | (ref)                                                        | 1.06x faster                                           |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251124-vultr-x86_64-python-main-3.15.0a2+-dc62b62 |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------:|
| json_dumps           | 10.5 ms                                                      | 9.06 ms: 1.16x faster                                  |
| xml_etree_iterparse  | 94.9 ms                                                      | 82.0 ms: 1.16x faster                                  |
| unpickle_pure_python | 210 us                                                       | 183 us: 1.15x faster                                   |
| xml_etree_process    | 59.3 ms                                                      | 53.6 ms: 1.11x faster                                  |
| xml_etree_generate   | 85.4 ms                                                      | 77.4 ms: 1.10x faster                                  |
| tomli_loads          | 2.01 sec                                                     | 1.82 sec: 1.10x faster                                 |
| xml_etree_parse      | 136 ms                                                       | 128 ms: 1.06x faster                                   |
| json_loads           | 27.0 us                                                      | 28.8 us: 1.07x slower                                  |
| Geometric mean       | (ref)                                                        | 1.08x faster                                           |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251124-vultr-x86_64-python-main-3.15.0a2+-dc62b62 |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.23 ms: 1.02x faster                                  |
| python_startup         | 11.0 ms                                                      | 12.4 ms: 1.13x slower                                  |
| Geometric mean         | (ref)                                                        | 1.05x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251124-vultr-x86_64-python-main-3.15.0a2+-dc62b62 |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------:|
| mako            | 11.3 ms                                                      | 10.4 ms: 1.09x faster                                  |
| django_template | 34.1 ms                                                      | 35.1 ms: 1.03x slower                                  |
| genshi_xml      | 48.8 ms                                                      | 56.1 ms: 1.15x slower                                  |
| Geometric mean  | (ref)                                                        | 1.02x slower                                           |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251124-vultr-x86_64-python-main-3.15.0a2+-dc62b62 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------:|
| richards                   | 45.2 ms                                                      | 20.9 ms: 2.16x faster                                  |
| richards_super             | 51.6 ms                                                      | 25.6 ms: 2.02x faster                                  |
| mdp                        | 2.36 sec                                                     | 1.33 sec: 1.78x faster                                 |
| deepcopy_memo              | 39.1 us                                                      | 25.0 us: 1.57x faster                                  |
| async_tree_io              | 876 ms                                                       | 563 ms: 1.56x faster                                   |
| async_tree_io_tg           | 913 ms                                                       | 595 ms: 1.53x faster                                   |
| async_tree_memoization     | 461 ms                                                       | 311 ms: 1.48x faster                                   |
| deepcopy                   | 355 us                                                       | 247 us: 1.44x faster                                   |
| async_tree_none            | 354 ms                                                       | 248 ms: 1.43x faster                                   |
| async_tree_none_tg         | 336 ms                                                       | 246 ms: 1.36x faster                                   |
| scimark_sor                | 134 ms                                                       | 98.6 ms: 1.36x faster                                  |
| scimark_fft                | 349 ms                                                       | 257 ms: 1.36x faster                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 490 ms: 1.36x faster                                   |
| go                         | 141 ms                                                       | 104 ms: 1.36x faster                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 310 ms: 1.34x faster                                   |
| spectral_norm              | 111 ms                                                       | 84.5 ms: 1.31x faster                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 489 ms: 1.30x faster                                   |
| float                      | 77.5 ms                                                      | 59.9 ms: 1.29x faster                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.54 us: 1.23x faster                                  |
| logging_silent             | 103 ns                                                       | 85.3 ns: 1.20x faster                                  |
| pyflate                    | 449 ms                                                       | 380 ms: 1.18x faster                                   |
| scimark_monte_carlo        | 65.4 ms                                                      | 55.8 ms: 1.17x faster                                  |
| json_dumps                 | 10.5 ms                                                      | 9.06 ms: 1.16x faster                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 82.0 ms: 1.16x faster                                  |
| regex_effbot               | 3.08 ms                                                      | 2.67 ms: 1.15x faster                                  |
| unpickle_pure_python       | 210 us                                                       | 183 us: 1.15x faster                                   |
| bpe_tokeniser              | 4.45 sec                                                     | 3.96 sec: 1.12x faster                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.23 ms: 1.11x faster                                  |
| scimark_lu                 | 113 ms                                                       | 101 ms: 1.11x faster                                   |
| pidigits                   | 217 ms                                                       | 195 ms: 1.11x faster                                   |
| xml_etree_process          | 59.3 ms                                                      | 53.6 ms: 1.11x faster                                  |
| xml_etree_generate         | 85.4 ms                                                      | 77.4 ms: 1.10x faster                                  |
| tomli_loads                | 2.01 sec                                                     | 1.82 sec: 1.10x faster                                 |
| pathlib                    | 19.2 ms                                                      | 17.6 ms: 1.09x faster                                  |
| deltablue                  | 3.12 ms                                                      | 2.87 ms: 1.09x faster                                  |
| mako                       | 11.3 ms                                                      | 10.4 ms: 1.09x faster                                  |
| pprint_safe_repr           | 738 ms                                                       | 682 ms: 1.08x faster                                   |
| logging_simple             | 6.16 us                                                      | 5.77 us: 1.07x faster                                  |
| xml_etree_parse            | 136 ms                                                       | 128 ms: 1.06x faster                                   |
| logging_format             | 6.84 us                                                      | 6.48 us: 1.06x faster                                  |
| regex_compile              | 132 ms                                                       | 125 ms: 1.05x faster                                   |
| thrift                     | 778 us                                                       | 739 us: 1.05x faster                                   |
| chaos                      | 57.3 ms                                                      | 54.5 ms: 1.05x faster                                  |
| async_generators           | 377 ms                                                       | 360 ms: 1.05x faster                                   |
| meteor_contest             | 102 ms                                                       | 97.0 ms: 1.05x faster                                  |
| comprehensions             | 16.5 us                                                      | 15.7 us: 1.05x faster                                  |
| 2to3                       | 260 ms                                                       | 249 ms: 1.04x faster                                   |
| pprint_pformat             | 1.50 sec                                                     | 1.45 sec: 1.03x faster                                 |
| regex_dna                  | 180 ms                                                       | 176 ms: 1.03x faster                                   |
| python_startup_no_site     | 7.39 ms                                                      | 7.23 ms: 1.02x faster                                  |
| coverage                   | 83.0 ms                                                      | 81.4 ms: 1.02x faster                                  |
| crypto_pyaes               | 67.9 ms                                                      | 67.1 ms: 1.01x faster                                  |
| dulwich_log                | 74.8 ms                                                      | 73.9 ms: 1.01x faster                                  |
| html5lib                   | 67.0 ms                                                      | 67.6 ms: 1.01x slower                                  |
| generators                 | 28.8 ms                                                      | 29.1 ms: 1.01x slower                                  |
| hexiom                     | 5.99 ms                                                      | 6.09 ms: 1.02x slower                                  |
| json                       | 4.93 ms                                                      | 5.02 ms: 1.02x slower                                  |
| typing_runtime_protocols   | 155 us                                                       | 158 us: 1.02x slower                                   |
| django_template            | 34.1 ms                                                      | 35.1 ms: 1.03x slower                                  |
| coroutines                 | 23.6 ms                                                      | 24.3 ms: 1.03x slower                                  |
| nbody                      | 85.1 ms                                                      | 88.0 ms: 1.03x slower                                  |
| raytrace                   | 253 ms                                                       | 264 ms: 1.05x slower                                   |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                   |
| docutils                   | 2.62 sec                                                     | 2.75 sec: 1.05x slower                                 |
| sympy_integrate            | 19.8 ms                                                      | 21.2 ms: 1.07x slower                                  |
| json_loads                 | 27.0 us                                                      | 28.8 us: 1.07x slower                                  |
| nqueens                    | 78.6 ms                                                      | 85.7 ms: 1.09x slower                                  |
| sympy_expand               | 457 ms                                                       | 506 ms: 1.11x slower                                   |
| sympy_sum                  | 156 ms                                                       | 175 ms: 1.12x slower                                   |
| python_startup             | 11.0 ms                                                      | 12.4 ms: 1.13x slower                                  |
| sympy_str                  | 275 ms                                                       | 313 ms: 1.14x slower                                   |
| genshi_xml                 | 48.8 ms                                                      | 56.1 ms: 1.15x slower                                  |
| bench_mp_pool              | 11.0 ms                                                      | 13.0 ms: 1.18x slower                                  |
| bench_thread_pool          | 919 us                                                       | 1.10 ms: 1.19x slower                                  |
| gc_traversal               | 3.14 ms                                                      | 4.27 ms: 1.36x slower                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.90 ms: 1.42x slower                                  |
| telco                      | 7.82 ms                                                      | 160 ms: 20.44x slower                                  |
| Geometric mean             | (ref)                                                        | 1.06x faster                                           |

Benchmark hidden because not significant (7): pylint, regex_v8, pickle_pure_python, fannkuch, pycparser, sqlite_synth, genshi_text
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (7) of results/bm-20251124-3.15.0a2+-dc62b62-JIT/bm-20251124-vultr-x86_64-python-main-3.15.0a2+-dc62b62.json: many_optionals, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.064x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.18x