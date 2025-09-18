# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: dynamic_opcode_targe
- machine: linux-x86_64
- commit hash: 178b03e
- commit date: 2025-09-17
- overall geometric mean: 1.124x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250917-vultr-x86_64-Fidget%2dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 246 ms: 1.07x faster                                                            |
| docutils       | 2.64 sec                                               | 2.48 sec: 1.06x faster                                                          |
| html5lib       | 63.6 ms                                                | 60.1 ms: 1.06x faster                                                           |
| Geometric mean | (ref)                                                  | 1.06x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250917-vultr-x86_64-Fidget%2dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_io              | 1.08 sec                                               | 586 ms: 1.85x faster                                                            |
| async_tree_none_tg         | 446 ms                                                 | 242 ms: 1.84x faster                                                            |
| async_tree_memoization     | 555 ms                                                 | 302 ms: 1.84x faster                                                            |
| async_tree_memoization_tg  | 560 ms                                                 | 304 ms: 1.84x faster                                                            |
| async_tree_io_tg           | 1.11 sec                                               | 608 ms: 1.83x faster                                                            |
| async_tree_none            | 464 ms                                                 | 256 ms: 1.81x faster                                                            |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 473 ms: 1.53x faster                                                            |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 471 ms: 1.52x faster                                                            |
| async_generators           | 384 ms                                                 | 317 ms: 1.21x faster                                                            |
| coroutines                 | 23.9 ms                                                | 23.2 ms: 1.03x faster                                                           |
| Geometric mean             | (ref)                                                  | 1.53x faster                                                                    |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250917-vultr-x86_64-Fidget%2dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 67.2 ms: 1.20x faster                                                           |
| nbody          | 89.3 ms                                                | 79.7 ms: 1.12x faster                                                           |
| pidigits       | 184 ms                                                 | 194 ms: 1.06x slower                                                            |
| Geometric mean | (ref)                                                  | 1.08x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250917-vultr-x86_64-Fidget%2dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 119 ms: 1.19x faster                                                            |
| regex_effbot   | 3.17 ms                                                | 2.95 ms: 1.07x faster                                                           |
| regex_v8       | 20.6 ms                                                | 21.2 ms: 1.03x slower                                                           |
| regex_dna      | 168 ms                                                 | 182 ms: 1.08x slower                                                            |
| Geometric mean | (ref)                                                  | 1.03x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250917-vultr-x86_64-Fidget%2dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| json_dumps           | 10.4 ms                                                | 8.84 ms: 1.17x faster                                                           |
| tomli_loads          | 2.11 sec                                               | 1.80 sec: 1.17x faster                                                          |
| unpickle_pure_python | 221 us                                                 | 200 us: 1.10x faster                                                            |
| xml_etree_process    | 59.0 ms                                                | 55.1 ms: 1.07x faster                                                           |
| xml_etree_generate   | 85.2 ms                                                | 79.9 ms: 1.07x faster                                                           |
| json_loads           | 26.5 us                                                | 25.5 us: 1.04x faster                                                           |
| pickle_pure_python   | 308 us                                                 | 298 us: 1.03x faster                                                            |
| xml_etree_iterparse  | 96.7 ms                                                | 94.7 ms: 1.02x faster                                                           |
| xml_etree_parse      | 139 ms                                                 | 145 ms: 1.04x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.07x faster                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250917-vultr-x86_64-Fidget%2dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.34 ms: 1.02x slower                                                           |
| python_startup         | 9.93 ms                                                | 12.6 ms: 1.27x slower                                                           |
| Geometric mean         | (ref)                                                  | 1.14x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250917-vultr-x86_64-Fidget%2dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 19.1 ms: 1.20x faster                                                           |
| genshi_xml      | 50.2 ms                                                | 45.1 ms: 1.11x faster                                                           |
| django_template | 34.7 ms                                                | 32.3 ms: 1.08x faster                                                           |
| mako            | 11.0 ms                                                | 11.6 ms: 1.05x slower                                                           |
| Geometric mean  | (ref)                                                  | 1.08x faster                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250917-vultr-x86_64-Fidget%2dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.10 sec: 2.21x faster                                                          |
| async_tree_io              | 1.08 sec                                               | 586 ms: 1.85x faster                                                            |
| async_tree_none_tg         | 446 ms                                                 | 242 ms: 1.84x faster                                                            |
| async_tree_memoization     | 555 ms                                                 | 302 ms: 1.84x faster                                                            |
| async_tree_memoization_tg  | 560 ms                                                 | 304 ms: 1.84x faster                                                            |
| async_tree_io_tg           | 1.11 sec                                               | 608 ms: 1.83x faster                                                            |
| async_tree_none            | 464 ms                                                 | 256 ms: 1.81x faster                                                            |
| deepcopy_memo              | 40.3 us                                                | 24.6 us: 1.64x faster                                                           |
| deepcopy                   | 352 us                                                 | 225 us: 1.56x faster                                                            |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 473 ms: 1.53x faster                                                            |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 471 ms: 1.52x faster                                                            |
| go                         | 139 ms                                                 | 97.3 ms: 1.43x faster                                                           |
| comprehensions             | 19.8 us                                                | 14.3 us: 1.39x faster                                                           |
| scimark_sor                | 130 ms                                                 | 97.2 ms: 1.33x faster                                                           |
| logging_silent             | 109 ns                                                 | 83.0 ns: 1.31x faster                                                           |
| spectral_norm              | 110 ms                                                 | 85.8 ms: 1.28x faster                                                           |
| deepcopy_reduce            | 3.08 us                                                | 2.41 us: 1.28x faster                                                           |
| raytrace                   | 299 ms                                                 | 235 ms: 1.28x faster                                                            |
| richards                   | 45.9 ms                                                | 36.2 ms: 1.27x faster                                                           |
| chaos                      | 62.8 ms                                                | 49.8 ms: 1.26x faster                                                           |
| scimark_monte_carlo        | 68.4 ms                                                | 54.7 ms: 1.25x faster                                                           |
| scimark_fft                | 342 ms                                                 | 275 ms: 1.24x faster                                                            |
| pathlib                    | 21.5 ms                                                | 17.4 ms: 1.24x faster                                                           |
| richards_super             | 51.9 ms                                                | 42.1 ms: 1.23x faster                                                           |
| async_generators           | 384 ms                                                 | 317 ms: 1.21x faster                                                            |
| float                      | 80.8 ms                                                | 67.2 ms: 1.20x faster                                                           |
| deltablue                  | 3.45 ms                                                | 2.88 ms: 1.20x faster                                                           |
| genshi_text                | 22.8 ms                                                | 19.1 ms: 1.20x faster                                                           |
| regex_compile              | 142 ms                                                 | 119 ms: 1.19x faster                                                            |
| dulwich_log                | 78.9 ms                                                | 66.3 ms: 1.19x faster                                                           |
| bpe_tokeniser              | 4.74 sec                                               | 4.00 sec: 1.19x faster                                                          |
| scimark_lu                 | 114 ms                                                 | 96.8 ms: 1.18x faster                                                           |
| pylint                     | 319 ms                                                 | 270 ms: 1.18x faster                                                            |
| generators                 | 32.2 ms                                                | 27.4 ms: 1.18x faster                                                           |
| json_dumps                 | 10.4 ms                                                | 8.84 ms: 1.17x faster                                                           |
| tomli_loads                | 2.11 sec                                               | 1.80 sec: 1.17x faster                                                          |
| logging_simple             | 6.63 us                                                | 5.68 us: 1.17x faster                                                           |
| crypto_pyaes               | 76.6 ms                                                | 65.8 ms: 1.16x faster                                                           |
| hexiom                     | 6.17 ms                                                | 5.32 ms: 1.16x faster                                                           |
| typing_runtime_protocols   | 163 us                                                 | 141 us: 1.16x faster                                                            |
| logging_format             | 7.35 us                                                | 6.36 us: 1.16x faster                                                           |
| pyflate                    | 448 ms                                                 | 390 ms: 1.15x faster                                                            |
| sympy_integrate            | 20.5 ms                                                | 18.1 ms: 1.13x faster                                                           |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 3.90 ms: 1.13x faster                                                           |
| nbody                      | 89.3 ms                                                | 79.7 ms: 1.12x faster                                                           |
| sympy_str                  | 292 ms                                                 | 261 ms: 1.12x faster                                                            |
| sympy_sum                  | 166 ms                                                 | 149 ms: 1.11x faster                                                            |
| pycparser                  | 1.17 sec                                               | 1.05 sec: 1.11x faster                                                          |
| genshi_xml                 | 50.2 ms                                                | 45.1 ms: 1.11x faster                                                           |
| pprint_pformat             | 1.52 sec                                               | 1.37 sec: 1.11x faster                                                          |
| unpickle_pure_python       | 221 us                                                 | 200 us: 1.10x faster                                                            |
| pprint_safe_repr           | 743 ms                                                 | 674 ms: 1.10x faster                                                            |
| thrift                     | 791 us                                                 | 726 us: 1.09x faster                                                            |
| nqueens                    | 80.1 ms                                                | 74.4 ms: 1.08x faster                                                           |
| django_template            | 34.7 ms                                                | 32.3 ms: 1.08x faster                                                           |
| regex_effbot               | 3.17 ms                                                | 2.95 ms: 1.07x faster                                                           |
| 2to3                       | 264 ms                                                 | 246 ms: 1.07x faster                                                            |
| xml_etree_process          | 59.0 ms                                                | 55.1 ms: 1.07x faster                                                           |
| xml_etree_generate         | 85.2 ms                                                | 79.9 ms: 1.07x faster                                                           |
| sympy_expand               | 468 ms                                                 | 439 ms: 1.06x faster                                                            |
| docutils                   | 2.64 sec                                               | 2.48 sec: 1.06x faster                                                          |
| html5lib                   | 63.6 ms                                                | 60.1 ms: 1.06x faster                                                           |
| json_loads                 | 26.5 us                                                | 25.5 us: 1.04x faster                                                           |
| fannkuch                   | 372 ms                                                 | 360 ms: 1.03x faster                                                            |
| coroutines                 | 23.9 ms                                                | 23.2 ms: 1.03x faster                                                           |
| pickle_pure_python         | 308 us                                                 | 298 us: 1.03x faster                                                            |
| meteor_contest             | 104 ms                                                 | 101 ms: 1.02x faster                                                            |
| xml_etree_iterparse        | 96.7 ms                                                | 94.7 ms: 1.02x faster                                                           |
| json                       | 5.02 ms                                                | 4.92 ms: 1.02x faster                                                           |
| python_startup_no_site     | 7.16 ms                                                | 7.34 ms: 1.02x slower                                                           |
| bench_thread_pool          | 941 us                                                 | 967 us: 1.03x slower                                                            |
| regex_v8                   | 20.6 ms                                                | 21.2 ms: 1.03x slower                                                           |
| coverage                   | 71.4 ms                                                | 74.4 ms: 1.04x slower                                                           |
| xml_etree_parse            | 139 ms                                                 | 145 ms: 1.04x slower                                                            |
| mako                       | 11.0 ms                                                | 11.6 ms: 1.05x slower                                                           |
| pidigits                   | 184 ms                                                 | 194 ms: 1.06x slower                                                            |
| regex_dna                  | 168 ms                                                 | 182 ms: 1.08x slower                                                            |
| bench_mp_pool              | 10.8 ms                                                | 12.4 ms: 1.15x slower                                                           |
| python_startup             | 9.93 ms                                                | 12.6 ms: 1.27x slower                                                           |
| gc_traversal               | 3.46 ms                                                | 4.60 ms: 1.33x slower                                                           |
| create_gc_cycles           | 1.09 ms                                                | 2.00 ms: 1.83x slower                                                           |
| telco                      | 6.53 ms                                                | 155 ms: 23.70x slower                                                           |
| Geometric mean             | (ref)                                                  | 1.12x faster                                                                    |

Benchmark hidden because not significant (2): sqlite_synth, asyncio_websockets
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250917-3.15.0a0-178b03e-CLANG/bm-20250917-vultr-x86_64-Fidget%2dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.124x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.11x
- 95% likely to have a speedup of 1.11x
- 99% likely to have a speedup of 1.10x

# Memory
- memory change: 1.19x