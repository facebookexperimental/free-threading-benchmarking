# Results vs. 3.13.0rc2

- fork: faster-cpython
- ref: tier_2_tos_caching
- machine: linux-x86_64
- commit hash: 4b24c15
- commit date: 2025-12-10
- overall geometric mean: 1.071x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251210-vultr-x86_64-faster%2dcpython-tier_2_tos_caching-3.15.0a2+-4b24c15 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 247 ms: 1.05x faster                                                           |
| html5lib       | 67.0 ms                                                      | 67.8 ms: 1.01x slower                                                          |
| Geometric mean | (ref)                                                        | 1.02x faster                                                                   |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251210-vultr-x86_64-faster%2dcpython-tier_2_tos_caching-3.15.0a2+-4b24c15 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| async_tree_io              | 876 ms                                                       | 551 ms: 1.59x faster                                                           |
| async_tree_io_tg           | 913 ms                                                       | 587 ms: 1.56x faster                                                           |
| async_tree_memoization     | 461 ms                                                       | 301 ms: 1.53x faster                                                           |
| async_tree_none            | 354 ms                                                       | 240 ms: 1.47x faster                                                           |
| async_tree_none_tg         | 336 ms                                                       | 243 ms: 1.39x faster                                                           |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 484 ms: 1.38x faster                                                           |
| async_tree_memoization_tg  | 414 ms                                                       | 302 ms: 1.37x faster                                                           |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 484 ms: 1.32x faster                                                           |
| async_generators           | 377 ms                                                       | 357 ms: 1.06x faster                                                           |
| coroutines                 | 23.6 ms                                                      | 23.7 ms: 1.01x slower                                                          |
| asyncio_websockets         | 520 ms                                                       | 545 ms: 1.05x slower                                                           |
| Geometric mean             | (ref)                                                        | 1.31x faster                                                                   |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251210-vultr-x86_64-faster%2dcpython-tier_2_tos_caching-3.15.0a2+-4b24c15 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 58.8 ms: 1.32x faster                                                          |
| nbody          | 85.1 ms                                                      | 70.8 ms: 1.20x faster                                                          |
| pidigits       | 217 ms                                                       | 191 ms: 1.13x faster                                                           |
| Geometric mean | (ref)                                                        | 1.21x faster                                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251210-vultr-x86_64-faster%2dcpython-tier_2_tos_caching-3.15.0a2+-4b24c15 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| regex_compile  | 132 ms                                                       | 123 ms: 1.08x faster                                                           |
| regex_effbot   | 3.08 ms                                                      | 2.92 ms: 1.05x faster                                                          |
| regex_v8       | 22.7 ms                                                      | 22.5 ms: 1.01x faster                                                          |
| regex_dna      | 180 ms                                                       | 186 ms: 1.03x slower                                                           |
| Geometric mean | (ref)                                                        | 1.03x faster                                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251210-vultr-x86_64-faster%2dcpython-tier_2_tos_caching-3.15.0a2+-4b24c15 |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| unpickle_pure_python | 210 us                                                       | 184 us: 1.14x faster                                                           |
| xml_etree_iterparse  | 94.9 ms                                                      | 84.1 ms: 1.13x faster                                                          |
| json_dumps           | 10.5 ms                                                      | 9.44 ms: 1.12x faster                                                          |
| xml_etree_generate   | 85.4 ms                                                      | 76.8 ms: 1.11x faster                                                          |
| xml_etree_process    | 59.3 ms                                                      | 53.6 ms: 1.11x faster                                                          |
| xml_etree_parse      | 136 ms                                                       | 130 ms: 1.05x faster                                                           |
| pickle_pure_python   | 294 us                                                       | 284 us: 1.04x faster                                                           |
| json_loads           | 27.0 us                                                      | 28.9 us: 1.07x slower                                                          |
| tomli_loads          | 2.01 sec                                                     | 2.33 sec: 1.16x slower                                                         |
| Geometric mean       | (ref)                                                        | 1.05x faster                                                                   |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251210-vultr-x86_64-faster%2dcpython-tier_2_tos_caching-3.15.0a2+-4b24c15 |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.35 ms: 1.01x faster                                                          |
| python_startup         | 11.0 ms                                                      | 12.6 ms: 1.15x slower                                                          |
| Geometric mean         | (ref)                                                        | 1.07x slower                                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251210-vultr-x86_64-faster%2dcpython-tier_2_tos_caching-3.15.0a2+-4b24c15 |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| mako            | 11.3 ms                                                      | 10.5 ms: 1.08x faster                                                          |
| genshi_text     | 21.5 ms                                                      | 21.2 ms: 1.02x faster                                                          |
| django_template | 34.1 ms                                                      | 36.1 ms: 1.06x slower                                                          |
| genshi_xml      | 48.8 ms                                                      | 55.1 ms: 1.13x slower                                                          |
| Geometric mean  | (ref)                                                        | 1.02x slower                                                                   |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251210-vultr-x86_64-faster%2dcpython-tier_2_tos_caching-3.15.0a2+-4b24c15 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| richards                   | 45.2 ms                                                      | 19.9 ms: 2.27x faster                                                          |
| richards_super             | 51.6 ms                                                      | 24.3 ms: 2.13x faster                                                          |
| mdp                        | 2.36 sec                                                     | 1.33 sec: 1.77x faster                                                         |
| async_tree_io              | 876 ms                                                       | 551 ms: 1.59x faster                                                           |
| async_tree_io_tg           | 913 ms                                                       | 587 ms: 1.56x faster                                                           |
| deepcopy_memo              | 39.1 us                                                      | 25.2 us: 1.55x faster                                                          |
| async_tree_memoization     | 461 ms                                                       | 301 ms: 1.53x faster                                                           |
| async_tree_none            | 354 ms                                                       | 240 ms: 1.47x faster                                                           |
| deepcopy                   | 355 us                                                       | 246 us: 1.45x faster                                                           |
| go                         | 141 ms                                                       | 99.5 ms: 1.41x faster                                                          |
| async_tree_none_tg         | 336 ms                                                       | 243 ms: 1.39x faster                                                           |
| scimark_fft                | 349 ms                                                       | 253 ms: 1.38x faster                                                           |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 484 ms: 1.38x faster                                                           |
| async_tree_memoization_tg  | 414 ms                                                       | 302 ms: 1.37x faster                                                           |
| scimark_sor                | 134 ms                                                       | 98.4 ms: 1.37x faster                                                          |
| spectral_norm              | 111 ms                                                       | 82.5 ms: 1.35x faster                                                          |
| float                      | 77.5 ms                                                      | 58.8 ms: 1.32x faster                                                          |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 484 ms: 1.32x faster                                                           |
| deepcopy_reduce            | 3.11 us                                                      | 2.53 us: 1.23x faster                                                          |
| pyflate                    | 449 ms                                                       | 368 ms: 1.22x faster                                                           |
| nbody                      | 85.1 ms                                                      | 70.8 ms: 1.20x faster                                                          |
| logging_silent             | 103 ns                                                       | 86.3 ns: 1.19x faster                                                          |
| scimark_monte_carlo        | 65.4 ms                                                      | 55.1 ms: 1.19x faster                                                          |
| unpickle_pure_python       | 210 us                                                       | 184 us: 1.14x faster                                                           |
| pidigits                   | 217 ms                                                       | 191 ms: 1.13x faster                                                           |
| xml_etree_iterparse        | 94.9 ms                                                      | 84.1 ms: 1.13x faster                                                          |
| pprint_pformat             | 1.50 sec                                                     | 1.33 sec: 1.12x faster                                                         |
| pprint_safe_repr           | 738 ms                                                       | 661 ms: 1.12x faster                                                           |
| json_dumps                 | 10.5 ms                                                      | 9.44 ms: 1.12x faster                                                          |
| xml_etree_generate         | 85.4 ms                                                      | 76.8 ms: 1.11x faster                                                          |
| xml_etree_process          | 59.3 ms                                                      | 53.6 ms: 1.11x faster                                                          |
| deltablue                  | 3.12 ms                                                      | 2.82 ms: 1.11x faster                                                          |
| bpe_tokeniser              | 4.45 sec                                                     | 4.02 sec: 1.11x faster                                                         |
| pathlib                    | 19.2 ms                                                      | 17.5 ms: 1.09x faster                                                          |
| scimark_lu                 | 113 ms                                                       | 104 ms: 1.09x faster                                                           |
| logging_simple             | 6.16 us                                                      | 5.71 us: 1.08x faster                                                          |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.36 ms: 1.08x faster                                                          |
| mako                       | 11.3 ms                                                      | 10.5 ms: 1.08x faster                                                          |
| regex_compile              | 132 ms                                                       | 123 ms: 1.08x faster                                                           |
| thrift                     | 778 us                                                       | 731 us: 1.06x faster                                                           |
| async_generators           | 377 ms                                                       | 357 ms: 1.06x faster                                                           |
| logging_format             | 6.84 us                                                      | 6.48 us: 1.06x faster                                                          |
| regex_effbot               | 3.08 ms                                                      | 2.92 ms: 1.05x faster                                                          |
| chaos                      | 57.3 ms                                                      | 54.4 ms: 1.05x faster                                                          |
| 2to3                       | 260 ms                                                       | 247 ms: 1.05x faster                                                           |
| xml_etree_parse            | 136 ms                                                       | 130 ms: 1.05x faster                                                           |
| dulwich_log                | 74.8 ms                                                      | 71.5 ms: 1.05x faster                                                          |
| meteor_contest             | 102 ms                                                       | 97.1 ms: 1.05x faster                                                          |
| pickle_pure_python         | 294 us                                                       | 284 us: 1.04x faster                                                           |
| generators                 | 28.8 ms                                                      | 28.0 ms: 1.03x faster                                                          |
| fannkuch                   | 370 ms                                                       | 360 ms: 1.03x faster                                                           |
| crypto_pyaes               | 67.9 ms                                                      | 66.4 ms: 1.02x faster                                                          |
| genshi_text                | 21.5 ms                                                      | 21.2 ms: 1.02x faster                                                          |
| coverage                   | 83.0 ms                                                      | 81.6 ms: 1.02x faster                                                          |
| comprehensions             | 16.5 us                                                      | 16.2 us: 1.01x faster                                                          |
| pycparser                  | 1.12 sec                                                     | 1.11 sec: 1.01x faster                                                         |
| regex_v8                   | 22.7 ms                                                      | 22.5 ms: 1.01x faster                                                          |
| python_startup_no_site     | 7.39 ms                                                      | 7.35 ms: 1.01x faster                                                          |
| coroutines                 | 23.6 ms                                                      | 23.7 ms: 1.01x slower                                                          |
| sqlite_synth               | 2.21 us                                                      | 2.23 us: 1.01x slower                                                          |
| html5lib                   | 67.0 ms                                                      | 67.8 ms: 1.01x slower                                                          |
| typing_runtime_protocols   | 155 us                                                       | 158 us: 1.02x slower                                                           |
| raytrace                   | 253 ms                                                       | 257 ms: 1.02x slower                                                           |
| regex_dna                  | 180 ms                                                       | 186 ms: 1.03x slower                                                           |
| hexiom                     | 5.99 ms                                                      | 6.21 ms: 1.04x slower                                                          |
| json                       | 4.93 ms                                                      | 5.12 ms: 1.04x slower                                                          |
| asyncio_websockets         | 520 ms                                                       | 545 ms: 1.05x slower                                                           |
| django_template            | 34.1 ms                                                      | 36.1 ms: 1.06x slower                                                          |
| sympy_integrate            | 19.8 ms                                                      | 21.2 ms: 1.07x slower                                                          |
| json_loads                 | 27.0 us                                                      | 28.9 us: 1.07x slower                                                          |
| nqueens                    | 78.6 ms                                                      | 85.2 ms: 1.08x slower                                                          |
| sympy_expand               | 457 ms                                                       | 510 ms: 1.12x slower                                                           |
| sympy_sum                  | 156 ms                                                       | 174 ms: 1.12x slower                                                           |
| genshi_xml                 | 48.8 ms                                                      | 55.1 ms: 1.13x slower                                                          |
| sympy_str                  | 275 ms                                                       | 314 ms: 1.14x slower                                                           |
| python_startup             | 11.0 ms                                                      | 12.6 ms: 1.15x slower                                                          |
| tomli_loads                | 2.01 sec                                                     | 2.33 sec: 1.16x slower                                                         |
| create_gc_cycles           | 1.34 ms                                                      | 1.85 ms: 1.38x slower                                                          |
| bench_thread_pool          | 919 us                                                       | 1.32 ms: 1.44x slower                                                          |
| gc_traversal               | 3.14 ms                                                      | 4.70 ms: 1.49x slower                                                          |
| bench_mp_pool              | 11.0 ms                                                      | 218 ms: 19.86x slower                                                          |
| telco                      | 7.82 ms                                                      | 160 ms: 20.39x slower                                                          |
| Geometric mean             | (ref)                                                        | 1.03x faster                                                                   |

Benchmark hidden because not significant (1): pylint
Ignored benchmarks (19) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, docutils, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251210-3.15.0a2+-4b24c15-JIT/bm-20251210-vultr-x86_64-faster%2dcpython-tier_2_tos_caching-3.15.0a2+-4b24c15.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.071x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.19x