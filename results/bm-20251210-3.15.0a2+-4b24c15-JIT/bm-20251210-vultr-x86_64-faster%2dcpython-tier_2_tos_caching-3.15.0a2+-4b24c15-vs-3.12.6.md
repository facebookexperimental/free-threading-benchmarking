# Results vs. 3.12.6

- fork: faster-cpython
- ref: tier_2_tos_caching
- machine: linux-x86_64
- commit hash: 4b24c15
- commit date: 2025-12-10
- overall geometric mean: 1.108x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251210-vultr-x86_64-faster%2dcpython-tier_2_tos_caching-3.15.0a2+-4b24c15 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 247 ms: 1.06x faster                                                           |
| html5lib       | 63.6 ms                                                | 67.8 ms: 1.07x slower                                                          |
| Geometric mean | (ref)                                                  | 1.00x slower                                                                   |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251210-vultr-x86_64-faster%2dcpython-tier_2_tos_caching-3.15.0a2+-4b24c15 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| async_tree_io              | 1.08 sec                                               | 551 ms: 1.97x faster                                                           |
| async_tree_none            | 464 ms                                                 | 240 ms: 1.94x faster                                                           |
| async_tree_io_tg           | 1.11 sec                                               | 587 ms: 1.89x faster                                                           |
| async_tree_memoization_tg  | 560 ms                                                 | 302 ms: 1.85x faster                                                           |
| async_tree_memoization     | 555 ms                                                 | 301 ms: 1.84x faster                                                           |
| async_tree_none_tg         | 446 ms                                                 | 243 ms: 1.84x faster                                                           |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 484 ms: 1.49x faster                                                           |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 484 ms: 1.48x faster                                                           |
| async_generators           | 384 ms                                                 | 357 ms: 1.08x faster                                                           |
| coroutines                 | 23.9 ms                                                | 23.7 ms: 1.01x faster                                                          |
| asyncio_websockets         | 517 ms                                                 | 545 ms: 1.05x slower                                                           |
| Geometric mean             | (ref)                                                  | 1.52x faster                                                                   |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251210-vultr-x86_64-faster%2dcpython-tier_2_tos_caching-3.15.0a2+-4b24c15 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 58.8 ms: 1.37x faster                                                          |
| nbody          | 89.3 ms                                                | 70.8 ms: 1.26x faster                                                          |
| pidigits       | 184 ms                                                 | 191 ms: 1.04x slower                                                           |
| Geometric mean | (ref)                                                  | 1.19x faster                                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251210-vultr-x86_64-faster%2dcpython-tier_2_tos_caching-3.15.0a2+-4b24c15 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 123 ms: 1.16x faster                                                           |
| regex_effbot   | 3.17 ms                                                | 2.92 ms: 1.08x faster                                                          |
| regex_v8       | 20.6 ms                                                | 22.5 ms: 1.09x slower                                                          |
| regex_dna      | 168 ms                                                 | 186 ms: 1.11x slower                                                           |
| Geometric mean | (ref)                                                  | 1.01x faster                                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251210-vultr-x86_64-faster%2dcpython-tier_2_tos_caching-3.15.0a2+-4b24c15 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| unpickle_pure_python | 221 us                                                 | 184 us: 1.20x faster                                                           |
| xml_etree_iterparse  | 96.7 ms                                                | 84.1 ms: 1.15x faster                                                          |
| xml_etree_generate   | 85.2 ms                                                | 76.8 ms: 1.11x faster                                                          |
| xml_etree_process    | 59.0 ms                                                | 53.6 ms: 1.10x faster                                                          |
| json_dumps           | 10.4 ms                                                | 9.44 ms: 1.10x faster                                                          |
| pickle_pure_python   | 308 us                                                 | 284 us: 1.08x faster                                                           |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.07x faster                                                           |
| json_loads           | 26.5 us                                                | 28.9 us: 1.09x slower                                                          |
| tomli_loads          | 2.11 sec                                               | 2.33 sec: 1.11x slower                                                         |
| Geometric mean       | (ref)                                                  | 1.07x faster                                                                   |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251210-vultr-x86_64-faster%2dcpython-tier_2_tos_caching-3.15.0a2+-4b24c15 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.35 ms: 1.03x slower                                                          |
| python_startup         | 9.93 ms                                                | 12.6 ms: 1.27x slower                                                          |
| Geometric mean         | (ref)                                                  | 1.14x slower                                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251210-vultr-x86_64-faster%2dcpython-tier_2_tos_caching-3.15.0a2+-4b24c15 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 21.2 ms: 1.08x faster                                                          |
| mako            | 11.0 ms                                                | 10.5 ms: 1.05x faster                                                          |
| django_template | 34.7 ms                                                | 36.1 ms: 1.04x slower                                                          |
| genshi_xml      | 50.2 ms                                                | 55.1 ms: 1.10x slower                                                          |
| Geometric mean  | (ref)                                                  | 1.00x slower                                                                   |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251210-vultr-x86_64-faster%2dcpython-tier_2_tos_caching-3.15.0a2+-4b24c15 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| richards                   | 45.9 ms                                                | 19.9 ms: 2.31x faster                                                          |
| richards_super             | 51.9 ms                                                | 24.3 ms: 2.14x faster                                                          |
| async_tree_io              | 1.08 sec                                               | 551 ms: 1.97x faster                                                           |
| async_tree_none            | 464 ms                                                 | 240 ms: 1.94x faster                                                           |
| async_tree_io_tg           | 1.11 sec                                               | 587 ms: 1.89x faster                                                           |
| async_tree_memoization_tg  | 560 ms                                                 | 302 ms: 1.85x faster                                                           |
| async_tree_memoization     | 555 ms                                                 | 301 ms: 1.84x faster                                                           |
| async_tree_none_tg         | 446 ms                                                 | 243 ms: 1.84x faster                                                           |
| mdp                        | 2.42 sec                                               | 1.33 sec: 1.81x faster                                                         |
| deepcopy_memo              | 40.3 us                                                | 25.2 us: 1.60x faster                                                          |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 484 ms: 1.49x faster                                                           |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 484 ms: 1.48x faster                                                           |
| deepcopy                   | 352 us                                                 | 246 us: 1.43x faster                                                           |
| go                         | 139 ms                                                 | 99.5 ms: 1.40x faster                                                          |
| float                      | 80.8 ms                                                | 58.8 ms: 1.37x faster                                                          |
| scimark_fft                | 342 ms                                                 | 253 ms: 1.35x faster                                                           |
| spectral_norm              | 110 ms                                                 | 82.5 ms: 1.34x faster                                                          |
| scimark_sor                | 130 ms                                                 | 98.4 ms: 1.32x faster                                                          |
| logging_silent             | 109 ns                                                 | 86.3 ns: 1.26x faster                                                          |
| nbody                      | 89.3 ms                                                | 70.8 ms: 1.26x faster                                                          |
| scimark_monte_carlo        | 68.4 ms                                                | 55.1 ms: 1.24x faster                                                          |
| pathlib                    | 21.5 ms                                                | 17.5 ms: 1.23x faster                                                          |
| comprehensions             | 19.8 us                                                | 16.2 us: 1.22x faster                                                          |
| deltablue                  | 3.45 ms                                                | 2.82 ms: 1.22x faster                                                          |
| pyflate                    | 448 ms                                                 | 368 ms: 1.22x faster                                                           |
| deepcopy_reduce            | 3.08 us                                                | 2.53 us: 1.22x faster                                                          |
| unpickle_pure_python       | 221 us                                                 | 184 us: 1.20x faster                                                           |
| bpe_tokeniser              | 4.74 sec                                               | 4.02 sec: 1.18x faster                                                         |
| raytrace                   | 299 ms                                                 | 257 ms: 1.16x faster                                                           |
| logging_simple             | 6.63 us                                                | 5.71 us: 1.16x faster                                                          |
| regex_compile              | 142 ms                                                 | 123 ms: 1.16x faster                                                           |
| chaos                      | 62.8 ms                                                | 54.4 ms: 1.16x faster                                                          |
| crypto_pyaes               | 76.6 ms                                                | 66.4 ms: 1.15x faster                                                          |
| generators                 | 32.2 ms                                                | 28.0 ms: 1.15x faster                                                          |
| xml_etree_iterparse        | 96.7 ms                                                | 84.1 ms: 1.15x faster                                                          |
| pprint_pformat             | 1.52 sec                                               | 1.33 sec: 1.14x faster                                                         |
| logging_format             | 7.35 us                                                | 6.48 us: 1.13x faster                                                          |
| pprint_safe_repr           | 743 ms                                                 | 661 ms: 1.12x faster                                                           |
| xml_etree_generate         | 85.2 ms                                                | 76.8 ms: 1.11x faster                                                          |
| dulwich_log                | 78.9 ms                                                | 71.5 ms: 1.10x faster                                                          |
| scimark_lu                 | 114 ms                                                 | 104 ms: 1.10x faster                                                           |
| xml_etree_process          | 59.0 ms                                                | 53.6 ms: 1.10x faster                                                          |
| json_dumps                 | 10.4 ms                                                | 9.44 ms: 1.10x faster                                                          |
| pickle_pure_python         | 308 us                                                 | 284 us: 1.08x faster                                                           |
| regex_effbot               | 3.17 ms                                                | 2.92 ms: 1.08x faster                                                          |
| thrift                     | 791 us                                                 | 731 us: 1.08x faster                                                           |
| genshi_text                | 22.8 ms                                                | 21.2 ms: 1.08x faster                                                          |
| async_generators           | 384 ms                                                 | 357 ms: 1.08x faster                                                           |
| meteor_contest             | 104 ms                                                 | 97.1 ms: 1.07x faster                                                          |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.07x faster                                                           |
| 2to3                       | 264 ms                                                 | 247 ms: 1.06x faster                                                           |
| pycparser                  | 1.17 sec                                               | 1.11 sec: 1.06x faster                                                         |
| mako                       | 11.0 ms                                                | 10.5 ms: 1.05x faster                                                          |
| typing_runtime_protocols   | 163 us                                                 | 158 us: 1.04x faster                                                           |
| fannkuch                   | 372 ms                                                 | 360 ms: 1.03x faster                                                           |
| coroutines                 | 23.9 ms                                                | 23.7 ms: 1.01x faster                                                          |
| hexiom                     | 6.17 ms                                                | 6.21 ms: 1.01x slower                                                          |
| sqlite_synth               | 2.20 us                                                | 2.23 us: 1.01x slower                                                          |
| json                       | 5.02 ms                                                | 5.12 ms: 1.02x slower                                                          |
| python_startup_no_site     | 7.16 ms                                                | 7.35 ms: 1.03x slower                                                          |
| sympy_integrate            | 20.5 ms                                                | 21.2 ms: 1.03x slower                                                          |
| pidigits                   | 184 ms                                                 | 191 ms: 1.04x slower                                                           |
| django_template            | 34.7 ms                                                | 36.1 ms: 1.04x slower                                                          |
| sympy_sum                  | 166 ms                                                 | 174 ms: 1.05x slower                                                           |
| asyncio_websockets         | 517 ms                                                 | 545 ms: 1.05x slower                                                           |
| nqueens                    | 80.1 ms                                                | 85.2 ms: 1.06x slower                                                          |
| html5lib                   | 63.6 ms                                                | 67.8 ms: 1.07x slower                                                          |
| sympy_str                  | 292 ms                                                 | 314 ms: 1.08x slower                                                           |
| json_loads                 | 26.5 us                                                | 28.9 us: 1.09x slower                                                          |
| sympy_expand               | 468 ms                                                 | 510 ms: 1.09x slower                                                           |
| regex_v8                   | 20.6 ms                                                | 22.5 ms: 1.09x slower                                                          |
| genshi_xml                 | 50.2 ms                                                | 55.1 ms: 1.10x slower                                                          |
| tomli_loads                | 2.11 sec                                               | 2.33 sec: 1.11x slower                                                         |
| regex_dna                  | 168 ms                                                 | 186 ms: 1.11x slower                                                           |
| coverage                   | 71.4 ms                                                | 81.6 ms: 1.14x slower                                                          |
| python_startup             | 9.93 ms                                                | 12.6 ms: 1.27x slower                                                          |
| gc_traversal               | 3.46 ms                                                | 4.70 ms: 1.36x slower                                                          |
| bench_thread_pool          | 941 us                                                 | 1.32 ms: 1.40x slower                                                          |
| create_gc_cycles           | 1.09 ms                                                | 1.85 ms: 1.70x slower                                                          |
| bench_mp_pool              | 10.8 ms                                                | 218 ms: 20.22x slower                                                          |
| telco                      | 6.53 ms                                                | 160 ms: 24.44x slower                                                          |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                                   |

Benchmark hidden because not significant (2): pylint, scimark_sparse_mat_mult
Ignored benchmarks (22) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, docutils, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251210-3.15.0a2+-4b24c15-JIT/bm-20251210-vultr-x86_64-faster%2dcpython-tier_2_tos_caching-3.15.0a2+-4b24c15.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.108x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.20x