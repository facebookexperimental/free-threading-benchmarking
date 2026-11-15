# Results vs. 3.12.6

- fork: python
- ref: edd6f7692ad1bb30ba48
- machine: darwin-arm64
- commit hash: edd6f76
- commit date: 2026-11-14
- overall geometric mean: 1.202x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 113 ms: 1.01x faster                                                        |
| docutils       | 1.02 sec                                                 | 900 ms: 1.14x faster                                                        |
| html5lib       | 23.0 ms                                                  | 20.4 ms: 1.13x faster                                                       |
| sphinx         | 434 ms                                                   | 384 ms: 1.13x faster                                                        |
| Geometric mean | (ref)                                                    | 1.10x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_generators                 | 206 ms                                                   | 97.6 ms: 2.11x faster                                                       |
| async_tree_eager_io              | 496 ms                                                   | 264 ms: 1.88x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 278 ms: 1.73x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 272 ms: 1.69x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 277 ms: 1.61x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 111 ms: 1.60x faster                                                        |
| async_tree_none_tg               | 172 ms                                                   | 112 ms: 1.54x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 157 ms: 1.46x faster                                                        |
| coroutines                       | 13.6 ms                                                  | 9.65 ms: 1.41x faster                                                       |
| async_tree_memoization           | 223 ms                                                   | 162 ms: 1.37x faster                                                        |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 265 ms: 1.26x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 270 ms: 1.25x faster                                                        |
| async_tree_eager_memoization     | 132 ms                                                   | 113 ms: 1.16x faster                                                        |
| async_tree_eager                 | 45.6 ms                                                  | 40.7 ms: 1.12x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 219 ms: 1.06x faster                                                        |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                        |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 248 ms: 1.17x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 141 ms: 1.25x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 93.6 ms: 2.91x slower                                                       |
| Geometric mean                   | (ref)                                                    | 1.25x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.6 ms: 1.37x faster                                                       |
| nbody          | 54.2 ms                                                  | 43.5 ms: 1.25x faster                                                       |
| pidigits       | 161 ms                                                   | 144 ms: 1.12x faster                                                        |
| Geometric mean | (ref)                                                    | 1.24x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.28 ms: 1.30x faster                                                       |
| regex_dna      | 99.6 ms                                                  | 89.8 ms: 1.11x faster                                                       |
| regex_v8       | 9.59 ms                                                  | 9.09 ms: 1.05x faster                                                       |
| regex_compile  | 54.6 ms                                                  | 53.2 ms: 1.03x faster                                                       |
| Geometric mean | (ref)                                                    | 1.12x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 41.7 ms: 1.24x faster                                                       |
| tomli_loads          | 957 ms                                                   | 785 ms: 1.22x faster                                                        |
| json_dumps           | 4.26 ms                                                  | 3.53 ms: 1.21x faster                                                       |
| xml_etree_generate   | 38.9 ms                                                  | 34.3 ms: 1.13x faster                                                       |
| unpickle_pure_python | 103 us                                                   | 94.5 us: 1.09x faster                                                       |
| xml_etree_process    | 26.7 ms                                                  | 24.8 ms: 1.08x faster                                                       |
| json_loads           | 10.9 us                                                  | 10.5 us: 1.03x faster                                                       |
| xml_etree_parse      | 67.9 ms                                                  | 66.1 ms: 1.03x faster                                                       |
| pickle_pure_python   | 139 us                                                   | 138 us: 1.01x faster                                                        |
| Geometric mean       | (ref)                                                    | 1.11x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 7.97 ms: 1.01x faster                                                       |
| python_startup_no_site | 5.71 ms                                                  | 6.25 ms: 1.10x slower                                                       |
| Geometric mean         | (ref)                                                    | 1.04x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|-----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.38 ms: 1.09x faster                                                       |
| django_template | 13.6 ms                                                  | 14.6 ms: 1.07x slower                                                       |
| Geometric mean  | (ref)                                                    | 1.01x faster                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.91 ms: 5.31x faster                                                       |
| pylint                           | 128 ms                                                   | 50.2 ms: 2.55x faster                                                       |
| mdp                              | 1.09 sec                                                 | 499 ms: 2.19x faster                                                        |
| async_generators                 | 206 ms                                                   | 97.6 ms: 2.11x faster                                                       |
| async_tree_eager_io              | 496 ms                                                   | 264 ms: 1.88x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 278 ms: 1.73x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 272 ms: 1.69x faster                                                        |
| deepcopy                         | 161 us                                                   | 96.3 us: 1.68x faster                                                       |
| async_tree_eager_io_tg           | 446 ms                                                   | 277 ms: 1.61x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 111 ms: 1.60x faster                                                        |
| typing_runtime_protocols         | 71.0 us                                                  | 45.0 us: 1.58x faster                                                       |
| deepcopy_memo                    | 18.3 us                                                  | 11.7 us: 1.56x faster                                                       |
| async_tree_none_tg               | 172 ms                                                   | 112 ms: 1.54x faster                                                        |
| comprehensions                   | 9.84 us                                                  | 6.57 us: 1.50x faster                                                       |
| async_tree_memoization_tg        | 231 ms                                                   | 157 ms: 1.46x faster                                                        |
| deepcopy_reduce                  | 1.46 us                                                  | 1.04 us: 1.41x faster                                                       |
| coroutines                       | 13.6 ms                                                  | 9.65 ms: 1.41x faster                                                       |
| async_tree_memoization           | 223 ms                                                   | 162 ms: 1.37x faster                                                        |
| float                            | 37.9 ms                                                  | 27.6 ms: 1.37x faster                                                       |
| go                               | 70.0 ms                                                  | 51.5 ms: 1.36x faster                                                       |
| create_gc_cycles                 | 830 us                                                   | 625 us: 1.33x faster                                                        |
| spectral_norm                    | 54.4 ms                                                  | 41.0 ms: 1.33x faster                                                       |
| generators                       | 21.9 ms                                                  | 16.9 ms: 1.30x faster                                                       |
| regex_effbot                     | 1.67 ms                                                  | 1.28 ms: 1.30x faster                                                       |
| raytrace                         | 145 ms                                                   | 113 ms: 1.28x faster                                                        |
| nqueens                          | 43.5 ms                                                  | 34.3 ms: 1.27x faster                                                       |
| scimark_fft                      | 142 ms                                                   | 112 ms: 1.26x faster                                                        |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 265 ms: 1.26x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 270 ms: 1.25x faster                                                        |
| scimark_sor                      | 61.0 ms                                                  | 48.9 ms: 1.25x faster                                                       |
| nbody                            | 54.2 ms                                                  | 43.5 ms: 1.25x faster                                                       |
| xml_etree_iterparse              | 51.6 ms                                                  | 41.7 ms: 1.24x faster                                                       |
| logging_silent                   | 50.9 ns                                                  | 41.5 ns: 1.23x faster                                                       |
| deltablue                        | 1.73 ms                                                  | 1.41 ms: 1.22x faster                                                       |
| scimark_monte_carlo              | 32.2 ms                                                  | 26.4 ms: 1.22x faster                                                       |
| tomli_loads                      | 957 ms                                                   | 785 ms: 1.22x faster                                                        |
| json_dumps                       | 4.26 ms                                                  | 3.53 ms: 1.21x faster                                                       |
| dulwich_log                      | 21.3 ms                                                  | 17.7 ms: 1.20x faster                                                       |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.73 ms: 1.20x faster                                                       |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.88 sec: 1.19x faster                                                      |
| pyflate                          | 216 ms                                                   | 182 ms: 1.19x faster                                                        |
| logging_simple                   | 2.57 us                                                  | 2.19 us: 1.18x faster                                                       |
| chaos                            | 28.9 ms                                                  | 24.6 ms: 1.17x faster                                                       |
| pathlib                          | 12.4 ms                                                  | 10.5 ms: 1.17x faster                                                       |
| async_tree_eager_memoization     | 132 ms                                                   | 113 ms: 1.16x faster                                                        |
| hexiom                           | 3.04 ms                                                  | 2.61 ms: 1.16x faster                                                       |
| logging_format                   | 2.80 us                                                  | 2.42 us: 1.16x faster                                                       |
| k_core                           | 1.12 sec                                                 | 967 ms: 1.16x faster                                                        |
| docutils                         | 1.02 sec                                                 | 900 ms: 1.14x faster                                                        |
| xml_etree_generate               | 38.9 ms                                                  | 34.3 ms: 1.13x faster                                                       |
| sphinx                           | 434 ms                                                   | 384 ms: 1.13x faster                                                        |
| html5lib                         | 23.0 ms                                                  | 20.4 ms: 1.13x faster                                                       |
| async_tree_eager                 | 45.6 ms                                                  | 40.7 ms: 1.12x faster                                                       |
| pidigits                         | 161 ms                                                   | 144 ms: 1.12x faster                                                        |
| richards_super                   | 25.4 ms                                                  | 22.7 ms: 1.12x faster                                                       |
| richards                         | 22.4 ms                                                  | 20.0 ms: 1.12x faster                                                       |
| fannkuch                         | 176 ms                                                   | 158 ms: 1.11x faster                                                        |
| regex_dna                        | 99.6 ms                                                  | 89.8 ms: 1.11x faster                                                       |
| sympy_integrate                  | 8.02 ms                                                  | 7.26 ms: 1.10x faster                                                       |
| scimark_lu                       | 51.3 ms                                                  | 46.5 ms: 1.10x faster                                                       |
| mako                             | 4.77 ms                                                  | 4.38 ms: 1.09x faster                                                       |
| unpickle_pure_python             | 103 us                                                   | 94.5 us: 1.09x faster                                                       |
| xml_etree_process                | 26.7 ms                                                  | 24.8 ms: 1.08x faster                                                       |
| pycparser                        | 497 ms                                                   | 463 ms: 1.08x faster                                                        |
| pprint_safe_repr                 | 328 ms                                                   | 306 ms: 1.07x faster                                                        |
| crypto_pyaes                     | 38.8 ms                                                  | 36.3 ms: 1.07x faster                                                       |
| sympy_str                        | 104 ms                                                   | 97.7 ms: 1.07x faster                                                       |
| thrift                           | 322 us                                                   | 303 us: 1.06x faster                                                        |
| sympy_sum                        | 57.6 ms                                                  | 54.3 ms: 1.06x faster                                                       |
| pprint_pformat                   | 665 ms                                                   | 628 ms: 1.06x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 219 ms: 1.06x faster                                                        |
| regex_v8                         | 9.59 ms                                                  | 9.09 ms: 1.05x faster                                                       |
| sqlite_synth                     | 967 ns                                                   | 922 ns: 1.05x faster                                                        |
| json                             | 1.93 ms                                                  | 1.85 ms: 1.05x faster                                                       |
| gc_traversal                     | 2.01 ms                                                  | 1.93 ms: 1.04x faster                                                       |
| json_loads                       | 10.9 us                                                  | 10.5 us: 1.03x faster                                                       |
| bench_thread_pool                | 419 us                                                   | 407 us: 1.03x faster                                                        |
| xml_etree_parse                  | 67.9 ms                                                  | 66.1 ms: 1.03x faster                                                       |
| regex_compile                    | 54.6 ms                                                  | 53.2 ms: 1.03x faster                                                       |
| pickle_pure_python               | 139 us                                                   | 138 us: 1.01x faster                                                        |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                        |
| 2to3                             | 114 ms                                                   | 113 ms: 1.01x faster                                                        |
| python_startup                   | 8.01 ms                                                  | 7.97 ms: 1.01x faster                                                       |
| meteor_contest                   | 47.7 ms                                                  | 48.1 ms: 1.01x slower                                                       |
| shortest_path                    | 219 ms                                                   | 222 ms: 1.01x slower                                                        |
| connected_components             | 201 ms                                                   | 206 ms: 1.03x slower                                                        |
| bench_mp_pool                    | 39.7 ms                                                  | 41.6 ms: 1.05x slower                                                       |
| telco                            | 2.61 ms                                                  | 2.79 ms: 1.07x slower                                                       |
| django_template                  | 13.6 ms                                                  | 14.6 ms: 1.07x slower                                                       |
| python_startup_no_site           | 5.71 ms                                                  | 6.25 ms: 1.10x slower                                                       |
| many_optionals                   | 195 us                                                   | 227 us: 1.16x slower                                                        |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 248 ms: 1.17x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 141 ms: 1.25x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 93.6 ms: 2.91x slower                                                       |
| Geometric mean                   | (ref)                                                    | 1.20x faster                                                                |

Benchmark hidden because not significant (1): sympy_expand
Ignored benchmarks (14) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20261114-3.16.0a2+dev-edd6f76/bm-20261114-macm4pro-arm64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.202x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.13x
- 95% likely to have a speedup of 1.12x
- 99% likely to have a speedup of 1.11x

# Memory
- memory change: 1.15x