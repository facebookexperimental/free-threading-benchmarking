# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: dynamic_opcode_targe
- machine: linux-x86_64
- commit hash: 178b03e
- commit date: 2025-09-17
- overall geometric mean: 1.086x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250917-vultr-x86_64-Fidget%2dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 246 ms: 1.06x faster                                                            |
| docutils       | 2.62 sec                                                     | 2.48 sec: 1.05x faster                                                          |
| html5lib       | 67.0 ms                                                      | 60.1 ms: 1.11x faster                                                           |
| Geometric mean | (ref)                                                        | 1.07x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250917-vultr-x86_64-Fidget%2dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e |
|----------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_memoization     | 461 ms                                                       | 302 ms: 1.53x faster                                                            |
| async_tree_io_tg           | 913 ms                                                       | 608 ms: 1.50x faster                                                            |
| async_tree_io              | 876 ms                                                       | 586 ms: 1.50x faster                                                            |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 471 ms: 1.41x faster                                                            |
| async_tree_none_tg         | 336 ms                                                       | 242 ms: 1.39x faster                                                            |
| async_tree_none            | 354 ms                                                       | 256 ms: 1.38x faster                                                            |
| async_tree_memoization_tg  | 414 ms                                                       | 304 ms: 1.36x faster                                                            |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 473 ms: 1.35x faster                                                            |
| async_generators           | 377 ms                                                       | 317 ms: 1.19x faster                                                            |
| coroutines                 | 23.6 ms                                                      | 23.2 ms: 1.02x faster                                                           |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                            |
| Geometric mean             | (ref)                                                        | 1.32x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250917-vultr-x86_64-Fidget%2dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 67.2 ms: 1.15x faster                                                           |
| pidigits       | 217 ms                                                       | 194 ms: 1.11x faster                                                            |
| nbody          | 85.1 ms                                                      | 79.7 ms: 1.07x faster                                                           |
| Geometric mean | (ref)                                                        | 1.11x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250917-vultr-x86_64-Fidget%2dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 132 ms                                                       | 119 ms: 1.11x faster                                                            |
| regex_v8       | 22.7 ms                                                      | 21.2 ms: 1.07x faster                                                           |
| regex_effbot   | 3.08 ms                                                      | 2.95 ms: 1.05x faster                                                           |
| regex_dna      | 180 ms                                                       | 182 ms: 1.01x slower                                                            |
| Geometric mean | (ref)                                                        | 1.05x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250917-vultr-x86_64-Fidget%2dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e |
|----------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| json_dumps           | 10.5 ms                                                      | 8.84 ms: 1.19x faster                                                           |
| tomli_loads          | 2.01 sec                                                     | 1.80 sec: 1.11x faster                                                          |
| xml_etree_process    | 59.3 ms                                                      | 55.1 ms: 1.08x faster                                                           |
| xml_etree_generate   | 85.4 ms                                                      | 79.9 ms: 1.07x faster                                                           |
| json_loads           | 27.0 us                                                      | 25.5 us: 1.06x faster                                                           |
| unpickle_pure_python | 210 us                                                       | 200 us: 1.05x faster                                                            |
| pickle_pure_python   | 294 us                                                       | 298 us: 1.01x slower                                                            |
| xml_etree_parse      | 136 ms                                                       | 145 ms: 1.06x slower                                                            |
| Geometric mean       | (ref)                                                        | 1.05x faster                                                                    |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250917-vultr-x86_64-Fidget%2dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e |
|------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.34 ms: 1.01x faster                                                           |
| python_startup         | 11.0 ms                                                      | 12.6 ms: 1.15x slower                                                           |
| Geometric mean         | (ref)                                                        | 1.07x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250917-vultr-x86_64-Fidget%2dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e |
|-----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 19.1 ms: 1.13x faster                                                           |
| genshi_xml      | 48.8 ms                                                      | 45.1 ms: 1.08x faster                                                           |
| django_template | 34.1 ms                                                      | 32.3 ms: 1.06x faster                                                           |
| mako            | 11.3 ms                                                      | 11.6 ms: 1.02x slower                                                           |
| Geometric mean  | (ref)                                                        | 1.06x faster                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250917-vultr-x86_64-Fidget%2dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e |
|----------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.10 sec: 2.15x faster                                                          |
| deepcopy_memo              | 39.1 us                                                      | 24.6 us: 1.59x faster                                                           |
| deepcopy                   | 355 us                                                       | 225 us: 1.58x faster                                                            |
| async_tree_memoization     | 461 ms                                                       | 302 ms: 1.53x faster                                                            |
| async_tree_io_tg           | 913 ms                                                       | 608 ms: 1.50x faster                                                            |
| async_tree_io              | 876 ms                                                       | 586 ms: 1.50x faster                                                            |
| go                         | 141 ms                                                       | 97.3 ms: 1.45x faster                                                           |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 471 ms: 1.41x faster                                                            |
| async_tree_none_tg         | 336 ms                                                       | 242 ms: 1.39x faster                                                            |
| scimark_sor                | 134 ms                                                       | 97.2 ms: 1.38x faster                                                           |
| async_tree_none            | 354 ms                                                       | 256 ms: 1.38x faster                                                            |
| async_tree_memoization_tg  | 414 ms                                                       | 304 ms: 1.36x faster                                                            |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 473 ms: 1.35x faster                                                            |
| spectral_norm              | 111 ms                                                       | 85.8 ms: 1.29x faster                                                           |
| deepcopy_reduce            | 3.11 us                                                      | 2.41 us: 1.29x faster                                                           |
| scimark_fft                | 349 ms                                                       | 275 ms: 1.27x faster                                                            |
| richards                   | 45.2 ms                                                      | 36.2 ms: 1.25x faster                                                           |
| logging_silent             | 103 ns                                                       | 83.0 ns: 1.24x faster                                                           |
| richards_super             | 51.6 ms                                                      | 42.1 ms: 1.23x faster                                                           |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 3.90 ms: 1.21x faster                                                           |
| scimark_monte_carlo        | 65.4 ms                                                      | 54.7 ms: 1.20x faster                                                           |
| json_dumps                 | 10.5 ms                                                      | 8.84 ms: 1.19x faster                                                           |
| async_generators           | 377 ms                                                       | 317 ms: 1.19x faster                                                            |
| pylint                     | 317 ms                                                       | 270 ms: 1.17x faster                                                            |
| scimark_lu                 | 113 ms                                                       | 96.8 ms: 1.16x faster                                                           |
| float                      | 77.5 ms                                                      | 67.2 ms: 1.15x faster                                                           |
| chaos                      | 57.3 ms                                                      | 49.8 ms: 1.15x faster                                                           |
| pyflate                    | 449 ms                                                       | 390 ms: 1.15x faster                                                            |
| comprehensions             | 16.5 us                                                      | 14.3 us: 1.15x faster                                                           |
| genshi_text                | 21.5 ms                                                      | 19.1 ms: 1.13x faster                                                           |
| dulwich_log                | 74.8 ms                                                      | 66.3 ms: 1.13x faster                                                           |
| hexiom                     | 5.99 ms                                                      | 5.32 ms: 1.13x faster                                                           |
| coverage                   | 83.0 ms                                                      | 74.4 ms: 1.12x faster                                                           |
| html5lib                   | 67.0 ms                                                      | 60.1 ms: 1.11x faster                                                           |
| pidigits                   | 217 ms                                                       | 194 ms: 1.11x faster                                                            |
| bpe_tokeniser              | 4.45 sec                                                     | 4.00 sec: 1.11x faster                                                          |
| tomli_loads                | 2.01 sec                                                     | 1.80 sec: 1.11x faster                                                          |
| regex_compile              | 132 ms                                                       | 119 ms: 1.11x faster                                                            |
| pathlib                    | 19.2 ms                                                      | 17.4 ms: 1.10x faster                                                           |
| typing_runtime_protocols   | 155 us                                                       | 141 us: 1.10x faster                                                            |
| pprint_safe_repr           | 738 ms                                                       | 674 ms: 1.09x faster                                                            |
| pprint_pformat             | 1.50 sec                                                     | 1.37 sec: 1.09x faster                                                          |
| sympy_integrate            | 19.8 ms                                                      | 18.1 ms: 1.09x faster                                                           |
| deltablue                  | 3.12 ms                                                      | 2.88 ms: 1.09x faster                                                           |
| logging_simple             | 6.16 us                                                      | 5.68 us: 1.08x faster                                                           |
| genshi_xml                 | 48.8 ms                                                      | 45.1 ms: 1.08x faster                                                           |
| raytrace                   | 253 ms                                                       | 235 ms: 1.08x faster                                                            |
| xml_etree_process          | 59.3 ms                                                      | 55.1 ms: 1.08x faster                                                           |
| logging_format             | 6.84 us                                                      | 6.36 us: 1.08x faster                                                           |
| thrift                     | 778 us                                                       | 726 us: 1.07x faster                                                            |
| regex_v8                   | 22.7 ms                                                      | 21.2 ms: 1.07x faster                                                           |
| xml_etree_generate         | 85.4 ms                                                      | 79.9 ms: 1.07x faster                                                           |
| nbody                      | 85.1 ms                                                      | 79.7 ms: 1.07x faster                                                           |
| pycparser                  | 1.12 sec                                                     | 1.05 sec: 1.06x faster                                                          |
| json_loads                 | 27.0 us                                                      | 25.5 us: 1.06x faster                                                           |
| django_template            | 34.1 ms                                                      | 32.3 ms: 1.06x faster                                                           |
| 2to3                       | 260 ms                                                       | 246 ms: 1.06x faster                                                            |
| nqueens                    | 78.6 ms                                                      | 74.4 ms: 1.06x faster                                                           |
| docutils                   | 2.62 sec                                                     | 2.48 sec: 1.05x faster                                                          |
| generators                 | 28.8 ms                                                      | 27.4 ms: 1.05x faster                                                           |
| unpickle_pure_python       | 210 us                                                       | 200 us: 1.05x faster                                                            |
| sympy_str                  | 275 ms                                                       | 261 ms: 1.05x faster                                                            |
| regex_effbot               | 3.08 ms                                                      | 2.95 ms: 1.05x faster                                                           |
| sympy_sum                  | 156 ms                                                       | 149 ms: 1.04x faster                                                            |
| sympy_expand               | 457 ms                                                       | 439 ms: 1.04x faster                                                            |
| crypto_pyaes               | 67.9 ms                                                      | 65.8 ms: 1.03x faster                                                           |
| fannkuch                   | 370 ms                                                       | 360 ms: 1.03x faster                                                            |
| coroutines                 | 23.6 ms                                                      | 23.2 ms: 1.02x faster                                                           |
| python_startup_no_site     | 7.39 ms                                                      | 7.34 ms: 1.01x faster                                                           |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                            |
| meteor_contest             | 102 ms                                                       | 101 ms: 1.00x faster                                                            |
| regex_dna                  | 180 ms                                                       | 182 ms: 1.01x slower                                                            |
| pickle_pure_python         | 294 us                                                       | 298 us: 1.01x slower                                                            |
| mako                       | 11.3 ms                                                      | 11.6 ms: 1.02x slower                                                           |
| bench_thread_pool          | 919 us                                                       | 967 us: 1.05x slower                                                            |
| xml_etree_parse            | 136 ms                                                       | 145 ms: 1.06x slower                                                            |
| bench_mp_pool              | 11.0 ms                                                      | 12.4 ms: 1.13x slower                                                           |
| python_startup             | 11.0 ms                                                      | 12.6 ms: 1.15x slower                                                           |
| gc_traversal               | 3.14 ms                                                      | 4.60 ms: 1.46x slower                                                           |
| create_gc_cycles           | 1.34 ms                                                      | 2.00 ms: 1.49x slower                                                           |
| telco                      | 7.82 ms                                                      | 155 ms: 19.77x slower                                                           |
| Geometric mean             | (ref)                                                        | 1.09x faster                                                                    |

Benchmark hidden because not significant (3): sqlite_synth, xml_etree_iterparse, json
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250917-3.15.0a0-178b03e-CLANG/bm-20250917-vultr-x86_64-Fidget%2dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.086x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.18x