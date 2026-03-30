# Results vs. 3.12.6

- fork: python
- ref: 4d0e8ee649ceff96b130
- machine: darwin-arm64
- commit hash: 4d0e8ee
- commit date: 2026-03-29
- overall geometric mean: 1.108x faster
- HPT reliability: 99.96%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.38x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260329-macm4pro-arm64-python-4d0e8ee649ceff96b130-3.15.0a7+-4d0e8ee |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 120 ms: 1.05x slower                                                     |
| docutils       | 1.02 sec                                                 | 980 ms: 1.04x faster                                                     |
| html5lib       | 23.0 ms                                                  | 22.6 ms: 1.02x faster                                                    |
| sphinx         | 434 ms                                                   | 417 ms: 1.04x faster                                                     |
| Geometric mean | (ref)                                                    | 1.01x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260329-macm4pro-arm64-python-4d0e8ee649ceff96b130-3.15.0a7+-4d0e8ee |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 240 ms: 2.07x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 234 ms: 2.05x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 239 ms: 1.92x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 235 ms: 1.89x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.63x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 142 ms: 1.62x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 114 ms: 1.57x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 147 ms: 1.51x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 254 ms: 1.33x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 260 ms: 1.28x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.8 ms: 1.26x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 113 ms: 1.17x faster                                                     |
| async_generators                 | 206 ms                                                   | 183 ms: 1.13x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 182 ms: 1.05x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.04x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 46.7 ms: 1.02x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 240 ms: 1.13x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 128 ms: 1.14x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 91.6 ms: 2.85x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.26x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260329-macm4pro-arm64-python-4d0e8ee649ceff96b130-3.15.0a7+-4d0e8ee |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.3 ms: 1.34x faster                                                    |
| pidigits       | 161 ms                                                   | 160 ms: 1.00x faster                                                     |
| nbody          | 54.2 ms                                                  | 57.0 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                    | 1.09x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260329-macm4pro-arm64-python-4d0e8ee649ceff96b130-3.15.0a7+-4d0e8ee |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 50.6 ms: 1.08x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 94.7 ms: 1.05x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.29 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260329-macm4pro-arm64-python-4d0e8ee649ceff96b130-3.15.0a7+-4d0e8ee |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.0 ms: 1.29x faster                                                    |
| tomli_loads          | 957 ms                                                   | 845 ms: 1.13x faster                                                     |
| xml_etree_parse      | 67.9 ms                                                  | 60.5 ms: 1.12x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.89 ms: 1.10x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 36.9 ms: 1.05x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 145 us: 1.04x slower                                                     |
| json_loads           | 10.9 us                                                  | 11.3 us: 1.04x slower                                                    |
| unpickle_pure_python | 103 us                                                   | 108 us: 1.05x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.06x faster                                                             |

Benchmark hidden because not significant (1): xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260329-macm4pro-arm64-python-4d0e8ee649ceff96b130-3.15.0a7+-4d0e8ee |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.68 ms: 1.21x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.05 ms: 1.24x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.22x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260329-macm4pro-arm64-python-4d0e8ee649ceff96b130-3.15.0a7+-4d0e8ee |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 22.4 ms: 1.03x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 10.9 ms: 1.04x slower                                                    |
| django_template | 13.6 ms                                                  | 15.4 ms: 1.13x slower                                                    |
| mako            | 4.77 ms                                                  | 5.55 ms: 1.16x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.09x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260329-macm4pro-arm64-python-4d0e8ee649ceff96b130-3.15.0a7+-4d0e8ee |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.04 ms: 5.13x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 780 us: 2.58x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 240 ms: 2.07x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 234 ms: 2.05x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 239 ms: 1.92x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 235 ms: 1.89x faster                                                     |
| mdp                              | 1.09 sec                                                 | 596 ms: 1.83x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 497 us: 1.67x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.63x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 142 ms: 1.62x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 114 ms: 1.57x faster                                                     |
| deepcopy                         | 161 us                                                   | 105 us: 1.54x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 147 ms: 1.51x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.4 us: 1.48x faster                                                    |
| float                            | 37.9 ms                                                  | 28.3 ms: 1.34x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 254 ms: 1.33x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.13 us: 1.29x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.0 ms: 1.29x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 260 ms: 1.28x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.8 ms: 1.26x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 786 ns: 1.23x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 8.27 us: 1.19x faster                                                    |
| go                               | 70.0 ms                                                  | 58.9 ms: 1.19x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 113 ms: 1.17x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 18.3 ms: 1.16x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.93 sec: 1.16x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.7 ms: 1.16x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 44.0 ns: 1.16x faster                                                    |
| raytrace                         | 145 ms                                                   | 126 ms: 1.15x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 125 ms: 1.14x faster                                                     |
| tomli_loads                      | 957 ms                                                   | 845 ms: 1.13x faster                                                     |
| k_core                           | 1.12 sec                                                 | 987 ms: 1.13x faster                                                     |
| async_generators                 | 206 ms                                                   | 183 ms: 1.13x faster                                                     |
| pyflate                          | 216 ms                                                   | 191 ms: 1.13x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 54.0 ms: 1.13x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 60.5 ms: 1.12x faster                                                    |
| pylint                           | 128 ms                                                   | 116 ms: 1.10x faster                                                     |
| logging_simple                   | 2.57 us                                                  | 2.33 us: 1.10x faster                                                    |
| pycparser                        | 497 ms                                                   | 453 ms: 1.10x faster                                                     |
| json_dumps                       | 4.26 ms                                                  | 3.89 ms: 1.10x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.59 us: 1.08x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 50.3 ms: 1.08x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 50.6 ms: 1.08x faster                                                    |
| chaos                            | 28.9 ms                                                  | 26.9 ms: 1.07x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 40.8 ms: 1.07x faster                                                    |
| generators                       | 21.9 ms                                                  | 20.8 ms: 1.05x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 36.9 ms: 1.05x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 94.7 ms: 1.05x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.65 ms: 1.05x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 182 ms: 1.05x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.04x faster                                                     |
| docutils                         | 1.02 sec                                                 | 980 ms: 1.04x faster                                                     |
| sphinx                           | 434 ms                                                   | 417 ms: 1.04x faster                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.29 ms: 1.03x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 22.6 ms: 1.02x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 325 ms: 1.01x faster                                                     |
| pidigits                         | 161 ms                                                   | 160 ms: 1.00x faster                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 7.99 ms: 1.00x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 663 ms: 1.00x faster                                                     |
| dask                             | 528 ms                                                   | 530 ms: 1.00x slower                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 32.4 ms: 1.01x slower                                                    |
| json                             | 1.93 ms                                                  | 1.96 ms: 1.02x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 46.7 ms: 1.02x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 22.4 ms: 1.03x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 73.1 us: 1.03x slower                                                    |
| richards                         | 22.4 ms                                                  | 23.1 ms: 1.03x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.14 ms: 1.03x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.15 ms: 1.04x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 53.3 ms: 1.04x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 26.5 ms: 1.04x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 10.9 ms: 1.04x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 145 us: 1.04x slower                                                     |
| json_loads                       | 10.9 us                                                  | 11.3 us: 1.04x slower                                                    |
| sympy_str                        | 104 ms                                                   | 109 ms: 1.05x slower                                                     |
| 2to3                             | 114 ms                                                   | 120 ms: 1.05x slower                                                     |
| sympy_sum                        | 57.6 ms                                                  | 60.4 ms: 1.05x slower                                                    |
| nbody                            | 54.2 ms                                                  | 57.0 ms: 1.05x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 108 us: 1.05x slower                                                     |
| thrift                           | 322 us                                                   | 342 us: 1.06x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 187 ms: 1.12x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 240 ms: 1.13x slower                                                     |
| django_template                  | 13.6 ms                                                  | 15.4 ms: 1.13x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 44.1 ms: 1.13x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 128 ms: 1.14x slower                                                     |
| telco                            | 2.61 ms                                                  | 2.98 ms: 1.14x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 54.6 ms: 1.14x slower                                                    |
| shortest_path                    | 219 ms                                                   | 250 ms: 1.14x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 45.8 ms: 1.15x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.55 ms: 1.16x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.68 ms: 1.21x slower                                                    |
| connected_components             | 201 ms                                                   | 244 ms: 1.22x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 7.05 ms: 1.24x slower                                                    |
| many_optionals                   | 195 us                                                   | 260 us: 1.33x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 572 us: 1.37x slower                                                     |
| coverage                         | 26.9 ms                                                  | 38.6 ms: 1.43x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 91.6 ms: 2.85x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                             |

Benchmark hidden because not significant (2): xml_etree_process, fannkuch
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260329-3.15.0a7+-4d0e8ee-NOGIL/bm-20260329-macm4pro-arm64-python-4d0e8ee649ceff96b130-3.15.0a7+-4d0e8ee.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.108x faster

# HPT report

- Reliability score: 99.96% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.38x