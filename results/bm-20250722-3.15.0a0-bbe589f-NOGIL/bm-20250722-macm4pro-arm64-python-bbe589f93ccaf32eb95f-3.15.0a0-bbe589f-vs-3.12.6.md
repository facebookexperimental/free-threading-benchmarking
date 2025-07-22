# Results vs. 3.12.6

- fork: python
- ref: bbe589f93ccaf32eb95f
- machine: darwin-arm64
- commit hash: bbe589f
- commit date: 2025-07-22
- overall geometric mean: 1.082x faster
- HPT reliability: 94.92%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.25x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250722-macm4pro-arm64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 124 ms: 1.09x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                  |
| html5lib       | 23.0 ms                                                  | 23.8 ms: 1.03x slower                                                   |
| sphinx         | 434 ms                                                   | 417 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                    | 1.02x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250722-macm4pro-arm64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 206 ms: 2.41x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 199 ms: 2.41x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 198 ms: 2.25x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 210 ms: 2.19x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 86.5 ms: 1.99x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.86x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.77x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.71x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 236 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 243 ms: 1.37x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 11.3 ms: 1.20x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.20x faster                                                    |
| async_generators                 | 206 ms                                                   | 186 ms: 1.11x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 48.4 ms: 1.06x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 227 ms: 1.07x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.1 ms: 2.43x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.37x faster                                                            |

Benchmark hidden because not significant (1): async_tree_eager_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250722-macm4pro-arm64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.3 ms: 1.34x faster                                                   |
| pidigits       | 161 ms                                                   | 165 ms: 1.02x slower                                                    |
| nbody          | 54.2 ms                                                  | 58.3 ms: 1.08x slower                                                   |
| Geometric mean | (ref)                                                    | 1.07x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250722-macm4pro-arm64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.48 ms: 1.13x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 52.5 ms: 1.04x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 96.6 ms: 1.03x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.35 ms: 1.03x faster                                                   |
| Geometric mean | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250722-macm4pro-arm64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.7 ms: 1.33x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 58.4 ms: 1.16x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 36.9 ms: 1.05x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 26.7 ms: 1.00x faster                                                   |
| tomli_loads          | 957 ms                                                   | 975 ms: 1.02x slower                                                    |
| unpickle_pure_python | 103 us                                                   | 110 us: 1.07x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 4.57 ms: 1.07x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 150 us: 1.08x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.7 us: 1.08x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.02x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250722-macm4pro-arm64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.69 ms: 1.21x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 7.03 ms: 1.23x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.22x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250722-macm4pro-arm64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 23.7 ms: 1.09x slower                                                   |
| genshi_text     | 10.5 ms                                                  | 11.4 ms: 1.09x slower                                                   |
| mako            | 4.77 ms                                                  | 5.71 ms: 1.20x slower                                                   |
| django_template | 13.6 ms                                                  | 16.5 ms: 1.21x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.15x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250722-macm4pro-arm64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 778 us: 2.58x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 206 ms: 2.41x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 199 ms: 2.41x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 198 ms: 2.25x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 210 ms: 2.19x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 86.5 ms: 1.99x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.86x faster                                                    |
| mdp                              | 1.09 sec                                                 | 601 ms: 1.82x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.77x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.71x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 487 us: 1.70x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 236 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 243 ms: 1.37x faster                                                    |
| deepcopy                         | 161 us                                                   | 118 us: 1.37x faster                                                    |
| float                            | 37.9 ms                                                  | 28.3 ms: 1.34x faster                                                   |
| deepcopy_memo                    | 18.3 us                                                  | 13.7 us: 1.33x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.7 ms: 1.33x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 11.3 ms: 1.20x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.20x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.25 us: 1.19x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 821 ns: 1.18x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.25 us: 1.17x faster                                                   |
| go                               | 70.0 ms                                                  | 60.2 ms: 1.16x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 58.4 ms: 1.16x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 44.7 ns: 1.14x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.98 sec: 1.13x faster                                                  |
| generators                       | 21.9 ms                                                  | 19.4 ms: 1.13x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.48 ms: 1.13x faster                                                   |
| k_core                           | 1.12 sec                                                 | 997 ms: 1.12x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 19.0 ms: 1.12x faster                                                   |
| subparsers                       | 20.8 ms                                                  | 18.5 ms: 1.12x faster                                                   |
| raytrace                         | 145 ms                                                   | 130 ms: 1.11x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.1 ms: 1.11x faster                                                   |
| async_generators                 | 206 ms                                                   | 186 ms: 1.11x faster                                                    |
| pyflate                          | 216 ms                                                   | 196 ms: 1.10x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 55.8 ms: 1.09x faster                                                   |
| pylint                           | 128 ms                                                   | 119 ms: 1.08x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 51.1 ms: 1.06x faster                                                   |
| pycparser                        | 497 ms                                                   | 470 ms: 1.06x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.63 ms: 1.06x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 36.9 ms: 1.05x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 52.5 ms: 1.04x faster                                                   |
| sphinx                           | 434 ms                                                   | 417 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.03x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 96.6 ms: 1.03x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.35 ms: 1.03x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 42.8 ms: 1.02x faster                                                   |
| docutils                         | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                  |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.55 us: 1.01x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 26.7 ms: 1.00x faster                                                   |
| chaos                            | 28.9 ms                                                  | 29.1 ms: 1.01x slower                                                   |
| dask                             | 528 ms                                                   | 531 ms: 1.01x slower                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.08 ms: 1.01x slower                                                   |
| scimark_fft                      | 142 ms                                                   | 143 ms: 1.01x slower                                                    |
| logging_format                   | 2.80 us                                                  | 2.83 us: 1.01x slower                                                   |
| fannkuch                         | 176 ms                                                   | 179 ms: 1.02x slower                                                    |
| tomli_loads                      | 957 ms                                                   | 975 ms: 1.02x slower                                                    |
| pidigits                         | 161 ms                                                   | 165 ms: 1.02x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.12 ms: 1.03x slower                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 73.1 us: 1.03x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 23.8 ms: 1.03x slower                                                   |
| thrift                           | 322 us                                                   | 333 us: 1.03x slower                                                    |
| json                             | 1.93 ms                                                  | 2.03 ms: 1.05x slower                                                   |
| richards                         | 22.4 ms                                                  | 23.6 ms: 1.05x slower                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.9 ms: 1.05x slower                                                   |
| shortest_path                    | 219 ms                                                   | 233 ms: 1.06x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 61.2 ms: 1.06x slower                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 48.4 ms: 1.06x slower                                                   |
| richards_super                   | 25.4 ms                                                  | 27.0 ms: 1.06x slower                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 349 ms: 1.06x slower                                                    |
| sympy_str                        | 104 ms                                                   | 111 ms: 1.06x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 227 ms: 1.07x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 712 ms: 1.07x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 110 us: 1.07x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 4.57 ms: 1.07x slower                                                   |
| nbody                            | 54.2 ms                                                  | 58.3 ms: 1.08x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 150 us: 1.08x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.7 us: 1.08x slower                                                   |
| genshi_xml                       | 21.8 ms                                                  | 23.7 ms: 1.09x slower                                                   |
| 2to3                             | 114 ms                                                   | 124 ms: 1.09x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.4 ms: 1.09x slower                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 42.9 ms: 1.10x slower                                                   |
| connected_components             | 201 ms                                                   | 222 ms: 1.10x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 57.9 ms: 1.13x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 189 ms: 1.13x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.35 ms: 1.13x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 46.0 ms: 1.16x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 56.3 ms: 1.18x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.71 ms: 1.20x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.69 ms: 1.21x slower                                                   |
| django_template                  | 13.6 ms                                                  | 16.5 ms: 1.21x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.21 ms: 1.23x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 7.03 ms: 1.23x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 598 us: 1.43x slower                                                    |
| coverage                         | 26.9 ms                                                  | 39.9 ms: 1.48x slower                                                   |
| many_optionals                   | 195 us                                                   | 338 us: 1.73x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.1 ms: 2.43x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                            |

Benchmark hidden because not significant (1): async_tree_eager_memoization_tg
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250722-3.15.0a0-bbe589f-NOGIL/bm-20250722-macm4pro-arm64-python-bbe589f93ccaf32eb95f-3.15.0a0-bbe589f.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.082x faster

# HPT report

- Reliability score: 94.92% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.25x