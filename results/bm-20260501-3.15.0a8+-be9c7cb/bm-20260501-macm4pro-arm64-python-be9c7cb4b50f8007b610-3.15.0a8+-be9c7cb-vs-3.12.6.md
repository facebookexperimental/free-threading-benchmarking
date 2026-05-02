# Results vs. 3.12.6

- fork: python
- ref: be9c7cb4b50f8007b610
- machine: darwin-arm64
- commit hash: be9c7cb
- commit date: 2026-05-01
- overall geometric mean: 1.128x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260501-macm4pro-arm64-python-be9c7cb4b50f8007b610-3.15.0a8+-be9c7cb |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 118 ms: 1.03x slower                                                     |
| docutils       | 1.02 sec                                                 | 969 ms: 1.05x faster                                                     |
| html5lib       | 23.0 ms                                                  | 22.2 ms: 1.04x faster                                                    |
| sphinx         | 434 ms                                                   | 408 ms: 1.06x faster                                                     |
| Geometric mean | (ref)                                                    | 1.03x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260501-macm4pro-arm64-python-be9c7cb4b50f8007b610-3.15.0a8+-be9c7cb |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 309 ms: 1.61x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 120 ms: 1.49x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 309 ms: 1.49x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 328 ms: 1.46x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 125 ms: 1.38x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 9.89 ms: 1.37x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 172 ms: 1.34x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 335 ms: 1.33x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 176 ms: 1.27x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 282 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 292 ms: 1.16x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 115 ms: 1.15x faster                                                     |
| async_generators                 | 206 ms                                                   | 181 ms: 1.14x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 40.2 ms: 1.13x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 263 ms: 1.24x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 152 ms: 1.35x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 102 ms: 3.18x slower                                                     |
| Geometric mean                   | (ref)                                                    | 1.12x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260501-macm4pro-arm64-python-be9c7cb4b50f8007b610-3.15.0a8+-be9c7cb |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.8 ms: 1.27x faster                                                    |
| nbody          | 54.2 ms                                                  | 44.4 ms: 1.22x faster                                                    |
| pidigits       | 161 ms                                                   | 165 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                    | 1.15x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260501-macm4pro-arm64-python-be9c7cb4b50f8007b610-3.15.0a8+-be9c7cb |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 45.7 ms: 1.20x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 95.1 ms: 1.05x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.73 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                    | 1.09x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260501-macm4pro-arm64-python-be9c7cb4b50f8007b610-3.15.0a8+-be9c7cb |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 43.0 ms: 1.20x faster                                                    |
| tomli_loads          | 957 ms                                                   | 820 ms: 1.17x faster                                                     |
| json_dumps           | 4.26 ms                                                  | 3.74 ms: 1.14x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 35.9 ms: 1.08x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 25.2 ms: 1.06x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 100 us: 1.03x faster                                                     |
| xml_etree_parse      | 67.9 ms                                                  | 66.6 ms: 1.02x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 140 us: 1.01x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.07x faster                                                             |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260501-macm4pro-arm64-python-be9c7cb4b50f8007b610-3.15.0a8+-be9c7cb |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 5.71 ms                                                  | 5.93 ms: 1.04x slower                                                    |
| python_startup         | 8.01 ms                                                  | 8.77 ms: 1.09x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.07x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260501-macm4pro-arm64-python-be9c7cb4b50f8007b610-3.15.0a8+-be9c7cb |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.89 ms: 1.02x slower                                                    |
| django_template | 13.6 ms                                                  | 14.9 ms: 1.10x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.06x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260501-macm4pro-arm64-python-be9c7cb4b50f8007b610-3.15.0a8+-be9c7cb |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.05 ms: 5.12x faster                                                    |
| pylint                           | 128 ms                                                   | 57.0 ms: 2.25x faster                                                    |
| mdp                              | 1.09 sec                                                 | 540 ms: 2.02x faster                                                     |
| deepcopy                         | 161 us                                                   | 99.1 us: 1.63x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 309 ms: 1.61x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 11.7 us: 1.57x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 120 ms: 1.49x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 309 ms: 1.49x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 328 ms: 1.46x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 6.97 us: 1.41x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 125 ms: 1.38x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 9.89 ms: 1.37x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.08 us: 1.36x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 172 ms: 1.34x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 335 ms: 1.33x faster                                                     |
| go                               | 70.0 ms                                                  | 53.0 ms: 1.32x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 39.7 ns: 1.28x faster                                                    |
| float                            | 37.9 ms                                                  | 29.8 ms: 1.27x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 176 ms: 1.27x faster                                                     |
| raytrace                         | 145 ms                                                   | 115 ms: 1.26x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 43.4 ms: 1.25x faster                                                    |
| generators                       | 21.9 ms                                                  | 17.6 ms: 1.24x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 35.0 ms: 1.24x faster                                                    |
| nbody                            | 54.2 ms                                                  | 44.4 ms: 1.22x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 43.0 ms: 1.20x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 45.7 ms: 1.20x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 51.1 ms: 1.19x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 119 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 282 ms: 1.18x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.46 ms: 1.18x faster                                                    |
| chaos                            | 28.9 ms                                                  | 24.6 ms: 1.18x faster                                                    |
| pyflate                          | 216 ms                                                   | 185 ms: 1.17x faster                                                     |
| tomli_loads                      | 957 ms                                                   | 820 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 292 ms: 1.16x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.24 us: 1.15x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 115 ms: 1.15x faster                                                     |
| logging_format                   | 2.80 us                                                  | 2.45 us: 1.15x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.96 sec: 1.15x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.14x faster                                                    |
| k_core                           | 1.12 sec                                                 | 979 ms: 1.14x faster                                                     |
| async_generators                 | 206 ms                                                   | 181 ms: 1.14x faster                                                     |
| typing_runtime_protocols         | 71.0 us                                                  | 62.2 us: 1.14x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.74 ms: 1.14x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 28.3 ms: 1.14x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 40.2 ms: 1.13x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.9 ms: 1.13x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.77 ms: 1.10x faster                                                    |
| richards                         | 22.4 ms                                                  | 20.6 ms: 1.09x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 23.4 ms: 1.08x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 35.9 ms: 1.08x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.92 ms: 1.08x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.44 ms: 1.08x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 305 ms: 1.08x faster                                                     |
| pprint_pformat                   | 665 ms                                                   | 623 ms: 1.07x faster                                                     |
| fannkuch                         | 176 ms                                                   | 165 ms: 1.07x faster                                                     |
| sphinx                           | 434 ms                                                   | 408 ms: 1.06x faster                                                     |
| scimark_lu                       | 51.3 ms                                                  | 48.4 ms: 1.06x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 25.2 ms: 1.06x faster                                                    |
| sympy_str                        | 104 ms                                                   | 98.5 ms: 1.06x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 54.5 ms: 1.06x faster                                                    |
| docutils                         | 1.02 sec                                                 | 969 ms: 1.05x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 95.1 ms: 1.05x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 927 ns: 1.04x faster                                                     |
| thrift                           | 322 us                                                   | 310 us: 1.04x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 22.2 ms: 1.04x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 1.95 ms: 1.03x faster                                                    |
| pycparser                        | 497 ms                                                   | 484 ms: 1.03x faster                                                     |
| unpickle_pure_python             | 103 us                                                   | 100 us: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                     |
| json                             | 1.93 ms                                                  | 1.89 ms: 1.02x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 66.6 ms: 1.02x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                     |
| pickle_pure_python               | 139 us                                                   | 140 us: 1.01x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 39.3 ms: 1.01x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.73 ms: 1.01x slower                                                    |
| shortest_path                    | 219 ms                                                   | 223 ms: 1.02x slower                                                     |
| pidigits                         | 161 ms                                                   | 165 ms: 1.02x slower                                                     |
| connected_components             | 201 ms                                                   | 205 ms: 1.02x slower                                                     |
| mako                             | 4.77 ms                                                  | 4.89 ms: 1.02x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 429 us: 1.02x slower                                                     |
| 2to3                             | 114 ms                                                   | 118 ms: 1.03x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 5.93 ms: 1.04x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 50.1 ms: 1.05x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 874 us: 1.05x slower                                                     |
| telco                            | 2.61 ms                                                  | 2.79 ms: 1.07x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.77 ms: 1.09x slower                                                    |
| django_template                  | 13.6 ms                                                  | 14.9 ms: 1.10x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 47.5 ms: 1.20x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 263 ms: 1.24x slower                                                     |
| coverage                         | 26.9 ms                                                  | 34.2 ms: 1.27x slower                                                    |
| many_optionals                   | 195 us                                                   | 256 us: 1.31x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 152 ms: 1.35x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 102 ms: 3.18x slower                                                     |
| Geometric mean                   | (ref)                                                    | 1.13x faster                                                             |

Benchmark hidden because not significant (2): json_loads, sympy_expand
Ignored benchmarks (12) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260501-3.15.0a8+-be9c7cb/bm-20260501-macm4pro-arm64-python-be9c7cb4b50f8007b610-3.15.0a8+-be9c7cb.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.128x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.22x