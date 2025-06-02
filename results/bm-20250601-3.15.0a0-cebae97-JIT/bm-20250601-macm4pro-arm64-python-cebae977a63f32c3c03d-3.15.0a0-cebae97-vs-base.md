# Results vs. base

- fork: python
- ref: cebae977a63f32c3c03d
- machine: darwin-arm64
- commit hash: cebae97
- commit date: 2025-06-01
- overall geometric mean: 1.330x faster
- HPT reliability: 70.57%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250601-3.15.0a0-cebae97/bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json | results/bm-20250601-3.15.0a0-cebae97-JIT/bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                                                                            | 118 ms: 1.03x slower                                                                                                  |
| docutils       | 1.06 sec                                                                                                          | 1.07 sec: 1.01x slower                                                                                                |
| html5lib       | 24.3 ms                                                                                                           | 24.5 ms: 1.01x slower                                                                                                 |
| Geometric mean | (ref)                                                                                                             | 1.01x slower                                                                                                          |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                     | results/bm-20250601-3.15.0a0-cebae97/bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json | results/bm-20250601-3.15.0a0-cebae97-JIT/bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json |
|-------------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_none               | 114 ms                                                                                                            | 111 ms: 1.03x faster                                                                                                  |
| async_tree_memoization        | 150 ms                                                                                                            | 147 ms: 1.02x faster                                                                                                  |
| async_tree_io                 | 259 ms                                                                                                            | 254 ms: 1.02x faster                                                                                                  |
| async_tree_eager              | 43.0 ms                                                                                                           | 42.2 ms: 1.02x faster                                                                                                 |
| async_tree_none_tg            | 107 ms                                                                                                            | 105 ms: 1.02x faster                                                                                                  |
| async_tree_io_tg              | 256 ms                                                                                                            | 252 ms: 1.01x faster                                                                                                  |
| coroutines                    | 10.2 ms                                                                                                           | 10.1 ms: 1.01x faster                                                                                                 |
| async_tree_eager_tg           | 88.7 ms                                                                                                           | 87.6 ms: 1.01x faster                                                                                                 |
| asyncio_websockets            | 193 ms                                                                                                            | 193 ms: 1.00x slower                                                                                                  |
| async_tree_eager_cpu_io_mixed | 225 ms                                                                                                            | 226 ms: 1.00x slower                                                                                                  |
| async_tree_cpu_io_mixed_tg    | 265 ms                                                                                                            | 267 ms: 1.01x slower                                                                                                  |
| async_tree_cpu_io_mixed       | 267 ms                                                                                                            | 268 ms: 1.01x slower                                                                                                  |
| async_generators              | 173 ms                                                                                                            | 184 ms: 1.06x slower                                                                                                  |
| Geometric mean                | (ref)                                                                                                             | 1.00x faster                                                                                                          |

Benchmark hidden because not significant (8): async_tree_eager_io_tg, async_tree_eager_io, async_tree_eager_memoization_tg, async_tree_memoization_tg, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_memoization, asyncio_tcp, asyncio_tcp_ssl

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250601-3.15.0a0-cebae97/bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json | results/bm-20250601-3.15.0a0-cebae97-JIT/bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| float          | 30.2 ms                                                                                                           | 28.9 ms: 1.04x faster                                                                                                 |
| nbody          | 48.1 ms                                                                                                           | 49.2 ms: 1.02x slower                                                                                                 |
| Geometric mean | (ref)                                                                                                             | 1.01x faster                                                                                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250601-3.15.0a0-cebae97/bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json | results/bm-20250601-3.15.0a0-cebae97-JIT/bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_compile  | 48.7 ms                                                                                                           | 42.0 ms: 1.16x faster                                                                                                 |
| regex_v8       | 9.78 ms                                                                                                           | 9.97 ms: 1.02x slower                                                                                                 |
| Geometric mean | (ref)                                                                                                             | 1.03x faster                                                                                                          |

Benchmark hidden because not significant (2): regex_dna, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250601-3.15.0a0-cebae97/bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json | results/bm-20250601-3.15.0a0-cebae97-JIT/bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| tomli_loads          | 926 ms                                                                                                            | 857 ms: 1.08x faster                                                                                                  |
| xml_etree_process    | 25.2 ms                                                                                                           | 23.3 ms: 1.08x faster                                                                                                 |
| xml_etree_generate   | 35.4 ms                                                                                                           | 33.6 ms: 1.05x faster                                                                                                 |
| unpickle_pure_python | 98.9 us                                                                                                           | 95.0 us: 1.04x faster                                                                                                 |
| pickle_pure_python   | 148 us                                                                                                            | 143 us: 1.04x faster                                                                                                  |
| json_dumps           | 4.46 ms                                                                                                           | 4.41 ms: 1.01x faster                                                                                                 |
| unpickle_list        | 1.98 us                                                                                                           | 1.96 us: 1.01x faster                                                                                                 |
| pickle_dict          | 12.9 us                                                                                                           | 13.0 us: 1.01x slower                                                                                                 |
| unpickle             | 6.29 us                                                                                                           | 6.37 us: 1.01x slower                                                                                                 |
| xml_etree_iterparse  | 43.3 ms                                                                                                           | 44.0 ms: 1.02x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                             | 1.02x faster                                                                                                          |

Benchmark hidden because not significant (4): xml_etree_parse, pickle, pickle_list, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250601-3.15.0a0-cebae97/bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json | results/bm-20250601-3.15.0a0-cebae97-JIT/bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 8.75 ms                                                                                                           | 8.76 ms: 1.00x slower                                                                                                 |
| python_startup_no_site | 6.26 ms                                                                                                           | 6.27 ms: 1.00x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                             | 1.00x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | results/bm-20250601-3.15.0a0-cebae97/bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json | results/bm-20250601-3.15.0a0-cebae97-JIT/bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| mako           | 4.93 ms                                                                                                           | 4.40 ms: 1.12x faster                                                                                                 |
| genshi_xml     | 21.7 ms                                                                                                           | 21.6 ms: 1.01x faster                                                                                                 |
| Geometric mean | (ref)                                                                                                             | 1.03x faster                                                                                                          |

Benchmark hidden because not significant (2): django_template, genshi_text

All benchmarks:
===============

| Benchmark                     | results/bm-20250601-3.15.0a0-cebae97/bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json | results/bm-20250601-3.15.0a0-cebae97-JIT/bm-20250601-macm4pro-arm64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json |
|-------------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| pprint_pformat                | 728 ms                                                                                                            | 590 ns: 1234007.81x faster                                                                                            |
| pprint_safe_repr              | 360 ms                                                                                                            | 344 ns: 1047034.77x faster                                                                                            |
| regex_compile                 | 48.7 ms                                                                                                           | 42.0 ms: 1.16x faster                                                                                                 |
| mako                          | 4.93 ms                                                                                                           | 4.40 ms: 1.12x faster                                                                                                 |
| tomli_loads                   | 926 ms                                                                                                            | 857 ms: 1.08x faster                                                                                                  |
| xml_etree_process             | 25.2 ms                                                                                                           | 23.3 ms: 1.08x faster                                                                                                 |
| xml_etree_generate            | 35.4 ms                                                                                                           | 33.6 ms: 1.05x faster                                                                                                 |
| float                         | 30.2 ms                                                                                                           | 28.9 ms: 1.04x faster                                                                                                 |
| fannkuch                      | 182 ms                                                                                                            | 174 ms: 1.04x faster                                                                                                  |
| unpickle_pure_python          | 98.9 us                                                                                                           | 95.0 us: 1.04x faster                                                                                                 |
| pickle_pure_python            | 148 us                                                                                                            | 143 us: 1.04x faster                                                                                                  |
| async_tree_none               | 114 ms                                                                                                            | 111 ms: 1.03x faster                                                                                                  |
| telco                         | 3.01 ms                                                                                                           | 2.91 ms: 1.03x faster                                                                                                 |
| scimark_monte_carlo           | 29.8 ms                                                                                                           | 28.9 ms: 1.03x faster                                                                                                 |
| pyflate                       | 197 ms                                                                                                            | 191 ms: 1.03x faster                                                                                                  |
| nqueens                       | 40.0 ms                                                                                                           | 39.0 ms: 1.03x faster                                                                                                 |
| generators                    | 18.0 ms                                                                                                           | 17.6 ms: 1.02x faster                                                                                                 |
| go                            | 58.4 ms                                                                                                           | 57.1 ms: 1.02x faster                                                                                                 |
| comprehensions                | 7.51 us                                                                                                           | 7.36 us: 1.02x faster                                                                                                 |
| raytrace                      | 120 ms                                                                                                            | 117 ms: 1.02x faster                                                                                                  |
| async_tree_memoization        | 150 ms                                                                                                            | 147 ms: 1.02x faster                                                                                                  |
| async_tree_io                 | 259 ms                                                                                                            | 254 ms: 1.02x faster                                                                                                  |
| deepcopy_reduce               | 1.15 us                                                                                                           | 1.13 us: 1.02x faster                                                                                                 |
| sqlite_synth                  | 960 ns                                                                                                            | 942 ns: 1.02x faster                                                                                                  |
| async_tree_eager              | 43.0 ms                                                                                                           | 42.2 ms: 1.02x faster                                                                                                 |
| scimark_lu                    | 48.3 ms                                                                                                           | 47.5 ms: 1.02x faster                                                                                                 |
| async_tree_none_tg            | 107 ms                                                                                                            | 105 ms: 1.02x faster                                                                                                  |
| sqlglot_v2_normalize          | 47.6 ms                                                                                                           | 46.9 ms: 1.02x faster                                                                                                 |
| deepcopy_memo                 | 13.0 us                                                                                                           | 12.8 us: 1.01x faster                                                                                                 |
| async_tree_io_tg              | 256 ms                                                                                                            | 252 ms: 1.01x faster                                                                                                  |
| sympy_sum                     | 56.8 ms                                                                                                           | 56.0 ms: 1.01x faster                                                                                                 |
| coroutines                    | 10.2 ms                                                                                                           | 10.1 ms: 1.01x faster                                                                                                 |
| async_tree_eager_tg           | 88.7 ms                                                                                                           | 87.6 ms: 1.01x faster                                                                                                 |
| json_dumps                    | 4.46 ms                                                                                                           | 4.41 ms: 1.01x faster                                                                                                 |
| unpickle_list                 | 1.98 us                                                                                                           | 1.96 us: 1.01x faster                                                                                                 |
| sqlglot_v2_parse              | 566 us                                                                                                            | 560 us: 1.01x faster                                                                                                  |
| richards_super                | 25.3 ms                                                                                                           | 25.0 ms: 1.01x faster                                                                                                 |
| richards                      | 22.3 ms                                                                                                           | 22.1 ms: 1.01x faster                                                                                                 |
| pathlib                       | 11.3 ms                                                                                                           | 11.2 ms: 1.01x faster                                                                                                 |
| deepcopy                      | 111 us                                                                                                            | 110 us: 1.01x faster                                                                                                  |
| genshi_xml                    | 21.7 ms                                                                                                           | 21.6 ms: 1.01x faster                                                                                                 |
| sqlglot_v2_transpile          | 690 us                                                                                                            | 687 us: 1.00x faster                                                                                                  |
| python_startup                | 8.75 ms                                                                                                           | 8.76 ms: 1.00x slower                                                                                                 |
| python_startup_no_site        | 6.26 ms                                                                                                           | 6.27 ms: 1.00x slower                                                                                                 |
| asyncio_websockets            | 193 ms                                                                                                            | 193 ms: 1.00x slower                                                                                                  |
| scimark_fft                   | 131 ms                                                                                                            | 131 ms: 1.00x slower                                                                                                  |
| async_tree_eager_cpu_io_mixed | 225 ms                                                                                                            | 226 ms: 1.00x slower                                                                                                  |
| pickle_dict                   | 12.9 us                                                                                                           | 13.0 us: 1.01x slower                                                                                                 |
| chaos                         | 26.4 ms                                                                                                           | 26.5 ms: 1.01x slower                                                                                                 |
| async_tree_cpu_io_mixed_tg    | 265 ms                                                                                                            | 267 ms: 1.01x slower                                                                                                  |
| html5lib                      | 24.3 ms                                                                                                           | 24.5 ms: 1.01x slower                                                                                                 |
| create_gc_cycles              | 948 us                                                                                                            | 954 us: 1.01x slower                                                                                                  |
| async_tree_cpu_io_mixed       | 267 ms                                                                                                            | 268 ms: 1.01x slower                                                                                                  |
| coverage                      | 32.9 ms                                                                                                           | 33.2 ms: 1.01x slower                                                                                                 |
| sympy_expand                  | 168 ms                                                                                                            | 169 ms: 1.01x slower                                                                                                  |
| bench_mp_pool                 | 44.8 ms                                                                                                           | 45.1 ms: 1.01x slower                                                                                                 |
| logging_silent                | 197 ns                                                                                                            | 198 ns: 1.01x slower                                                                                                  |
| typing_runtime_protocols      | 61.9 us                                                                                                           | 62.6 us: 1.01x slower                                                                                                 |
| unpickle                      | 6.29 us                                                                                                           | 6.37 us: 1.01x slower                                                                                                 |
| docutils                      | 1.06 sec                                                                                                          | 1.07 sec: 1.01x slower                                                                                                |
| subparsers                    | 9.67 ms                                                                                                           | 9.79 ms: 1.01x slower                                                                                                 |
| sympy_integrate               | 7.53 ms                                                                                                           | 7.62 ms: 1.01x slower                                                                                                 |
| hexiom                        | 2.80 ms                                                                                                           | 2.84 ms: 1.01x slower                                                                                                 |
| xml_etree_iterparse           | 43.3 ms                                                                                                           | 44.0 ms: 1.02x slower                                                                                                 |
| pycparser                     | 503 ms                                                                                                            | 512 ms: 1.02x slower                                                                                                  |
| regex_v8                      | 9.78 ms                                                                                                           | 9.97 ms: 1.02x slower                                                                                                 |
| bpe_tokeniser                 | 1.97 sec                                                                                                          | 2.01 sec: 1.02x slower                                                                                                |
| nbody                         | 48.1 ms                                                                                                           | 49.2 ms: 1.02x slower                                                                                                 |
| crypto_pyaes                  | 38.1 ms                                                                                                           | 38.9 ms: 1.02x slower                                                                                                 |
| mdp                           | 514 ms                                                                                                            | 527 ms: 1.02x slower                                                                                                  |
| meteor_contest                | 48.3 ms                                                                                                           | 49.6 ms: 1.03x slower                                                                                                 |
| many_optionals                | 246 us                                                                                                            | 254 us: 1.03x slower                                                                                                  |
| 2to3                          | 114 ms                                                                                                            | 118 ms: 1.03x slower                                                                                                  |
| k_core                        | 951 ms                                                                                                            | 990 ms: 1.04x slower                                                                                                  |
| connected_components          | 203 ms                                                                                                            | 212 ms: 1.04x slower                                                                                                  |
| shortest_path                 | 220 ms                                                                                                            | 230 ms: 1.05x slower                                                                                                  |
| async_generators              | 173 ms                                                                                                            | 184 ms: 1.06x slower                                                                                                  |
| deltablue                     | 1.54 ms                                                                                                           | 1.64 ms: 1.07x slower                                                                                                 |
| gc_traversal                  | 2.11 ms                                                                                                           | 2.29 ms: 1.09x slower                                                                                                 |
| scimark_sparse_mat_mult       | 1.89 ms                                                                                                           | 2.10 ms: 1.11x slower                                                                                                 |
| unpack_sequence               | 30.5 ns                                                                                                           | 38.1 ns: 1.25x slower                                                                                                 |
| Geometric mean                | (ref)                                                                                                             | 1.29x faster                                                                                                          |

Benchmark hidden because not significant (30): async_tree_eager_io_tg, xml_etree_parse, thrift, json, logging_simple, async_tree_eager_io, sphinx, pickle, dulwich_log, async_tree_eager_memoization_tg, logging_format, async_tree_memoization_tg, django_template, pidigits, dask, sympy_str, spectral_norm, sqlglot_v2_optimize, scimark_sor, regex_dna, genshi_text, bench_thread_pool, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_memoization, pickle_list, regex_effbot, json_loads, asyncio_tcp, pylint, asyncio_tcp_ssl

- Geometric mean (including insignificant results): 1.330x faster

# HPT report

- Reliability score: 70.57% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x