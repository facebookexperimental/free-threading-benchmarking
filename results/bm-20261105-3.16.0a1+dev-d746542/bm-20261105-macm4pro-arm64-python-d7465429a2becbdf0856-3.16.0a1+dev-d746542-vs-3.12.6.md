# Results vs. 3.12.6

- fork: python
- ref: d7465429a2becbdf0856
- machine: darwin-arm64
- commit hash: d746542
- commit date: 2026-11-05
- overall geometric mean: 1.206x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261105-macm4pro-arm64-python-d7465429a2becbdf0856-3.16.0a1+dev-d746542 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 111 ms: 1.03x faster                                                        |
| docutils       | 1.02 sec                                                 | 894 ms: 1.14x faster                                                        |
| html5lib       | 23.0 ms                                                  | 20.3 ms: 1.14x faster                                                       |
| sphinx         | 434 ms                                                   | 386 ms: 1.12x faster                                                        |
| Geometric mean | (ref)                                                    | 1.11x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261105-macm4pro-arm64-python-d7465429a2becbdf0856-3.16.0a1+dev-d746542 |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_generators                 | 206 ms                                                   | 97.3 ms: 2.12x faster                                                       |
| async_tree_eager_io              | 496 ms                                                   | 260 ms: 1.91x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 275 ms: 1.75x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 268 ms: 1.71x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 109 ms: 1.64x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 275 ms: 1.62x faster                                                        |
| async_tree_none_tg               | 172 ms                                                   | 111 ms: 1.55x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 157 ms: 1.47x faster                                                        |
| async_tree_memoization           | 223 ms                                                   | 160 ms: 1.39x faster                                                        |
| coroutines                       | 13.6 ms                                                  | 9.75 ms: 1.39x faster                                                       |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 260 ms: 1.28x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 267 ms: 1.27x faster                                                        |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.18x faster                                                        |
| async_tree_eager                 | 45.6 ms                                                  | 40.1 ms: 1.13x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 215 ms: 1.07x faster                                                        |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                        |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 244 ms: 1.15x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 140 ms: 1.24x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 92.4 ms: 2.88x slower                                                       |
| Geometric mean                   | (ref)                                                    | 1.26x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261105-macm4pro-arm64-python-d7465429a2becbdf0856-3.16.0a1+dev-d746542 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.3 ms: 1.39x faster                                                       |
| nbody          | 54.2 ms                                                  | 43.4 ms: 1.25x faster                                                       |
| pidigits       | 161 ms                                                   | 148 ms: 1.09x faster                                                        |
| Geometric mean | (ref)                                                    | 1.24x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261105-macm4pro-arm64-python-d7465429a2becbdf0856-3.16.0a1+dev-d746542 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.35 ms: 1.23x faster                                                       |
| regex_dna      | 99.6 ms                                                  | 91.7 ms: 1.09x faster                                                       |
| regex_v8       | 9.59 ms                                                  | 9.36 ms: 1.02x faster                                                       |
| regex_compile  | 54.6 ms                                                  | 53.5 ms: 1.02x faster                                                       |
| Geometric mean | (ref)                                                    | 1.09x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261105-macm4pro-arm64-python-d7465429a2becbdf0856-3.16.0a1+dev-d746542 |
|----------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.8 ms: 1.26x faster                                                       |
| json_dumps           | 4.26 ms                                                  | 3.54 ms: 1.20x faster                                                       |
| tomli_loads          | 957 ms                                                   | 798 ms: 1.20x faster                                                        |
| xml_etree_generate   | 38.9 ms                                                  | 34.8 ms: 1.12x faster                                                       |
| unpickle_pure_python | 103 us                                                   | 93.2 us: 1.10x faster                                                       |
| xml_etree_parse      | 67.9 ms                                                  | 61.8 ms: 1.10x faster                                                       |
| xml_etree_process    | 26.7 ms                                                  | 24.8 ms: 1.08x faster                                                       |
| json_loads           | 10.9 us                                                  | 10.3 us: 1.05x faster                                                       |
| pickle_pure_python   | 139 us                                                   | 139 us: 1.01x faster                                                        |
| Geometric mean       | (ref)                                                    | 1.12x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261105-macm4pro-arm64-python-d7465429a2becbdf0856-3.16.0a1+dev-d746542 |
|------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.23 ms: 1.03x slower                                                       |
| python_startup_no_site | 5.71 ms                                                  | 6.36 ms: 1.12x slower                                                       |
| Geometric mean         | (ref)                                                    | 1.07x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261105-macm4pro-arm64-python-d7465429a2becbdf0856-3.16.0a1+dev-d746542 |
|-----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.38 ms: 1.09x faster                                                       |
| django_template | 13.6 ms                                                  | 14.4 ms: 1.06x slower                                                       |
| Geometric mean  | (ref)                                                    | 1.01x faster                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261105-macm4pro-arm64-python-d7465429a2becbdf0856-3.16.0a1+dev-d746542 |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.87 ms: 5.36x faster                                                       |
| pylint                           | 128 ms                                                   | 51.3 ms: 2.50x faster                                                       |
| mdp                              | 1.09 sec                                                 | 500 ms: 2.18x faster                                                        |
| async_generators                 | 206 ms                                                   | 97.3 ms: 2.12x faster                                                       |
| async_tree_eager_io              | 496 ms                                                   | 260 ms: 1.91x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 275 ms: 1.75x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 268 ms: 1.71x faster                                                        |
| deepcopy                         | 161 us                                                   | 95.4 us: 1.69x faster                                                       |
| async_tree_none                  | 178 ms                                                   | 109 ms: 1.64x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 275 ms: 1.62x faster                                                        |
| deepcopy_memo                    | 18.3 us                                                  | 11.4 us: 1.60x faster                                                       |
| async_tree_none_tg               | 172 ms                                                   | 111 ms: 1.55x faster                                                        |
| typing_runtime_protocols         | 71.0 us                                                  | 46.0 us: 1.54x faster                                                       |
| comprehensions                   | 9.84 us                                                  | 6.54 us: 1.50x faster                                                       |
| async_tree_memoization_tg        | 231 ms                                                   | 157 ms: 1.47x faster                                                        |
| deepcopy_reduce                  | 1.46 us                                                  | 1.04 us: 1.41x faster                                                       |
| async_tree_memoization           | 223 ms                                                   | 160 ms: 1.39x faster                                                        |
| coroutines                       | 13.6 ms                                                  | 9.75 ms: 1.39x faster                                                       |
| float                            | 37.9 ms                                                  | 27.3 ms: 1.39x faster                                                       |
| go                               | 70.0 ms                                                  | 51.4 ms: 1.36x faster                                                       |
| create_gc_cycles                 | 830 us                                                   | 616 us: 1.35x faster                                                        |
| spectral_norm                    | 54.4 ms                                                  | 41.4 ms: 1.31x faster                                                       |
| generators                       | 21.9 ms                                                  | 16.8 ms: 1.30x faster                                                       |
| raytrace                         | 145 ms                                                   | 113 ms: 1.29x faster                                                        |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 260 ms: 1.28x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 267 ms: 1.27x faster                                                        |
| scimark_fft                      | 142 ms                                                   | 112 ms: 1.26x faster                                                        |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.8 ms: 1.26x faster                                                       |
| nqueens                          | 43.5 ms                                                  | 34.6 ms: 1.26x faster                                                       |
| nbody                            | 54.2 ms                                                  | 43.4 ms: 1.25x faster                                                       |
| scimark_sor                      | 61.0 ms                                                  | 49.3 ms: 1.24x faster                                                       |
| regex_effbot                     | 1.67 ms                                                  | 1.35 ms: 1.23x faster                                                       |
| logging_silent                   | 50.9 ns                                                  | 41.5 ns: 1.23x faster                                                       |
| scimark_monte_carlo              | 32.2 ms                                                  | 26.3 ms: 1.22x faster                                                       |
| deltablue                        | 1.73 ms                                                  | 1.42 ms: 1.21x faster                                                       |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.85 sec: 1.21x faster                                                      |
| dulwich_log                      | 21.3 ms                                                  | 17.5 ms: 1.21x faster                                                       |
| json_dumps                       | 4.26 ms                                                  | 3.54 ms: 1.20x faster                                                       |
| tomli_loads                      | 957 ms                                                   | 798 ms: 1.20x faster                                                        |
| logging_simple                   | 2.57 us                                                  | 2.16 us: 1.19x faster                                                       |
| pyflate                          | 216 ms                                                   | 182 ms: 1.19x faster                                                        |
| chaos                            | 28.9 ms                                                  | 24.4 ms: 1.19x faster                                                       |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.18x faster                                                        |
| logging_format                   | 2.80 us                                                  | 2.37 us: 1.18x faster                                                       |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.77 ms: 1.18x faster                                                       |
| hexiom                           | 3.04 ms                                                  | 2.59 ms: 1.17x faster                                                       |
| pathlib                          | 12.4 ms                                                  | 10.6 ms: 1.16x faster                                                       |
| gc_traversal                     | 2.01 ms                                                  | 1.74 ms: 1.16x faster                                                       |
| k_core                           | 1.12 sec                                                 | 971 ms: 1.15x faster                                                        |
| docutils                         | 1.02 sec                                                 | 894 ms: 1.14x faster                                                        |
| html5lib                         | 23.0 ms                                                  | 20.3 ms: 1.14x faster                                                       |
| async_tree_eager                 | 45.6 ms                                                  | 40.1 ms: 1.13x faster                                                       |
| richards                         | 22.4 ms                                                  | 19.9 ms: 1.13x faster                                                       |
| sphinx                           | 434 ms                                                   | 386 ms: 1.12x faster                                                        |
| xml_etree_generate               | 38.9 ms                                                  | 34.8 ms: 1.12x faster                                                       |
| richards_super                   | 25.4 ms                                                  | 22.7 ms: 1.12x faster                                                       |
| fannkuch                         | 176 ms                                                   | 158 ms: 1.11x faster                                                        |
| sympy_integrate                  | 8.02 ms                                                  | 7.26 ms: 1.11x faster                                                       |
| unpickle_pure_python             | 103 us                                                   | 93.2 us: 1.10x faster                                                       |
| xml_etree_parse                  | 67.9 ms                                                  | 61.8 ms: 1.10x faster                                                       |
| scimark_lu                       | 51.3 ms                                                  | 46.8 ms: 1.10x faster                                                       |
| mako                             | 4.77 ms                                                  | 4.38 ms: 1.09x faster                                                       |
| pidigits                         | 161 ms                                                   | 148 ms: 1.09x faster                                                        |
| regex_dna                        | 99.6 ms                                                  | 91.7 ms: 1.09x faster                                                       |
| xml_etree_process                | 26.7 ms                                                  | 24.8 ms: 1.08x faster                                                       |
| crypto_pyaes                     | 38.8 ms                                                  | 36.0 ms: 1.08x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 215 ms: 1.07x faster                                                        |
| thrift                           | 322 us                                                   | 300 us: 1.07x faster                                                        |
| pprint_safe_repr                 | 328 ms                                                   | 307 ms: 1.07x faster                                                        |
| sympy_str                        | 104 ms                                                   | 97.8 ms: 1.07x faster                                                       |
| pycparser                        | 497 ms                                                   | 468 ms: 1.06x faster                                                        |
| sqlite_synth                     | 967 ns                                                   | 915 ns: 1.06x faster                                                        |
| sympy_sum                        | 57.6 ms                                                  | 54.6 ms: 1.06x faster                                                       |
| pprint_pformat                   | 665 ms                                                   | 632 ms: 1.05x faster                                                        |
| json_loads                       | 10.9 us                                                  | 10.3 us: 1.05x faster                                                       |
| json                             | 1.93 ms                                                  | 1.85 ms: 1.05x faster                                                       |
| 2to3                             | 114 ms                                                   | 111 ms: 1.03x faster                                                        |
| regex_v8                         | 9.59 ms                                                  | 9.36 ms: 1.02x faster                                                       |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                        |
| regex_compile                    | 54.6 ms                                                  | 53.5 ms: 1.02x faster                                                       |
| bench_thread_pool                | 419 us                                                   | 411 us: 1.02x faster                                                        |
| pickle_pure_python               | 139 us                                                   | 139 us: 1.01x faster                                                        |
| sympy_expand                     | 167 ms                                                   | 166 ms: 1.00x faster                                                        |
| meteor_contest                   | 47.7 ms                                                  | 48.4 ms: 1.01x slower                                                       |
| shortest_path                    | 219 ms                                                   | 224 ms: 1.03x slower                                                        |
| python_startup                   | 8.01 ms                                                  | 8.23 ms: 1.03x slower                                                       |
| connected_components             | 201 ms                                                   | 207 ms: 1.03x slower                                                        |
| bench_mp_pool                    | 39.7 ms                                                  | 41.1 ms: 1.03x slower                                                       |
| django_template                  | 13.6 ms                                                  | 14.4 ms: 1.06x slower                                                       |
| telco                            | 2.61 ms                                                  | 2.80 ms: 1.07x slower                                                       |
| python_startup_no_site           | 5.71 ms                                                  | 6.36 ms: 1.12x slower                                                       |
| many_optionals                   | 195 us                                                   | 223 us: 1.14x slower                                                        |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 244 ms: 1.15x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 140 ms: 1.24x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 92.4 ms: 2.88x slower                                                       |
| Geometric mean                   | (ref)                                                    | 1.20x faster                                                                |
Ignored benchmarks (14) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261105-3.16.0a1+dev-d746542/bm-20261105-macm4pro-arm64-python-d7465429a2becbdf0856-3.16.0a1+dev-d746542.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.206x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.13x
- 95% likely to have a speedup of 1.12x
- 99% likely to have a speedup of 1.11x

# Memory
- memory change: 1.15x