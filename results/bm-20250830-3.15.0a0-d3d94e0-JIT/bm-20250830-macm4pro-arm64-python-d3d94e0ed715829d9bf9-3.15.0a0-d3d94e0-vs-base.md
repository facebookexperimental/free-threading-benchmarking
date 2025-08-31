# Results vs. base

- fork: python
- ref: d3d94e0ed715829d9bf9
- machine: darwin-arm64
- commit hash: d3d94e0
- commit date: 2025-08-30
- overall geometric mean: 1.007x faster
- HPT reliability: 99.27%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250830-3.15.0a0-d3d94e0/bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0.json | results/bm-20250830-3.15.0a0-d3d94e0-JIT/bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 118 ms                                                                                                            | 118 ms: 1.00x slower                                                                                                  |
| docutils       | 1.07 sec                                                                                                          | 1.06 sec: 1.01x faster                                                                                                |
| html5lib       | 24.5 ms                                                                                                           | 24.1 ms: 1.01x faster                                                                                                 |
| Geometric mean | (ref)                                                                                                             | 1.01x faster                                                                                                          |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | results/bm-20250830-3.15.0a0-d3d94e0/bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0.json | results/bm-20250830-3.15.0a0-d3d94e0-JIT/bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0.json |
|----------------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io                    | 260 ms                                                                                                            | 252 ms: 1.03x faster                                                                                                  |
| async_tree_none                  | 115 ms                                                                                                            | 113 ms: 1.02x faster                                                                                                  |
| async_tree_eager                 | 42.8 ms                                                                                                           | 41.9 ms: 1.02x faster                                                                                                 |
| async_tree_none_tg               | 106 ms                                                                                                            | 105 ms: 1.02x faster                                                                                                  |
| async_tree_io_tg                 | 254 ms                                                                                                            | 251 ms: 1.01x faster                                                                                                  |
| async_tree_eager_tg              | 88.1 ms                                                                                                           | 87.0 ms: 1.01x faster                                                                                                 |
| async_tree_cpu_io_mixed_tg       | 266 ms                                                                                                            | 262 ms: 1.01x faster                                                                                                  |
| async_tree_eager_cpu_io_mixed_tg | 252 ms                                                                                                            | 249 ms: 1.01x faster                                                                                                  |
| async_tree_cpu_io_mixed          | 268 ms                                                                                                            | 266 ms: 1.01x faster                                                                                                  |
| async_tree_memoization           | 150 ms                                                                                                            | 149 ms: 1.01x faster                                                                                                  |
| async_tree_eager_cpu_io_mixed    | 226 ms                                                                                                            | 224 ms: 1.01x faster                                                                                                  |
| asyncio_websockets               | 193 ms                                                                                                            | 193 ms: 1.00x faster                                                                                                  |
| coroutines                       | 9.91 ms                                                                                                           | 10.0 ms: 1.01x slower                                                                                                 |
| async_generators                 | 179 ms                                                                                                            | 184 ms: 1.03x slower                                                                                                  |
| Geometric mean                   | (ref)                                                                                                             | 1.01x faster                                                                                                          |

Benchmark hidden because not significant (7): asyncio_tcp_ssl, async_tree_memoization_tg, async_tree_eager_memoization_tg, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_io, asyncio_tcp

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250830-3.15.0a0-d3d94e0/bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0.json | results/bm-20250830-3.15.0a0-d3d94e0-JIT/bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 168 ms                                                                                                            | 166 ms: 1.01x faster                                                                                                  |
| float          | 30.2 ms                                                                                                           | 31.5 ms: 1.04x slower                                                                                                 |
| nbody          | 48.2 ms                                                                                                           | 56.8 ms: 1.18x slower                                                                                                 |
| Geometric mean | (ref)                                                                                                             | 1.07x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250830-3.15.0a0-d3d94e0/bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0.json | results/bm-20250830-3.15.0a0-d3d94e0-JIT/bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 9.93 ms                                                                                                           | 9.61 ms: 1.03x faster                                                                                                 |
| regex_dna      | 99.3 ms                                                                                                           | 97.1 ms: 1.02x faster                                                                                                 |
| regex_compile  | 48.9 ms                                                                                                           | 48.1 ms: 1.02x faster                                                                                                 |
| Geometric mean | (ref)                                                                                                             | 1.01x faster                                                                                                          |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250830-3.15.0a0-d3d94e0/bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0.json | results/bm-20250830-3.15.0a0-d3d94e0-JIT/bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| tomli_loads          | 933 ms                                                                                                            | 823 ms: 1.13x faster                                                                                                  |
| xml_etree_process    | 25.4 ms                                                                                                           | 23.7 ms: 1.07x faster                                                                                                 |
| unpickle_pure_python | 100 us                                                                                                            | 93.5 us: 1.07x faster                                                                                                 |
| pickle_pure_python   | 148 us                                                                                                            | 141 us: 1.05x faster                                                                                                  |
| xml_etree_generate   | 35.7 ms                                                                                                           | 34.2 ms: 1.04x faster                                                                                                 |
| json_loads           | 11.4 us                                                                                                           | 11.1 us: 1.02x faster                                                                                                 |
| pickle               | 6.08 us                                                                                                           | 6.03 us: 1.01x faster                                                                                                 |
| xml_etree_iterparse  | 44.8 ms                                                                                                           | 44.5 ms: 1.01x faster                                                                                                 |
| json_dumps           | 3.78 ms                                                                                                           | 3.80 ms: 1.00x slower                                                                                                 |
| xml_etree_parse      | 62.9 ms                                                                                                           | 64.2 ms: 1.02x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                             | 1.03x faster                                                                                                          |

Benchmark hidden because not significant (4): pickle_list, unpickle_list, unpickle, pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250830-3.15.0a0-d3d94e0/bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0.json | results/bm-20250830-3.15.0a0-d3d94e0-JIT/bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 8.81 ms                                                                                                           | 8.74 ms: 1.01x faster                                                                                                 |
| python_startup_no_site | 6.30 ms                                                                                                           | 6.28 ms: 1.00x faster                                                                                                 |
| Geometric mean         | (ref)                                                                                                             | 1.01x faster                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | results/bm-20250830-3.15.0a0-d3d94e0/bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0.json | results/bm-20250830-3.15.0a0-d3d94e0-JIT/bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| mako           | 4.98 ms                                                                                                           | 4.51 ms: 1.10x faster                                                                                                 |
| genshi_text    | 10.0 ms                                                                                                           | 9.93 ms: 1.01x faster                                                                                                 |
| genshi_xml     | 21.9 ms                                                                                                           | 21.7 ms: 1.01x faster                                                                                                 |
| Geometric mean | (ref)                                                                                                             | 1.03x faster                                                                                                          |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                        | results/bm-20250830-3.15.0a0-d3d94e0/bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0.json | results/bm-20250830-3.15.0a0-d3d94e0-JIT/bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0.json |
|----------------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| pprint_pformat                   | 688 ms                                                                                                            | 594 ms: 1.16x faster                                                                                                  |
| pprint_safe_repr                 | 337 ms                                                                                                            | 296 ms: 1.14x faster                                                                                                  |
| tomli_loads                      | 933 ms                                                                                                            | 823 ms: 1.13x faster                                                                                                  |
| mako                             | 4.98 ms                                                                                                           | 4.51 ms: 1.10x faster                                                                                                 |
| xml_etree_process                | 25.4 ms                                                                                                           | 23.7 ms: 1.07x faster                                                                                                 |
| unpickle_pure_python             | 100 us                                                                                                            | 93.5 us: 1.07x faster                                                                                                 |
| telco                            | 2.82 ms                                                                                                           | 2.69 ms: 1.05x faster                                                                                                 |
| pickle_pure_python               | 148 us                                                                                                            | 141 us: 1.05x faster                                                                                                  |
| fannkuch                         | 180 ms                                                                                                            | 172 ms: 1.05x faster                                                                                                  |
| comprehensions                   | 7.65 us                                                                                                           | 7.32 us: 1.04x faster                                                                                                 |
| xml_etree_generate               | 35.7 ms                                                                                                           | 34.2 ms: 1.04x faster                                                                                                 |
| meteor_contest                   | 51.3 ms                                                                                                           | 49.5 ms: 1.04x faster                                                                                                 |
| regex_v8                         | 9.93 ms                                                                                                           | 9.61 ms: 1.03x faster                                                                                                 |
| async_tree_io                    | 260 ms                                                                                                            | 252 ms: 1.03x faster                                                                                                  |
| sqlglot_v2_parse                 | 567 us                                                                                                            | 549 us: 1.03x faster                                                                                                  |
| logging_simple                   | 2.35 us                                                                                                           | 2.29 us: 1.03x faster                                                                                                 |
| sqlglot_v2_transpile             | 691 us                                                                                                            | 674 us: 1.02x faster                                                                                                  |
| pyflate                          | 197 ms                                                                                                            | 193 ms: 1.02x faster                                                                                                  |
| regex_dna                        | 99.3 ms                                                                                                           | 97.1 ms: 1.02x faster                                                                                                 |
| async_tree_none                  | 115 ms                                                                                                            | 113 ms: 1.02x faster                                                                                                  |
| json_loads                       | 11.4 us                                                                                                           | 11.1 us: 1.02x faster                                                                                                 |
| async_tree_eager                 | 42.8 ms                                                                                                           | 41.9 ms: 1.02x faster                                                                                                 |
| create_gc_cycles                 | 963 us                                                                                                            | 944 us: 1.02x faster                                                                                                  |
| sqlite_synth                     | 966 ns                                                                                                            | 947 ns: 1.02x faster                                                                                                  |
| sympy_sum                        | 56.9 ms                                                                                                           | 55.8 ms: 1.02x faster                                                                                                 |
| async_tree_none_tg               | 106 ms                                                                                                            | 105 ms: 1.02x faster                                                                                                  |
| thrift                           | 316 us                                                                                                            | 310 us: 1.02x faster                                                                                                  |
| logging_format                   | 2.54 us                                                                                                           | 2.50 us: 1.02x faster                                                                                                 |
| regex_compile                    | 48.9 ms                                                                                                           | 48.1 ms: 1.02x faster                                                                                                 |
| subparsers                       | 17.6 ms                                                                                                           | 17.3 ms: 1.02x faster                                                                                                 |
| gc_traversal                     | 2.11 ms                                                                                                           | 2.07 ms: 1.02x faster                                                                                                 |
| typing_runtime_protocols         | 64.3 us                                                                                                           | 63.3 us: 1.02x faster                                                                                                 |
| async_tree_io_tg                 | 254 ms                                                                                                            | 251 ms: 1.01x faster                                                                                                  |
| html5lib                         | 24.5 ms                                                                                                           | 24.1 ms: 1.01x faster                                                                                                 |
| sqlglot_v2_normalize             | 47.2 ms                                                                                                           | 46.6 ms: 1.01x faster                                                                                                 |
| async_tree_eager_tg              | 88.1 ms                                                                                                           | 87.0 ms: 1.01x faster                                                                                                 |
| async_tree_cpu_io_mixed_tg       | 266 ms                                                                                                            | 262 ms: 1.01x faster                                                                                                  |
| scimark_fft                      | 131 ms                                                                                                            | 129 ms: 1.01x faster                                                                                                  |
| bench_mp_pool                    | 45.2 ms                                                                                                           | 44.7 ms: 1.01x faster                                                                                                 |
| async_tree_eager_cpu_io_mixed_tg | 252 ms                                                                                                            | 249 ms: 1.01x faster                                                                                                  |
| pathlib                          | 11.0 ms                                                                                                           | 10.9 ms: 1.01x faster                                                                                                 |
| docutils                         | 1.07 sec                                                                                                          | 1.06 sec: 1.01x faster                                                                                                |
| raytrace                         | 119 ms                                                                                                            | 118 ms: 1.01x faster                                                                                                  |
| genshi_text                      | 10.0 ms                                                                                                           | 9.93 ms: 1.01x faster                                                                                                 |
| pidigits                         | 168 ms                                                                                                            | 166 ms: 1.01x faster                                                                                                  |
| async_tree_cpu_io_mixed          | 268 ms                                                                                                            | 266 ms: 1.01x faster                                                                                                  |
| genshi_xml                       | 21.9 ms                                                                                                           | 21.7 ms: 1.01x faster                                                                                                 |
| python_startup                   | 8.81 ms                                                                                                           | 8.74 ms: 1.01x faster                                                                                                 |
| deepcopy                         | 112 us                                                                                                            | 111 us: 1.01x faster                                                                                                  |
| generators                       | 17.8 ms                                                                                                           | 17.7 ms: 1.01x faster                                                                                                 |
| async_tree_memoization           | 150 ms                                                                                                            | 149 ms: 1.01x faster                                                                                                  |
| async_tree_eager_cpu_io_mixed    | 226 ms                                                                                                            | 224 ms: 1.01x faster                                                                                                  |
| deepcopy_reduce                  | 1.16 us                                                                                                           | 1.15 us: 1.01x faster                                                                                                 |
| dulwich_log                      | 18.4 ms                                                                                                           | 18.2 ms: 1.01x faster                                                                                                 |
| pickle                           | 6.08 us                                                                                                           | 6.03 us: 1.01x faster                                                                                                 |
| xml_etree_iterparse              | 44.8 ms                                                                                                           | 44.5 ms: 1.01x faster                                                                                                 |
| many_optionals                   | 326 us                                                                                                            | 324 us: 1.01x faster                                                                                                  |
| deepcopy_memo                    | 13.0 us                                                                                                           | 12.9 us: 1.01x faster                                                                                                 |
| python_startup_no_site           | 6.30 ms                                                                                                           | 6.28 ms: 1.00x faster                                                                                                 |
| asyncio_websockets               | 193 ms                                                                                                            | 193 ms: 1.00x faster                                                                                                  |
| sympy_str                        | 101 ms                                                                                                            | 101 ms: 1.00x faster                                                                                                  |
| nqueens                          | 39.3 ms                                                                                                           | 39.4 ms: 1.00x slower                                                                                                 |
| sympy_expand                     | 172 ms                                                                                                            | 172 ms: 1.00x slower                                                                                                  |
| 2to3                             | 118 ms                                                                                                            | 118 ms: 1.00x slower                                                                                                  |
| sympy_integrate                  | 7.54 ms                                                                                                           | 7.57 ms: 1.00x slower                                                                                                 |
| json_dumps                       | 3.78 ms                                                                                                           | 3.80 ms: 1.00x slower                                                                                                 |
| bpe_tokeniser                    | 1.99 sec                                                                                                          | 2.00 sec: 1.01x slower                                                                                                |
| crypto_pyaes                     | 37.7 ms                                                                                                           | 38.0 ms: 1.01x slower                                                                                                 |
| coverage                         | 32.9 ms                                                                                                           | 33.3 ms: 1.01x slower                                                                                                 |
| coroutines                       | 9.91 ms                                                                                                           | 10.0 ms: 1.01x slower                                                                                                 |
| chaos                            | 26.5 ms                                                                                                           | 26.8 ms: 1.01x slower                                                                                                 |
| mdp                              | 541 ms                                                                                                            | 548 ms: 1.01x slower                                                                                                  |
| scimark_sor                      | 50.3 ms                                                                                                           | 50.9 ms: 1.01x slower                                                                                                 |
| pycparser                        | 498 ms                                                                                                            | 505 ms: 1.01x slower                                                                                                  |
| richards_super                   | 24.1 ms                                                                                                           | 24.5 ms: 1.02x slower                                                                                                 |
| spectral_norm                    | 43.8 ms                                                                                                           | 44.6 ms: 1.02x slower                                                                                                 |
| scimark_monte_carlo              | 29.7 ms                                                                                                           | 30.3 ms: 1.02x slower                                                                                                 |
| xml_etree_parse                  | 62.9 ms                                                                                                           | 64.2 ms: 1.02x slower                                                                                                 |
| richards                         | 21.3 ms                                                                                                           | 21.8 ms: 1.02x slower                                                                                                 |
| go                               | 56.5 ms                                                                                                           | 57.9 ms: 1.03x slower                                                                                                 |
| async_generators                 | 179 ms                                                                                                            | 184 ms: 1.03x slower                                                                                                  |
| k_core                           | 961 ms                                                                                                            | 991 ms: 1.03x slower                                                                                                  |
| unpack_sequence                  | 30.7 ns                                                                                                           | 31.7 ns: 1.03x slower                                                                                                 |
| hexiom                           | 2.86 ms                                                                                                           | 2.98 ms: 1.04x slower                                                                                                 |
| float                            | 30.2 ms                                                                                                           | 31.5 ms: 1.04x slower                                                                                                 |
| scimark_lu                       | 48.1 ms                                                                                                           | 50.7 ms: 1.05x slower                                                                                                 |
| shortest_path                    | 219 ms                                                                                                            | 235 ms: 1.07x slower                                                                                                  |
| deltablue                        | 1.54 ms                                                                                                           | 1.66 ms: 1.08x slower                                                                                                 |
| connected_components             | 202 ms                                                                                                            | 218 ms: 1.08x slower                                                                                                  |
| scimark_sparse_mat_mult          | 1.91 ms                                                                                                           | 2.16 ms: 1.13x slower                                                                                                 |
| nbody                            | 48.2 ms                                                                                                           | 56.8 ms: 1.18x slower                                                                                                 |
| Geometric mean                   | (ref)                                                                                                             | 1.01x faster                                                                                                          |

Benchmark hidden because not significant (20): asyncio_tcp_ssl, sphinx, async_tree_memoization_tg, async_tree_eager_memoization_tg, async_tree_eager_io_tg, pylint, async_tree_eager_memoization, pickle_list, unpickle_list, json, unpickle, pickle_dict, logging_silent, bench_thread_pool, sqlglot_v2_optimize, dask, async_tree_eager_io, django_template, asyncio_tcp, regex_effbot

- Geometric mean (including insignificant results): 1.007x faster

# HPT report

- Reliability score: 99.27% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x