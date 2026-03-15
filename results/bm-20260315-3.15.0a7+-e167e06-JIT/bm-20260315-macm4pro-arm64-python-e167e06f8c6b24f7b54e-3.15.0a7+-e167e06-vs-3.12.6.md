# Results vs. 3.12.6

- fork: python
- ref: e167e06f8c6b24f7b54e
- machine: darwin-arm64
- commit hash: e167e06
- commit date: 2026-03-15
- overall geometric mean: 1.260x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.12x faster
- Memory change: 1.26x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260315-macm4pro-arm64-python-e167e06f8c6b24f7b54e-3.15.0a7+-e167e06 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 114 ms: 1.00x slower                                                     |
| docutils       | 1.02 sec                                                 | 990 ms: 1.03x faster                                                     |
| html5lib       | 23.0 ms                                                  | 20.2 ms: 1.14x faster                                                    |
| sphinx         | 434 ms                                                   | 391 ms: 1.11x faster                                                     |
| Geometric mean | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260315-macm4pro-arm64-python-e167e06f8c6b24f7b54e-3.15.0a7+-e167e06 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 218 ms: 2.27x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 219 ms: 2.19x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 222 ms: 2.07x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 215 ms: 2.07x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 93.9 ms: 1.90x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 95.6 ms: 1.80x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 133 ms: 1.73x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 131 ms: 1.70x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 248 ms: 1.37x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 246 ms: 1.36x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 103 ms: 1.28x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 36.5 ms: 1.25x faster                                                    |
| async_generators                 | 206 ms                                                   | 185 ms: 1.11x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 216 ms: 1.07x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 120 ms: 1.06x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 240 ms: 1.13x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 80.6 ms: 2.51x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.36x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260315-macm4pro-arm64-python-e167e06f8c6b24f7b54e-3.15.0a7+-e167e06 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 23.6 ms: 1.60x faster                                                    |
| nbody          | 54.2 ms                                                  | 40.2 ms: 1.35x faster                                                    |
| pidigits       | 161 ms                                                   | 164 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                    | 1.29x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260315-macm4pro-arm64-python-e167e06f8c6b24f7b54e-3.15.0a7+-e167e06 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 40.5 ms: 1.35x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.51 ms: 1.10x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 97.5 ms: 1.02x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.92 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                    | 1.10x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260315-macm4pro-arm64-python-e167e06f8c6b24f7b54e-3.15.0a7+-e167e06 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 957 ms                                                   | 636 ms: 1.50x faster                                                     |
| xml_etree_iterparse  | 51.6 ms                                                  | 38.6 ms: 1.34x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 31.3 ms: 1.24x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 22.1 ms: 1.21x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 85.4 us: 1.20x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.57 ms: 1.19x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 127 us: 1.10x faster                                                     |
| xml_etree_parse      | 67.9 ms                                                  | 63.8 ms: 1.06x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.7 us: 1.02x faster                                                    |
| Geometric mean       | (ref)                                                    | 1.20x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260315-macm4pro-arm64-python-e167e06f8c6b24f7b54e-3.15.0a7+-e167e06 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.77 ms: 1.09x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.32 ms: 1.11x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.10x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260315-macm4pro-arm64-python-e167e06f8c6b24f7b54e-3.15.0a7+-e167e06 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.03 ms: 1.19x faster                                                    |
| django_template | 13.6 ms                                                  | 13.7 ms: 1.01x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.09x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260315-macm4pro-arm64-python-e167e06f8c6b24f7b54e-3.15.0a7+-e167e06 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.56 ms: 5.83x faster                                                    |
| richards                         | 22.4 ms                                                  | 9.46 ms: 2.37x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 218 ms: 2.27x faster                                                     |
| richards_super                   | 25.4 ms                                                  | 11.2 ms: 2.27x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 219 ms: 2.19x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 222 ms: 2.07x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 215 ms: 2.07x faster                                                     |
| mdp                              | 1.09 sec                                                 | 536 ms: 2.04x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 93.9 ms: 1.90x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 10.00 us: 1.83x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 95.6 ms: 1.80x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 28.5 ms: 1.80x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 133 ms: 1.73x faster                                                     |
| deepcopy                         | 161 us                                                   | 94.9 us: 1.70x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 131 ms: 1.70x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 5.87 us: 1.68x faster                                                    |
| float                            | 37.9 ms                                                  | 23.6 ms: 1.60x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 38.5 ms: 1.58x faster                                                    |
| go                               | 70.0 ms                                                  | 46.4 ms: 1.51x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 636 ms: 1.50x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.17 ms: 1.47x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 998 ns: 1.46x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 97.3 ms: 1.46x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 35.0 ns: 1.45x faster                                                    |
| pyflate                          | 216 ms                                                   | 151 ms: 1.43x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 37.9 ms: 1.43x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 23.3 ms: 1.38x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 248 ms: 1.37x faster                                                     |
| nqueens                          | 43.5 ms                                                  | 32.0 ms: 1.36x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 246 ms: 1.36x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 40.5 ms: 1.35x faster                                                    |
| nbody                            | 54.2 ms                                                  | 40.2 ms: 1.35x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.6 ms: 1.34x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 509 ms: 1.31x faster                                                     |
| chaos                            | 28.9 ms                                                  | 22.2 ms: 1.30x faster                                                    |
| raytrace                         | 145 ms                                                   | 111 ms: 1.30x faster                                                     |
| k_core                           | 1.12 sec                                                 | 858 ms: 1.30x faster                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 253 ms: 1.30x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 103 ms: 1.28x faster                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.78 sec: 1.26x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 36.5 ms: 1.25x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.44 ms: 1.24x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 31.3 ms: 1.24x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 31.9 ms: 1.22x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 22.1 ms: 1.21x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.13 us: 1.21x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 85.4 us: 1.20x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.34 us: 1.20x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.57 ms: 1.19x faster                                                    |
| mako                             | 4.77 ms                                                  | 4.03 ms: 1.19x faster                                                    |
| fannkuch                         | 176 ms                                                   | 149 ms: 1.18x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 10.6 ms: 1.16x faster                                                    |
| generators                       | 21.9 ms                                                  | 19.0 ms: 1.16x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.5 ms: 1.15x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 20.2 ms: 1.14x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.85 ms: 1.12x faster                                                    |
| async_generators                 | 206 ms                                                   | 185 ms: 1.11x faster                                                     |
| typing_runtime_protocols         | 71.0 us                                                  | 63.7 us: 1.11x faster                                                    |
| sphinx                           | 434 ms                                                   | 391 ms: 1.11x faster                                                     |
| pycparser                        | 497 ms                                                   | 450 ms: 1.11x faster                                                     |
| pylint                           | 128 ms                                                   | 116 ms: 1.10x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.51 ms: 1.10x faster                                                    |
| pickle_pure_python               | 139 us                                                   | 127 us: 1.10x faster                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 7.44 ms: 1.08x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 216 ms: 1.07x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 63.8 ms: 1.06x faster                                                    |
| json                             | 1.93 ms                                                  | 1.84 ms: 1.05x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 54.8 ms: 1.05x faster                                                    |
| meteor_contest                   | 47.7 ms                                                  | 45.9 ms: 1.04x faster                                                    |
| sympy_str                        | 104 ms                                                   | 100 ms: 1.04x faster                                                     |
| thrift                           | 322 us                                                   | 310 us: 1.04x faster                                                     |
| docutils                         | 1.02 sec                                                 | 990 ms: 1.03x faster                                                     |
| sqlite_synth                     | 967 ns                                                   | 944 ns: 1.02x faster                                                     |
| connected_components             | 201 ms                                                   | 196 ms: 1.02x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 97.5 ms: 1.02x faster                                                    |
| json_loads                       | 10.9 us                                                  | 10.7 us: 1.02x faster                                                    |
| shortest_path                    | 219 ms                                                   | 215 ms: 1.02x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                     |
| 2to3                             | 114 ms                                                   | 114 ms: 1.00x slower                                                     |
| django_template                  | 13.6 ms                                                  | 13.7 ms: 1.01x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 169 ms: 1.01x slower                                                     |
| pidigits                         | 161 ms                                                   | 164 ms: 1.01x slower                                                     |
| gc_traversal                     | 2.01 ms                                                  | 2.05 ms: 1.02x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 429 us: 1.03x slower                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.92 ms: 1.03x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 120 ms: 1.06x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 8.77 ms: 1.09x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 910 us: 1.10x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 6.32 ms: 1.11x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 240 ms: 1.13x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 45.0 ms: 1.13x slower                                                    |
| many_optionals                   | 195 us                                                   | 237 us: 1.21x slower                                                     |
| coverage                         | 26.9 ms                                                  | 33.3 ms: 1.24x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 80.6 ms: 2.51x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.25x faster                                                             |

Benchmark hidden because not significant (1): telco
Ignored benchmarks (12) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260315-3.15.0a7+-e167e06-JIT/bm-20260315-macm4pro-arm64-python-e167e06f8c6b24f7b54e-3.15.0a7+-e167e06.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.260x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.17x
- 95% likely to have a speedup of 1.15x
- 99% likely to have a speedup of 1.12x

# Memory
- memory change: 1.26x