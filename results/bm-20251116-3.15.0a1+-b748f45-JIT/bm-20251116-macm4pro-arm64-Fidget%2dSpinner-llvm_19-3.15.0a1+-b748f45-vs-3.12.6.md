# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: llvm_19
- machine: darwin-arm64
- commit hash: b748f45
- commit date: 2025-11-16
- overall geometric mean: 1.138x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.25x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251116-macm4pro-arm64-Fidget%2dSpinner-llvm_19-3.15.0a1+-b748f45 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 112 ms: 1.02x faster                                                  |
| html5lib       | 23.0 ms                                                  | 22.2 ms: 1.04x faster                                                 |
| sphinx         | 434 ms                                                   | 403 ms: 1.08x faster                                                  |
| Geometric mean | (ref)                                                    | 1.04x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251116-macm4pro-arm64-Fidget%2dSpinner-llvm_19-3.15.0a1+-b748f45 |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 223 ms: 2.23x faster                                                  |
| async_tree_io_tg                 | 480 ms                                                   | 226 ms: 2.12x faster                                                  |
| async_tree_io                    | 459 ms                                                   | 226 ms: 2.03x faster                                                  |
| async_tree_eager_io_tg           | 446 ms                                                   | 222 ms: 2.00x faster                                                  |
| async_tree_none                  | 178 ms                                                   | 97.9 ms: 1.82x faster                                                 |
| async_tree_none_tg               | 172 ms                                                   | 95.6 ms: 1.80x faster                                                 |
| async_tree_memoization_tg        | 231 ms                                                   | 137 ms: 1.68x faster                                                  |
| async_tree_memoization           | 223 ms                                                   | 139 ms: 1.61x faster                                                  |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 247 ms: 1.37x faster                                                  |
| coroutines                       | 13.6 ms                                                  | 10.0 ms: 1.35x faster                                                 |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 247 ms: 1.35x faster                                                  |
| async_tree_eager_memoization     | 132 ms                                                   | 107 ms: 1.23x faster                                                  |
| async_generators                 | 206 ms                                                   | 181 ms: 1.14x faster                                                  |
| async_tree_eager                 | 45.6 ms                                                  | 41.8 ms: 1.09x faster                                                 |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                  |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                  |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 123 ms: 1.09x slower                                                  |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 240 ms: 1.13x slower                                                  |
| async_tree_eager_tg              | 32.1 ms                                                  | 80.4 ms: 2.50x slower                                                 |
| Geometric mean                   | (ref)                                                    | 1.33x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251116-macm4pro-arm64-Fidget%2dSpinner-llvm_19-3.15.0a1+-b748f45 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.2 ms: 1.30x faster                                                 |
| nbody          | 54.2 ms                                                  | 53.4 ms: 1.01x faster                                                 |
| pidigits       | 161 ms                                                   | 160 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                    | 1.10x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251116-macm4pro-arm64-Fidget%2dSpinner-llvm_19-3.15.0a1+-b748f45 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 44.6 ms: 1.22x faster                                                 |
| regex_effbot   | 1.67 ms                                                  | 1.41 ms: 1.18x faster                                                 |
| regex_dna      | 99.6 ms                                                  | 94.1 ms: 1.06x faster                                                 |
| Geometric mean | (ref)                                                    | 1.11x faster                                                          |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251116-macm4pro-arm64-Fidget%2dSpinner-llvm_19-3.15.0a1+-b748f45 |
|----------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 37.5 ms: 1.38x faster                                                 |
| tomli_loads          | 957 ms                                                   | 819 ms: 1.17x faster                                                  |
| xml_etree_parse      | 67.9 ms                                                  | 59.3 ms: 1.15x faster                                                 |
| xml_etree_generate   | 38.9 ms                                                  | 34.5 ms: 1.13x faster                                                 |
| xml_etree_process    | 26.7 ms                                                  | 23.8 ms: 1.12x faster                                                 |
| json_dumps           | 4.26 ms                                                  | 3.83 ms: 1.11x faster                                                 |
| unpickle_pure_python | 103 us                                                   | 92.7 us: 1.11x faster                                                 |
| pickle_pure_python   | 139 us                                                   | 131 us: 1.06x faster                                                  |
| json_loads           | 10.9 us                                                  | 10.7 us: 1.02x faster                                                 |
| Geometric mean       | (ref)                                                    | 1.13x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251116-macm4pro-arm64-Fidget%2dSpinner-llvm_19-3.15.0a1+-b748f45 |
|------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.77 ms: 1.09x slower                                                 |
| python_startup_no_site | 5.71 ms                                                  | 6.32 ms: 1.11x slower                                                 |
| Geometric mean         | (ref)                                                    | 1.10x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251116-macm4pro-arm64-Fidget%2dSpinner-llvm_19-3.15.0a1+-b748f45 |
|-----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.37 ms: 1.09x faster                                                 |
| genshi_text     | 10.5 ms                                                  | 10.2 ms: 1.03x faster                                                 |
| genshi_xml      | 21.8 ms                                                  | 23.2 ms: 1.07x slower                                                 |
| django_template | 13.6 ms                                                  | 14.8 ms: 1.08x slower                                                 |
| Geometric mean  | (ref)                                                    | 1.01x slower                                                          |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251116-macm4pro-arm64-Fidget%2dSpinner-llvm_19-3.15.0a1+-b748f45 |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 223 ms: 2.23x faster                                                  |
| async_tree_io_tg                 | 480 ms                                                   | 226 ms: 2.12x faster                                                  |
| async_tree_io                    | 459 ms                                                   | 226 ms: 2.03x faster                                                  |
| async_tree_eager_io_tg           | 446 ms                                                   | 222 ms: 2.00x faster                                                  |
| async_tree_none                  | 178 ms                                                   | 97.9 ms: 1.82x faster                                                 |
| async_tree_none_tg               | 172 ms                                                   | 95.6 ms: 1.80x faster                                                 |
| mdp                              | 1.09 sec                                                 | 613 ms: 1.78x faster                                                  |
| deepcopy_memo                    | 18.3 us                                                  | 10.8 us: 1.69x faster                                                 |
| async_tree_memoization_tg        | 231 ms                                                   | 137 ms: 1.68x faster                                                  |
| async_tree_memoization           | 223 ms                                                   | 139 ms: 1.61x faster                                                  |
| richards                         | 22.4 ms                                                  | 14.1 ms: 1.59x faster                                                 |
| deepcopy                         | 161 us                                                   | 102 us: 1.59x faster                                                  |
| richards_super                   | 25.4 ms                                                  | 16.4 ms: 1.55x faster                                                 |
| deepcopy_reduce                  | 1.46 us                                                  | 1.02 us: 1.43x faster                                                 |
| xml_etree_iterparse              | 51.6 ms                                                  | 37.5 ms: 1.38x faster                                                 |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 247 ms: 1.37x faster                                                  |
| coroutines                       | 13.6 ms                                                  | 10.0 ms: 1.35x faster                                                 |
| comprehensions                   | 9.84 us                                                  | 7.28 us: 1.35x faster                                                 |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 247 ms: 1.35x faster                                                  |
| float                            | 37.9 ms                                                  | 29.2 ms: 1.30x faster                                                 |
| async_tree_eager_memoization     | 132 ms                                                   | 107 ms: 1.23x faster                                                  |
| regex_compile                    | 54.6 ms                                                  | 44.6 ms: 1.22x faster                                                 |
| go                               | 70.0 ms                                                  | 57.4 ms: 1.22x faster                                                 |
| scimark_sor                      | 61.0 ms                                                  | 50.0 ms: 1.22x faster                                                 |
| raytrace                         | 145 ms                                                   | 120 ms: 1.21x faster                                                  |
| logging_simple                   | 2.57 us                                                  | 2.16 us: 1.19x faster                                                 |
| scimark_fft                      | 142 ms                                                   | 120 ms: 1.18x faster                                                  |
| regex_effbot                     | 1.67 ms                                                  | 1.41 ms: 1.18x faster                                                 |
| logging_format                   | 2.80 us                                                  | 2.38 us: 1.18x faster                                                 |
| generators                       | 21.9 ms                                                  | 18.8 ms: 1.17x faster                                                 |
| tomli_loads                      | 957 ms                                                   | 819 ms: 1.17x faster                                                  |
| scimark_monte_carlo              | 32.2 ms                                                  | 27.6 ms: 1.17x faster                                                 |
| subparsers                       | 20.8 ms                                                  | 17.8 ms: 1.17x faster                                                 |
| pyflate                          | 216 ms                                                   | 187 ms: 1.16x faster                                                  |
| pathlib                          | 12.4 ms                                                  | 10.7 ms: 1.15x faster                                                 |
| pprint_safe_repr                 | 328 ms                                                   | 286 ms: 1.15x faster                                                  |
| xml_etree_parse                  | 67.9 ms                                                  | 59.3 ms: 1.15x faster                                                 |
| deltablue                        | 1.73 ms                                                  | 1.51 ms: 1.14x faster                                                 |
| pprint_pformat                   | 665 ms                                                   | 583 ms: 1.14x faster                                                  |
| async_generators                 | 206 ms                                                   | 181 ms: 1.14x faster                                                  |
| xml_etree_generate               | 38.9 ms                                                  | 34.5 ms: 1.13x faster                                                 |
| spectral_norm                    | 54.4 ms                                                  | 48.2 ms: 1.13x faster                                                 |
| xml_etree_process                | 26.7 ms                                                  | 23.8 ms: 1.12x faster                                                 |
| json_dumps                       | 4.26 ms                                                  | 3.83 ms: 1.11x faster                                                 |
| unpickle_pure_python             | 103 us                                                   | 92.7 us: 1.11x faster                                                 |
| dulwich_log                      | 21.3 ms                                                  | 19.2 ms: 1.11x faster                                                 |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.03 sec: 1.10x faster                                                |
| mako                             | 4.77 ms                                                  | 4.37 ms: 1.09x faster                                                 |
| chaos                            | 28.9 ms                                                  | 26.5 ms: 1.09x faster                                                 |
| async_tree_eager                 | 45.6 ms                                                  | 41.8 ms: 1.09x faster                                                 |
| typing_runtime_protocols         | 71.0 us                                                  | 65.3 us: 1.09x faster                                                 |
| sphinx                           | 434 ms                                                   | 403 ms: 1.08x faster                                                  |
| thrift                           | 322 us                                                   | 300 us: 1.07x faster                                                  |
| pycparser                        | 497 ms                                                   | 468 ms: 1.06x faster                                                  |
| pickle_pure_python               | 139 us                                                   | 131 us: 1.06x faster                                                  |
| regex_dna                        | 99.6 ms                                                  | 94.1 ms: 1.06x faster                                                 |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                  |
| crypto_pyaes                     | 38.8 ms                                                  | 37.3 ms: 1.04x faster                                                 |
| html5lib                         | 23.0 ms                                                  | 22.2 ms: 1.04x faster                                                 |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.00 ms: 1.04x faster                                                 |
| logging_silent                   | 50.9 ns                                                  | 49.3 ns: 1.03x faster                                                 |
| genshi_text                      | 10.5 ms                                                  | 10.2 ms: 1.03x faster                                                 |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                  |
| scimark_lu                       | 51.3 ms                                                  | 50.0 ms: 1.03x faster                                                 |
| json                             | 1.93 ms                                                  | 1.90 ms: 1.02x faster                                                 |
| json_loads                       | 10.9 us                                                  | 10.7 us: 1.02x faster                                                 |
| 2to3                             | 114 ms                                                   | 112 ms: 1.02x faster                                                  |
| nqueens                          | 43.5 ms                                                  | 42.8 ms: 1.02x faster                                                 |
| nbody                            | 54.2 ms                                                  | 53.4 ms: 1.01x faster                                                 |
| sqlite_synth                     | 967 ns                                                   | 953 ns: 1.01x faster                                                  |
| pidigits                         | 161 ms                                                   | 160 ms: 1.01x faster                                                  |
| fannkuch                         | 176 ms                                                   | 177 ms: 1.01x slower                                                  |
| meteor_contest                   | 47.7 ms                                                  | 48.1 ms: 1.01x slower                                                 |
| gc_traversal                     | 2.01 ms                                                  | 2.03 ms: 1.01x slower                                                 |
| sympy_sum                        | 57.6 ms                                                  | 59.5 ms: 1.03x slower                                                 |
| dask                             | 528 ms                                                   | 547 ms: 1.04x slower                                                  |
| bench_thread_pool                | 419 us                                                   | 434 us: 1.04x slower                                                  |
| sympy_integrate                  | 8.02 ms                                                  | 8.32 ms: 1.04x slower                                                 |
| hexiom                           | 3.04 ms                                                  | 3.19 ms: 1.05x slower                                                 |
| telco                            | 2.61 ms                                                  | 2.76 ms: 1.06x slower                                                 |
| genshi_xml                       | 21.8 ms                                                  | 23.2 ms: 1.07x slower                                                 |
| sympy_str                        | 104 ms                                                   | 112 ms: 1.07x slower                                                  |
| sympy_expand                     | 167 ms                                                   | 179 ms: 1.07x slower                                                  |
| django_template                  | 13.6 ms                                                  | 14.8 ms: 1.08x slower                                                 |
| python_startup                   | 8.01 ms                                                  | 8.77 ms: 1.09x slower                                                 |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 123 ms: 1.09x slower                                                  |
| create_gc_cycles                 | 830 us                                                   | 909 us: 1.10x slower                                                  |
| bench_mp_pool                    | 39.7 ms                                                  | 43.9 ms: 1.11x slower                                                 |
| python_startup_no_site           | 5.71 ms                                                  | 6.32 ms: 1.11x slower                                                 |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 240 ms: 1.13x slower                                                  |
| coverage                         | 26.9 ms                                                  | 33.3 ms: 1.24x slower                                                 |
| many_optionals                   | 195 us                                                   | 361 us: 1.85x slower                                                  |
| async_tree_eager_tg              | 32.1 ms                                                  | 80.4 ms: 2.50x slower                                                 |
| Geometric mean                   | (ref)                                                    | 1.13x faster                                                          |

Benchmark hidden because not significant (2): pylint, regex_v8
Ignored benchmarks (14) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, connected_components, djangocms, docutils, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251116-3.15.0a1+-b748f45-JIT/bm-20251116-macm4pro-arm64-Fidget%2dSpinner-llvm_19-3.15.0a1+-b748f45.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.138x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.25x