# Results vs. 3.12.6

- fork: colesbury
- ref: experiment_interp_ti
- machine: linux-x86_64
- commit hash: 62b231d
- commit date: 2025-03-19
- overall geometric mean: 1.043x faster
- HPT reliability: 77.23%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.40x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250319-vultr-x86_64-colesbury-experiment_interp_ti-3.14.0a6+-62b231d |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 276 ms: 1.05x slower                                                      |
| Geometric mean | (ref)                                                  | 1.02x slower                                                              |

Benchmark hidden because not significant (2): docutils, html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250319-vultr-x86_64-colesbury-experiment_interp_ti-3.14.0a6+-62b231d |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 493 ms: 2.25x faster                                                      |
| async_tree_none_tg         | 446 ms                                                 | 213 ms: 2.10x faster                                                      |
| async_tree_io              | 1.08 sec                                               | 529 ms: 2.05x faster                                                      |
| async_tree_memoization_tg  | 560 ms                                                 | 274 ms: 2.04x faster                                                      |
| async_tree_none            | 464 ms                                                 | 252 ms: 1.85x faster                                                      |
| async_tree_memoization     | 555 ms                                                 | 310 ms: 1.79x faster                                                      |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 435 ms: 1.66x faster                                                      |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 469 ms: 1.52x faster                                                      |
| coroutines                 | 23.9 ms                                                | 19.5 ms: 1.23x faster                                                     |
| async_generators           | 384 ms                                                 | 326 ms: 1.18x faster                                                      |
| Geometric mean             | (ref)                                                  | 1.65x faster                                                              |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250319-vultr-x86_64-colesbury-experiment_interp_ti-3.14.0a6+-62b231d |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 69.1 ms: 1.17x faster                                                     |
| pidigits       | 184 ms                                                 | 187 ms: 1.02x slower                                                      |
| nbody          | 89.3 ms                                                | 120 ms: 1.34x slower                                                      |
| Geometric mean | (ref)                                                  | 1.05x slower                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250319-vultr-x86_64-colesbury-experiment_interp_ti-3.14.0a6+-62b231d |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 140 ms: 1.01x faster                                                      |
| regex_effbot   | 3.17 ms                                                | 3.19 ms: 1.01x slower                                                     |
| regex_v8       | 20.6 ms                                                | 21.9 ms: 1.06x slower                                                     |
| regex_dna      | 168 ms                                                 | 188 ms: 1.12x slower                                                      |
| Geometric mean | (ref)                                                  | 1.04x slower                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250319-vultr-x86_64-colesbury-experiment_interp_ti-3.14.0a6+-62b231d |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 86.0 ms: 1.12x faster                                                     |
| xml_etree_generate   | 85.2 ms                                                | 85.6 ms: 1.00x slower                                                     |
| unpickle_pure_python | 221 us                                                 | 227 us: 1.03x slower                                                      |
| xml_etree_parse      | 139 ms                                                 | 143 ms: 1.03x slower                                                      |
| xml_etree_process    | 59.0 ms                                                | 60.9 ms: 1.03x slower                                                     |
| pickle_pure_python   | 308 us                                                 | 321 us: 1.04x slower                                                      |
| json_loads           | 26.5 us                                                | 30.2 us: 1.14x slower                                                     |
| json_dumps           | 10.4 ms                                                | 12.7 ms: 1.23x slower                                                     |
| Geometric mean       | (ref)                                                  | 1.04x slower                                                              |

Benchmark hidden because not significant (1): tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250319-vultr-x86_64-colesbury-experiment_interp_ti-3.14.0a6+-62b231d |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 11.0 ms: 1.54x slower                                                     |
| python_startup         | 9.93 ms                                                | 15.5 ms: 1.57x slower                                                     |
| Geometric mean         | (ref)                                                  | 1.55x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250319-vultr-x86_64-colesbury-experiment_interp_ti-3.14.0a6+-62b231d |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 52.1 ms: 1.04x slower                                                     |
| genshi_text     | 22.8 ms                                                | 24.4 ms: 1.07x slower                                                     |
| django_template | 34.7 ms                                                | 37.2 ms: 1.07x slower                                                     |
| mako            | 11.0 ms                                                | 14.9 ms: 1.36x slower                                                     |
| Geometric mean  | (ref)                                                  | 1.13x slower                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250319-vultr-x86_64-colesbury-experiment_interp_ti-3.14.0a6+-62b231d |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 493 ms: 2.25x faster                                                      |
| async_tree_none_tg         | 446 ms                                                 | 213 ms: 2.10x faster                                                      |
| async_tree_io              | 1.08 sec                                               | 529 ms: 2.05x faster                                                      |
| async_tree_memoization_tg  | 560 ms                                                 | 274 ms: 2.04x faster                                                      |
| async_tree_none            | 464 ms                                                 | 252 ms: 1.85x faster                                                      |
| async_tree_memoization     | 555 ms                                                 | 310 ms: 1.79x faster                                                      |
| gc_traversal               | 3.46 ms                                                | 2.07 ms: 1.67x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 435 ms: 1.66x faster                                                      |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 469 ms: 1.52x faster                                                      |
| deepcopy                   | 352 us                                                 | 268 us: 1.31x faster                                                      |
| coroutines                 | 23.9 ms                                                | 19.5 ms: 1.23x faster                                                     |
| logging_silent             | 109 ns                                                 | 89.3 ns: 1.22x faster                                                     |
| async_generators           | 384 ms                                                 | 326 ms: 1.18x faster                                                      |
| generators                 | 32.2 ms                                                | 27.4 ms: 1.18x faster                                                     |
| deepcopy_memo              | 40.3 us                                                | 34.4 us: 1.17x faster                                                     |
| float                      | 80.8 ms                                                | 69.1 ms: 1.17x faster                                                     |
| spectral_norm              | 110 ms                                                 | 95.2 ms: 1.16x faster                                                     |
| scimark_sor                | 130 ms                                                 | 113 ms: 1.14x faster                                                      |
| pathlib                    | 21.5 ms                                                | 19.0 ms: 1.13x faster                                                     |
| comprehensions             | 19.8 us                                                | 17.6 us: 1.13x faster                                                     |
| go                         | 139 ms                                                 | 124 ms: 1.12x faster                                                      |
| xml_etree_iterparse        | 96.7 ms                                                | 86.0 ms: 1.12x faster                                                     |
| deepcopy_reduce            | 3.08 us                                                | 2.75 us: 1.12x faster                                                     |
| dulwich_log                | 78.9 ms                                                | 70.9 ms: 1.11x faster                                                     |
| sqlite_synth               | 2.20 us                                                | 1.99 us: 1.11x faster                                                     |
| pylint                     | 319 ms                                                 | 294 ms: 1.09x faster                                                      |
| bpe_tokeniser              | 4.74 sec                                               | 4.39 sec: 1.08x faster                                                    |
| raytrace                   | 299 ms                                                 | 288 ms: 1.04x faster                                                      |
| logging_simple             | 6.63 us                                                | 6.46 us: 1.03x faster                                                     |
| chaos                      | 62.8 ms                                                | 61.2 ms: 1.03x faster                                                     |
| regex_compile              | 142 ms                                                 | 140 ms: 1.01x faster                                                      |
| pycparser                  | 1.17 sec                                               | 1.15 sec: 1.01x faster                                                    |
| logging_format             | 7.35 us                                                | 7.29 us: 1.01x faster                                                     |
| xml_etree_generate         | 85.2 ms                                                | 85.6 ms: 1.00x slower                                                     |
| pyflate                    | 448 ms                                                 | 450 ms: 1.01x slower                                                      |
| regex_effbot               | 3.17 ms                                                | 3.19 ms: 1.01x slower                                                     |
| scimark_fft                | 342 ms                                                 | 345 ms: 1.01x slower                                                      |
| richards                   | 45.9 ms                                                | 46.6 ms: 1.02x slower                                                     |
| pidigits                   | 184 ms                                                 | 187 ms: 1.02x slower                                                      |
| scimark_lu                 | 114 ms                                                 | 117 ms: 1.02x slower                                                      |
| unpickle_pure_python       | 221 us                                                 | 227 us: 1.03x slower                                                      |
| deltablue                  | 3.45 ms                                                | 3.55 ms: 1.03x slower                                                     |
| xml_etree_parse            | 139 ms                                                 | 143 ms: 1.03x slower                                                      |
| xml_etree_process          | 59.0 ms                                                | 60.9 ms: 1.03x slower                                                     |
| json                       | 5.02 ms                                                | 5.20 ms: 1.03x slower                                                     |
| scimark_monte_carlo        | 68.4 ms                                                | 70.8 ms: 1.04x slower                                                     |
| genshi_xml                 | 50.2 ms                                                | 52.1 ms: 1.04x slower                                                     |
| sympy_sum                  | 166 ms                                                 | 172 ms: 1.04x slower                                                      |
| sqlalchemy_imperative      | 21.8 ms                                                | 22.6 ms: 1.04x slower                                                     |
| pickle_pure_python         | 308 us                                                 | 321 us: 1.04x slower                                                      |
| sqlalchemy_declarative     | 143 ms                                                 | 149 ms: 1.04x slower                                                      |
| thrift                     | 791 us                                                 | 827 us: 1.05x slower                                                      |
| 2to3                       | 264 ms                                                 | 276 ms: 1.05x slower                                                      |
| pprint_safe_repr           | 743 ms                                                 | 781 ms: 1.05x slower                                                      |
| sympy_str                  | 292 ms                                                 | 308 ms: 1.06x slower                                                      |
| pprint_pformat             | 1.52 sec                                               | 1.60 sec: 1.06x slower                                                    |
| crypto_pyaes               | 76.6 ms                                                | 80.9 ms: 1.06x slower                                                     |
| nqueens                    | 80.1 ms                                                | 84.9 ms: 1.06x slower                                                     |
| regex_v8                   | 20.6 ms                                                | 21.9 ms: 1.06x slower                                                     |
| hexiom                     | 6.17 ms                                                | 6.58 ms: 1.07x slower                                                     |
| typing_runtime_protocols   | 163 us                                                 | 174 us: 1.07x slower                                                      |
| genshi_text                | 22.8 ms                                                | 24.4 ms: 1.07x slower                                                     |
| richards_super             | 51.9 ms                                                | 55.6 ms: 1.07x slower                                                     |
| django_template            | 34.7 ms                                                | 37.2 ms: 1.07x slower                                                     |
| sympy_integrate            | 20.5 ms                                                | 22.1 ms: 1.08x slower                                                     |
| sympy_expand               | 468 ms                                                 | 505 ms: 1.08x slower                                                      |
| regex_dna                  | 168 ms                                                 | 188 ms: 1.12x slower                                                      |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.96 ms: 1.13x slower                                                     |
| json_loads                 | 26.5 us                                                | 30.2 us: 1.14x slower                                                     |
| mdp                        | 2.42 sec                                               | 2.80 sec: 1.16x slower                                                    |
| meteor_contest             | 104 ms                                                 | 120 ms: 1.16x slower                                                      |
| fannkuch                   | 372 ms                                                 | 433 ms: 1.16x slower                                                      |
| json_dumps                 | 10.4 ms                                                | 12.7 ms: 1.23x slower                                                     |
| telco                      | 6.53 ms                                                | 8.08 ms: 1.24x slower                                                     |
| create_gc_cycles           | 1.09 ms                                                | 1.36 ms: 1.24x slower                                                     |
| coverage                   | 71.4 ms                                                | 90.4 ms: 1.27x slower                                                     |
| nbody                      | 89.3 ms                                                | 120 ms: 1.34x slower                                                      |
| mako                       | 11.0 ms                                                | 14.9 ms: 1.36x slower                                                     |
| python_startup_no_site     | 7.16 ms                                                | 11.0 ms: 1.54x slower                                                     |
| python_startup             | 9.93 ms                                                | 15.5 ms: 1.57x slower                                                     |
| bench_thread_pool          | 941 us                                                 | 3.12 ms: 3.31x slower                                                     |
| bench_mp_pool              | 10.8 ms                                                | 95.4 ms: 8.83x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.00x faster                                                              |

Benchmark hidden because not significant (4): html5lib, asyncio_websockets, tomli_loads, docutils
Ignored benchmarks (19) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250319-3.14.0a6+-62b231d-CLANG,NOGIL/bm-20250319-vultr-x86_64-colesbury-experiment_interp_ti-3.14.0a6+-62b231d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.043x faster

# HPT report

- Reliability score: 77.23% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.40x