# Results vs. 3.12.6

- fork: python
- ref: v3.14.0a6
- machine: darwin-arm64
- commit hash: 77b2c93
- commit date: 2025-03-14
- overall geometric mean: 1.063x faster
- HPT reliability: 99.55%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 114 ms: 1.00x slower                                         |
| docutils       | 1.02 sec                                                 | 1.07 sec: 1.05x slower                                       |
| sphinx         | 434 ms                                                   | 421 ms: 1.03x faster                                         |
| Geometric mean | (ref)                                                    | 1.00x slower                                                 |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 260 ms: 1.90x faster                                         |
| async_tree_io_tg                 | 480 ms                                                   | 266 ms: 1.81x faster                                         |
| async_tree_io                    | 459 ms                                                   | 266 ms: 1.72x faster                                         |
| async_tree_eager_io_tg           | 446 ms                                                   | 268 ms: 1.66x faster                                         |
| async_tree_none_tg               | 172 ms                                                   | 112 ms: 1.54x faster                                         |
| async_tree_none                  | 178 ms                                                   | 117 ms: 1.53x faster                                         |
| async_tree_memoization_tg        | 231 ms                                                   | 155 ms: 1.49x faster                                         |
| async_tree_memoization           | 223 ms                                                   | 155 ms: 1.43x faster                                         |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 270 ms: 1.25x faster                                         |
| coroutines                       | 13.6 ms                                                  | 10.9 ms: 1.25x faster                                        |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 270 ms: 1.23x faster                                         |
| async_generators                 | 206 ms                                                   | 179 ms: 1.16x faster                                         |
| async_tree_eager_memoization     | 132 ms                                                   | 117 ms: 1.13x faster                                         |
| async_tree_eager                 | 45.6 ms                                                  | 43.8 ms: 1.04x faster                                        |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.03x faster                                         |
| asyncio_websockets               | 190 ms                                                   | 194 ms: 1.02x slower                                         |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 252 ms: 1.19x slower                                         |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 139 ms: 1.23x slower                                         |
| async_tree_eager_tg              | 32.1 ms                                                  | 91.8 ms: 2.86x slower                                        |
| Geometric mean                   | (ref)                                                    | 1.20x faster                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 33.0 ms: 1.15x faster                                        |
| nbody          | 54.2 ms                                                  | 51.0 ms: 1.06x faster                                        |
| pidigits       | 161 ms                                                   | 163 ms: 1.01x slower                                         |
| Geometric mean | (ref)                                                    | 1.06x faster                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                        |
| regex_compile  | 54.6 ms                                                  | 49.0 ms: 1.11x faster                                        |
| regex_dna      | 99.6 ms                                                  | 92.8 ms: 1.07x faster                                        |
| regex_v8       | 9.59 ms                                                  | 10.9 ms: 1.14x slower                                        |
| Geometric mean | (ref)                                                    | 1.05x faster                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------:|
| tomli_loads          | 957 ms                                                   | 862 ms: 1.11x faster                                         |
| xml_etree_iterparse  | 51.6 ms                                                  | 46.6 ms: 1.11x faster                                        |
| xml_etree_parse      | 67.9 ms                                                  | 62.2 ms: 1.09x faster                                        |
| xml_etree_generate   | 38.9 ms                                                  | 37.3 ms: 1.04x faster                                        |
| xml_etree_process    | 26.7 ms                                                  | 27.1 ms: 1.01x slower                                        |
| unpickle_pure_python | 103 us                                                   | 105 us: 1.02x slower                                         |
| json_loads           | 10.9 us                                                  | 11.5 us: 1.06x slower                                        |
| pickle_pure_python   | 139 us                                                   | 148 us: 1.06x slower                                         |
| json_dumps           | 4.26 ms                                                  | 5.06 ms: 1.19x slower                                        |
| Geometric mean       | (ref)                                                    | 1.00x faster                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.66 ms: 1.08x slower                                        |
| python_startup_no_site | 5.71 ms                                                  | 6.42 ms: 1.13x slower                                        |
| Geometric mean         | (ref)                                                    | 1.10x slower                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.82 ms: 1.01x slower                                        |
| genshi_text     | 10.5 ms                                                  | 10.6 ms: 1.01x slower                                        |
| django_template | 13.6 ms                                                  | 15.7 ms: 1.15x slower                                        |
| Geometric mean  | (ref)                                                    | 1.04x slower                                                 |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 8.80 ms: 2.36x faster                                        |
| async_tree_eager_io              | 496 ms                                                   | 260 ms: 1.90x faster                                         |
| async_tree_io_tg                 | 480 ms                                                   | 266 ms: 1.81x faster                                         |
| async_tree_io                    | 459 ms                                                   | 266 ms: 1.72x faster                                         |
| async_tree_eager_io_tg           | 446 ms                                                   | 268 ms: 1.66x faster                                         |
| async_tree_none_tg               | 172 ms                                                   | 112 ms: 1.54x faster                                         |
| async_tree_none                  | 178 ms                                                   | 117 ms: 1.53x faster                                         |
| async_tree_memoization_tg        | 231 ms                                                   | 155 ms: 1.49x faster                                         |
| deepcopy                         | 161 us                                                   | 109 us: 1.48x faster                                         |
| async_tree_memoization           | 223 ms                                                   | 155 ms: 1.43x faster                                         |
| deepcopy_memo                    | 18.3 us                                                  | 12.9 us: 1.42x faster                                        |
| deepcopy_reduce                  | 1.46 us                                                  | 1.15 us: 1.27x faster                                        |
| comprehensions                   | 9.84 us                                                  | 7.79 us: 1.26x faster                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 270 ms: 1.25x faster                                         |
| coroutines                       | 13.6 ms                                                  | 10.9 ms: 1.25x faster                                        |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 270 ms: 1.23x faster                                         |
| dulwich_log                      | 21.3 ms                                                  | 17.8 ms: 1.20x faster                                        |
| go                               | 70.0 ms                                                  | 58.9 ms: 1.19x faster                                        |
| generators                       | 21.9 ms                                                  | 18.5 ms: 1.18x faster                                        |
| logging_silent                   | 50.9 ns                                                  | 43.8 ns: 1.16x faster                                        |
| raytrace                         | 145 ms                                                   | 125 ms: 1.16x faster                                         |
| k_core                           | 1.12 sec                                                 | 964 ms: 1.16x faster                                         |
| async_generators                 | 206 ms                                                   | 179 ms: 1.16x faster                                         |
| float                            | 37.9 ms                                                  | 33.0 ms: 1.15x faster                                        |
| regex_effbot                     | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                        |
| async_tree_eager_memoization     | 132 ms                                                   | 117 ms: 1.13x faster                                         |
| regex_compile                    | 54.6 ms                                                  | 49.0 ms: 1.11x faster                                        |
| scimark_sor                      | 61.0 ms                                                  | 54.9 ms: 1.11x faster                                        |
| tomli_loads                      | 957 ms                                                   | 862 ms: 1.11x faster                                         |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.87 ms: 1.11x faster                                        |
| xml_etree_iterparse              | 51.6 ms                                                  | 46.6 ms: 1.11x faster                                        |
| spectral_norm                    | 54.4 ms                                                  | 49.2 ms: 1.11x faster                                        |
| pylint                           | 128 ms                                                   | 117 ms: 1.09x faster                                         |
| xml_etree_parse                  | 67.9 ms                                                  | 62.2 ms: 1.09x faster                                        |
| pathlib                          | 12.4 ms                                                  | 11.4 ms: 1.08x faster                                        |
| deltablue                        | 1.73 ms                                                  | 1.60 ms: 1.08x faster                                        |
| regex_dna                        | 99.6 ms                                                  | 92.8 ms: 1.07x faster                                        |
| scimark_fft                      | 142 ms                                                   | 132 ms: 1.07x faster                                         |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.09 sec: 1.07x faster                                       |
| logging_format                   | 2.80 us                                                  | 2.63 us: 1.06x faster                                        |
| logging_simple                   | 2.57 us                                                  | 2.42 us: 1.06x faster                                        |
| nbody                            | 54.2 ms                                                  | 51.0 ms: 1.06x faster                                        |
| bench_mp_pool                    | 39.7 ms                                                  | 37.7 ms: 1.05x faster                                        |
| typing_runtime_protocols         | 71.0 us                                                  | 67.7 us: 1.05x faster                                        |
| pyflate                          | 216 ms                                                   | 207 ms: 1.04x faster                                         |
| xml_etree_generate               | 38.9 ms                                                  | 37.3 ms: 1.04x faster                                        |
| async_tree_eager                 | 45.6 ms                                                  | 43.8 ms: 1.04x faster                                        |
| sqlalchemy_declarative           | 46.8 ms                                                  | 45.3 ms: 1.03x faster                                        |
| sphinx                           | 434 ms                                                   | 421 ms: 1.03x faster                                         |
| scimark_lu                       | 51.3 ms                                                  | 49.9 ms: 1.03x faster                                        |
| scimark_monte_carlo              | 32.2 ms                                                  | 31.3 ms: 1.03x faster                                        |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.03x faster                                         |
| sqlite_synth                     | 967 ns                                                   | 950 ns: 1.02x faster                                         |
| chaos                            | 28.9 ms                                                  | 28.4 ms: 1.02x faster                                        |
| sympy_sum                        | 57.6 ms                                                  | 56.7 ms: 1.01x faster                                        |
| hexiom                           | 3.04 ms                                                  | 3.00 ms: 1.01x faster                                        |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                         |
| sympy_str                        | 104 ms                                                   | 103 ms: 1.01x faster                                         |
| thrift                           | 322 us                                                   | 320 us: 1.01x faster                                         |
| sqlglot_parse                    | 577 us                                                   | 575 us: 1.00x faster                                         |
| 2to3                             | 114 ms                                                   | 114 ms: 1.00x slower                                         |
| richards_super                   | 25.4 ms                                                  | 25.5 ms: 1.00x slower                                        |
| mako                             | 4.77 ms                                                  | 4.82 ms: 1.01x slower                                        |
| genshi_text                      | 10.5 ms                                                  | 10.6 ms: 1.01x slower                                        |
| mdp                              | 1.09 sec                                                 | 1.11 sec: 1.01x slower                                       |
| pidigits                         | 161 ms                                                   | 163 ms: 1.01x slower                                         |
| xml_etree_process                | 26.7 ms                                                  | 27.1 ms: 1.01x slower                                        |
| json                             | 1.93 ms                                                  | 1.96 ms: 1.01x slower                                        |
| shortest_path                    | 219 ms                                                   | 223 ms: 1.02x slower                                         |
| nqueens                          | 43.5 ms                                                  | 44.3 ms: 1.02x slower                                        |
| sqlglot_optimize                 | 23.4 ms                                                  | 23.9 ms: 1.02x slower                                        |
| sqlglot_normalize                | 126 ms                                                   | 128 ms: 1.02x slower                                         |
| richards                         | 22.4 ms                                                  | 22.9 ms: 1.02x slower                                        |
| unpickle_pure_python             | 103 us                                                   | 105 us: 1.02x slower                                         |
| asyncio_websockets               | 190 ms                                                   | 194 ms: 1.02x slower                                         |
| connected_components             | 201 ms                                                   | 206 ms: 1.02x slower                                         |
| sympy_integrate                  | 8.02 ms                                                  | 8.23 ms: 1.03x slower                                        |
| sympy_expand                     | 167 ms                                                   | 172 ms: 1.03x slower                                         |
| sqlalchemy_imperative            | 5.17 ms                                                  | 5.33 ms: 1.03x slower                                        |
| bench_thread_pool                | 419 us                                                   | 432 us: 1.03x slower                                         |
| meteor_contest                   | 47.7 ms                                                  | 49.5 ms: 1.04x slower                                        |
| crypto_pyaes                     | 38.8 ms                                                  | 40.4 ms: 1.04x slower                                        |
| docutils                         | 1.02 sec                                                 | 1.07 sec: 1.05x slower                                       |
| json_loads                       | 10.9 us                                                  | 11.5 us: 1.06x slower                                        |
| pickle_pure_python               | 139 us                                                   | 148 us: 1.06x slower                                         |
| gc_traversal                     | 2.01 ms                                                  | 2.13 ms: 1.06x slower                                        |
| python_startup                   | 8.01 ms                                                  | 8.66 ms: 1.08x slower                                        |
| create_gc_cycles                 | 830 us                                                   | 900 us: 1.08x slower                                         |
| fannkuch                         | 176 ms                                                   | 191 ms: 1.09x slower                                         |
| python_startup_no_site           | 5.71 ms                                                  | 6.42 ms: 1.13x slower                                        |
| regex_v8                         | 9.59 ms                                                  | 10.9 ms: 1.14x slower                                        |
| django_template                  | 13.6 ms                                                  | 15.7 ms: 1.15x slower                                        |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 252 ms: 1.19x slower                                         |
| json_dumps                       | 4.26 ms                                                  | 5.06 ms: 1.19x slower                                        |
| coverage                         | 26.9 ms                                                  | 32.0 ms: 1.19x slower                                        |
| telco                            | 2.61 ms                                                  | 3.16 ms: 1.21x slower                                        |
| many_optionals                   | 195 us                                                   | 238 us: 1.22x slower                                         |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 139 ms: 1.23x slower                                         |
| async_tree_eager_tg              | 32.1 ms                                                  | 91.8 ms: 2.86x slower                                        |
| Geometric mean                   | (ref)                                                    | 1.06x faster                                                 |

Benchmark hidden because not significant (6): html5lib, genshi_xml, pycparser, sqlglot_transpile, pprint_pformat, pprint_safe_repr
Ignored benchmarks (4) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, tornado_http

- Geometric mean (including insignificant results): 1.063x faster

# HPT report

- Reliability score: 99.55% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.11x