# Results vs. 3.12.6

- fork: python
- ref: e123a1d09bcb75aae0c5
- machine: darwin-arm64
- commit hash: e123a1d
- commit date: 2025-05-14
- overall geometric mean: 1.079x faster
- HPT reliability: 92.75%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.27x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250514-macm4pro-arm64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 124 ms: 1.09x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.02 sec: 1.01x faster                                                  |
| html5lib       | 23.0 ms                                                  | 25.9 ms: 1.13x slower                                                   |
| sphinx         | 434 ms                                                   | 423 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                    | 1.04x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250514-macm4pro-arm64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 198 ms: 2.42x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 206 ms: 2.41x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 195 ms: 2.28x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 210 ms: 2.19x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 88.0 ms: 1.96x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.85x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.74x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 131 ms: 1.70x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 237 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 245 ms: 1.36x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.18x faster                                                    |
| async_generators                 | 206 ms                                                   | 183 ms: 1.13x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 228 ms: 1.07x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 50.5 ms: 1.11x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.7 ms: 2.45x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.37x faster                                                            |

Benchmark hidden because not significant (1): async_tree_eager_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250514-macm4pro-arm64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.4 ms: 1.33x faster                                                   |
| pidigits       | 161 ms                                                   | 163 ms: 1.01x slower                                                    |
| nbody          | 54.2 ms                                                  | 57.2 ms: 1.06x slower                                                   |
| Geometric mean | (ref)                                                    | 1.08x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250514-macm4pro-arm64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.52 ms: 1.09x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.32 ms: 1.03x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 98.0 ms: 1.02x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 53.9 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                    | 1.04x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250514-macm4pro-arm64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.4 ms: 1.31x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 58.9 ms: 1.15x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 37.9 ms: 1.03x faster                                                   |
| tomli_loads          | 957 ms                                                   | 980 ms: 1.02x slower                                                    |
| xml_etree_process    | 26.7 ms                                                  | 27.7 ms: 1.03x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 110 us: 1.07x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 154 us: 1.11x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 4.84 ms: 1.14x slower                                                   |
| json_loads           | 10.9 us                                                  | 12.6 us: 1.16x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.01x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250514-macm4pro-arm64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.48 ms: 1.18x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.91 ms: 1.21x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.20x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250514-macm4pro-arm64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 23.6 ms: 1.08x slower                                                   |
| genshi_text     | 10.5 ms                                                  | 11.5 ms: 1.10x slower                                                   |
| mako            | 4.77 ms                                                  | 5.61 ms: 1.17x slower                                                   |
| django_template | 13.6 ms                                                  | 17.2 ms: 1.26x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.15x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250514-macm4pro-arm64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 772 us: 2.60x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 198 ms: 2.42x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 206 ms: 2.41x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 195 ms: 2.28x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 210 ms: 2.19x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 10.1 ms: 2.06x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 88.0 ms: 1.96x faster                                                   |
| mdp                              | 1.09 sec                                                 | 582 ms: 1.88x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.85x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.74x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 487 us: 1.70x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 131 ms: 1.70x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 237 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 245 ms: 1.36x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                   |
| float                            | 37.9 ms                                                  | 28.4 ms: 1.33x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.4 ms: 1.31x faster                                                   |
| deepcopy                         | 161 us                                                   | 125 us: 1.29x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 14.3 us: 1.28x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.18x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 827 ns: 1.17x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.9 ms: 1.16x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.27 us: 1.15x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 58.9 ms: 1.15x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.97 sec: 1.14x faster                                                  |
| async_generators                 | 206 ms                                                   | 183 ms: 1.13x faster                                                    |
| k_core                           | 1.12 sec                                                 | 993 ms: 1.13x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 19.0 ms: 1.12x faster                                                   |
| go                               | 70.0 ms                                                  | 62.6 ms: 1.12x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 8.82 us: 1.12x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 11.2 ms: 1.10x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 55.6 ms: 1.10x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.52 ms: 1.09x faster                                                   |
| raytrace                         | 145 ms                                                   | 132 ms: 1.09x faster                                                    |
| pyflate                          | 216 ms                                                   | 201 ms: 1.08x faster                                                    |
| pylint                           | 128 ms                                                   | 120 ms: 1.07x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.62 ms: 1.06x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 51.2 ms: 1.06x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 41.7 ms: 1.04x faster                                                   |
| pycparser                        | 497 ms                                                   | 478 ms: 1.04x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.32 ms: 1.03x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 37.9 ms: 1.03x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.03x faster                                                    |
| sphinx                           | 434 ms                                                   | 423 ms: 1.02x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 98.0 ms: 1.02x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 53.9 ms: 1.01x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                    |
| docutils                         | 1.02 sec                                                 | 1.02 sec: 1.01x faster                                                  |
| scimark_fft                      | 142 ms                                                   | 143 ms: 1.01x slower                                                    |
| pidigits                         | 161 ms                                                   | 163 ms: 1.01x slower                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.11 ms: 1.01x slower                                                   |
| tomli_loads                      | 957 ms                                                   | 980 ms: 1.02x slower                                                    |
| chaos                            | 28.9 ms                                                  | 29.7 ms: 1.03x slower                                                   |
| xml_etree_process                | 26.7 ms                                                  | 27.7 ms: 1.03x slower                                                   |
| thrift                           | 322 us                                                   | 336 us: 1.04x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.6 ms: 1.04x slower                                                   |
| hexiom                           | 3.04 ms                                                  | 3.18 ms: 1.05x slower                                                   |
| fannkuch                         | 176 ms                                                   | 184 ms: 1.05x slower                                                    |
| nbody                            | 54.2 ms                                                  | 57.2 ms: 1.06x slower                                                   |
| shortest_path                    | 219 ms                                                   | 231 ms: 1.06x slower                                                    |
| sympy_str                        | 104 ms                                                   | 111 ms: 1.06x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.21 ms: 1.07x slower                                                   |
| sympy_sum                        | 57.6 ms                                                  | 61.5 ms: 1.07x slower                                                   |
| unpickle_pure_python             | 103 us                                                   | 110 us: 1.07x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 228 ms: 1.07x slower                                                    |
| json                             | 1.93 ms                                                  | 2.09 ms: 1.08x slower                                                   |
| genshi_xml                       | 21.8 ms                                                  | 23.6 ms: 1.08x slower                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 76.9 us: 1.08x slower                                                   |
| 2to3                             | 114 ms                                                   | 124 ms: 1.09x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 722 ms: 1.09x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 356 ms: 1.09x slower                                                    |
| connected_components             | 201 ms                                                   | 219 ms: 1.09x slower                                                    |
| richards                         | 22.4 ms                                                  | 24.4 ms: 1.09x slower                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 42.6 ms: 1.10x slower                                                   |
| genshi_text                      | 10.5 ms                                                  | 11.5 ms: 1.10x slower                                                   |
| richards_super                   | 25.4 ms                                                  | 28.0 ms: 1.10x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 154 us: 1.11x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 50.5 ms: 1.11x slower                                                   |
| logging_simple                   | 2.57 us                                                  | 2.87 us: 1.12x slower                                                   |
| logging_format                   | 2.80 us                                                  | 3.16 us: 1.13x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 25.9 ms: 1.13x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 45.0 ms: 1.13x slower                                                   |
| json_dumps                       | 4.26 ms                                                  | 4.84 ms: 1.14x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 190 ms: 1.14x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 55.4 ms: 1.16x slower                                                   |
| json_loads                       | 10.9 us                                                  | 12.6 us: 1.16x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.61 ms: 1.17x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.48 ms: 1.18x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.91 ms: 1.21x slower                                                   |
| django_template                  | 13.6 ms                                                  | 17.2 ms: 1.26x slower                                                   |
| scimark_lu                       | 51.3 ms                                                  | 66.4 ms: 1.30x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.41 ms: 1.31x slower                                                   |
| many_optionals                   | 195 us                                                   | 261 us: 1.34x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 584 us: 1.39x slower                                                    |
| coverage                         | 26.9 ms                                                  | 40.1 ms: 1.49x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.7 ms: 2.45x slower                                                   |
| logging_silent                   | 50.9 ns                                                  | 215 ns: 4.23x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.06x faster                                                            |

Benchmark hidden because not significant (1): async_tree_eager_memoization_tg
Ignored benchmarks (11) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250514-3.15.0a0-e123a1d-NOGIL/bm-20250514-macm4pro-arm64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.079x faster

# HPT report

- Reliability score: 92.75% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.27x