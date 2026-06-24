# Results vs. 3.12.6

- fork: kumaraditya303
- ref: mrocache
- machine: linux-x86_64
- commit hash: 4fbec93
- commit date: 2026-06-16
- overall geometric mean: 1.043x slower
- HPT reliability: 96.82%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 297 ms: 1.13x slower                                              |
| docutils       | 2.64 sec                                               | 2.93 sec: 1.11x slower                                            |
| html5lib       | 63.6 ms                                                | 68.6 ms: 1.08x slower                                             |
| Geometric mean | (ref)                                                  | 1.11x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 681 ms: 1.63x faster                                              |
| async_tree_io              | 1.08 sec                                               | 709 ms: 1.53x faster                                              |
| async_tree_memoization_tg  | 560 ms                                                 | 394 ms: 1.42x faster                                              |
| async_tree_none_tg         | 446 ms                                                 | 324 ms: 1.38x faster                                              |
| async_tree_none            | 464 ms                                                 | 345 ms: 1.35x faster                                              |
| async_tree_memoization     | 555 ms                                                 | 420 ms: 1.32x faster                                              |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 578 ms: 1.25x faster                                              |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 605 ms: 1.18x faster                                              |
| asyncio_websockets         | 517 ms                                                 | 513 ms: 1.01x faster                                              |
| async_generators           | 384 ms                                                 | 390 ms: 1.02x slower                                              |
| coroutines                 | 23.9 ms                                                | 25.0 ms: 1.05x slower                                             |
| Geometric mean             | (ref)                                                  | 1.26x faster                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 188 ms: 1.02x slower                                              |
| float          | 80.8 ms                                                | 86.9 ms: 1.08x slower                                             |
| nbody          | 89.3 ms                                                | 125 ms: 1.40x slower                                              |
| Geometric mean | (ref)                                                  | 1.15x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 3.14 ms: 1.01x faster                                             |
| regex_v8       | 20.6 ms                                                | 21.6 ms: 1.05x slower                                             |
| regex_dna      | 168 ms                                                 | 188 ms: 1.12x slower                                              |
| Geometric mean | (ref)                                                  | 1.04x slower                                                      |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.98 sec: 1.06x faster                                            |
| xml_etree_iterparse  | 96.7 ms                                                | 95.7 ms: 1.01x faster                                             |
| xml_etree_parse      | 139 ms                                                 | 142 ms: 1.02x slower                                              |
| json_dumps           | 10.4 ms                                                | 10.7 ms: 1.03x slower                                             |
| unpickle_pure_python | 221 us                                                 | 239 us: 1.08x slower                                              |
| pickle_pure_python   | 308 us                                                 | 335 us: 1.09x slower                                              |
| json_loads           | 26.5 us                                                | 29.8 us: 1.12x slower                                             |
| xml_etree_generate   | 85.2 ms                                                | 102 ms: 1.19x slower                                              |
| xml_etree_process    | 59.0 ms                                                | 75.8 ms: 1.29x slower                                             |
| Geometric mean       | (ref)                                                  | 1.08x slower                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.18 ms: 1.28x slower                                             |
| python_startup         | 9.93 ms                                                | 15.6 ms: 1.57x slower                                             |
| Geometric mean         | (ref)                                                  | 1.42x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 41.8 ms: 1.20x slower                                             |
| mako            | 11.0 ms                                                | 15.9 ms: 1.44x slower                                             |
| Geometric mean  | (ref)                                                  | 1.32x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| pylint                     | 319 ms                                                 | 134 ms: 2.38x faster                                              |
| gc_traversal               | 3.46 ms                                                | 1.78 ms: 1.94x faster                                             |
| mdp                        | 2.42 sec                                               | 1.32 sec: 1.83x faster                                            |
| async_tree_io_tg           | 1.11 sec                                               | 681 ms: 1.63x faster                                              |
| bench_mp_pool              | 10.8 ms                                                | 6.76 ms: 1.60x faster                                             |
| async_tree_io              | 1.08 sec                                               | 709 ms: 1.53x faster                                              |
| async_tree_memoization_tg  | 560 ms                                                 | 394 ms: 1.42x faster                                              |
| async_tree_none_tg         | 446 ms                                                 | 324 ms: 1.38x faster                                              |
| async_tree_none            | 464 ms                                                 | 345 ms: 1.35x faster                                              |
| async_tree_memoization     | 555 ms                                                 | 420 ms: 1.32x faster                                              |
| deepcopy                   | 352 us                                                 | 267 us: 1.32x faster                                              |
| deepcopy_memo              | 40.3 us                                                | 31.4 us: 1.28x faster                                             |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 578 ms: 1.25x faster                                              |
| pathlib                    | 21.5 ms                                                | 17.9 ms: 1.20x faster                                             |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 605 ms: 1.18x faster                                              |
| go                         | 139 ms                                                 | 122 ms: 1.14x faster                                              |
| comprehensions             | 19.8 us                                                | 17.6 us: 1.13x faster                                             |
| sqlite_synth               | 2.20 us                                                | 1.96 us: 1.13x faster                                             |
| dulwich_log                | 78.9 ms                                                | 70.4 ms: 1.12x faster                                             |
| typing_runtime_protocols   | 163 us                                                 | 147 us: 1.11x faster                                              |
| bpe_tokeniser              | 4.74 sec                                               | 4.42 sec: 1.07x faster                                            |
| tomli_loads                | 2.11 sec                                               | 1.98 sec: 1.06x faster                                            |
| scimark_sor                | 130 ms                                                 | 123 ms: 1.06x faster                                              |
| deepcopy_reduce            | 3.08 us                                                | 2.94 us: 1.05x faster                                             |
| xml_etree_iterparse        | 96.7 ms                                                | 95.7 ms: 1.01x faster                                             |
| regex_effbot               | 3.17 ms                                                | 3.14 ms: 1.01x faster                                             |
| asyncio_websockets         | 517 ms                                                 | 513 ms: 1.01x faster                                              |
| async_generators           | 384 ms                                                 | 390 ms: 1.02x slower                                              |
| scimark_fft                | 342 ms                                                 | 348 ms: 1.02x slower                                              |
| pidigits                   | 184 ms                                                 | 188 ms: 1.02x slower                                              |
| xml_etree_parse            | 139 ms                                                 | 142 ms: 1.02x slower                                              |
| generators                 | 32.2 ms                                                | 33.1 ms: 1.03x slower                                             |
| raytrace                   | 299 ms                                                 | 307 ms: 1.03x slower                                              |
| pycparser                  | 1.17 sec                                               | 1.20 sec: 1.03x slower                                            |
| json_dumps                 | 10.4 ms                                                | 10.7 ms: 1.03x slower                                             |
| pyflate                    | 448 ms                                                 | 463 ms: 1.03x slower                                              |
| coroutines                 | 23.9 ms                                                | 25.0 ms: 1.05x slower                                             |
| regex_v8                   | 20.6 ms                                                | 21.6 ms: 1.05x slower                                             |
| json                       | 5.02 ms                                                | 5.26 ms: 1.05x slower                                             |
| sympy_integrate            | 20.5 ms                                                | 21.9 ms: 1.07x slower                                             |
| float                      | 80.8 ms                                                | 86.9 ms: 1.08x slower                                             |
| html5lib                   | 63.6 ms                                                | 68.6 ms: 1.08x slower                                             |
| hexiom                     | 6.17 ms                                                | 6.66 ms: 1.08x slower                                             |
| logging_simple             | 6.63 us                                                | 7.16 us: 1.08x slower                                             |
| unpickle_pure_python       | 221 us                                                 | 239 us: 1.08x slower                                              |
| deltablue                  | 3.45 ms                                                | 3.73 ms: 1.08x slower                                             |
| pprint_safe_repr           | 743 ms                                                 | 807 ms: 1.09x slower                                              |
| pickle_pure_python         | 308 us                                                 | 335 us: 1.09x slower                                              |
| sympy_str                  | 292 ms                                                 | 318 ms: 1.09x slower                                              |
| sympy_sum                  | 166 ms                                                 | 181 ms: 1.09x slower                                              |
| logging_format             | 7.35 us                                                | 8.05 us: 1.10x slower                                             |
| nqueens                    | 80.1 ms                                                | 88.0 ms: 1.10x slower                                             |
| pprint_pformat             | 1.52 sec                                               | 1.68 sec: 1.10x slower                                            |
| docutils                   | 2.64 sec                                               | 2.93 sec: 1.11x slower                                            |
| regex_dna                  | 168 ms                                                 | 188 ms: 1.12x slower                                              |
| json_loads                 | 26.5 us                                                | 29.8 us: 1.12x slower                                             |
| 2to3                       | 264 ms                                                 | 297 ms: 1.13x slower                                              |
| sympy_expand               | 468 ms                                                 | 531 ms: 1.14x slower                                              |
| scimark_lu                 | 114 ms                                                 | 130 ms: 1.14x slower                                              |
| richards                   | 45.9 ms                                                | 53.1 ms: 1.16x slower                                             |
| thrift                     | 791 us                                                 | 919 us: 1.16x slower                                              |
| scimark_monte_carlo        | 68.4 ms                                                | 80.0 ms: 1.17x slower                                             |
| richards_super             | 51.9 ms                                                | 60.7 ms: 1.17x slower                                             |
| crypto_pyaes               | 76.6 ms                                                | 90.4 ms: 1.18x slower                                             |
| xml_etree_generate         | 85.2 ms                                                | 102 ms: 1.19x slower                                              |
| django_template            | 34.7 ms                                                | 41.8 ms: 1.20x slower                                             |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.30 ms: 1.21x slower                                             |
| fannkuch                   | 372 ms                                                 | 458 ms: 1.23x slower                                              |
| meteor_contest             | 104 ms                                                 | 129 ms: 1.24x slower                                              |
| create_gc_cycles           | 1.09 ms                                                | 1.37 ms: 1.26x slower                                             |
| python_startup_no_site     | 7.16 ms                                                | 9.18 ms: 1.28x slower                                             |
| xml_etree_process          | 59.0 ms                                                | 75.8 ms: 1.29x slower                                             |
| nbody                      | 89.3 ms                                                | 125 ms: 1.40x slower                                              |
| mako                       | 11.0 ms                                                | 15.9 ms: 1.44x slower                                             |
| python_startup             | 9.93 ms                                                | 15.6 ms: 1.57x slower                                             |
| bench_thread_pool          | 941 us                                                 | 1.48 ms: 1.57x slower                                             |
| coverage                   | 71.4 ms                                                | 115 ms: 1.61x slower                                              |
| telco                      | 6.53 ms                                                | 175 ms: 26.85x slower                                             |
| Geometric mean             | (ref)                                                  | 1.04x slower                                                      |

Benchmark hidden because not significant (4): logging_silent, spectral_norm, regex_compile, chaos
Ignored benchmarks (23) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260616-3.16.0a0-4fbec93-NOGIL/bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.043x slower

# HPT report

- Reliability score: 96.82% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.36x