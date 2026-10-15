# Results vs. 3.12.6

- fork: python
- ref: a6b4aa687cd9f8f95e3b
- machine: darwin-arm64
- commit hash: a6b4aa6
- commit date: 2026-10-14
- overall geometric mean: 1.059x faster
- HPT reliability: 85.35%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.29x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261014-macm4pro-arm64-python-a6b4aa687cd9f8f95e3b-3.16.0a1+dev-a6b4aa6 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 129 ms: 1.13x slower                                                        |
| docutils       | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                      |
| html5lib       | 23.0 ms                                                  | 22.8 ms: 1.01x faster                                                       |
| sphinx         | 434 ms                                                   | 445 ms: 1.03x slower                                                        |
| Geometric mean | (ref)                                                    | 1.04x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261014-macm4pro-arm64-python-a6b4aa687cd9f8f95e3b-3.16.0a1+dev-a6b4aa6 |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 298 ms: 1.67x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 297 ms: 1.62x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 295 ms: 1.51x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 307 ms: 1.49x faster                                                        |
| async_generators                 | 206 ms                                                   | 159 ms: 1.29x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 181 ms: 1.27x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 143 ms: 1.25x faster                                                        |
| async_tree_none_tg               | 172 ms                                                   | 140 ms: 1.23x faster                                                        |
| async_tree_memoization           | 223 ms                                                   | 186 ms: 1.20x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 295 ms: 1.15x faster                                                        |
| coroutines                       | 13.6 ms                                                  | 12.1 ms: 1.12x faster                                                       |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 302 ms: 1.10x faster                                                        |
| async_tree_eager_memoization     | 132 ms                                                   | 125 ms: 1.05x faster                                                        |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 236 ms: 1.02x slower                                                        |
| async_tree_eager                 | 45.6 ms                                                  | 50.4 ms: 1.11x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 276 ms: 1.30x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 164 ms: 1.45x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 114 ms: 3.55x slower                                                        |
| Geometric mean                   | (ref)                                                    | 1.07x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261014-macm4pro-arm64-python-a6b4aa687cd9f8f95e3b-3.16.0a1+dev-a6b4aa6 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 33.1 ms: 1.14x faster                                                       |
| pidigits       | 161 ms                                                   | 163 ms: 1.01x slower                                                        |
| nbody          | 54.2 ms                                                  | 57.5 ms: 1.06x slower                                                       |
| Geometric mean | (ref)                                                    | 1.02x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261014-macm4pro-arm64-python-a6b4aa687cd9f8f95e3b-3.16.0a1+dev-a6b4aa6 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.33 ms: 1.25x faster                                                       |
| regex_dna      | 99.6 ms                                                  | 92.4 ms: 1.08x faster                                                       |
| regex_v8       | 9.59 ms                                                  | 9.22 ms: 1.04x faster                                                       |
| regex_compile  | 54.6 ms                                                  | 64.5 ms: 1.18x slower                                                       |
| Geometric mean | (ref)                                                    | 1.04x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261014-macm4pro-arm64-python-a6b4aa687cd9f8f95e3b-3.16.0a1+dev-a6b4aa6 |
|----------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.9 ms: 1.26x faster                                                       |
| xml_etree_parse      | 67.9 ms                                                  | 58.9 ms: 1.15x faster                                                       |
| json_dumps           | 4.26 ms                                                  | 3.78 ms: 1.13x faster                                                       |
| tomli_loads          | 957 ms                                                   | 868 ms: 1.10x faster                                                        |
| xml_etree_generate   | 38.9 ms                                                  | 39.0 ms: 1.00x slower                                                       |
| json_loads           | 10.9 us                                                  | 11.1 us: 1.02x slower                                                       |
| unpickle_pure_python | 103 us                                                   | 110 us: 1.07x slower                                                        |
| pickle_pure_python   | 139 us                                                   | 154 us: 1.11x slower                                                        |
| xml_etree_process    | 26.7 ms                                                  | 30.0 ms: 1.12x slower                                                       |
| Geometric mean       | (ref)                                                    | 1.03x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261014-macm4pro-arm64-python-a6b4aa687cd9f8f95e3b-3.16.0a1+dev-a6b4aa6 |
|------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.96 ms: 1.24x slower                                                       |
| python_startup_no_site | 5.71 ms                                                  | 7.31 ms: 1.28x slower                                                       |
| Geometric mean         | (ref)                                                    | 1.26x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261014-macm4pro-arm64-python-a6b4aa687cd9f8f95e3b-3.16.0a1+dev-a6b4aa6 |
|-----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 5.76 ms: 1.21x slower                                                       |
| django_template | 13.6 ms                                                  | 16.9 ms: 1.24x slower                                                       |
| Geometric mean  | (ref)                                                    | 1.22x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261014-macm4pro-arm64-python-a6b4aa687cd9f8f95e3b-3.16.0a1+dev-a6b4aa6 |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.32 ms: 4.81x faster                                                       |
| gc_traversal                     | 2.01 ms                                                  | 778 us: 2.58x faster                                                        |
| pylint                           | 128 ms                                                   | 53.0 ms: 2.42x faster                                                       |
| mdp                              | 1.09 sec                                                 | 590 ms: 1.85x faster                                                        |
| create_gc_cycles                 | 830 us                                                   | 474 us: 1.75x faster                                                        |
| async_tree_eager_io              | 496 ms                                                   | 298 ms: 1.67x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 297 ms: 1.62x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 295 ms: 1.51x faster                                                        |
| deepcopy                         | 161 us                                                   | 108 us: 1.50x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 307 ms: 1.49x faster                                                        |
| deepcopy_memo                    | 18.3 us                                                  | 13.9 us: 1.32x faster                                                       |
| async_generators                 | 206 ms                                                   | 159 ms: 1.29x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 181 ms: 1.27x faster                                                        |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.9 ms: 1.26x faster                                                       |
| regex_effbot                     | 1.67 ms                                                  | 1.33 ms: 1.25x faster                                                       |
| async_tree_none                  | 178 ms                                                   | 143 ms: 1.25x faster                                                        |
| typing_runtime_protocols         | 71.0 us                                                  | 57.3 us: 1.24x faster                                                       |
| deepcopy_reduce                  | 1.46 us                                                  | 1.18 us: 1.24x faster                                                       |
| async_tree_none_tg               | 172 ms                                                   | 140 ms: 1.23x faster                                                        |
| sqlite_synth                     | 967 ns                                                   | 803 ns: 1.20x faster                                                        |
| async_tree_memoization           | 223 ms                                                   | 186 ms: 1.20x faster                                                        |
| comprehensions                   | 9.84 us                                                  | 8.32 us: 1.18x faster                                                       |
| go                               | 70.0 ms                                                  | 60.0 ms: 1.17x faster                                                       |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.93 sec: 1.16x faster                                                      |
| xml_etree_parse                  | 67.9 ms                                                  | 58.9 ms: 1.15x faster                                                       |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 295 ms: 1.15x faster                                                        |
| float                            | 37.9 ms                                                  | 33.1 ms: 1.14x faster                                                       |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.14x faster                                                       |
| json_dumps                       | 4.26 ms                                                  | 3.78 ms: 1.13x faster                                                       |
| k_core                           | 1.12 sec                                                 | 997 ms: 1.12x faster                                                        |
| coroutines                       | 13.6 ms                                                  | 12.1 ms: 1.12x faster                                                       |
| pyflate                          | 216 ms                                                   | 196 ms: 1.11x faster                                                        |
| dulwich_log                      | 21.3 ms                                                  | 19.2 ms: 1.10x faster                                                       |
| tomli_loads                      | 957 ms                                                   | 868 ms: 1.10x faster                                                        |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 302 ms: 1.10x faster                                                        |
| spectral_norm                    | 54.4 ms                                                  | 49.5 ms: 1.10x faster                                                       |
| scimark_fft                      | 142 ms                                                   | 130 ms: 1.09x faster                                                        |
| regex_dna                        | 99.6 ms                                                  | 92.4 ms: 1.08x faster                                                       |
| raytrace                         | 145 ms                                                   | 138 ms: 1.05x faster                                                        |
| scimark_sor                      | 61.0 ms                                                  | 58.0 ms: 1.05x faster                                                       |
| async_tree_eager_memoization     | 132 ms                                                   | 125 ms: 1.05x faster                                                        |
| logging_simple                   | 2.57 us                                                  | 2.47 us: 1.04x faster                                                       |
| logging_format                   | 2.80 us                                                  | 2.69 us: 1.04x faster                                                       |
| regex_v8                         | 9.59 ms                                                  | 9.22 ms: 1.04x faster                                                       |
| pycparser                        | 497 ms                                                   | 478 ms: 1.04x faster                                                        |
| logging_silent                   | 50.9 ns                                                  | 49.1 ns: 1.04x faster                                                       |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                        |
| nqueens                          | 43.5 ms                                                  | 43.0 ms: 1.01x faster                                                       |
| html5lib                         | 23.0 ms                                                  | 22.8 ms: 1.01x faster                                                       |
| xml_etree_generate               | 38.9 ms                                                  | 39.0 ms: 1.00x slower                                                       |
| pidigits                         | 161 ms                                                   | 163 ms: 1.01x slower                                                        |
| sympy_integrate                  | 8.02 ms                                                  | 8.13 ms: 1.01x slower                                                       |
| docutils                         | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                      |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 236 ms: 1.02x slower                                                        |
| json_loads                       | 10.9 us                                                  | 11.1 us: 1.02x slower                                                       |
| sphinx                           | 434 ms                                                   | 445 ms: 1.03x slower                                                        |
| deltablue                        | 1.73 ms                                                  | 1.80 ms: 1.04x slower                                                       |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.9 ms: 1.05x slower                                                       |
| crypto_pyaes                     | 38.8 ms                                                  | 41.0 ms: 1.06x slower                                                       |
| sympy_sum                        | 57.6 ms                                                  | 60.9 ms: 1.06x slower                                                       |
| nbody                            | 54.2 ms                                                  | 57.5 ms: 1.06x slower                                                       |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.20 ms: 1.06x slower                                                       |
| hexiom                           | 3.04 ms                                                  | 3.22 ms: 1.06x slower                                                       |
| sympy_str                        | 104 ms                                                   | 111 ms: 1.07x slower                                                        |
| unpickle_pure_python             | 103 us                                                   | 110 us: 1.07x slower                                                        |
| richards                         | 22.4 ms                                                  | 24.1 ms: 1.07x slower                                                       |
| pprint_safe_repr                 | 328 ms                                                   | 352 ms: 1.07x slower                                                        |
| generators                       | 21.9 ms                                                  | 23.6 ms: 1.08x slower                                                       |
| thrift                           | 322 us                                                   | 347 us: 1.08x slower                                                        |
| bench_mp_pool                    | 39.7 ms                                                  | 43.0 ms: 1.08x slower                                                       |
| richards_super                   | 25.4 ms                                                  | 27.6 ms: 1.09x slower                                                       |
| async_tree_eager                 | 45.6 ms                                                  | 50.4 ms: 1.11x slower                                                       |
| pickle_pure_python               | 139 us                                                   | 154 us: 1.11x slower                                                        |
| pprint_pformat                   | 665 ms                                                   | 738 ms: 1.11x slower                                                        |
| meteor_contest                   | 47.7 ms                                                  | 53.3 ms: 1.12x slower                                                       |
| xml_etree_process                | 26.7 ms                                                  | 30.0 ms: 1.12x slower                                                       |
| 2to3                             | 114 ms                                                   | 129 ms: 1.13x slower                                                        |
| sympy_expand                     | 167 ms                                                   | 189 ms: 1.13x slower                                                        |
| shortest_path                    | 219 ms                                                   | 248 ms: 1.13x slower                                                        |
| regex_compile                    | 54.6 ms                                                  | 64.5 ms: 1.18x slower                                                       |
| connected_components             | 201 ms                                                   | 239 ms: 1.19x slower                                                        |
| mako                             | 4.77 ms                                                  | 5.76 ms: 1.21x slower                                                       |
| telco                            | 2.61 ms                                                  | 3.19 ms: 1.22x slower                                                       |
| python_startup                   | 8.01 ms                                                  | 9.96 ms: 1.24x slower                                                       |
| django_template                  | 13.6 ms                                                  | 16.9 ms: 1.24x slower                                                       |
| python_startup_no_site           | 5.71 ms                                                  | 7.31 ms: 1.28x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 276 ms: 1.30x slower                                                        |
| many_optionals                   | 195 us                                                   | 254 us: 1.30x slower                                                        |
| scimark_lu                       | 51.3 ms                                                  | 68.4 ms: 1.33x slower                                                       |
| bench_thread_pool                | 419 us                                                   | 577 us: 1.38x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 164 ms: 1.45x slower                                                        |
| coverage                         | 26.9 ms                                                  | 40.3 ms: 1.50x slower                                                       |
| async_tree_eager_tg              | 32.1 ms                                                  | 114 ms: 3.55x slower                                                        |
| Geometric mean                   | (ref)                                                    | 1.05x faster                                                                |

Benchmark hidden because not significant (3): chaos, json, fannkuch
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261014-3.16.0a1+dev-a6b4aa6-NOGIL/bm-20261014-macm4pro-arm64-python-a6b4aa687cd9f8f95e3b-3.16.0a1+dev-a6b4aa6.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.059x faster

# HPT report

- Reliability score: 85.35% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.29x