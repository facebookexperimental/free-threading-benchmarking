# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: eb73378
- commit date: 2025-10-23
- overall geometric mean: 1.118x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251023-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-eb73378 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 249 ms: 1.06x faster                                                    |
| docutils       | 2.64 sec                                               | 2.65 sec: 1.00x slower                                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                                            |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251023-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-eb73378 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none_tg         | 446 ms                                                 | 244 ms: 1.83x faster                                                    |
| async_tree_memoization_tg  | 560 ms                                                 | 306 ms: 1.83x faster                                                    |
| async_tree_io              | 1.08 sec                                               | 594 ms: 1.82x faster                                                    |
| async_tree_io_tg           | 1.11 sec                                               | 611 ms: 1.82x faster                                                    |
| async_tree_none            | 464 ms                                                 | 258 ms: 1.80x faster                                                    |
| async_tree_memoization     | 555 ms                                                 | 308 ms: 1.80x faster                                                    |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 475 ms: 1.52x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 474 ms: 1.51x faster                                                    |
| async_generators           | 384 ms                                                 | 338 ms: 1.14x faster                                                    |
| coroutines                 | 23.9 ms                                                | 22.3 ms: 1.07x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.51x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251023-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-eb73378 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 62.7 ms: 1.29x faster                                                   |
| nbody          | 89.3 ms                                                | 83.3 ms: 1.07x faster                                                   |
| pidigits       | 184 ms                                                 | 192 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                  | 1.10x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251023-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-eb73378 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 137 ms: 1.04x faster                                                    |
| regex_effbot   | 3.17 ms                                                | 3.14 ms: 1.01x faster                                                   |
| regex_v8       | 20.6 ms                                                | 23.0 ms: 1.12x slower                                                   |
| regex_dna      | 168 ms                                                 | 191 ms: 1.14x slower                                                    |
| Geometric mean | (ref)                                                  | 1.05x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251023-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-eb73378 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| unpickle_pure_python | 221 us                                                 | 183 us: 1.21x faster                                                    |
| json_dumps           | 10.4 ms                                                | 8.66 ms: 1.20x faster                                                   |
| tomli_loads          | 2.11 sec                                               | 1.77 sec: 1.19x faster                                                  |
| xml_etree_process    | 59.0 ms                                                | 52.2 ms: 1.13x faster                                                   |
| xml_etree_generate   | 85.2 ms                                                | 75.9 ms: 1.12x faster                                                   |
| xml_etree_iterparse  | 96.7 ms                                                | 93.6 ms: 1.03x faster                                                   |
| json_loads           | 26.5 us                                                | 25.7 us: 1.03x faster                                                   |
| xml_etree_parse      | 139 ms                                                 | 143 ms: 1.03x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.09x faster                                                            |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251023-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-eb73378 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.37 ms: 1.03x slower                                                   |
| python_startup         | 9.93 ms                                                | 12.6 ms: 1.27x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.15x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251023-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-eb73378 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 20.1 ms: 1.14x faster                                                   |
| django_template | 34.7 ms                                                | 33.4 ms: 1.04x faster                                                   |
| mako            | 11.0 ms                                                | 11.3 ms: 1.03x slower                                                   |
| Geometric mean  | (ref)                                                  | 1.03x faster                                                            |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251023-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-eb73378 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.17 sec: 2.06x faster                                                  |
| richards                   | 45.9 ms                                                | 22.6 ms: 2.03x faster                                                   |
| richards_super             | 51.9 ms                                                | 26.5 ms: 1.96x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 244 ms: 1.83x faster                                                    |
| async_tree_memoization_tg  | 560 ms                                                 | 306 ms: 1.83x faster                                                    |
| deepcopy_memo              | 40.3 us                                                | 22.0 us: 1.83x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 594 ms: 1.82x faster                                                    |
| async_tree_io_tg           | 1.11 sec                                               | 611 ms: 1.82x faster                                                    |
| async_tree_none            | 464 ms                                                 | 258 ms: 1.80x faster                                                    |
| async_tree_memoization     | 555 ms                                                 | 308 ms: 1.80x faster                                                    |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 475 ms: 1.52x faster                                                    |
| deepcopy                   | 352 us                                                 | 231 us: 1.52x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 474 ms: 1.51x faster                                                    |
| logging_silent             | 109 ns                                                 | 76.9 ns: 1.42x faster                                                   |
| scimark_fft                | 342 ms                                                 | 242 ms: 1.41x faster                                                    |
| comprehensions             | 19.8 us                                                | 14.4 us: 1.38x faster                                                   |
| scimark_sor                | 130 ms                                                 | 99.2 ms: 1.31x faster                                                   |
| spectral_norm              | 110 ms                                                 | 84.3 ms: 1.31x faster                                                   |
| deepcopy_reduce            | 3.08 us                                                | 2.37 us: 1.30x faster                                                   |
| float                      | 80.8 ms                                                | 62.7 ms: 1.29x faster                                                   |
| scimark_monte_carlo        | 68.4 ms                                                | 54.8 ms: 1.25x faster                                                   |
| deltablue                  | 3.45 ms                                                | 2.76 ms: 1.25x faster                                                   |
| bpe_tokeniser              | 4.74 sec                                               | 3.90 sec: 1.21x faster                                                  |
| unpickle_pure_python       | 221 us                                                 | 183 us: 1.21x faster                                                    |
| json_dumps                 | 10.4 ms                                                | 8.66 ms: 1.20x faster                                                   |
| tomli_loads                | 2.11 sec                                               | 1.77 sec: 1.19x faster                                                  |
| crypto_pyaes               | 76.6 ms                                                | 64.3 ms: 1.19x faster                                                   |
| scimark_lu                 | 114 ms                                                 | 95.9 ms: 1.19x faster                                                   |
| chaos                      | 62.8 ms                                                | 52.9 ms: 1.19x faster                                                   |
| go                         | 139 ms                                                 | 120 ms: 1.16x faster                                                    |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 3.80 ms: 1.16x faster                                                   |
| generators                 | 32.2 ms                                                | 28.1 ms: 1.15x faster                                                   |
| pyflate                    | 448 ms                                                 | 390 ms: 1.15x faster                                                    |
| async_generators           | 384 ms                                                 | 338 ms: 1.14x faster                                                    |
| pylint                     | 319 ms                                                 | 280 ms: 1.14x faster                                                    |
| genshi_text                | 22.8 ms                                                | 20.1 ms: 1.14x faster                                                   |
| pprint_safe_repr           | 743 ms                                                 | 655 ms: 1.13x faster                                                    |
| xml_etree_process          | 59.0 ms                                                | 52.2 ms: 1.13x faster                                                   |
| xml_etree_generate         | 85.2 ms                                                | 75.9 ms: 1.12x faster                                                   |
| pathlib                    | 21.5 ms                                                | 19.2 ms: 1.12x faster                                                   |
| logging_simple             | 6.63 us                                                | 5.91 us: 1.12x faster                                                   |
| raytrace                   | 299 ms                                                 | 268 ms: 1.12x faster                                                    |
| typing_runtime_protocols   | 163 us                                                 | 147 us: 1.11x faster                                                    |
| logging_format             | 7.35 us                                                | 6.60 us: 1.11x faster                                                   |
| sympy_integrate            | 20.5 ms                                                | 18.5 ms: 1.11x faster                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.38 sec: 1.10x faster                                                  |
| sympy_sum                  | 166 ms                                                 | 153 ms: 1.08x faster                                                    |
| nbody                      | 89.3 ms                                                | 83.3 ms: 1.07x faster                                                   |
| coroutines                 | 23.9 ms                                                | 22.3 ms: 1.07x faster                                                   |
| thrift                     | 791 us                                                 | 739 us: 1.07x faster                                                    |
| hexiom                     | 6.17 ms                                                | 5.78 ms: 1.07x faster                                                   |
| dulwich_log                | 78.9 ms                                                | 74.1 ms: 1.06x faster                                                   |
| sympy_str                  | 292 ms                                                 | 275 ms: 1.06x faster                                                    |
| 2to3                       | 264 ms                                                 | 249 ms: 1.06x faster                                                    |
| fannkuch                   | 372 ms                                                 | 358 ms: 1.04x faster                                                    |
| django_template            | 34.7 ms                                                | 33.4 ms: 1.04x faster                                                   |
| regex_compile              | 142 ms                                                 | 137 ms: 1.04x faster                                                    |
| xml_etree_iterparse        | 96.7 ms                                                | 93.6 ms: 1.03x faster                                                   |
| json_loads                 | 26.5 us                                                | 25.7 us: 1.03x faster                                                   |
| json                       | 5.02 ms                                                | 4.88 ms: 1.03x faster                                                   |
| sqlite_synth               | 2.20 us                                                | 2.15 us: 1.02x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 3.14 ms: 1.01x faster                                                   |
| docutils                   | 2.64 sec                                               | 2.65 sec: 1.00x slower                                                  |
| meteor_contest             | 104 ms                                                 | 104 ms: 1.01x slower                                                    |
| nqueens                    | 80.1 ms                                                | 80.9 ms: 1.01x slower                                                   |
| mako                       | 11.0 ms                                                | 11.3 ms: 1.03x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 7.37 ms: 1.03x slower                                                   |
| bench_thread_pool          | 941 us                                                 | 970 us: 1.03x slower                                                    |
| xml_etree_parse            | 139 ms                                                 | 143 ms: 1.03x slower                                                    |
| pidigits                   | 184 ms                                                 | 192 ms: 1.04x slower                                                    |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                    |
| coverage                   | 71.4 ms                                                | 75.5 ms: 1.06x slower                                                   |
| regex_v8                   | 20.6 ms                                                | 23.0 ms: 1.12x slower                                                   |
| regex_dna                  | 168 ms                                                 | 191 ms: 1.14x slower                                                    |
| bench_mp_pool              | 10.8 ms                                                | 12.3 ms: 1.14x slower                                                   |
| gc_traversal               | 3.46 ms                                                | 4.35 ms: 1.26x slower                                                   |
| python_startup             | 9.93 ms                                                | 12.6 ms: 1.27x slower                                                   |
| create_gc_cycles           | 1.09 ms                                                | 2.01 ms: 1.84x slower                                                   |
| telco                      | 6.53 ms                                                | 157 ms: 24.05x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.12x faster                                                            |

Benchmark hidden because not significant (5): pickle_pure_python, pycparser, genshi_xml, sympy_expand, html5lib
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251023-3.15.0a1+-eb73378-CLANG,JIT/bm-20251023-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-eb73378.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.118x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.22x