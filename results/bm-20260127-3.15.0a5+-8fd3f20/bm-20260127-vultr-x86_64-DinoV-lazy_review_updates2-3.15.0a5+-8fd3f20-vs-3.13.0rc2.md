# Results vs. 3.13.0rc2

- fork: DinoV
- ref: lazy_review_updates2
- machine: linux-x86_64
- commit hash: 8fd3f20
- commit date: 2026-01-27
- overall geometric mean: 1.038x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260127-vultr-x86_64-DinoV-lazy_review_updates2-3.15.0a5+-8fd3f20 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 249 ms: 1.04x faster                                                  |
| docutils       | 2.62 sec                                                     | 2.58 sec: 1.02x faster                                                |
| html5lib       | 67.0 ms                                                      | 61.3 ms: 1.09x faster                                                 |
| Geometric mean | (ref)                                                        | 1.05x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260127-vultr-x86_64-DinoV-lazy_review_updates2-3.15.0a5+-8fd3f20 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 566 ms: 1.61x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 300 ms: 1.54x faster                                                  |
| async_tree_io              | 876 ms                                                       | 574 ms: 1.53x faster                                                  |
| async_tree_none            | 354 ms                                                       | 248 ms: 1.42x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 295 ms: 1.41x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 483 ms: 1.38x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 246 ms: 1.37x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 486 ms: 1.31x faster                                                  |
| async_generators           | 377 ms                                                       | 342 ms: 1.10x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 23.8 ms: 1.01x slower                                                 |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.31x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260127-vultr-x86_64-DinoV-lazy_review_updates2-3.15.0a5+-8fd3f20 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 193 ms: 1.12x faster                                                  |
| float          | 77.5 ms                                                      | 70.0 ms: 1.11x faster                                                 |
| nbody          | 85.1 ms                                                      | 91.0 ms: 1.07x slower                                                 |
| Geometric mean | (ref)                                                        | 1.05x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260127-vultr-x86_64-DinoV-lazy_review_updates2-3.15.0a5+-8fd3f20 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 132 ms                                                       | 123 ms: 1.08x faster                                                  |
| regex_effbot   | 3.08 ms                                                      | 2.93 ms: 1.05x faster                                                 |
| regex_v8       | 22.7 ms                                                      | 21.8 ms: 1.04x faster                                                 |
| regex_dna      | 180 ms                                                       | 179 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                        | 1.04x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260127-vultr-x86_64-DinoV-lazy_review_updates2-3.15.0a5+-8fd3f20 |
|---------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse | 94.9 ms                                                      | 84.8 ms: 1.12x faster                                                 |
| tomli_loads         | 2.01 sec                                                     | 1.83 sec: 1.09x faster                                                |
| json_dumps          | 10.5 ms                                                      | 9.84 ms: 1.07x faster                                                 |
| xml_etree_parse     | 136 ms                                                       | 131 ms: 1.04x faster                                                  |
| xml_etree_generate  | 85.4 ms                                                      | 83.4 ms: 1.02x faster                                                 |
| xml_etree_process   | 59.3 ms                                                      | 58.0 ms: 1.02x faster                                                 |
| pickle_pure_python  | 294 us                                                       | 305 us: 1.04x slower                                                  |
| json_loads          | 27.0 us                                                      | 28.3 us: 1.05x slower                                                 |
| Geometric mean      | (ref)                                                        | 1.03x faster                                                          |

Benchmark hidden because not significant (1): unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260127-vultr-x86_64-DinoV-lazy_review_updates2-3.15.0a5+-8fd3f20 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.34 ms: 1.01x faster                                                 |
| python_startup         | 11.0 ms                                                      | 12.5 ms: 1.14x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.06x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260127-vultr-x86_64-DinoV-lazy_review_updates2-3.15.0a5+-8fd3f20 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 49.2 ms: 1.01x slower                                                 |
| django_template | 34.1 ms                                                      | 35.1 ms: 1.03x slower                                                 |
| mako            | 11.3 ms                                                      | 11.8 ms: 1.04x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.02x slower                                                          |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260127-vultr-x86_64-DinoV-lazy_review_updates2-3.15.0a5+-8fd3f20 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.16 sec: 2.02x faster                                                |
| async_tree_io_tg           | 913 ms                                                       | 566 ms: 1.61x faster                                                  |
| deepcopy                   | 355 us                                                       | 229 us: 1.56x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 300 ms: 1.54x faster                                                  |
| async_tree_io              | 876 ms                                                       | 574 ms: 1.53x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 26.5 us: 1.48x faster                                                 |
| async_tree_none            | 354 ms                                                       | 248 ms: 1.42x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 295 ms: 1.41x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 483 ms: 1.38x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 246 ms: 1.37x faster                                                  |
| go                         | 141 ms                                                       | 106 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 486 ms: 1.31x faster                                                  |
| scimark_sor                | 134 ms                                                       | 106 ms: 1.27x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.54 us: 1.23x faster                                                 |
| scimark_fft                | 349 ms                                                       | 300 ms: 1.16x faster                                                  |
| spectral_norm              | 111 ms                                                       | 96.9 ms: 1.15x faster                                                 |
| pidigits                   | 217 ms                                                       | 193 ms: 1.12x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 84.8 ms: 1.12x faster                                                 |
| float                      | 77.5 ms                                                      | 70.0 ms: 1.11x faster                                                 |
| pylint                     | 317 ms                                                       | 287 ms: 1.10x faster                                                  |
| async_generators           | 377 ms                                                       | 342 ms: 1.10x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 68.3 ms: 1.10x faster                                                 |
| tomli_loads                | 2.01 sec                                                     | 1.83 sec: 1.09x faster                                                |
| html5lib                   | 67.0 ms                                                      | 61.3 ms: 1.09x faster                                                 |
| pyflate                    | 449 ms                                                       | 411 ms: 1.09x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 17.7 ms: 1.09x faster                                                 |
| regex_compile              | 132 ms                                                       | 123 ms: 1.08x faster                                                  |
| json_dumps                 | 10.5 ms                                                      | 9.84 ms: 1.07x faster                                                 |
| hexiom                     | 5.99 ms                                                      | 5.65 ms: 1.06x faster                                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 61.6 ms: 1.06x faster                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.21 sec: 1.06x faster                                                |
| regex_effbot               | 3.08 ms                                                      | 2.93 ms: 1.05x faster                                                 |
| richards                   | 45.2 ms                                                      | 43.0 ms: 1.05x faster                                                 |
| pprint_safe_repr           | 738 ms                                                       | 706 ms: 1.05x faster                                                  |
| sympy_integrate            | 19.8 ms                                                      | 19.0 ms: 1.04x faster                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.51 ms: 1.04x faster                                                 |
| 2to3                       | 260 ms                                                       | 249 ms: 1.04x faster                                                  |
| scimark_lu                 | 113 ms                                                       | 108 ms: 1.04x faster                                                  |
| regex_v8                   | 22.7 ms                                                      | 21.8 ms: 1.04x faster                                                 |
| pprint_pformat             | 1.50 sec                                                     | 1.44 sec: 1.04x faster                                                |
| richards_super             | 51.6 ms                                                      | 49.7 ms: 1.04x faster                                                 |
| xml_etree_parse            | 136 ms                                                       | 131 ms: 1.04x faster                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 83.4 ms: 1.02x faster                                                 |
| comprehensions             | 16.5 us                                                      | 16.1 us: 1.02x faster                                                 |
| xml_etree_process          | 59.3 ms                                                      | 58.0 ms: 1.02x faster                                                 |
| chaos                      | 57.3 ms                                                      | 56.1 ms: 1.02x faster                                                 |
| pycparser                  | 1.12 sec                                                     | 1.10 sec: 1.02x faster                                                |
| logging_simple             | 6.16 us                                                      | 6.05 us: 1.02x faster                                                 |
| docutils                   | 2.62 sec                                                     | 2.58 sec: 1.02x faster                                                |
| generators                 | 28.8 ms                                                      | 28.4 ms: 1.01x faster                                                 |
| coverage                   | 83.0 ms                                                      | 82.0 ms: 1.01x faster                                                 |
| logging_silent             | 103 ns                                                       | 101 ns: 1.01x faster                                                  |
| logging_format             | 6.84 us                                                      | 6.76 us: 1.01x faster                                                 |
| thrift                     | 778 us                                                       | 772 us: 1.01x faster                                                  |
| meteor_contest             | 102 ms                                                       | 101 ms: 1.01x faster                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 7.34 ms: 1.01x faster                                                 |
| regex_dna                  | 180 ms                                                       | 179 ms: 1.01x faster                                                  |
| raytrace                   | 253 ms                                                       | 251 ms: 1.01x faster                                                  |
| sympy_str                  | 275 ms                                                       | 276 ms: 1.01x slower                                                  |
| genshi_xml                 | 48.8 ms                                                      | 49.2 ms: 1.01x slower                                                 |
| coroutines                 | 23.6 ms                                                      | 23.8 ms: 1.01x slower                                                 |
| json                       | 4.93 ms                                                      | 4.99 ms: 1.01x slower                                                 |
| sqlite_synth               | 2.21 us                                                      | 2.25 us: 1.02x slower                                                 |
| typing_runtime_protocols   | 155 us                                                       | 158 us: 1.02x slower                                                  |
| django_template            | 34.1 ms                                                      | 35.1 ms: 1.03x slower                                                 |
| fannkuch                   | 370 ms                                                       | 382 ms: 1.03x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 305 us: 1.04x slower                                                  |
| mako                       | 11.3 ms                                                      | 11.8 ms: 1.04x slower                                                 |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                  |
| json_loads                 | 27.0 us                                                      | 28.3 us: 1.05x slower                                                 |
| deltablue                  | 3.12 ms                                                      | 3.28 ms: 1.05x slower                                                 |
| nbody                      | 85.1 ms                                                      | 91.0 ms: 1.07x slower                                                 |
| sympy_expand               | 457 ms                                                       | 493 ms: 1.08x slower                                                  |
| python_startup             | 11.0 ms                                                      | 12.5 ms: 1.14x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.87 ms: 1.40x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 4.42 ms: 1.41x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 1.32 ms: 1.44x slower                                                 |
| telco                      | 7.82 ms                                                      | 160 ms: 20.51x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 269 ms: 24.47x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.00x slower                                                          |

Benchmark hidden because not significant (5): genshi_text, unpickle_pure_python, sympy_sum, crypto_pyaes, nqueens
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260127-3.15.0a5+-8fd3f20/bm-20260127-vultr-x86_64-DinoV-lazy_review_updates2-3.15.0a5+-8fd3f20.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.038x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.16x