# Results vs. 3.12.6

- fork: python
- ref: fe3a26f43fad1d6eed20
- machine: darwin-arm64
- commit hash: fe3a26f
- commit date: 2026-08-26
- overall geometric mean: 1.140x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260826-macm4pro-arm64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 119 ms: 1.04x slower                                                    |
| docutils       | 1.02 sec                                                 | 950 ms: 1.08x faster                                                    |
| html5lib       | 23.0 ms                                                  | 21.3 ms: 1.08x faster                                                   |
| sphinx         | 434 ms                                                   | 405 ms: 1.07x faster                                                    |
| Geometric mean | (ref)                                                    | 1.05x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260826-macm4pro-arm64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 310 ms: 1.60x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 121 ms: 1.47x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 314 ms: 1.46x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 331 ms: 1.45x faster                                                    |
| async_generators                 | 206 ms                                                   | 145 ms: 1.42x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.86 ms: 1.38x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 126 ms: 1.37x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 334 ms: 1.33x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 173 ms: 1.33x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 177 ms: 1.26x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 283 ms: 1.18x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 292 ms: 1.16x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 116 ms: 1.14x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 41.4 ms: 1.10x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 227 ms: 1.02x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 263 ms: 1.24x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 153 ms: 1.36x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 103 ms: 3.22x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.13x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260826-macm4pro-arm64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.3 ms: 1.29x faster                                                   |
| nbody          | 54.2 ms                                                  | 43.1 ms: 1.26x faster                                                   |
| pidigits       | 161 ms                                                   | 166 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                    | 1.17x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260826-macm4pro-arm64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.40 ms: 1.19x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 91.7 ms: 1.09x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.21 ms: 1.04x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 54.8 ms: 1.00x slower                                                   |
| Geometric mean | (ref)                                                    | 1.08x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260826-macm4pro-arm64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 957 ms                                                   | 804 ms: 1.19x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.60 ms: 1.18x faster                                                   |
| xml_etree_iterparse  | 51.6 ms                                                  | 43.8 ms: 1.18x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 36.6 ms: 1.06x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 97.9 us: 1.05x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 25.8 ms: 1.04x faster                                                   |
| pickle_pure_python   | 139 us                                                   | 141 us: 1.02x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.07x faster                                                            |

Benchmark hidden because not significant (2): xml_etree_parse, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260826-macm4pro-arm64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.18 ms: 1.15x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.68 ms: 1.17x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.16x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260826-macm4pro-arm64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.66 ms: 1.02x faster                                                   |
| django_template | 13.6 ms                                                  | 15.3 ms: 1.12x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.05x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260826-macm4pro-arm64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.09 ms: 5.07x faster                                                   |
| pylint                           | 128 ms                                                   | 56.8 ms: 2.25x faster                                                   |
| mdp                              | 1.09 sec                                                 | 521 ms: 2.10x faster                                                    |
| deepcopy                         | 161 us                                                   | 97.1 us: 1.66x faster                                                   |
| async_tree_eager_io              | 496 ms                                                   | 310 ms: 1.60x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 11.7 us: 1.56x faster                                                   |
| async_tree_none                  | 178 ms                                                   | 121 ms: 1.47x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 6.73 us: 1.46x faster                                                   |
| async_tree_io                    | 459 ms                                                   | 314 ms: 1.46x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 331 ms: 1.45x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 49.3 us: 1.44x faster                                                   |
| async_generators                 | 206 ms                                                   | 145 ms: 1.42x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.86 ms: 1.38x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.07 us: 1.37x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 126 ms: 1.37x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 334 ms: 1.33x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 173 ms: 1.33x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 41.8 ms: 1.30x faster                                                   |
| go                               | 70.0 ms                                                  | 53.9 ms: 1.30x faster                                                   |
| float                            | 37.9 ms                                                  | 29.3 ms: 1.29x faster                                                   |
| nbody                            | 54.2 ms                                                  | 43.1 ms: 1.26x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 177 ms: 1.26x faster                                                    |
| raytrace                         | 145 ms                                                   | 118 ms: 1.23x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 41.4 ns: 1.23x faster                                                   |
| generators                       | 21.9 ms                                                  | 17.9 ms: 1.23x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 116 ms: 1.23x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 49.8 ms: 1.23x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 35.5 ms: 1.22x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.40 ms: 1.19x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 804 ms: 1.19x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.60 ms: 1.18x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 283 ms: 1.18x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 43.8 ms: 1.18x faster                                                   |
| pyflate                          | 216 ms                                                   | 184 ms: 1.17x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.21 us: 1.17x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 292 ms: 1.16x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.3 ms: 1.16x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.49 ms: 1.16x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.95 sec: 1.15x faster                                                  |
| scimark_monte_carlo              | 32.2 ms                                                  | 28.0 ms: 1.15x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.44 us: 1.15x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.15x faster                                                   |
| k_core                           | 1.12 sec                                                 | 981 ms: 1.14x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.82 ms: 1.14x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 116 ms: 1.14x faster                                                    |
| chaos                            | 28.9 ms                                                  | 25.5 ms: 1.13x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.73 ms: 1.11x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 41.4 ms: 1.10x faster                                                   |
| richards                         | 22.4 ms                                                  | 20.4 ms: 1.10x faster                                                   |
| fannkuch                         | 176 ms                                                   | 160 ms: 1.10x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 23.2 ms: 1.09x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 91.7 ms: 1.09x faster                                                   |
| html5lib                         | 23.0 ms                                                  | 21.3 ms: 1.08x faster                                                   |
| docutils                         | 1.02 sec                                                 | 950 ms: 1.08x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.49 ms: 1.07x faster                                                   |
| sphinx                           | 434 ms                                                   | 405 ms: 1.07x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 36.6 ms: 1.06x faster                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 309 ms: 1.06x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 97.9 us: 1.05x faster                                                   |
| pprint_pformat                   | 665 ms                                                   | 635 ms: 1.05x faster                                                    |
| sympy_str                        | 104 ms                                                   | 100.0 ms: 1.04x faster                                                  |
| gc_traversal                     | 2.01 ms                                                  | 1.93 ms: 1.04x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.21 ms: 1.04x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 55.6 ms: 1.04x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 25.8 ms: 1.04x faster                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 37.6 ms: 1.03x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 49.7 ms: 1.03x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 937 ns: 1.03x faster                                                    |
| mako                             | 4.77 ms                                                  | 4.66 ms: 1.02x faster                                                   |
| thrift                           | 322 us                                                   | 315 us: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 227 ms: 1.02x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                    |
| json                             | 1.93 ms                                                  | 1.92 ms: 1.01x faster                                                   |
| pycparser                        | 497 ms                                                   | 494 ms: 1.01x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 826 us: 1.00x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 54.8 ms: 1.00x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 422 us: 1.01x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 169 ms: 1.01x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 141 us: 1.02x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 48.8 ms: 1.02x slower                                                   |
| pidigits                         | 161 ms                                                   | 166 ms: 1.03x slower                                                    |
| shortest_path                    | 219 ms                                                   | 225 ms: 1.03x slower                                                    |
| 2to3                             | 114 ms                                                   | 119 ms: 1.04x slower                                                    |
| connected_components             | 201 ms                                                   | 209 ms: 1.04x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.90 ms: 1.11x slower                                                   |
| django_template                  | 13.6 ms                                                  | 15.3 ms: 1.12x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.9 ms: 1.13x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.18 ms: 1.15x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.68 ms: 1.17x slower                                                   |
| many_optionals                   | 195 us                                                   | 239 us: 1.23x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 263 ms: 1.24x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 153 ms: 1.36x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 103 ms: 3.22x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.14x faster                                                            |

Benchmark hidden because not significant (2): xml_etree_parse, json_loads
Ignored benchmarks (14) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260826-3.16.0a0-fe3a26f/bm-20260826-macm4pro-arm64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.140x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.19x