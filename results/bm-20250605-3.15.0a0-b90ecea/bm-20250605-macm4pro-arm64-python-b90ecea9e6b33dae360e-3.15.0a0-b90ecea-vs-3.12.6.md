# Results vs. 3.12.6

- fork: python
- ref: b90ecea9e6b33dae360e
- machine: darwin-arm64
- commit hash: b90ecea
- commit date: 2025-06-05
- overall geometric mean: 1.115x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250605-macm4pro-arm64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 112 ms: 1.02x faster                                                    |
| docutils       | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                  |
| html5lib       | 23.0 ms                                                  | 24.1 ms: 1.05x slower                                                   |
| sphinx         | 434 ms                                                   | 406 ms: 1.07x faster                                                    |
| Geometric mean | (ref)                                                    | 1.00x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250605-macm4pro-arm64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 247 ms: 2.01x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 250 ms: 1.92x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 251 ms: 1.83x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 253 ms: 1.76x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 105 ms: 1.65x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 110 ms: 1.63x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 148 ms: 1.56x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 146 ms: 1.53x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 263 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 265 ms: 1.26x faster                                                    |
| async_generators                 | 206 ms                                                   | 170 ms: 1.21x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.19x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 41.8 ms: 1.09x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.03x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.15x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 248 ms: 1.17x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.0 ms: 2.71x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.26x faster                                                            |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250605-macm4pro-arm64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.8 ms: 1.27x faster                                                   |
| nbody          | 54.2 ms                                                  | 47.1 ms: 1.15x faster                                                   |
| pidigits       | 161 ms                                                   | 165 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.13x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250605-macm4pro-arm64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 47.4 ms: 1.15x faster                                                   |
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.15x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 97.1 ms: 1.03x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.75 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                    | 1.07x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250605-macm4pro-arm64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 43.3 ms: 1.19x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 35.2 ms: 1.10x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 61.5 ms: 1.10x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 25.0 ms: 1.07x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 97.8 us: 1.05x faster                                                   |
| tomli_loads          | 957 ms                                                   | 917 ms: 1.04x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.8 us: 1.01x faster                                                   |
| pickle_pure_python   | 139 us                                                   | 144 us: 1.03x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 4.43 ms: 1.04x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.05x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250605-macm4pro-arm64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.59 ms: 1.07x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.15 ms: 1.08x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.07x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250605-macm4pro-arm64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.82 ms: 1.07x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 21.7 ms: 1.01x faster                                                   |
| mako            | 4.77 ms                                                  | 4.83 ms: 1.01x slower                                                   |
| django_template | 13.6 ms                                                  | 15.3 ms: 1.12x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.01x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250605-macm4pro-arm64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 9.58 ms: 2.17x faster                                                   |
| mdp                              | 1.09 sec                                                 | 512 ms: 2.13x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 247 ms: 2.01x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 250 ms: 1.92x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 251 ms: 1.83x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 253 ms: 1.76x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 105 ms: 1.65x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 110 ms: 1.63x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 148 ms: 1.56x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 146 ms: 1.53x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.2 us: 1.50x faster                                                   |
| deepcopy                         | 161 us                                                   | 109 us: 1.48x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.32 us: 1.34x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 263 ms: 1.28x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.15 us: 1.27x faster                                                   |
| go                               | 70.0 ms                                                  | 55.0 ms: 1.27x faster                                                   |
| float                            | 37.9 ms                                                  | 29.8 ms: 1.27x faster                                                   |
| generators                       | 21.9 ms                                                  | 17.3 ms: 1.27x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 265 ms: 1.26x faster                                                    |
| raytrace                         | 145 ms                                                   | 118 ms: 1.23x faster                                                    |
| async_generators                 | 206 ms                                                   | 170 ms: 1.21x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 17.7 ms: 1.20x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 50.9 ms: 1.20x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.19x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 43.3 ms: 1.19x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 46.0 ms: 1.18x faster                                                   |
| k_core                           | 1.12 sec                                                 | 951 ms: 1.18x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 47.4 ms: 1.15x faster                                                   |
| nbody                            | 54.2 ms                                                  | 47.1 ms: 1.15x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 61.6 us: 1.15x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.50 ms: 1.15x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.15x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.96 sec: 1.14x faster                                                  |
| nqueens                          | 43.5 ms                                                  | 38.1 ms: 1.14x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.84 ms: 1.13x faster                                                   |
| pylint                           | 128 ms                                                   | 114 ms: 1.13x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.1 ms: 1.11x faster                                                   |
| chaos                            | 28.9 ms                                                  | 26.0 ms: 1.11x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.74 ms: 1.11x faster                                                   |
| pyflate                          | 216 ms                                                   | 195 ms: 1.11x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 35.2 ms: 1.10x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 61.5 ms: 1.10x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 129 ms: 1.10x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 41.8 ms: 1.09x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.6 ms: 1.09x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.40 ms: 1.08x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 47.7 ms: 1.08x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 25.0 ms: 1.07x faster                                                   |
| sphinx                           | 434 ms                                                   | 406 ms: 1.07x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.82 ms: 1.07x faster                                                   |
| thrift                           | 322 us                                                   | 302 us: 1.07x faster                                                    |
| sympy_str                        | 104 ms                                                   | 98.1 ms: 1.06x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 97.8 us: 1.05x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 24.3 ms: 1.05x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 917 ms: 1.04x faster                                                    |
| richards                         | 22.4 ms                                                  | 21.5 ms: 1.04x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 55.5 ms: 1.04x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.03x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.50 us: 1.03x faster                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 37.8 ms: 1.03x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 97.1 ms: 1.03x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.73 us: 1.03x faster                                                   |
| json                             | 1.93 ms                                                  | 1.90 ms: 1.02x faster                                                   |
| 2to3                             | 114 ms                                                   | 112 ms: 1.02x faster                                                    |
| pycparser                        | 497 ms                                                   | 491 ms: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 521 ms: 1.01x faster                                                    |
| json_loads                       | 10.9 us                                                  | 10.8 us: 1.01x faster                                                   |
| fannkuch                         | 176 ms                                                   | 174 ms: 1.01x faster                                                    |
| sympy_expand                     | 167 ms                                                   | 166 ms: 1.01x faster                                                    |
| shortest_path                    | 219 ms                                                   | 218 ms: 1.01x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 21.7 ms: 1.01x faster                                                   |
| connected_components             | 201 ms                                                   | 202 ms: 1.01x slower                                                    |
| mako                             | 4.77 ms                                                  | 4.83 ms: 1.01x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 48.3 ms: 1.01x slower                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.75 ms: 1.02x slower                                                   |
| docutils                         | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                  |
| pidigits                         | 161 ms                                                   | 165 ms: 1.02x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 431 us: 1.03x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 144 us: 1.03x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 4.43 ms: 1.04x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 24.1 ms: 1.05x slower                                                   |
| pprint_pformat                   | 665 ms                                                   | 710 ms: 1.07x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.59 ms: 1.07x slower                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 353 ms: 1.08x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.15 ms: 1.08x slower                                                   |
| gc_traversal                     | 2.01 ms                                                  | 2.19 ms: 1.09x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 43.8 ms: 1.10x slower                                                   |
| django_template                  | 13.6 ms                                                  | 15.3 ms: 1.12x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 935 us: 1.13x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.00 ms: 1.15x slower                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.15x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 248 ms: 1.17x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.9 ms: 1.23x slower                                                   |
| many_optionals                   | 195 us                                                   | 243 us: 1.25x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.0 ms: 2.71x slower                                                   |
| logging_silent                   | 50.9 ns                                                  | 196 ns: 3.84x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                            |

Benchmark hidden because not significant (2): sqlite_synth, asyncio_websockets
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250605-3.15.0a0-b90ecea/bm-20250605-macm4pro-arm64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.115x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.15x