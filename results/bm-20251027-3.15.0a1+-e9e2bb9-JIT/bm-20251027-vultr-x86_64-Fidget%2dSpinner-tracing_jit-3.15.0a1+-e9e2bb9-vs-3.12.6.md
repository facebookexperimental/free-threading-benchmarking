# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: e9e2bb9
- commit date: 2025-10-27
- overall geometric mean: 1.084x faster
- HPT reliability: 99.98%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251027-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-e9e2bb9 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 251 ms: 1.05x faster                                                    |
| docutils       | 2.64 sec                                               | 2.80 sec: 1.06x slower                                                  |
| html5lib       | 63.6 ms                                                | 69.0 ms: 1.09x slower                                                   |
| Geometric mean | (ref)                                                  | 1.03x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251027-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-e9e2bb9 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io              | 1.08 sec                                               | 559 ms: 1.94x faster                                                    |
| async_tree_none            | 464 ms                                                 | 247 ms: 1.88x faster                                                    |
| async_tree_io_tg           | 1.11 sec                                               | 599 ms: 1.85x faster                                                    |
| async_tree_none_tg         | 446 ms                                                 | 248 ms: 1.80x faster                                                    |
| async_tree_memoization_tg  | 560 ms                                                 | 311 ms: 1.80x faster                                                    |
| async_tree_memoization     | 555 ms                                                 | 310 ms: 1.79x faster                                                    |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 491 ms: 1.47x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 494 ms: 1.45x faster                                                    |
| async_generators           | 384 ms                                                 | 364 ms: 1.06x faster                                                    |
| coroutines                 | 23.9 ms                                                | 24.5 ms: 1.02x slower                                                   |
| asyncio_websockets         | 517 ms                                                 | 545 ms: 1.05x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.49x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251027-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-e9e2bb9 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 60.6 ms: 1.33x faster                                                   |
| nbody          | 89.3 ms                                                | 84.1 ms: 1.06x faster                                                   |
| pidigits       | 184 ms                                                 | 198 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                  | 1.10x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251027-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-e9e2bb9 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.78 ms: 1.14x faster                                                   |
| regex_compile  | 142 ms                                                 | 128 ms: 1.11x faster                                                    |
| regex_v8       | 20.6 ms                                                | 22.6 ms: 1.10x slower                                                   |
| regex_dna      | 168 ms                                                 | 185 ms: 1.10x slower                                                    |
| Geometric mean | (ref)                                                  | 1.01x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251027-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-e9e2bb9 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| unpickle_pure_python | 221 us                                                 | 186 us: 1.19x faster                                                    |
| xml_etree_iterparse  | 96.7 ms                                                | 83.4 ms: 1.16x faster                                                   |
| tomli_loads          | 2.11 sec                                               | 1.86 sec: 1.13x faster                                                  |
| json_dumps           | 10.4 ms                                                | 9.42 ms: 1.10x faster                                                   |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.08x faster                                                    |
| xml_etree_generate   | 85.2 ms                                                | 80.1 ms: 1.06x faster                                                   |
| xml_etree_process    | 59.0 ms                                                | 56.6 ms: 1.04x faster                                                   |
| pickle_pure_python   | 308 us                                                 | 305 us: 1.01x faster                                                    |
| json_loads           | 26.5 us                                                | 27.9 us: 1.05x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.08x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251027-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-e9e2bb9 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.24 ms: 1.01x slower                                                   |
| python_startup         | 9.93 ms                                                | 12.4 ms: 1.25x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.13x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251027-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-e9e2bb9 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 21.2 ms: 1.08x faster                                                   |
| mako            | 11.0 ms                                                | 10.5 ms: 1.05x faster                                                   |
| genshi_xml      | 50.2 ms                                                | 54.4 ms: 1.08x slower                                                   |
| django_template | 34.7 ms                                                | 39.6 ms: 1.14x slower                                                   |
| Geometric mean  | (ref)                                                  | 1.02x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251027-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-e9e2bb9 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| richards                   | 45.9 ms                                                | 21.2 ms: 2.17x faster                                                   |
| richards_super             | 51.9 ms                                                | 25.8 ms: 2.01x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 559 ms: 1.94x faster                                                    |
| async_tree_none            | 464 ms                                                 | 247 ms: 1.88x faster                                                    |
| async_tree_io_tg           | 1.11 sec                                               | 599 ms: 1.85x faster                                                    |
| mdp                        | 2.42 sec                                               | 1.33 sec: 1.82x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 248 ms: 1.80x faster                                                    |
| async_tree_memoization_tg  | 560 ms                                                 | 311 ms: 1.80x faster                                                    |
| async_tree_memoization     | 555 ms                                                 | 310 ms: 1.79x faster                                                    |
| deepcopy_memo              | 40.3 us                                                | 23.4 us: 1.72x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 491 ms: 1.47x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 494 ms: 1.45x faster                                                    |
| deepcopy                   | 352 us                                                 | 257 us: 1.37x faster                                                    |
| float                      | 80.8 ms                                                | 60.6 ms: 1.33x faster                                                   |
| scimark_fft                | 342 ms                                                 | 260 ms: 1.32x faster                                                    |
| spectral_norm              | 110 ms                                                 | 84.0 ms: 1.31x faster                                                   |
| scimark_sor                | 130 ms                                                 | 99.8 ms: 1.30x faster                                                   |
| comprehensions             | 19.8 us                                                | 16.1 us: 1.23x faster                                                   |
| logging_silent             | 109 ns                                                 | 88.3 ns: 1.23x faster                                                   |
| deltablue                  | 3.45 ms                                                | 2.89 ms: 1.19x faster                                                   |
| go                         | 139 ms                                                 | 117 ms: 1.19x faster                                                    |
| unpickle_pure_python       | 221 us                                                 | 186 us: 1.19x faster                                                    |
| scimark_monte_carlo        | 68.4 ms                                                | 57.8 ms: 1.18x faster                                                   |
| deepcopy_reduce            | 3.08 us                                                | 2.61 us: 1.18x faster                                                   |
| bpe_tokeniser              | 4.74 sec                                               | 4.06 sec: 1.17x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 83.4 ms: 1.16x faster                                                   |
| pyflate                    | 448 ms                                                 | 387 ms: 1.16x faster                                                    |
| chaos                      | 62.8 ms                                                | 54.8 ms: 1.15x faster                                                   |
| crypto_pyaes               | 76.6 ms                                                | 66.9 ms: 1.15x faster                                                   |
| generators                 | 32.2 ms                                                | 28.3 ms: 1.14x faster                                                   |
| regex_effbot               | 3.17 ms                                                | 2.78 ms: 1.14x faster                                                   |
| tomli_loads                | 2.11 sec                                               | 1.86 sec: 1.13x faster                                                  |
| pathlib                    | 21.5 ms                                                | 19.1 ms: 1.13x faster                                                   |
| scimark_lu                 | 114 ms                                                 | 102 ms: 1.11x faster                                                    |
| regex_compile              | 142 ms                                                 | 128 ms: 1.11x faster                                                    |
| json_dumps                 | 10.4 ms                                                | 9.42 ms: 1.10x faster                                                   |
| logging_simple             | 6.63 us                                                | 6.13 us: 1.08x faster                                                   |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.08x faster                                                    |
| logging_format             | 7.35 us                                                | 6.81 us: 1.08x faster                                                   |
| genshi_text                | 22.8 ms                                                | 21.2 ms: 1.08x faster                                                   |
| pprint_safe_repr           | 743 ms                                                 | 692 ms: 1.07x faster                                                    |
| dulwich_log                | 78.9 ms                                                | 73.7 ms: 1.07x faster                                                   |
| raytrace                   | 299 ms                                                 | 281 ms: 1.07x faster                                                    |
| xml_etree_generate         | 85.2 ms                                                | 80.1 ms: 1.06x faster                                                   |
| nbody                      | 89.3 ms                                                | 84.1 ms: 1.06x faster                                                   |
| async_generators           | 384 ms                                                 | 364 ms: 1.06x faster                                                    |
| mako                       | 11.0 ms                                                | 10.5 ms: 1.05x faster                                                   |
| 2to3                       | 264 ms                                                 | 251 ms: 1.05x faster                                                    |
| xml_etree_process          | 59.0 ms                                                | 56.6 ms: 1.04x faster                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.47 sec: 1.03x faster                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.25 ms: 1.03x faster                                                   |
| json                       | 5.02 ms                                                | 4.88 ms: 1.03x faster                                                   |
| meteor_contest             | 104 ms                                                 | 102 ms: 1.02x faster                                                    |
| thrift                     | 791 us                                                 | 777 us: 1.02x faster                                                    |
| typing_runtime_protocols   | 163 us                                                 | 160 us: 1.02x faster                                                    |
| pickle_pure_python         | 308 us                                                 | 305 us: 1.01x faster                                                    |
| sqlite_synth               | 2.20 us                                                | 2.19 us: 1.01x faster                                                   |
| python_startup_no_site     | 7.16 ms                                                | 7.24 ms: 1.01x slower                                                   |
| sympy_sum                  | 166 ms                                                 | 170 ms: 1.02x slower                                                    |
| coroutines                 | 23.9 ms                                                | 24.5 ms: 1.02x slower                                                   |
| hexiom                     | 6.17 ms                                                | 6.40 ms: 1.04x slower                                                   |
| json_loads                 | 26.5 us                                                | 27.9 us: 1.05x slower                                                   |
| asyncio_websockets         | 517 ms                                                 | 545 ms: 1.05x slower                                                    |
| docutils                   | 2.64 sec                                               | 2.80 sec: 1.06x slower                                                  |
| sympy_str                  | 292 ms                                                 | 310 ms: 1.06x slower                                                    |
| pidigits                   | 184 ms                                                 | 198 ms: 1.07x slower                                                    |
| bench_thread_pool          | 941 us                                                 | 1.01 ms: 1.08x slower                                                   |
| genshi_xml                 | 50.2 ms                                                | 54.4 ms: 1.08x slower                                                   |
| html5lib                   | 63.6 ms                                                | 69.0 ms: 1.09x slower                                                   |
| nqueens                    | 80.1 ms                                                | 87.3 ms: 1.09x slower                                                   |
| regex_v8                   | 20.6 ms                                                | 22.6 ms: 1.10x slower                                                   |
| regex_dna                  | 168 ms                                                 | 185 ms: 1.10x slower                                                    |
| sympy_expand               | 468 ms                                                 | 522 ms: 1.12x slower                                                    |
| django_template            | 34.7 ms                                                | 39.6 ms: 1.14x slower                                                   |
| coverage                   | 71.4 ms                                                | 82.3 ms: 1.15x slower                                                   |
| bench_mp_pool              | 10.8 ms                                                | 12.5 ms: 1.16x slower                                                   |
| python_startup             | 9.93 ms                                                | 12.4 ms: 1.25x slower                                                   |
| gc_traversal               | 3.46 ms                                                | 4.78 ms: 1.38x slower                                                   |
| create_gc_cycles           | 1.09 ms                                                | 1.92 ms: 1.76x slower                                                   |
| telco                      | 6.53 ms                                                | 164 ms: 25.17x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.08x faster                                                            |

Benchmark hidden because not significant (4): pycparser, pylint, sympy_integrate, fannkuch
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251027-3.15.0a1+-e9e2bb9-JIT/bm-20251027-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-e9e2bb9.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.084x faster

# HPT report

- Reliability score: 99.98% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.19x