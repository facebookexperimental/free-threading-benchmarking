# Results vs. 3.12.6

- fork: python
- ref: fdec4df45ab69fc25019
- machine: darwin-arm64
- commit hash: fdec4df
- commit date: 2026-10-15
- overall geometric mean: 1.054x faster
- HPT reliability: 84.34%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.29x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261015-macm4pro-arm64-python-fdec4df45ab69fc25019-3.16.0a1+dev-fdec4df |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 130 ms: 1.14x slower                                                        |
| docutils       | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                      |
| sphinx         | 434 ms                                                   | 449 ms: 1.04x slower                                                        |
| Geometric mean | (ref)                                                    | 1.05x slower                                                                |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261015-macm4pro-arm64-python-fdec4df45ab69fc25019-3.16.0a1+dev-fdec4df |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 298 ms: 1.67x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 297 ms: 1.61x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 295 ms: 1.51x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 308 ms: 1.49x faster                                                        |
| async_generators                 | 206 ms                                                   | 160 ms: 1.29x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 182 ms: 1.27x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 143 ms: 1.24x faster                                                        |
| async_tree_none_tg               | 172 ms                                                   | 141 ms: 1.22x faster                                                        |
| async_tree_memoization           | 223 ms                                                   | 187 ms: 1.19x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 297 ms: 1.14x faster                                                        |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 303 ms: 1.10x faster                                                        |
| coroutines                       | 13.6 ms                                                  | 12.7 ms: 1.07x faster                                                       |
| async_tree_eager_memoization     | 132 ms                                                   | 126 ms: 1.05x faster                                                        |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.03x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 237 ms: 1.03x slower                                                        |
| async_tree_eager                 | 45.6 ms                                                  | 50.2 ms: 1.10x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 277 ms: 1.30x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 164 ms: 1.46x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 114 ms: 3.56x slower                                                        |
| Geometric mean                   | (ref)                                                    | 1.07x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261015-macm4pro-arm64-python-fdec4df45ab69fc25019-3.16.0a1+dev-fdec4df |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 33.0 ms: 1.15x faster                                                       |
| pidigits       | 161 ms                                                   | 166 ms: 1.03x slower                                                        |
| nbody          | 54.2 ms                                                  | 57.4 ms: 1.06x slower                                                       |
| Geometric mean | (ref)                                                    | 1.02x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261015-macm4pro-arm64-python-fdec4df45ab69fc25019-3.16.0a1+dev-fdec4df |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.34 ms: 1.24x faster                                                       |
| regex_dna      | 99.6 ms                                                  | 93.0 ms: 1.07x faster                                                       |
| regex_v8       | 9.59 ms                                                  | 9.23 ms: 1.04x faster                                                       |
| regex_compile  | 54.6 ms                                                  | 64.3 ms: 1.18x slower                                                       |
| Geometric mean | (ref)                                                    | 1.04x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261015-macm4pro-arm64-python-fdec4df45ab69fc25019-3.16.0a1+dev-fdec4df |
|----------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 41.1 ms: 1.25x faster                                                       |
| xml_etree_parse      | 67.9 ms                                                  | 59.9 ms: 1.13x faster                                                       |
| json_dumps           | 4.26 ms                                                  | 3.82 ms: 1.12x faster                                                       |
| tomli_loads          | 957 ms                                                   | 892 ms: 1.07x faster                                                        |
| xml_etree_generate   | 38.9 ms                                                  | 39.0 ms: 1.00x slower                                                       |
| json_loads           | 10.9 us                                                  | 11.0 us: 1.02x slower                                                       |
| unpickle_pure_python | 103 us                                                   | 109 us: 1.06x slower                                                        |
| pickle_pure_python   | 139 us                                                   | 153 us: 1.10x slower                                                        |
| xml_etree_process    | 26.7 ms                                                  | 29.9 ms: 1.12x slower                                                       |
| Geometric mean       | (ref)                                                    | 1.03x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261015-macm4pro-arm64-python-fdec4df45ab69fc25019-3.16.0a1+dev-fdec4df |
|------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 10.1 ms: 1.26x slower                                                       |
| python_startup_no_site | 5.71 ms                                                  | 7.39 ms: 1.30x slower                                                       |
| Geometric mean         | (ref)                                                    | 1.28x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261015-macm4pro-arm64-python-fdec4df45ab69fc25019-3.16.0a1+dev-fdec4df |
|-----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 5.79 ms: 1.21x slower                                                       |
| django_template | 13.6 ms                                                  | 17.1 ms: 1.25x slower                                                       |
| Geometric mean  | (ref)                                                    | 1.23x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261015-macm4pro-arm64-python-fdec4df45ab69fc25019-3.16.0a1+dev-fdec4df |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.31 ms: 4.82x faster                                                       |
| gc_traversal                     | 2.01 ms                                                  | 785 us: 2.56x faster                                                        |
| pylint                           | 128 ms                                                   | 53.6 ms: 2.39x faster                                                       |
| mdp                              | 1.09 sec                                                 | 597 ms: 1.83x faster                                                        |
| create_gc_cycles                 | 830 us                                                   | 473 us: 1.75x faster                                                        |
| async_tree_eager_io              | 496 ms                                                   | 298 ms: 1.67x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 297 ms: 1.61x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 295 ms: 1.51x faster                                                        |
| deepcopy                         | 161 us                                                   | 108 us: 1.49x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 308 ms: 1.49x faster                                                        |
| async_generators                 | 206 ms                                                   | 160 ms: 1.29x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 182 ms: 1.27x faster                                                        |
| xml_etree_iterparse              | 51.6 ms                                                  | 41.1 ms: 1.25x faster                                                       |
| deepcopy_memo                    | 18.3 us                                                  | 14.6 us: 1.25x faster                                                       |
| async_tree_none                  | 178 ms                                                   | 143 ms: 1.24x faster                                                        |
| regex_effbot                     | 1.67 ms                                                  | 1.34 ms: 1.24x faster                                                       |
| deepcopy_reduce                  | 1.46 us                                                  | 1.18 us: 1.24x faster                                                       |
| typing_runtime_protocols         | 71.0 us                                                  | 57.8 us: 1.23x faster                                                       |
| async_tree_none_tg               | 172 ms                                                   | 141 ms: 1.22x faster                                                        |
| sqlite_synth                     | 967 ns                                                   | 804 ns: 1.20x faster                                                        |
| async_tree_memoization           | 223 ms                                                   | 187 ms: 1.19x faster                                                        |
| comprehensions                   | 9.84 us                                                  | 8.47 us: 1.16x faster                                                       |
| go                               | 70.0 ms                                                  | 60.6 ms: 1.16x faster                                                       |
| float                            | 37.9 ms                                                  | 33.0 ms: 1.15x faster                                                       |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.96 sec: 1.14x faster                                                      |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 297 ms: 1.14x faster                                                        |
| xml_etree_parse                  | 67.9 ms                                                  | 59.9 ms: 1.13x faster                                                       |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.13x faster                                                       |
| json_dumps                       | 4.26 ms                                                  | 3.82 ms: 1.12x faster                                                       |
| k_core                           | 1.12 sec                                                 | 1.01 sec: 1.11x faster                                                      |
| scimark_fft                      | 142 ms                                                   | 128 ms: 1.11x faster                                                        |
| spectral_norm                    | 54.4 ms                                                  | 49.0 ms: 1.11x faster                                                       |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 303 ms: 1.10x faster                                                        |
| pyflate                          | 216 ms                                                   | 198 ms: 1.09x faster                                                        |
| dulwich_log                      | 21.3 ms                                                  | 19.6 ms: 1.09x faster                                                       |
| tomli_loads                      | 957 ms                                                   | 892 ms: 1.07x faster                                                        |
| regex_dna                        | 99.6 ms                                                  | 93.0 ms: 1.07x faster                                                       |
| coroutines                       | 13.6 ms                                                  | 12.7 ms: 1.07x faster                                                       |
| raytrace                         | 145 ms                                                   | 136 ms: 1.07x faster                                                        |
| async_tree_eager_memoization     | 132 ms                                                   | 126 ms: 1.05x faster                                                        |
| scimark_sor                      | 61.0 ms                                                  | 58.5 ms: 1.04x faster                                                       |
| logging_simple                   | 2.57 us                                                  | 2.47 us: 1.04x faster                                                       |
| regex_v8                         | 9.59 ms                                                  | 9.23 ms: 1.04x faster                                                       |
| pycparser                        | 497 ms                                                   | 483 ms: 1.03x faster                                                        |
| logging_silent                   | 50.9 ns                                                  | 49.6 ns: 1.03x faster                                                       |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.03x faster                                                        |
| logging_format                   | 2.80 us                                                  | 2.73 us: 1.03x faster                                                       |
| nqueens                          | 43.5 ms                                                  | 43.3 ms: 1.00x faster                                                       |
| xml_etree_generate               | 38.9 ms                                                  | 39.0 ms: 1.00x slower                                                       |
| json                             | 1.93 ms                                                  | 1.95 ms: 1.01x slower                                                       |
| json_loads                       | 10.9 us                                                  | 11.0 us: 1.02x slower                                                       |
| sympy_integrate                  | 8.02 ms                                                  | 8.19 ms: 1.02x slower                                                       |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 237 ms: 1.03x slower                                                        |
| pidigits                         | 161 ms                                                   | 166 ms: 1.03x slower                                                        |
| docutils                         | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                      |
| sphinx                           | 434 ms                                                   | 449 ms: 1.04x slower                                                        |
| deltablue                        | 1.73 ms                                                  | 1.80 ms: 1.04x slower                                                       |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.8 ms: 1.05x slower                                                       |
| unpickle_pure_python             | 103 us                                                   | 109 us: 1.06x slower                                                        |
| nbody                            | 54.2 ms                                                  | 57.4 ms: 1.06x slower                                                       |
| crypto_pyaes                     | 38.8 ms                                                  | 41.5 ms: 1.07x slower                                                       |
| hexiom                           | 3.04 ms                                                  | 3.25 ms: 1.07x slower                                                       |
| sympy_sum                        | 57.6 ms                                                  | 61.6 ms: 1.07x slower                                                       |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.23 ms: 1.07x slower                                                       |
| sympy_str                        | 104 ms                                                   | 112 ms: 1.07x slower                                                        |
| pprint_safe_repr                 | 328 ms                                                   | 353 ms: 1.08x slower                                                        |
| thrift                           | 322 us                                                   | 347 us: 1.08x slower                                                        |
| richards                         | 22.4 ms                                                  | 24.2 ms: 1.08x slower                                                       |
| generators                       | 21.9 ms                                                  | 23.8 ms: 1.09x slower                                                       |
| richards_super                   | 25.4 ms                                                  | 27.8 ms: 1.09x slower                                                       |
| bench_mp_pool                    | 39.7 ms                                                  | 43.5 ms: 1.10x slower                                                       |
| pickle_pure_python               | 139 us                                                   | 153 us: 1.10x slower                                                        |
| async_tree_eager                 | 45.6 ms                                                  | 50.2 ms: 1.10x slower                                                       |
| pprint_pformat                   | 665 ms                                                   | 741 ms: 1.11x slower                                                        |
| xml_etree_process                | 26.7 ms                                                  | 29.9 ms: 1.12x slower                                                       |
| sympy_expand                     | 167 ms                                                   | 189 ms: 1.13x slower                                                        |
| meteor_contest                   | 47.7 ms                                                  | 54.3 ms: 1.14x slower                                                       |
| 2to3                             | 114 ms                                                   | 130 ms: 1.14x slower                                                        |
| shortest_path                    | 219 ms                                                   | 250 ms: 1.14x slower                                                        |
| regex_compile                    | 54.6 ms                                                  | 64.3 ms: 1.18x slower                                                       |
| connected_components             | 201 ms                                                   | 240 ms: 1.20x slower                                                        |
| telco                            | 2.61 ms                                                  | 3.16 ms: 1.21x slower                                                       |
| mako                             | 4.77 ms                                                  | 5.79 ms: 1.21x slower                                                       |
| scimark_lu                       | 51.3 ms                                                  | 62.6 ms: 1.22x slower                                                       |
| django_template                  | 13.6 ms                                                  | 17.1 ms: 1.25x slower                                                       |
| python_startup                   | 8.01 ms                                                  | 10.1 ms: 1.26x slower                                                       |
| python_startup_no_site           | 5.71 ms                                                  | 7.39 ms: 1.30x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 277 ms: 1.30x slower                                                        |
| many_optionals                   | 195 us                                                   | 258 us: 1.32x slower                                                        |
| bench_thread_pool                | 419 us                                                   | 578 us: 1.38x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 164 ms: 1.46x slower                                                        |
| coverage                         | 26.9 ms                                                  | 40.6 ms: 1.51x slower                                                       |
| async_tree_eager_tg              | 32.1 ms                                                  | 114 ms: 3.56x slower                                                        |
| Geometric mean                   | (ref)                                                    | 1.05x faster                                                                |

Benchmark hidden because not significant (3): fannkuch, chaos, html5lib
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261015-3.16.0a1+dev-fdec4df-NOGIL/bm-20261015-macm4pro-arm64-python-fdec4df45ab69fc25019-3.16.0a1+dev-fdec4df.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.054x faster

# HPT report

- Reliability score: 84.34% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.29x