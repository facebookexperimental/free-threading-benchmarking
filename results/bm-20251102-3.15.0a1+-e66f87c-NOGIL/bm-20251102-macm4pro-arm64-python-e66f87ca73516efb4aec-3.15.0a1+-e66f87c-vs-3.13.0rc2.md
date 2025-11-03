# Results vs. 3.13.0rc2

- fork: python
- ref: e66f87ca73516efb4aec
- machine: darwin-arm64
- commit hash: e66f87c
- commit date: 2025-11-02
- overall geometric mean: 1.024x faster
- HPT reliability: 61.96%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.31x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251102-macm4pro-arm64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 119 ms: 1.06x slower                                                     |
| docutils       | 1.05 sec                                                       | 984 ms: 1.06x faster                                                     |
| html5lib       | 23.1 ms                                                        | 22.7 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                          | 1.00x faster                                                             |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251102-macm4pro-arm64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 190 ms: 2.74x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 199 ms: 2.64x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 196 ms: 2.07x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 207 ms: 1.86x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 84.8 ms: 1.56x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 122 ms: 1.52x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 97.5 ms: 1.46x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 128 ms: 1.44x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 231 ms: 1.30x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 238 ms: 1.23x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.13x faster                                                     |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 218 ms: 1.03x faster                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 110 ms: 1.07x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 223 ms: 1.07x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 47.4 ms: 1.10x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 75.5 ms: 2.61x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.27x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251102-macm4pro-arm64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.8 ms: 1.13x faster                                                    |
| pidigits       | 166 ms                                                         | 158 ms: 1.05x faster                                                     |
| nbody          | 42.5 ms                                                        | 54.6 ms: 1.29x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251102-macm4pro-arm64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.42 ms: 1.13x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.46 ms: 1.13x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 92.3 ms: 1.03x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 52.2 ms: 1.09x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251102-macm4pro-arm64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.99 ms: 1.17x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.4 ms: 1.14x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 910 ms: 1.10x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 59.2 ms: 1.05x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.2 ms: 1.04x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.4 us: 1.05x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 27.0 ms: 1.07x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 108 us: 1.09x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 148 us: 1.13x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.01x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251102-macm4pro-arm64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.56 ms: 1.11x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.98 ms: 1.17x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.14x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251102-macm4pro-arm64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.6 ms: 1.10x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.4 ms: 1.14x slower                                                    |
| mako            | 4.41 ms                                                        | 5.62 ms: 1.27x slower                                                    |
| django_template | 12.5 ms                                                        | 16.4 ms: 1.32x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.21x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251102-macm4pro-arm64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 190 ms: 2.74x faster                                                     |
| gc_traversal                     | 2.04 ms                                                        | 748 us: 2.73x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 199 ms: 2.64x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 468 us: 2.12x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 196 ms: 2.07x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 207 ms: 1.86x faster                                                     |
| mdp                              | 1.06 sec                                                       | 600 ms: 1.76x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 84.8 ms: 1.56x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 122 ms: 1.52x faster                                                     |
| k_core                           | 1.46 sec                                                       | 993 ms: 1.47x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 97.5 ms: 1.46x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 128 ms: 1.44x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.5 us: 1.32x faster                                                    |
| deepcopy                         | 145 us                                                         | 111 us: 1.31x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 231 ms: 1.30x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 238 ms: 1.23x faster                                                     |
| go                               | 72.6 ms                                                        | 59.1 ms: 1.23x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 54.4 ms: 1.18x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.99 ms: 1.17x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 818 ns: 1.16x faster                                                     |
| pyflate                          | 222 ms                                                         | 192 ms: 1.15x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.4 ms: 1.14x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 107 ms: 1.13x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.42 ms: 1.13x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.46 ms: 1.13x faster                                                    |
| float                            | 31.4 ms                                                        | 27.8 ms: 1.13x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 910 ms: 1.10x faster                                                     |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.97 sec: 1.08x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.21 us: 1.07x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.6 ms: 1.07x faster                                                    |
| docutils                         | 1.05 sec                                                       | 984 ms: 1.06x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 59.2 ms: 1.05x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.05x faster                                                    |
| pidigits                         | 166 ms                                                         | 158 ms: 1.05x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 218 ms: 1.03x faster                                                     |
| regex_dna                        | 94.6 ms                                                        | 92.3 ms: 1.03x faster                                                    |
| fannkuch                         | 179 ms                                                         | 174 ms: 1.02x faster                                                     |
| pycparser                        | 470 ms                                                         | 461 ms: 1.02x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 22.7 ms: 1.02x faster                                                    |
| telco                            | 3.07 ms                                                        | 3.04 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 532 ms: 1.01x slower                                                     |
| json                             | 1.94 ms                                                        | 1.97 ms: 1.02x slower                                                    |
| shortest_path                    | 225 ms                                                         | 233 ms: 1.04x slower                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 37.2 ms: 1.04x slower                                                    |
| richards                         | 22.1 ms                                                        | 23.1 ms: 1.05x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.4 us: 1.05x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.93 ms: 1.05x slower                                                    |
| 2to3                             | 112 ms                                                         | 119 ms: 1.06x slower                                                     |
| xml_etree_process                | 25.4 ms                                                        | 27.0 ms: 1.07x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 132 ms: 1.07x slower                                                     |
| connected_components             | 208 ms                                                         | 223 ms: 1.07x slower                                                     |
| richards_super                   | 24.7 ms                                                        | 26.5 ms: 1.07x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 110 ms: 1.07x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 223 ms: 1.07x slower                                                     |
| hexiom                           | 2.85 ms                                                        | 3.06 ms: 1.08x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 346 ms: 1.08x slower                                                     |
| thrift                           | 309 us                                                         | 335 us: 1.08x slower                                                     |
| pylint                           | 106 ms                                                         | 115 ms: 1.09x slower                                                     |
| logging_silent                   | 40.6 ns                                                        | 44.1 ns: 1.09x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 706 ms: 1.09x slower                                                     |
| deltablue                        | 1.45 ms                                                        | 1.58 ms: 1.09x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 108 us: 1.09x slower                                                     |
| regex_compile                    | 47.9 ms                                                        | 52.2 ms: 1.09x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 47.4 ms: 1.10x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.46 us: 1.10x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 41.7 ms: 1.10x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 23.6 ms: 1.10x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.0 ms: 1.11x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.71 us: 1.11x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.56 ms: 1.11x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 148 us: 1.13x slower                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 73.7 us: 1.14x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 11.4 ms: 1.14x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 59.9 ms: 1.14x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 50.1 ms: 1.15x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 110 ms: 1.15x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 55.4 ms: 1.16x slower                                                    |
| chaos                            | 24.3 ms                                                        | 28.2 ms: 1.16x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 43.5 ms: 1.17x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.98 ms: 1.17x slower                                                    |
| raytrace                         | 109 ms                                                         | 128 ms: 1.18x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 189 ms: 1.18x slower                                                     |
| generators                       | 15.7 ms                                                        | 18.9 ms: 1.21x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.24 us: 1.21x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 41.8 ms: 1.24x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.24 ms: 1.26x slower                                                    |
| coverage                         | 31.2 ms                                                        | 39.3 ms: 1.26x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.62 ms: 1.27x slower                                                    |
| nbody                            | 42.5 ms                                                        | 54.6 ms: 1.29x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 535 us: 1.30x slower                                                     |
| django_template                  | 12.5 ms                                                        | 16.4 ms: 1.32x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 61.6 ms: 1.44x slower                                                    |
| many_optionals                   | 200 us                                                         | 369 us: 1.84x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 75.5 ms: 2.61x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 18.4 ms: 2.94x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                             |

Benchmark hidden because not significant (1): sphinx
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251102-3.15.0a1+-e66f87c-NOGIL/bm-20251102-macm4pro-arm64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.024x faster

# HPT report

- Reliability score: 61.96% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.31x