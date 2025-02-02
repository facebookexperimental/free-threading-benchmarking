# Results vs. 3.12.6

- fork: mpage
- ref: revert_c3ae5c9
- machine: linux-x86_64
- commit hash: 3edc57c
- commit date: 2025-02-01
- overall geometric mean: 1.051x slower
- HPT reliability: 99.97%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250201-vultr-x86_64-mpage-revert_c3ae5c9-3.14.0a4+-3edc57c |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 304 ms: 1.16x slower                                            |
| docutils       | 2.64 sec                                               | 2.80 sec: 1.06x slower                                          |
| html5lib       | 63.6 ms                                                | 70.9 ms: 1.11x slower                                           |
| Geometric mean | (ref)                                                  | 1.11x slower                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250201-vultr-x86_64-mpage-revert_c3ae5c9-3.14.0a4+-3edc57c |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 587 ms: 1.89x faster                                            |
| async_tree_none_tg         | 446 ms                                                 | 252 ms: 1.77x faster                                            |
| async_tree_io              | 1.08 sec                                               | 614 ms: 1.76x faster                                            |
| async_tree_memoization_tg  | 560 ms                                                 | 326 ms: 1.72x faster                                            |
| async_tree_none            | 464 ms                                                 | 289 ms: 1.61x faster                                            |
| async_tree_memoization     | 555 ms                                                 | 354 ms: 1.57x faster                                            |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 506 ms: 1.43x faster                                            |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 540 ms: 1.33x faster                                            |
| coroutines                 | 23.9 ms                                                | 23.2 ms: 1.03x faster                                           |
| async_generators           | 384 ms                                                 | 375 ms: 1.03x faster                                            |
| Geometric mean             | (ref)                                                  | 1.43x faster                                                    |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250201-vultr-x86_64-mpage-revert_c3ae5c9-3.14.0a4+-3edc57c |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------:|
| float          | 80.8 ms                                                | 76.7 ms: 1.05x faster                                           |
| pidigits       | 184 ms                                                 | 192 ms: 1.04x slower                                            |
| nbody          | 89.3 ms                                                | 137 ms: 1.54x slower                                            |
| Geometric mean | (ref)                                                  | 1.15x slower                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250201-vultr-x86_64-mpage-revert_c3ae5c9-3.14.0a4+-3edc57c |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.79 ms: 1.13x faster                                           |
| regex_compile  | 142 ms                                                 | 150 ms: 1.05x slower                                            |
| regex_dna      | 168 ms                                                 | 181 ms: 1.08x slower                                            |
| regex_v8       | 20.6 ms                                                | 23.7 ms: 1.15x slower                                           |
| Geometric mean | (ref)                                                  | 1.04x slower                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250201-vultr-x86_64-mpage-revert_c3ae5c9-3.14.0a4+-3edc57c |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.5 ms: 1.10x faster                                           |
| xml_etree_parse      | 139 ms                                                 | 127 ms: 1.09x faster                                            |
| unpickle_pure_python | 221 us                                                 | 246 us: 1.12x slower                                            |
| xml_etree_generate   | 85.2 ms                                                | 96.1 ms: 1.13x slower                                           |
| tomli_loads          | 2.11 sec                                               | 2.38 sec: 1.13x slower                                          |
| xml_etree_process    | 59.0 ms                                                | 68.9 ms: 1.17x slower                                           |
| json_loads           | 26.5 us                                                | 31.6 us: 1.19x slower                                           |
| pickle_pure_python   | 308 us                                                 | 374 us: 1.22x slower                                            |
| json_dumps           | 10.4 ms                                                | 12.9 ms: 1.25x slower                                           |
| Geometric mean       | (ref)                                                  | 1.11x slower                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250201-vultr-x86_64-mpage-revert_c3ae5c9-3.14.0a4+-3edc57c |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.64 ms: 1.35x slower                                           |
| python_startup         | 9.93 ms                                                | 15.4 ms: 1.55x slower                                           |
| Geometric mean         | (ref)                                                  | 1.44x slower                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250201-vultr-x86_64-mpage-revert_c3ae5c9-3.14.0a4+-3edc57c |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 42.1 ms: 1.22x slower                                           |
| genshi_xml      | 50.2 ms                                                | 61.1 ms: 1.22x slower                                           |
| genshi_text     | 22.8 ms                                                | 28.3 ms: 1.24x slower                                           |
| mako            | 11.0 ms                                                | 15.9 ms: 1.44x slower                                           |
| Geometric mean  | (ref)                                                  | 1.28x slower                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250201-vultr-x86_64-mpage-revert_c3ae5c9-3.14.0a4+-3edc57c |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------:|
| gc_traversal               | 3.46 ms                                                | 1.66 ms: 2.08x faster                                           |
| async_tree_io_tg           | 1.11 sec                                               | 587 ms: 1.89x faster                                            |
| async_tree_none_tg         | 446 ms                                                 | 252 ms: 1.77x faster                                            |
| async_tree_io              | 1.08 sec                                               | 614 ms: 1.76x faster                                            |
| async_tree_memoization_tg  | 560 ms                                                 | 326 ms: 1.72x faster                                            |
| async_tree_none            | 464 ms                                                 | 289 ms: 1.61x faster                                            |
| async_tree_memoization     | 555 ms                                                 | 354 ms: 1.57x faster                                            |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 506 ms: 1.43x faster                                            |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 540 ms: 1.33x faster                                            |
| pathlib                    | 21.5 ms                                                | 18.5 ms: 1.16x faster                                           |
| regex_effbot               | 3.17 ms                                                | 2.79 ms: 1.13x faster                                           |
| deepcopy                   | 352 us                                                 | 312 us: 1.13x faster                                            |
| xml_etree_iterparse        | 96.7 ms                                                | 87.5 ms: 1.10x faster                                           |
| xml_etree_parse            | 139 ms                                                 | 127 ms: 1.09x faster                                            |
| sqlite_synth               | 2.20 us                                                | 2.05 us: 1.07x faster                                           |
| float                      | 80.8 ms                                                | 76.7 ms: 1.05x faster                                           |
| coroutines                 | 23.9 ms                                                | 23.2 ms: 1.03x faster                                           |
| deepcopy_memo              | 40.3 us                                                | 39.1 us: 1.03x faster                                           |
| async_generators           | 384 ms                                                 | 375 ms: 1.03x faster                                            |
| bpe_tokeniser              | 4.74 sec                                               | 4.64 sec: 1.02x faster                                          |
| go                         | 139 ms                                                 | 137 ms: 1.02x faster                                            |
| spectral_norm              | 110 ms                                                 | 109 ms: 1.01x faster                                            |
| pycparser                  | 1.17 sec                                               | 1.18 sec: 1.01x slower                                          |
| scimark_sor                | 130 ms                                                 | 133 ms: 1.03x slower                                            |
| generators                 | 32.2 ms                                                | 33.3 ms: 1.03x slower                                           |
| pidigits                   | 184 ms                                                 | 192 ms: 1.04x slower                                            |
| deepcopy_reduce            | 3.08 us                                                | 3.23 us: 1.05x slower                                           |
| regex_compile              | 142 ms                                                 | 150 ms: 1.05x slower                                            |
| dulwich_log                | 78.9 ms                                                | 82.9 ms: 1.05x slower                                           |
| docutils                   | 2.64 sec                                               | 2.80 sec: 1.06x slower                                          |
| regex_dna                  | 168 ms                                                 | 181 ms: 1.08x slower                                            |
| json                       | 5.02 ms                                                | 5.46 ms: 1.09x slower                                           |
| chaos                      | 62.8 ms                                                | 68.6 ms: 1.09x slower                                           |
| raytrace                   | 299 ms                                                 | 327 ms: 1.09x slower                                            |
| mdp                        | 2.42 sec                                               | 2.64 sec: 1.09x slower                                          |
| sqlalchemy_declarative     | 143 ms                                                 | 157 ms: 1.10x slower                                            |
| logging_simple             | 6.63 us                                                | 7.30 us: 1.10x slower                                           |
| logging_format             | 7.35 us                                                | 8.10 us: 1.10x slower                                           |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.1 ms: 1.10x slower                                           |
| pprint_safe_repr           | 743 ms                                                 | 823 ms: 1.11x slower                                            |
| html5lib                   | 63.6 ms                                                | 70.9 ms: 1.11x slower                                           |
| unpickle_pure_python       | 221 us                                                 | 246 us: 1.12x slower                                            |
| pprint_pformat             | 1.52 sec                                               | 1.70 sec: 1.12x slower                                          |
| pyflate                    | 448 ms                                                 | 501 ms: 1.12x slower                                            |
| sympy_sum                  | 166 ms                                                 | 186 ms: 1.12x slower                                            |
| sqlglot_normalize          | 107 ms                                                 | 120 ms: 1.12x slower                                            |
| xml_etree_generate         | 85.2 ms                                                | 96.1 ms: 1.13x slower                                           |
| tomli_loads                | 2.11 sec                                               | 2.38 sec: 1.13x slower                                          |
| scimark_fft                | 342 ms                                                 | 389 ms: 1.14x slower                                            |
| sqlglot_transpile          | 1.67 ms                                                | 1.91 ms: 1.14x slower                                           |
| sqlglot_optimize           | 53.3 ms                                                | 61.2 ms: 1.15x slower                                           |
| regex_v8                   | 20.6 ms                                                | 23.7 ms: 1.15x slower                                           |
| 2to3                       | 264 ms                                                 | 304 ms: 1.16x slower                                            |
| sympy_str                  | 292 ms                                                 | 337 ms: 1.16x slower                                            |
| crypto_pyaes               | 76.6 ms                                                | 89.0 ms: 1.16x slower                                           |
| thrift                     | 791 us                                                 | 922 us: 1.16x slower                                            |
| sqlglot_parse              | 1.36 ms                                                | 1.58 ms: 1.17x slower                                           |
| xml_etree_process          | 59.0 ms                                                | 68.9 ms: 1.17x slower                                           |
| sympy_expand               | 468 ms                                                 | 550 ms: 1.18x slower                                            |
| sympy_integrate            | 20.5 ms                                                | 24.2 ms: 1.18x slower                                           |
| json_loads                 | 26.5 us                                                | 31.6 us: 1.19x slower                                           |
| hexiom                     | 6.17 ms                                                | 7.41 ms: 1.20x slower                                           |
| scimark_lu                 | 114 ms                                                 | 137 ms: 1.20x slower                                            |
| nqueens                    | 80.1 ms                                                | 96.6 ms: 1.21x slower                                           |
| scimark_monte_carlo        | 68.4 ms                                                | 83.1 ms: 1.21x slower                                           |
| django_template            | 34.7 ms                                                | 42.1 ms: 1.22x slower                                           |
| pickle_pure_python         | 308 us                                                 | 374 us: 1.22x slower                                            |
| genshi_xml                 | 50.2 ms                                                | 61.1 ms: 1.22x slower                                           |
| typing_runtime_protocols   | 163 us                                                 | 199 us: 1.22x slower                                            |
| richards                   | 45.9 ms                                                | 56.5 ms: 1.23x slower                                           |
| genshi_text                | 22.8 ms                                                | 28.3 ms: 1.24x slower                                           |
| json_dumps                 | 10.4 ms                                                | 12.9 ms: 1.25x slower                                           |
| meteor_contest             | 104 ms                                                 | 130 ms: 1.26x slower                                            |
| richards_super             | 51.9 ms                                                | 66.0 ms: 1.27x slower                                           |
| create_gc_cycles           | 1.09 ms                                                | 1.40 ms: 1.28x slower                                           |
| telco                      | 6.53 ms                                                | 8.61 ms: 1.32x slower                                           |
| fannkuch                   | 372 ms                                                 | 493 ms: 1.32x slower                                            |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.83 ms: 1.33x slower                                           |
| python_startup_no_site     | 7.16 ms                                                | 9.64 ms: 1.35x slower                                           |
| deltablue                  | 3.45 ms                                                | 4.67 ms: 1.35x slower                                           |
| coverage                   | 71.4 ms                                                | 98.5 ms: 1.38x slower                                           |
| mako                       | 11.0 ms                                                | 15.9 ms: 1.44x slower                                           |
| nbody                      | 89.3 ms                                                | 137 ms: 1.54x slower                                            |
| python_startup             | 9.93 ms                                                | 15.4 ms: 1.55x slower                                           |
| bench_thread_pool          | 941 us                                                 | 3.29 ms: 3.50x slower                                           |
| bench_mp_pool              | 10.8 ms                                                | 91.1 ms: 8.44x slower                                           |
| Geometric mean             | (ref)                                                  | 1.09x slower                                                    |

Benchmark hidden because not significant (4): pylint, asyncio_websockets, comprehensions, logging_silent
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250201-3.14.0a4+-3edc57c-NOGIL/bm-20250201-vultr-x86_64-mpage-revert_c3ae5c9-3.14.0a4+-3edc57c.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.051x slower

# HPT report

- Reliability score: 99.97% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.35x