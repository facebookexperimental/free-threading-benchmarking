# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: eb73378
- commit date: 2025-10-23
- overall geometric mean: 1.080x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251023-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-eb73378 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 249 ms: 1.04x faster                                                    |
| docutils       | 2.62 sec                                                     | 2.65 sec: 1.01x slower                                                  |
| html5lib       | 67.0 ms                                                      | 63.9 ms: 1.05x faster                                                   |
| Geometric mean | (ref)                                                        | 1.03x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251023-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-eb73378 |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_memoization     | 461 ms                                                       | 308 ms: 1.50x faster                                                    |
| async_tree_io_tg           | 913 ms                                                       | 611 ms: 1.49x faster                                                    |
| async_tree_io              | 876 ms                                                       | 594 ms: 1.48x faster                                                    |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 474 ms: 1.41x faster                                                    |
| async_tree_none_tg         | 336 ms                                                       | 244 ms: 1.38x faster                                                    |
| async_tree_none            | 354 ms                                                       | 258 ms: 1.37x faster                                                    |
| async_tree_memoization_tg  | 414 ms                                                       | 306 ms: 1.35x faster                                                    |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 475 ms: 1.34x faster                                                    |
| async_generators           | 377 ms                                                       | 338 ms: 1.12x faster                                                    |
| coroutines                 | 23.6 ms                                                      | 22.3 ms: 1.05x faster                                                   |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                    |
| Geometric mean             | (ref)                                                        | 1.30x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251023-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-eb73378 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 62.7 ms: 1.23x faster                                                   |
| pidigits       | 217 ms                                                       | 192 ms: 1.13x faster                                                    |
| nbody          | 85.1 ms                                                      | 83.3 ms: 1.02x faster                                                   |
| Geometric mean | (ref)                                                        | 1.12x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251023-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-eb73378 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 22.7 ms                                                      | 23.0 ms: 1.01x slower                                                   |
| regex_effbot   | 3.08 ms                                                      | 3.14 ms: 1.02x slower                                                   |
| regex_compile  | 132 ms                                                       | 137 ms: 1.04x slower                                                    |
| regex_dna      | 180 ms                                                       | 191 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                        | 1.03x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251023-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-eb73378 |
|----------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 10.5 ms                                                      | 8.66 ms: 1.22x faster                                                   |
| unpickle_pure_python | 210 us                                                       | 183 us: 1.15x faster                                                    |
| xml_etree_process    | 59.3 ms                                                      | 52.2 ms: 1.14x faster                                                   |
| tomli_loads          | 2.01 sec                                                     | 1.77 sec: 1.14x faster                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 75.9 ms: 1.13x faster                                                   |
| json_loads           | 27.0 us                                                      | 25.7 us: 1.05x faster                                                   |
| xml_etree_iterparse  | 94.9 ms                                                      | 93.6 ms: 1.01x faster                                                   |
| pickle_pure_python   | 294 us                                                       | 306 us: 1.04x slower                                                    |
| xml_etree_parse      | 136 ms                                                       | 143 ms: 1.05x slower                                                    |
| Geometric mean       | (ref)                                                        | 1.08x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251023-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-eb73378 |
|------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.37 ms: 1.00x faster                                                   |
| python_startup         | 11.0 ms                                                      | 12.6 ms: 1.15x slower                                                   |
| Geometric mean         | (ref)                                                        | 1.07x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251023-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-eb73378 |
|-----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 20.1 ms: 1.07x faster                                                   |
| django_template | 34.1 ms                                                      | 33.4 ms: 1.02x faster                                                   |
| genshi_xml      | 48.8 ms                                                      | 50.3 ms: 1.03x slower                                                   |
| Geometric mean  | (ref)                                                        | 1.02x faster                                                            |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251023-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-eb73378 |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.17 sec: 2.01x faster                                                  |
| richards                   | 45.2 ms                                                      | 22.6 ms: 2.00x faster                                                   |
| richards_super             | 51.6 ms                                                      | 26.5 ms: 1.95x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 22.0 us: 1.77x faster                                                   |
| deepcopy                   | 355 us                                                       | 231 us: 1.54x faster                                                    |
| async_tree_memoization     | 461 ms                                                       | 308 ms: 1.50x faster                                                    |
| async_tree_io_tg           | 913 ms                                                       | 611 ms: 1.49x faster                                                    |
| async_tree_io              | 876 ms                                                       | 594 ms: 1.48x faster                                                    |
| scimark_fft                | 349 ms                                                       | 242 ms: 1.44x faster                                                    |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 474 ms: 1.41x faster                                                    |
| async_tree_none_tg         | 336 ms                                                       | 244 ms: 1.38x faster                                                    |
| async_tree_none            | 354 ms                                                       | 258 ms: 1.37x faster                                                    |
| scimark_sor                | 134 ms                                                       | 99.2 ms: 1.36x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 306 ms: 1.35x faster                                                    |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 475 ms: 1.34x faster                                                    |
| logging_silent             | 103 ns                                                       | 76.9 ns: 1.33x faster                                                   |
| spectral_norm              | 111 ms                                                       | 84.3 ms: 1.32x faster                                                   |
| deepcopy_reduce            | 3.11 us                                                      | 2.37 us: 1.31x faster                                                   |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 3.80 ms: 1.24x faster                                                   |
| float                      | 77.5 ms                                                      | 62.7 ms: 1.23x faster                                                   |
| json_dumps                 | 10.5 ms                                                      | 8.66 ms: 1.22x faster                                                   |
| scimark_monte_carlo        | 65.4 ms                                                      | 54.8 ms: 1.19x faster                                                   |
| scimark_lu                 | 113 ms                                                       | 95.9 ms: 1.17x faster                                                   |
| go                         | 141 ms                                                       | 120 ms: 1.17x faster                                                    |
| pyflate                    | 449 ms                                                       | 390 ms: 1.15x faster                                                    |
| unpickle_pure_python       | 210 us                                                       | 183 us: 1.15x faster                                                    |
| comprehensions             | 16.5 us                                                      | 14.4 us: 1.14x faster                                                   |
| bpe_tokeniser              | 4.45 sec                                                     | 3.90 sec: 1.14x faster                                                  |
| xml_etree_process          | 59.3 ms                                                      | 52.2 ms: 1.14x faster                                                   |
| tomli_loads                | 2.01 sec                                                     | 1.77 sec: 1.14x faster                                                  |
| deltablue                  | 3.12 ms                                                      | 2.76 ms: 1.13x faster                                                   |
| pylint                     | 317 ms                                                       | 280 ms: 1.13x faster                                                    |
| pidigits                   | 217 ms                                                       | 192 ms: 1.13x faster                                                    |
| pprint_safe_repr           | 738 ms                                                       | 655 ms: 1.13x faster                                                    |
| xml_etree_generate         | 85.4 ms                                                      | 75.9 ms: 1.13x faster                                                   |
| async_generators           | 377 ms                                                       | 338 ms: 1.12x faster                                                    |
| coverage                   | 83.0 ms                                                      | 75.5 ms: 1.10x faster                                                   |
| pprint_pformat             | 1.50 sec                                                     | 1.38 sec: 1.09x faster                                                  |
| chaos                      | 57.3 ms                                                      | 52.9 ms: 1.08x faster                                                   |
| genshi_text                | 21.5 ms                                                      | 20.1 ms: 1.07x faster                                                   |
| sympy_integrate            | 19.8 ms                                                      | 18.5 ms: 1.07x faster                                                   |
| crypto_pyaes               | 67.9 ms                                                      | 64.3 ms: 1.06x faster                                                   |
| typing_runtime_protocols   | 155 us                                                       | 147 us: 1.06x faster                                                    |
| coroutines                 | 23.6 ms                                                      | 22.3 ms: 1.05x faster                                                   |
| thrift                     | 778 us                                                       | 739 us: 1.05x faster                                                    |
| json_loads                 | 27.0 us                                                      | 25.7 us: 1.05x faster                                                   |
| html5lib                   | 67.0 ms                                                      | 63.9 ms: 1.05x faster                                                   |
| 2to3                       | 260 ms                                                       | 249 ms: 1.04x faster                                                    |
| logging_simple             | 6.16 us                                                      | 5.91 us: 1.04x faster                                                   |
| logging_format             | 6.84 us                                                      | 6.60 us: 1.04x faster                                                   |
| hexiom                     | 5.99 ms                                                      | 5.78 ms: 1.04x faster                                                   |
| fannkuch                   | 370 ms                                                       | 358 ms: 1.03x faster                                                    |
| sqlite_synth               | 2.21 us                                                      | 2.15 us: 1.03x faster                                                   |
| generators                 | 28.8 ms                                                      | 28.1 ms: 1.03x faster                                                   |
| nbody                      | 85.1 ms                                                      | 83.3 ms: 1.02x faster                                                   |
| django_template            | 34.1 ms                                                      | 33.4 ms: 1.02x faster                                                   |
| sympy_sum                  | 156 ms                                                       | 153 ms: 1.02x faster                                                    |
| xml_etree_iterparse        | 94.9 ms                                                      | 93.6 ms: 1.01x faster                                                   |
| json                       | 4.93 ms                                                      | 4.88 ms: 1.01x faster                                                   |
| dulwich_log                | 74.8 ms                                                      | 74.1 ms: 1.01x faster                                                   |
| python_startup_no_site     | 7.39 ms                                                      | 7.37 ms: 1.00x faster                                                   |
| docutils                   | 2.62 sec                                                     | 2.65 sec: 1.01x slower                                                  |
| regex_v8                   | 22.7 ms                                                      | 23.0 ms: 1.01x slower                                                   |
| regex_effbot               | 3.08 ms                                                      | 3.14 ms: 1.02x slower                                                   |
| sympy_expand               | 457 ms                                                       | 469 ms: 1.03x slower                                                    |
| meteor_contest             | 102 ms                                                       | 104 ms: 1.03x slower                                                    |
| nqueens                    | 78.6 ms                                                      | 80.9 ms: 1.03x slower                                                   |
| genshi_xml                 | 48.8 ms                                                      | 50.3 ms: 1.03x slower                                                   |
| regex_compile              | 132 ms                                                       | 137 ms: 1.04x slower                                                    |
| pickle_pure_python         | 294 us                                                       | 306 us: 1.04x slower                                                    |
| pycparser                  | 1.12 sec                                                     | 1.16 sec: 1.04x slower                                                  |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                    |
| xml_etree_parse            | 136 ms                                                       | 143 ms: 1.05x slower                                                    |
| bench_thread_pool          | 919 us                                                       | 970 us: 1.06x slower                                                    |
| regex_dna                  | 180 ms                                                       | 191 ms: 1.06x slower                                                    |
| raytrace                   | 253 ms                                                       | 268 ms: 1.06x slower                                                    |
| bench_mp_pool              | 11.0 ms                                                      | 12.3 ms: 1.12x slower                                                   |
| python_startup             | 11.0 ms                                                      | 12.6 ms: 1.15x slower                                                   |
| gc_traversal               | 3.14 ms                                                      | 4.35 ms: 1.38x slower                                                   |
| create_gc_cycles           | 1.34 ms                                                      | 2.01 ms: 1.50x slower                                                   |
| telco                      | 7.82 ms                                                      | 157 ms: 20.06x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.08x faster                                                            |

Benchmark hidden because not significant (3): mako, pathlib, sympy_str
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251023-3.15.0a1+-eb73378-CLANG,JIT/bm-20251023-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-eb73378.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.080x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.21x