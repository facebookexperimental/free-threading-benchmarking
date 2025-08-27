# Results vs. 3.12.6

- fork: python
- ref: ffaec6e2a11fb7b41fac
- machine: darwin-arm64
- commit hash: ffaec6e
- commit date: 2025-08-27
- overall geometric mean: 1.077x faster
- HPT reliability: 91.46%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.25x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250827-macm4pro-arm64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 126 ms: 1.11x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                  |
| html5lib       | 23.0 ms                                                  | 23.8 ms: 1.03x slower                                                   |
| sphinx         | 434 ms                                                   | 412 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                    | 1.02x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250827-macm4pro-arm64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 198 ms: 2.42x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 206 ms: 2.41x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 197 ms: 2.26x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 210 ms: 2.19x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 86.9 ms: 1.98x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.85x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.75x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 131 ms: 1.70x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 237 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 245 ms: 1.36x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.9 ms: 1.25x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                    |
| async_generators                 | 206 ms                                                   | 183 ms: 1.13x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 229 ms: 1.08x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 49.4 ms: 1.08x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.6 ms: 2.45x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.37x faster                                                            |

Benchmark hidden because not significant (1): async_tree_eager_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250827-macm4pro-arm64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.9 ms: 1.27x faster                                                   |
| pidigits       | 161 ms                                                   | 166 ms: 1.03x slower                                                    |
| nbody          | 54.2 ms                                                  | 57.7 ms: 1.06x slower                                                   |
| Geometric mean | (ref)                                                    | 1.05x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250827-macm4pro-arm64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.22 ms: 1.04x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 97.5 ms: 1.02x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 53.6 ms: 1.02x faster                                                   |
| Geometric mean | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250827-macm4pro-arm64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.5 ms: 1.34x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 57.5 ms: 1.18x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.96 ms: 1.07x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 36.8 ms: 1.06x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 26.9 ms: 1.01x slower                                                   |
| tomli_loads          | 957 ms                                                   | 985 ms: 1.03x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.4 us: 1.05x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 112 us: 1.09x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 153 us: 1.10x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.04x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250827-macm4pro-arm64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.65 ms: 1.20x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 7.01 ms: 1.23x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.22x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250827-macm4pro-arm64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 24.3 ms: 1.11x slower                                                   |
| genshi_text     | 10.5 ms                                                  | 11.7 ms: 1.12x slower                                                   |
| mako            | 4.77 ms                                                  | 5.80 ms: 1.21x slower                                                   |
| django_template | 13.6 ms                                                  | 16.9 ms: 1.24x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.17x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250827-macm4pro-arm64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 779 us: 2.58x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 198 ms: 2.42x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 206 ms: 2.41x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 197 ms: 2.26x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 210 ms: 2.19x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 86.9 ms: 1.98x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.85x faster                                                    |
| mdp                              | 1.09 sec                                                 | 610 ms: 1.79x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.75x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 483 us: 1.72x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 131 ms: 1.70x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 237 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 245 ms: 1.36x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.5 ms: 1.34x faster                                                   |
| deepcopy                         | 161 us                                                   | 121 us: 1.34x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 14.3 us: 1.28x faster                                                   |
| float                            | 37.9 ms                                                  | 29.9 ms: 1.27x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.9 ms: 1.25x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 818 ns: 1.18x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 57.5 ms: 1.18x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 8.40 us: 1.17x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.26 us: 1.16x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                   |
| async_generators                 | 206 ms                                                   | 183 ms: 1.13x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.13x faster                                                   |
| generators                       | 21.9 ms                                                  | 19.5 ms: 1.13x faster                                                   |
| k_core                           | 1.12 sec                                                 | 997 ms: 1.12x faster                                                    |
| go                               | 70.0 ms                                                  | 62.5 ms: 1.12x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 45.6 ns: 1.12x faster                                                   |
| subparsers                       | 20.8 ms                                                  | 18.6 ms: 1.12x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.01 sec: 1.11x faster                                                  |
| dulwich_log                      | 21.3 ms                                                  | 19.1 ms: 1.11x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 55.5 ms: 1.10x faster                                                   |
| raytrace                         | 145 ms                                                   | 133 ms: 1.09x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 50.5 ms: 1.08x faster                                                   |
| json_dumps                       | 4.26 ms                                                  | 3.96 ms: 1.07x faster                                                   |
| pyflate                          | 216 ms                                                   | 201 ms: 1.07x faster                                                    |
| pylint                           | 128 ms                                                   | 120 ms: 1.07x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 36.8 ms: 1.06x faster                                                   |
| sphinx                           | 434 ms                                                   | 412 ms: 1.05x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.65 ms: 1.05x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.22 ms: 1.04x faster                                                   |
| pycparser                        | 497 ms                                                   | 479 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 97.5 ms: 1.02x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 53.6 ms: 1.02x faster                                                   |
| docutils                         | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                  |
| logging_simple                   | 2.57 us                                                  | 2.55 us: 1.01x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 26.9 ms: 1.01x slower                                                   |
| dask                             | 528 ms                                                   | 532 ms: 1.01x slower                                                    |
| scimark_fft                      | 142 ms                                                   | 143 ms: 1.01x slower                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.11 ms: 1.01x slower                                                   |
| nqueens                          | 43.5 ms                                                  | 44.0 ms: 1.01x slower                                                   |
| json                             | 1.93 ms                                                  | 1.96 ms: 1.02x slower                                                   |
| tomli_loads                      | 957 ms                                                   | 985 ms: 1.03x slower                                                    |
| pidigits                         | 161 ms                                                   | 166 ms: 1.03x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 73.3 us: 1.03x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 23.8 ms: 1.03x slower                                                   |
| chaos                            | 28.9 ms                                                  | 30.1 ms: 1.04x slower                                                   |
| hexiom                           | 3.04 ms                                                  | 3.19 ms: 1.05x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.4 us: 1.05x slower                                                   |
| thrift                           | 322 us                                                   | 339 us: 1.05x slower                                                    |
| richards                         | 22.4 ms                                                  | 23.8 ms: 1.06x slower                                                   |
| nbody                            | 54.2 ms                                                  | 57.7 ms: 1.06x slower                                                   |
| fannkuch                         | 176 ms                                                   | 187 ms: 1.07x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 27.1 ms: 1.07x slower                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 34.4 ms: 1.07x slower                                                   |
| shortest_path                    | 219 ms                                                   | 235 ms: 1.07x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 61.8 ms: 1.07x slower                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 352 ms: 1.07x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 229 ms: 1.08x slower                                                    |
| sympy_str                        | 104 ms                                                   | 112 ms: 1.08x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 719 ms: 1.08x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 49.4 ms: 1.08x slower                                                   |
| unpickle_pure_python             | 103 us                                                   | 112 us: 1.09x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 153 us: 1.10x slower                                                    |
| 2to3                             | 114 ms                                                   | 126 ms: 1.11x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 42.9 ms: 1.11x slower                                                   |
| connected_components             | 201 ms                                                   | 223 ms: 1.11x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 57.1 ms: 1.11x slower                                                   |
| genshi_xml                       | 21.8 ms                                                  | 24.3 ms: 1.11x slower                                                   |
| genshi_text                      | 10.5 ms                                                  | 11.7 ms: 1.12x slower                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.32 ms: 1.12x slower                                                   |
| telco                            | 2.61 ms                                                  | 2.98 ms: 1.14x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 45.3 ms: 1.14x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 192 ms: 1.15x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.65 ms: 1.20x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 57.7 ms: 1.21x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.80 ms: 1.21x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 7.01 ms: 1.23x slower                                                   |
| django_template                  | 13.6 ms                                                  | 16.9 ms: 1.24x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 593 us: 1.42x slower                                                    |
| coverage                         | 26.9 ms                                                  | 40.1 ms: 1.49x slower                                                   |
| many_optionals                   | 195 us                                                   | 340 us: 1.74x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.6 ms: 2.45x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.07x faster                                                            |

Benchmark hidden because not significant (2): async_tree_eager_memoization_tg, logging_format
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250827-3.15.0a0-ffaec6e-NOGIL/bm-20250827-macm4pro-arm64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.077x faster

# HPT report

- Reliability score: 91.46% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.25x