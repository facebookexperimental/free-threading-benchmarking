# Results vs. 3.12.6

- fork: python
- ref: ab5187ce84a1e6641b5a
- machine: darwin-arm64
- commit hash: ab5187c
- commit date: 2026-10-22
- overall geometric mean: 1.204x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261022-macm4pro-arm64-python-ab5187ce84a1e6641b5a-3.16.0a1+dev-ab5187c |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 111 ms: 1.03x faster                                                        |
| docutils       | 1.02 sec                                                 | 898 ms: 1.14x faster                                                        |
| html5lib       | 23.0 ms                                                  | 20.5 ms: 1.12x faster                                                       |
| sphinx         | 434 ms                                                   | 384 ms: 1.13x faster                                                        |
| Geometric mean | (ref)                                                    | 1.10x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261022-macm4pro-arm64-python-ab5187ce84a1e6641b5a-3.16.0a1+dev-ab5187c |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 261 ms: 1.90x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 276 ms: 1.74x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 267 ms: 1.72x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 108 ms: 1.65x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 274 ms: 1.63x faster                                                        |
| async_tree_none_tg               | 172 ms                                                   | 110 ms: 1.57x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 155 ms: 1.49x faster                                                        |
| async_generators                 | 206 ms                                                   | 140 ms: 1.48x faster                                                        |
| async_tree_memoization           | 223 ms                                                   | 159 ms: 1.40x faster                                                        |
| coroutines                       | 13.6 ms                                                  | 9.84 ms: 1.38x faster                                                       |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 262 ms: 1.27x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 267 ms: 1.27x faster                                                        |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.19x faster                                                        |
| async_tree_eager                 | 45.6 ms                                                  | 39.6 ms: 1.15x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 216 ms: 1.07x faster                                                        |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                        |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 246 ms: 1.16x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 139 ms: 1.24x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 91.4 ms: 2.84x slower                                                       |
| Geometric mean                   | (ref)                                                    | 1.24x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261022-macm4pro-arm64-python-ab5187ce84a1e6641b5a-3.16.0a1+dev-ab5187c |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 26.9 ms: 1.41x faster                                                       |
| nbody          | 54.2 ms                                                  | 43.3 ms: 1.25x faster                                                       |
| pidigits       | 161 ms                                                   | 159 ms: 1.01x faster                                                        |
| Geometric mean | (ref)                                                    | 1.21x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261022-macm4pro-arm64-python-ab5187ce84a1e6641b5a-3.16.0a1+dev-ab5187c |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.31 ms: 1.28x faster                                                       |
| regex_dna      | 99.6 ms                                                  | 89.5 ms: 1.11x faster                                                       |
| regex_v8       | 9.59 ms                                                  | 9.17 ms: 1.05x faster                                                       |
| regex_compile  | 54.6 ms                                                  | 53.0 ms: 1.03x faster                                                       |
| Geometric mean | (ref)                                                    | 1.11x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261022-macm4pro-arm64-python-ab5187ce84a1e6641b5a-3.16.0a1+dev-ab5187c |
|----------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 41.7 ms: 1.23x faster                                                       |
| json_dumps           | 4.26 ms                                                  | 3.49 ms: 1.22x faster                                                       |
| tomli_loads          | 957 ms                                                   | 807 ms: 1.19x faster                                                        |
| xml_etree_generate   | 38.9 ms                                                  | 34.3 ms: 1.13x faster                                                       |
| unpickle_pure_python | 103 us                                                   | 93.0 us: 1.11x faster                                                       |
| xml_etree_process    | 26.7 ms                                                  | 24.6 ms: 1.09x faster                                                       |
| json_loads           | 10.9 us                                                  | 10.2 us: 1.06x faster                                                       |
| xml_etree_parse      | 67.9 ms                                                  | 64.1 ms: 1.06x faster                                                       |
| pickle_pure_python   | 139 us                                                   | 138 us: 1.01x faster                                                        |
| Geometric mean       | (ref)                                                    | 1.12x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261022-macm4pro-arm64-python-ab5187ce84a1e6641b5a-3.16.0a1+dev-ab5187c |
|------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.23 ms: 1.03x slower                                                       |
| python_startup_no_site | 5.71 ms                                                  | 6.41 ms: 1.12x slower                                                       |
| Geometric mean         | (ref)                                                    | 1.07x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261022-macm4pro-arm64-python-ab5187ce84a1e6641b5a-3.16.0a1+dev-ab5187c |
|-----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.41 ms: 1.08x faster                                                       |
| django_template | 13.6 ms                                                  | 14.5 ms: 1.07x slower                                                       |
| Geometric mean  | (ref)                                                    | 1.01x faster                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261022-macm4pro-arm64-python-ab5187ce84a1e6641b5a-3.16.0a1+dev-ab5187c |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.87 ms: 5.37x faster                                                       |
| pylint                           | 128 ms                                                   | 51.5 ms: 2.49x faster                                                       |
| mdp                              | 1.09 sec                                                 | 497 ms: 2.20x faster                                                        |
| async_tree_eager_io              | 496 ms                                                   | 261 ms: 1.90x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 276 ms: 1.74x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 267 ms: 1.72x faster                                                        |
| deepcopy                         | 161 us                                                   | 94.6 us: 1.71x faster                                                       |
| async_tree_none                  | 178 ms                                                   | 108 ms: 1.65x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 274 ms: 1.63x faster                                                        |
| deepcopy_memo                    | 18.3 us                                                  | 11.5 us: 1.59x faster                                                       |
| async_tree_none_tg               | 172 ms                                                   | 110 ms: 1.57x faster                                                        |
| comprehensions                   | 9.84 us                                                  | 6.60 us: 1.49x faster                                                       |
| async_tree_memoization_tg        | 231 ms                                                   | 155 ms: 1.49x faster                                                        |
| async_generators                 | 206 ms                                                   | 140 ms: 1.48x faster                                                        |
| typing_runtime_protocols         | 71.0 us                                                  | 48.1 us: 1.48x faster                                                       |
| float                            | 37.9 ms                                                  | 26.9 ms: 1.41x faster                                                       |
| async_tree_memoization           | 223 ms                                                   | 159 ms: 1.40x faster                                                        |
| deepcopy_reduce                  | 1.46 us                                                  | 1.06 us: 1.38x faster                                                       |
| coroutines                       | 13.6 ms                                                  | 9.84 ms: 1.38x faster                                                       |
| go                               | 70.0 ms                                                  | 51.3 ms: 1.37x faster                                                       |
| create_gc_cycles                 | 830 us                                                   | 619 us: 1.34x faster                                                        |
| spectral_norm                    | 54.4 ms                                                  | 40.7 ms: 1.33x faster                                                       |
| generators                       | 21.9 ms                                                  | 16.8 ms: 1.30x faster                                                       |
| raytrace                         | 145 ms                                                   | 111 ms: 1.30x faster                                                        |
| scimark_fft                      | 142 ms                                                   | 111 ms: 1.28x faster                                                        |
| regex_effbot                     | 1.67 ms                                                  | 1.31 ms: 1.28x faster                                                       |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 262 ms: 1.27x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 267 ms: 1.27x faster                                                        |
| scimark_sor                      | 61.0 ms                                                  | 48.1 ms: 1.27x faster                                                       |
| nbody                            | 54.2 ms                                                  | 43.3 ms: 1.25x faster                                                       |
| nqueens                          | 43.5 ms                                                  | 34.8 ms: 1.25x faster                                                       |
| logging_silent                   | 50.9 ns                                                  | 40.9 ns: 1.24x faster                                                       |
| xml_etree_iterparse              | 51.6 ms                                                  | 41.7 ms: 1.23x faster                                                       |
| json_dumps                       | 4.26 ms                                                  | 3.49 ms: 1.22x faster                                                       |
| deltablue                        | 1.73 ms                                                  | 1.42 ms: 1.21x faster                                                       |
| logging_simple                   | 2.57 us                                                  | 2.12 us: 1.21x faster                                                       |
| scimark_monte_carlo              | 32.2 ms                                                  | 26.7 ms: 1.20x faster                                                       |
| logging_format                   | 2.80 us                                                  | 2.33 us: 1.20x faster                                                       |
| pyflate                          | 216 ms                                                   | 179 ms: 1.20x faster                                                        |
| chaos                            | 28.9 ms                                                  | 24.2 ms: 1.20x faster                                                       |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.87 sec: 1.20x faster                                                      |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.19x faster                                                        |
| dulwich_log                      | 21.3 ms                                                  | 17.9 ms: 1.19x faster                                                       |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.75 ms: 1.19x faster                                                       |
| tomli_loads                      | 957 ms                                                   | 807 ms: 1.19x faster                                                        |
| pathlib                          | 12.4 ms                                                  | 10.5 ms: 1.18x faster                                                       |
| hexiom                           | 3.04 ms                                                  | 2.59 ms: 1.17x faster                                                       |
| gc_traversal                     | 2.01 ms                                                  | 1.73 ms: 1.16x faster                                                       |
| k_core                           | 1.12 sec                                                 | 967 ms: 1.16x faster                                                        |
| async_tree_eager                 | 45.6 ms                                                  | 39.6 ms: 1.15x faster                                                       |
| scimark_lu                       | 51.3 ms                                                  | 44.7 ms: 1.15x faster                                                       |
| docutils                         | 1.02 sec                                                 | 898 ms: 1.14x faster                                                        |
| xml_etree_generate               | 38.9 ms                                                  | 34.3 ms: 1.13x faster                                                       |
| sphinx                           | 434 ms                                                   | 384 ms: 1.13x faster                                                        |
| richards                         | 22.4 ms                                                  | 19.9 ms: 1.13x faster                                                       |
| richards_super                   | 25.4 ms                                                  | 22.6 ms: 1.12x faster                                                       |
| html5lib                         | 23.0 ms                                                  | 20.5 ms: 1.12x faster                                                       |
| regex_dna                        | 99.6 ms                                                  | 89.5 ms: 1.11x faster                                                       |
| sympy_integrate                  | 8.02 ms                                                  | 7.21 ms: 1.11x faster                                                       |
| unpickle_pure_python             | 103 us                                                   | 93.0 us: 1.11x faster                                                       |
| fannkuch                         | 176 ms                                                   | 161 ms: 1.09x faster                                                        |
| xml_etree_process                | 26.7 ms                                                  | 24.6 ms: 1.09x faster                                                       |
| mako                             | 4.77 ms                                                  | 4.41 ms: 1.08x faster                                                       |
| crypto_pyaes                     | 38.8 ms                                                  | 36.1 ms: 1.08x faster                                                       |
| sympy_str                        | 104 ms                                                   | 97.3 ms: 1.07x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 216 ms: 1.07x faster                                                        |
| pycparser                        | 497 ms                                                   | 466 ms: 1.07x faster                                                        |
| sympy_sum                        | 57.6 ms                                                  | 53.9 ms: 1.07x faster                                                       |
| sqlite_synth                     | 967 ns                                                   | 907 ns: 1.07x faster                                                        |
| json_loads                       | 10.9 us                                                  | 10.2 us: 1.06x faster                                                       |
| pprint_safe_repr                 | 328 ms                                                   | 308 ms: 1.06x faster                                                        |
| json                             | 1.93 ms                                                  | 1.82 ms: 1.06x faster                                                       |
| xml_etree_parse                  | 67.9 ms                                                  | 64.1 ms: 1.06x faster                                                       |
| thrift                           | 322 us                                                   | 305 us: 1.06x faster                                                        |
| pprint_pformat                   | 665 ms                                                   | 632 ms: 1.05x faster                                                        |
| regex_v8                         | 9.59 ms                                                  | 9.17 ms: 1.05x faster                                                       |
| regex_compile                    | 54.6 ms                                                  | 53.0 ms: 1.03x faster                                                       |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                        |
| bench_thread_pool                | 419 us                                                   | 408 us: 1.03x faster                                                        |
| 2to3                             | 114 ms                                                   | 111 ms: 1.03x faster                                                        |
| pidigits                         | 161 ms                                                   | 159 ms: 1.01x faster                                                        |
| pickle_pure_python               | 139 us                                                   | 138 us: 1.01x faster                                                        |
| sympy_expand                     | 167 ms                                                   | 166 ms: 1.01x faster                                                        |
| python_startup                   | 8.01 ms                                                  | 8.23 ms: 1.03x slower                                                       |
| shortest_path                    | 219 ms                                                   | 226 ms: 1.03x slower                                                        |
| connected_components             | 201 ms                                                   | 208 ms: 1.04x slower                                                        |
| django_template                  | 13.6 ms                                                  | 14.5 ms: 1.07x slower                                                       |
| bench_mp_pool                    | 39.7 ms                                                  | 42.9 ms: 1.08x slower                                                       |
| telco                            | 2.61 ms                                                  | 2.83 ms: 1.09x slower                                                       |
| many_optionals                   | 195 us                                                   | 219 us: 1.12x slower                                                        |
| python_startup_no_site           | 5.71 ms                                                  | 6.41 ms: 1.12x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 246 ms: 1.16x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 139 ms: 1.24x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 91.4 ms: 2.84x slower                                                       |
| Geometric mean                   | (ref)                                                    | 1.20x faster                                                                |

Benchmark hidden because not significant (1): meteor_contest
Ignored benchmarks (14) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261022-3.16.0a1+dev-ab5187c/bm-20261022-macm4pro-arm64-python-ab5187ce84a1e6641b5a-3.16.0a1+dev-ab5187c.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.204x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.13x
- 95% likely to have a speedup of 1.13x
- 99% likely to have a speedup of 1.11x

# Memory
- memory change: 1.17x