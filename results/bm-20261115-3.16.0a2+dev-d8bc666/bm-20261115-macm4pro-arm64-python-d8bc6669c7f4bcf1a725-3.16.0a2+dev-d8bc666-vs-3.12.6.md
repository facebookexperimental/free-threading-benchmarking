# Results vs. 3.12.6

- fork: python
- ref: d8bc6669c7f4bcf1a725
- machine: darwin-arm64
- commit hash: d8bc666
- commit date: 2026-11-15
- overall geometric mean: 1.187x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.09x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261115-macm4pro-arm64-python-d8bc6669c7f4bcf1a725-3.16.0a2+dev-d8bc666 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 115 ms: 1.01x slower                                                        |
| docutils       | 1.02 sec                                                 | 918 ms: 1.11x faster                                                        |
| html5lib       | 23.0 ms                                                  | 21.0 ms: 1.10x faster                                                       |
| sphinx         | 434 ms                                                   | 392 ms: 1.11x faster                                                        |
| Geometric mean | (ref)                                                    | 1.08x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261115-macm4pro-arm64-python-d8bc6669c7f4bcf1a725-3.16.0a2+dev-d8bc666 |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_generators                 | 206 ms                                                   | 98.0 ms: 2.11x faster                                                       |
| async_tree_eager_io              | 496 ms                                                   | 270 ms: 1.84x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 284 ms: 1.69x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 276 ms: 1.66x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 282 ms: 1.58x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 113 ms: 1.57x faster                                                        |
| async_tree_none_tg               | 172 ms                                                   | 114 ms: 1.52x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 160 ms: 1.44x faster                                                        |
| coroutines                       | 13.6 ms                                                  | 9.51 ms: 1.43x faster                                                       |
| async_tree_memoization           | 223 ms                                                   | 165 ms: 1.35x faster                                                        |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 270 ms: 1.23x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 276 ms: 1.23x faster                                                        |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.15x faster                                                        |
| async_tree_eager                 | 45.6 ms                                                  | 40.5 ms: 1.13x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                        |
| asyncio_websockets               | 190 ms                                                   | 191 ms: 1.00x slower                                                        |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 253 ms: 1.19x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 144 ms: 1.28x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 95.4 ms: 2.97x slower                                                       |
| Geometric mean                   | (ref)                                                    | 1.23x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261115-macm4pro-arm64-python-d8bc6669c7f4bcf1a725-3.16.0a2+dev-d8bc666 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.5 ms: 1.38x faster                                                       |
| nbody          | 54.2 ms                                                  | 43.3 ms: 1.25x faster                                                       |
| pidigits       | 161 ms                                                   | 151 ms: 1.07x faster                                                        |
| Geometric mean | (ref)                                                    | 1.23x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261115-macm4pro-arm64-python-d8bc6669c7f4bcf1a725-3.16.0a2+dev-d8bc666 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.32 ms: 1.26x faster                                                       |
| regex_dna      | 99.6 ms                                                  | 92.6 ms: 1.08x faster                                                       |
| regex_v8       | 9.59 ms                                                  | 9.15 ms: 1.05x faster                                                       |
| regex_compile  | 54.6 ms                                                  | 54.2 ms: 1.01x faster                                                       |
| Geometric mean | (ref)                                                    | 1.09x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261115-macm4pro-arm64-python-d8bc6669c7f4bcf1a725-3.16.0a2+dev-d8bc666 |
|----------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 41.9 ms: 1.23x faster                                                       |
| json_dumps           | 4.26 ms                                                  | 3.54 ms: 1.20x faster                                                       |
| tomli_loads          | 957 ms                                                   | 830 ms: 1.15x faster                                                        |
| xml_etree_generate   | 38.9 ms                                                  | 34.0 ms: 1.14x faster                                                       |
| unpickle_pure_python | 103 us                                                   | 93.0 us: 1.11x faster                                                       |
| xml_etree_process    | 26.7 ms                                                  | 24.8 ms: 1.08x faster                                                       |
| xml_etree_parse      | 67.9 ms                                                  | 64.9 ms: 1.05x faster                                                       |
| json_loads           | 10.9 us                                                  | 10.7 us: 1.02x faster                                                       |
| Geometric mean       | (ref)                                                    | 1.11x faster                                                                |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261115-macm4pro-arm64-python-d8bc6669c7f4bcf1a725-3.16.0a2+dev-d8bc666 |
|------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.30 ms: 1.04x slower                                                       |
| python_startup_no_site | 5.71 ms                                                  | 6.51 ms: 1.14x slower                                                       |
| Geometric mean         | (ref)                                                    | 1.09x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261115-macm4pro-arm64-python-d8bc6669c7f4bcf1a725-3.16.0a2+dev-d8bc666 |
|-----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.40 ms: 1.09x faster                                                       |
| django_template | 13.6 ms                                                  | 14.7 ms: 1.08x slower                                                       |
| Geometric mean  | (ref)                                                    | 1.00x faster                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261115-macm4pro-arm64-python-d8bc6669c7f4bcf1a725-3.16.0a2+dev-d8bc666 |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.95 ms: 5.26x faster                                                       |
| pylint                           | 128 ms                                                   | 51.4 ms: 2.49x faster                                                       |
| mdp                              | 1.09 sec                                                 | 504 ms: 2.17x faster                                                        |
| async_generators                 | 206 ms                                                   | 98.0 ms: 2.11x faster                                                       |
| async_tree_eager_io              | 496 ms                                                   | 270 ms: 1.84x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 284 ms: 1.69x faster                                                        |
| deepcopy                         | 161 us                                                   | 95.7 us: 1.69x faster                                                       |
| async_tree_io                    | 459 ms                                                   | 276 ms: 1.66x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 282 ms: 1.58x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 113 ms: 1.57x faster                                                        |
| typing_runtime_protocols         | 71.0 us                                                  | 45.4 us: 1.56x faster                                                       |
| deepcopy_memo                    | 18.3 us                                                  | 12.0 us: 1.53x faster                                                       |
| async_tree_none_tg               | 172 ms                                                   | 114 ms: 1.52x faster                                                        |
| comprehensions                   | 9.84 us                                                  | 6.60 us: 1.49x faster                                                       |
| async_tree_memoization_tg        | 231 ms                                                   | 160 ms: 1.44x faster                                                        |
| coroutines                       | 13.6 ms                                                  | 9.51 ms: 1.43x faster                                                       |
| deepcopy_reduce                  | 1.46 us                                                  | 1.04 us: 1.40x faster                                                       |
| float                            | 37.9 ms                                                  | 27.5 ms: 1.38x faster                                                       |
| async_tree_memoization           | 223 ms                                                   | 165 ms: 1.35x faster                                                        |
| go                               | 70.0 ms                                                  | 52.2 ms: 1.34x faster                                                       |
| spectral_norm                    | 54.4 ms                                                  | 41.2 ms: 1.32x faster                                                       |
| scimark_fft                      | 142 ms                                                   | 110 ms: 1.29x faster                                                        |
| raytrace                         | 145 ms                                                   | 113 ms: 1.28x faster                                                        |
| generators                       | 21.9 ms                                                  | 17.2 ms: 1.28x faster                                                       |
| regex_effbot                     | 1.67 ms                                                  | 1.32 ms: 1.26x faster                                                       |
| nqueens                          | 43.5 ms                                                  | 34.4 ms: 1.26x faster                                                       |
| create_gc_cycles                 | 830 us                                                   | 659 us: 1.26x faster                                                        |
| nbody                            | 54.2 ms                                                  | 43.3 ms: 1.25x faster                                                       |
| scimark_sor                      | 61.0 ms                                                  | 48.8 ms: 1.25x faster                                                       |
| scimark_monte_carlo              | 32.2 ms                                                  | 25.9 ms: 1.24x faster                                                       |
| logging_silent                   | 50.9 ns                                                  | 41.1 ns: 1.24x faster                                                       |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 270 ms: 1.23x faster                                                        |
| xml_etree_iterparse              | 51.6 ms                                                  | 41.9 ms: 1.23x faster                                                       |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 276 ms: 1.23x faster                                                        |
| deltablue                        | 1.73 ms                                                  | 1.43 ms: 1.21x faster                                                       |
| json_dumps                       | 4.26 ms                                                  | 3.54 ms: 1.20x faster                                                       |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.87 sec: 1.20x faster                                                      |
| logging_simple                   | 2.57 us                                                  | 2.16 us: 1.19x faster                                                       |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.76 ms: 1.18x faster                                                       |
| chaos                            | 28.9 ms                                                  | 24.6 ms: 1.17x faster                                                       |
| dulwich_log                      | 21.3 ms                                                  | 18.1 ms: 1.17x faster                                                       |
| pyflate                          | 216 ms                                                   | 185 ms: 1.17x faster                                                        |
| logging_format                   | 2.80 us                                                  | 2.41 us: 1.17x faster                                                       |
| hexiom                           | 3.04 ms                                                  | 2.63 ms: 1.16x faster                                                       |
| tomli_loads                      | 957 ms                                                   | 830 ms: 1.15x faster                                                        |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.15x faster                                                        |
| xml_etree_generate               | 38.9 ms                                                  | 34.0 ms: 1.14x faster                                                       |
| k_core                           | 1.12 sec                                                 | 989 ms: 1.13x faster                                                        |
| pathlib                          | 12.4 ms                                                  | 11.0 ms: 1.13x faster                                                       |
| async_tree_eager                 | 45.6 ms                                                  | 40.5 ms: 1.13x faster                                                       |
| richards                         | 22.4 ms                                                  | 20.0 ms: 1.12x faster                                                       |
| scimark_lu                       | 51.3 ms                                                  | 46.0 ms: 1.12x faster                                                       |
| richards_super                   | 25.4 ms                                                  | 22.8 ms: 1.11x faster                                                       |
| docutils                         | 1.02 sec                                                 | 918 ms: 1.11x faster                                                        |
| fannkuch                         | 176 ms                                                   | 158 ms: 1.11x faster                                                        |
| unpickle_pure_python             | 103 us                                                   | 93.0 us: 1.11x faster                                                       |
| sphinx                           | 434 ms                                                   | 392 ms: 1.11x faster                                                        |
| html5lib                         | 23.0 ms                                                  | 21.0 ms: 1.10x faster                                                       |
| sympy_integrate                  | 8.02 ms                                                  | 7.38 ms: 1.09x faster                                                       |
| mako                             | 4.77 ms                                                  | 4.40 ms: 1.09x faster                                                       |
| xml_etree_process                | 26.7 ms                                                  | 24.8 ms: 1.08x faster                                                       |
| regex_dna                        | 99.6 ms                                                  | 92.6 ms: 1.08x faster                                                       |
| pidigits                         | 161 ms                                                   | 151 ms: 1.07x faster                                                        |
| thrift                           | 322 us                                                   | 303 us: 1.06x faster                                                        |
| crypto_pyaes                     | 38.8 ms                                                  | 36.6 ms: 1.06x faster                                                       |
| pycparser                        | 497 ms                                                   | 473 ms: 1.05x faster                                                        |
| regex_v8                         | 9.59 ms                                                  | 9.15 ms: 1.05x faster                                                       |
| sympy_str                        | 104 ms                                                   | 99.6 ms: 1.05x faster                                                       |
| xml_etree_parse                  | 67.9 ms                                                  | 64.9 ms: 1.05x faster                                                       |
| sqlite_synth                     | 967 ns                                                   | 925 ns: 1.05x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                        |
| pprint_safe_repr                 | 328 ms                                                   | 316 ms: 1.04x faster                                                        |
| gc_traversal                     | 2.01 ms                                                  | 1.94 ms: 1.03x faster                                                       |
| bench_thread_pool                | 419 us                                                   | 405 us: 1.03x faster                                                        |
| sympy_sum                        | 57.6 ms                                                  | 55.7 ms: 1.03x faster                                                       |
| pprint_pformat                   | 665 ms                                                   | 644 ms: 1.03x faster                                                        |
| json                             | 1.93 ms                                                  | 1.89 ms: 1.02x faster                                                       |
| json_loads                       | 10.9 us                                                  | 10.7 us: 1.02x faster                                                       |
| regex_compile                    | 54.6 ms                                                  | 54.2 ms: 1.01x faster                                                       |
| asyncio_websockets               | 190 ms                                                   | 191 ms: 1.00x slower                                                        |
| 2to3                             | 114 ms                                                   | 115 ms: 1.01x slower                                                        |
| sympy_expand                     | 167 ms                                                   | 169 ms: 1.01x slower                                                        |
| python_startup                   | 8.01 ms                                                  | 8.30 ms: 1.04x slower                                                       |
| meteor_contest                   | 47.7 ms                                                  | 49.6 ms: 1.04x slower                                                       |
| shortest_path                    | 219 ms                                                   | 229 ms: 1.05x slower                                                        |
| connected_components             | 201 ms                                                   | 211 ms: 1.05x slower                                                        |
| telco                            | 2.61 ms                                                  | 2.81 ms: 1.08x slower                                                       |
| django_template                  | 13.6 ms                                                  | 14.7 ms: 1.08x slower                                                       |
| bench_mp_pool                    | 39.7 ms                                                  | 43.1 ms: 1.08x slower                                                       |
| python_startup_no_site           | 5.71 ms                                                  | 6.51 ms: 1.14x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 253 ms: 1.19x slower                                                        |
| many_optionals                   | 195 us                                                   | 233 us: 1.19x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 144 ms: 1.28x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 95.4 ms: 2.97x slower                                                       |
| Geometric mean                   | (ref)                                                    | 1.18x faster                                                                |

Benchmark hidden because not significant (1): pickle_pure_python
Ignored benchmarks (14) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261115-3.16.0a2+dev-d8bc666/bm-20261115-macm4pro-arm64-python-d8bc6669c7f4bcf1a725-3.16.0a2+dev-d8bc666.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.187x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.11x
- 95% likely to have a speedup of 1.11x
- 99% likely to have a speedup of 1.09x

# Memory
- memory change: 1.15x