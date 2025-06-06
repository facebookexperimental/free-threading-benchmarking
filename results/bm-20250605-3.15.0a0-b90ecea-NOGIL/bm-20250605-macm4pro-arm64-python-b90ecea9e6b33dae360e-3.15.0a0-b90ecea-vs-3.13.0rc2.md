# Results vs. 3.13.0rc2

- fork: python
- ref: b90ecea9e6b33dae360e
- machine: darwin-arm64
- commit hash: b90ecea
- commit date: 2025-06-05
- overall geometric mean: 1.013x faster
- HPT reliability: 70.58%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250605-macm4pro-arm64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 122 ms: 1.09x slower                                                    |
| docutils       | 1.05 sec                                                       | 999 ms: 1.05x faster                                                    |
| html5lib       | 23.1 ms                                                        | 23.4 ms: 1.01x slower                                                   |
| sphinx         | 409 ms                                                         | 417 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.02x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250605-macm4pro-arm64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 194 ms: 2.68x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 204 ms: 2.57x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 198 ms: 2.05x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 210 ms: 1.84x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 87.5 ms: 1.52x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 131 ms: 1.41x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 237 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 246 ms: 1.20x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                    |
| async_generators                 | 193 ms                                                         | 179 ms: 1.08x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.02x faster                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.10x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 229 ms: 1.10x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 49.9 ms: 1.15x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 79.1 ms: 2.73x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.24x faster                                                            |

Benchmark hidden because not significant (1): async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250605-macm4pro-arm64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.9 ms: 1.09x faster                                                   |
| pidigits       | 166 ms                                                         | 163 ms: 1.02x faster                                                    |
| nbody          | 42.5 ms                                                        | 56.2 ms: 1.32x slower                                                   |
| Geometric mean | (ref)                                                          | 1.06x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250605-macm4pro-arm64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.30 ms: 1.15x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 96.9 ms: 1.02x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 53.1 ms: 1.11x slower                                                   |
| Geometric mean | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250605-macm4pro-arm64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 37.4 ms: 1.23x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 56.2 ms: 1.11x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 984 ms: 1.02x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 36.8 ms: 1.03x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.5 us: 1.06x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 27.1 ms: 1.07x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 110 us: 1.11x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 152 us: 1.17x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.01x slower                                                            |

Benchmark hidden because not significant (1): json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250605-macm4pro-arm64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.45 ms: 1.09x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.88 ms: 1.16x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.13x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250605-macm4pro-arm64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.5 ms: 1.10x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.3 ms: 1.13x slower                                                   |
| mako            | 4.41 ms                                                        | 5.64 ms: 1.28x slower                                                   |
| django_template | 12.5 ms                                                        | 16.7 ms: 1.34x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.21x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250605-macm4pro-arm64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 194 ms: 2.68x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 779 us: 2.62x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 204 ms: 2.57x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 198 ms: 2.05x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 487 us: 2.04x faster                                                    |
| mdp                              | 1.06 sec                                                       | 563 ms: 1.88x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 210 ms: 1.84x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 87.5 ms: 1.52x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 124 ms: 1.50x faster                                                    |
| k_core                           | 1.46 sec                                                       | 984 ms: 1.49x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.41x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 131 ms: 1.41x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 237 ms: 1.27x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 37.4 ms: 1.23x faster                                                   |
| deepcopy                         | 145 us                                                         | 121 us: 1.20x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 246 ms: 1.20x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 13.9 us: 1.18x faster                                                   |
| go                               | 72.6 ms                                                        | 62.3 ms: 1.17x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 55.2 ms: 1.16x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 823 ns: 1.15x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.30 ms: 1.15x faster                                                   |
| pyflate                          | 222 ms                                                         | 200 ms: 1.11x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 56.2 ms: 1.11x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                   |
| float                            | 31.4 ms                                                        | 28.9 ms: 1.09x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.96 sec: 1.09x faster                                                  |
| async_generators                 | 193 ms                                                         | 179 ms: 1.08x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.7 ms: 1.06x faster                                                   |
| docutils                         | 1.05 sec                                                       | 999 ms: 1.05x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.25 us: 1.04x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.02x faster                                                   |
| pidigits                         | 166 ms                                                         | 163 ms: 1.02x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 984 ms: 1.02x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 11.2 ms: 1.00x slower                                                   |
| pycparser                        | 470 ms                                                         | 475 ms: 1.01x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 23.4 ms: 1.01x slower                                                   |
| json                             | 1.94 ms                                                        | 1.98 ms: 1.02x slower                                                   |
| fannkuch                         | 179 ms                                                         | 182 ms: 1.02x slower                                                    |
| sphinx                           | 409 ms                                                         | 417 ms: 1.02x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 96.9 ms: 1.02x slower                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 36.8 ms: 1.03x slower                                                   |
| shortest_path                    | 225 ms                                                         | 232 ms: 1.03x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.97 ms: 1.06x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.5 us: 1.06x slower                                                   |
| connected_components             | 208 ms                                                         | 221 ms: 1.06x slower                                                    |
| telco                            | 3.07 ms                                                        | 3.26 ms: 1.06x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 27.1 ms: 1.07x slower                                                   |
| thrift                           | 309 us                                                         | 332 us: 1.08x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.07 ms: 1.08x slower                                                   |
| 2to3                             | 112 ms                                                         | 122 ms: 1.09x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.45 ms: 1.09x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 112 ms: 1.10x slower                                                    |
| richards                         | 22.1 ms                                                        | 24.3 ms: 1.10x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 41.0 ms: 1.10x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 23.5 ms: 1.10x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 229 ms: 1.10x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 110 us: 1.11x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 53.1 ms: 1.11x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 53.3 ms: 1.11x slower                                                   |
| richards_super                   | 24.7 ms                                                        | 27.6 ms: 1.12x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.62 ms: 1.12x slower                                                   |
| pylint                           | 106 ms                                                         | 118 ms: 1.12x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.6 ms: 1.12x slower                                                   |
| genshi_text                      | 9.97 ms                                                        | 11.3 ms: 1.13x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 140 ms: 1.13x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 73.9 us: 1.14x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 109 ms: 1.14x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 49.9 ms: 1.15x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 60.5 ms: 1.16x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.88 ms: 1.16x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 152 us: 1.17x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.98 us: 1.17x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 44.5 ms: 1.18x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 380 ms: 1.18x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 51.7 ms: 1.18x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 189 ms: 1.18x slower                                                    |
| raytrace                         | 109 ms                                                         | 129 ms: 1.19x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 773 ms: 1.19x slower                                                    |
| chaos                            | 24.3 ms                                                        | 29.5 ms: 1.22x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.18 ms: 1.22x slower                                                   |
| generators                       | 15.7 ms                                                        | 19.4 ms: 1.24x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.82 us: 1.26x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 42.7 ms: 1.27x slower                                                   |
| logging_format                   | 2.45 us                                                        | 3.11 us: 1.27x slower                                                   |
| many_optionals                   | 200 us                                                         | 255 us: 1.27x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.64 ms: 1.28x slower                                                   |
| coverage                         | 31.2 ms                                                        | 40.3 ms: 1.29x slower                                                   |
| nbody                            | 42.5 ms                                                        | 56.2 ms: 1.32x slower                                                   |
| django_template                  | 12.5 ms                                                        | 16.7 ms: 1.34x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 591 us: 1.44x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 62.2 ms: 1.46x slower                                                   |
| subparsers                       | 6.26 ms                                                        | 9.84 ms: 1.57x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 79.1 ms: 2.73x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 217 ns: 5.35x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.01x slower                                                            |

Benchmark hidden because not significant (2): json_dumps, async_tree_eager_cpu_io_mixed
Ignored benchmarks (11) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250605-3.15.0a0-b90ecea-NOGIL/bm-20250605-macm4pro-arm64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.013x faster

# HPT report

- Reliability score: 70.58% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.22x