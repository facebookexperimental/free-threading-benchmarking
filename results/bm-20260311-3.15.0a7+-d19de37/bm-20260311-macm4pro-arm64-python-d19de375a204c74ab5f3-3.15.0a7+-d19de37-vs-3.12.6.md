# Results vs. 3.12.6

- fork: python
- ref: d19de375a204c74ab5f3
- machine: darwin-arm64
- commit hash: d19de37
- commit date: 2026-03-11
- overall geometric mean: 1.169x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7+-d19de37 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| docutils       | 1.02 sec                                                 | 994 ms: 1.03x faster                                                     |
| html5lib       | 23.0 ms                                                  | 21.0 ms: 1.09x faster                                                    |
| sphinx         | 434 ms                                                   | 390 ms: 1.11x faster                                                     |
| Geometric mean | (ref)                                                    | 1.06x faster                                                             |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7+-d19de37 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 223 ms: 2.23x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 224 ms: 2.15x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 219 ms: 2.03x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 233 ms: 1.97x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 99.8 ms: 1.79x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 98.5 ms: 1.75x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 135 ms: 1.71x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 137 ms: 1.63x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 249 ms: 1.36x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.0 ms: 1.35x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 251 ms: 1.33x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 106 ms: 1.24x faster                                                     |
| async_generators                 | 206 ms                                                   | 176 ms: 1.17x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 40.2 ms: 1.13x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 219 ms: 1.05x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 119 ms: 1.06x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 238 ms: 1.12x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 81.3 ms: 2.53x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.33x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7+-d19de37 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 26.8 ms: 1.42x faster                                                    |
| nbody          | 54.2 ms                                                  | 44.8 ms: 1.21x faster                                                    |
| pidigits       | 161 ms                                                   | 162 ms: 1.00x slower                                                     |
| Geometric mean | (ref)                                                    | 1.20x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7+-d19de37 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 45.8 ms: 1.19x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.52 ms: 1.09x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 97.0 ms: 1.03x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.91 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7+-d19de37 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.7 ms: 1.30x faster                                                    |
| tomli_loads          | 957 ms                                                   | 816 ms: 1.17x faster                                                     |
| json_dumps           | 4.26 ms                                                  | 3.76 ms: 1.13x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 34.8 ms: 1.12x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 62.1 ms: 1.09x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 24.7 ms: 1.08x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 97.5 us: 1.06x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.8 us: 1.01x faster                                                    |
| Geometric mean       | (ref)                                                    | 1.10x faster                                                             |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7+-d19de37 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.83 ms: 1.10x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.38 ms: 1.12x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.11x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7+-d19de37 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.78 ms: 1.07x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 21.0 ms: 1.04x faster                                                    |
| django_template | 13.6 ms                                                  | 14.5 ms: 1.07x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.01x faster                                                             |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7+-d19de37 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.98 ms: 5.22x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 223 ms: 2.23x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 224 ms: 2.15x faster                                                     |
| mdp                              | 1.09 sec                                                 | 532 ms: 2.05x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 219 ms: 2.03x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 233 ms: 1.97x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 99.8 ms: 1.79x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 98.5 ms: 1.75x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 135 ms: 1.71x faster                                                     |
| deepcopy                         | 161 us                                                   | 97.7 us: 1.65x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 137 ms: 1.63x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 11.7 us: 1.57x faster                                                    |
| float                            | 37.9 ms                                                  | 26.8 ms: 1.42x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.07 us: 1.39x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.06 us: 1.37x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 249 ms: 1.36x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.0 ms: 1.35x faster                                                    |
| go                               | 70.0 ms                                                  | 52.5 ms: 1.33x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 251 ms: 1.33x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.7 ms: 1.30x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 42.2 ms: 1.29x faster                                                    |
| raytrace                         | 145 ms                                                   | 113 ms: 1.29x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 40.2 ns: 1.27x faster                                                    |
| k_core                           | 1.12 sec                                                 | 897 ms: 1.25x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 106 ms: 1.24x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 49.9 ms: 1.22x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 35.6 ms: 1.22x faster                                                    |
| nbody                            | 54.2 ms                                                  | 44.8 ms: 1.21x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.13 us: 1.20x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.34 us: 1.20x faster                                                    |
| chaos                            | 28.9 ms                                                  | 24.2 ms: 1.19x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 45.8 ms: 1.19x faster                                                    |
| pyflate                          | 216 ms                                                   | 182 ms: 1.19x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.45 ms: 1.19x faster                                                    |
| async_generators                 | 206 ms                                                   | 176 ms: 1.17x faster                                                     |
| tomli_loads                      | 957 ms                                                   | 816 ms: 1.17x faster                                                     |
| generators                       | 21.9 ms                                                  | 18.7 ms: 1.17x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.92 sec: 1.17x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 122 ms: 1.16x faster                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 27.8 ms: 1.16x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.7 ms: 1.15x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 44.5 ms: 1.15x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.6 ms: 1.14x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.83 ms: 1.14x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 22.4 ms: 1.14x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 40.2 ms: 1.13x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.76 ms: 1.13x faster                                                    |
| richards                         | 22.4 ms                                                  | 19.8 ms: 1.13x faster                                                    |
| pylint                           | 128 ms                                                   | 114 ms: 1.12x faster                                                     |
| typing_runtime_protocols         | 71.0 us                                                  | 63.2 us: 1.12x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.72 ms: 1.12x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 34.8 ms: 1.12x faster                                                    |
| sphinx                           | 434 ms                                                   | 390 ms: 1.11x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 21.0 ms: 1.09x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.52 ms: 1.09x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 62.1 ms: 1.09x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.38 ms: 1.09x faster                                                    |
| pycparser                        | 497 ms                                                   | 460 ms: 1.08x faster                                                     |
| xml_etree_process                | 26.7 ms                                                  | 24.7 ms: 1.08x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.78 ms: 1.07x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 97.5 us: 1.06x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 630 ms: 1.06x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 219 ms: 1.05x faster                                                     |
| thrift                           | 322 us                                                   | 306 us: 1.05x faster                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 312 ms: 1.05x faster                                                     |
| fannkuch                         | 176 ms                                                   | 167 ms: 1.05x faster                                                     |
| sympy_str                        | 104 ms                                                   | 99.9 ms: 1.04x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 55.4 ms: 1.04x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 21.0 ms: 1.04x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 37.6 ms: 1.03x faster                                                    |
| docutils                         | 1.02 sec                                                 | 994 ms: 1.03x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 97.0 ms: 1.03x faster                                                    |
| json                             | 1.93 ms                                                  | 1.88 ms: 1.03x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 943 ns: 1.02x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                     |
| json_loads                       | 10.9 us                                                  | 10.8 us: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                     |
| pidigits                         | 161 ms                                                   | 162 ms: 1.00x slower                                                     |
| gc_traversal                     | 2.01 ms                                                  | 2.03 ms: 1.01x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 169 ms: 1.01x slower                                                     |
| shortest_path                    | 219 ms                                                   | 224 ms: 1.02x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 428 us: 1.02x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 48.9 ms: 1.03x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.91 ms: 1.03x slower                                                    |
| connected_components             | 201 ms                                                   | 208 ms: 1.04x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 119 ms: 1.06x slower                                                     |
| django_template                  | 13.6 ms                                                  | 14.5 ms: 1.07x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.82 ms: 1.08x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 898 us: 1.08x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 8.83 ms: 1.10x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.38 ms: 1.12x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 238 ms: 1.12x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 45.3 ms: 1.14x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.3 ms: 1.20x slower                                                    |
| many_optionals                   | 195 us                                                   | 251 us: 1.28x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 81.3 ms: 2.53x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.17x faster                                                             |

Benchmark hidden because not significant (3): mako, pickle_pure_python, 2to3
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260311-3.15.0a7+-d19de37/bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7+-d19de37.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.169x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.23x