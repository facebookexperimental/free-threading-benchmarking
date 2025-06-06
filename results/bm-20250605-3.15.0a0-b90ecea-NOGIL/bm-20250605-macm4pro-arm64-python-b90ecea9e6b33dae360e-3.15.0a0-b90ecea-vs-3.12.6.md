# Results vs. 3.12.6

- fork: python
- ref: b90ecea9e6b33dae360e
- machine: darwin-arm64
- commit hash: b90ecea
- commit date: 2025-06-05
- overall geometric mean: 1.093x faster
- HPT reliability: 97.40%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.27x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250605-macm4pro-arm64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 122 ms: 1.07x slower                                                    |
| docutils       | 1.02 sec                                                 | 999 ms: 1.02x faster                                                    |
| html5lib       | 23.0 ms                                                  | 23.4 ms: 1.02x slower                                                   |
| sphinx         | 434 ms                                                   | 417 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                    | 1.01x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250605-macm4pro-arm64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 204 ms: 2.43x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 198 ms: 2.43x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 194 ms: 2.30x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 210 ms: 2.19x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 87.5 ms: 1.97x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.86x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.76x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 131 ms: 1.70x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 237 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 246 ms: 1.36x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.5 ms: 1.29x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                    |
| async_generators                 | 206 ms                                                   | 179 ms: 1.15x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 229 ms: 1.08x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 49.9 ms: 1.09x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 79.1 ms: 2.46x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.37x faster                                                            |

Benchmark hidden because not significant (1): async_tree_eager_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250605-macm4pro-arm64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.9 ms: 1.31x faster                                                   |
| pidigits       | 161 ms                                                   | 163 ms: 1.01x slower                                                    |
| nbody          | 54.2 ms                                                  | 56.2 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                    | 1.08x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250605-macm4pro-arm64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.47 ms: 1.13x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.30 ms: 1.03x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 96.9 ms: 1.03x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 53.1 ms: 1.03x faster                                                   |
| Geometric mean | (ref)                                                    | 1.05x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250605-macm4pro-arm64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 37.4 ms: 1.38x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 56.2 ms: 1.21x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 36.8 ms: 1.06x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 27.1 ms: 1.01x slower                                                   |
| tomli_loads          | 957 ms                                                   | 984 ms: 1.03x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.5 us: 1.06x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 110 us: 1.07x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 4.64 ms: 1.09x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 152 us: 1.09x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.03x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250605-macm4pro-arm64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.45 ms: 1.18x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.88 ms: 1.21x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.19x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250605-macm4pro-arm64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 11.3 ms: 1.07x slower                                                   |
| genshi_xml      | 21.8 ms                                                  | 23.5 ms: 1.08x slower                                                   |
| mako            | 4.77 ms                                                  | 5.64 ms: 1.18x slower                                                   |
| django_template | 13.6 ms                                                  | 16.7 ms: 1.23x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.14x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250605-macm4pro-arm64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 779 us: 2.58x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 204 ms: 2.43x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 198 ms: 2.43x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 194 ms: 2.30x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 210 ms: 2.19x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 9.84 ms: 2.11x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 87.5 ms: 1.97x faster                                                   |
| mdp                              | 1.09 sec                                                 | 563 ms: 1.94x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.86x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.76x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 487 us: 1.70x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 131 ms: 1.70x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 237 ms: 1.43x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 37.4 ms: 1.38x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 246 ms: 1.36x faster                                                    |
| deepcopy                         | 161 us                                                   | 121 us: 1.34x faster                                                    |
| float                            | 37.9 ms                                                  | 28.9 ms: 1.31x faster                                                   |
| deepcopy_memo                    | 18.3 us                                                  | 13.9 us: 1.31x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.5 ms: 1.29x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.98 us: 1.23x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 56.2 ms: 1.21x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 823 ns: 1.17x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.25 us: 1.17x faster                                                   |
| async_generators                 | 206 ms                                                   | 179 ms: 1.15x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.96 sec: 1.14x faster                                                  |
| dulwich_log                      | 21.3 ms                                                  | 18.7 ms: 1.14x faster                                                   |
| k_core                           | 1.12 sec                                                 | 984 ms: 1.14x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.47 ms: 1.13x faster                                                   |
| generators                       | 21.9 ms                                                  | 19.4 ms: 1.13x faster                                                   |
| go                               | 70.0 ms                                                  | 62.3 ms: 1.12x faster                                                   |
| raytrace                         | 145 ms                                                   | 129 ms: 1.12x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.2 ms: 1.11x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 55.2 ms: 1.10x faster                                                   |
| pylint                           | 128 ms                                                   | 118 ms: 1.08x faster                                                    |
| pyflate                          | 216 ms                                                   | 200 ms: 1.08x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.62 ms: 1.06x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 41.0 ms: 1.06x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 36.8 ms: 1.06x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 51.7 ms: 1.05x faster                                                   |
| pycparser                        | 497 ms                                                   | 475 ms: 1.05x faster                                                    |
| sphinx                           | 434 ms                                                   | 417 ms: 1.04x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.30 ms: 1.03x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 96.9 ms: 1.03x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 53.1 ms: 1.03x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.03x faster                                                    |
| docutils                         | 1.02 sec                                                 | 999 ms: 1.02x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 140 ms: 1.01x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.97 ms: 1.01x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 3.07 ms: 1.01x slower                                                   |
| pidigits                         | 161 ms                                                   | 163 ms: 1.01x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 27.1 ms: 1.01x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 23.4 ms: 1.02x slower                                                   |
| chaos                            | 28.9 ms                                                  | 29.5 ms: 1.02x slower                                                   |
| json                             | 1.93 ms                                                  | 1.98 ms: 1.03x slower                                                   |
| tomli_loads                      | 957 ms                                                   | 984 ms: 1.03x slower                                                    |
| thrift                           | 322 us                                                   | 332 us: 1.03x slower                                                    |
| nbody                            | 54.2 ms                                                  | 56.2 ms: 1.04x slower                                                   |
| fannkuch                         | 176 ms                                                   | 182 ms: 1.04x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 73.9 us: 1.04x slower                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.6 ms: 1.04x slower                                                   |
| sympy_str                        | 104 ms                                                   | 109 ms: 1.05x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.18 ms: 1.05x slower                                                   |
| sympy_sum                        | 57.6 ms                                                  | 60.5 ms: 1.05x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.5 us: 1.06x slower                                                   |
| shortest_path                    | 219 ms                                                   | 232 ms: 1.06x slower                                                    |
| 2to3                             | 114 ms                                                   | 122 ms: 1.07x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 110 us: 1.07x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.3 ms: 1.07x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 229 ms: 1.08x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 23.5 ms: 1.08x slower                                                   |
| richards                         | 22.4 ms                                                  | 24.3 ms: 1.08x slower                                                   |
| richards_super                   | 25.4 ms                                                  | 27.6 ms: 1.09x slower                                                   |
| json_dumps                       | 4.26 ms                                                  | 4.64 ms: 1.09x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 152 us: 1.09x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 49.9 ms: 1.09x slower                                                   |
| logging_simple                   | 2.57 us                                                  | 2.82 us: 1.10x slower                                                   |
| connected_components             | 201 ms                                                   | 221 ms: 1.10x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 42.7 ms: 1.10x slower                                                   |
| logging_format                   | 2.80 us                                                  | 3.11 us: 1.11x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 53.3 ms: 1.12x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.5 ms: 1.12x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 189 ms: 1.13x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 380 ms: 1.16x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 773 ms: 1.16x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.45 ms: 1.18x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.64 ms: 1.18x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.88 ms: 1.21x slower                                                   |
| scimark_lu                       | 51.3 ms                                                  | 62.2 ms: 1.21x slower                                                   |
| django_template                  | 13.6 ms                                                  | 16.7 ms: 1.23x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.26 ms: 1.25x slower                                                   |
| many_optionals                   | 195 us                                                   | 255 us: 1.31x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 591 us: 1.41x slower                                                    |
| coverage                         | 26.9 ms                                                  | 40.3 ms: 1.50x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 79.1 ms: 2.46x slower                                                   |
| logging_silent                   | 50.9 ns                                                  | 217 ns: 4.27x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.07x faster                                                            |

Benchmark hidden because not significant (1): async_tree_eager_memoization_tg
Ignored benchmarks (11) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250605-3.15.0a0-b90ecea-NOGIL/bm-20250605-macm4pro-arm64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.093x faster

# HPT report

- Reliability score: 97.40% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.27x