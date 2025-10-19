# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: 9bb03a8
- commit date: 2025-10-19
- overall geometric mean: 1.113x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-9bb03a8 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 251 ms: 1.05x faster                                                    |
| docutils       | 2.64 sec                                               | 2.57 sec: 1.03x faster                                                  |
| html5lib       | 63.6 ms                                                | 65.7 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                  | 1.01x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-9bb03a8 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io              | 1.08 sec                                               | 588 ms: 1.84x faster                                                    |
| async_tree_none_tg         | 446 ms                                                 | 243 ms: 1.84x faster                                                    |
| async_tree_memoization_tg  | 560 ms                                                 | 305 ms: 1.83x faster                                                    |
| async_tree_memoization     | 555 ms                                                 | 303 ms: 1.83x faster                                                    |
| async_tree_io_tg           | 1.11 sec                                               | 608 ms: 1.83x faster                                                    |
| async_tree_none            | 464 ms                                                 | 256 ms: 1.82x faster                                                    |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 469 ms: 1.54x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 469 ms: 1.52x faster                                                    |
| async_generators           | 384 ms                                                 | 331 ms: 1.16x faster                                                    |
| coroutines                 | 23.9 ms                                                | 22.7 ms: 1.05x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 545 ms: 1.05x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.52x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-9bb03a8 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 62.2 ms: 1.30x faster                                                   |
| nbody          | 89.3 ms                                                | 87.3 ms: 1.02x faster                                                   |
| pidigits       | 184 ms                                                 | 192 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                  | 1.08x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-9bb03a8 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.94 ms: 1.08x faster                                                   |
| regex_compile  | 142 ms                                                 | 136 ms: 1.04x faster                                                    |
| regex_v8       | 20.6 ms                                                | 21.6 ms: 1.05x slower                                                   |
| regex_dna      | 168 ms                                                 | 177 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                  | 1.00x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-9bb03a8 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| unpickle_pure_python | 221 us                                                 | 183 us: 1.21x faster                                                    |
| tomli_loads          | 2.11 sec                                               | 1.76 sec: 1.20x faster                                                  |
| json_dumps           | 10.4 ms                                                | 8.87 ms: 1.17x faster                                                   |
| xml_etree_process    | 59.0 ms                                                | 52.0 ms: 1.13x faster                                                   |
| xml_etree_generate   | 85.2 ms                                                | 76.2 ms: 1.12x faster                                                   |
| xml_etree_iterparse  | 96.7 ms                                                | 93.5 ms: 1.03x faster                                                   |
| json_loads           | 26.5 us                                                | 26.0 us: 1.02x faster                                                   |
| pickle_pure_python   | 308 us                                                 | 302 us: 1.02x faster                                                    |
| xml_etree_parse      | 139 ms                                                 | 144 ms: 1.04x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.09x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-9bb03a8 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.39 ms: 1.03x slower                                                   |
| python_startup         | 9.93 ms                                                | 12.7 ms: 1.28x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.15x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-9bb03a8 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 20.0 ms: 1.14x faster                                                   |
| genshi_xml      | 50.2 ms                                                | 49.4 ms: 1.02x faster                                                   |
| django_template | 34.7 ms                                                | 35.2 ms: 1.01x slower                                                   |
| mako            | 11.0 ms                                                | 11.4 ms: 1.04x slower                                                   |
| Geometric mean  | (ref)                                                  | 1.02x faster                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-9bb03a8 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.18 sec: 2.06x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 588 ms: 1.84x faster                                                    |
| deepcopy_memo              | 40.3 us                                                | 21.9 us: 1.84x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 243 ms: 1.84x faster                                                    |
| async_tree_memoization_tg  | 560 ms                                                 | 305 ms: 1.83x faster                                                    |
| async_tree_memoization     | 555 ms                                                 | 303 ms: 1.83x faster                                                    |
| async_tree_io_tg           | 1.11 sec                                               | 608 ms: 1.83x faster                                                    |
| async_tree_none            | 464 ms                                                 | 256 ms: 1.82x faster                                                    |
| richards                   | 45.9 ms                                                | 29.0 ms: 1.59x faster                                                   |
| richards_super             | 51.9 ms                                                | 33.5 ms: 1.55x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 469 ms: 1.54x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 469 ms: 1.52x faster                                                    |
| deepcopy                   | 352 us                                                 | 233 us: 1.51x faster                                                    |
| scimark_fft                | 342 ms                                                 | 242 ms: 1.41x faster                                                    |
| logging_silent             | 109 ns                                                 | 78.0 ns: 1.40x faster                                                   |
| comprehensions             | 19.8 us                                                | 14.7 us: 1.35x faster                                                   |
| spectral_norm              | 110 ms                                                 | 83.1 ms: 1.33x faster                                                   |
| scimark_sor                | 130 ms                                                 | 98.8 ms: 1.31x faster                                                   |
| float                      | 80.8 ms                                                | 62.2 ms: 1.30x faster                                                   |
| deepcopy_reduce            | 3.08 us                                                | 2.38 us: 1.29x faster                                                   |
| deltablue                  | 3.45 ms                                                | 2.78 ms: 1.24x faster                                                   |
| scimark_monte_carlo        | 68.4 ms                                                | 55.5 ms: 1.23x faster                                                   |
| unpickle_pure_python       | 221 us                                                 | 183 us: 1.21x faster                                                    |
| chaos                      | 62.8 ms                                                | 52.3 ms: 1.20x faster                                                   |
| tomli_loads                | 2.11 sec                                               | 1.76 sec: 1.20x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 3.97 sec: 1.19x faster                                                  |
| crypto_pyaes               | 76.6 ms                                                | 64.6 ms: 1.19x faster                                                   |
| json_dumps                 | 10.4 ms                                                | 8.87 ms: 1.17x faster                                                   |
| async_generators           | 384 ms                                                 | 331 ms: 1.16x faster                                                    |
| go                         | 139 ms                                                 | 120 ms: 1.16x faster                                                    |
| generators                 | 32.2 ms                                                | 27.9 ms: 1.16x faster                                                   |
| pylint                     | 319 ms                                                 | 276 ms: 1.15x faster                                                    |
| pyflate                    | 448 ms                                                 | 391 ms: 1.15x faster                                                    |
| pprint_safe_repr           | 743 ms                                                 | 649 ms: 1.14x faster                                                    |
| genshi_text                | 22.8 ms                                                | 20.0 ms: 1.14x faster                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.34 sec: 1.14x faster                                                  |
| xml_etree_process          | 59.0 ms                                                | 52.0 ms: 1.13x faster                                                   |
| scimark_lu                 | 114 ms                                                 | 101 ms: 1.13x faster                                                    |
| logging_simple             | 6.63 us                                                | 5.88 us: 1.13x faster                                                   |
| raytrace                   | 299 ms                                                 | 267 ms: 1.12x faster                                                    |
| logging_format             | 7.35 us                                                | 6.57 us: 1.12x faster                                                   |
| xml_etree_generate         | 85.2 ms                                                | 76.2 ms: 1.12x faster                                                   |
| pathlib                    | 21.5 ms                                                | 19.3 ms: 1.12x faster                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 3.95 ms: 1.11x faster                                                   |
| typing_runtime_protocols   | 163 us                                                 | 147 us: 1.11x faster                                                    |
| sympy_integrate            | 20.5 ms                                                | 18.7 ms: 1.10x faster                                                   |
| sympy_sum                  | 166 ms                                                 | 154 ms: 1.08x faster                                                    |
| hexiom                     | 6.17 ms                                                | 5.74 ms: 1.08x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 2.94 ms: 1.08x faster                                                   |
| thrift                     | 791 us                                                 | 744 us: 1.06x faster                                                    |
| dulwich_log                | 78.9 ms                                                | 74.6 ms: 1.06x faster                                                   |
| coroutines                 | 23.9 ms                                                | 22.7 ms: 1.05x faster                                                   |
| fannkuch                   | 372 ms                                                 | 355 ms: 1.05x faster                                                    |
| 2to3                       | 264 ms                                                 | 251 ms: 1.05x faster                                                    |
| regex_compile              | 142 ms                                                 | 136 ms: 1.04x faster                                                    |
| sympy_str                  | 292 ms                                                 | 280 ms: 1.04x faster                                                    |
| pycparser                  | 1.17 sec                                               | 1.13 sec: 1.04x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 93.5 ms: 1.03x faster                                                   |
| sqlite_synth               | 2.20 us                                                | 2.14 us: 1.03x faster                                                   |
| docutils                   | 2.64 sec                                               | 2.57 sec: 1.03x faster                                                  |
| json                       | 5.02 ms                                                | 4.90 ms: 1.02x faster                                                   |
| nbody                      | 89.3 ms                                                | 87.3 ms: 1.02x faster                                                   |
| json_loads                 | 26.5 us                                                | 26.0 us: 1.02x faster                                                   |
| pickle_pure_python         | 308 us                                                 | 302 us: 1.02x faster                                                    |
| genshi_xml                 | 50.2 ms                                                | 49.4 ms: 1.02x faster                                                   |
| meteor_contest             | 104 ms                                                 | 104 ms: 1.01x slower                                                    |
| django_template            | 34.7 ms                                                | 35.2 ms: 1.01x slower                                                   |
| bench_thread_pool          | 941 us                                                 | 963 us: 1.02x slower                                                    |
| sympy_expand               | 468 ms                                                 | 479 ms: 1.02x slower                                                    |
| python_startup_no_site     | 7.16 ms                                                | 7.39 ms: 1.03x slower                                                   |
| html5lib                   | 63.6 ms                                                | 65.7 ms: 1.03x slower                                                   |
| xml_etree_parse            | 139 ms                                                 | 144 ms: 1.04x slower                                                    |
| mako                       | 11.0 ms                                                | 11.4 ms: 1.04x slower                                                   |
| pidigits                   | 184 ms                                                 | 192 ms: 1.04x slower                                                    |
| coverage                   | 71.4 ms                                                | 74.5 ms: 1.04x slower                                                   |
| regex_v8                   | 20.6 ms                                                | 21.6 ms: 1.05x slower                                                   |
| asyncio_websockets         | 517 ms                                                 | 545 ms: 1.05x slower                                                    |
| regex_dna                  | 168 ms                                                 | 177 ms: 1.06x slower                                                    |
| bench_mp_pool              | 10.8 ms                                                | 12.3 ms: 1.14x slower                                                   |
| gc_traversal               | 3.46 ms                                                | 4.27 ms: 1.24x slower                                                   |
| python_startup             | 9.93 ms                                                | 12.7 ms: 1.28x slower                                                   |
| create_gc_cycles           | 1.09 ms                                                | 2.03 ms: 1.86x slower                                                   |
| telco                      | 6.53 ms                                                | 158 ms: 24.14x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.11x faster                                                            |

Benchmark hidden because not significant (1): nqueens
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251019-3.15.0a1+-9bb03a8-CLANG,JIT/bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-9bb03a8.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.113x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.22x