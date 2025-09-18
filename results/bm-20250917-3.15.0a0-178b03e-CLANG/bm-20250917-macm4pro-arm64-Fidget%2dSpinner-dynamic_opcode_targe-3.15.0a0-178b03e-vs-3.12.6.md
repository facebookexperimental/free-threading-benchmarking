# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: dynamic_opcode_targe
- machine: darwin-arm64
- commit hash: 178b03e
- commit date: 2025-09-17
- overall geometric mean: 1.147x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250917-macm4pro-arm64-Fidget%2dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 108 ms: 1.06x faster                                                              |
| docutils       | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                            |
| html5lib       | 23.0 ms                                                  | 21.9 ms: 1.05x faster                                                             |
| sphinx         | 434 ms                                                   | 401 ms: 1.08x faster                                                              |
| Geometric mean | (ref)                                                    | 1.04x faster                                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250917-macm4pro-arm64-Fidget%2dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 235 ms: 2.11x faster                                                              |
| async_tree_io_tg                 | 480 ms                                                   | 242 ms: 1.98x faster                                                              |
| async_tree_io                    | 459 ms                                                   | 245 ms: 1.88x faster                                                              |
| async_tree_eager_io_tg           | 446 ms                                                   | 240 ms: 1.86x faster                                                              |
| async_tree_none_tg               | 172 ms                                                   | 101 ms: 1.70x faster                                                              |
| async_tree_none                  | 178 ms                                                   | 110 ms: 1.63x faster                                                              |
| async_tree_memoization_tg        | 231 ms                                                   | 144 ms: 1.60x faster                                                              |
| async_tree_memoization           | 223 ms                                                   | 145 ms: 1.54x faster                                                              |
| coroutines                       | 13.6 ms                                                  | 10.0 ms: 1.36x faster                                                             |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 256 ms: 1.32x faster                                                              |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 257 ms: 1.30x faster                                                              |
| async_tree_eager_memoization     | 132 ms                                                   | 107 ms: 1.24x faster                                                              |
| async_generators                 | 206 ms                                                   | 169 ms: 1.22x faster                                                              |
| async_tree_eager                 | 45.6 ms                                                  | 38.8 ms: 1.18x faster                                                             |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 217 ms: 1.06x faster                                                              |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                              |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 127 ms: 1.12x slower                                                              |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 241 ms: 1.14x slower                                                              |
| async_tree_eager_tg              | 32.1 ms                                                  | 83.3 ms: 2.59x slower                                                             |
| Geometric mean                   | (ref)                                                    | 1.29x faster                                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250917-macm4pro-arm64-Fidget%2dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.3 ms: 1.29x faster                                                             |
| nbody          | 54.2 ms                                                  | 48.5 ms: 1.12x faster                                                             |
| pidigits       | 161 ms                                                   | 162 ms: 1.01x slower                                                              |
| Geometric mean | (ref)                                                    | 1.13x faster                                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250917-macm4pro-arm64-Fidget%2dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 43.5 ms: 1.25x faster                                                             |
| regex_dna      | 99.6 ms                                                  | 104 ms: 1.04x slower                                                              |
| regex_effbot   | 1.67 ms                                                  | 1.74 ms: 1.05x slower                                                             |
| regex_v8       | 9.59 ms                                                  | 11.2 ms: 1.17x slower                                                             |
| Geometric mean | (ref)                                                    | 1.00x slower                                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250917-macm4pro-arm64-Fidget%2dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e |
|----------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| tomli_loads          | 957 ms                                                   | 778 ms: 1.23x faster                                                              |
| xml_etree_generate   | 38.9 ms                                                  | 32.9 ms: 1.18x faster                                                             |
| xml_etree_iterparse  | 51.6 ms                                                  | 44.3 ms: 1.16x faster                                                             |
| json_dumps           | 4.26 ms                                                  | 3.68 ms: 1.16x faster                                                             |
| unpickle_pure_python | 103 us                                                   | 91.4 us: 1.13x faster                                                             |
| xml_etree_process    | 26.7 ms                                                  | 23.8 ms: 1.13x faster                                                             |
| xml_etree_parse      | 67.9 ms                                                  | 64.6 ms: 1.05x faster                                                             |
| pickle_pure_python   | 139 us                                                   | 134 us: 1.04x faster                                                              |
| json_loads           | 10.9 us                                                  | 10.7 us: 1.02x faster                                                             |
| Geometric mean       | (ref)                                                    | 1.12x faster                                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250917-macm4pro-arm64-Fidget%2dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e |
|------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.59 ms: 1.07x slower                                                             |
| python_startup_no_site | 5.71 ms                                                  | 6.15 ms: 1.08x slower                                                             |
| Geometric mean         | (ref)                                                    | 1.07x slower                                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250917-macm4pro-arm64-Fidget%2dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e |
|-----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.06 ms: 1.16x faster                                                             |
| genshi_xml      | 21.8 ms                                                  | 19.5 ms: 1.12x faster                                                             |
| mako            | 4.77 ms                                                  | 4.69 ms: 1.02x faster                                                             |
| django_template | 13.6 ms                                                  | 14.0 ms: 1.02x slower                                                             |
| Geometric mean  | (ref)                                                    | 1.06x faster                                                                      |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250917-macm4pro-arm64-Fidget%2dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 235 ms: 2.11x faster                                                              |
| mdp                              | 1.09 sec                                                 | 520 ms: 2.10x faster                                                              |
| async_tree_io_tg                 | 480 ms                                                   | 242 ms: 1.98x faster                                                              |
| async_tree_io                    | 459 ms                                                   | 245 ms: 1.88x faster                                                              |
| async_tree_eager_io_tg           | 446 ms                                                   | 240 ms: 1.86x faster                                                              |
| async_tree_none_tg               | 172 ms                                                   | 101 ms: 1.70x faster                                                              |
| deepcopy                         | 161 us                                                   | 97.3 us: 1.66x faster                                                             |
| deepcopy_memo                    | 18.3 us                                                  | 11.2 us: 1.63x faster                                                             |
| async_tree_none                  | 178 ms                                                   | 110 ms: 1.63x faster                                                              |
| async_tree_memoization_tg        | 231 ms                                                   | 144 ms: 1.60x faster                                                              |
| generators                       | 21.9 ms                                                  | 14.2 ms: 1.54x faster                                                             |
| async_tree_memoization           | 223 ms                                                   | 145 ms: 1.54x faster                                                              |
| comprehensions                   | 9.84 us                                                  | 6.88 us: 1.43x faster                                                             |
| deepcopy_reduce                  | 1.46 us                                                  | 1.05 us: 1.39x faster                                                             |
| go                               | 70.0 ms                                                  | 50.6 ms: 1.38x faster                                                             |
| coroutines                       | 13.6 ms                                                  | 10.0 ms: 1.36x faster                                                             |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 256 ms: 1.32x faster                                                              |
| logging_silent                   | 50.9 ns                                                  | 38.7 ns: 1.31x faster                                                             |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 257 ms: 1.30x faster                                                              |
| float                            | 37.9 ms                                                  | 29.3 ms: 1.29x faster                                                             |
| raytrace                         | 145 ms                                                   | 115 ms: 1.26x faster                                                              |
| regex_compile                    | 54.6 ms                                                  | 43.5 ms: 1.25x faster                                                             |
| dulwich_log                      | 21.3 ms                                                  | 17.1 ms: 1.25x faster                                                             |
| async_tree_eager_memoization     | 132 ms                                                   | 107 ms: 1.24x faster                                                              |
| tomli_loads                      | 957 ms                                                   | 778 ms: 1.23x faster                                                              |
| subparsers                       | 20.8 ms                                                  | 17.0 ms: 1.22x faster                                                             |
| async_generators                 | 206 ms                                                   | 169 ms: 1.22x faster                                                              |
| logging_format                   | 2.80 us                                                  | 2.32 us: 1.21x faster                                                             |
| spectral_norm                    | 54.4 ms                                                  | 45.1 ms: 1.20x faster                                                             |
| logging_simple                   | 2.57 us                                                  | 2.16 us: 1.19x faster                                                             |
| scimark_sor                      | 61.0 ms                                                  | 51.2 ms: 1.19x faster                                                             |
| hexiom                           | 3.04 ms                                                  | 2.55 ms: 1.19x faster                                                             |
| k_core                           | 1.12 sec                                                 | 942 ms: 1.19x faster                                                              |
| pathlib                          | 12.4 ms                                                  | 10.4 ms: 1.19x faster                                                             |
| deltablue                        | 1.73 ms                                                  | 1.46 ms: 1.18x faster                                                             |
| xml_etree_generate               | 38.9 ms                                                  | 32.9 ms: 1.18x faster                                                             |
| pylint                           | 128 ms                                                   | 108 ms: 1.18x faster                                                              |
| async_tree_eager                 | 45.6 ms                                                  | 38.8 ms: 1.18x faster                                                             |
| typing_runtime_protocols         | 71.0 us                                                  | 60.7 us: 1.17x faster                                                             |
| richards                         | 22.4 ms                                                  | 19.2 ms: 1.17x faster                                                             |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.92 sec: 1.16x faster                                                            |
| xml_etree_iterparse              | 51.6 ms                                                  | 44.3 ms: 1.16x faster                                                             |
| richards_super                   | 25.4 ms                                                  | 21.8 ms: 1.16x faster                                                             |
| pyflate                          | 216 ms                                                   | 186 ms: 1.16x faster                                                              |
| json_dumps                       | 4.26 ms                                                  | 3.68 ms: 1.16x faster                                                             |
| genshi_text                      | 10.5 ms                                                  | 9.06 ms: 1.16x faster                                                             |
| nqueens                          | 43.5 ms                                                  | 37.7 ms: 1.15x faster                                                             |
| chaos                            | 28.9 ms                                                  | 25.4 ms: 1.14x faster                                                             |
| scimark_lu                       | 51.3 ms                                                  | 45.2 ms: 1.14x faster                                                             |
| unpickle_pure_python             | 103 us                                                   | 91.4 us: 1.13x faster                                                             |
| xml_etree_process                | 26.7 ms                                                  | 23.8 ms: 1.13x faster                                                             |
| genshi_xml                       | 21.8 ms                                                  | 19.5 ms: 1.12x faster                                                             |
| nbody                            | 54.2 ms                                                  | 48.5 ms: 1.12x faster                                                             |
| sympy_integrate                  | 8.02 ms                                                  | 7.17 ms: 1.12x faster                                                             |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.1 ms: 1.11x faster                                                             |
| sympy_str                        | 104 ms                                                   | 94.4 ms: 1.10x faster                                                             |
| thrift                           | 322 us                                                   | 293 us: 1.10x faster                                                              |
| sympy_sum                        | 57.6 ms                                                  | 52.8 ms: 1.09x faster                                                             |
| sphinx                           | 434 ms                                                   | 401 ms: 1.08x faster                                                              |
| scimark_fft                      | 142 ms                                                   | 132 ms: 1.08x faster                                                              |
| pprint_pformat                   | 665 ms                                                   | 618 ms: 1.08x faster                                                              |
| pprint_safe_repr                 | 328 ms                                                   | 308 ms: 1.07x faster                                                              |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 217 ms: 1.06x faster                                                              |
| crypto_pyaes                     | 38.8 ms                                                  | 36.6 ms: 1.06x faster                                                             |
| sympy_expand                     | 167 ms                                                   | 157 ms: 1.06x faster                                                              |
| 2to3                             | 114 ms                                                   | 108 ms: 1.06x faster                                                              |
| bench_thread_pool                | 419 us                                                   | 396 us: 1.06x faster                                                              |
| xml_etree_parse                  | 67.9 ms                                                  | 64.6 ms: 1.05x faster                                                             |
| pycparser                        | 497 ms                                                   | 474 ms: 1.05x faster                                                              |
| html5lib                         | 23.0 ms                                                  | 21.9 ms: 1.05x faster                                                             |
| pickle_pure_python               | 139 us                                                   | 134 us: 1.04x faster                                                              |
| fannkuch                         | 176 ms                                                   | 170 ms: 1.03x faster                                                              |
| sqlite_synth                     | 967 ns                                                   | 937 ns: 1.03x faster                                                              |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.01 ms: 1.03x faster                                                             |
| json                             | 1.93 ms                                                  | 1.88 ms: 1.03x faster                                                             |
| json_loads                       | 10.9 us                                                  | 10.7 us: 1.02x faster                                                             |
| mako                             | 4.77 ms                                                  | 4.69 ms: 1.02x faster                                                             |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                              |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                              |
| shortest_path                    | 219 ms                                                   | 220 ms: 1.00x slower                                                              |
| pidigits                         | 161 ms                                                   | 162 ms: 1.01x slower                                                              |
| gc_traversal                     | 2.01 ms                                                  | 2.03 ms: 1.01x slower                                                             |
| meteor_contest                   | 47.7 ms                                                  | 48.3 ms: 1.01x slower                                                             |
| docutils                         | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                            |
| connected_components             | 201 ms                                                   | 206 ms: 1.02x slower                                                              |
| django_template                  | 13.6 ms                                                  | 14.0 ms: 1.02x slower                                                             |
| bench_mp_pool                    | 39.7 ms                                                  | 41.2 ms: 1.04x slower                                                             |
| regex_dna                        | 99.6 ms                                                  | 104 ms: 1.04x slower                                                              |
| regex_effbot                     | 1.67 ms                                                  | 1.74 ms: 1.05x slower                                                             |
| telco                            | 2.61 ms                                                  | 2.75 ms: 1.05x slower                                                             |
| python_startup                   | 8.01 ms                                                  | 8.59 ms: 1.07x slower                                                             |
| python_startup_no_site           | 5.71 ms                                                  | 6.15 ms: 1.08x slower                                                             |
| create_gc_cycles                 | 830 us                                                   | 919 us: 1.11x slower                                                              |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 127 ms: 1.12x slower                                                              |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 241 ms: 1.14x slower                                                              |
| regex_v8                         | 9.59 ms                                                  | 11.2 ms: 1.17x slower                                                             |
| coverage                         | 26.9 ms                                                  | 32.0 ms: 1.19x slower                                                             |
| many_optionals                   | 195 us                                                   | 306 us: 1.56x slower                                                              |
| async_tree_eager_tg              | 32.1 ms                                                  | 83.3 ms: 2.59x slower                                                             |
| Geometric mean                   | (ref)                                                    | 1.15x faster                                                                      |
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250917-3.15.0a0-178b03e-CLANG/bm-20250917-macm4pro-arm64-Fidget%2dSpinner-dynamic_opcode_targe-3.15.0a0-178b03e.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.147x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.10x
- 95% likely to have a speedup of 1.09x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.14x