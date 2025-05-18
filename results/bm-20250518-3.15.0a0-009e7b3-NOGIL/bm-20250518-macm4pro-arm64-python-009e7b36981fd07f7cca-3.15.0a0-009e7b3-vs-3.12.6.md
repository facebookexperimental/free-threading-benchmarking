# Results vs. 3.12.6

- fork: python
- ref: 009e7b36981fd07f7cca
- machine: darwin-arm64
- commit hash: 009e7b3
- commit date: 2025-05-18
- overall geometric mean: 1.079x faster
- HPT reliability: 93.11%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.27x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 124 ms: 1.09x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                  |
| html5lib       | 23.0 ms                                                  | 26.2 ms: 1.14x slower                                                   |
| sphinx         | 434 ms                                                   | 419 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                    | 1.04x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 198 ms: 2.42x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 206 ms: 2.41x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 196 ms: 2.28x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 211 ms: 2.18x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 88.0 ms: 1.96x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.86x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.74x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 131 ms: 1.70x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 235 ms: 1.44x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 243 ms: 1.37x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.18x faster                                                    |
| async_generators                 | 206 ms                                                   | 182 ms: 1.14x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 226 ms: 1.06x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 50.8 ms: 1.12x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 79.3 ms: 2.47x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.37x faster                                                            |

Benchmark hidden because not significant (1): async_tree_eager_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.5 ms: 1.33x faster                                                   |
| pidigits       | 161 ms                                                   | 162 ms: 1.00x slower                                                    |
| nbody          | 54.2 ms                                                  | 57.2 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                    | 1.08x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.51 ms: 1.10x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.32 ms: 1.03x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 53.7 ms: 1.02x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 99.0 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                    | 1.04x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.2 ms: 1.31x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 59.6 ms: 1.14x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 37.9 ms: 1.03x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 27.6 ms: 1.03x slower                                                   |
| tomli_loads          | 957 ms                                                   | 992 ms: 1.04x slower                                                    |
| unpickle_pure_python | 103 us                                                   | 110 us: 1.07x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 156 us: 1.12x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 4.83 ms: 1.13x slower                                                   |
| json_loads           | 10.9 us                                                  | 12.8 us: 1.18x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.01x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.45 ms: 1.18x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.88 ms: 1.21x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.19x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 23.8 ms: 1.09x slower                                                   |
| genshi_text     | 10.5 ms                                                  | 11.5 ms: 1.10x slower                                                   |
| mako            | 4.77 ms                                                  | 5.71 ms: 1.20x slower                                                   |
| django_template | 13.6 ms                                                  | 17.2 ms: 1.26x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.16x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 777 us: 2.58x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 198 ms: 2.42x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 206 ms: 2.41x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 196 ms: 2.28x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 211 ms: 2.18x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 9.93 ms: 2.09x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 88.0 ms: 1.96x faster                                                   |
| mdp                              | 1.09 sec                                                 | 580 ms: 1.88x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.86x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.74x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 484 us: 1.71x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 131 ms: 1.70x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 235 ms: 1.44x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 243 ms: 1.37x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                   |
| float                            | 37.9 ms                                                  | 28.5 ms: 1.33x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.2 ms: 1.31x faster                                                   |
| deepcopy                         | 161 us                                                   | 126 us: 1.28x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 14.3 us: 1.28x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.18x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 824 ns: 1.17x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.8 ms: 1.17x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 59.6 ms: 1.14x faster                                                   |
| async_generators                 | 206 ms                                                   | 182 ms: 1.14x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.30 us: 1.13x faster                                                   |
| k_core                           | 1.12 sec                                                 | 997 ms: 1.12x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.00 sec: 1.12x faster                                                  |
| dulwich_log                      | 21.3 ms                                                  | 19.0 ms: 1.12x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 8.84 us: 1.11x faster                                                   |
| go                               | 70.0 ms                                                  | 63.1 ms: 1.11x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 11.1 ms: 1.11x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.51 ms: 1.10x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 55.6 ms: 1.10x faster                                                   |
| raytrace                         | 145 ms                                                   | 132 ms: 1.10x faster                                                    |
| pyflate                          | 216 ms                                                   | 199 ms: 1.08x faster                                                    |
| pylint                           | 128 ms                                                   | 119 ms: 1.07x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.63 ms: 1.06x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 41.6 ms: 1.05x faster                                                   |
| pycparser                        | 497 ms                                                   | 476 ms: 1.04x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 52.3 ms: 1.04x faster                                                   |
| sphinx                           | 434 ms                                                   | 419 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.03x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.32 ms: 1.03x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 37.9 ms: 1.03x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 53.7 ms: 1.02x faster                                                   |
| docutils                         | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                  |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 99.0 ms: 1.01x faster                                                   |
| pidigits                         | 161 ms                                                   | 162 ms: 1.00x slower                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.06 ms: 1.00x slower                                                   |
| scimark_fft                      | 142 ms                                                   | 144 ms: 1.01x slower                                                    |
| chaos                            | 28.9 ms                                                  | 29.6 ms: 1.02x slower                                                   |
| xml_etree_process                | 26.7 ms                                                  | 27.6 ms: 1.03x slower                                                   |
| hexiom                           | 3.04 ms                                                  | 3.15 ms: 1.03x slower                                                   |
| tomli_loads                      | 957 ms                                                   | 992 ms: 1.04x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.7 ms: 1.05x slower                                                   |
| thrift                           | 322 us                                                   | 337 us: 1.05x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.18 ms: 1.05x slower                                                   |
| nbody                            | 54.2 ms                                                  | 57.2 ms: 1.05x slower                                                   |
| fannkuch                         | 176 ms                                                   | 185 ms: 1.06x slower                                                    |
| shortest_path                    | 219 ms                                                   | 231 ms: 1.06x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 61.1 ms: 1.06x slower                                                   |
| sympy_str                        | 104 ms                                                   | 111 ms: 1.06x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 226 ms: 1.06x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 110 us: 1.07x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 76.0 us: 1.07x slower                                                   |
| richards                         | 22.4 ms                                                  | 24.2 ms: 1.08x slower                                                   |
| json                             | 1.93 ms                                                  | 2.10 ms: 1.09x slower                                                   |
| 2to3                             | 114 ms                                                   | 124 ms: 1.09x slower                                                    |
| connected_components             | 201 ms                                                   | 219 ms: 1.09x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 23.8 ms: 1.09x slower                                                   |
| richards_super                   | 25.4 ms                                                  | 27.8 ms: 1.09x slower                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 359 ms: 1.10x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 730 ms: 1.10x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.5 ms: 1.10x slower                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 42.9 ms: 1.11x slower                                                   |
| logging_simple                   | 2.57 us                                                  | 2.86 us: 1.11x slower                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 50.8 ms: 1.12x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 156 us: 1.12x slower                                                    |
| logging_format                   | 2.80 us                                                  | 3.16 us: 1.13x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.9 ms: 1.13x slower                                                   |
| json_dumps                       | 4.26 ms                                                  | 4.83 ms: 1.13x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 26.2 ms: 1.14x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 190 ms: 1.14x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 55.5 ms: 1.16x slower                                                   |
| json_loads                       | 10.9 us                                                  | 12.8 us: 1.18x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.45 ms: 1.18x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.71 ms: 1.20x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.88 ms: 1.21x slower                                                   |
| django_template                  | 13.6 ms                                                  | 17.2 ms: 1.26x slower                                                   |
| scimark_lu                       | 51.3 ms                                                  | 65.6 ms: 1.28x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.37 ms: 1.29x slower                                                   |
| many_optionals                   | 195 us                                                   | 258 us: 1.32x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 601 us: 1.44x slower                                                    |
| coverage                         | 26.9 ms                                                  | 40.3 ms: 1.50x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 79.3 ms: 2.47x slower                                                   |
| logging_silent                   | 50.9 ns                                                  | 217 ns: 4.26x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.06x faster                                                            |

Benchmark hidden because not significant (1): async_tree_eager_memoization_tg
Ignored benchmarks (11) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250518-3.15.0a0-009e7b3-NOGIL/bm-20250518-macm4pro-arm64-python-009e7b36981fd07f7cca-3.15.0a0-009e7b3.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.079x faster

# HPT report

- Reliability score: 93.11% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.27x