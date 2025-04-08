# Results vs. 3.12.6

- fork: mpage
- ref: exp_no_vectorize
- machine: linux-x86_64
- commit hash: 135c7fb
- commit date: 2025-04-07
- overall geometric mean: 1.125x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6+-135c7fb |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 245 ms: 1.07x faster                                              |
| docutils       | 2.64 sec                                               | 2.49 sec: 1.06x faster                                            |
| Geometric mean | (ref)                                                  | 1.07x faster                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6+-135c7fb |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 612 ms: 1.81x faster                                              |
| async_tree_memoization     | 555 ms                                                 | 311 ms: 1.79x faster                                              |
| async_tree_memoization_tg  | 560 ms                                                 | 315 ms: 1.77x faster                                              |
| async_tree_io              | 1.08 sec                                               | 613 ms: 1.77x faster                                              |
| async_tree_none_tg         | 446 ms                                                 | 259 ms: 1.72x faster                                              |
| async_tree_none            | 464 ms                                                 | 271 ms: 1.72x faster                                              |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 494 ms: 1.46x faster                                              |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 493 ms: 1.45x faster                                              |
| async_generators           | 384 ms                                                 | 322 ms: 1.19x faster                                              |
| coroutines                 | 23.9 ms                                                | 23.4 ms: 1.02x faster                                             |
| Geometric mean             | (ref)                                                  | 1.49x faster                                                      |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6+-135c7fb |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| float          | 80.8 ms                                                | 68.5 ms: 1.18x faster                                             |
| nbody          | 89.3 ms                                                | 82.3 ms: 1.09x faster                                             |
| pidigits       | 184 ms                                                 | 198 ms: 1.07x slower                                              |
| Geometric mean | (ref)                                                  | 1.06x faster                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6+-135c7fb |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.64 ms: 1.20x faster                                             |
| regex_compile  | 142 ms                                                 | 121 ms: 1.17x faster                                              |
| regex_dna      | 168 ms                                                 | 171 ms: 1.02x slower                                              |
| regex_v8       | 20.6 ms                                                | 21.3 ms: 1.04x slower                                             |
| Geometric mean | (ref)                                                  | 1.07x faster                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6+-135c7fb |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.84 sec: 1.15x faster                                            |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.07x faster                                              |
| unpickle_pure_python | 221 us                                                 | 207 us: 1.07x faster                                              |
| xml_etree_iterparse  | 96.7 ms                                                | 91.7 ms: 1.05x faster                                             |
| xml_etree_generate   | 85.2 ms                                                | 82.5 ms: 1.03x faster                                             |
| pickle_pure_python   | 308 us                                                 | 302 us: 1.02x faster                                              |
| xml_etree_process    | 59.0 ms                                                | 58.0 ms: 1.02x faster                                             |
| json_loads           | 26.5 us                                                | 27.0 us: 1.02x slower                                             |
| json_dumps           | 10.4 ms                                                | 11.2 ms: 1.08x slower                                             |
| Geometric mean       | (ref)                                                  | 1.03x faster                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6+-135c7fb |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 8.66 ms: 1.21x slower                                             |
| python_startup         | 9.93 ms                                                | 15.1 ms: 1.52x slower                                             |
| Geometric mean         | (ref)                                                  | 1.36x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6+-135c7fb |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 19.9 ms: 1.15x faster                                             |
| genshi_xml      | 50.2 ms                                                | 47.2 ms: 1.06x faster                                             |
| django_template | 34.7 ms                                                | 34.4 ms: 1.01x faster                                             |
| mako            | 11.0 ms                                                | 11.7 ms: 1.06x slower                                             |
| Geometric mean  | (ref)                                                  | 1.04x faster                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6+-135c7fb |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.13 sec: 2.15x faster                                            |
| async_tree_io_tg           | 1.11 sec                                               | 612 ms: 1.81x faster                                              |
| async_tree_memoization     | 555 ms                                                 | 311 ms: 1.79x faster                                              |
| async_tree_memoization_tg  | 560 ms                                                 | 315 ms: 1.77x faster                                              |
| async_tree_io              | 1.08 sec                                               | 613 ms: 1.77x faster                                              |
| async_tree_none_tg         | 446 ms                                                 | 259 ms: 1.72x faster                                              |
| async_tree_none            | 464 ms                                                 | 271 ms: 1.72x faster                                              |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 494 ms: 1.46x faster                                              |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 493 ms: 1.45x faster                                              |
| deepcopy_memo              | 40.3 us                                                | 28.2 us: 1.43x faster                                             |
| deepcopy                   | 352 us                                                 | 248 us: 1.42x faster                                              |
| go                         | 139 ms                                                 | 105 ms: 1.32x faster                                              |
| comprehensions             | 19.8 us                                                | 16.2 us: 1.22x faster                                             |
| chaos                      | 62.8 ms                                                | 51.7 ms: 1.21x faster                                             |
| raytrace                   | 299 ms                                                 | 247 ms: 1.21x faster                                              |
| scimark_sor                | 130 ms                                                 | 107 ms: 1.21x faster                                              |
| generators                 | 32.2 ms                                                | 26.7 ms: 1.21x faster                                             |
| spectral_norm              | 110 ms                                                 | 91.9 ms: 1.20x faster                                             |
| regex_effbot               | 3.17 ms                                                | 2.64 ms: 1.20x faster                                             |
| async_generators           | 384 ms                                                 | 322 ms: 1.19x faster                                              |
| dulwich_log                | 78.9 ms                                                | 66.6 ms: 1.18x faster                                             |
| float                      | 80.8 ms                                                | 68.5 ms: 1.18x faster                                             |
| regex_compile              | 142 ms                                                 | 121 ms: 1.17x faster                                              |
| deepcopy_reduce            | 3.08 us                                                | 2.64 us: 1.17x faster                                             |
| pylint                     | 319 ms                                                 | 277 ms: 1.15x faster                                              |
| tomli_loads                | 2.11 sec                                               | 1.84 sec: 1.15x faster                                            |
| genshi_text                | 22.8 ms                                                | 19.9 ms: 1.15x faster                                             |
| logging_silent             | 109 ns                                                 | 95.5 ns: 1.14x faster                                             |
| scimark_monte_carlo        | 68.4 ms                                                | 60.2 ms: 1.14x faster                                             |
| bpe_tokeniser              | 4.74 sec                                               | 4.17 sec: 1.13x faster                                            |
| crypto_pyaes               | 76.6 ms                                                | 67.5 ms: 1.13x faster                                             |
| richards                   | 45.9 ms                                                | 40.5 ms: 1.13x faster                                             |
| pathlib                    | 21.5 ms                                                | 19.0 ms: 1.13x faster                                             |
| logging_simple             | 6.63 us                                                | 5.87 us: 1.13x faster                                             |
| richards_super             | 51.9 ms                                                | 46.1 ms: 1.12x faster                                             |
| logging_format             | 7.35 us                                                | 6.54 us: 1.12x faster                                             |
| scimark_fft                | 342 ms                                                 | 305 ms: 1.12x faster                                              |
| pyflate                    | 448 ms                                                 | 401 ms: 1.12x faster                                              |
| sqlalchemy_declarative     | 143 ms                                                 | 128 ms: 1.11x faster                                              |
| sqlalchemy_imperative      | 21.8 ms                                                | 19.6 ms: 1.11x faster                                             |
| deltablue                  | 3.45 ms                                                | 3.14 ms: 1.10x faster                                             |
| hexiom                     | 6.17 ms                                                | 5.66 ms: 1.09x faster                                             |
| nbody                      | 89.3 ms                                                | 82.3 ms: 1.09x faster                                             |
| pprint_safe_repr           | 743 ms                                                 | 686 ms: 1.08x faster                                              |
| pprint_pformat             | 1.52 sec                                               | 1.40 sec: 1.08x faster                                            |
| sympy_sum                  | 166 ms                                                 | 153 ms: 1.08x faster                                              |
| sympy_integrate            | 20.5 ms                                                | 19.0 ms: 1.08x faster                                             |
| sympy_str                  | 292 ms                                                 | 270 ms: 1.08x faster                                              |
| 2to3                       | 264 ms                                                 | 245 ms: 1.07x faster                                              |
| pycparser                  | 1.17 sec                                               | 1.09 sec: 1.07x faster                                            |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.07x faster                                              |
| unpickle_pure_python       | 221 us                                                 | 207 us: 1.07x faster                                              |
| genshi_xml                 | 50.2 ms                                                | 47.2 ms: 1.06x faster                                             |
| docutils                   | 2.64 sec                                               | 2.49 sec: 1.06x faster                                            |
| nqueens                    | 80.1 ms                                                | 75.8 ms: 1.06x faster                                             |
| xml_etree_iterparse        | 96.7 ms                                                | 91.7 ms: 1.05x faster                                             |
| scimark_lu                 | 114 ms                                                 | 108 ms: 1.05x faster                                              |
| meteor_contest             | 104 ms                                                 | 98.9 ms: 1.05x faster                                             |
| typing_runtime_protocols   | 163 us                                                 | 157 us: 1.04x faster                                              |
| sympy_expand               | 468 ms                                                 | 453 ms: 1.03x faster                                              |
| xml_etree_generate         | 85.2 ms                                                | 82.5 ms: 1.03x faster                                             |
| json                       | 5.02 ms                                                | 4.90 ms: 1.03x faster                                             |
| coroutines                 | 23.9 ms                                                | 23.4 ms: 1.02x faster                                             |
| pickle_pure_python         | 308 us                                                 | 302 us: 1.02x faster                                              |
| xml_etree_process          | 59.0 ms                                                | 58.0 ms: 1.02x faster                                             |
| sqlite_synth               | 2.20 us                                                | 2.18 us: 1.01x faster                                             |
| django_template            | 34.7 ms                                                | 34.4 ms: 1.01x faster                                             |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.36 ms: 1.01x faster                                             |
| fannkuch                   | 372 ms                                                 | 370 ms: 1.01x faster                                              |
| json_loads                 | 26.5 us                                                | 27.0 us: 1.02x slower                                             |
| regex_dna                  | 168 ms                                                 | 171 ms: 1.02x slower                                              |
| regex_v8                   | 20.6 ms                                                | 21.3 ms: 1.04x slower                                             |
| mako                       | 11.0 ms                                                | 11.7 ms: 1.06x slower                                             |
| pidigits                   | 184 ms                                                 | 198 ms: 1.07x slower                                              |
| telco                      | 6.53 ms                                                | 7.07 ms: 1.08x slower                                             |
| json_dumps                 | 10.4 ms                                                | 11.2 ms: 1.08x slower                                             |
| coverage                   | 71.4 ms                                                | 78.2 ms: 1.09x slower                                             |
| bench_thread_pool          | 941 us                                                 | 1.04 ms: 1.11x slower                                             |
| python_startup_no_site     | 7.16 ms                                                | 8.66 ms: 1.21x slower                                             |
| gc_traversal               | 3.46 ms                                                | 4.58 ms: 1.33x slower                                             |
| python_startup             | 9.93 ms                                                | 15.1 ms: 1.52x slower                                             |
| create_gc_cycles           | 1.09 ms                                                | 1.84 ms: 1.69x slower                                             |
| bench_mp_pool              | 10.8 ms                                                | 88.3 ms: 8.18x slower                                             |
| Geometric mean             | (ref)                                                  | 1.09x faster                                                      |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250407-3.14.0a6+-135c7fb/bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6+-135c7fb.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.125x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.12x