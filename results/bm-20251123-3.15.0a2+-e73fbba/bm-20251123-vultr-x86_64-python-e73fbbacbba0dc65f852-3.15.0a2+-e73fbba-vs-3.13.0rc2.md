# Results vs. 3.13.0rc2

- fork: python
- ref: e73fbbacbba0dc65f852
- machine: linux-x86_64
- commit hash: e73fbba
- commit date: 2025-11-23
- overall geometric mean: 1.037x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 247 ms: 1.05x faster                                                   |
| docutils       | 2.62 sec                                                     | 2.55 sec: 1.03x faster                                                 |
| html5lib       | 67.0 ms                                                      | 61.5 ms: 1.09x faster                                                  |
| Geometric mean | (ref)                                                        | 1.06x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 876 ms                                                       | 555 ms: 1.58x faster                                                   |
| async_tree_io_tg           | 913 ms                                                       | 593 ms: 1.54x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 308 ms: 1.50x faster                                                   |
| async_tree_none            | 354 ms                                                       | 246 ms: 1.44x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 245 ms: 1.37x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 305 ms: 1.36x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 531 ms: 1.26x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 527 ms: 1.21x faster                                                   |
| async_generators           | 377 ms                                                       | 338 ms: 1.11x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 23.9 ms: 1.02x slower                                                  |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.28x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 70.0 ms: 1.11x faster                                                  |
| pidigits       | 217 ms                                                       | 220 ms: 1.02x slower                                                   |
| nbody          | 85.1 ms                                                      | 88.1 ms: 1.03x slower                                                  |
| Geometric mean | (ref)                                                        | 1.02x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.88 ms: 1.07x faster                                                  |
| regex_compile  | 132 ms                                                       | 124 ms: 1.07x faster                                                   |
| regex_dna      | 180 ms                                                       | 188 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                        | 1.02x faster                                                           |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_dumps           | 10.5 ms                                                      | 9.28 ms: 1.14x faster                                                  |
| xml_etree_iterparse  | 94.9 ms                                                      | 85.5 ms: 1.11x faster                                                  |
| tomli_loads          | 2.01 sec                                                     | 1.90 sec: 1.06x faster                                                 |
| xml_etree_parse      | 136 ms                                                       | 131 ms: 1.04x faster                                                   |
| xml_etree_generate   | 85.4 ms                                                      | 83.0 ms: 1.03x faster                                                  |
| xml_etree_process    | 59.3 ms                                                      | 58.2 ms: 1.02x faster                                                  |
| unpickle_pure_python | 210 us                                                       | 210 us: 1.00x faster                                                   |
| pickle_pure_python   | 294 us                                                       | 305 us: 1.04x slower                                                   |
| json_loads           | 27.0 us                                                      | 28.4 us: 1.05x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.03x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.26 ms: 1.02x faster                                                  |
| python_startup         | 11.0 ms                                                      | 12.4 ms: 1.13x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.05x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 20.7 ms: 1.04x faster                                                  |
| genshi_xml      | 48.8 ms                                                      | 48.5 ms: 1.01x faster                                                  |
| django_template | 34.1 ms                                                      | 34.3 ms: 1.00x slower                                                  |
| mako            | 11.3 ms                                                      | 11.4 ms: 1.00x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.01x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.15 sec: 2.05x faster                                                 |
| async_tree_io              | 876 ms                                                       | 555 ms: 1.58x faster                                                   |
| async_tree_io_tg           | 913 ms                                                       | 593 ms: 1.54x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 308 ms: 1.50x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 26.6 us: 1.47x faster                                                  |
| deepcopy                   | 355 us                                                       | 244 us: 1.45x faster                                                   |
| async_tree_none            | 354 ms                                                       | 246 ms: 1.44x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 245 ms: 1.37x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 305 ms: 1.36x faster                                                   |
| go                         | 141 ms                                                       | 104 ms: 1.35x faster                                                   |
| scimark_sor                | 134 ms                                                       | 107 ms: 1.26x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 531 ms: 1.26x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 527 ms: 1.21x faster                                                   |
| deepcopy_reduce            | 3.11 us                                                      | 2.63 us: 1.18x faster                                                  |
| spectral_norm              | 111 ms                                                       | 93.9 ms: 1.18x faster                                                  |
| scimark_fft                | 349 ms                                                       | 307 ms: 1.14x faster                                                   |
| json_dumps                 | 10.5 ms                                                      | 9.28 ms: 1.14x faster                                                  |
| async_generators           | 377 ms                                                       | 338 ms: 1.11x faster                                                   |
| xml_etree_iterparse        | 94.9 ms                                                      | 85.5 ms: 1.11x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 17.3 ms: 1.11x faster                                                  |
| float                      | 77.5 ms                                                      | 70.0 ms: 1.11x faster                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.27 ms: 1.10x faster                                                  |
| pyflate                    | 449 ms                                                       | 408 ms: 1.10x faster                                                   |
| dulwich_log                | 74.8 ms                                                      | 68.1 ms: 1.10x faster                                                  |
| pylint                     | 317 ms                                                       | 289 ms: 1.10x faster                                                   |
| html5lib                   | 67.0 ms                                                      | 61.5 ms: 1.09x faster                                                  |
| richards                   | 45.2 ms                                                      | 41.8 ms: 1.08x faster                                                  |
| richards_super             | 51.6 ms                                                      | 47.8 ms: 1.08x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.88 ms: 1.07x faster                                                  |
| regex_compile              | 132 ms                                                       | 124 ms: 1.07x faster                                                   |
| hexiom                     | 5.99 ms                                                      | 5.64 ms: 1.06x faster                                                  |
| logging_simple             | 6.16 us                                                      | 5.81 us: 1.06x faster                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 61.8 ms: 1.06x faster                                                  |
| tomli_loads                | 2.01 sec                                                     | 1.90 sec: 1.06x faster                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.21 sec: 1.06x faster                                                 |
| pprint_safe_repr           | 738 ms                                                       | 698 ms: 1.06x faster                                                   |
| 2to3                       | 260 ms                                                       | 247 ms: 1.05x faster                                                   |
| pprint_pformat             | 1.50 sec                                                     | 1.43 sec: 1.05x faster                                                 |
| logging_silent             | 103 ns                                                       | 97.9 ns: 1.05x faster                                                  |
| sympy_integrate            | 19.8 ms                                                      | 19.0 ms: 1.05x faster                                                  |
| comprehensions             | 16.5 us                                                      | 15.8 us: 1.04x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 131 ms: 1.04x faster                                                   |
| pycparser                  | 1.12 sec                                                     | 1.07 sec: 1.04x faster                                                 |
| genshi_text                | 21.5 ms                                                      | 20.7 ms: 1.04x faster                                                  |
| logging_format             | 6.84 us                                                      | 6.59 us: 1.04x faster                                                  |
| generators                 | 28.8 ms                                                      | 28.0 ms: 1.03x faster                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 83.0 ms: 1.03x faster                                                  |
| chaos                      | 57.3 ms                                                      | 55.8 ms: 1.03x faster                                                  |
| docutils                   | 2.62 sec                                                     | 2.55 sec: 1.03x faster                                                 |
| thrift                     | 778 us                                                       | 758 us: 1.03x faster                                                   |
| meteor_contest             | 102 ms                                                       | 99.0 ms: 1.03x faster                                                  |
| raytrace                   | 253 ms                                                       | 246 ms: 1.03x faster                                                   |
| coverage                   | 83.0 ms                                                      | 81.0 ms: 1.02x faster                                                  |
| scimark_lu                 | 113 ms                                                       | 110 ms: 1.02x faster                                                   |
| xml_etree_process          | 59.3 ms                                                      | 58.2 ms: 1.02x faster                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 7.26 ms: 1.02x faster                                                  |
| nqueens                    | 78.6 ms                                                      | 78.1 ms: 1.01x faster                                                  |
| genshi_xml                 | 48.8 ms                                                      | 48.5 ms: 1.01x faster                                                  |
| unpickle_pure_python       | 210 us                                                       | 210 us: 1.00x faster                                                   |
| django_template            | 34.1 ms                                                      | 34.3 ms: 1.00x slower                                                  |
| mako                       | 11.3 ms                                                      | 11.4 ms: 1.00x slower                                                  |
| coroutines                 | 23.6 ms                                                      | 23.9 ms: 1.02x slower                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.24 us: 1.02x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 69.0 ms: 1.02x slower                                                  |
| pidigits                   | 217 ms                                                       | 220 ms: 1.02x slower                                                   |
| sympy_expand               | 457 ms                                                       | 468 ms: 1.02x slower                                                   |
| json                       | 4.93 ms                                                      | 5.07 ms: 1.03x slower                                                  |
| nbody                      | 85.1 ms                                                      | 88.1 ms: 1.03x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 305 us: 1.04x slower                                                   |
| regex_dna                  | 180 ms                                                       | 188 ms: 1.04x slower                                                   |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                   |
| fannkuch                   | 370 ms                                                       | 387 ms: 1.05x slower                                                   |
| json_loads                 | 27.0 us                                                      | 28.4 us: 1.05x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 3.32 ms: 1.06x slower                                                  |
| python_startup             | 11.0 ms                                                      | 12.4 ms: 1.13x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.08 ms: 1.18x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 13.1 ms: 1.19x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.93 ms: 1.45x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 4.78 ms: 1.52x slower                                                  |
| telco                      | 7.82 ms                                                      | 158 ms: 20.23x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.03x faster                                                           |

Benchmark hidden because not significant (4): sympy_str, sympy_sum, typing_runtime_protocols, regex_v8
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (7) of results/bm-20251123-3.15.0a2+-e73fbba/bm-20251123-vultr-x86_64-python-e73fbbacbba0dc65f852-3.15.0a2+-e73fbba.json: many_optionals, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.037x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.16x