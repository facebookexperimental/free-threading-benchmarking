# Results vs. base

- fork: python
- ref: c1df6843d36233ec1da7
- machine: darwin-arm64
- commit hash: c1df684
- commit date: 2026-09-19
- overall geometric mean: 1.100x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.05x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20260919-3.16.0a0-c1df684/bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684.json | results/bm-20260919-3.16.0a0-c1df684-JIT/bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 120 ms                                                                                                            | 118 ms: 1.01x faster                                                                                                  |
| docutils       | 947 ms                                                                                                            | 942 ms: 1.01x faster                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.00x faster                                                                                                          |

Benchmark hidden because not significant (2): html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                       | results/bm-20260919-3.16.0a0-c1df684/bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684.json | results/bm-20260919-3.16.0a0-c1df684-JIT/bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684.json |
|---------------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_none                 | 137 ms                                                                                                            | 124 ms: 1.11x faster                                                                                                  |
| async_tree_none_tg              | 126 ms                                                                                                            | 115 ms: 1.09x faster                                                                                                  |
| async_tree_io_tg                | 331 ms                                                                                                            | 305 ms: 1.09x faster                                                                                                  |
| async_tree_io                   | 344 ms                                                                                                            | 319 ms: 1.08x faster                                                                                                  |
| async_tree_eager_io_tg          | 344 ms                                                                                                            | 319 ms: 1.08x faster                                                                                                  |
| async_tree_eager_io             | 345 ms                                                                                                            | 321 ms: 1.07x faster                                                                                                  |
| async_tree_eager                | 65.1 ms                                                                                                           | 60.7 ms: 1.07x faster                                                                                                 |
| async_tree_memoization          | 184 ms                                                                                                            | 173 ms: 1.06x faster                                                                                                  |
| async_tree_eager_tg             | 104 ms                                                                                                            | 98.3 ms: 1.06x faster                                                                                                 |
| async_tree_memoization_tg       | 174 ms                                                                                                            | 166 ms: 1.05x faster                                                                                                  |
| async_tree_eager_memoization    | 134 ms                                                                                                            | 131 ms: 1.03x faster                                                                                                  |
| async_tree_cpu_io_mixed         | 285 ms                                                                                                            | 277 ms: 1.03x faster                                                                                                  |
| async_tree_eager_memoization_tg | 154 ms                                                                                                            | 151 ms: 1.02x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg      | 292 ms                                                                                                            | 288 ms: 1.02x faster                                                                                                  |
| asyncio_tcp_ssl                 | 545 ms                                                                                                            | 543 ms: 1.00x faster                                                                                                  |
| coroutines                      | 9.41 ms                                                                                                           | 9.84 ms: 1.05x slower                                                                                                 |
| async_generators                | 145 ms                                                                                                            | 152 ms: 1.05x slower                                                                                                  |
| Geometric mean                  | (ref)                                                                                                             | 1.04x faster                                                                                                          |

Benchmark hidden because not significant (4): async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, asyncio_websockets, asyncio_tcp

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20260919-3.16.0a0-c1df684/bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684.json | results/bm-20260919-3.16.0a0-c1df684-JIT/bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| nbody          | 42.7 ms                                                                                                           | 32.1 ms: 1.33x faster                                                                                                 |
| float          | 28.9 ms                                                                                                           | 23.3 ms: 1.24x faster                                                                                                 |
| Geometric mean | (ref)                                                                                                             | 1.18x faster                                                                                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20260919-3.16.0a0-c1df684/bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684.json | results/bm-20260919-3.16.0a0-c1df684-JIT/bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_compile  | 54.7 ms                                                                                                           | 46.9 ms: 1.17x faster                                                                                                 |
| regex_v8       | 9.29 ms                                                                                                           | 9.17 ms: 1.01x faster                                                                                                 |
| regex_effbot   | 1.32 ms                                                                                                           | 1.37 ms: 1.03x slower                                                                                                 |
| Geometric mean | (ref)                                                                                                             | 1.03x faster                                                                                                          |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20260919-3.16.0a0-c1df684/bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684.json | results/bm-20260919-3.16.0a0-c1df684-JIT/bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| pickle_pure_python   | 140 us                                                                                                            | 108 us: 1.29x faster                                                                                                  |
| unpickle_pure_python | 98.4 us                                                                                                           | 80.9 us: 1.22x faster                                                                                                 |
| xml_etree_process    | 25.2 ms                                                                                                           | 22.8 ms: 1.11x faster                                                                                                 |
| xml_etree_iterparse  | 43.5 ms                                                                                                           | 39.7 ms: 1.09x faster                                                                                                 |
| json_dumps           | 3.57 ms                                                                                                           | 3.32 ms: 1.08x faster                                                                                                 |
| tomli_loads          | 818 ms                                                                                                            | 767 ms: 1.07x faster                                                                                                  |
| xml_etree_generate   | 35.8 ms                                                                                                           | 33.6 ms: 1.06x faster                                                                                                 |
| unpickle             | 6.36 us                                                                                                           | 6.12 us: 1.04x faster                                                                                                 |
| xml_etree_parse      | 66.6 ms                                                                                                           | 65.8 ms: 1.01x faster                                                                                                 |
| pickle               | 6.09 us                                                                                                           | 6.03 us: 1.01x faster                                                                                                 |
| pickle_dict          | 12.9 us                                                                                                           | 12.9 us: 1.01x faster                                                                                                 |
| unpickle_list        | 2.06 us                                                                                                           | 2.07 us: 1.01x slower                                                                                                 |
| pickle_list          | 2.32 us                                                                                                           | 2.35 us: 1.01x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                             | 1.07x faster                                                                                                          |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20260919-3.16.0a0-c1df684/bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684.json | results/bm-20260919-3.16.0a0-c1df684-JIT/bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup_no_site | 6.71 ms                                                                                                           | 6.80 ms: 1.01x slower                                                                                                 |
| python_startup         | 9.20 ms                                                                                                           | 9.32 ms: 1.01x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                             | 1.01x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20260919-3.16.0a0-c1df684/bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684.json | results/bm-20260919-3.16.0a0-c1df684-JIT/bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| mako            | 4.62 ms                                                                                                           | 3.87 ms: 1.19x faster                                                                                                 |
| django_template | 14.9 ms                                                                                                           | 15.0 ms: 1.01x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                             | 1.09x faster                                                                                                          |

All benchmarks:
===============

| Benchmark                       | results/bm-20260919-3.16.0a0-c1df684/bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684.json | results/bm-20260919-3.16.0a0-c1df684-JIT/bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684.json |
|---------------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| richards_super                  | 23.2 ms                                                                                                           | 10.9 ms: 2.12x faster                                                                                                 |
| richards                        | 20.3 ms                                                                                                           | 9.73 ms: 2.08x faster                                                                                                 |
| scimark_lu                      | 49.7 ms                                                                                                           | 31.3 ms: 1.59x faster                                                                                                 |
| scimark_sor                     | 49.0 ms                                                                                                           | 32.5 ms: 1.51x faster                                                                                                 |
| spectral_norm                   | 42.8 ms                                                                                                           | 32.1 ms: 1.33x faster                                                                                                 |
| nbody                           | 42.7 ms                                                                                                           | 32.1 ms: 1.33x faster                                                                                                 |
| pickle_pure_python              | 140 us                                                                                                            | 108 us: 1.29x faster                                                                                                  |
| pprint_pformat                  | 658 ms                                                                                                            | 514 ms: 1.28x faster                                                                                                  |
| pprint_safe_repr                | 319 ms                                                                                                            | 252 ms: 1.26x faster                                                                                                  |
| scimark_fft                     | 121 ms                                                                                                            | 96.1 ms: 1.26x faster                                                                                                 |
| chaos                           | 25.5 ms                                                                                                           | 20.4 ms: 1.25x faster                                                                                                 |
| logging_format                  | 2.40 us                                                                                                           | 1.92 us: 1.25x faster                                                                                                 |
| deltablue                       | 1.48 ms                                                                                                           | 1.19 ms: 1.25x faster                                                                                                 |
| float                           | 28.9 ms                                                                                                           | 23.3 ms: 1.24x faster                                                                                                 |
| logging_simple                  | 2.17 us                                                                                                           | 1.75 us: 1.24x faster                                                                                                 |
| pyflate                         | 190 ms                                                                                                            | 154 ms: 1.23x faster                                                                                                  |
| unpickle_pure_python            | 98.4 us                                                                                                           | 80.9 us: 1.22x faster                                                                                                 |
| crypto_pyaes                    | 38.1 ms                                                                                                           | 31.4 ms: 1.21x faster                                                                                                 |
| raytrace                        | 120 ms                                                                                                            | 100.0 ms: 1.20x faster                                                                                                |
| mako                            | 4.62 ms                                                                                                           | 3.87 ms: 1.19x faster                                                                                                 |
| sqlglot_v2_parse                | 502 us                                                                                                            | 423 us: 1.19x faster                                                                                                  |
| regex_compile                   | 54.7 ms                                                                                                           | 46.9 ms: 1.17x faster                                                                                                 |
| scimark_monte_carlo             | 28.3 ms                                                                                                           | 24.4 ms: 1.16x faster                                                                                                 |
| sqlglot_v2_transpile            | 618 us                                                                                                            | 533 us: 1.16x faster                                                                                                  |
| nqueens                         | 34.8 ms                                                                                                           | 30.3 ms: 1.15x faster                                                                                                 |
| comprehensions                  | 6.62 us                                                                                                           | 5.89 us: 1.12x faster                                                                                                 |
| hexiom                          | 2.68 ms                                                                                                           | 2.41 ms: 1.11x faster                                                                                                 |
| async_tree_none                 | 137 ms                                                                                                            | 124 ms: 1.11x faster                                                                                                  |
| telco                           | 2.88 ms                                                                                                           | 2.60 ms: 1.11x faster                                                                                                 |
| typing_runtime_protocols        | 49.0 us                                                                                                           | 44.3 us: 1.11x faster                                                                                                 |
| xml_etree_process               | 25.2 ms                                                                                                           | 22.8 ms: 1.11x faster                                                                                                 |
| subparsers                      | 4.13 ms                                                                                                           | 3.74 ms: 1.11x faster                                                                                                 |
| sqlglot_v2_normalize            | 45.4 ms                                                                                                           | 41.2 ms: 1.10x faster                                                                                                 |
| xml_etree_iterparse             | 43.5 ms                                                                                                           | 39.7 ms: 1.09x faster                                                                                                 |
| scimark_sparse_mat_mult         | 1.85 ms                                                                                                           | 1.69 ms: 1.09x faster                                                                                                 |
| async_tree_none_tg              | 126 ms                                                                                                            | 115 ms: 1.09x faster                                                                                                  |
| deepcopy_memo                   | 11.8 us                                                                                                           | 10.8 us: 1.09x faster                                                                                                 |
| async_tree_io_tg                | 331 ms                                                                                                            | 305 ms: 1.09x faster                                                                                                  |
| go                              | 52.7 ms                                                                                                           | 48.5 ms: 1.09x faster                                                                                                 |
| async_tree_io                   | 344 ms                                                                                                            | 319 ms: 1.08x faster                                                                                                  |
| async_tree_eager_io_tg          | 344 ms                                                                                                            | 319 ms: 1.08x faster                                                                                                  |
| json_dumps                      | 3.57 ms                                                                                                           | 3.32 ms: 1.08x faster                                                                                                 |
| async_tree_eager_io             | 345 ms                                                                                                            | 321 ms: 1.07x faster                                                                                                  |
| async_tree_eager                | 65.1 ms                                                                                                           | 60.7 ms: 1.07x faster                                                                                                 |
| tomli_loads                     | 818 ms                                                                                                            | 767 ms: 1.07x faster                                                                                                  |
| meteor_contest                  | 48.8 ms                                                                                                           | 45.9 ms: 1.06x faster                                                                                                 |
| xml_etree_generate              | 35.8 ms                                                                                                           | 33.6 ms: 1.06x faster                                                                                                 |
| async_tree_memoization          | 184 ms                                                                                                            | 173 ms: 1.06x faster                                                                                                  |
| sqlglot_v2_optimize             | 22.2 ms                                                                                                           | 20.9 ms: 1.06x faster                                                                                                 |
| async_tree_eager_tg             | 104 ms                                                                                                            | 98.3 ms: 1.06x faster                                                                                                 |
| sympy_expand                    | 169 ms                                                                                                            | 160 ms: 1.06x faster                                                                                                  |
| many_optionals                  | 245 us                                                                                                            | 232 us: 1.06x faster                                                                                                  |
| bpe_tokeniser                   | 1.95 sec                                                                                                          | 1.85 sec: 1.06x faster                                                                                                |
| dulwich_log                     | 18.2 ms                                                                                                           | 17.3 ms: 1.05x faster                                                                                                 |
| async_tree_memoization_tg       | 174 ms                                                                                                            | 166 ms: 1.05x faster                                                                                                  |
| fannkuch                        | 159 ms                                                                                                            | 153 ms: 1.04x faster                                                                                                  |
| unpickle                        | 6.36 us                                                                                                           | 6.12 us: 1.04x faster                                                                                                 |
| deepcopy_reduce                 | 1.03 us                                                                                                           | 992 ns: 1.04x faster                                                                                                  |
| sympy_sum                       | 55.3 ms                                                                                                           | 53.3 ms: 1.04x faster                                                                                                 |
| sympy_str                       | 99.6 ms                                                                                                           | 96.2 ms: 1.04x faster                                                                                                 |
| json                            | 1.90 ms                                                                                                           | 1.84 ms: 1.03x faster                                                                                                 |
| async_tree_eager_memoization    | 134 ms                                                                                                            | 131 ms: 1.03x faster                                                                                                  |
| async_tree_cpu_io_mixed         | 285 ms                                                                                                            | 277 ms: 1.03x faster                                                                                                  |
| async_tree_eager_memoization_tg | 154 ms                                                                                                            | 151 ms: 1.02x faster                                                                                                  |
| thrift                          | 311 us                                                                                                            | 305 us: 1.02x faster                                                                                                  |
| connected_components            | 207 ms                                                                                                            | 204 ms: 1.02x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg      | 292 ms                                                                                                            | 288 ms: 1.02x faster                                                                                                  |
| pathlib                         | 10.6 ms                                                                                                           | 10.5 ms: 1.01x faster                                                                                                 |
| regex_v8                        | 9.29 ms                                                                                                           | 9.17 ms: 1.01x faster                                                                                                 |
| 2to3                            | 120 ms                                                                                                            | 118 ms: 1.01x faster                                                                                                  |
| xml_etree_parse                 | 66.6 ms                                                                                                           | 65.8 ms: 1.01x faster                                                                                                 |
| pickle                          | 6.09 us                                                                                                           | 6.03 us: 1.01x faster                                                                                                 |
| shortest_path                   | 224 ms                                                                                                            | 222 ms: 1.01x faster                                                                                                  |
| docutils                        | 947 ms                                                                                                            | 942 ms: 1.01x faster                                                                                                  |
| pickle_dict                     | 12.9 us                                                                                                           | 12.9 us: 1.01x faster                                                                                                 |
| asyncio_tcp_ssl                 | 545 ms                                                                                                            | 543 ms: 1.00x faster                                                                                                  |
| bench_mp_pool                   | 45.4 ms                                                                                                           | 45.7 ms: 1.01x slower                                                                                                 |
| generators                      | 17.2 ms                                                                                                           | 17.4 ms: 1.01x slower                                                                                                 |
| unpickle_list                   | 2.06 us                                                                                                           | 2.07 us: 1.01x slower                                                                                                 |
| deepcopy                        | 95.6 us                                                                                                           | 96.5 us: 1.01x slower                                                                                                 |
| django_template                 | 14.9 ms                                                                                                           | 15.0 ms: 1.01x slower                                                                                                 |
| sqlite_synth                    | 923 ns                                                                                                            | 931 ns: 1.01x slower                                                                                                  |
| bench_thread_pool               | 420 us                                                                                                            | 425 us: 1.01x slower                                                                                                  |
| python_startup_no_site          | 6.71 ms                                                                                                           | 6.80 ms: 1.01x slower                                                                                                 |
| python_startup                  | 9.20 ms                                                                                                           | 9.32 ms: 1.01x slower                                                                                                 |
| pickle_list                     | 2.32 us                                                                                                           | 2.35 us: 1.01x slower                                                                                                 |
| gc_traversal                    | 1.96 ms                                                                                                           | 1.99 ms: 1.01x slower                                                                                                 |
| create_gc_cycles                | 837 us                                                                                                            | 848 us: 1.01x slower                                                                                                  |
| pycparser                       | 486 ms                                                                                                            | 494 ms: 1.02x slower                                                                                                  |
| logging_silent                  | 41.5 ns                                                                                                           | 42.2 ns: 1.02x slower                                                                                                 |
| regex_effbot                    | 1.32 ms                                                                                                           | 1.37 ms: 1.03x slower                                                                                                 |
| coroutines                      | 9.41 ms                                                                                                           | 9.84 ms: 1.05x slower                                                                                                 |
| async_generators                | 145 ms                                                                                                            | 152 ms: 1.05x slower                                                                                                  |
| mdp                             | 511 ms                                                                                                            | 573 ms: 1.12x slower                                                                                                  |
| k_core                          | 980 ms                                                                                                            | 1.13 sec: 1.16x slower                                                                                                |
| unpack_sequence                 | 23.4 ns                                                                                                           | 30.5 ns: 1.30x slower                                                                                                 |
| Geometric mean                  | (ref)                                                                                                             | 1.08x faster                                                                                                          |

Benchmark hidden because not significant (11): async_tree_eager_cpu_io_mixed, sphinx, pylint, async_tree_eager_cpu_io_mixed_tg, asyncio_websockets, pidigits, asyncio_tcp, regex_dna, sympy_integrate, html5lib, json_loads

- Geometric mean (including insignificant results): 1.100x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.05x