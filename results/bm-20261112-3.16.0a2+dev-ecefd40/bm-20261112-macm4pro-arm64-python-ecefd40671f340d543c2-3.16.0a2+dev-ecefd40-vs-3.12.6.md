# Results vs. 3.12.6

- fork: python
- ref: ecefd40671f340d543c2
- machine: darwin-arm64
- commit hash: ecefd40
- commit date: 2026-11-12
- overall geometric mean: 1.187x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.09x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261112-macm4pro-arm64-python-ecefd40671f340d543c2-3.16.0a2+dev-ecefd40 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 115 ms: 1.01x slower                                                        |
| docutils       | 1.02 sec                                                 | 918 ms: 1.11x faster                                                        |
| html5lib       | 23.0 ms                                                  | 22.0 ms: 1.05x faster                                                       |
| sphinx         | 434 ms                                                   | 394 ms: 1.10x faster                                                        |
| Geometric mean | (ref)                                                    | 1.06x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261112-macm4pro-arm64-python-ecefd40671f340d543c2-3.16.0a2+dev-ecefd40 |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_generators                 | 206 ms                                                   | 98.6 ms: 2.09x faster                                                       |
| async_tree_eager_io              | 496 ms                                                   | 265 ms: 1.87x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 277 ms: 1.73x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 272 ms: 1.69x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 278 ms: 1.61x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 111 ms: 1.60x faster                                                        |
| async_tree_none_tg               | 172 ms                                                   | 112 ms: 1.54x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 158 ms: 1.46x faster                                                        |
| coroutines                       | 13.6 ms                                                  | 9.67 ms: 1.40x faster                                                       |
| async_tree_memoization           | 223 ms                                                   | 163 ms: 1.37x faster                                                        |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 268 ms: 1.24x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 273 ms: 1.24x faster                                                        |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.16x faster                                                        |
| async_tree_eager                 | 45.6 ms                                                  | 40.6 ms: 1.12x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                        |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 252 ms: 1.19x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 143 ms: 1.27x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 94.0 ms: 2.93x slower                                                       |
| Geometric mean                   | (ref)                                                    | 1.24x faster                                                                |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261112-macm4pro-arm64-python-ecefd40671f340d543c2-3.16.0a2+dev-ecefd40 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.4 ms: 1.38x faster                                                       |
| nbody          | 54.2 ms                                                  | 41.8 ms: 1.30x faster                                                       |
| pidigits       | 161 ms                                                   | 152 ms: 1.06x faster                                                        |
| Geometric mean | (ref)                                                    | 1.24x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261112-macm4pro-arm64-python-ecefd40671f340d543c2-3.16.0a2+dev-ecefd40 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.36 ms: 1.22x faster                                                       |
| regex_compile  | 54.6 ms                                                  | 53.9 ms: 1.01x faster                                                       |
| regex_dna      | 99.6 ms                                                  | 98.6 ms: 1.01x faster                                                       |
| regex_v8       | 9.59 ms                                                  | 9.72 ms: 1.01x slower                                                       |
| Geometric mean | (ref)                                                    | 1.05x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261112-macm4pro-arm64-python-ecefd40671f340d543c2-3.16.0a2+dev-ecefd40 |
|----------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 41.9 ms: 1.23x faster                                                       |
| json_dumps           | 4.26 ms                                                  | 3.59 ms: 1.18x faster                                                       |
| tomli_loads          | 957 ms                                                   | 822 ms: 1.16x faster                                                        |
| xml_etree_generate   | 38.9 ms                                                  | 34.2 ms: 1.14x faster                                                       |
| unpickle_pure_python | 103 us                                                   | 91.9 us: 1.12x faster                                                       |
| xml_etree_process    | 26.7 ms                                                  | 24.8 ms: 1.08x faster                                                       |
| xml_etree_parse      | 67.9 ms                                                  | 66.0 ms: 1.03x faster                                                       |
| json_loads           | 10.9 us                                                  | 10.7 us: 1.01x faster                                                       |
| Geometric mean       | (ref)                                                    | 1.10x faster                                                                |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261112-macm4pro-arm64-python-ecefd40671f340d543c2-3.16.0a2+dev-ecefd40 |
|------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.72 ms: 1.09x slower                                                       |
| python_startup_no_site | 5.71 ms                                                  | 6.71 ms: 1.18x slower                                                       |
| Geometric mean         | (ref)                                                    | 1.13x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261112-macm4pro-arm64-python-ecefd40671f340d543c2-3.16.0a2+dev-ecefd40 |
|-----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.33 ms: 1.10x faster                                                       |
| django_template | 13.6 ms                                                  | 14.7 ms: 1.08x slower                                                       |
| Geometric mean  | (ref)                                                    | 1.01x faster                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261112-macm4pro-arm64-python-ecefd40671f340d543c2-3.16.0a2+dev-ecefd40 |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.97 ms: 5.23x faster                                                       |
| pylint                           | 128 ms                                                   | 52.3 ms: 2.45x faster                                                       |
| mdp                              | 1.09 sec                                                 | 505 ms: 2.16x faster                                                        |
| async_generators                 | 206 ms                                                   | 98.6 ms: 2.09x faster                                                       |
| async_tree_eager_io              | 496 ms                                                   | 265 ms: 1.87x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 277 ms: 1.73x faster                                                        |
| deepcopy                         | 161 us                                                   | 95.5 us: 1.69x faster                                                       |
| async_tree_io                    | 459 ms                                                   | 272 ms: 1.69x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 278 ms: 1.61x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 111 ms: 1.60x faster                                                        |
| deepcopy_memo                    | 18.3 us                                                  | 11.6 us: 1.58x faster                                                       |
| typing_runtime_protocols         | 71.0 us                                                  | 45.1 us: 1.57x faster                                                       |
| async_tree_none_tg               | 172 ms                                                   | 112 ms: 1.54x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 158 ms: 1.46x faster                                                        |
| comprehensions                   | 9.84 us                                                  | 6.83 us: 1.44x faster                                                       |
| deepcopy_reduce                  | 1.46 us                                                  | 1.03 us: 1.41x faster                                                       |
| coroutines                       | 13.6 ms                                                  | 9.67 ms: 1.40x faster                                                       |
| float                            | 37.9 ms                                                  | 27.4 ms: 1.38x faster                                                       |
| async_tree_memoization           | 223 ms                                                   | 163 ms: 1.37x faster                                                        |
| go                               | 70.0 ms                                                  | 52.0 ms: 1.35x faster                                                       |
| spectral_norm                    | 54.4 ms                                                  | 41.6 ms: 1.31x faster                                                       |
| nbody                            | 54.2 ms                                                  | 41.8 ms: 1.30x faster                                                       |
| create_gc_cycles                 | 830 us                                                   | 642 us: 1.29x faster                                                        |
| raytrace                         | 145 ms                                                   | 113 ms: 1.28x faster                                                        |
| generators                       | 21.9 ms                                                  | 17.2 ms: 1.27x faster                                                       |
| nqueens                          | 43.5 ms                                                  | 34.3 ms: 1.27x faster                                                       |
| scimark_fft                      | 142 ms                                                   | 114 ms: 1.25x faster                                                        |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 268 ms: 1.24x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 273 ms: 1.24x faster                                                        |
| xml_etree_iterparse              | 51.6 ms                                                  | 41.9 ms: 1.23x faster                                                       |
| scimark_sor                      | 61.0 ms                                                  | 49.6 ms: 1.23x faster                                                       |
| scimark_monte_carlo              | 32.2 ms                                                  | 26.3 ms: 1.23x faster                                                       |
| regex_effbot                     | 1.67 ms                                                  | 1.36 ms: 1.22x faster                                                       |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.87 sec: 1.20x faster                                                      |
| deltablue                        | 1.73 ms                                                  | 1.45 ms: 1.19x faster                                                       |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.74 ms: 1.19x faster                                                       |
| logging_simple                   | 2.57 us                                                  | 2.17 us: 1.19x faster                                                       |
| json_dumps                       | 4.26 ms                                                  | 3.59 ms: 1.18x faster                                                       |
| logging_silent                   | 50.9 ns                                                  | 43.2 ns: 1.18x faster                                                       |
| pyflate                          | 216 ms                                                   | 183 ms: 1.18x faster                                                        |
| dulwich_log                      | 21.3 ms                                                  | 18.1 ms: 1.18x faster                                                       |
| chaos                            | 28.9 ms                                                  | 24.7 ms: 1.17x faster                                                       |
| tomli_loads                      | 957 ms                                                   | 822 ms: 1.16x faster                                                        |
| logging_format                   | 2.80 us                                                  | 2.42 us: 1.16x faster                                                       |
| hexiom                           | 3.04 ms                                                  | 2.62 ms: 1.16x faster                                                       |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.16x faster                                                        |
| scimark_lu                       | 51.3 ms                                                  | 44.7 ms: 1.15x faster                                                       |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.14x faster                                                       |
| xml_etree_generate               | 38.9 ms                                                  | 34.2 ms: 1.14x faster                                                       |
| k_core                           | 1.12 sec                                                 | 993 ms: 1.13x faster                                                        |
| async_tree_eager                 | 45.6 ms                                                  | 40.6 ms: 1.12x faster                                                       |
| unpickle_pure_python             | 103 us                                                   | 91.9 us: 1.12x faster                                                       |
| docutils                         | 1.02 sec                                                 | 918 ms: 1.11x faster                                                        |
| gc_traversal                     | 2.01 ms                                                  | 1.81 ms: 1.11x faster                                                       |
| richards                         | 22.4 ms                                                  | 20.2 ms: 1.11x faster                                                       |
| richards_super                   | 25.4 ms                                                  | 23.0 ms: 1.10x faster                                                       |
| mako                             | 4.77 ms                                                  | 4.33 ms: 1.10x faster                                                       |
| sphinx                           | 434 ms                                                   | 394 ms: 1.10x faster                                                        |
| fannkuch                         | 176 ms                                                   | 160 ms: 1.09x faster                                                        |
| sympy_integrate                  | 8.02 ms                                                  | 7.38 ms: 1.09x faster                                                       |
| xml_etree_process                | 26.7 ms                                                  | 24.8 ms: 1.08x faster                                                       |
| thrift                           | 322 us                                                   | 302 us: 1.06x faster                                                        |
| crypto_pyaes                     | 38.8 ms                                                  | 36.7 ms: 1.06x faster                                                       |
| sqlite_synth                     | 967 ns                                                   | 913 ns: 1.06x faster                                                        |
| pidigits                         | 161 ms                                                   | 152 ms: 1.06x faster                                                        |
| sympy_str                        | 104 ms                                                   | 99.1 ms: 1.05x faster                                                       |
| html5lib                         | 23.0 ms                                                  | 22.0 ms: 1.05x faster                                                       |
| pprint_safe_repr                 | 328 ms                                                   | 314 ms: 1.04x faster                                                        |
| pycparser                        | 497 ms                                                   | 477 ms: 1.04x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                        |
| sympy_sum                        | 57.6 ms                                                  | 55.4 ms: 1.04x faster                                                       |
| xml_etree_parse                  | 67.9 ms                                                  | 66.0 ms: 1.03x faster                                                       |
| json                             | 1.93 ms                                                  | 1.88 ms: 1.03x faster                                                       |
| bench_thread_pool                | 419 us                                                   | 407 us: 1.03x faster                                                        |
| pprint_pformat                   | 665 ms                                                   | 648 ms: 1.03x faster                                                        |
| json_loads                       | 10.9 us                                                  | 10.7 us: 1.01x faster                                                       |
| regex_compile                    | 54.6 ms                                                  | 53.9 ms: 1.01x faster                                                       |
| regex_dna                        | 99.6 ms                                                  | 98.6 ms: 1.01x faster                                                       |
| 2to3                             | 114 ms                                                   | 115 ms: 1.01x slower                                                        |
| sympy_expand                     | 167 ms                                                   | 168 ms: 1.01x slower                                                        |
| regex_v8                         | 9.59 ms                                                  | 9.72 ms: 1.01x slower                                                       |
| shortest_path                    | 219 ms                                                   | 225 ms: 1.03x slower                                                        |
| meteor_contest                   | 47.7 ms                                                  | 49.6 ms: 1.04x slower                                                       |
| connected_components             | 201 ms                                                   | 210 ms: 1.04x slower                                                        |
| bench_mp_pool                    | 39.7 ms                                                  | 42.8 ms: 1.08x slower                                                       |
| django_template                  | 13.6 ms                                                  | 14.7 ms: 1.08x slower                                                       |
| telco                            | 2.61 ms                                                  | 2.83 ms: 1.08x slower                                                       |
| python_startup                   | 8.01 ms                                                  | 8.72 ms: 1.09x slower                                                       |
| python_startup_no_site           | 5.71 ms                                                  | 6.71 ms: 1.18x slower                                                       |
| many_optionals                   | 195 us                                                   | 231 us: 1.18x slower                                                        |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 252 ms: 1.19x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 143 ms: 1.27x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 94.0 ms: 2.93x slower                                                       |
| Geometric mean                   | (ref)                                                    | 1.18x faster                                                                |

Benchmark hidden because not significant (2): pickle_pure_python, asyncio_websockets
Ignored benchmarks (14) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261112-3.16.0a2+dev-ecefd40/bm-20261112-macm4pro-arm64-python-ecefd40671f340d543c2-3.16.0a2+dev-ecefd40.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.187x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.11x
- 95% likely to have a speedup of 1.10x
- 99% likely to have a speedup of 1.09x

# Memory
- memory change: 1.15x