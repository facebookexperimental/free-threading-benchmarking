# Results vs. 3.12.6

- fork: python
- ref: 0bb9ef9695d30c9ca90a
- machine: darwin-arm64
- commit hash: 0bb9ef9
- commit date: 2026-11-08
- overall geometric mean: 1.068x faster
- HPT reliability: 91.23%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261108-macm4pro-arm64-python-0bb9ef9695d30c9ca90a-3.16.0a1+dev-0bb9ef9 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 126 ms: 1.11x slower                                                        |
| docutils       | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                      |
| sphinx         | 434 ms                                                   | 446 ms: 1.03x slower                                                        |
| Geometric mean | (ref)                                                    | 1.03x slower                                                                |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261108-macm4pro-arm64-python-0bb9ef9695d30c9ca90a-3.16.0a1+dev-0bb9ef9 |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_generators                 | 206 ms                                                   | 112 ms: 1.84x faster                                                        |
| async_tree_eager_io              | 496 ms                                                   | 301 ms: 1.65x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 301 ms: 1.60x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 302 ms: 1.52x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 297 ms: 1.50x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 182 ms: 1.27x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 141 ms: 1.26x faster                                                        |
| async_tree_none_tg               | 172 ms                                                   | 142 ms: 1.21x faster                                                        |
| async_tree_memoization           | 223 ms                                                   | 184 ms: 1.21x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 291 ms: 1.16x faster                                                        |
| coroutines                       | 13.6 ms                                                  | 11.8 ms: 1.15x faster                                                       |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 294 ms: 1.13x faster                                                        |
| async_tree_eager_memoization     | 132 ms                                                   | 126 ms: 1.05x faster                                                        |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 230 ms: 1.01x faster                                                        |
| async_tree_eager                 | 45.6 ms                                                  | 50.1 ms: 1.10x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 269 ms: 1.27x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 156 ms: 1.38x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 115 ms: 3.57x slower                                                        |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261108-macm4pro-arm64-python-0bb9ef9695d30c9ca90a-3.16.0a1+dev-0bb9ef9 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 33.1 ms: 1.14x faster                                                       |
| pidigits       | 161 ms                                                   | 146 ms: 1.10x faster                                                        |
| nbody          | 54.2 ms                                                  | 60.2 ms: 1.11x slower                                                       |
| Geometric mean | (ref)                                                    | 1.04x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261108-macm4pro-arm64-python-0bb9ef9695d30c9ca90a-3.16.0a1+dev-0bb9ef9 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.32 ms: 1.26x faster                                                       |
| regex_dna      | 99.6 ms                                                  | 91.5 ms: 1.09x faster                                                       |
| regex_v8       | 9.59 ms                                                  | 9.17 ms: 1.05x faster                                                       |
| regex_compile  | 54.6 ms                                                  | 64.2 ms: 1.18x slower                                                       |
| Geometric mean | (ref)                                                    | 1.05x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261108-macm4pro-arm64-python-0bb9ef9695d30c9ca90a-3.16.0a1+dev-0bb9ef9 |
|----------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 41.0 ms: 1.26x faster                                                       |
| xml_etree_parse      | 67.9 ms                                                  | 58.5 ms: 1.16x faster                                                       |
| json_dumps           | 4.26 ms                                                  | 3.77 ms: 1.13x faster                                                       |
| tomli_loads          | 957 ms                                                   | 881 ms: 1.09x faster                                                        |
| xml_etree_generate   | 38.9 ms                                                  | 37.9 ms: 1.02x faster                                                       |
| json_loads           | 10.9 us                                                  | 11.2 us: 1.03x slower                                                       |
| unpickle_pure_python | 103 us                                                   | 110 us: 1.07x slower                                                        |
| xml_etree_process    | 26.7 ms                                                  | 29.2 ms: 1.09x slower                                                       |
| pickle_pure_python   | 139 us                                                   | 158 us: 1.13x slower                                                        |
| Geometric mean       | (ref)                                                    | 1.03x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261108-macm4pro-arm64-python-0bb9ef9695d30c9ca90a-3.16.0a1+dev-0bb9ef9 |
|------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.62 ms: 1.08x slower                                                       |
| python_startup_no_site | 5.71 ms                                                  | 6.73 ms: 1.18x slower                                                       |
| Geometric mean         | (ref)                                                    | 1.13x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261108-macm4pro-arm64-python-0bb9ef9695d30c9ca90a-3.16.0a1+dev-0bb9ef9 |
|-----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 5.62 ms: 1.18x slower                                                       |
| django_template | 13.6 ms                                                  | 16.8 ms: 1.24x slower                                                       |
| Geometric mean  | (ref)                                                    | 1.21x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261108-macm4pro-arm64-python-0bb9ef9695d30c9ca90a-3.16.0a1+dev-0bb9ef9 |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.32 ms: 4.80x faster                                                       |
| pylint                           | 128 ms                                                   | 52.0 ms: 2.46x faster                                                       |
| gc_traversal                     | 2.01 ms                                                  | 893 us: 2.25x faster                                                        |
| mdp                              | 1.09 sec                                                 | 577 ms: 1.89x faster                                                        |
| async_generators                 | 206 ms                                                   | 112 ms: 1.84x faster                                                        |
| create_gc_cycles                 | 830 us                                                   | 478 us: 1.73x faster                                                        |
| async_tree_eager_io              | 496 ms                                                   | 301 ms: 1.65x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 301 ms: 1.60x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 302 ms: 1.52x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 297 ms: 1.50x faster                                                        |
| deepcopy                         | 161 us                                                   | 111 us: 1.46x faster                                                        |
| typing_runtime_protocols         | 71.0 us                                                  | 53.6 us: 1.32x faster                                                       |
| async_tree_memoization_tg        | 231 ms                                                   | 182 ms: 1.27x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 141 ms: 1.26x faster                                                        |
| regex_effbot                     | 1.67 ms                                                  | 1.32 ms: 1.26x faster                                                       |
| xml_etree_iterparse              | 51.6 ms                                                  | 41.0 ms: 1.26x faster                                                       |
| deepcopy_memo                    | 18.3 us                                                  | 14.7 us: 1.25x faster                                                       |
| async_tree_none_tg               | 172 ms                                                   | 142 ms: 1.21x faster                                                        |
| async_tree_memoization           | 223 ms                                                   | 184 ms: 1.21x faster                                                        |
| deepcopy_reduce                  | 1.46 us                                                  | 1.21 us: 1.20x faster                                                       |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.89 sec: 1.19x faster                                                      |
| comprehensions                   | 9.84 us                                                  | 8.29 us: 1.19x faster                                                       |
| sqlite_synth                     | 967 ns                                                   | 823 ns: 1.18x faster                                                        |
| go                               | 70.0 ms                                                  | 59.9 ms: 1.17x faster                                                       |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 291 ms: 1.16x faster                                                        |
| xml_etree_parse                  | 67.9 ms                                                  | 58.5 ms: 1.16x faster                                                       |
| coroutines                       | 13.6 ms                                                  | 11.8 ms: 1.15x faster                                                       |
| float                            | 37.9 ms                                                  | 33.1 ms: 1.14x faster                                                       |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.14x faster                                                       |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 294 ms: 1.13x faster                                                        |
| k_core                           | 1.12 sec                                                 | 990 ms: 1.13x faster                                                        |
| json_dumps                       | 4.26 ms                                                  | 3.77 ms: 1.13x faster                                                       |
| pidigits                         | 161 ms                                                   | 146 ms: 1.10x faster                                                        |
| spectral_norm                    | 54.4 ms                                                  | 49.6 ms: 1.10x faster                                                       |
| regex_dna                        | 99.6 ms                                                  | 91.5 ms: 1.09x faster                                                       |
| pyflate                          | 216 ms                                                   | 199 ms: 1.09x faster                                                        |
| tomli_loads                      | 957 ms                                                   | 881 ms: 1.09x faster                                                        |
| dulwich_log                      | 21.3 ms                                                  | 19.6 ms: 1.09x faster                                                       |
| scimark_fft                      | 142 ms                                                   | 132 ms: 1.08x faster                                                        |
| raytrace                         | 145 ms                                                   | 137 ms: 1.06x faster                                                        |
| async_tree_eager_memoization     | 132 ms                                                   | 126 ms: 1.05x faster                                                        |
| regex_v8                         | 9.59 ms                                                  | 9.17 ms: 1.05x faster                                                       |
| logging_simple                   | 2.57 us                                                  | 2.47 us: 1.04x faster                                                       |
| scimark_sor                      | 61.0 ms                                                  | 58.6 ms: 1.04x faster                                                       |
| logging_format                   | 2.80 us                                                  | 2.71 us: 1.03x faster                                                       |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                        |
| xml_etree_generate               | 38.9 ms                                                  | 37.9 ms: 1.02x faster                                                       |
| logging_silent                   | 50.9 ns                                                  | 49.8 ns: 1.02x faster                                                       |
| pycparser                        | 497 ms                                                   | 491 ms: 1.01x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 230 ms: 1.01x faster                                                        |
| json                             | 1.93 ms                                                  | 1.95 ms: 1.01x slower                                                       |
| nqueens                          | 43.5 ms                                                  | 43.9 ms: 1.01x slower                                                       |
| docutils                         | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                      |
| sympy_integrate                  | 8.02 ms                                                  | 8.12 ms: 1.01x slower                                                       |
| chaos                            | 28.9 ms                                                  | 29.4 ms: 1.02x slower                                                       |
| sphinx                           | 434 ms                                                   | 446 ms: 1.03x slower                                                        |
| json_loads                       | 10.9 us                                                  | 11.2 us: 1.03x slower                                                       |
| fannkuch                         | 176 ms                                                   | 181 ms: 1.03x slower                                                        |
| deltablue                        | 1.73 ms                                                  | 1.79 ms: 1.04x slower                                                       |
| hexiom                           | 3.04 ms                                                  | 3.16 ms: 1.04x slower                                                       |
| bench_mp_pool                    | 39.7 ms                                                  | 41.3 ms: 1.04x slower                                                       |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.17 ms: 1.04x slower                                                       |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.9 ms: 1.05x slower                                                       |
| sympy_sum                        | 57.6 ms                                                  | 60.9 ms: 1.06x slower                                                       |
| sympy_str                        | 104 ms                                                   | 111 ms: 1.06x slower                                                        |
| generators                       | 21.9 ms                                                  | 23.4 ms: 1.07x slower                                                       |
| crypto_pyaes                     | 38.8 ms                                                  | 41.5 ms: 1.07x slower                                                       |
| unpickle_pure_python             | 103 us                                                   | 110 us: 1.07x slower                                                        |
| pprint_safe_repr                 | 328 ms                                                   | 352 ms: 1.07x slower                                                        |
| richards                         | 22.4 ms                                                  | 24.1 ms: 1.07x slower                                                       |
| python_startup                   | 8.01 ms                                                  | 8.62 ms: 1.08x slower                                                       |
| thrift                           | 322 us                                                   | 347 us: 1.08x slower                                                        |
| richards_super                   | 25.4 ms                                                  | 27.7 ms: 1.09x slower                                                       |
| xml_etree_process                | 26.7 ms                                                  | 29.2 ms: 1.09x slower                                                       |
| async_tree_eager                 | 45.6 ms                                                  | 50.1 ms: 1.10x slower                                                       |
| meteor_contest                   | 47.7 ms                                                  | 52.8 ms: 1.11x slower                                                       |
| 2to3                             | 114 ms                                                   | 126 ms: 1.11x slower                                                        |
| nbody                            | 54.2 ms                                                  | 60.2 ms: 1.11x slower                                                       |
| pprint_pformat                   | 665 ms                                                   | 738 ms: 1.11x slower                                                        |
| bench_thread_pool                | 419 us                                                   | 468 us: 1.12x slower                                                        |
| shortest_path                    | 219 ms                                                   | 245 ms: 1.12x slower                                                        |
| sympy_expand                     | 167 ms                                                   | 189 ms: 1.13x slower                                                        |
| pickle_pure_python               | 139 us                                                   | 158 us: 1.13x slower                                                        |
| telco                            | 2.61 ms                                                  | 3.06 ms: 1.17x slower                                                       |
| regex_compile                    | 54.6 ms                                                  | 64.2 ms: 1.18x slower                                                       |
| mako                             | 4.77 ms                                                  | 5.62 ms: 1.18x slower                                                       |
| python_startup_no_site           | 5.71 ms                                                  | 6.73 ms: 1.18x slower                                                       |
| connected_components             | 201 ms                                                   | 238 ms: 1.18x slower                                                        |
| scimark_lu                       | 51.3 ms                                                  | 62.9 ms: 1.23x slower                                                       |
| django_template                  | 13.6 ms                                                  | 16.8 ms: 1.24x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 269 ms: 1.27x slower                                                        |
| many_optionals                   | 195 us                                                   | 254 us: 1.30x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 156 ms: 1.38x slower                                                        |
| coverage                         | 26.9 ms                                                  | 41.7 ms: 1.55x slower                                                       |
| async_tree_eager_tg              | 32.1 ms                                                  | 115 ms: 3.57x slower                                                        |
| Geometric mean                   | (ref)                                                    | 1.07x faster                                                                |

Benchmark hidden because not significant (1): html5lib
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261108-3.16.0a1+dev-0bb9ef9-NOGIL/bm-20261108-macm4pro-arm64-python-0bb9ef9695d30c9ca90a-3.16.0a1+dev-0bb9ef9.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.068x faster

# HPT report

- Reliability score: 91.23% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.23x