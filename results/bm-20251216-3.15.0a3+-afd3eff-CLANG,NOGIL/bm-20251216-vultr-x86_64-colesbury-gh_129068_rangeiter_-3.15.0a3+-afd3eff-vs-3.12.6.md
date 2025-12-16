# Results vs. 3.12.6

- fork: colesbury
- ref: gh_129068_rangeiter_
- machine: linux-x86_64
- commit hash: afd3eff
- commit date: 2025-12-16
- overall geometric mean: 1.025x faster
- HPT reliability: 94.95%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.45x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251216-vultr-x86_64-colesbury-gh_129068_rangeiter_-3.15.0a3+-afd3eff |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 269 ms: 1.02x slower                                                      |
| docutils       | 2.64 sec                                               | 2.65 sec: 1.01x slower                                                    |
| html5lib       | 63.6 ms                                                | 65.3 ms: 1.03x slower                                                     |
| Geometric mean | (ref)                                                  | 1.02x slower                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251216-vultr-x86_64-colesbury-gh_129068_rangeiter_-3.15.0a3+-afd3eff |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 573 ms: 1.94x faster                                                      |
| async_tree_memoization_tg  | 560 ms                                                 | 308 ms: 1.82x faster                                                      |
| async_tree_io              | 1.08 sec                                               | 597 ms: 1.81x faster                                                      |
| async_tree_none_tg         | 446 ms                                                 | 250 ms: 1.78x faster                                                      |
| async_tree_none            | 464 ms                                                 | 269 ms: 1.73x faster                                                      |
| async_tree_memoization     | 555 ms                                                 | 334 ms: 1.66x faster                                                      |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 486 ms: 1.49x faster                                                      |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 514 ms: 1.39x faster                                                      |
| async_generators           | 384 ms                                                 | 338 ms: 1.14x faster                                                      |
| coroutines                 | 23.9 ms                                                | 21.9 ms: 1.09x faster                                                     |
| asyncio_websockets         | 517 ms                                                 | 510 ms: 1.01x faster                                                      |
| Geometric mean             | (ref)                                                  | 1.50x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251216-vultr-x86_64-colesbury-gh_129068_rangeiter_-3.15.0a3+-afd3eff |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 69.8 ms: 1.16x faster                                                     |
| pidigits       | 184 ms                                                 | 192 ms: 1.04x slower                                                      |
| nbody          | 89.3 ms                                                | 117 ms: 1.31x slower                                                      |
| Geometric mean | (ref)                                                  | 1.06x slower                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251216-vultr-x86_64-colesbury-gh_129068_rangeiter_-3.15.0a3+-afd3eff |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 134 ms: 1.06x faster                                                      |
| regex_effbot   | 3.17 ms                                                | 3.39 ms: 1.07x slower                                                     |
| regex_v8       | 20.6 ms                                                | 24.1 ms: 1.17x slower                                                     |
| regex_dna      | 168 ms                                                 | 206 ms: 1.23x slower                                                      |
| Geometric mean | (ref)                                                  | 1.10x slower                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251216-vultr-x86_64-colesbury-gh_129068_rangeiter_-3.15.0a3+-afd3eff |
|---------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| xml_etree_iterparse | 96.7 ms                                                | 84.1 ms: 1.15x faster                                                     |
| json_dumps          | 10.4 ms                                                | 9.54 ms: 1.09x faster                                                     |
| pickle_pure_python  | 308 us                                                 | 313 us: 1.02x slower                                                      |
| xml_etree_generate  | 85.2 ms                                                | 87.3 ms: 1.02x slower                                                     |
| tomli_loads         | 2.11 sec                                               | 2.16 sec: 1.03x slower                                                    |
| xml_etree_parse     | 139 ms                                                 | 143 ms: 1.03x slower                                                      |
| xml_etree_process   | 59.0 ms                                                | 62.2 ms: 1.06x slower                                                     |
| json_loads          | 26.5 us                                                | 28.4 us: 1.07x slower                                                     |
| Geometric mean      | (ref)                                                  | 1.00x faster                                                              |

Benchmark hidden because not significant (1): unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251216-vultr-x86_64-colesbury-gh_129068_rangeiter_-3.15.0a3+-afd3eff |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.59 ms: 1.34x slower                                                     |
| python_startup         | 9.93 ms                                                | 15.6 ms: 1.57x slower                                                     |
| Geometric mean         | (ref)                                                  | 1.45x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251216-vultr-x86_64-colesbury-gh_129068_rangeiter_-3.15.0a3+-afd3eff |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 22.9 ms: 1.00x slower                                                     |
| genshi_xml      | 50.2 ms                                                | 50.4 ms: 1.00x slower                                                     |
| django_template | 34.7 ms                                                | 36.0 ms: 1.04x slower                                                     |
| mako            | 11.0 ms                                                | 15.1 ms: 1.37x slower                                                     |
| Geometric mean  | (ref)                                                  | 1.09x slower                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251216-vultr-x86_64-colesbury-gh_129068_rangeiter_-3.15.0a3+-afd3eff |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 573 ms: 1.94x faster                                                      |
| mdp                        | 2.42 sec                                               | 1.26 sec: 1.93x faster                                                    |
| async_tree_memoization_tg  | 560 ms                                                 | 308 ms: 1.82x faster                                                      |
| async_tree_io              | 1.08 sec                                               | 597 ms: 1.81x faster                                                      |
| async_tree_none_tg         | 446 ms                                                 | 250 ms: 1.78x faster                                                      |
| async_tree_none            | 464 ms                                                 | 269 ms: 1.73x faster                                                      |
| async_tree_memoization     | 555 ms                                                 | 334 ms: 1.66x faster                                                      |
| gc_traversal               | 3.46 ms                                                | 2.19 ms: 1.58x faster                                                     |
| bench_mp_pool              | 10.8 ms                                                | 7.14 ms: 1.51x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 486 ms: 1.49x faster                                                      |
| deepcopy                   | 352 us                                                 | 247 us: 1.42x faster                                                      |
| deepcopy_memo              | 40.3 us                                                | 28.5 us: 1.41x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 514 ms: 1.39x faster                                                      |
| pathlib                    | 21.5 ms                                                | 17.1 ms: 1.26x faster                                                     |
| logging_silent             | 109 ns                                                 | 86.5 ns: 1.26x faster                                                     |
| comprehensions             | 19.8 us                                                | 16.3 us: 1.22x faster                                                     |
| go                         | 139 ms                                                 | 115 ms: 1.21x faster                                                      |
| deepcopy_reduce            | 3.08 us                                                | 2.62 us: 1.17x faster                                                     |
| scimark_sor                | 130 ms                                                 | 112 ms: 1.16x faster                                                      |
| float                      | 80.8 ms                                                | 69.8 ms: 1.16x faster                                                     |
| pylint                     | 319 ms                                                 | 277 ms: 1.15x faster                                                      |
| xml_etree_iterparse        | 96.7 ms                                                | 84.1 ms: 1.15x faster                                                     |
| generators                 | 32.2 ms                                                | 28.1 ms: 1.15x faster                                                     |
| scimark_fft                | 342 ms                                                 | 299 ms: 1.14x faster                                                      |
| async_generators           | 384 ms                                                 | 338 ms: 1.14x faster                                                      |
| spectral_norm              | 110 ms                                                 | 97.6 ms: 1.13x faster                                                     |
| bpe_tokeniser              | 4.74 sec                                               | 4.23 sec: 1.12x faster                                                    |
| coroutines                 | 23.9 ms                                                | 21.9 ms: 1.09x faster                                                     |
| sqlite_synth               | 2.20 us                                                | 2.03 us: 1.09x faster                                                     |
| json_dumps                 | 10.4 ms                                                | 9.54 ms: 1.09x faster                                                     |
| chaos                      | 62.8 ms                                                | 58.2 ms: 1.08x faster                                                     |
| raytrace                   | 299 ms                                                 | 278 ms: 1.08x faster                                                      |
| dulwich_log                | 78.9 ms                                                | 73.6 ms: 1.07x faster                                                     |
| regex_compile              | 142 ms                                                 | 134 ms: 1.06x faster                                                      |
| scimark_lu                 | 114 ms                                                 | 108 ms: 1.06x faster                                                      |
| pyflate                    | 448 ms                                                 | 425 ms: 1.05x faster                                                      |
| deltablue                  | 3.45 ms                                                | 3.27 ms: 1.05x faster                                                     |
| pycparser                  | 1.17 sec                                               | 1.12 sec: 1.05x faster                                                    |
| pprint_safe_repr           | 743 ms                                                 | 720 ms: 1.03x faster                                                      |
| logging_simple             | 6.63 us                                                | 6.48 us: 1.02x faster                                                     |
| pprint_pformat             | 1.52 sec                                               | 1.49 sec: 1.02x faster                                                    |
| hexiom                     | 6.17 ms                                                | 6.07 ms: 1.02x faster                                                     |
| asyncio_websockets         | 517 ms                                                 | 510 ms: 1.01x faster                                                      |
| genshi_text                | 22.8 ms                                                | 22.9 ms: 1.00x slower                                                     |
| genshi_xml                 | 50.2 ms                                                | 50.4 ms: 1.00x slower                                                     |
| docutils                   | 2.64 sec                                               | 2.65 sec: 1.01x slower                                                    |
| scimark_monte_carlo        | 68.4 ms                                                | 69.4 ms: 1.01x slower                                                     |
| logging_format             | 7.35 us                                                | 7.46 us: 1.02x slower                                                     |
| sympy_str                  | 292 ms                                                 | 297 ms: 1.02x slower                                                      |
| pickle_pure_python         | 308 us                                                 | 313 us: 1.02x slower                                                      |
| 2to3                       | 264 ms                                                 | 269 ms: 1.02x slower                                                      |
| json                       | 5.02 ms                                                | 5.14 ms: 1.02x slower                                                     |
| xml_etree_generate         | 85.2 ms                                                | 87.3 ms: 1.02x slower                                                     |
| tomli_loads                | 2.11 sec                                               | 2.16 sec: 1.03x slower                                                    |
| html5lib                   | 63.6 ms                                                | 65.3 ms: 1.03x slower                                                     |
| richards_super             | 51.9 ms                                                | 53.4 ms: 1.03x slower                                                     |
| xml_etree_parse            | 139 ms                                                 | 143 ms: 1.03x slower                                                      |
| django_template            | 34.7 ms                                                | 36.0 ms: 1.04x slower                                                     |
| nqueens                    | 80.1 ms                                                | 83.2 ms: 1.04x slower                                                     |
| pidigits                   | 184 ms                                                 | 192 ms: 1.04x slower                                                      |
| typing_runtime_protocols   | 163 us                                                 | 172 us: 1.05x slower                                                      |
| crypto_pyaes               | 76.6 ms                                                | 80.6 ms: 1.05x slower                                                     |
| xml_etree_process          | 59.0 ms                                                | 62.2 ms: 1.06x slower                                                     |
| json_loads                 | 26.5 us                                                | 28.4 us: 1.07x slower                                                     |
| regex_effbot               | 3.17 ms                                                | 3.39 ms: 1.07x slower                                                     |
| sympy_expand               | 468 ms                                                 | 505 ms: 1.08x slower                                                      |
| thrift                     | 791 us                                                 | 860 us: 1.09x slower                                                      |
| fannkuch                   | 372 ms                                                 | 412 ms: 1.11x slower                                                      |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.97 ms: 1.13x slower                                                     |
| meteor_contest             | 104 ms                                                 | 121 ms: 1.17x slower                                                      |
| regex_v8                   | 20.6 ms                                                | 24.1 ms: 1.17x slower                                                     |
| regex_dna                  | 168 ms                                                 | 206 ms: 1.23x slower                                                      |
| nbody                      | 89.3 ms                                                | 117 ms: 1.31x slower                                                      |
| python_startup_no_site     | 7.16 ms                                                | 9.59 ms: 1.34x slower                                                     |
| coverage                   | 71.4 ms                                                | 95.7 ms: 1.34x slower                                                     |
| create_gc_cycles           | 1.09 ms                                                | 1.47 ms: 1.35x slower                                                     |
| mako                       | 11.0 ms                                                | 15.1 ms: 1.37x slower                                                     |
| bench_thread_pool          | 941 us                                                 | 1.46 ms: 1.55x slower                                                     |
| python_startup             | 9.93 ms                                                | 15.6 ms: 1.57x slower                                                     |
| telco                      | 6.53 ms                                                | 168 ms: 25.67x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.03x faster                                                              |

Benchmark hidden because not significant (4): richards, unpickle_pure_python, sympy_integrate, sympy_sum
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251216-3.15.0a3+-afd3eff-CLANG,NOGIL/bm-20251216-vultr-x86_64-colesbury-gh_129068_rangeiter_-3.15.0a3+-afd3eff.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.025x faster

# HPT report

- Reliability score: 94.95% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.45x