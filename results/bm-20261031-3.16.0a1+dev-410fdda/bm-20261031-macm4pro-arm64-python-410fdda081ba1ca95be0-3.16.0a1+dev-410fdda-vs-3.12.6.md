# Results vs. 3.12.6

- fork: python
- ref: 410fdda081ba1ca95be0
- machine: darwin-arm64
- commit hash: 410fdda
- commit date: 2026-10-31
- overall geometric mean: 1.215x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.12x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 112 ms: 1.02x faster                                                        |
| docutils       | 1.02 sec                                                 | 885 ms: 1.15x faster                                                        |
| html5lib       | 23.0 ms                                                  | 20.1 ms: 1.15x faster                                                       |
| sphinx         | 434 ms                                                   | 381 ms: 1.14x faster                                                        |
| Geometric mean | (ref)                                                    | 1.11x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_generators                 | 206 ms                                                   | 98.2 ms: 2.10x faster                                                       |
| async_tree_eager_io              | 496 ms                                                   | 262 ms: 1.89x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 274 ms: 1.75x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 267 ms: 1.72x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 108 ms: 1.65x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 276 ms: 1.61x faster                                                        |
| async_tree_none_tg               | 172 ms                                                   | 109 ms: 1.58x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 155 ms: 1.49x faster                                                        |
| coroutines                       | 13.6 ms                                                  | 9.59 ms: 1.41x faster                                                       |
| async_tree_memoization           | 223 ms                                                   | 159 ms: 1.40x faster                                                        |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 261 ms: 1.28x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 267 ms: 1.27x faster                                                        |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                        |
| async_tree_eager                 | 45.6 ms                                                  | 40.1 ms: 1.14x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 216 ms: 1.07x faster                                                        |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                        |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 244 ms: 1.15x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 140 ms: 1.24x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 91.8 ms: 2.86x slower                                                       |
| Geometric mean                   | (ref)                                                    | 1.27x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.0 ms: 1.40x faster                                                       |
| nbody          | 54.2 ms                                                  | 42.8 ms: 1.27x faster                                                       |
| pidigits       | 161 ms                                                   | 158 ms: 1.02x faster                                                        |
| Geometric mean | (ref)                                                    | 1.22x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.29 ms: 1.29x faster                                                       |
| regex_dna      | 99.6 ms                                                  | 87.6 ms: 1.14x faster                                                       |
| regex_v8       | 9.59 ms                                                  | 8.99 ms: 1.07x faster                                                       |
| regex_compile  | 54.6 ms                                                  | 52.9 ms: 1.03x faster                                                       |
| Geometric mean | (ref)                                                    | 1.13x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.6 ms: 1.27x faster                                                       |
| tomli_loads          | 957 ms                                                   | 785 ms: 1.22x faster                                                        |
| json_dumps           | 4.26 ms                                                  | 3.53 ms: 1.21x faster                                                       |
| unpickle_pure_python | 103 us                                                   | 89.9 us: 1.14x faster                                                       |
| xml_etree_generate   | 38.9 ms                                                  | 34.6 ms: 1.12x faster                                                       |
| xml_etree_process    | 26.7 ms                                                  | 24.5 ms: 1.09x faster                                                       |
| xml_etree_parse      | 67.9 ms                                                  | 62.7 ms: 1.08x faster                                                       |
| json_loads           | 10.9 us                                                  | 10.3 us: 1.06x faster                                                       |
| pickle_pure_python   | 139 us                                                   | 136 us: 1.02x faster                                                        |
| Geometric mean       | (ref)                                                    | 1.13x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.13 ms: 1.01x slower                                                       |
| python_startup_no_site | 5.71 ms                                                  | 6.33 ms: 1.11x slower                                                       |
| Geometric mean         | (ref)                                                    | 1.06x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|-----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.37 ms: 1.09x faster                                                       |
| django_template | 13.6 ms                                                  | 14.6 ms: 1.07x slower                                                       |
| Geometric mean  | (ref)                                                    | 1.01x faster                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.90 ms: 5.33x faster                                                       |
| pylint                           | 128 ms                                                   | 49.8 ms: 2.57x faster                                                       |
| mdp                              | 1.09 sec                                                 | 499 ms: 2.19x faster                                                        |
| async_generators                 | 206 ms                                                   | 98.2 ms: 2.10x faster                                                       |
| async_tree_eager_io              | 496 ms                                                   | 262 ms: 1.89x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 274 ms: 1.75x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 267 ms: 1.72x faster                                                        |
| deepcopy                         | 161 us                                                   | 93.7 us: 1.72x faster                                                       |
| async_tree_none                  | 178 ms                                                   | 108 ms: 1.65x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 276 ms: 1.61x faster                                                        |
| deepcopy_memo                    | 18.3 us                                                  | 11.5 us: 1.59x faster                                                       |
| async_tree_none_tg               | 172 ms                                                   | 109 ms: 1.58x faster                                                        |
| typing_runtime_protocols         | 71.0 us                                                  | 45.5 us: 1.56x faster                                                       |
| comprehensions                   | 9.84 us                                                  | 6.51 us: 1.51x faster                                                       |
| async_tree_memoization_tg        | 231 ms                                                   | 155 ms: 1.49x faster                                                        |
| deepcopy_reduce                  | 1.46 us                                                  | 1.03 us: 1.42x faster                                                       |
| coroutines                       | 13.6 ms                                                  | 9.59 ms: 1.41x faster                                                       |
| float                            | 37.9 ms                                                  | 27.0 ms: 1.40x faster                                                       |
| async_tree_memoization           | 223 ms                                                   | 159 ms: 1.40x faster                                                        |
| go                               | 70.0 ms                                                  | 51.0 ms: 1.37x faster                                                       |
| create_gc_cycles                 | 830 us                                                   | 610 us: 1.36x faster                                                        |
| spectral_norm                    | 54.4 ms                                                  | 41.3 ms: 1.32x faster                                                       |
| generators                       | 21.9 ms                                                  | 16.8 ms: 1.30x faster                                                       |
| raytrace                         | 145 ms                                                   | 112 ms: 1.30x faster                                                        |
| regex_effbot                     | 1.67 ms                                                  | 1.29 ms: 1.29x faster                                                       |
| scimark_fft                      | 142 ms                                                   | 111 ms: 1.28x faster                                                        |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 261 ms: 1.28x faster                                                        |
| scimark_sor                      | 61.0 ms                                                  | 47.7 ms: 1.28x faster                                                       |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.6 ms: 1.27x faster                                                       |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 267 ms: 1.27x faster                                                        |
| nqueens                          | 43.5 ms                                                  | 34.3 ms: 1.27x faster                                                       |
| nbody                            | 54.2 ms                                                  | 42.8 ms: 1.27x faster                                                       |
| logging_silent                   | 50.9 ns                                                  | 41.3 ns: 1.23x faster                                                       |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.70 ms: 1.22x faster                                                       |
| tomli_loads                      | 957 ms                                                   | 785 ms: 1.22x faster                                                        |
| scimark_monte_carlo              | 32.2 ms                                                  | 26.5 ms: 1.22x faster                                                       |
| deltablue                        | 1.73 ms                                                  | 1.42 ms: 1.21x faster                                                       |
| dulwich_log                      | 21.3 ms                                                  | 17.6 ms: 1.21x faster                                                       |
| json_dumps                       | 4.26 ms                                                  | 3.53 ms: 1.21x faster                                                       |
| pyflate                          | 216 ms                                                   | 180 ms: 1.20x faster                                                        |
| logging_simple                   | 2.57 us                                                  | 2.15 us: 1.19x faster                                                       |
| pathlib                          | 12.4 ms                                                  | 10.4 ms: 1.19x faster                                                       |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                        |
| chaos                            | 28.9 ms                                                  | 24.4 ms: 1.19x faster                                                       |
| logging_format                   | 2.80 us                                                  | 2.37 us: 1.18x faster                                                       |
| hexiom                           | 3.04 ms                                                  | 2.58 ms: 1.18x faster                                                       |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.91 sec: 1.17x faster                                                      |
| gc_traversal                     | 2.01 ms                                                  | 1.72 ms: 1.17x faster                                                       |
| k_core                           | 1.12 sec                                                 | 964 ms: 1.16x faster                                                        |
| docutils                         | 1.02 sec                                                 | 885 ms: 1.15x faster                                                        |
| html5lib                         | 23.0 ms                                                  | 20.1 ms: 1.15x faster                                                       |
| unpickle_pure_python             | 103 us                                                   | 89.9 us: 1.14x faster                                                       |
| scimark_lu                       | 51.3 ms                                                  | 45.0 ms: 1.14x faster                                                       |
| sphinx                           | 434 ms                                                   | 381 ms: 1.14x faster                                                        |
| regex_dna                        | 99.6 ms                                                  | 87.6 ms: 1.14x faster                                                       |
| async_tree_eager                 | 45.6 ms                                                  | 40.1 ms: 1.14x faster                                                       |
| xml_etree_generate               | 38.9 ms                                                  | 34.6 ms: 1.12x faster                                                       |
| richards_super                   | 25.4 ms                                                  | 22.6 ms: 1.12x faster                                                       |
| fannkuch                         | 176 ms                                                   | 157 ms: 1.12x faster                                                        |
| richards                         | 22.4 ms                                                  | 20.0 ms: 1.12x faster                                                       |
| sympy_integrate                  | 8.02 ms                                                  | 7.18 ms: 1.12x faster                                                       |
| mako                             | 4.77 ms                                                  | 4.37 ms: 1.09x faster                                                       |
| xml_etree_process                | 26.7 ms                                                  | 24.5 ms: 1.09x faster                                                       |
| thrift                           | 322 us                                                   | 296 us: 1.09x faster                                                        |
| pycparser                        | 497 ms                                                   | 459 ms: 1.08x faster                                                        |
| xml_etree_parse                  | 67.9 ms                                                  | 62.7 ms: 1.08x faster                                                       |
| crypto_pyaes                     | 38.8 ms                                                  | 36.0 ms: 1.08x faster                                                       |
| sympy_sum                        | 57.6 ms                                                  | 53.5 ms: 1.08x faster                                                       |
| pprint_safe_repr                 | 328 ms                                                   | 305 ms: 1.08x faster                                                        |
| pprint_pformat                   | 665 ms                                                   | 619 ms: 1.07x faster                                                        |
| sqlite_synth                     | 967 ns                                                   | 901 ns: 1.07x faster                                                        |
| sympy_str                        | 104 ms                                                   | 97.2 ms: 1.07x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 216 ms: 1.07x faster                                                        |
| regex_v8                         | 9.59 ms                                                  | 8.99 ms: 1.07x faster                                                       |
| json                             | 1.93 ms                                                  | 1.82 ms: 1.06x faster                                                       |
| json_loads                       | 10.9 us                                                  | 10.3 us: 1.06x faster                                                       |
| regex_compile                    | 54.6 ms                                                  | 52.9 ms: 1.03x faster                                                       |
| bench_thread_pool                | 419 us                                                   | 409 us: 1.02x faster                                                        |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                        |
| pickle_pure_python               | 139 us                                                   | 136 us: 1.02x faster                                                        |
| pidigits                         | 161 ms                                                   | 158 ms: 1.02x faster                                                        |
| 2to3                             | 114 ms                                                   | 112 ms: 1.02x faster                                                        |
| sympy_expand                     | 167 ms                                                   | 166 ms: 1.01x faster                                                        |
| meteor_contest                   | 47.7 ms                                                  | 47.5 ms: 1.01x faster                                                       |
| python_startup                   | 8.01 ms                                                  | 8.13 ms: 1.01x slower                                                       |
| shortest_path                    | 219 ms                                                   | 225 ms: 1.03x slower                                                        |
| connected_components             | 201 ms                                                   | 209 ms: 1.04x slower                                                        |
| telco                            | 2.61 ms                                                  | 2.78 ms: 1.07x slower                                                       |
| bench_mp_pool                    | 39.7 ms                                                  | 42.3 ms: 1.07x slower                                                       |
| django_template                  | 13.6 ms                                                  | 14.6 ms: 1.07x slower                                                       |
| python_startup_no_site           | 5.71 ms                                                  | 6.33 ms: 1.11x slower                                                       |
| many_optionals                   | 195 us                                                   | 224 us: 1.15x slower                                                        |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 244 ms: 1.15x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 140 ms: 1.24x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 91.8 ms: 2.86x slower                                                       |
| Geometric mean                   | (ref)                                                    | 1.21x faster                                                                |
Ignored benchmarks (14) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261031-3.16.0a1+dev-410fdda/bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1+dev-410fdda.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.215x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.14x
- 95% likely to have a speedup of 1.13x
- 99% likely to have a speedup of 1.12x

# Memory
- memory change: 1.15x