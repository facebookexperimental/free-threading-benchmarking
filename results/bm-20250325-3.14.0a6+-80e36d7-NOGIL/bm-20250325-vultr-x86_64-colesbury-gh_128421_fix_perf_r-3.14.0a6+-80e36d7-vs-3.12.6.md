# Results vs. 3.12.6

- fork: colesbury
- ref: gh_128421_fix_perf_r
- machine: linux-x86_64
- commit hash: 80e36d7
- commit date: 2025-03-25
- overall geometric mean: 1.044x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.02x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250325-vultr-x86_64-colesbury-gh_128421_fix_perf_r-3.14.0a6+-80e36d7 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 297 ms: 1.13x slower                                                      |
| docutils       | 2.64 sec                                               | 2.79 sec: 1.06x slower                                                    |
| html5lib       | 63.6 ms                                                | 72.5 ms: 1.14x slower                                                     |
| Geometric mean | (ref)                                                  | 1.11x slower                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250325-vultr-x86_64-colesbury-gh_128421_fix_perf_r-3.14.0a6+-80e36d7 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 552 ms: 2.01x faster                                                      |
| async_tree_none_tg         | 446 ms                                                 | 238 ms: 1.88x faster                                                      |
| async_tree_memoization_tg  | 560 ms                                                 | 299 ms: 1.87x faster                                                      |
| async_tree_io              | 1.08 sec                                               | 580 ms: 1.87x faster                                                      |
| async_tree_none            | 464 ms                                                 | 275 ms: 1.69x faster                                                      |
| async_tree_memoization     | 555 ms                                                 | 331 ms: 1.68x faster                                                      |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 485 ms: 1.49x faster                                                      |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 518 ms: 1.38x faster                                                      |
| coroutines                 | 23.9 ms                                                | 23.2 ms: 1.03x faster                                                     |
| async_generators           | 384 ms                                                 | 391 ms: 1.02x slower                                                      |
| Geometric mean             | (ref)                                                  | 1.49x faster                                                              |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250325-vultr-x86_64-colesbury-gh_128421_fix_perf_r-3.14.0a6+-80e36d7 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 77.7 ms: 1.04x faster                                                     |
| pidigits       | 184 ms                                                 | 191 ms: 1.04x slower                                                      |
| nbody          | 89.3 ms                                                | 137 ms: 1.53x slower                                                      |
| Geometric mean | (ref)                                                  | 1.15x slower                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250325-vultr-x86_64-colesbury-gh_128421_fix_perf_r-3.14.0a6+-80e36d7 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.76 ms: 1.15x faster                                                     |
| regex_v8       | 20.6 ms                                                | 20.9 ms: 1.02x slower                                                     |
| regex_dna      | 168 ms                                                 | 175 ms: 1.04x slower                                                      |
| regex_compile  | 142 ms                                                 | 157 ms: 1.10x slower                                                      |
| Geometric mean | (ref)                                                  | 1.00x slower                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250325-vultr-x86_64-colesbury-gh_128421_fix_perf_r-3.14.0a6+-80e36d7 |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.1 ms: 1.10x faster                                                     |
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.08x faster                                                      |
| tomli_loads          | 2.11 sec                                               | 2.35 sec: 1.11x slower                                                    |
| xml_etree_generate   | 85.2 ms                                                | 96.9 ms: 1.14x slower                                                     |
| json_loads           | 26.5 us                                                | 30.5 us: 1.15x slower                                                     |
| unpickle_pure_python | 221 us                                                 | 254 us: 1.15x slower                                                      |
| pickle_pure_python   | 308 us                                                 | 358 us: 1.16x slower                                                      |
| xml_etree_process    | 59.0 ms                                                | 70.9 ms: 1.20x slower                                                     |
| json_dumps           | 10.4 ms                                                | 12.9 ms: 1.24x slower                                                     |
| Geometric mean       | (ref)                                                  | 1.11x slower                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250325-vultr-x86_64-colesbury-gh_128421_fix_perf_r-3.14.0a6+-80e36d7 |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 11.1 ms: 1.55x slower                                                     |
| python_startup         | 9.93 ms                                                | 15.7 ms: 1.59x slower                                                     |
| Geometric mean         | (ref)                                                  | 1.57x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250325-vultr-x86_64-colesbury-gh_128421_fix_perf_r-3.14.0a6+-80e36d7 |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 59.3 ms: 1.18x slower                                                     |
| django_template | 34.7 ms                                                | 42.7 ms: 1.23x slower                                                     |
| genshi_text     | 22.8 ms                                                | 28.4 ms: 1.24x slower                                                     |
| mako            | 11.0 ms                                                | 16.0 ms: 1.45x slower                                                     |
| Geometric mean  | (ref)                                                  | 1.27x slower                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250325-vultr-x86_64-colesbury-gh_128421_fix_perf_r-3.14.0a6+-80e36d7 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 552 ms: 2.01x faster                                                      |
| gc_traversal               | 3.46 ms                                                | 1.79 ms: 1.93x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 238 ms: 1.88x faster                                                      |
| async_tree_memoization_tg  | 560 ms                                                 | 299 ms: 1.87x faster                                                      |
| async_tree_io              | 1.08 sec                                               | 580 ms: 1.87x faster                                                      |
| async_tree_none            | 464 ms                                                 | 275 ms: 1.69x faster                                                      |
| async_tree_memoization     | 555 ms                                                 | 331 ms: 1.68x faster                                                      |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 485 ms: 1.49x faster                                                      |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 518 ms: 1.38x faster                                                      |
| regex_effbot               | 3.17 ms                                                | 2.76 ms: 1.15x faster                                                     |
| deepcopy                   | 352 us                                                 | 310 us: 1.14x faster                                                      |
| xml_etree_iterparse        | 96.7 ms                                                | 88.1 ms: 1.10x faster                                                     |
| sqlite_synth               | 2.20 us                                                | 2.02 us: 1.09x faster                                                     |
| pathlib                    | 21.5 ms                                                | 19.9 ms: 1.08x faster                                                     |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.08x faster                                                      |
| dulwich_log                | 78.9 ms                                                | 73.3 ms: 1.08x faster                                                     |
| float                      | 80.8 ms                                                | 77.7 ms: 1.04x faster                                                     |
| coroutines                 | 23.9 ms                                                | 23.2 ms: 1.03x faster                                                     |
| deepcopy_memo              | 40.3 us                                                | 39.6 us: 1.02x faster                                                     |
| regex_v8                   | 20.6 ms                                                | 20.9 ms: 1.02x slower                                                     |
| deepcopy_reduce            | 3.08 us                                                | 3.13 us: 1.02x slower                                                     |
| async_generators           | 384 ms                                                 | 391 ms: 1.02x slower                                                      |
| generators                 | 32.2 ms                                                | 32.8 ms: 1.02x slower                                                     |
| bpe_tokeniser              | 4.74 sec                                               | 4.84 sec: 1.02x slower                                                    |
| pycparser                  | 1.17 sec                                               | 1.20 sec: 1.02x slower                                                    |
| go                         | 139 ms                                                 | 144 ms: 1.03x slower                                                      |
| spectral_norm              | 110 ms                                                 | 114 ms: 1.04x slower                                                      |
| comprehensions             | 19.8 us                                                | 20.6 us: 1.04x slower                                                     |
| json                       | 5.02 ms                                                | 5.22 ms: 1.04x slower                                                     |
| pidigits                   | 184 ms                                                 | 191 ms: 1.04x slower                                                      |
| regex_dna                  | 168 ms                                                 | 175 ms: 1.04x slower                                                      |
| docutils                   | 2.64 sec                                               | 2.79 sec: 1.06x slower                                                    |
| logging_silent             | 109 ns                                                 | 116 ns: 1.06x slower                                                      |
| scimark_sor                | 130 ms                                                 | 138 ms: 1.06x slower                                                      |
| mdp                        | 2.42 sec                                               | 2.62 sec: 1.08x slower                                                    |
| sqlalchemy_imperative      | 21.8 ms                                                | 23.7 ms: 1.09x slower                                                     |
| raytrace                   | 299 ms                                                 | 325 ms: 1.09x slower                                                      |
| chaos                      | 62.8 ms                                                | 68.9 ms: 1.10x slower                                                     |
| regex_compile              | 142 ms                                                 | 157 ms: 1.10x slower                                                      |
| logging_simple             | 6.63 us                                                | 7.31 us: 1.10x slower                                                     |
| sqlalchemy_declarative     | 143 ms                                                 | 158 ms: 1.11x slower                                                      |
| thrift                     | 791 us                                                 | 876 us: 1.11x slower                                                      |
| tomli_loads                | 2.11 sec                                               | 2.35 sec: 1.11x slower                                                    |
| sympy_sum                  | 166 ms                                                 | 186 ms: 1.12x slower                                                      |
| 2to3                       | 264 ms                                                 | 297 ms: 1.13x slower                                                      |
| pprint_safe_repr           | 743 ms                                                 | 839 ms: 1.13x slower                                                      |
| deltablue                  | 3.45 ms                                                | 3.91 ms: 1.13x slower                                                     |
| xml_etree_generate         | 85.2 ms                                                | 96.9 ms: 1.14x slower                                                     |
| logging_format             | 7.35 us                                                | 8.37 us: 1.14x slower                                                     |
| html5lib                   | 63.6 ms                                                | 72.5 ms: 1.14x slower                                                     |
| pprint_pformat             | 1.52 sec                                               | 1.74 sec: 1.14x slower                                                    |
| sympy_integrate            | 20.5 ms                                                | 23.5 ms: 1.15x slower                                                     |
| sympy_str                  | 292 ms                                                 | 335 ms: 1.15x slower                                                      |
| json_loads                 | 26.5 us                                                | 30.5 us: 1.15x slower                                                     |
| unpickle_pure_python       | 221 us                                                 | 254 us: 1.15x slower                                                      |
| crypto_pyaes               | 76.6 ms                                                | 88.5 ms: 1.15x slower                                                     |
| pyflate                    | 448 ms                                                 | 518 ms: 1.16x slower                                                      |
| pickle_pure_python         | 308 us                                                 | 358 us: 1.16x slower                                                      |
| scimark_fft                | 342 ms                                                 | 400 ms: 1.17x slower                                                      |
| sympy_expand               | 468 ms                                                 | 549 ms: 1.17x slower                                                      |
| genshi_xml                 | 50.2 ms                                                | 59.3 ms: 1.18x slower                                                     |
| xml_etree_process          | 59.0 ms                                                | 70.9 ms: 1.20x slower                                                     |
| richards                   | 45.9 ms                                                | 55.9 ms: 1.22x slower                                                     |
| scimark_monte_carlo        | 68.4 ms                                                | 83.5 ms: 1.22x slower                                                     |
| nqueens                    | 80.1 ms                                                | 98.3 ms: 1.23x slower                                                     |
| hexiom                     | 6.17 ms                                                | 7.60 ms: 1.23x slower                                                     |
| django_template            | 34.7 ms                                                | 42.7 ms: 1.23x slower                                                     |
| create_gc_cycles           | 1.09 ms                                                | 1.35 ms: 1.23x slower                                                     |
| typing_runtime_protocols   | 163 us                                                 | 202 us: 1.24x slower                                                      |
| scimark_lu                 | 114 ms                                                 | 142 ms: 1.24x slower                                                      |
| genshi_text                | 22.8 ms                                                | 28.4 ms: 1.24x slower                                                     |
| json_dumps                 | 10.4 ms                                                | 12.9 ms: 1.24x slower                                                     |
| richards_super             | 51.9 ms                                                | 64.6 ms: 1.25x slower                                                     |
| meteor_contest             | 104 ms                                                 | 133 ms: 1.29x slower                                                      |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.85 ms: 1.33x slower                                                     |
| fannkuch                   | 372 ms                                                 | 500 ms: 1.34x slower                                                      |
| telco                      | 6.53 ms                                                | 9.09 ms: 1.39x slower                                                     |
| coverage                   | 71.4 ms                                                | 99.6 ms: 1.39x slower                                                     |
| mako                       | 11.0 ms                                                | 16.0 ms: 1.45x slower                                                     |
| nbody                      | 89.3 ms                                                | 137 ms: 1.53x slower                                                      |
| python_startup_no_site     | 7.16 ms                                                | 11.1 ms: 1.55x slower                                                     |
| python_startup             | 9.93 ms                                                | 15.7 ms: 1.59x slower                                                     |
| bench_thread_pool          | 941 us                                                 | 3.16 ms: 3.36x slower                                                     |
| bench_mp_pool              | 10.8 ms                                                | 96.9 ms: 8.98x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.09x slower                                                              |

Benchmark hidden because not significant (2): pylint, asyncio_websockets
Ignored benchmarks (19) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250325-3.14.0a6+-80e36d7-NOGIL/bm-20250325-vultr-x86_64-colesbury-gh_128421_fix_perf_r-3.14.0a6+-80e36d7.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.044x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.05x
- 95% likely to have a slowdown of 1.04x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: 1.36x