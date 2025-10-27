# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: bdd2123
- commit date: 2025-10-27
- overall geometric mean: 1.047x faster
- HPT reliability: 99.91%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251027-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-bdd2123 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 253 ms: 1.03x faster                                                    |
| docutils       | 2.62 sec                                                     | 2.70 sec: 1.03x slower                                                  |
| html5lib       | 67.0 ms                                                      | 70.0 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                        | 1.02x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251027-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-bdd2123 |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io              | 876 ms                                                       | 563 ms: 1.56x faster                                                    |
| async_tree_io_tg           | 913 ms                                                       | 599 ms: 1.52x faster                                                    |
| async_tree_memoization     | 461 ms                                                       | 313 ms: 1.47x faster                                                    |
| async_tree_none            | 354 ms                                                       | 250 ms: 1.41x faster                                                    |
| async_tree_none_tg         | 336 ms                                                       | 248 ms: 1.36x faster                                                    |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 494 ms: 1.35x faster                                                    |
| async_tree_memoization_tg  | 414 ms                                                       | 311 ms: 1.33x faster                                                    |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 493 ms: 1.29x faster                                                    |
| async_generators           | 377 ms                                                       | 375 ms: 1.01x faster                                                    |
| coroutines                 | 23.6 ms                                                      | 24.0 ms: 1.02x slower                                                   |
| asyncio_websockets         | 520 ms                                                       | 546 ms: 1.05x slower                                                    |
| Geometric mean             | (ref)                                                        | 1.28x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251027-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-bdd2123 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 62.3 ms: 1.24x faster                                                   |
| pidigits       | 217 ms                                                       | 204 ms: 1.06x faster                                                    |
| nbody          | 85.1 ms                                                      | 90.5 ms: 1.06x slower                                                   |
| Geometric mean | (ref)                                                        | 1.07x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251027-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-bdd2123 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.79 ms: 1.11x faster                                                   |
| regex_dna      | 180 ms                                                       | 176 ms: 1.03x faster                                                    |
| regex_v8       | 22.7 ms                                                      | 22.1 ms: 1.02x faster                                                   |
| regex_compile  | 132 ms                                                       | 130 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                        | 1.04x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251027-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-bdd2123 |
|----------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| unpickle_pure_python | 210 us                                                       | 186 us: 1.13x faster                                                    |
| xml_etree_iterparse  | 94.9 ms                                                      | 85.1 ms: 1.12x faster                                                   |
| json_dumps           | 10.5 ms                                                      | 9.46 ms: 1.11x faster                                                   |
| tomli_loads          | 2.01 sec                                                     | 1.83 sec: 1.10x faster                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 80.6 ms: 1.06x faster                                                   |
| xml_etree_parse      | 136 ms                                                       | 130 ms: 1.05x faster                                                    |
| xml_etree_process    | 59.3 ms                                                      | 57.0 ms: 1.04x faster                                                   |
| pickle_pure_python   | 294 us                                                       | 299 us: 1.01x slower                                                    |
| json_loads           | 27.0 us                                                      | 27.8 us: 1.03x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.06x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251027-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-bdd2123 |
|------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.27 ms: 1.02x faster                                                   |
| python_startup         | 11.0 ms                                                      | 12.5 ms: 1.14x slower                                                   |
| Geometric mean         | (ref)                                                        | 1.06x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251027-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-bdd2123 |
|-----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 11.3 ms                                                      | 10.8 ms: 1.05x faster                                                   |
| django_template | 34.1 ms                                                      | 38.8 ms: 1.14x slower                                                   |
| genshi_xml      | 48.8 ms                                                      | 56.2 ms: 1.15x slower                                                   |
| Geometric mean  | (ref)                                                        | 1.06x slower                                                            |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251027-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-bdd2123 |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| richards                   | 45.2 ms                                                      | 20.8 ms: 2.18x faster                                                   |
| richards_super             | 51.6 ms                                                      | 25.2 ms: 2.05x faster                                                   |
| mdp                        | 2.36 sec                                                     | 1.27 sec: 1.85x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 23.3 us: 1.68x faster                                                   |
| async_tree_io              | 876 ms                                                       | 563 ms: 1.56x faster                                                    |
| async_tree_io_tg           | 913 ms                                                       | 599 ms: 1.52x faster                                                    |
| async_tree_memoization     | 461 ms                                                       | 313 ms: 1.47x faster                                                    |
| async_tree_none            | 354 ms                                                       | 250 ms: 1.41x faster                                                    |
| scimark_sor                | 134 ms                                                       | 97.0 ms: 1.39x faster                                                   |
| deepcopy                   | 355 us                                                       | 257 us: 1.38x faster                                                    |
| async_tree_none_tg         | 336 ms                                                       | 248 ms: 1.36x faster                                                    |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 494 ms: 1.35x faster                                                    |
| scimark_fft                | 349 ms                                                       | 260 ms: 1.34x faster                                                    |
| async_tree_memoization_tg  | 414 ms                                                       | 311 ms: 1.33x faster                                                    |
| spectral_norm              | 111 ms                                                       | 84.8 ms: 1.31x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 493 ms: 1.29x faster                                                    |
| float                      | 77.5 ms                                                      | 62.3 ms: 1.24x faster                                                   |
| go                         | 141 ms                                                       | 116 ms: 1.21x faster                                                    |
| deepcopy_reduce            | 3.11 us                                                      | 2.61 us: 1.19x faster                                                   |
| logging_silent             | 103 ns                                                       | 86.8 ns: 1.18x faster                                                   |
| pyflate                    | 449 ms                                                       | 393 ms: 1.14x faster                                                    |
| scimark_monte_carlo        | 65.4 ms                                                      | 57.9 ms: 1.13x faster                                                   |
| unpickle_pure_python       | 210 us                                                       | 186 us: 1.13x faster                                                    |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.22 ms: 1.12x faster                                                   |
| xml_etree_iterparse        | 94.9 ms                                                      | 85.1 ms: 1.12x faster                                                   |
| json_dumps                 | 10.5 ms                                                      | 9.46 ms: 1.11x faster                                                   |
| regex_effbot               | 3.08 ms                                                      | 2.79 ms: 1.11x faster                                                   |
| tomli_loads                | 2.01 sec                                                     | 1.83 sec: 1.10x faster                                                  |
| deltablue                  | 3.12 ms                                                      | 2.84 ms: 1.10x faster                                                   |
| bpe_tokeniser              | 4.45 sec                                                     | 4.06 sec: 1.10x faster                                                  |
| scimark_lu                 | 113 ms                                                       | 103 ms: 1.09x faster                                                    |
| pprint_safe_repr           | 738 ms                                                       | 683 ms: 1.08x faster                                                    |
| pidigits                   | 217 ms                                                       | 204 ms: 1.06x faster                                                    |
| xml_etree_generate         | 85.4 ms                                                      | 80.6 ms: 1.06x faster                                                   |
| chaos                      | 57.3 ms                                                      | 54.3 ms: 1.06x faster                                                   |
| mako                       | 11.3 ms                                                      | 10.8 ms: 1.05x faster                                                   |
| xml_etree_parse            | 136 ms                                                       | 130 ms: 1.05x faster                                                    |
| xml_etree_process          | 59.3 ms                                                      | 57.0 ms: 1.04x faster                                                   |
| pprint_pformat             | 1.50 sec                                                     | 1.45 sec: 1.03x faster                                                  |
| 2to3                       | 260 ms                                                       | 253 ms: 1.03x faster                                                    |
| regex_dna                  | 180 ms                                                       | 176 ms: 1.03x faster                                                    |
| regex_v8                   | 22.7 ms                                                      | 22.1 ms: 1.02x faster                                                   |
| comprehensions             | 16.5 us                                                      | 16.1 us: 1.02x faster                                                   |
| coverage                   | 83.0 ms                                                      | 81.5 ms: 1.02x faster                                                   |
| generators                 | 28.8 ms                                                      | 28.3 ms: 1.02x faster                                                   |
| regex_compile              | 132 ms                                                       | 130 ms: 1.02x faster                                                    |
| python_startup_no_site     | 7.39 ms                                                      | 7.27 ms: 1.02x faster                                                   |
| dulwich_log                | 74.8 ms                                                      | 73.8 ms: 1.01x faster                                                   |
| meteor_contest             | 102 ms                                                       | 100 ms: 1.01x faster                                                    |
| pathlib                    | 19.2 ms                                                      | 19.0 ms: 1.01x faster                                                   |
| async_generators           | 377 ms                                                       | 375 ms: 1.01x faster                                                    |
| sqlite_synth               | 2.21 us                                                      | 2.23 us: 1.01x slower                                                   |
| pickle_pure_python         | 294 us                                                       | 299 us: 1.01x slower                                                    |
| coroutines                 | 23.6 ms                                                      | 24.0 ms: 1.02x slower                                                   |
| thrift                     | 778 us                                                       | 794 us: 1.02x slower                                                    |
| sympy_integrate            | 19.8 ms                                                      | 20.3 ms: 1.02x slower                                                   |
| logging_format             | 6.84 us                                                      | 7.05 us: 1.03x slower                                                   |
| docutils                   | 2.62 sec                                                     | 2.70 sec: 1.03x slower                                                  |
| json_loads                 | 27.0 us                                                      | 27.8 us: 1.03x slower                                                   |
| typing_runtime_protocols   | 155 us                                                       | 161 us: 1.04x slower                                                    |
| html5lib                   | 67.0 ms                                                      | 70.0 ms: 1.04x slower                                                   |
| asyncio_websockets         | 520 ms                                                       | 546 ms: 1.05x slower                                                    |
| pycparser                  | 1.12 sec                                                     | 1.17 sec: 1.05x slower                                                  |
| hexiom                     | 5.99 ms                                                      | 6.31 ms: 1.05x slower                                                   |
| nbody                      | 85.1 ms                                                      | 90.5 ms: 1.06x slower                                                   |
| sympy_sum                  | 156 ms                                                       | 168 ms: 1.08x slower                                                    |
| raytrace                   | 253 ms                                                       | 278 ms: 1.10x slower                                                    |
| sympy_str                  | 275 ms                                                       | 304 ms: 1.11x slower                                                    |
| bench_thread_pool          | 919 us                                                       | 1.02 ms: 1.11x slower                                                   |
| nqueens                    | 78.6 ms                                                      | 88.0 ms: 1.12x slower                                                   |
| django_template            | 34.1 ms                                                      | 38.8 ms: 1.14x slower                                                   |
| python_startup             | 11.0 ms                                                      | 12.5 ms: 1.14x slower                                                   |
| sympy_expand               | 457 ms                                                       | 523 ms: 1.14x slower                                                    |
| bench_mp_pool              | 11.0 ms                                                      | 12.6 ms: 1.15x slower                                                   |
| genshi_xml                 | 48.8 ms                                                      | 56.2 ms: 1.15x slower                                                   |
| create_gc_cycles           | 1.34 ms                                                      | 1.93 ms: 1.44x slower                                                   |
| gc_traversal               | 3.14 ms                                                      | 4.88 ms: 1.55x slower                                                   |
| telco                      | 7.82 ms                                                      | 163 ms: 20.88x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.04x faster                                                            |

Benchmark hidden because not significant (6): pylint, logging_simple, fannkuch, crypto_pyaes, genshi_text, json
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251027-3.15.0a1+-bdd2123-JIT/bm-20251027-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-bdd2123.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.047x faster

# HPT report

- Reliability score: 99.91% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.18x