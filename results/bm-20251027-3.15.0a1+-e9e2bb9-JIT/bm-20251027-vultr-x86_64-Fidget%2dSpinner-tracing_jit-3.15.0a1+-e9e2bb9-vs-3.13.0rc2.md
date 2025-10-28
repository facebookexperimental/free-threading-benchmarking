# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: e9e2bb9
- commit date: 2025-10-27
- overall geometric mean: 1.047x faster
- HPT reliability: 99.93%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251027-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-e9e2bb9 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 251 ms: 1.03x faster                                                    |
| docutils       | 2.62 sec                                                     | 2.80 sec: 1.07x slower                                                  |
| html5lib       | 67.0 ms                                                      | 69.0 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                        | 1.02x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251027-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-e9e2bb9 |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io              | 876 ms                                                       | 559 ms: 1.57x faster                                                    |
| async_tree_io_tg           | 913 ms                                                       | 599 ms: 1.53x faster                                                    |
| async_tree_memoization     | 461 ms                                                       | 310 ms: 1.49x faster                                                    |
| async_tree_none            | 354 ms                                                       | 247 ms: 1.43x faster                                                    |
| async_tree_none_tg         | 336 ms                                                       | 248 ms: 1.36x faster                                                    |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 494 ms: 1.35x faster                                                    |
| async_tree_memoization_tg  | 414 ms                                                       | 311 ms: 1.33x faster                                                    |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 491 ms: 1.30x faster                                                    |
| async_generators           | 377 ms                                                       | 364 ms: 1.04x faster                                                    |
| coroutines                 | 23.6 ms                                                      | 24.5 ms: 1.04x slower                                                   |
| asyncio_websockets         | 520 ms                                                       | 545 ms: 1.05x slower                                                    |
| Geometric mean             | (ref)                                                        | 1.28x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251027-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-e9e2bb9 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 60.6 ms: 1.28x faster                                                   |
| pidigits       | 217 ms                                                       | 198 ms: 1.10x faster                                                    |
| nbody          | 85.1 ms                                                      | 84.1 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                        | 1.12x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251027-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-e9e2bb9 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.78 ms: 1.11x faster                                                   |
| regex_compile  | 132 ms                                                       | 128 ms: 1.03x faster                                                    |
| regex_v8       | 22.7 ms                                                      | 22.6 ms: 1.00x faster                                                   |
| regex_dna      | 180 ms                                                       | 185 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                        | 1.03x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251027-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-e9e2bb9 |
|----------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 83.4 ms: 1.14x faster                                                   |
| unpickle_pure_python | 210 us                                                       | 186 us: 1.13x faster                                                    |
| json_dumps           | 10.5 ms                                                      | 9.42 ms: 1.12x faster                                                   |
| tomli_loads          | 2.01 sec                                                     | 1.86 sec: 1.08x faster                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 80.1 ms: 1.07x faster                                                   |
| xml_etree_parse      | 136 ms                                                       | 128 ms: 1.06x faster                                                    |
| xml_etree_process    | 59.3 ms                                                      | 56.6 ms: 1.05x faster                                                   |
| pickle_pure_python   | 294 us                                                       | 305 us: 1.03x slower                                                    |
| json_loads           | 27.0 us                                                      | 27.9 us: 1.03x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.06x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251027-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-e9e2bb9 |
|------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.24 ms: 1.02x faster                                                   |
| python_startup         | 11.0 ms                                                      | 12.4 ms: 1.13x slower                                                   |
| Geometric mean         | (ref)                                                        | 1.05x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251027-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-e9e2bb9 |
|-----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 11.3 ms                                                      | 10.5 ms: 1.09x faster                                                   |
| genshi_text     | 21.5 ms                                                      | 21.2 ms: 1.02x faster                                                   |
| genshi_xml      | 48.8 ms                                                      | 54.4 ms: 1.12x slower                                                   |
| django_template | 34.1 ms                                                      | 39.6 ms: 1.16x slower                                                   |
| Geometric mean  | (ref)                                                        | 1.04x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251027-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-e9e2bb9 |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| richards                   | 45.2 ms                                                      | 21.2 ms: 2.13x faster                                                   |
| richards_super             | 51.6 ms                                                      | 25.8 ms: 2.00x faster                                                   |
| mdp                        | 2.36 sec                                                     | 1.33 sec: 1.77x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 23.4 us: 1.67x faster                                                   |
| async_tree_io              | 876 ms                                                       | 559 ms: 1.57x faster                                                    |
| async_tree_io_tg           | 913 ms                                                       | 599 ms: 1.53x faster                                                    |
| async_tree_memoization     | 461 ms                                                       | 310 ms: 1.49x faster                                                    |
| async_tree_none            | 354 ms                                                       | 247 ms: 1.43x faster                                                    |
| deepcopy                   | 355 us                                                       | 257 us: 1.38x faster                                                    |
| async_tree_none_tg         | 336 ms                                                       | 248 ms: 1.36x faster                                                    |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 494 ms: 1.35x faster                                                    |
| scimark_sor                | 134 ms                                                       | 99.8 ms: 1.35x faster                                                   |
| scimark_fft                | 349 ms                                                       | 260 ms: 1.35x faster                                                    |
| async_tree_memoization_tg  | 414 ms                                                       | 311 ms: 1.33x faster                                                    |
| spectral_norm              | 111 ms                                                       | 84.0 ms: 1.32x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 491 ms: 1.30x faster                                                    |
| float                      | 77.5 ms                                                      | 60.6 ms: 1.28x faster                                                   |
| go                         | 141 ms                                                       | 117 ms: 1.20x faster                                                    |
| deepcopy_reduce            | 3.11 us                                                      | 2.61 us: 1.19x faster                                                   |
| logging_silent             | 103 ns                                                       | 88.3 ns: 1.16x faster                                                   |
| pyflate                    | 449 ms                                                       | 387 ms: 1.16x faster                                                    |
| xml_etree_iterparse        | 94.9 ms                                                      | 83.4 ms: 1.14x faster                                                   |
| scimark_monte_carlo        | 65.4 ms                                                      | 57.8 ms: 1.13x faster                                                   |
| unpickle_pure_python       | 210 us                                                       | 186 us: 1.13x faster                                                    |
| json_dumps                 | 10.5 ms                                                      | 9.42 ms: 1.12x faster                                                   |
| regex_effbot               | 3.08 ms                                                      | 2.78 ms: 1.11x faster                                                   |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.25 ms: 1.11x faster                                                   |
| scimark_lu                 | 113 ms                                                       | 102 ms: 1.10x faster                                                    |
| pidigits                   | 217 ms                                                       | 198 ms: 1.10x faster                                                    |
| bpe_tokeniser              | 4.45 sec                                                     | 4.06 sec: 1.10x faster                                                  |
| mako                       | 11.3 ms                                                      | 10.5 ms: 1.09x faster                                                   |
| deltablue                  | 3.12 ms                                                      | 2.89 ms: 1.08x faster                                                   |
| tomli_loads                | 2.01 sec                                                     | 1.86 sec: 1.08x faster                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 80.1 ms: 1.07x faster                                                   |
| pprint_safe_repr           | 738 ms                                                       | 692 ms: 1.07x faster                                                    |
| xml_etree_parse            | 136 ms                                                       | 128 ms: 1.06x faster                                                    |
| xml_etree_process          | 59.3 ms                                                      | 56.6 ms: 1.05x faster                                                   |
| chaos                      | 57.3 ms                                                      | 54.8 ms: 1.05x faster                                                   |
| async_generators           | 377 ms                                                       | 364 ms: 1.04x faster                                                    |
| 2to3                       | 260 ms                                                       | 251 ms: 1.03x faster                                                    |
| regex_compile              | 132 ms                                                       | 128 ms: 1.03x faster                                                    |
| comprehensions             | 16.5 us                                                      | 16.1 us: 1.02x faster                                                   |
| python_startup_no_site     | 7.39 ms                                                      | 7.24 ms: 1.02x faster                                                   |
| pprint_pformat             | 1.50 sec                                                     | 1.47 sec: 1.02x faster                                                  |
| generators                 | 28.8 ms                                                      | 28.3 ms: 1.02x faster                                                   |
| genshi_text                | 21.5 ms                                                      | 21.2 ms: 1.02x faster                                                   |
| crypto_pyaes               | 67.9 ms                                                      | 66.9 ms: 1.02x faster                                                   |
| dulwich_log                | 74.8 ms                                                      | 73.7 ms: 1.02x faster                                                   |
| nbody                      | 85.1 ms                                                      | 84.1 ms: 1.01x faster                                                   |
| sqlite_synth               | 2.21 us                                                      | 2.19 us: 1.01x faster                                                   |
| json                       | 4.93 ms                                                      | 4.88 ms: 1.01x faster                                                   |
| coverage                   | 83.0 ms                                                      | 82.3 ms: 1.01x faster                                                   |
| regex_v8                   | 22.7 ms                                                      | 22.6 ms: 1.00x faster                                                   |
| regex_dna                  | 180 ms                                                       | 185 ms: 1.03x slower                                                    |
| html5lib                   | 67.0 ms                                                      | 69.0 ms: 1.03x slower                                                   |
| pickle_pure_python         | 294 us                                                       | 305 us: 1.03x slower                                                    |
| json_loads                 | 27.0 us                                                      | 27.9 us: 1.03x slower                                                   |
| sympy_integrate            | 19.8 ms                                                      | 20.5 ms: 1.04x slower                                                   |
| typing_runtime_protocols   | 155 us                                                       | 160 us: 1.04x slower                                                    |
| coroutines                 | 23.6 ms                                                      | 24.5 ms: 1.04x slower                                                   |
| pycparser                  | 1.12 sec                                                     | 1.17 sec: 1.05x slower                                                  |
| asyncio_websockets         | 520 ms                                                       | 545 ms: 1.05x slower                                                    |
| hexiom                     | 5.99 ms                                                      | 6.40 ms: 1.07x slower                                                   |
| docutils                   | 2.62 sec                                                     | 2.80 sec: 1.07x slower                                                  |
| sympy_sum                  | 156 ms                                                       | 170 ms: 1.09x slower                                                    |
| bench_thread_pool          | 919 us                                                       | 1.01 ms: 1.10x slower                                                   |
| raytrace                   | 253 ms                                                       | 281 ms: 1.11x slower                                                    |
| nqueens                    | 78.6 ms                                                      | 87.3 ms: 1.11x slower                                                   |
| genshi_xml                 | 48.8 ms                                                      | 54.4 ms: 1.12x slower                                                   |
| sympy_str                  | 275 ms                                                       | 310 ms: 1.13x slower                                                    |
| python_startup             | 11.0 ms                                                      | 12.4 ms: 1.13x slower                                                   |
| bench_mp_pool              | 11.0 ms                                                      | 12.5 ms: 1.13x slower                                                   |
| sympy_expand               | 457 ms                                                       | 522 ms: 1.14x slower                                                    |
| django_template            | 34.1 ms                                                      | 39.6 ms: 1.16x slower                                                   |
| create_gc_cycles           | 1.34 ms                                                      | 1.92 ms: 1.44x slower                                                   |
| gc_traversal               | 3.14 ms                                                      | 4.78 ms: 1.52x slower                                                   |
| telco                      | 7.82 ms                                                      | 164 ms: 20.99x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.05x faster                                                            |

Benchmark hidden because not significant (7): logging_simple, pathlib, logging_format, thrift, meteor_contest, pylint, fannkuch
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251027-3.15.0a1+-e9e2bb9-JIT/bm-20251027-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-e9e2bb9.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.047x faster

# HPT report

- Reliability score: 99.93% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.18x