# Results vs. base

- fork: python
- ref: bc26f95e8ff60ccca981
- machine: darwin-arm64
- commit hash: bc26f95
- commit date: 2025-03-22
- overall geometric mean: 1.019x faster
- HPT reliability: 91.36%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250322-3.14.0a6+-bc26f95/bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json | results/bm-20250322-3.14.0a6+-bc26f95-JIT/bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json |
|----------------|:-------------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 117 ms                                                                                                              | 120 ms: 1.02x slower                                                                                                    |
| docutils       | 1.09 sec                                                                                                            | 1.10 sec: 1.01x slower                                                                                                  |
| html5lib       | 24.1 ms                                                                                                             | 24.4 ms: 1.01x slower                                                                                                   |
| Geometric mean | (ref)                                                                                                               | 1.01x slower                                                                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | results/bm-20250322-3.14.0a6+-bc26f95/bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json | results/bm-20250322-3.14.0a6+-bc26f95-JIT/bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json |
|----------------------------------|:-------------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_io                    | 279 ms                                                                                                              | 277 ms: 1.01x faster                                                                                                    |
| asyncio_websockets               | 193 ms                                                                                                              | 194 ms: 1.01x slower                                                                                                    |
| async_tree_eager_cpu_io_mixed_tg | 249 ms                                                                                                              | 251 ms: 1.01x slower                                                                                                    |
| async_tree_cpu_io_mixed          | 269 ms                                                                                                              | 271 ms: 1.01x slower                                                                                                    |
| async_tree_eager_cpu_io_mixed    | 224 ms                                                                                                              | 226 ms: 1.01x slower                                                                                                    |
| async_tree_eager_memoization     | 117 ms                                                                                                              | 118 ms: 1.01x slower                                                                                                    |
| async_tree_cpu_io_mixed_tg       | 270 ms                                                                                                              | 272 ms: 1.01x slower                                                                                                    |
| async_tree_eager                 | 46.0 ms                                                                                                             | 46.7 ms: 1.01x slower                                                                                                   |
| coroutines                       | 11.9 ms                                                                                                             | 12.2 ms: 1.02x slower                                                                                                   |
| async_generators                 | 182 ms                                                                                                              | 197 ms: 1.08x slower                                                                                                    |
| Geometric mean                   | (ref)                                                                                                               | 1.00x slower                                                                                                            |

Benchmark hidden because not significant (11): asyncio_tcp, async_tree_none_tg, async_tree_eager_io_tg, async_tree_io_tg, async_tree_eager_tg, async_tree_eager_io, async_tree_memoization_tg, async_tree_memoization, async_tree_none, async_tree_eager_memoization_tg, asyncio_tcp_ssl

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250322-3.14.0a6+-bc26f95/bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json | results/bm-20250322-3.14.0a6+-bc26f95-JIT/bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json |
|----------------|:-------------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| nbody          | 60.2 ms                                                                                                             | 49.3 ms: 1.22x faster                                                                                                   |
| float          | 35.8 ms                                                                                                             | 32.7 ms: 1.09x faster                                                                                                   |
| pidigits       | 164 ms                                                                                                              | 163 ms: 1.01x faster                                                                                                    |
| Geometric mean | (ref)                                                                                                               | 1.10x faster                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250322-3.14.0a6+-bc26f95/bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json | results/bm-20250322-3.14.0a6+-bc26f95-JIT/bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json |
|----------------|:-------------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_compile  | 52.9 ms                                                                                                             | 51.9 ms: 1.02x faster                                                                                                   |
| regex_dna      | 93.7 ms                                                                                                             | 92.9 ms: 1.01x faster                                                                                                   |
| regex_effbot   | 1.42 ms                                                                                                             | 1.47 ms: 1.03x slower                                                                                                   |
| Geometric mean | (ref)                                                                                                               | 1.00x faster                                                                                                            |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250322-3.14.0a6+-bc26f95/bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json | results/bm-20250322-3.14.0a6+-bc26f95-JIT/bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json |
|----------------------|:-------------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| unpickle_pure_python | 113 us                                                                                                              | 96.1 us: 1.18x faster                                                                                                   |
| tomli_loads          | 995 ms                                                                                                              | 881 ms: 1.13x faster                                                                                                    |
| xml_etree_process    | 28.7 ms                                                                                                             | 25.8 ms: 1.11x faster                                                                                                   |
| xml_etree_generate   | 39.2 ms                                                                                                             | 36.1 ms: 1.09x faster                                                                                                   |
| pickle_pure_python   | 155 us                                                                                                              | 147 us: 1.05x faster                                                                                                    |
| unpickle             | 6.72 us                                                                                                             | 6.64 us: 1.01x faster                                                                                                   |
| pickle_dict          | 13.3 us                                                                                                             | 13.2 us: 1.01x faster                                                                                                   |
| unpickle_list        | 2.00 us                                                                                                             | 1.98 us: 1.01x faster                                                                                                   |
| json_loads           | 11.4 us                                                                                                             | 11.5 us: 1.01x slower                                                                                                   |
| json_dumps           | 5.19 ms                                                                                                             | 5.24 ms: 1.01x slower                                                                                                   |
| xml_etree_parse      | 61.3 ms                                                                                                             | 62.7 ms: 1.02x slower                                                                                                   |
| xml_etree_iterparse  | 46.5 ms                                                                                                             | 47.9 ms: 1.03x slower                                                                                                   |
| Geometric mean       | (ref)                                                                                                               | 1.04x faster                                                                                                            |

Benchmark hidden because not significant (2): pickle, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250322-3.14.0a6+-bc26f95/bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json | results/bm-20250322-3.14.0a6+-bc26f95-JIT/bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json |
|------------------------|:-------------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 8.71 ms                                                                                                             | 8.73 ms: 1.00x slower                                                                                                   |
| python_startup_no_site | 6.45 ms                                                                                                             | 6.47 ms: 1.00x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                               | 1.00x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250322-3.14.0a6+-bc26f95/bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json | results/bm-20250322-3.14.0a6+-bc26f95-JIT/bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json |
|-----------------|:-------------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| mako            | 5.30 ms                                                                                                             | 4.56 ms: 1.16x faster                                                                                                   |
| django_template | 17.2 ms                                                                                                             | 17.3 ms: 1.01x slower                                                                                                   |
| genshi_text     | 11.6 ms                                                                                                             | 11.7 ms: 1.01x slower                                                                                                   |
| genshi_xml      | 23.8 ms                                                                                                             | 24.2 ms: 1.02x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                               | 1.03x faster                                                                                                            |

All benchmarks:
===============

| Benchmark                        | results/bm-20250322-3.14.0a6+-bc26f95/bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json | results/bm-20250322-3.14.0a6+-bc26f95-JIT/bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json |
|----------------------------------|:-------------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| nbody                            | 60.2 ms                                                                                                             | 49.3 ms: 1.22x faster                                                                                                   |
| richards_super                   | 27.7 ms                                                                                                             | 23.6 ms: 1.18x faster                                                                                                   |
| unpickle_pure_python             | 113 us                                                                                                              | 96.1 us: 1.18x faster                                                                                                   |
| richards                         | 24.8 ms                                                                                                             | 21.2 ms: 1.17x faster                                                                                                   |
| fannkuch                         | 209 ms                                                                                                              | 179 ms: 1.16x faster                                                                                                    |
| mako                             | 5.30 ms                                                                                                             | 4.56 ms: 1.16x faster                                                                                                   |
| scimark_fft                      | 145 ms                                                                                                              | 127 ms: 1.15x faster                                                                                                    |
| pprint_safe_repr                 | 353 ms                                                                                                              | 310 ms: 1.14x faster                                                                                                    |
| pprint_pformat                   | 708 ms                                                                                                              | 623 ms: 1.14x faster                                                                                                    |
| tomli_loads                      | 995 ms                                                                                                              | 881 ms: 1.13x faster                                                                                                    |
| xml_etree_process                | 28.7 ms                                                                                                             | 25.8 ms: 1.11x faster                                                                                                   |
| float                            | 35.8 ms                                                                                                             | 32.7 ms: 1.09x faster                                                                                                   |
| xml_etree_generate               | 39.2 ms                                                                                                             | 36.1 ms: 1.09x faster                                                                                                   |
| pyflate                          | 227 ms                                                                                                              | 211 ms: 1.07x faster                                                                                                    |
| bpe_tokeniser                    | 2.23 sec                                                                                                            | 2.09 sec: 1.07x faster                                                                                                  |
| deltablue                        | 1.76 ms                                                                                                             | 1.65 ms: 1.07x faster                                                                                                   |
| comprehensions                   | 8.62 us                                                                                                             | 8.11 us: 1.06x faster                                                                                                   |
| pickle_pure_python               | 155 us                                                                                                              | 147 us: 1.05x faster                                                                                                    |
| nqueens                          | 46.3 ms                                                                                                             | 44.6 ms: 1.04x faster                                                                                                   |
| meteor_contest                   | 51.8 ms                                                                                                             | 50.4 ms: 1.03x faster                                                                                                   |
| k_core                           | 1.00 sec                                                                                                            | 974 ms: 1.03x faster                                                                                                    |
| mdp                              | 1.14 sec                                                                                                            | 1.10 sec: 1.03x faster                                                                                                  |
| scimark_lu                       | 56.6 ms                                                                                                             | 55.1 ms: 1.03x faster                                                                                                   |
| connected_components             | 212 ms                                                                                                              | 207 ms: 1.02x faster                                                                                                    |
| regex_compile                    | 52.9 ms                                                                                                             | 51.9 ms: 1.02x faster                                                                                                   |
| shortest_path                    | 231 ms                                                                                                              | 227 ms: 1.02x faster                                                                                                    |
| unpickle                         | 6.72 us                                                                                                             | 6.64 us: 1.01x faster                                                                                                   |
| sympy_sum                        | 58.1 ms                                                                                                             | 57.4 ms: 1.01x faster                                                                                                   |
| raytrace                         | 136 ms                                                                                                              | 135 ms: 1.01x faster                                                                                                    |
| scimark_sparse_mat_mult          | 2.01 ms                                                                                                             | 1.99 ms: 1.01x faster                                                                                                   |
| pickle_dict                      | 13.3 us                                                                                                             | 13.2 us: 1.01x faster                                                                                                   |
| unpickle_list                    | 2.00 us                                                                                                             | 1.98 us: 1.01x faster                                                                                                   |
| regex_dna                        | 93.7 ms                                                                                                             | 92.9 ms: 1.01x faster                                                                                                   |
| create_gc_cycles                 | 926 us                                                                                                              | 919 us: 1.01x faster                                                                                                    |
| bench_thread_pool                | 442 us                                                                                                              | 439 us: 1.01x faster                                                                                                    |
| crypto_pyaes                     | 42.7 ms                                                                                                             | 42.4 ms: 1.01x faster                                                                                                   |
| async_tree_io                    | 279 ms                                                                                                              | 277 ms: 1.01x faster                                                                                                    |
| pidigits                         | 164 ms                                                                                                              | 163 ms: 1.01x faster                                                                                                    |
| sqlglot_v2_transpile             | 751 us                                                                                                              | 747 us: 1.01x faster                                                                                                    |
| sqlglot_v2_parse                 | 624 us                                                                                                              | 621 us: 1.01x faster                                                                                                    |
| hexiom                           | 3.38 ms                                                                                                             | 3.36 ms: 1.01x faster                                                                                                   |
| scimark_sor                      | 63.3 ms                                                                                                             | 63.0 ms: 1.00x faster                                                                                                   |
| scimark_monte_carlo              | 33.9 ms                                                                                                             | 33.7 ms: 1.00x faster                                                                                                   |
| python_startup                   | 8.71 ms                                                                                                             | 8.73 ms: 1.00x slower                                                                                                   |
| python_startup_no_site           | 6.45 ms                                                                                                             | 6.47 ms: 1.00x slower                                                                                                   |
| sqlalchemy_declarative           | 46.6 ms                                                                                                             | 46.8 ms: 1.00x slower                                                                                                   |
| thrift                           | 322 us                                                                                                              | 324 us: 1.01x slower                                                                                                    |
| asyncio_websockets               | 193 ms                                                                                                              | 194 ms: 1.01x slower                                                                                                    |
| django_template                  | 17.2 ms                                                                                                             | 17.3 ms: 1.01x slower                                                                                                   |
| json_loads                       | 11.4 us                                                                                                             | 11.5 us: 1.01x slower                                                                                                   |
| dulwich_log                      | 18.2 ms                                                                                                             | 18.4 ms: 1.01x slower                                                                                                   |
| chaos                            | 30.3 ms                                                                                                             | 30.5 ms: 1.01x slower                                                                                                   |
| deepcopy_memo                    | 14.2 us                                                                                                             | 14.3 us: 1.01x slower                                                                                                   |
| docutils                         | 1.09 sec                                                                                                            | 1.10 sec: 1.01x slower                                                                                                  |
| async_tree_eager_cpu_io_mixed_tg | 249 ms                                                                                                              | 251 ms: 1.01x slower                                                                                                    |
| pathlib                          | 11.7 ms                                                                                                             | 11.8 ms: 1.01x slower                                                                                                   |
| bench_mp_pool                    | 38.4 ms                                                                                                             | 38.7 ms: 1.01x slower                                                                                                   |
| subparsers                       | 9.07 ms                                                                                                             | 9.14 ms: 1.01x slower                                                                                                   |
| genshi_text                      | 11.6 ms                                                                                                             | 11.7 ms: 1.01x slower                                                                                                   |
| json_dumps                       | 5.19 ms                                                                                                             | 5.24 ms: 1.01x slower                                                                                                   |
| async_tree_cpu_io_mixed          | 269 ms                                                                                                              | 271 ms: 1.01x slower                                                                                                    |
| async_tree_eager_cpu_io_mixed    | 224 ms                                                                                                              | 226 ms: 1.01x slower                                                                                                    |
| async_tree_eager_memoization     | 117 ms                                                                                                              | 118 ms: 1.01x slower                                                                                                    |
| sympy_integrate                  | 8.36 ms                                                                                                             | 8.44 ms: 1.01x slower                                                                                                   |
| json                             | 1.99 ms                                                                                                             | 2.01 ms: 1.01x slower                                                                                                   |
| async_tree_cpu_io_mixed_tg       | 270 ms                                                                                                              | 272 ms: 1.01x slower                                                                                                    |
| logging_simple                   | 2.60 us                                                                                                             | 2.63 us: 1.01x slower                                                                                                   |
| deepcopy                         | 117 us                                                                                                              | 119 us: 1.01x slower                                                                                                    |
| html5lib                         | 24.1 ms                                                                                                             | 24.4 ms: 1.01x slower                                                                                                   |
| pycparser                        | 518 ms                                                                                                              | 525 ms: 1.01x slower                                                                                                    |
| logging_format                   | 2.83 us                                                                                                             | 2.88 us: 1.01x slower                                                                                                   |
| async_tree_eager                 | 46.0 ms                                                                                                             | 46.7 ms: 1.01x slower                                                                                                   |
| genshi_xml                       | 23.8 ms                                                                                                             | 24.2 ms: 1.02x slower                                                                                                   |
| sympy_expand                     | 178 ms                                                                                                              | 181 ms: 1.02x slower                                                                                                    |
| 2to3                             | 117 ms                                                                                                              | 120 ms: 1.02x slower                                                                                                    |
| xml_etree_parse                  | 61.3 ms                                                                                                             | 62.7 ms: 1.02x slower                                                                                                   |
| coroutines                       | 11.9 ms                                                                                                             | 12.2 ms: 1.02x slower                                                                                                   |
| coverage                         | 32.8 ms                                                                                                             | 33.7 ms: 1.03x slower                                                                                                   |
| xml_etree_iterparse              | 46.5 ms                                                                                                             | 47.9 ms: 1.03x slower                                                                                                   |
| go                               | 65.9 ms                                                                                                             | 68.1 ms: 1.03x slower                                                                                                   |
| regex_effbot                     | 1.42 ms                                                                                                             | 1.47 ms: 1.03x slower                                                                                                   |
| many_optionals                   | 242 us                                                                                                              | 251 us: 1.04x slower                                                                                                    |
| async_generators                 | 182 ms                                                                                                              | 197 ms: 1.08x slower                                                                                                    |
| unpack_sequence                  | 29.6 ns                                                                                                             | 36.3 ns: 1.23x slower                                                                                                   |
| Geometric mean                   | (ref)                                                                                                               | 1.02x faster                                                                                                            |

Benchmark hidden because not significant (29): asyncio_tcp, telco, regex_v8, sqlite_synth, spectral_norm, async_tree_none_tg, typing_runtime_protocols, async_tree_eager_io_tg, sqlglot_v2_optimize, pickle, gc_traversal, pickle_list, async_tree_io_tg, generators, dask, async_tree_eager_tg, async_tree_eager_io, async_tree_memoization_tg, sqlalchemy_imperative, logging_silent, pylint, sqlglot_v2_normalize, sphinx, async_tree_memoization, sympy_str, async_tree_none, async_tree_eager_memoization_tg, asyncio_tcp_ssl, deepcopy_reduce

- Geometric mean (including insignificant results): 1.019x faster

# HPT report

- Reliability score: 91.36% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x