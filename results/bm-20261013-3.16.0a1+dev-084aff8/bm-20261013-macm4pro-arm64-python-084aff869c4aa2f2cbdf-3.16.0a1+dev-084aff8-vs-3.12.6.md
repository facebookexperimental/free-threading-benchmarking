# Results vs. 3.12.6

- fork: python
- ref: 084aff869c4aa2f2cbdf
- machine: darwin-arm64
- commit hash: 084aff8
- commit date: 2026-10-13
- overall geometric mean: 1.184x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.09x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261013-macm4pro-arm64-python-084aff869c4aa2f2cbdf-3.16.0a1+dev-084aff8 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 116 ms: 1.02x slower                                                        |
| docutils       | 1.02 sec                                                 | 915 ms: 1.12x faster                                                        |
| html5lib       | 23.0 ms                                                  | 20.7 ms: 1.11x faster                                                       |
| sphinx         | 434 ms                                                   | 391 ms: 1.11x faster                                                        |
| Geometric mean | (ref)                                                    | 1.08x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261013-macm4pro-arm64-python-084aff869c4aa2f2cbdf-3.16.0a1+dev-084aff8 |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 265 ms: 1.87x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 282 ms: 1.70x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 273 ms: 1.68x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 277 ms: 1.61x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 112 ms: 1.59x faster                                                        |
| async_tree_none_tg               | 172 ms                                                   | 112 ms: 1.53x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 158 ms: 1.46x faster                                                        |
| async_generators                 | 206 ms                                                   | 143 ms: 1.44x faster                                                        |
| coroutines                       | 13.6 ms                                                  | 9.68 ms: 1.40x faster                                                       |
| async_tree_memoization           | 223 ms                                                   | 162 ms: 1.37x faster                                                        |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 269 ms: 1.24x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 274 ms: 1.23x faster                                                        |
| async_tree_eager_memoization     | 132 ms                                                   | 113 ms: 1.17x faster                                                        |
| async_tree_eager                 | 45.6 ms                                                  | 40.8 ms: 1.12x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                        |
| asyncio_websockets               | 190 ms                                                   | 190 ms: 1.00x faster                                                        |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 252 ms: 1.19x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 142 ms: 1.26x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 94.4 ms: 2.94x slower                                                       |
| Geometric mean                   | (ref)                                                    | 1.22x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261013-macm4pro-arm64-python-084aff869c4aa2f2cbdf-3.16.0a1+dev-084aff8 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.4 ms: 1.38x faster                                                       |
| nbody          | 54.2 ms                                                  | 42.8 ms: 1.27x faster                                                       |
| pidigits       | 161 ms                                                   | 165 ms: 1.02x slower                                                        |
| Geometric mean | (ref)                                                    | 1.20x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261013-macm4pro-arm64-python-084aff869c4aa2f2cbdf-3.16.0a1+dev-084aff8 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.31 ms: 1.27x faster                                                       |
| regex_dna      | 99.6 ms                                                  | 89.8 ms: 1.11x faster                                                       |
| regex_v8       | 9.59 ms                                                  | 9.09 ms: 1.05x faster                                                       |
| Geometric mean | (ref)                                                    | 1.10x faster                                                                |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261013-macm4pro-arm64-python-084aff869c4aa2f2cbdf-3.16.0a1+dev-084aff8 |
|----------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 42.2 ms: 1.22x faster                                                       |
| json_dumps           | 4.26 ms                                                  | 3.57 ms: 1.19x faster                                                       |
| tomli_loads          | 957 ms                                                   | 836 ms: 1.14x faster                                                        |
| unpickle_pure_python | 103 us                                                   | 92.0 us: 1.12x faster                                                       |
| xml_etree_generate   | 38.9 ms                                                  | 35.3 ms: 1.10x faster                                                       |
| xml_etree_process    | 26.7 ms                                                  | 24.9 ms: 1.07x faster                                                       |
| json_loads           | 10.9 us                                                  | 10.4 us: 1.04x faster                                                       |
| xml_etree_parse      | 67.9 ms                                                  | 65.9 ms: 1.03x faster                                                       |
| Geometric mean       | (ref)                                                    | 1.10x faster                                                                |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261013-macm4pro-arm64-python-084aff869c4aa2f2cbdf-3.16.0a1+dev-084aff8 |
|------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.88 ms: 1.11x slower                                                       |
| python_startup_no_site | 5.71 ms                                                  | 6.48 ms: 1.13x slower                                                       |
| Geometric mean         | (ref)                                                    | 1.12x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261013-macm4pro-arm64-python-084aff869c4aa2f2cbdf-3.16.0a1+dev-084aff8 |
|-----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.46 ms: 1.07x faster                                                       |
| django_template | 13.6 ms                                                  | 15.0 ms: 1.10x slower                                                       |
| Geometric mean  | (ref)                                                    | 1.02x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261013-macm4pro-arm64-python-084aff869c4aa2f2cbdf-3.16.0a1+dev-084aff8 |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.02 ms: 5.17x faster                                                       |
| pylint                           | 128 ms                                                   | 52.5 ms: 2.44x faster                                                       |
| mdp                              | 1.09 sec                                                 | 504 ms: 2.17x faster                                                        |
| async_tree_eager_io              | 496 ms                                                   | 265 ms: 1.87x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 282 ms: 1.70x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 273 ms: 1.68x faster                                                        |
| deepcopy                         | 161 us                                                   | 96.2 us: 1.68x faster                                                       |
| async_tree_eager_io_tg           | 446 ms                                                   | 277 ms: 1.61x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 112 ms: 1.59x faster                                                        |
| deepcopy_memo                    | 18.3 us                                                  | 11.8 us: 1.55x faster                                                       |
| async_tree_none_tg               | 172 ms                                                   | 112 ms: 1.53x faster                                                        |
| comprehensions                   | 9.84 us                                                  | 6.67 us: 1.47x faster                                                       |
| async_tree_memoization_tg        | 231 ms                                                   | 158 ms: 1.46x faster                                                        |
| typing_runtime_protocols         | 71.0 us                                                  | 48.7 us: 1.46x faster                                                       |
| async_generators                 | 206 ms                                                   | 143 ms: 1.44x faster                                                        |
| coroutines                       | 13.6 ms                                                  | 9.68 ms: 1.40x faster                                                       |
| deepcopy_reduce                  | 1.46 us                                                  | 1.05 us: 1.39x faster                                                       |
| float                            | 37.9 ms                                                  | 27.4 ms: 1.38x faster                                                       |
| async_tree_memoization           | 223 ms                                                   | 162 ms: 1.37x faster                                                        |
| go                               | 70.0 ms                                                  | 52.2 ms: 1.34x faster                                                       |
| spectral_norm                    | 54.4 ms                                                  | 41.1 ms: 1.32x faster                                                       |
| create_gc_cycles                 | 830 us                                                   | 635 us: 1.31x faster                                                        |
| generators                       | 21.9 ms                                                  | 17.1 ms: 1.28x faster                                                       |
| raytrace                         | 145 ms                                                   | 113 ms: 1.28x faster                                                        |
| regex_effbot                     | 1.67 ms                                                  | 1.31 ms: 1.27x faster                                                       |
| scimark_fft                      | 142 ms                                                   | 112 ms: 1.27x faster                                                        |
| nbody                            | 54.2 ms                                                  | 42.8 ms: 1.27x faster                                                       |
| nqueens                          | 43.5 ms                                                  | 34.9 ms: 1.25x faster                                                       |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 269 ms: 1.24x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 274 ms: 1.23x faster                                                        |
| scimark_sor                      | 61.0 ms                                                  | 49.5 ms: 1.23x faster                                                       |
| xml_etree_iterparse              | 51.6 ms                                                  | 42.2 ms: 1.22x faster                                                       |
| deltablue                        | 1.73 ms                                                  | 1.42 ms: 1.21x faster                                                       |
| logging_silent                   | 50.9 ns                                                  | 42.3 ns: 1.20x faster                                                       |
| logging_simple                   | 2.57 us                                                  | 2.14 us: 1.20x faster                                                       |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.73 ms: 1.20x faster                                                       |
| scimark_monte_carlo              | 32.2 ms                                                  | 26.9 ms: 1.20x faster                                                       |
| logging_format                   | 2.80 us                                                  | 2.34 us: 1.20x faster                                                       |
| json_dumps                       | 4.26 ms                                                  | 3.57 ms: 1.19x faster                                                       |
| dulwich_log                      | 21.3 ms                                                  | 17.9 ms: 1.18x faster                                                       |
| pyflate                          | 216 ms                                                   | 183 ms: 1.18x faster                                                        |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.91 sec: 1.17x faster                                                      |
| pathlib                          | 12.4 ms                                                  | 10.6 ms: 1.17x faster                                                       |
| async_tree_eager_memoization     | 132 ms                                                   | 113 ms: 1.17x faster                                                        |
| chaos                            | 28.9 ms                                                  | 24.8 ms: 1.17x faster                                                       |
| k_core                           | 1.12 sec                                                 | 971 ms: 1.15x faster                                                        |
| hexiom                           | 3.04 ms                                                  | 2.64 ms: 1.15x faster                                                       |
| tomli_loads                      | 957 ms                                                   | 836 ms: 1.14x faster                                                        |
| gc_traversal                     | 2.01 ms                                                  | 1.78 ms: 1.13x faster                                                       |
| scimark_lu                       | 51.3 ms                                                  | 45.7 ms: 1.12x faster                                                       |
| unpickle_pure_python             | 103 us                                                   | 92.0 us: 1.12x faster                                                       |
| docutils                         | 1.02 sec                                                 | 915 ms: 1.12x faster                                                        |
| async_tree_eager                 | 45.6 ms                                                  | 40.8 ms: 1.12x faster                                                       |
| html5lib                         | 23.0 ms                                                  | 20.7 ms: 1.11x faster                                                       |
| richards                         | 22.4 ms                                                  | 20.2 ms: 1.11x faster                                                       |
| regex_dna                        | 99.6 ms                                                  | 89.8 ms: 1.11x faster                                                       |
| sphinx                           | 434 ms                                                   | 391 ms: 1.11x faster                                                        |
| xml_etree_generate               | 38.9 ms                                                  | 35.3 ms: 1.10x faster                                                       |
| richards_super                   | 25.4 ms                                                  | 23.0 ms: 1.10x faster                                                       |
| fannkuch                         | 176 ms                                                   | 160 ms: 1.10x faster                                                        |
| sympy_integrate                  | 8.02 ms                                                  | 7.38 ms: 1.09x faster                                                       |
| xml_etree_process                | 26.7 ms                                                  | 24.9 ms: 1.07x faster                                                       |
| mako                             | 4.77 ms                                                  | 4.46 ms: 1.07x faster                                                       |
| thrift                           | 322 us                                                   | 305 us: 1.06x faster                                                        |
| regex_v8                         | 9.59 ms                                                  | 9.09 ms: 1.05x faster                                                       |
| pycparser                        | 497 ms                                                   | 472 ms: 1.05x faster                                                        |
| sqlite_synth                     | 967 ns                                                   | 920 ns: 1.05x faster                                                        |
| sympy_str                        | 104 ms                                                   | 99.2 ms: 1.05x faster                                                       |
| crypto_pyaes                     | 38.8 ms                                                  | 37.0 ms: 1.05x faster                                                       |
| pprint_safe_repr                 | 328 ms                                                   | 313 ms: 1.05x faster                                                        |
| sympy_sum                        | 57.6 ms                                                  | 55.1 ms: 1.04x faster                                                       |
| json_loads                       | 10.9 us                                                  | 10.4 us: 1.04x faster                                                       |
| pprint_pformat                   | 665 ms                                                   | 638 ms: 1.04x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                        |
| json                             | 1.93 ms                                                  | 1.86 ms: 1.04x faster                                                       |
| xml_etree_parse                  | 67.9 ms                                                  | 65.9 ms: 1.03x faster                                                       |
| bench_thread_pool                | 419 us                                                   | 407 us: 1.03x faster                                                        |
| asyncio_websockets               | 190 ms                                                   | 190 ms: 1.00x faster                                                        |
| sympy_expand                     | 167 ms                                                   | 168 ms: 1.01x slower                                                        |
| 2to3                             | 114 ms                                                   | 116 ms: 1.02x slower                                                        |
| shortest_path                    | 219 ms                                                   | 223 ms: 1.02x slower                                                        |
| pidigits                         | 161 ms                                                   | 165 ms: 1.02x slower                                                        |
| meteor_contest                   | 47.7 ms                                                  | 49.0 ms: 1.03x slower                                                       |
| connected_components             | 201 ms                                                   | 207 ms: 1.03x slower                                                        |
| django_template                  | 13.6 ms                                                  | 15.0 ms: 1.10x slower                                                       |
| python_startup                   | 8.01 ms                                                  | 8.88 ms: 1.11x slower                                                       |
| telco                            | 2.61 ms                                                  | 2.89 ms: 1.11x slower                                                       |
| bench_mp_pool                    | 39.7 ms                                                  | 44.0 ms: 1.11x slower                                                       |
| python_startup_no_site           | 5.71 ms                                                  | 6.48 ms: 1.13x slower                                                       |
| many_optionals                   | 195 us                                                   | 231 us: 1.18x slower                                                        |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 252 ms: 1.19x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 142 ms: 1.26x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 94.4 ms: 2.94x slower                                                       |
| Geometric mean                   | (ref)                                                    | 1.18x faster                                                                |

Benchmark hidden because not significant (2): pickle_pure_python, regex_compile
Ignored benchmarks (14) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261013-3.16.0a1+dev-084aff8/bm-20261013-macm4pro-arm64-python-084aff869c4aa2f2cbdf-3.16.0a1+dev-084aff8.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.184x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.11x
- 95% likely to have a speedup of 1.11x
- 99% likely to have a speedup of 1.09x

# Memory
- memory change: 1.18x