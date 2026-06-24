# Results vs. 3.12.6

- fork: kumaraditya303
- ref: mrocache
- machine: linux-x86_64
- commit hash: 4fbec93
- commit date: 2026-06-16
- overall geometric mean: 1.057x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 262 ms: 1.01x faster                                              |
| docutils       | 2.64 sec                                               | 2.39 sec: 1.10x faster                                            |
| html5lib       | 63.6 ms                                                | 60.9 ms: 1.04x faster                                             |
| Geometric mean | (ref)                                                  | 1.05x faster                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_none            | 464 ms                                                 | 296 ms: 1.57x faster                                              |
| async_tree_memoization_tg  | 560 ms                                                 | 368 ms: 1.52x faster                                              |
| async_tree_io              | 1.08 sec                                               | 726 ms: 1.49x faster                                              |
| async_tree_none_tg         | 446 ms                                                 | 301 ms: 1.48x faster                                              |
| async_tree_memoization     | 555 ms                                                 | 377 ms: 1.47x faster                                              |
| async_tree_io_tg           | 1.11 sec                                               | 769 ms: 1.44x faster                                              |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 546 ms: 1.31x faster                                              |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 559 ms: 1.29x faster                                              |
| async_generators           | 384 ms                                                 | 340 ms: 1.13x faster                                              |
| coroutines                 | 23.9 ms                                                | 23.5 ms: 1.02x faster                                             |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                              |
| Geometric mean             | (ref)                                                  | 1.32x faster                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| float          | 80.8 ms                                                | 74.3 ms: 1.09x faster                                             |
| pidigits       | 184 ms                                                 | 191 ms: 1.04x slower                                              |
| nbody          | 89.3 ms                                                | 95.0 ms: 1.06x slower                                             |
| Geometric mean | (ref)                                                  | 1.00x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.75 ms: 1.15x faster                                             |
| regex_compile  | 142 ms                                                 | 125 ms: 1.14x faster                                              |
| regex_v8       | 20.6 ms                                                | 22.2 ms: 1.08x slower                                             |
| regex_dna      | 168 ms                                                 | 181 ms: 1.08x slower                                              |
| Geometric mean | (ref)                                                  | 1.03x faster                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.88 sec: 1.12x faster                                            |
| xml_etree_iterparse  | 96.7 ms                                                | 91.6 ms: 1.06x faster                                             |
| json_dumps           | 10.4 ms                                                | 9.84 ms: 1.05x faster                                             |
| unpickle_pure_python | 221 us                                                 | 216 us: 1.02x faster                                              |
| pickle_pure_python   | 308 us                                                 | 313 us: 1.02x slower                                              |
| json_loads           | 26.5 us                                                | 27.2 us: 1.03x slower                                             |
| xml_etree_parse      | 139 ms                                                 | 143 ms: 1.03x slower                                              |
| xml_etree_generate   | 85.2 ms                                                | 88.6 ms: 1.04x slower                                             |
| xml_etree_process    | 59.0 ms                                                | 63.1 ms: 1.07x slower                                             |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 6.97 ms: 1.03x faster                                             |
| python_startup         | 9.93 ms                                                | 12.4 ms: 1.25x slower                                             |
| Geometric mean         | (ref)                                                  | 1.10x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 37.2 ms: 1.07x slower                                             |
| mako            | 11.0 ms                                                | 11.9 ms: 1.08x slower                                             |
| Geometric mean  | (ref)                                                  | 1.08x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| pylint                     | 319 ms                                                 | 116 ms: 2.75x faster                                              |
| mdp                        | 2.42 sec                                               | 1.14 sec: 2.11x faster                                            |
| async_tree_none            | 464 ms                                                 | 296 ms: 1.57x faster                                              |
| deepcopy_memo              | 40.3 us                                                | 26.4 us: 1.53x faster                                             |
| async_tree_memoization_tg  | 560 ms                                                 | 368 ms: 1.52x faster                                              |
| async_tree_io              | 1.08 sec                                               | 726 ms: 1.49x faster                                              |
| async_tree_none_tg         | 446 ms                                                 | 301 ms: 1.48x faster                                              |
| deepcopy                   | 352 us                                                 | 238 us: 1.48x faster                                              |
| async_tree_memoization     | 555 ms                                                 | 377 ms: 1.47x faster                                              |
| async_tree_io_tg           | 1.11 sec                                               | 769 ms: 1.44x faster                                              |
| typing_runtime_protocols   | 163 us                                                 | 122 us: 1.34x faster                                              |
| go                         | 139 ms                                                 | 106 ms: 1.32x faster                                              |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 546 ms: 1.31x faster                                              |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 559 ms: 1.29x faster                                              |
| comprehensions             | 19.8 us                                                | 15.7 us: 1.26x faster                                             |
| pathlib                    | 21.5 ms                                                | 18.2 ms: 1.18x faster                                             |
| scimark_sor                | 130 ms                                                 | 111 ms: 1.17x faster                                              |
| spectral_norm              | 110 ms                                                 | 94.3 ms: 1.17x faster                                             |
| raytrace                   | 299 ms                                                 | 256 ms: 1.17x faster                                              |
| deepcopy_reduce            | 3.08 us                                                | 2.67 us: 1.15x faster                                             |
| dulwich_log                | 78.9 ms                                                | 68.4 ms: 1.15x faster                                             |
| regex_effbot               | 3.17 ms                                                | 2.75 ms: 1.15x faster                                             |
| chaos                      | 62.8 ms                                                | 54.8 ms: 1.15x faster                                             |
| generators                 | 32.2 ms                                                | 28.3 ms: 1.14x faster                                             |
| regex_compile              | 142 ms                                                 | 125 ms: 1.14x faster                                              |
| async_generators           | 384 ms                                                 | 340 ms: 1.13x faster                                              |
| tomli_loads                | 2.11 sec                                               | 1.88 sec: 1.12x faster                                            |
| bpe_tokeniser              | 4.74 sec                                               | 4.25 sec: 1.11x faster                                            |
| docutils                   | 2.64 sec                                               | 2.39 sec: 1.10x faster                                            |
| crypto_pyaes               | 76.6 ms                                                | 69.5 ms: 1.10x faster                                             |
| pyflate                    | 448 ms                                                 | 408 ms: 1.10x faster                                              |
| logging_silent             | 109 ns                                                 | 100 ns: 1.09x faster                                              |
| float                      | 80.8 ms                                                | 74.3 ms: 1.09x faster                                             |
| scimark_monte_carlo        | 68.4 ms                                                | 63.8 ms: 1.07x faster                                             |
| logging_simple             | 6.63 us                                                | 6.22 us: 1.07x faster                                             |
| sympy_integrate            | 20.5 ms                                                | 19.3 ms: 1.06x faster                                             |
| nqueens                    | 80.1 ms                                                | 75.4 ms: 1.06x faster                                             |
| xml_etree_iterparse        | 96.7 ms                                                | 91.6 ms: 1.06x faster                                             |
| hexiom                     | 6.17 ms                                                | 5.85 ms: 1.05x faster                                             |
| json_dumps                 | 10.4 ms                                                | 9.84 ms: 1.05x faster                                             |
| scimark_fft                | 342 ms                                                 | 325 ms: 1.05x faster                                              |
| sympy_sum                  | 166 ms                                                 | 158 ms: 1.05x faster                                              |
| html5lib                   | 63.6 ms                                                | 60.9 ms: 1.04x faster                                             |
| meteor_contest             | 104 ms                                                 | 99.3 ms: 1.04x faster                                             |
| sympy_str                  | 292 ms                                                 | 280 ms: 1.04x faster                                              |
| logging_format             | 7.35 us                                                | 7.08 us: 1.04x faster                                             |
| python_startup_no_site     | 7.16 ms                                                | 6.97 ms: 1.03x faster                                             |
| richards                   | 45.9 ms                                                | 44.7 ms: 1.03x faster                                             |
| unpickle_pure_python       | 221 us                                                 | 216 us: 1.02x faster                                              |
| pycparser                  | 1.17 sec                                               | 1.15 sec: 1.02x faster                                            |
| json                       | 5.02 ms                                                | 4.93 ms: 1.02x faster                                             |
| coroutines                 | 23.9 ms                                                | 23.5 ms: 1.02x faster                                             |
| richards_super             | 51.9 ms                                                | 51.1 ms: 1.01x faster                                             |
| deltablue                  | 3.45 ms                                                | 3.41 ms: 1.01x faster                                             |
| 2to3                       | 264 ms                                                 | 262 ms: 1.01x faster                                              |
| pprint_safe_repr           | 743 ms                                                 | 738 ms: 1.01x faster                                              |
| pprint_pformat             | 1.52 sec                                               | 1.51 sec: 1.00x faster                                            |
| sympy_expand               | 468 ms                                                 | 475 ms: 1.02x slower                                              |
| pickle_pure_python         | 308 us                                                 | 313 us: 1.02x slower                                              |
| fannkuch                   | 372 ms                                                 | 381 ms: 1.02x slower                                              |
| gc_traversal               | 3.46 ms                                                | 3.54 ms: 1.03x slower                                             |
| json_loads                 | 26.5 us                                                | 27.2 us: 1.03x slower                                             |
| xml_etree_parse            | 139 ms                                                 | 143 ms: 1.03x slower                                              |
| thrift                     | 791 us                                                 | 818 us: 1.03x slower                                              |
| pidigits                   | 184 ms                                                 | 191 ms: 1.04x slower                                              |
| xml_etree_generate         | 85.2 ms                                                | 88.6 ms: 1.04x slower                                             |
| scimark_lu                 | 114 ms                                                 | 119 ms: 1.04x slower                                              |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                              |
| nbody                      | 89.3 ms                                                | 95.0 ms: 1.06x slower                                             |
| xml_etree_process          | 59.0 ms                                                | 63.1 ms: 1.07x slower                                             |
| django_template            | 34.7 ms                                                | 37.2 ms: 1.07x slower                                             |
| regex_v8                   | 20.6 ms                                                | 22.2 ms: 1.08x slower                                             |
| regex_dna                  | 168 ms                                                 | 181 ms: 1.08x slower                                              |
| mako                       | 11.0 ms                                                | 11.9 ms: 1.08x slower                                             |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.83 ms: 1.10x slower                                             |
| coverage                   | 71.4 ms                                                | 85.7 ms: 1.20x slower                                             |
| python_startup             | 9.93 ms                                                | 12.4 ms: 1.25x slower                                             |
| bench_thread_pool          | 941 us                                                 | 1.34 ms: 1.42x slower                                             |
| create_gc_cycles           | 1.09 ms                                                | 1.65 ms: 1.52x slower                                             |
| bench_mp_pool              | 10.8 ms                                                | 219 ms: 20.27x slower                                             |
| telco                      | 6.53 ms                                                | 165 ms: 25.24x slower                                             |
| Geometric mean             | (ref)                                                  | 1.01x faster                                                      |

Benchmark hidden because not significant (1): sqlite_synth
Ignored benchmarks (23) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260616-3.16.0a0-4fbec93/bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.057x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.14x