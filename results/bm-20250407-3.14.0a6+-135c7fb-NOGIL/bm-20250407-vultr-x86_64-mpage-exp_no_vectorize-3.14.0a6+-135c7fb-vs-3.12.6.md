# Results vs. 3.12.6

- fork: mpage
- ref: exp_no_vectorize
- machine: linux-x86_64
- commit hash: 135c7fb
- commit date: 2025-04-07
- overall geometric mean: 1.011x slower
- HPT reliability: 99.18%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.37x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6+-135c7fb |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 291 ms: 1.10x slower                                              |
| docutils       | 2.64 sec                                               | 2.79 sec: 1.06x slower                                            |
| html5lib       | 63.6 ms                                                | 68.2 ms: 1.07x slower                                             |
| Geometric mean | (ref)                                                  | 1.08x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6+-135c7fb |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 534 ms: 2.08x faster                                              |
| async_tree_io              | 1.08 sec                                               | 567 ms: 1.91x faster                                              |
| async_tree_none_tg         | 446 ms                                                 | 234 ms: 1.90x faster                                              |
| async_tree_memoization_tg  | 560 ms                                                 | 295 ms: 1.90x faster                                              |
| async_tree_none            | 464 ms                                                 | 268 ms: 1.74x faster                                              |
| async_tree_memoization     | 555 ms                                                 | 325 ms: 1.71x faster                                              |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 486 ms: 1.49x faster                                              |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 514 ms: 1.39x faster                                              |
| async_generators           | 384 ms                                                 | 367 ms: 1.05x faster                                              |
| coroutines                 | 23.9 ms                                                | 23.2 ms: 1.03x faster                                             |
| asyncio_websockets         | 517 ms                                                 | 516 ms: 1.00x faster                                              |
| Geometric mean             | (ref)                                                  | 1.51x faster                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6+-135c7fb |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| float          | 80.8 ms                                                | 73.1 ms: 1.11x faster                                             |
| pidigits       | 184 ms                                                 | 198 ms: 1.07x slower                                              |
| nbody          | 89.3 ms                                                | 120 ms: 1.35x slower                                              |
| Geometric mean | (ref)                                                  | 1.09x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6+-135c7fb |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.69 ms: 1.18x faster                                             |
| regex_v8       | 20.6 ms                                                | 20.7 ms: 1.01x slower                                             |
| regex_dna      | 168 ms                                                 | 175 ms: 1.04x slower                                              |
| regex_compile  | 142 ms                                                 | 152 ms: 1.07x slower                                              |
| Geometric mean | (ref)                                                  | 1.01x faster                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6+-135c7fb |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.8 ms: 1.10x faster                                             |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.08x faster                                              |
| tomli_loads          | 2.11 sec                                               | 2.28 sec: 1.08x slower                                            |
| json_loads           | 26.5 us                                                | 29.5 us: 1.11x slower                                             |
| unpickle_pure_python | 221 us                                                 | 245 us: 1.11x slower                                              |
| pickle_pure_python   | 308 us                                                 | 348 us: 1.13x slower                                              |
| xml_etree_generate   | 85.2 ms                                                | 96.8 ms: 1.14x slower                                             |
| xml_etree_process    | 59.0 ms                                                | 70.4 ms: 1.19x slower                                             |
| json_dumps           | 10.4 ms                                                | 12.7 ms: 1.23x slower                                             |
| Geometric mean       | (ref)                                                  | 1.09x slower                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6+-135c7fb |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 11.2 ms: 1.57x slower                                             |
| python_startup         | 9.93 ms                                                | 15.9 ms: 1.60x slower                                             |
| Geometric mean         | (ref)                                                  | 1.58x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6+-135c7fb |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 59.3 ms: 1.18x slower                                             |
| django_template | 34.7 ms                                                | 42.0 ms: 1.21x slower                                             |
| genshi_text     | 22.8 ms                                                | 28.0 ms: 1.23x slower                                             |
| mako            | 11.0 ms                                                | 15.7 ms: 1.42x slower                                             |
| Geometric mean  | (ref)                                                  | 1.26x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6+-135c7fb |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 534 ms: 2.08x faster                                              |
| gc_traversal               | 3.46 ms                                                | 1.78 ms: 1.94x faster                                             |
| async_tree_io              | 1.08 sec                                               | 567 ms: 1.91x faster                                              |
| async_tree_none_tg         | 446 ms                                                 | 234 ms: 1.90x faster                                              |
| async_tree_memoization_tg  | 560 ms                                                 | 295 ms: 1.90x faster                                              |
| mdp                        | 2.42 sec                                               | 1.36 sec: 1.78x faster                                            |
| async_tree_none            | 464 ms                                                 | 268 ms: 1.74x faster                                              |
| async_tree_memoization     | 555 ms                                                 | 325 ms: 1.71x faster                                              |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 486 ms: 1.49x faster                                              |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 514 ms: 1.39x faster                                              |
| regex_effbot               | 3.17 ms                                                | 2.69 ms: 1.18x faster                                             |
| deepcopy                   | 352 us                                                 | 302 us: 1.16x faster                                              |
| float                      | 80.8 ms                                                | 73.1 ms: 1.11x faster                                             |
| xml_etree_iterparse        | 96.7 ms                                                | 87.8 ms: 1.10x faster                                             |
| pathlib                    | 21.5 ms                                                | 19.6 ms: 1.10x faster                                             |
| dulwich_log                | 78.9 ms                                                | 72.7 ms: 1.08x faster                                             |
| sqlite_synth               | 2.20 us                                                | 2.03 us: 1.08x faster                                             |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.08x faster                                              |
| deepcopy_memo              | 40.3 us                                                | 37.5 us: 1.07x faster                                             |
| async_generators           | 384 ms                                                 | 367 ms: 1.05x faster                                              |
| coroutines                 | 23.9 ms                                                | 23.2 ms: 1.03x faster                                             |
| go                         | 139 ms                                                 | 136 ms: 1.02x faster                                              |
| deepcopy_reduce            | 3.08 us                                                | 3.02 us: 1.02x faster                                             |
| spectral_norm              | 110 ms                                                 | 109 ms: 1.02x faster                                              |
| bpe_tokeniser              | 4.74 sec                                               | 4.70 sec: 1.01x faster                                            |
| asyncio_websockets         | 517 ms                                                 | 516 ms: 1.00x faster                                              |
| regex_v8                   | 20.6 ms                                                | 20.7 ms: 1.01x slower                                             |
| pycparser                  | 1.17 sec                                               | 1.18 sec: 1.01x slower                                            |
| scimark_sor                | 130 ms                                                 | 132 ms: 1.02x slower                                              |
| raytrace                   | 299 ms                                                 | 309 ms: 1.03x slower                                              |
| generators                 | 32.2 ms                                                | 33.3 ms: 1.03x slower                                             |
| logging_silent             | 109 ns                                                 | 113 ns: 1.03x slower                                              |
| comprehensions             | 19.8 us                                                | 20.6 us: 1.04x slower                                             |
| chaos                      | 62.8 ms                                                | 65.4 ms: 1.04x slower                                             |
| regex_dna                  | 168 ms                                                 | 175 ms: 1.04x slower                                              |
| scimark_fft                | 342 ms                                                 | 360 ms: 1.05x slower                                              |
| docutils                   | 2.64 sec                                               | 2.79 sec: 1.06x slower                                            |
| regex_compile              | 142 ms                                                 | 152 ms: 1.07x slower                                              |
| html5lib                   | 63.6 ms                                                | 68.2 ms: 1.07x slower                                             |
| pidigits                   | 184 ms                                                 | 198 ms: 1.07x slower                                              |
| pprint_safe_repr           | 743 ms                                                 | 803 ms: 1.08x slower                                              |
| tomli_loads                | 2.11 sec                                               | 2.28 sec: 1.08x slower                                            |
| pyflate                    | 448 ms                                                 | 490 ms: 1.09x slower                                              |
| logging_simple             | 6.63 us                                                | 7.26 us: 1.10x slower                                             |
| 2to3                       | 264 ms                                                 | 291 ms: 1.10x slower                                              |
| deltablue                  | 3.45 ms                                                | 3.80 ms: 1.10x slower                                             |
| pprint_pformat             | 1.52 sec                                               | 1.68 sec: 1.11x slower                                            |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.2 ms: 1.11x slower                                             |
| json_loads                 | 26.5 us                                                | 29.5 us: 1.11x slower                                             |
| unpickle_pure_python       | 221 us                                                 | 245 us: 1.11x slower                                              |
| sqlalchemy_declarative     | 143 ms                                                 | 159 ms: 1.11x slower                                              |
| nqueens                    | 80.1 ms                                                | 89.3 ms: 1.11x slower                                             |
| logging_format             | 7.35 us                                                | 8.20 us: 1.12x slower                                             |
| sympy_sum                  | 166 ms                                                 | 186 ms: 1.12x slower                                              |
| sympy_str                  | 292 ms                                                 | 328 ms: 1.13x slower                                              |
| sympy_integrate            | 20.5 ms                                                | 23.2 ms: 1.13x slower                                             |
| crypto_pyaes               | 76.6 ms                                                | 86.3 ms: 1.13x slower                                             |
| scimark_monte_carlo        | 68.4 ms                                                | 77.3 ms: 1.13x slower                                             |
| pickle_pure_python         | 308 us                                                 | 348 us: 1.13x slower                                              |
| xml_etree_generate         | 85.2 ms                                                | 96.8 ms: 1.14x slower                                             |
| sympy_expand               | 468 ms                                                 | 543 ms: 1.16x slower                                              |
| scimark_lu                 | 114 ms                                                 | 134 ms: 1.17x slower                                              |
| hexiom                     | 6.17 ms                                                | 7.26 ms: 1.18x slower                                             |
| genshi_xml                 | 50.2 ms                                                | 59.3 ms: 1.18x slower                                             |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.20 ms: 1.18x slower                                             |
| xml_etree_process          | 59.0 ms                                                | 70.4 ms: 1.19x slower                                             |
| richards                   | 45.9 ms                                                | 55.0 ms: 1.20x slower                                             |
| django_template            | 34.7 ms                                                | 42.0 ms: 1.21x slower                                             |
| richards_super             | 51.9 ms                                                | 63.2 ms: 1.22x slower                                             |
| typing_runtime_protocols   | 163 us                                                 | 200 us: 1.22x slower                                              |
| genshi_text                | 22.8 ms                                                | 28.0 ms: 1.23x slower                                             |
| json_dumps                 | 10.4 ms                                                | 12.7 ms: 1.23x slower                                             |
| meteor_contest             | 104 ms                                                 | 128 ms: 1.24x slower                                              |
| create_gc_cycles           | 1.09 ms                                                | 1.36 ms: 1.24x slower                                             |
| fannkuch                   | 372 ms                                                 | 467 ms: 1.26x slower                                              |
| telco                      | 6.53 ms                                                | 8.35 ms: 1.28x slower                                             |
| nbody                      | 89.3 ms                                                | 120 ms: 1.35x slower                                              |
| mako                       | 11.0 ms                                                | 15.7 ms: 1.42x slower                                             |
| coverage                   | 71.4 ms                                                | 108 ms: 1.51x slower                                              |
| python_startup_no_site     | 7.16 ms                                                | 11.2 ms: 1.57x slower                                             |
| python_startup             | 9.93 ms                                                | 15.9 ms: 1.60x slower                                             |
| bench_thread_pool          | 941 us                                                 | 3.16 ms: 3.35x slower                                             |
| bench_mp_pool              | 10.8 ms                                                | 96.2 ms: 8.91x slower                                             |
| Geometric mean             | (ref)                                                  | 1.05x slower                                                      |

Benchmark hidden because not significant (2): pylint, json
Ignored benchmarks (20) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250407-3.14.0a6+-135c7fb-NOGIL/bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6+-135c7fb.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.011x slower

# HPT report

- Reliability score: 99.18% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.37x