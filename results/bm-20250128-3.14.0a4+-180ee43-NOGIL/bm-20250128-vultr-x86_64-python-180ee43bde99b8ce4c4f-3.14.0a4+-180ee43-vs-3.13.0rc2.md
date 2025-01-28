# Results vs. 3.13.0rc2

- fork: python
- ref: 180ee43bde99b8ce4c4f
- machine: linux-x86_64
- commit hash: 180ee43
- commit date: 2025-01-28
- overall geometric mean: 1.108x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-vultr-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 313 ms: 1.21x slower                                                   |
| docutils       | 2.62 sec                                                     | 2.87 sec: 1.10x slower                                                 |
| html5lib       | 67.0 ms                                                      | 72.3 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                        | 1.13x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-vultr-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 590 ms: 1.55x faster                                                   |
| async_tree_io              | 876 ms                                                       | 619 ms: 1.41x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 256 ms: 1.31x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 362 ms: 1.28x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 327 ms: 1.27x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 514 ms: 1.24x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 547 ms: 1.22x faster                                                   |
| async_tree_none            | 354 ms                                                       | 296 ms: 1.20x faster                                                   |
| asyncio_websockets         | 520 ms                                                       | 518 ms: 1.00x faster                                                   |
| async_generators           | 377 ms                                                       | 378 ms: 1.00x slower                                                   |
| coroutines                 | 23.6 ms                                                      | 24.8 ms: 1.05x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.21x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-vultr-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 191 ms: 1.14x faster                                                   |
| float          | 77.5 ms                                                      | 78.3 ms: 1.01x slower                                                  |
| nbody          | 85.1 ms                                                      | 141 ms: 1.66x slower                                                   |
| Geometric mean | (ref)                                                        | 1.14x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-vultr-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.87 ms: 1.07x faster                                                  |
| regex_dna      | 180 ms                                                       | 185 ms: 1.03x slower                                                   |
| regex_v8       | 22.7 ms                                                      | 24.1 ms: 1.06x slower                                                  |
| regex_compile  | 132 ms                                                       | 157 ms: 1.19x slower                                                   |
| Geometric mean | (ref)                                                        | 1.05x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-vultr-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 88.1 ms: 1.08x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 129 ms: 1.06x faster                                                   |
| xml_etree_generate   | 85.4 ms                                                      | 98.2 ms: 1.15x slower                                                  |
| json_loads           | 27.0 us                                                      | 31.4 us: 1.16x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 71.2 ms: 1.20x slower                                                  |
| tomli_loads          | 2.01 sec                                                     | 2.42 sec: 1.21x slower                                                 |
| unpickle_pure_python | 210 us                                                       | 258 us: 1.23x slower                                                   |
| json_dumps           | 10.5 ms                                                      | 13.1 ms: 1.24x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 387 us: 1.31x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.15x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-vultr-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.55 ms: 1.29x slower                                                  |
| python_startup         | 11.0 ms                                                      | 15.2 ms: 1.38x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.34x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-vultr-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 62.6 ms: 1.28x slower                                                  |
| django_template | 34.1 ms                                                      | 45.1 ms: 1.32x slower                                                  |
| genshi_text     | 21.5 ms                                                      | 28.7 ms: 1.33x slower                                                  |
| mako            | 11.3 ms                                                      | 16.3 ms: 1.43x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.34x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-vultr-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 590 ms: 1.55x faster                                                   |
| async_tree_io              | 876 ms                                                       | 619 ms: 1.41x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 256 ms: 1.31x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 362 ms: 1.28x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 327 ms: 1.27x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 514 ms: 1.24x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 547 ms: 1.22x faster                                                   |
| async_tree_none            | 354 ms                                                       | 296 ms: 1.20x faster                                                   |
| pidigits                   | 217 ms                                                       | 191 ms: 1.14x faster                                                   |
| deepcopy                   | 355 us                                                       | 324 us: 1.10x faster                                                   |
| xml_etree_iterparse        | 94.9 ms                                                      | 88.1 ms: 1.08x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.87 ms: 1.07x faster                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.06 us: 1.07x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 129 ms: 1.06x faster                                                   |
| create_gc_cycles           | 1.34 ms                                                      | 1.32 ms: 1.01x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 19.1 ms: 1.01x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 518 ms: 1.00x faster                                                   |
| async_generators           | 377 ms                                                       | 378 ms: 1.00x slower                                                   |
| deepcopy_memo              | 39.1 us                                                      | 39.5 us: 1.01x slower                                                  |
| float                      | 77.5 ms                                                      | 78.3 ms: 1.01x slower                                                  |
| go                         | 141 ms                                                       | 144 ms: 1.02x slower                                                   |
| regex_dna                  | 180 ms                                                       | 185 ms: 1.03x slower                                                   |
| spectral_norm              | 111 ms                                                       | 114 ms: 1.03x slower                                                   |
| scimark_sor                | 134 ms                                                       | 140 ms: 1.04x slower                                                   |
| coroutines                 | 23.6 ms                                                      | 24.8 ms: 1.05x slower                                                  |
| regex_v8                   | 22.7 ms                                                      | 24.1 ms: 1.06x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 3.35 ms: 1.06x slower                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.76 sec: 1.07x slower                                                 |
| html5lib                   | 67.0 ms                                                      | 72.3 ms: 1.08x slower                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 3.38 us: 1.09x slower                                                  |
| json                       | 4.93 ms                                                      | 5.37 ms: 1.09x slower                                                  |
| docutils                   | 2.62 sec                                                     | 2.87 sec: 1.10x slower                                                 |
| pycparser                  | 1.12 sec                                                     | 1.23 sec: 1.10x slower                                                 |
| telco                      | 7.82 ms                                                      | 8.64 ms: 1.10x slower                                                  |
| pyflate                    | 449 ms                                                       | 504 ms: 1.12x slower                                                   |
| dulwich_log                | 74.8 ms                                                      | 84.2 ms: 1.13x slower                                                  |
| scimark_fft                | 349 ms                                                       | 399 ms: 1.14x slower                                                   |
| logging_silent             | 103 ns                                                       | 118 ns: 1.15x slower                                                   |
| xml_etree_generate         | 85.4 ms                                                      | 98.2 ms: 1.15x slower                                                  |
| generators                 | 28.8 ms                                                      | 33.4 ms: 1.16x slower                                                  |
| mdp                        | 2.36 sec                                                     | 2.73 sec: 1.16x slower                                                 |
| json_loads                 | 27.0 us                                                      | 31.4 us: 1.16x slower                                                  |
| pprint_safe_repr           | 738 ms                                                       | 861 ms: 1.17x slower                                                   |
| sqlglot_normalize          | 106 ms                                                       | 125 ms: 1.18x slower                                                   |
| thrift                     | 778 us                                                       | 920 us: 1.18x slower                                                   |
| pprint_pformat             | 1.50 sec                                                     | 1.77 sec: 1.19x slower                                                 |
| regex_compile              | 132 ms                                                       | 157 ms: 1.19x slower                                                   |
| coverage                   | 83.0 ms                                                      | 99.0 ms: 1.19x slower                                                  |
| sqlglot_optimize           | 52.7 ms                                                      | 63.1 ms: 1.20x slower                                                  |
| xml_etree_process          | 59.3 ms                                                      | 71.2 ms: 1.20x slower                                                  |
| 2to3                       | 260 ms                                                       | 313 ms: 1.21x slower                                                   |
| tomli_loads                | 2.01 sec                                                     | 2.42 sec: 1.21x slower                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.70 ms: 1.21x slower                                                  |
| logging_simple             | 6.16 us                                                      | 7.47 us: 1.21x slower                                                  |
| sympy_sum                  | 156 ms                                                       | 190 ms: 1.22x slower                                                   |
| unpickle_pure_python       | 210 us                                                       | 258 us: 1.23x slower                                                   |
| sympy_expand               | 457 ms                                                       | 565 ms: 1.24x slower                                                   |
| nqueens                    | 78.6 ms                                                      | 97.6 ms: 1.24x slower                                                  |
| json_dumps                 | 10.5 ms                                                      | 13.1 ms: 1.24x slower                                                  |
| sympy_integrate            | 19.8 ms                                                      | 24.7 ms: 1.25x slower                                                  |
| sympy_str                  | 275 ms                                                       | 343 ms: 1.25x slower                                                   |
| logging_format             | 6.84 us                                                      | 8.54 us: 1.25x slower                                                  |
| chaos                      | 57.3 ms                                                      | 72.0 ms: 1.26x slower                                                  |
| sqlglot_transpile          | 1.56 ms                                                      | 1.97 ms: 1.26x slower                                                  |
| scimark_lu                 | 113 ms                                                       | 143 ms: 1.27x slower                                                   |
| hexiom                     | 5.99 ms                                                      | 7.62 ms: 1.27x slower                                                  |
| genshi_xml                 | 48.8 ms                                                      | 62.6 ms: 1.28x slower                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 9.55 ms: 1.29x slower                                                  |
| comprehensions             | 16.5 us                                                      | 21.3 us: 1.29x slower                                                  |
| meteor_contest             | 102 ms                                                       | 132 ms: 1.30x slower                                                   |
| richards                   | 45.2 ms                                                      | 58.8 ms: 1.30x slower                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 85.3 ms: 1.30x slower                                                  |
| sqlglot_parse              | 1.25 ms                                                      | 1.64 ms: 1.31x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 387 us: 1.31x slower                                                   |
| richards_super             | 51.6 ms                                                      | 68.0 ms: 1.32x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 89.6 ms: 1.32x slower                                                  |
| django_template            | 34.1 ms                                                      | 45.1 ms: 1.32x slower                                                  |
| fannkuch                   | 370 ms                                                       | 491 ms: 1.33x slower                                                   |
| genshi_text                | 21.5 ms                                                      | 28.7 ms: 1.33x slower                                                  |
| typing_runtime_protocols   | 155 us                                                       | 207 us: 1.34x slower                                                   |
| raytrace                   | 253 ms                                                       | 340 ms: 1.35x slower                                                   |
| python_startup             | 11.0 ms                                                      | 15.2 ms: 1.38x slower                                                  |
| mako                       | 11.3 ms                                                      | 16.3 ms: 1.43x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 4.79 ms: 1.53x slower                                                  |
| nbody                      | 85.1 ms                                                      | 141 ms: 1.66x slower                                                   |
| bench_thread_pool          | 919 us                                                       | 3.34 ms: 3.63x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 95.1 ms: 8.65x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.16x slower                                                           |

Benchmark hidden because not significant (1): pylint
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250128-3.14.0a4+-180ee43-NOGIL/bm-20250128-vultr-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.108x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.10x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 1.33x