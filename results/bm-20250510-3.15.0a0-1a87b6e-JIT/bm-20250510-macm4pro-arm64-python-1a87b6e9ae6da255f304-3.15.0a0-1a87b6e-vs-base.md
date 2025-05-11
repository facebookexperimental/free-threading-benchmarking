# Results vs. base

- fork: python
- ref: 1a87b6e9ae6da255f304
- machine: darwin-arm64
- commit hash: 1a87b6e
- commit date: 2025-05-10
- overall geometric mean: 1.005x faster
- HPT reliability: 98.03%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250510-3.15.0a0-1a87b6e/bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e.json | results/bm-20250510-3.15.0a0-1a87b6e-JIT/bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| docutils       | 1.05 sec                                                                                                          | 1.06 sec: 1.01x slower                                                                                                |
| Geometric mean | (ref)                                                                                                             | 1.00x slower                                                                                                          |

Benchmark hidden because not significant (3): 2to3, html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | results/bm-20250510-3.15.0a0-1a87b6e/bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e.json | results/bm-20250510-3.15.0a0-1a87b6e-JIT/bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e.json |
|----------------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg       | 266 ms                                                                                                            | 260 ms: 1.02x faster                                                                                                  |
| async_tree_none                  | 114 ms                                                                                                            | 112 ms: 1.02x faster                                                                                                  |
| async_tree_none_tg               | 106 ms                                                                                                            | 104 ms: 1.02x faster                                                                                                  |
| async_tree_eager_io_tg           | 258 ms                                                                                                            | 253 ms: 1.02x faster                                                                                                  |
| async_tree_cpu_io_mixed          | 268 ms                                                                                                            | 265 ms: 1.01x faster                                                                                                  |
| async_tree_eager_tg              | 88.3 ms                                                                                                           | 87.2 ms: 1.01x faster                                                                                                 |
| async_tree_io_tg                 | 254 ms                                                                                                            | 251 ms: 1.01x faster                                                                                                  |
| async_tree_eager                 | 42.9 ms                                                                                                           | 42.5 ms: 1.01x faster                                                                                                 |
| async_tree_eager_cpu_io_mixed_tg | 249 ms                                                                                                            | 246 ms: 1.01x faster                                                                                                  |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                                                                            | 224 ms: 1.01x faster                                                                                                  |
| async_tree_memoization           | 148 ms                                                                                                            | 147 ms: 1.01x faster                                                                                                  |
| asyncio_websockets               | 192 ms                                                                                                            | 191 ms: 1.01x faster                                                                                                  |
| coroutines                       | 10.8 ms                                                                                                           | 10.7 ms: 1.00x faster                                                                                                 |
| async_generators                 | 177 ms                                                                                                            | 183 ms: 1.04x slower                                                                                                  |
| Geometric mean                   | (ref)                                                                                                             | 1.01x faster                                                                                                          |

Benchmark hidden because not significant (7): async_tree_memoization_tg, async_tree_eager_io, async_tree_io, async_tree_eager_memoization_tg, async_tree_eager_memoization, asyncio_tcp_ssl, asyncio_tcp

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250510-3.15.0a0-1a87b6e/bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e.json | results/bm-20250510-3.15.0a0-1a87b6e-JIT/bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| float          | 30.4 ms                                                                                                           | 28.7 ms: 1.06x faster                                                                                                 |
| nbody          | 50.5 ms                                                                                                           | 50.0 ms: 1.01x faster                                                                                                 |
| Geometric mean | (ref)                                                                                                             | 1.02x faster                                                                                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250510-3.15.0a0-1a87b6e/bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e.json | results/bm-20250510-3.15.0a0-1a87b6e-JIT/bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_compile  | 49.4 ms                                                                                                           | 48.7 ms: 1.02x faster                                                                                                 |
| regex_v8       | 9.88 ms                                                                                                           | 10.0 ms: 1.01x slower                                                                                                 |
| Geometric mean | (ref)                                                                                                             | 1.00x faster                                                                                                          |

Benchmark hidden because not significant (2): regex_dna, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250510-3.15.0a0-1a87b6e/bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e.json | results/bm-20250510-3.15.0a0-1a87b6e-JIT/bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| tomli_loads          | 952 ms                                                                                                            | 865 ms: 1.10x faster                                                                                                  |
| xml_etree_process    | 25.8 ms                                                                                                           | 24.0 ms: 1.08x faster                                                                                                 |
| unpickle_pure_python | 100 us                                                                                                            | 94.3 us: 1.06x faster                                                                                                 |
| xml_etree_generate   | 36.2 ms                                                                                                           | 34.3 ms: 1.06x faster                                                                                                 |
| pickle_pure_python   | 146 us                                                                                                            | 141 us: 1.03x faster                                                                                                  |
| unpickle_list        | 2.00 us                                                                                                           | 1.96 us: 1.02x faster                                                                                                 |
| json_dumps           | 5.22 ms                                                                                                           | 5.14 ms: 1.02x faster                                                                                                 |
| pickle               | 6.14 us                                                                                                           | 6.09 us: 1.01x faster                                                                                                 |
| xml_etree_iterparse  | 44.8 ms                                                                                                           | 45.1 ms: 1.01x slower                                                                                                 |
| json_loads           | 11.7 us                                                                                                           | 11.9 us: 1.02x slower                                                                                                 |
| xml_etree_parse      | 62.2 ms                                                                                                           | 63.5 ms: 1.02x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                             | 1.02x faster                                                                                                          |

Benchmark hidden because not significant (3): pickle_dict, pickle_list, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250510-3.15.0a0-1a87b6e/bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e.json | results/bm-20250510-3.15.0a0-1a87b6e-JIT/bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup_no_site | 6.09 ms                                                                                                           | 6.11 ms: 1.00x slower                                                                                                 |
| python_startup         | 8.51 ms                                                                                                           | 8.55 ms: 1.00x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                             | 1.00x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | results/bm-20250510-3.15.0a0-1a87b6e/bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e.json | results/bm-20250510-3.15.0a0-1a87b6e-JIT/bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| mako           | 4.80 ms                                                                                                           | 4.39 ms: 1.09x faster                                                                                                 |
| genshi_text    | 10.4 ms                                                                                                           | 10.2 ms: 1.02x faster                                                                                                 |
| genshi_xml     | 22.1 ms                                                                                                           | 21.8 ms: 1.01x faster                                                                                                 |
| Geometric mean | (ref)                                                                                                             | 1.03x faster                                                                                                          |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                        | results/bm-20250510-3.15.0a0-1a87b6e/bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e.json | results/bm-20250510-3.15.0a0-1a87b6e-JIT/bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e.json |
|----------------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| pprint_safe_repr                 | 326 ms                                                                                                            | 292 ms: 1.12x faster                                                                                                  |
| pprint_pformat                   | 656 ms                                                                                                            | 591 ms: 1.11x faster                                                                                                  |
| tomli_loads                      | 952 ms                                                                                                            | 865 ms: 1.10x faster                                                                                                  |
| mako                             | 4.80 ms                                                                                                           | 4.39 ms: 1.09x faster                                                                                                 |
| xml_etree_process                | 25.8 ms                                                                                                           | 24.0 ms: 1.08x faster                                                                                                 |
| unpickle_pure_python             | 100 us                                                                                                            | 94.3 us: 1.06x faster                                                                                                 |
| float                            | 30.4 ms                                                                                                           | 28.7 ms: 1.06x faster                                                                                                 |
| xml_etree_generate               | 36.2 ms                                                                                                           | 34.3 ms: 1.06x faster                                                                                                 |
| telco                            | 3.10 ms                                                                                                           | 2.98 ms: 1.04x faster                                                                                                 |
| pickle_pure_python               | 146 us                                                                                                            | 141 us: 1.03x faster                                                                                                  |
| pyflate                          | 198 ms                                                                                                            | 192 ms: 1.03x faster                                                                                                  |
| richards                         | 22.4 ms                                                                                                           | 21.8 ms: 1.03x faster                                                                                                 |
| async_tree_cpu_io_mixed_tg       | 266 ms                                                                                                            | 260 ms: 1.02x faster                                                                                                  |
| deepcopy_reduce                  | 1.14 us                                                                                                           | 1.12 us: 1.02x faster                                                                                                 |
| async_tree_none                  | 114 ms                                                                                                            | 112 ms: 1.02x faster                                                                                                  |
| async_tree_none_tg               | 106 ms                                                                                                            | 104 ms: 1.02x faster                                                                                                  |
| async_tree_eager_io_tg           | 258 ms                                                                                                            | 253 ms: 1.02x faster                                                                                                  |
| subparsers                       | 9.56 ms                                                                                                           | 9.38 ms: 1.02x faster                                                                                                 |
| fannkuch                         | 180 ms                                                                                                            | 176 ms: 1.02x faster                                                                                                  |
| unpickle_list                    | 2.00 us                                                                                                           | 1.96 us: 1.02x faster                                                                                                 |
| regex_compile                    | 49.4 ms                                                                                                           | 48.7 ms: 1.02x faster                                                                                                 |
| genshi_text                      | 10.4 ms                                                                                                           | 10.2 ms: 1.02x faster                                                                                                 |
| json_dumps                       | 5.22 ms                                                                                                           | 5.14 ms: 1.02x faster                                                                                                 |
| scimark_fft                      | 133 ms                                                                                                            | 131 ms: 1.02x faster                                                                                                  |
| deepcopy                         | 110 us                                                                                                            | 108 us: 1.02x faster                                                                                                  |
| richards_super                   | 25.1 ms                                                                                                           | 24.7 ms: 1.02x faster                                                                                                 |
| deepcopy_memo                    | 12.6 us                                                                                                           | 12.4 us: 1.01x faster                                                                                                 |
| sqlite_synth                     | 960 ns                                                                                                            | 946 ns: 1.01x faster                                                                                                  |
| async_tree_cpu_io_mixed          | 268 ms                                                                                                            | 265 ms: 1.01x faster                                                                                                  |
| async_tree_eager_tg              | 88.3 ms                                                                                                           | 87.2 ms: 1.01x faster                                                                                                 |
| genshi_xml                       | 22.1 ms                                                                                                           | 21.8 ms: 1.01x faster                                                                                                 |
| dulwich_log                      | 18.1 ms                                                                                                           | 17.9 ms: 1.01x faster                                                                                                 |
| nbody                            | 50.5 ms                                                                                                           | 50.0 ms: 1.01x faster                                                                                                 |
| create_gc_cycles                 | 945 us                                                                                                            | 935 us: 1.01x faster                                                                                                  |
| async_tree_io_tg                 | 254 ms                                                                                                            | 251 ms: 1.01x faster                                                                                                  |
| generators                       | 17.8 ms                                                                                                           | 17.6 ms: 1.01x faster                                                                                                 |
| async_tree_eager                 | 42.9 ms                                                                                                           | 42.5 ms: 1.01x faster                                                                                                 |
| async_tree_eager_cpu_io_mixed_tg | 249 ms                                                                                                            | 246 ms: 1.01x faster                                                                                                  |
| pickle                           | 6.14 us                                                                                                           | 6.09 us: 1.01x faster                                                                                                 |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                                                                            | 224 ms: 1.01x faster                                                                                                  |
| scimark_lu                       | 48.7 ms                                                                                                           | 48.4 ms: 1.01x faster                                                                                                 |
| async_tree_memoization           | 148 ms                                                                                                            | 147 ms: 1.01x faster                                                                                                  |
| asyncio_websockets               | 192 ms                                                                                                            | 191 ms: 1.01x faster                                                                                                  |
| bpe_tokeniser                    | 1.97 sec                                                                                                          | 1.96 sec: 1.01x faster                                                                                                |
| comprehensions                   | 7.90 us                                                                                                           | 7.86 us: 1.01x faster                                                                                                 |
| coroutines                       | 10.8 ms                                                                                                           | 10.7 ms: 1.00x faster                                                                                                 |
| nqueens                          | 39.0 ms                                                                                                           | 38.9 ms: 1.00x faster                                                                                                 |
| python_startup_no_site           | 6.09 ms                                                                                                           | 6.11 ms: 1.00x slower                                                                                                 |
| sqlglot_v2_optimize              | 23.3 ms                                                                                                           | 23.4 ms: 1.00x slower                                                                                                 |
| sqlglot_v2_transpile             | 674 us                                                                                                            | 677 us: 1.00x slower                                                                                                  |
| python_startup                   | 8.51 ms                                                                                                           | 8.55 ms: 1.00x slower                                                                                                 |
| sympy_sum                        | 56.5 ms                                                                                                           | 56.8 ms: 1.01x slower                                                                                                 |
| docutils                         | 1.05 sec                                                                                                          | 1.06 sec: 1.01x slower                                                                                                |
| meteor_contest                   | 50.2 ms                                                                                                           | 50.5 ms: 1.01x slower                                                                                                 |
| xml_etree_iterparse              | 44.8 ms                                                                                                           | 45.1 ms: 1.01x slower                                                                                                 |
| logging_simple                   | 2.60 us                                                                                                           | 2.61 us: 1.01x slower                                                                                                 |
| json                             | 1.97 ms                                                                                                           | 1.98 ms: 1.01x slower                                                                                                 |
| go                               | 56.7 ms                                                                                                           | 57.2 ms: 1.01x slower                                                                                                 |
| chaos                            | 26.7 ms                                                                                                           | 26.9 ms: 1.01x slower                                                                                                 |
| crypto_pyaes                     | 38.0 ms                                                                                                           | 38.4 ms: 1.01x slower                                                                                                 |
| logging_format                   | 2.84 us                                                                                                           | 2.87 us: 1.01x slower                                                                                                 |
| hexiom                           | 2.83 ms                                                                                                           | 2.86 ms: 1.01x slower                                                                                                 |
| mdp                              | 534 ms                                                                                                            | 540 ms: 1.01x slower                                                                                                  |
| regex_v8                         | 9.88 ms                                                                                                           | 10.0 ms: 1.01x slower                                                                                                 |
| logging_silent                   | 196 ns                                                                                                            | 199 ns: 1.02x slower                                                                                                  |
| sympy_str                        | 100 ms                                                                                                            | 102 ms: 1.02x slower                                                                                                  |
| json_loads                       | 11.7 us                                                                                                           | 11.9 us: 1.02x slower                                                                                                 |
| xml_etree_parse                  | 62.2 ms                                                                                                           | 63.5 ms: 1.02x slower                                                                                                 |
| pycparser                        | 494 ms                                                                                                            | 504 ms: 1.02x slower                                                                                                  |
| scimark_monte_carlo              | 29.9 ms                                                                                                           | 30.6 ms: 1.02x slower                                                                                                 |
| sympy_expand                     | 168 ms                                                                                                            | 172 ms: 1.02x slower                                                                                                  |
| spectral_norm                    | 47.1 ms                                                                                                           | 48.3 ms: 1.03x slower                                                                                                 |
| sympy_integrate                  | 7.54 ms                                                                                                           | 7.74 ms: 1.03x slower                                                                                                 |
| async_generators                 | 177 ms                                                                                                            | 183 ms: 1.04x slower                                                                                                  |
| k_core                           | 960 ms                                                                                                            | 1.00 sec: 1.04x slower                                                                                                |
| scimark_sparse_mat_mult          | 1.99 ms                                                                                                           | 2.09 ms: 1.05x slower                                                                                                 |
| connected_components             | 199 ms                                                                                                            | 212 ms: 1.06x slower                                                                                                  |
| shortest_path                    | 217 ms                                                                                                            | 230 ms: 1.06x slower                                                                                                  |
| deltablue                        | 1.50 ms                                                                                                           | 1.65 ms: 1.10x slower                                                                                                 |
| unpack_sequence                  | 28.3 ns                                                                                                           | 36.2 ns: 1.28x slower                                                                                                 |
| Geometric mean                   | (ref)                                                                                                             | 1.00x faster                                                                                                          |

Benchmark hidden because not significant (31): async_tree_memoization_tg, async_tree_eager_io, async_tree_io, coverage, html5lib, async_tree_eager_memoization_tg, django_template, typing_runtime_protocols, gc_traversal, raytrace, pathlib, pidigits, pickle_dict, bench_thread_pool, dask, regex_dna, 2to3, bench_mp_pool, pickle_list, sqlglot_v2_normalize, scimark_sor, sqlglot_v2_parse, regex_effbot, thrift, many_optionals, unpickle, async_tree_eager_memoization, sphinx, asyncio_tcp_ssl, asyncio_tcp, pylint

- Geometric mean (including insignificant results): 1.005x faster

# HPT report

- Reliability score: 98.03% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x