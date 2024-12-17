# Results vs. 3.13.0rc2

- fork: corona10
- ref: gh_115999_BINARY_SUB
- machine: linux-x86_64
- commit hash: 3aa9426
- commit date: 2024-12-17
- overall geometric mean: 1.022x faster
- HPT reliability: 97.48%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-3aa9426 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 257 ms: 1.01x faster                                                     |
| docutils       | 2.62 sec                                                     | 2.57 sec: 1.02x faster                                                   |
| Geometric mean | (ref)                                                        | 1.01x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-3aa9426 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 621 ms: 1.47x faster                                                     |
| async_tree_io              | 876 ms                                                       | 610 ms: 1.44x faster                                                     |
| async_tree_memoization     | 461 ms                                                       | 341 ms: 1.35x faster                                                     |
| async_tree_none            | 354 ms                                                       | 276 ms: 1.28x faster                                                     |
| async_tree_memoization_tg  | 414 ms                                                       | 330 ms: 1.26x faster                                                     |
| async_tree_none_tg         | 336 ms                                                       | 273 ms: 1.23x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 605 ms: 1.10x faster                                                     |
| coroutines                 | 23.6 ms                                                      | 22.0 ms: 1.07x faster                                                    |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 601 ms: 1.06x faster                                                     |
| async_generators           | 377 ms                                                       | 362 ms: 1.04x faster                                                     |
| asyncio_websockets         | 520 ms                                                       | 523 ms: 1.00x slower                                                     |
| Geometric mean             | (ref)                                                        | 1.20x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-3aa9426 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 222 ms: 1.03x slower                                                     |
| float          | 77.5 ms                                                      | 79.6 ms: 1.03x slower                                                    |
| nbody          | 85.1 ms                                                      | 95.4 ms: 1.12x slower                                                    |
| Geometric mean | (ref)                                                        | 1.06x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-3aa9426 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.77 ms: 1.11x faster                                                    |
| regex_dna      | 180 ms                                                       | 171 ms: 1.05x faster                                                     |
| regex_compile  | 132 ms                                                       | 130 ms: 1.02x faster                                                     |
| regex_v8       | 22.7 ms                                                      | 24.3 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                        | 1.03x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-3aa9426 |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_loads           | 27.0 us                                                      | 25.1 us: 1.07x faster                                                    |
| xml_etree_parse      | 136 ms                                                       | 128 ms: 1.07x faster                                                     |
| xml_etree_iterparse  | 94.9 ms                                                      | 91.0 ms: 1.04x faster                                                    |
| xml_etree_process    | 59.3 ms                                                      | 59.6 ms: 1.00x slower                                                    |
| unpickle_pure_python | 210 us                                                       | 215 us: 1.03x slower                                                     |
| tomli_loads          | 2.01 sec                                                     | 2.11 sec: 1.05x slower                                                   |
| pickle_pure_python   | 294 us                                                       | 322 us: 1.09x slower                                                     |
| json_dumps           | 10.5 ms                                                      | 11.5 ms: 1.10x slower                                                    |
| Geometric mean       | (ref)                                                        | 1.01x slower                                                             |

Benchmark hidden because not significant (1): xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-3aa9426 |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.48 ms: 1.01x slower                                                    |
| python_startup         | 11.0 ms                                                      | 14.6 ms: 1.33x slower                                                    |
| Geometric mean         | (ref)                                                        | 1.16x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-3aa9426 |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 21.8 ms: 1.01x slower                                                    |
| django_template | 34.1 ms                                                      | 35.3 ms: 1.03x slower                                                    |
| genshi_xml      | 48.8 ms                                                      | 50.8 ms: 1.04x slower                                                    |
| mako            | 11.3 ms                                                      | 11.9 ms: 1.05x slower                                                    |
| Geometric mean  | (ref)                                                        | 1.04x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-3aa9426 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 621 ms: 1.47x faster                                                     |
| async_tree_io              | 876 ms                                                       | 610 ms: 1.44x faster                                                     |
| deepcopy                   | 355 us                                                       | 262 us: 1.36x faster                                                     |
| async_tree_memoization     | 461 ms                                                       | 341 ms: 1.35x faster                                                     |
| async_tree_none            | 354 ms                                                       | 276 ms: 1.28x faster                                                     |
| deepcopy_memo              | 39.1 us                                                      | 30.6 us: 1.28x faster                                                    |
| async_tree_memoization_tg  | 414 ms                                                       | 330 ms: 1.26x faster                                                     |
| async_tree_none_tg         | 336 ms                                                       | 273 ms: 1.23x faster                                                     |
| deepcopy_reduce            | 3.11 us                                                      | 2.66 us: 1.17x faster                                                    |
| go                         | 141 ms                                                       | 121 ms: 1.16x faster                                                     |
| pylint                     | 317 ms                                                       | 279 ms: 1.14x faster                                                     |
| regex_effbot               | 3.08 ms                                                      | 2.77 ms: 1.11x faster                                                    |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 605 ms: 1.10x faster                                                     |
| json                       | 4.93 ms                                                      | 4.55 ms: 1.08x faster                                                    |
| json_loads                 | 27.0 us                                                      | 25.1 us: 1.07x faster                                                    |
| coroutines                 | 23.6 ms                                                      | 22.0 ms: 1.07x faster                                                    |
| xml_etree_parse            | 136 ms                                                       | 128 ms: 1.07x faster                                                     |
| telco                      | 7.82 ms                                                      | 7.37 ms: 1.06x faster                                                    |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 601 ms: 1.06x faster                                                     |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.46 ms: 1.06x faster                                                    |
| regex_dna                  | 180 ms                                                       | 171 ms: 1.05x faster                                                     |
| thrift                     | 778 us                                                       | 743 us: 1.05x faster                                                     |
| async_generators           | 377 ms                                                       | 362 ms: 1.04x faster                                                     |
| xml_etree_iterparse        | 94.9 ms                                                      | 91.0 ms: 1.04x faster                                                    |
| coverage                   | 83.0 ms                                                      | 79.7 ms: 1.04x faster                                                    |
| pathlib                    | 19.2 ms                                                      | 18.5 ms: 1.04x faster                                                    |
| scimark_fft                | 349 ms                                                       | 339 ms: 1.03x faster                                                     |
| scimark_lu                 | 113 ms                                                       | 109 ms: 1.03x faster                                                     |
| bpe_tokeniser              | 4.45 sec                                                     | 4.33 sec: 1.03x faster                                                   |
| pprint_safe_repr           | 738 ms                                                       | 718 ms: 1.03x faster                                                     |
| regex_compile              | 132 ms                                                       | 130 ms: 1.02x faster                                                     |
| docutils                   | 2.62 sec                                                     | 2.57 sec: 1.02x faster                                                   |
| pprint_pformat             | 1.50 sec                                                     | 1.47 sec: 1.02x faster                                                   |
| sympy_sum                  | 156 ms                                                       | 154 ms: 1.01x faster                                                     |
| logging_simple             | 6.16 us                                                      | 6.08 us: 1.01x faster                                                    |
| 2to3                       | 260 ms                                                       | 257 ms: 1.01x faster                                                     |
| pycparser                  | 1.12 sec                                                     | 1.11 sec: 1.01x faster                                                   |
| hexiom                     | 5.99 ms                                                      | 5.94 ms: 1.01x faster                                                    |
| meteor_contest             | 102 ms                                                       | 101 ms: 1.01x faster                                                     |
| sympy_str                  | 275 ms                                                       | 273 ms: 1.01x faster                                                     |
| sympy_integrate            | 19.8 ms                                                      | 19.9 ms: 1.00x slower                                                    |
| asyncio_websockets         | 520 ms                                                       | 523 ms: 1.00x slower                                                     |
| xml_etree_process          | 59.3 ms                                                      | 59.6 ms: 1.00x slower                                                    |
| richards_super             | 51.6 ms                                                      | 52.0 ms: 1.01x slower                                                    |
| sympy_expand               | 457 ms                                                       | 460 ms: 1.01x slower                                                     |
| crypto_pyaes               | 67.9 ms                                                      | 68.4 ms: 1.01x slower                                                    |
| richards                   | 45.2 ms                                                      | 45.6 ms: 1.01x slower                                                    |
| dulwich_log                | 74.8 ms                                                      | 75.7 ms: 1.01x slower                                                    |
| python_startup_no_site     | 7.39 ms                                                      | 7.48 ms: 1.01x slower                                                    |
| genshi_text                | 21.5 ms                                                      | 21.8 ms: 1.01x slower                                                    |
| sqlglot_normalize          | 106 ms                                                       | 108 ms: 1.02x slower                                                     |
| sqlglot_optimize           | 52.7 ms                                                      | 53.8 ms: 1.02x slower                                                    |
| sqlglot_transpile          | 1.56 ms                                                      | 1.59 ms: 1.02x slower                                                    |
| pidigits                   | 217 ms                                                       | 222 ms: 1.03x slower                                                     |
| typing_runtime_protocols   | 155 us                                                       | 159 us: 1.03x slower                                                     |
| unpickle_pure_python       | 210 us                                                       | 215 us: 1.03x slower                                                     |
| float                      | 77.5 ms                                                      | 79.6 ms: 1.03x slower                                                    |
| sqlglot_parse              | 1.25 ms                                                      | 1.29 ms: 1.03x slower                                                    |
| deltablue                  | 3.12 ms                                                      | 3.23 ms: 1.03x slower                                                    |
| django_template            | 34.1 ms                                                      | 35.3 ms: 1.03x slower                                                    |
| fannkuch                   | 370 ms                                                       | 382 ms: 1.03x slower                                                     |
| logging_silent             | 103 ns                                                       | 107 ns: 1.04x slower                                                     |
| chaos                      | 57.3 ms                                                      | 59.6 ms: 1.04x slower                                                    |
| genshi_xml                 | 48.8 ms                                                      | 50.8 ms: 1.04x slower                                                    |
| sqlite_synth               | 2.21 us                                                      | 2.31 us: 1.04x slower                                                    |
| mako                       | 11.3 ms                                                      | 11.9 ms: 1.05x slower                                                    |
| tomli_loads                | 2.01 sec                                                     | 2.11 sec: 1.05x slower                                                   |
| raytrace                   | 253 ms                                                       | 267 ms: 1.06x slower                                                     |
| comprehensions             | 16.5 us                                                      | 17.5 us: 1.07x slower                                                    |
| regex_v8                   | 22.7 ms                                                      | 24.3 ms: 1.07x slower                                                    |
| pickle_pure_python         | 294 us                                                       | 322 us: 1.09x slower                                                     |
| json_dumps                 | 10.5 ms                                                      | 11.5 ms: 1.10x slower                                                    |
| nbody                      | 85.1 ms                                                      | 95.4 ms: 1.12x slower                                                    |
| bench_thread_pool          | 919 us                                                       | 1.03 ms: 1.12x slower                                                    |
| create_gc_cycles           | 1.34 ms                                                      | 1.71 ms: 1.28x slower                                                    |
| python_startup             | 11.0 ms                                                      | 14.6 ms: 1.33x slower                                                    |
| gc_traversal               | 3.14 ms                                                      | 4.29 ms: 1.37x slower                                                    |
| bench_mp_pool              | 11.0 ms                                                      | 85.5 ms: 7.77x slower                                                    |
| Geometric mean             | (ref)                                                        | 1.00x slower                                                             |

Benchmark hidden because not significant (9): logging_format, scimark_sor, pyflate, xml_etree_generate, mdp, spectral_norm, generators, scimark_monte_carlo, nqueens
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241217-3.14.0a2+-3aa9426/bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-3aa9426.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.022x faster

# HPT report

- Reliability score: 97.48% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.10x