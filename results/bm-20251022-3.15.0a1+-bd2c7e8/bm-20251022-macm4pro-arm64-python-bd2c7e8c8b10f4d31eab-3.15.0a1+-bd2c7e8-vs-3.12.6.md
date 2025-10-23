# Results vs. 3.12.6

- fork: python
- ref: bd2c7e8c8b10f4d31eab
- machine: darwin-arm64
- commit hash: bd2c7e8
- commit date: 2025-10-22
- overall geometric mean: 1.084x faster
- HPT reliability: 99.78%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251022-macm4pro-arm64-python-bd2c7e8c8b10f4d31eab-3.15.0a1+-bd2c7e8 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 116 ms: 1.02x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                   |
| html5lib       | 23.0 ms                                                  | 23.8 ms: 1.03x slower                                                    |
| sphinx         | 434 ms                                                   | 408 ms: 1.06x faster                                                     |
| Geometric mean | (ref)                                                    | 1.00x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251022-macm4pro-arm64-python-bd2c7e8c8b10f4d31eab-3.15.0a1+-bd2c7e8 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 233 ms: 2.12x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 231 ms: 2.08x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 236 ms: 1.95x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 231 ms: 1.93x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 103 ms: 1.67x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 108 ms: 1.66x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 142 ms: 1.63x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 145 ms: 1.54x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 254 ms: 1.33x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 255 ms: 1.31x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.5 ms: 1.29x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.21x faster                                                     |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.03x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 44.4 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 127 ms: 1.13x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 241 ms: 1.13x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 84.6 ms: 2.63x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.28x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251022-macm4pro-arm64-python-bd2c7e8c8b10f4d31eab-3.15.0a1+-bd2c7e8 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 30.7 ms: 1.23x faster                                                    |
| nbody          | 54.2 ms                                                  | 51.6 ms: 1.05x faster                                                    |
| pidigits       | 161 ms                                                   | 165 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251022-macm4pro-arm64-python-bd2c7e8c8b10f4d31eab-3.15.0a1+-bd2c7e8 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.43 ms: 1.17x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 51.4 ms: 1.06x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 94.8 ms: 1.05x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.87 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                    | 1.06x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251022-macm4pro-arm64-python-bd2c7e8c8b10f4d31eab-3.15.0a1+-bd2c7e8 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.4 ms: 1.28x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 36.3 ms: 1.07x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 4.01 ms: 1.06x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 64.1 ms: 1.06x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 26.2 ms: 1.02x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.9 us: 1.01x slower                                                    |
| tomli_loads          | 957 ms                                                   | 974 ms: 1.02x slower                                                     |
| unpickle_pure_python | 103 us                                                   | 105 us: 1.02x slower                                                     |
| pickle_pure_python   | 139 us                                                   | 155 us: 1.11x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.03x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251022-macm4pro-arm64-python-bd2c7e8c8b10f4d31eab-3.15.0a1+-bd2c7e8 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 5.71 ms                                                  | 6.29 ms: 1.10x slower                                                    |
| python_startup         | 8.01 ms                                                  | 8.88 ms: 1.11x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.11x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251022-macm4pro-arm64-python-bd2c7e8c8b10f4d31eab-3.15.0a1+-bd2c7e8 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 5.05 ms: 1.06x slower                                                    |
| genshi_xml      | 21.8 ms                                                  | 23.2 ms: 1.06x slower                                                    |
| django_template | 13.6 ms                                                  | 15.9 ms: 1.17x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.07x slower                                                             |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251022-macm4pro-arm64-python-bd2c7e8c8b10f4d31eab-3.15.0a1+-bd2c7e8 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 233 ms: 2.12x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 231 ms: 2.08x faster                                                     |
| mdp                              | 1.09 sec                                                 | 547 ms: 2.00x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 236 ms: 1.95x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 231 ms: 1.93x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 103 ms: 1.67x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 108 ms: 1.66x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 142 ms: 1.63x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 145 ms: 1.54x faster                                                     |
| deepcopy                         | 161 us                                                   | 113 us: 1.43x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 13.1 us: 1.40x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 254 ms: 1.33x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 255 ms: 1.31x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.5 ms: 1.29x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.4 ms: 1.28x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.76 us: 1.27x faster                                                    |
| float                            | 37.9 ms                                                  | 30.7 ms: 1.23x faster                                                    |
| k_core                           | 1.12 sec                                                 | 907 ms: 1.23x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 44.4 ms: 1.22x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.20 us: 1.22x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.21x faster                                                     |
| generators                       | 21.9 ms                                                  | 18.3 ms: 1.20x faster                                                    |
| raytrace                         | 145 ms                                                   | 123 ms: 1.18x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.43 ms: 1.17x faster                                                    |
| go                               | 70.0 ms                                                  | 60.3 ms: 1.16x faster                                                    |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                     |
| subparsers                       | 20.8 ms                                                  | 18.1 ms: 1.15x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 44.6 ns: 1.14x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.53 ms: 1.13x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.0 ms: 1.13x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 54.1 ms: 1.13x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.85 ms: 1.12x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 130 ms: 1.09x faster                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.06 sec: 1.09x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 19.6 ms: 1.09x faster                                                    |
| pylint                           | 128 ms                                                   | 118 ms: 1.08x faster                                                     |
| nqueens                          | 43.5 ms                                                  | 40.3 ms: 1.08x faster                                                    |
| pyflate                          | 216 ms                                                   | 202 ms: 1.07x faster                                                     |
| xml_etree_generate               | 38.9 ms                                                  | 36.3 ms: 1.07x faster                                                    |
| chaos                            | 28.9 ms                                                  | 27.1 ms: 1.07x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.63 us: 1.06x faster                                                    |
| sphinx                           | 434 ms                                                   | 408 ms: 1.06x faster                                                     |
| logging_simple                   | 2.57 us                                                  | 2.42 us: 1.06x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 4.01 ms: 1.06x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 51.4 ms: 1.06x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 64.1 ms: 1.06x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.60 ms: 1.06x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 67.2 us: 1.06x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 94.8 ms: 1.05x faster                                                    |
| nbody                            | 54.2 ms                                                  | 51.6 ms: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.03x faster                                                     |
| hexiom                           | 3.04 ms                                                  | 2.95 ms: 1.03x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 49.8 ms: 1.03x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 44.4 ms: 1.03x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 38.0 ms: 1.02x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 26.2 ms: 1.02x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 31.6 ms: 1.02x faster                                                    |
| pycparser                        | 497 ms                                                   | 492 ms: 1.01x faster                                                     |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                     |
| bench_thread_pool                | 419 us                                                   | 420 us: 1.00x slower                                                     |
| json                             | 1.93 ms                                                  | 1.95 ms: 1.01x slower                                                    |
| json_loads                       | 10.9 us                                                  | 10.9 us: 1.01x slower                                                    |
| richards                         | 22.4 ms                                                  | 22.6 ms: 1.01x slower                                                    |
| sqlite_synth                     | 967 ns                                                   | 981 ns: 1.01x slower                                                     |
| tomli_loads                      | 957 ms                                                   | 974 ms: 1.02x slower                                                     |
| unpickle_pure_python             | 103 us                                                   | 105 us: 1.02x slower                                                     |
| 2to3                             | 114 ms                                                   | 116 ms: 1.02x slower                                                     |
| shortest_path                    | 219 ms                                                   | 224 ms: 1.02x slower                                                     |
| pidigits                         | 161 ms                                                   | 165 ms: 1.02x slower                                                     |
| docutils                         | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                   |
| gc_traversal                     | 2.01 ms                                                  | 2.07 ms: 1.03x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.87 ms: 1.03x slower                                                    |
| connected_components             | 201 ms                                                   | 207 ms: 1.03x slower                                                     |
| html5lib                         | 23.0 ms                                                  | 23.8 ms: 1.03x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 691 ms: 1.04x slower                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 341 ms: 1.04x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 50.1 ms: 1.05x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 41.7 ms: 1.05x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.05 ms: 1.06x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 23.2 ms: 1.06x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 178 ms: 1.07x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 6.29 ms: 1.10x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.88 ms: 1.11x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 155 us: 1.11x slower                                                     |
| create_gc_cycles                 | 830 us                                                   | 926 us: 1.12x slower                                                     |
| fannkuch                         | 176 ms                                                   | 197 ms: 1.12x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 127 ms: 1.13x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 241 ms: 1.13x slower                                                     |
| telco                            | 2.61 ms                                                  | 2.98 ms: 1.14x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.9 ms: 1.17x slower                                                    |
| coverage                         | 26.9 ms                                                  | 31.8 ms: 1.18x slower                                                    |
| many_optionals                   | 195 us                                                   | 370 us: 1.90x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 84.6 ms: 2.63x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                             |

Benchmark hidden because not significant (5): thrift, genshi_text, richards_super, sympy_sum, sympy_str
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251022-3.15.0a1+-bd2c7e8/bm-20251022-macm4pro-arm64-python-bd2c7e8c8b10f4d31eab-3.15.0a1+-bd2c7e8.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.084x faster

# HPT report

- Reliability score: 99.78% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.20x