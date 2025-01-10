# Results vs. 3.12.6

- fork: Yhg1s
- ref: list_realloc
- machine: linux-x86_64
- commit hash: 89c4629
- commit date: 2025-01-09
- overall geometric mean: 1.162x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.12x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250109-vultr-x86_64-Yhg1s-list_realloc-3.14.0a3+-89c4629 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 346 ms: 1.31x slower                                          |
| docutils       | 2.64 sec                                               | 3.01 sec: 1.14x slower                                        |
| html5lib       | 63.6 ms                                                | 90.3 ms: 1.42x slower                                         |
| Geometric mean | (ref)                                                  | 1.29x slower                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250109-vultr-x86_64-Yhg1s-list_realloc-3.14.0a3+-89c4629 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 737 ms: 1.51x faster                                          |
| async_tree_io              | 1.08 sec                                               | 759 ms: 1.43x faster                                          |
| async_tree_none_tg         | 446 ms                                                 | 316 ms: 1.41x faster                                          |
| async_tree_memoization_tg  | 560 ms                                                 | 397 ms: 1.41x faster                                          |
| async_tree_none            | 464 ms                                                 | 351 ms: 1.32x faster                                          |
| async_tree_memoization     | 555 ms                                                 | 430 ms: 1.29x faster                                          |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 566 ms: 1.28x faster                                          |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 595 ms: 1.20x faster                                          |
| coroutines                 | 23.9 ms                                                | 23.2 ms: 1.03x faster                                         |
| asyncio_websockets         | 517 ms                                                 | 518 ms: 1.00x slower                                          |
| async_generators           | 384 ms                                                 | 446 ms: 1.16x slower                                          |
| Geometric mean             | (ref)                                                  | 1.23x faster                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250109-vultr-x86_64-Yhg1s-list_realloc-3.14.0a3+-89c4629 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 184 ms: 1.00x faster                                          |
| float          | 80.8 ms                                                | 106 ms: 1.31x slower                                          |
| nbody          | 89.3 ms                                                | 130 ms: 1.45x slower                                          |
| Geometric mean | (ref)                                                  | 1.24x slower                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250109-vultr-x86_64-Yhg1s-list_realloc-3.14.0a3+-89c4629 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.85 ms: 1.11x faster                                         |
| regex_dna      | 168 ms                                                 | 187 ms: 1.11x slower                                          |
| regex_compile  | 142 ms                                                 | 167 ms: 1.17x slower                                          |
| regex_v8       | 20.6 ms                                                | 25.4 ms: 1.23x slower                                         |
| Geometric mean | (ref)                                                  | 1.10x slower                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250109-vultr-x86_64-Yhg1s-list_realloc-3.14.0a3+-89c4629 |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 89.3 ms: 1.08x faster                                         |
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.08x faster                                          |
| json_loads           | 26.5 us                                                | 28.6 us: 1.08x slower                                         |
| tomli_loads          | 2.11 sec                                               | 2.37 sec: 1.12x slower                                        |
| xml_etree_generate   | 85.2 ms                                                | 98.3 ms: 1.15x slower                                         |
| xml_etree_process    | 59.0 ms                                                | 74.1 ms: 1.26x slower                                         |
| json_dumps           | 10.4 ms                                                | 13.9 ms: 1.34x slower                                         |
| unpickle_pure_python | 221 us                                                 | 324 us: 1.47x slower                                          |
| pickle_pure_python   | 308 us                                                 | 486 us: 1.58x slower                                          |
| Geometric mean       | (ref)                                                  | 1.19x slower                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250109-vultr-x86_64-Yhg1s-list_realloc-3.14.0a3+-89c4629 |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.79 ms: 1.37x slower                                         |
| python_startup         | 9.93 ms                                                | 15.6 ms: 1.58x slower                                         |
| Geometric mean         | (ref)                                                  | 1.47x slower                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250109-vultr-x86_64-Yhg1s-list_realloc-3.14.0a3+-89c4629 |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 63.2 ms: 1.26x slower                                         |
| genshi_text     | 22.8 ms                                                | 30.4 ms: 1.33x slower                                         |
| django_template | 34.7 ms                                                | 49.7 ms: 1.43x slower                                         |
| mako            | 11.0 ms                                                | 17.0 ms: 1.55x slower                                         |
| Geometric mean  | (ref)                                                  | 1.39x slower                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250109-vultr-x86_64-Yhg1s-list_realloc-3.14.0a3+-89c4629 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 737 ms: 1.51x faster                                          |
| async_tree_io              | 1.08 sec                                               | 759 ms: 1.43x faster                                          |
| async_tree_none_tg         | 446 ms                                                 | 316 ms: 1.41x faster                                          |
| async_tree_memoization_tg  | 560 ms                                                 | 397 ms: 1.41x faster                                          |
| async_tree_none            | 464 ms                                                 | 351 ms: 1.32x faster                                          |
| async_tree_memoization     | 555 ms                                                 | 430 ms: 1.29x faster                                          |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 566 ms: 1.28x faster                                          |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 595 ms: 1.20x faster                                          |
| regex_effbot               | 3.17 ms                                                | 2.85 ms: 1.11x faster                                         |
| pathlib                    | 21.5 ms                                                | 19.5 ms: 1.11x faster                                         |
| deepcopy                   | 352 us                                                 | 325 us: 1.08x faster                                          |
| xml_etree_iterparse        | 96.7 ms                                                | 89.3 ms: 1.08x faster                                         |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.08x faster                                          |
| gc_traversal               | 3.46 ms                                                | 3.29 ms: 1.05x faster                                         |
| sqlite_synth               | 2.20 us                                                | 2.11 us: 1.05x faster                                         |
| coroutines                 | 23.9 ms                                                | 23.2 ms: 1.03x faster                                         |
| pidigits                   | 184 ms                                                 | 184 ms: 1.00x faster                                          |
| asyncio_websockets         | 517 ms                                                 | 518 ms: 1.00x slower                                          |
| deepcopy_memo              | 40.3 us                                                | 40.6 us: 1.01x slower                                         |
| json                       | 5.02 ms                                                | 5.09 ms: 1.01x slower                                         |
| bpe_tokeniser              | 4.74 sec                                               | 4.93 sec: 1.04x slower                                        |
| json_loads                 | 26.5 us                                                | 28.6 us: 1.08x slower                                         |
| pylint                     | 319 ms                                                 | 343 ms: 1.08x slower                                          |
| deepcopy_reduce            | 3.08 us                                                | 3.38 us: 1.10x slower                                         |
| scimark_fft                | 342 ms                                                 | 378 ms: 1.11x slower                                          |
| regex_dna                  | 168 ms                                                 | 187 ms: 1.11x slower                                          |
| tomli_loads                | 2.11 sec                                               | 2.37 sec: 1.12x slower                                        |
| mdp                        | 2.42 sec                                               | 2.73 sec: 1.13x slower                                        |
| docutils                   | 2.64 sec                                               | 3.01 sec: 1.14x slower                                        |
| dulwich_log                | 78.9 ms                                                | 90.4 ms: 1.15x slower                                         |
| xml_etree_generate         | 85.2 ms                                                | 98.3 ms: 1.15x slower                                         |
| pycparser                  | 1.17 sec                                               | 1.35 sec: 1.16x slower                                        |
| async_generators           | 384 ms                                                 | 446 ms: 1.16x slower                                          |
| sympy_sum                  | 166 ms                                                 | 193 ms: 1.16x slower                                          |
| crypto_pyaes               | 76.6 ms                                                | 89.4 ms: 1.17x slower                                         |
| regex_compile              | 142 ms                                                 | 167 ms: 1.17x slower                                          |
| generators                 | 32.2 ms                                                | 38.6 ms: 1.20x slower                                         |
| nqueens                    | 80.1 ms                                                | 96.4 ms: 1.20x slower                                         |
| sympy_str                  | 292 ms                                                 | 353 ms: 1.21x slower                                          |
| sympy_integrate            | 20.5 ms                                                | 25.0 ms: 1.22x slower                                         |
| regex_v8                   | 20.6 ms                                                | 25.4 ms: 1.23x slower                                         |
| sympy_expand               | 468 ms                                                 | 582 ms: 1.24x slower                                          |
| sqlglot_normalize          | 107 ms                                                 | 133 ms: 1.25x slower                                          |
| sqlglot_optimize           | 53.3 ms                                                | 66.9 ms: 1.26x slower                                         |
| xml_etree_process          | 59.0 ms                                                | 74.1 ms: 1.26x slower                                         |
| typing_runtime_protocols   | 163 us                                                 | 205 us: 1.26x slower                                          |
| genshi_xml                 | 50.2 ms                                                | 63.2 ms: 1.26x slower                                         |
| meteor_contest             | 104 ms                                                 | 131 ms: 1.27x slower                                          |
| thrift                     | 791 us                                                 | 1.01 ms: 1.27x slower                                         |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.59 ms: 1.27x slower                                         |
| pprint_safe_repr           | 743 ms                                                 | 946 ms: 1.27x slower                                          |
| sqlalchemy_imperative      | 21.8 ms                                                | 27.8 ms: 1.27x slower                                         |
| sqlalchemy_declarative     | 143 ms                                                 | 183 ms: 1.28x slower                                          |
| pprint_pformat             | 1.52 sec                                               | 1.97 sec: 1.29x slower                                        |
| fannkuch                   | 372 ms                                                 | 484 ms: 1.30x slower                                          |
| float                      | 80.8 ms                                                | 106 ms: 1.31x slower                                          |
| 2to3                       | 264 ms                                                 | 346 ms: 1.31x slower                                          |
| telco                      | 6.53 ms                                                | 8.58 ms: 1.31x slower                                         |
| genshi_text                | 22.8 ms                                                | 30.4 ms: 1.33x slower                                         |
| json_dumps                 | 10.4 ms                                                | 13.9 ms: 1.34x slower                                         |
| logging_simple             | 6.63 us                                                | 8.90 us: 1.34x slower                                         |
| logging_format             | 7.35 us                                                | 9.96 us: 1.36x slower                                         |
| python_startup_no_site     | 7.16 ms                                                | 9.79 ms: 1.37x slower                                         |
| comprehensions             | 19.8 us                                                | 27.3 us: 1.38x slower                                         |
| coverage                   | 71.4 ms                                                | 98.7 ms: 1.38x slower                                         |
| scimark_lu                 | 114 ms                                                 | 160 ms: 1.40x slower                                          |
| pyflate                    | 448 ms                                                 | 632 ms: 1.41x slower                                          |
| richards                   | 45.9 ms                                                | 65.1 ms: 1.42x slower                                         |
| html5lib                   | 63.6 ms                                                | 90.3 ms: 1.42x slower                                         |
| django_template            | 34.7 ms                                                | 49.7 ms: 1.43x slower                                         |
| nbody                      | 89.3 ms                                                | 130 ms: 1.45x slower                                          |
| unpickle_pure_python       | 221 us                                                 | 324 us: 1.47x slower                                          |
| hexiom                     | 6.17 ms                                                | 9.21 ms: 1.49x slower                                         |
| richards_super             | 51.9 ms                                                | 77.5 ms: 1.49x slower                                         |
| scimark_monte_carlo        | 68.4 ms                                                | 103 ms: 1.51x slower                                          |
| chaos                      | 62.8 ms                                                | 95.3 ms: 1.52x slower                                         |
| mako                       | 11.0 ms                                                | 17.0 ms: 1.55x slower                                         |
| scimark_sor                | 130 ms                                                 | 202 ms: 1.56x slower                                          |
| python_startup             | 9.93 ms                                                | 15.6 ms: 1.58x slower                                         |
| pickle_pure_python         | 308 us                                                 | 486 us: 1.58x slower                                          |
| sqlglot_transpile          | 1.67 ms                                                | 2.66 ms: 1.59x slower                                         |
| raytrace                   | 299 ms                                                 | 491 ms: 1.64x slower                                          |
| logging_silent             | 109 ns                                                 | 179 ns: 1.65x slower                                          |
| go                         | 139 ms                                                 | 231 ms: 1.66x slower                                          |
| create_gc_cycles           | 1.09 ms                                                | 1.82 ms: 1.66x slower                                         |
| sqlglot_parse              | 1.36 ms                                                | 2.30 ms: 1.70x slower                                         |
| deltablue                  | 3.45 ms                                                | 7.13 ms: 2.07x slower                                         |
| bench_thread_pool          | 941 us                                                 | 3.38 ms: 3.59x slower                                         |
| bench_mp_pool              | 10.8 ms                                                | 100 ms: 9.28x slower                                          |
| Geometric mean             | (ref)                                                  | 1.24x slower                                                  |

Benchmark hidden because not significant (1): spectral_norm
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250109-3.14.0a3+-89c4629-NOGIL/bm-20250109-vultr-x86_64-Yhg1s-list_realloc-3.14.0a3+-89c4629.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.162x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.15x
- 95% likely to have a slowdown of 1.14x
- 99% likely to have a slowdown of 1.12x

# Memory
- memory change: 1.34x