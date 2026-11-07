# Results vs. 3.12.6

- fork: python
- ref: ce4ac8c0459eba99459f
- machine: darwin-arm64
- commit hash: ce4ac8c
- commit date: 2026-11-07
- overall geometric mean: 1.207x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261107-macm4pro-arm64-python-ce4ac8c0459eba99459f-3.16.0a1+dev-ce4ac8c |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 113 ms: 1.01x faster                                                        |
| docutils       | 1.02 sec                                                 | 892 ms: 1.15x faster                                                        |
| html5lib       | 23.0 ms                                                  | 20.3 ms: 1.13x faster                                                       |
| sphinx         | 434 ms                                                   | 384 ms: 1.13x faster                                                        |
| Geometric mean | (ref)                                                    | 1.10x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261107-macm4pro-arm64-python-ce4ac8c0459eba99459f-3.16.0a1+dev-ce4ac8c |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_generators                 | 206 ms                                                   | 97.9 ms: 2.11x faster                                                       |
| async_tree_eager_io              | 496 ms                                                   | 262 ms: 1.89x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 278 ms: 1.73x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 269 ms: 1.71x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 109 ms: 1.63x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 277 ms: 1.61x faster                                                        |
| async_tree_none_tg               | 172 ms                                                   | 111 ms: 1.56x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 157 ms: 1.47x faster                                                        |
| coroutines                       | 13.6 ms                                                  | 9.68 ms: 1.40x faster                                                       |
| async_tree_memoization           | 223 ms                                                   | 160 ms: 1.39x faster                                                        |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 262 ms: 1.27x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 268 ms: 1.26x faster                                                        |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.18x faster                                                        |
| async_tree_eager                 | 45.6 ms                                                  | 40.7 ms: 1.12x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 218 ms: 1.06x faster                                                        |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                        |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 247 ms: 1.16x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 141 ms: 1.25x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 92.7 ms: 2.89x slower                                                       |
| Geometric mean                   | (ref)                                                    | 1.26x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261107-macm4pro-arm64-python-ce4ac8c0459eba99459f-3.16.0a1+dev-ce4ac8c |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 26.8 ms: 1.41x faster                                                       |
| nbody          | 54.2 ms                                                  | 41.3 ms: 1.31x faster                                                       |
| pidigits       | 161 ms                                                   | 148 ms: 1.09x faster                                                        |
| Geometric mean | (ref)                                                    | 1.27x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261107-macm4pro-arm64-python-ce4ac8c0459eba99459f-3.16.0a1+dev-ce4ac8c |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.38 ms: 1.21x faster                                                       |
| regex_dna      | 99.6 ms                                                  | 93.3 ms: 1.07x faster                                                       |
| regex_v8       | 9.59 ms                                                  | 9.03 ms: 1.06x faster                                                       |
| regex_compile  | 54.6 ms                                                  | 53.4 ms: 1.02x faster                                                       |
| Geometric mean | (ref)                                                    | 1.09x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261107-macm4pro-arm64-python-ce4ac8c0459eba99459f-3.16.0a1+dev-ce4ac8c |
|----------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 41.5 ms: 1.24x faster                                                       |
| json_dumps           | 4.26 ms                                                  | 3.55 ms: 1.20x faster                                                       |
| tomli_loads          | 957 ms                                                   | 814 ms: 1.18x faster                                                        |
| xml_etree_generate   | 38.9 ms                                                  | 34.6 ms: 1.12x faster                                                       |
| unpickle_pure_python | 103 us                                                   | 91.8 us: 1.12x faster                                                       |
| xml_etree_parse      | 67.9 ms                                                  | 62.5 ms: 1.09x faster                                                       |
| xml_etree_process    | 26.7 ms                                                  | 24.7 ms: 1.08x faster                                                       |
| json_loads           | 10.9 us                                                  | 10.4 us: 1.04x faster                                                       |
| pickle_pure_python   | 139 us                                                   | 137 us: 1.02x faster                                                        |
| Geometric mean       | (ref)                                                    | 1.12x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261107-macm4pro-arm64-python-ce4ac8c0459eba99459f-3.16.0a1+dev-ce4ac8c |
|------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 7.96 ms: 1.01x faster                                                       |
| python_startup_no_site | 5.71 ms                                                  | 6.25 ms: 1.10x slower                                                       |
| Geometric mean         | (ref)                                                    | 1.04x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261107-macm4pro-arm64-python-ce4ac8c0459eba99459f-3.16.0a1+dev-ce4ac8c |
|-----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.34 ms: 1.10x faster                                                       |
| django_template | 13.6 ms                                                  | 14.5 ms: 1.06x slower                                                       |
| Geometric mean  | (ref)                                                    | 1.02x faster                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261107-macm4pro-arm64-python-ce4ac8c0459eba99459f-3.16.0a1+dev-ce4ac8c |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.91 ms: 5.31x faster                                                       |
| pylint                           | 128 ms                                                   | 50.0 ms: 2.56x faster                                                       |
| mdp                              | 1.09 sec                                                 | 500 ms: 2.18x faster                                                        |
| async_generators                 | 206 ms                                                   | 97.9 ms: 2.11x faster                                                       |
| async_tree_eager_io              | 496 ms                                                   | 262 ms: 1.89x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 278 ms: 1.73x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 269 ms: 1.71x faster                                                        |
| deepcopy                         | 161 us                                                   | 95.1 us: 1.70x faster                                                       |
| async_tree_none                  | 178 ms                                                   | 109 ms: 1.63x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 277 ms: 1.61x faster                                                        |
| deepcopy_memo                    | 18.3 us                                                  | 11.5 us: 1.59x faster                                                       |
| typing_runtime_protocols         | 71.0 us                                                  | 45.5 us: 1.56x faster                                                       |
| async_tree_none_tg               | 172 ms                                                   | 111 ms: 1.56x faster                                                        |
| comprehensions                   | 9.84 us                                                  | 6.58 us: 1.50x faster                                                       |
| async_tree_memoization_tg        | 231 ms                                                   | 157 ms: 1.47x faster                                                        |
| deepcopy_reduce                  | 1.46 us                                                  | 1.02 us: 1.43x faster                                                       |
| float                            | 37.9 ms                                                  | 26.8 ms: 1.41x faster                                                       |
| coroutines                       | 13.6 ms                                                  | 9.68 ms: 1.40x faster                                                       |
| async_tree_memoization           | 223 ms                                                   | 160 ms: 1.39x faster                                                        |
| go                               | 70.0 ms                                                  | 51.1 ms: 1.37x faster                                                       |
| create_gc_cycles                 | 830 us                                                   | 623 us: 1.33x faster                                                        |
| spectral_norm                    | 54.4 ms                                                  | 41.1 ms: 1.32x faster                                                       |
| nbody                            | 54.2 ms                                                  | 41.3 ms: 1.31x faster                                                       |
| generators                       | 21.9 ms                                                  | 16.8 ms: 1.31x faster                                                       |
| raytrace                         | 145 ms                                                   | 112 ms: 1.29x faster                                                        |
| scimark_fft                      | 142 ms                                                   | 111 ms: 1.27x faster                                                        |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 262 ms: 1.27x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 268 ms: 1.26x faster                                                        |
| nqueens                          | 43.5 ms                                                  | 34.6 ms: 1.26x faster                                                       |
| scimark_sor                      | 61.0 ms                                                  | 48.8 ms: 1.25x faster                                                       |
| xml_etree_iterparse              | 51.6 ms                                                  | 41.5 ms: 1.24x faster                                                       |
| scimark_monte_carlo              | 32.2 ms                                                  | 25.9 ms: 1.24x faster                                                       |
| dulwich_log                      | 21.3 ms                                                  | 17.5 ms: 1.21x faster                                                       |
| logging_silent                   | 50.9 ns                                                  | 42.0 ns: 1.21x faster                                                       |
| regex_effbot                     | 1.67 ms                                                  | 1.38 ms: 1.21x faster                                                       |
| pyflate                          | 216 ms                                                   | 179 ms: 1.21x faster                                                        |
| deltablue                        | 1.73 ms                                                  | 1.43 ms: 1.20x faster                                                       |
| json_dumps                       | 4.26 ms                                                  | 3.55 ms: 1.20x faster                                                       |
| logging_simple                   | 2.57 us                                                  | 2.14 us: 1.20x faster                                                       |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.87 sec: 1.20x faster                                                      |
| chaos                            | 28.9 ms                                                  | 24.3 ms: 1.19x faster                                                       |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.75 ms: 1.19x faster                                                       |
| logging_format                   | 2.80 us                                                  | 2.37 us: 1.18x faster                                                       |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.18x faster                                                        |
| pathlib                          | 12.4 ms                                                  | 10.5 ms: 1.18x faster                                                       |
| tomli_loads                      | 957 ms                                                   | 814 ms: 1.18x faster                                                        |
| hexiom                           | 3.04 ms                                                  | 2.60 ms: 1.17x faster                                                       |
| k_core                           | 1.12 sec                                                 | 972 ms: 1.15x faster                                                        |
| gc_traversal                     | 2.01 ms                                                  | 1.75 ms: 1.15x faster                                                       |
| docutils                         | 1.02 sec                                                 | 892 ms: 1.15x faster                                                        |
| html5lib                         | 23.0 ms                                                  | 20.3 ms: 1.13x faster                                                       |
| sphinx                           | 434 ms                                                   | 384 ms: 1.13x faster                                                        |
| xml_etree_generate               | 38.9 ms                                                  | 34.6 ms: 1.12x faster                                                       |
| unpickle_pure_python             | 103 us                                                   | 91.8 us: 1.12x faster                                                       |
| richards                         | 22.4 ms                                                  | 20.0 ms: 1.12x faster                                                       |
| async_tree_eager                 | 45.6 ms                                                  | 40.7 ms: 1.12x faster                                                       |
| richards_super                   | 25.4 ms                                                  | 22.8 ms: 1.11x faster                                                       |
| scimark_lu                       | 51.3 ms                                                  | 46.1 ms: 1.11x faster                                                       |
| sympy_integrate                  | 8.02 ms                                                  | 7.25 ms: 1.11x faster                                                       |
| fannkuch                         | 176 ms                                                   | 159 ms: 1.10x faster                                                        |
| mako                             | 4.77 ms                                                  | 4.34 ms: 1.10x faster                                                       |
| pidigits                         | 161 ms                                                   | 148 ms: 1.09x faster                                                        |
| xml_etree_parse                  | 67.9 ms                                                  | 62.5 ms: 1.09x faster                                                       |
| xml_etree_process                | 26.7 ms                                                  | 24.7 ms: 1.08x faster                                                       |
| crypto_pyaes                     | 38.8 ms                                                  | 36.1 ms: 1.08x faster                                                       |
| pycparser                        | 497 ms                                                   | 463 ms: 1.08x faster                                                        |
| thrift                           | 322 us                                                   | 301 us: 1.07x faster                                                        |
| regex_dna                        | 99.6 ms                                                  | 93.3 ms: 1.07x faster                                                       |
| sympy_str                        | 104 ms                                                   | 97.9 ms: 1.06x faster                                                       |
| pprint_safe_repr                 | 328 ms                                                   | 308 ms: 1.06x faster                                                        |
| regex_v8                         | 9.59 ms                                                  | 9.03 ms: 1.06x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 218 ms: 1.06x faster                                                        |
| sqlite_synth                     | 967 ns                                                   | 913 ns: 1.06x faster                                                        |
| sympy_sum                        | 57.6 ms                                                  | 54.4 ms: 1.06x faster                                                       |
| json                             | 1.93 ms                                                  | 1.84 ms: 1.05x faster                                                       |
| json_loads                       | 10.9 us                                                  | 10.4 us: 1.04x faster                                                       |
| pprint_pformat                   | 665 ms                                                   | 638 ms: 1.04x faster                                                        |
| bench_thread_pool                | 419 us                                                   | 410 us: 1.02x faster                                                        |
| regex_compile                    | 54.6 ms                                                  | 53.4 ms: 1.02x faster                                                       |
| pickle_pure_python               | 139 us                                                   | 137 us: 1.02x faster                                                        |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                        |
| 2to3                             | 114 ms                                                   | 113 ms: 1.01x faster                                                        |
| python_startup                   | 8.01 ms                                                  | 7.96 ms: 1.01x faster                                                       |
| sympy_expand                     | 167 ms                                                   | 167 ms: 1.00x faster                                                        |
| meteor_contest                   | 47.7 ms                                                  | 48.3 ms: 1.01x slower                                                       |
| shortest_path                    | 219 ms                                                   | 226 ms: 1.03x slower                                                        |
| connected_components             | 201 ms                                                   | 208 ms: 1.04x slower                                                        |
| bench_mp_pool                    | 39.7 ms                                                  | 41.4 ms: 1.04x slower                                                       |
| django_template                  | 13.6 ms                                                  | 14.5 ms: 1.06x slower                                                       |
| telco                            | 2.61 ms                                                  | 2.84 ms: 1.09x slower                                                       |
| python_startup_no_site           | 5.71 ms                                                  | 6.25 ms: 1.10x slower                                                       |
| many_optionals                   | 195 us                                                   | 225 us: 1.15x slower                                                        |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 247 ms: 1.16x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 141 ms: 1.25x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 92.7 ms: 2.89x slower                                                       |
| Geometric mean                   | (ref)                                                    | 1.20x faster                                                                |
Ignored benchmarks (14) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261107-3.16.0a1+dev-ce4ac8c/bm-20261107-macm4pro-arm64-python-ce4ac8c0459eba99459f-3.16.0a1+dev-ce4ac8c.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.207x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.13x
- 95% likely to have a speedup of 1.12x
- 99% likely to have a speedup of 1.11x

# Memory
- memory change: 1.15x