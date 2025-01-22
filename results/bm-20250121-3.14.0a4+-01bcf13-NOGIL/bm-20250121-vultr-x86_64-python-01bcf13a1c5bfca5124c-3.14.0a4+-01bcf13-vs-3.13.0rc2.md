# Results vs. 3.13.0rc2

- fork: python
- ref: 01bcf13a1c5bfca5124c
- machine: linux-x86_64
- commit hash: 01bcf13
- commit date: 2025-01-21
- overall geometric mean: 1.105x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 311 ms: 1.20x slower                                                   |
| docutils       | 2.62 sec                                                     | 2.84 sec: 1.09x slower                                                 |
| html5lib       | 67.0 ms                                                      | 74.5 ms: 1.11x slower                                                  |
| Geometric mean | (ref)                                                        | 1.13x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 582 ms: 1.57x faster                                                   |
| async_tree_io              | 876 ms                                                       | 613 ms: 1.43x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 245 ms: 1.37x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 317 ms: 1.31x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 353 ms: 1.31x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 498 ms: 1.28x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 532 ms: 1.25x faster                                                   |
| async_tree_none            | 354 ms                                                       | 287 ms: 1.23x faster                                                   |
| async_generators           | 377 ms                                                       | 374 ms: 1.01x faster                                                   |
| asyncio_websockets         | 520 ms                                                       | 518 ms: 1.00x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 24.9 ms: 1.06x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.23x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 191 ms: 1.14x faster                                                   |
| float          | 77.5 ms                                                      | 78.0 ms: 1.01x slower                                                  |
| nbody          | 85.1 ms                                                      | 138 ms: 1.62x slower                                                   |
| Geometric mean | (ref)                                                        | 1.13x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.80 ms: 1.10x faster                                                  |
| regex_dna      | 180 ms                                                       | 182 ms: 1.01x slower                                                   |
| regex_v8       | 22.7 ms                                                      | 23.4 ms: 1.03x slower                                                  |
| regex_compile  | 132 ms                                                       | 159 ms: 1.20x slower                                                   |
| Geometric mean | (ref)                                                        | 1.03x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 88.6 ms: 1.07x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 128 ms: 1.07x faster                                                   |
| json_loads           | 27.0 us                                                      | 30.4 us: 1.13x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 98.6 ms: 1.15x slower                                                  |
| tomli_loads          | 2.01 sec                                                     | 2.42 sec: 1.20x slower                                                 |
| json_dumps           | 10.5 ms                                                      | 13.0 ms: 1.23x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 74.7 ms: 1.26x slower                                                  |
| unpickle_pure_python | 210 us                                                       | 274 us: 1.30x slower                                                   |
| pickle_pure_python   | 294 us                                                       | 392 us: 1.33x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.16x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.59 ms: 1.30x slower                                                  |
| python_startup         | 11.0 ms                                                      | 15.3 ms: 1.39x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.35x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 63.1 ms: 1.29x slower                                                  |
| django_template | 34.1 ms                                                      | 44.8 ms: 1.31x slower                                                  |
| genshi_text     | 21.5 ms                                                      | 29.7 ms: 1.38x slower                                                  |
| mako            | 11.3 ms                                                      | 16.1 ms: 1.42x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.35x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 582 ms: 1.57x faster                                                   |
| async_tree_io              | 876 ms                                                       | 613 ms: 1.43x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 245 ms: 1.37x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 317 ms: 1.31x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 353 ms: 1.31x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 498 ms: 1.28x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 532 ms: 1.25x faster                                                   |
| async_tree_none            | 354 ms                                                       | 287 ms: 1.23x faster                                                   |
| pidigits                   | 217 ms                                                       | 191 ms: 1.14x faster                                                   |
| regex_effbot               | 3.08 ms                                                      | 2.80 ms: 1.10x faster                                                  |
| deepcopy                   | 355 us                                                       | 324 us: 1.10x faster                                                   |
| sqlite_synth               | 2.21 us                                                      | 2.06 us: 1.07x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 88.6 ms: 1.07x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 128 ms: 1.07x faster                                                   |
| pathlib                    | 19.2 ms                                                      | 18.6 ms: 1.03x faster                                                  |
| async_generators           | 377 ms                                                       | 374 ms: 1.01x faster                                                   |
| asyncio_websockets         | 520 ms                                                       | 518 ms: 1.00x faster                                                   |
| gc_traversal               | 3.14 ms                                                      | 3.13 ms: 1.00x faster                                                  |
| float                      | 77.5 ms                                                      | 78.0 ms: 1.01x slower                                                  |
| regex_dna                  | 180 ms                                                       | 182 ms: 1.01x slower                                                   |
| go                         | 141 ms                                                       | 143 ms: 1.02x slower                                                   |
| deepcopy_memo              | 39.1 us                                                      | 40.0 us: 1.02x slower                                                  |
| spectral_norm              | 111 ms                                                       | 114 ms: 1.03x slower                                                   |
| scimark_sor                | 134 ms                                                       | 139 ms: 1.03x slower                                                   |
| regex_v8                   | 22.7 ms                                                      | 23.4 ms: 1.03x slower                                                  |
| coroutines                 | 23.6 ms                                                      | 24.9 ms: 1.06x slower                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.81 sec: 1.08x slower                                                 |
| docutils                   | 2.62 sec                                                     | 2.84 sec: 1.09x slower                                                 |
| deepcopy_reduce            | 3.11 us                                                      | 3.40 us: 1.09x slower                                                  |
| json                       | 4.93 ms                                                      | 5.39 ms: 1.09x slower                                                  |
| pycparser                  | 1.12 sec                                                     | 1.22 sec: 1.10x slower                                                 |
| telco                      | 7.82 ms                                                      | 8.62 ms: 1.10x slower                                                  |
| html5lib                   | 67.0 ms                                                      | 74.5 ms: 1.11x slower                                                  |
| json_loads                 | 27.0 us                                                      | 30.4 us: 1.13x slower                                                  |
| dulwich_log                | 74.8 ms                                                      | 84.4 ms: 1.13x slower                                                  |
| scimark_fft                | 349 ms                                                       | 398 ms: 1.14x slower                                                   |
| pprint_safe_repr           | 738 ms                                                       | 848 ms: 1.15x slower                                                   |
| pyflate                    | 449 ms                                                       | 517 ms: 1.15x slower                                                   |
| xml_etree_generate         | 85.4 ms                                                      | 98.6 ms: 1.15x slower                                                  |
| generators                 | 28.8 ms                                                      | 33.4 ms: 1.16x slower                                                  |
| mdp                        | 2.36 sec                                                     | 2.74 sec: 1.16x slower                                                 |
| pprint_pformat             | 1.50 sec                                                     | 1.75 sec: 1.17x slower                                                 |
| sqlglot_normalize          | 106 ms                                                       | 123 ms: 1.17x slower                                                   |
| logging_silent             | 103 ns                                                       | 121 ns: 1.18x slower                                                   |
| sqlglot_optimize           | 52.7 ms                                                      | 62.3 ms: 1.18x slower                                                  |
| thrift                     | 778 us                                                       | 927 us: 1.19x slower                                                   |
| coverage                   | 83.0 ms                                                      | 99.3 ms: 1.20x slower                                                  |
| 2to3                       | 260 ms                                                       | 311 ms: 1.20x slower                                                   |
| regex_compile              | 132 ms                                                       | 159 ms: 1.20x slower                                                   |
| tomli_loads                | 2.01 sec                                                     | 2.42 sec: 1.20x slower                                                 |
| sympy_sum                  | 156 ms                                                       | 191 ms: 1.23x slower                                                   |
| json_dumps                 | 10.5 ms                                                      | 13.0 ms: 1.23x slower                                                  |
| richards                   | 45.2 ms                                                      | 55.9 ms: 1.24x slower                                                  |
| sympy_expand               | 457 ms                                                       | 567 ms: 1.24x slower                                                   |
| chaos                      | 57.3 ms                                                      | 71.1 ms: 1.24x slower                                                  |
| sympy_integrate            | 19.8 ms                                                      | 24.7 ms: 1.25x slower                                                  |
| sympy_str                  | 275 ms                                                       | 344 ms: 1.25x slower                                                   |
| logging_simple             | 6.16 us                                                      | 7.72 us: 1.25x slower                                                  |
| scimark_lu                 | 113 ms                                                       | 142 ms: 1.26x slower                                                   |
| xml_etree_process          | 59.3 ms                                                      | 74.7 ms: 1.26x slower                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.93 ms: 1.26x slower                                                  |
| richards_super             | 51.6 ms                                                      | 65.1 ms: 1.26x slower                                                  |
| nqueens                    | 78.6 ms                                                      | 99.3 ms: 1.26x slower                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 83.0 ms: 1.27x slower                                                  |
| logging_format             | 6.84 us                                                      | 8.71 us: 1.27x slower                                                  |
| sqlglot_transpile          | 1.56 ms                                                      | 1.99 ms: 1.27x slower                                                  |
| hexiom                     | 5.99 ms                                                      | 7.64 ms: 1.27x slower                                                  |
| sqlglot_parse              | 1.25 ms                                                      | 1.60 ms: 1.28x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 87.6 ms: 1.29x slower                                                  |
| genshi_xml                 | 48.8 ms                                                      | 63.1 ms: 1.29x slower                                                  |
| meteor_contest             | 102 ms                                                       | 132 ms: 1.29x slower                                                   |
| python_startup_no_site     | 7.39 ms                                                      | 9.59 ms: 1.30x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 274 us: 1.30x slower                                                   |
| comprehensions             | 16.5 us                                                      | 21.5 us: 1.31x slower                                                  |
| django_template            | 34.1 ms                                                      | 44.8 ms: 1.31x slower                                                  |
| raytrace                   | 253 ms                                                       | 337 ms: 1.33x slower                                                   |
| pickle_pure_python         | 294 us                                                       | 392 us: 1.33x slower                                                   |
| fannkuch                   | 370 ms                                                       | 495 ms: 1.34x slower                                                   |
| typing_runtime_protocols   | 155 us                                                       | 212 us: 1.37x slower                                                   |
| genshi_text                | 21.5 ms                                                      | 29.7 ms: 1.38x slower                                                  |
| python_startup             | 11.0 ms                                                      | 15.3 ms: 1.39x slower                                                  |
| mako                       | 11.3 ms                                                      | 16.1 ms: 1.42x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 4.73 ms: 1.52x slower                                                  |
| nbody                      | 85.1 ms                                                      | 138 ms: 1.62x slower                                                   |
| bench_thread_pool          | 919 us                                                       | 3.35 ms: 3.64x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 95.7 ms: 8.71x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.16x slower                                                           |

Benchmark hidden because not significant (2): create_gc_cycles, pylint
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250121-3.14.0a4+-01bcf13-NOGIL/bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.105x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 1.33x