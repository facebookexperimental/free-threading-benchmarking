# Results vs. 3.12.6

- fork: python
- ref: b8e925b4f8f6c5e28fbe
- machine: darwin-arm64
- commit hash: b8e925b
- commit date: 2026-01-14
- overall geometric mean: 1.155x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260114-macm4pro-arm64-python-b8e925b4f8f6c5e28fbe-3.15.0a5+-b8e925b |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 115 ms: 1.01x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                   |
| html5lib       | 23.0 ms                                                  | 21.7 ms: 1.06x faster                                                    |
| sphinx         | 434 ms                                                   | 394 ms: 1.10x faster                                                     |
| Geometric mean | (ref)                                                    | 1.03x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260114-macm4pro-arm64-python-b8e925b4f8f6c5e28fbe-3.15.0a5+-b8e925b |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 225 ms: 2.20x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 227 ms: 2.12x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 223 ms: 2.00x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 236 ms: 1.94x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 103 ms: 1.73x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 101 ms: 1.70x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 137 ms: 1.68x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 140 ms: 1.59x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.35x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 256 ms: 1.32x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 253 ms: 1.32x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.22x faster                                                     |
| async_generators                 | 206 ms                                                   | 175 ms: 1.18x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 40.5 ms: 1.12x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 121 ms: 1.07x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 242 ms: 1.14x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 80.1 ms: 2.49x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.32x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260114-macm4pro-arm64-python-b8e925b4f8f6c5e28fbe-3.15.0a5+-b8e925b |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.1 ms: 1.40x faster                                                    |
| nbody          | 54.2 ms                                                  | 44.8 ms: 1.21x faster                                                    |
| pidigits       | 161 ms                                                   | 167 ms: 1.04x slower                                                     |
| Geometric mean | (ref)                                                    | 1.18x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260114-macm4pro-arm64-python-b8e925b4f8f6c5e28fbe-3.15.0a5+-b8e925b |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 46.2 ms: 1.18x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 96.9 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260114-macm4pro-arm64-python-b8e925b4f8f6c5e28fbe-3.15.0a5+-b8e925b |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.3 ms: 1.28x faster                                                    |
| tomli_loads          | 957 ms                                                   | 838 ms: 1.14x faster                                                     |
| xml_etree_generate   | 38.9 ms                                                  | 34.3 ms: 1.13x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.85 ms: 1.11x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 24.4 ms: 1.10x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 62.1 ms: 1.09x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 99.3 us: 1.04x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 141 us: 1.01x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.09x faster                                                             |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260114-macm4pro-arm64-python-b8e925b4f8f6c5e28fbe-3.15.0a5+-b8e925b |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.95 ms: 1.12x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.44 ms: 1.13x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.12x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260114-macm4pro-arm64-python-b8e925b4f8f6c5e28fbe-3.15.0a5+-b8e925b |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.67 ms: 1.08x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 21.1 ms: 1.03x faster                                                    |
| mako            | 4.77 ms                                                  | 4.80 ms: 1.01x slower                                                    |
| django_template | 13.6 ms                                                  | 14.7 ms: 1.08x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.01x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260114-macm4pro-arm64-python-b8e925b4f8f6c5e28fbe-3.15.0a5+-b8e925b |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.10 ms: 5.06x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 225 ms: 2.20x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 227 ms: 2.12x faster                                                     |
| mdp                              | 1.09 sec                                                 | 545 ms: 2.00x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 223 ms: 2.00x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 236 ms: 1.94x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 103 ms: 1.73x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 101 ms: 1.70x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 137 ms: 1.68x faster                                                     |
| deepcopy                         | 161 us                                                   | 99.8 us: 1.62x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 140 ms: 1.59x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 11.7 us: 1.56x faster                                                    |
| float                            | 37.9 ms                                                  | 27.1 ms: 1.40x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.10 us: 1.39x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.07 us: 1.36x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.35x faster                                                    |
| go                               | 70.0 ms                                                  | 53.0 ms: 1.32x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 256 ms: 1.32x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 253 ms: 1.32x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.3 ms: 1.28x faster                                                    |
| raytrace                         | 145 ms                                                   | 113 ms: 1.28x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 43.1 ms: 1.26x faster                                                    |
| k_core                           | 1.12 sec                                                 | 900 ms: 1.24x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 41.2 ns: 1.24x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.22x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 50.2 ms: 1.22x faster                                                    |
| nbody                            | 54.2 ms                                                  | 44.8 ms: 1.21x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.5 ms: 1.18x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 46.2 ms: 1.18x faster                                                    |
| async_generators                 | 206 ms                                                   | 175 ms: 1.18x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 120 ms: 1.18x faster                                                     |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.78 ms: 1.17x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 27.7 ms: 1.16x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.21 us: 1.16x faster                                                    |
| chaos                            | 28.9 ms                                                  | 24.9 ms: 1.16x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.49 ms: 1.16x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.42 us: 1.16x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 44.4 ms: 1.16x faster                                                    |
| pyflate                          | 216 ms                                                   | 188 ms: 1.15x faster                                                     |
| tomli_loads                      | 957 ms                                                   | 838 ms: 1.14x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.14x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 62.3 us: 1.14x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 34.3 ms: 1.13x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 38.4 ms: 1.13x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.98 sec: 1.13x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 40.5 ms: 1.12x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 19.0 ms: 1.12x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 22.7 ms: 1.12x faster                                                    |
| richards                         | 22.4 ms                                                  | 20.1 ms: 1.12x faster                                                    |
| pylint                           | 128 ms                                                   | 115 ms: 1.11x faster                                                     |
| json_dumps                       | 4.26 ms                                                  | 3.85 ms: 1.11x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.75 ms: 1.10x faster                                                    |
| sphinx                           | 434 ms                                                   | 394 ms: 1.10x faster                                                     |
| xml_etree_process                | 26.7 ms                                                  | 24.4 ms: 1.10x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 62.1 ms: 1.09x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.67 ms: 1.08x faster                                                    |
| pycparser                        | 497 ms                                                   | 465 ms: 1.07x faster                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 7.53 ms: 1.06x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 626 ms: 1.06x faster                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 310 ms: 1.06x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 21.7 ms: 1.06x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 36.7 ms: 1.06x faster                                                    |
| thrift                           | 322 us                                                   | 305 us: 1.06x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                     |
| sympy_str                        | 104 ms                                                   | 100 ms: 1.04x faster                                                     |
| unpickle_pure_python             | 103 us                                                   | 99.3 us: 1.04x faster                                                    |
| fannkuch                         | 176 ms                                                   | 169 ms: 1.04x faster                                                     |
| sympy_sum                        | 57.6 ms                                                  | 55.9 ms: 1.03x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 21.1 ms: 1.03x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 96.9 ms: 1.03x faster                                                    |
| json                             | 1.93 ms                                                  | 1.90 ms: 1.02x faster                                                    |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| mako                             | 4.77 ms                                                  | 4.80 ms: 1.01x slower                                                    |
| 2to3                             | 114 ms                                                   | 115 ms: 1.01x slower                                                     |
| pickle_pure_python               | 139 us                                                   | 141 us: 1.01x slower                                                     |
| docutils                         | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 169 ms: 1.01x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 431 us: 1.03x slower                                                     |
| shortest_path                    | 219 ms                                                   | 227 ms: 1.04x slower                                                     |
| pidigits                         | 161 ms                                                   | 167 ms: 1.04x slower                                                     |
| connected_components             | 201 ms                                                   | 209 ms: 1.04x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 50.5 ms: 1.06x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.13 ms: 1.06x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 121 ms: 1.07x slower                                                     |
| django_template                  | 13.6 ms                                                  | 14.7 ms: 1.08x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.85 ms: 1.09x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.95 ms: 1.12x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.44 ms: 1.13x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 242 ms: 1.14x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 46.1 ms: 1.16x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 964 us: 1.16x slower                                                     |
| coverage                         | 26.9 ms                                                  | 32.1 ms: 1.19x slower                                                    |
| many_optionals                   | 195 us                                                   | 260 us: 1.33x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 80.1 ms: 2.49x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.15x faster                                                             |

Benchmark hidden because not significant (3): sqlite_synth, json_loads, regex_v8
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260114-3.15.0a5+-b8e925b/bm-20260114-macm4pro-arm64-python-b8e925b4f8f6c5e28fbe-3.15.0a5+-b8e925b.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.155x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.23x