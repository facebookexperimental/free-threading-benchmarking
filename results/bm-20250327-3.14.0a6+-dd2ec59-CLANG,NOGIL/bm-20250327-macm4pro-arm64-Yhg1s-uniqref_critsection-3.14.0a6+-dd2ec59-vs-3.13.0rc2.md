# Results vs. 3.13.0rc2

- fork: Yhg1s
- ref: uniqref_critsection
- machine: darwin-arm64
- commit hash: dd2ec59
- commit date: 2025-03-27
- overall geometric mean: 1.049x faster
- HPT reliability: 66.15%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250327-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6+-dd2ec59 |
|----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 112 ms: 1.01x slower                                                   |
| docutils       | 1.05 sec                                                       | 967 ms: 1.08x faster                                                   |
| html5lib       | 23.1 ms                                                        | 22.3 ms: 1.04x faster                                                  |
| sphinx         | 409 ms                                                         | 402 ms: 1.02x faster                                                   |
| Geometric mean | (ref)                                                          | 1.03x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250327-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6+-dd2ec59 |
|----------------------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 183 ms: 2.84x faster                                                   |
| async_tree_eager_io              | 525 ms                                                         | 196 ms: 2.68x faster                                                   |
| async_tree_io_tg                 | 405 ms                                                         | 189 ms: 2.14x faster                                                   |
| async_tree_io                    | 386 ms                                                         | 204 ms: 1.89x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 82.7 ms: 1.60x faster                                                  |
| async_tree_memoization_tg        | 186 ms                                                         | 120 ms: 1.54x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 98.1 ms: 1.45x faster                                                  |
| async_tree_memoization           | 184 ms                                                         | 128 ms: 1.44x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 227 ms: 1.33x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 236 ms: 1.24x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 9.17 ms: 1.17x faster                                                  |
| async_generators                 | 193 ms                                                         | 167 ms: 1.15x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.13x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 216 ms: 1.04x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 219 ms: 1.05x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 109 ms: 1.06x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 46.2 ms: 1.07x slower                                                  |
| async_tree_eager_tg              | 28.9 ms                                                        | 74.0 ms: 2.56x slower                                                  |
| Geometric mean                   | (ref)                                                          | 1.30x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250327-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6+-dd2ec59 |
|----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.8 ms: 1.09x faster                                                  |
| pidigits       | 166 ms                                                         | 163 ms: 1.02x faster                                                   |
| nbody          | 42.5 ms                                                        | 61.3 ms: 1.44x slower                                                  |
| Geometric mean | (ref)                                                          | 1.09x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250327-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6+-dd2ec59 |
|----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.50 ms: 1.08x faster                                                  |
| regex_v8       | 10.7 ms                                                        | 10.1 ms: 1.05x faster                                                  |
| regex_compile  | 47.9 ms                                                        | 49.4 ms: 1.03x slower                                                  |
| regex_dna      | 94.6 ms                                                        | 102 ms: 1.08x slower                                                   |
| Geometric mean | (ref)                                                          | 1.01x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250327-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6+-dd2ec59 |
|----------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 36.4 ms: 1.27x faster                                                  |
| tomli_loads          | 1000 ms                                                        | 884 ms: 1.13x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 56.6 ms: 1.10x faster                                                  |
| xml_etree_generate   | 35.8 ms                                                        | 33.8 ms: 1.06x faster                                                  |
| xml_etree_process    | 25.4 ms                                                        | 24.9 ms: 1.02x faster                                                  |
| unpickle_pure_python | 99.5 us                                                        | 99.2 us: 1.00x faster                                                  |
| json_loads           | 10.8 us                                                        | 11.6 us: 1.07x slower                                                  |
| pickle_pure_python   | 130 us                                                         | 141 us: 1.08x slower                                                   |
| json_dumps           | 4.65 ms                                                        | 5.06 ms: 1.09x slower                                                  |
| Geometric mean       | (ref)                                                          | 1.03x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250327-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6+-dd2ec59 |
|------------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.21 ms: 1.07x slower                                                  |
| python_startup_no_site | 5.95 ms                                                        | 7.28 ms: 1.22x slower                                                  |
| Geometric mean         | (ref)                                                          | 1.14x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250327-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6+-dd2ec59 |
|-----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 20.9 ms: 1.02x faster                                                  |
| genshi_text     | 9.97 ms                                                        | 10.6 ms: 1.06x slower                                                  |
| django_template | 12.5 ms                                                        | 15.2 ms: 1.22x slower                                                  |
| mako            | 4.41 ms                                                        | 5.46 ms: 1.24x slower                                                  |
| Geometric mean  | (ref)                                                          | 1.12x slower                                                           |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250327-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6+-dd2ec59 |
|----------------------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 183 ms: 2.84x faster                                                   |
| gc_traversal                     | 2.04 ms                                                        | 758 us: 2.69x faster                                                   |
| async_tree_eager_io              | 525 ms                                                         | 196 ms: 2.68x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 458 us: 2.17x faster                                                   |
| async_tree_io_tg                 | 405 ms                                                         | 189 ms: 2.14x faster                                                   |
| async_tree_io                    | 386 ms                                                         | 204 ms: 1.89x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 82.7 ms: 1.60x faster                                                  |
| async_tree_memoization_tg        | 186 ms                                                         | 120 ms: 1.54x faster                                                   |
| k_core                           | 1.46 sec                                                       | 1.01 sec: 1.45x faster                                                 |
| async_tree_none                  | 142 ms                                                         | 98.1 ms: 1.45x faster                                                  |
| async_tree_memoization           | 184 ms                                                         | 128 ms: 1.44x faster                                                   |
| deepcopy                         | 145 us                                                         | 109 us: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 227 ms: 1.33x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 36.4 ms: 1.27x faster                                                  |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 236 ms: 1.24x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 13.3 us: 1.24x faster                                                  |
| go                               | 72.6 ms                                                        | 58.4 ms: 1.24x faster                                                  |
| scimark_sor                      | 64.0 ms                                                        | 54.4 ms: 1.18x faster                                                  |
| coroutines                       | 10.8 ms                                                        | 9.17 ms: 1.17x faster                                                  |
| sqlite_synth                     | 948 ns                                                         | 810 ns: 1.17x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.11 us: 1.17x faster                                                  |
| async_generators                 | 193 ms                                                         | 167 ms: 1.15x faster                                                   |
| pyflate                          | 222 ms                                                         | 196 ms: 1.14x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 884 ms: 1.13x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.13x faster                                                   |
| generators                       | 15.7 ms                                                        | 13.9 ms: 1.13x faster                                                  |
| dulwich_log                      | 19.8 ms                                                        | 17.8 ms: 1.11x faster                                                  |
| xml_etree_parse                  | 62.4 ms                                                        | 56.6 ms: 1.10x faster                                                  |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.94 sec: 1.10x faster                                                 |
| float                            | 31.4 ms                                                        | 28.8 ms: 1.09x faster                                                  |
| docutils                         | 1.05 sec                                                       | 967 ms: 1.08x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.50 ms: 1.08x faster                                                  |
| xml_etree_generate               | 35.8 ms                                                        | 33.8 ms: 1.06x faster                                                  |
| regex_v8                         | 10.7 ms                                                        | 10.1 ms: 1.05x faster                                                  |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 216 ms: 1.04x faster                                                   |
| html5lib                         | 23.1 ms                                                        | 22.3 ms: 1.04x faster                                                  |
| pycparser                        | 470 ms                                                         | 453 ms: 1.04x faster                                                   |
| genshi_xml                       | 21.4 ms                                                        | 20.9 ms: 1.02x faster                                                  |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                   |
| xml_etree_process                | 25.4 ms                                                        | 24.9 ms: 1.02x faster                                                  |
| sphinx                           | 409 ms                                                         | 402 ms: 1.02x faster                                                   |
| pidigits                         | 166 ms                                                         | 163 ms: 1.02x faster                                                   |
| json                             | 1.94 ms                                                        | 1.92 ms: 1.01x faster                                                  |
| unpickle_pure_python             | 99.5 us                                                        | 99.2 us: 1.00x faster                                                  |
| 2to3                             | 112 ms                                                         | 112 ms: 1.01x slower                                                   |
| richards                         | 22.1 ms                                                        | 22.3 ms: 1.01x slower                                                  |
| hexiom                           | 2.85 ms                                                        | 2.93 ms: 1.03x slower                                                  |
| regex_compile                    | 47.9 ms                                                        | 49.4 ms: 1.03x slower                                                  |
| bench_mp_pool                    | 37.8 ms                                                        | 39.1 ms: 1.03x slower                                                  |
| richards_super                   | 24.7 ms                                                        | 25.6 ms: 1.04x slower                                                  |
| sympy_integrate                  | 7.53 ms                                                        | 7.87 ms: 1.05x slower                                                  |
| mdp                              | 1.06 sec                                                       | 1.11 sec: 1.05x slower                                                 |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 219 ms: 1.05x slower                                                   |
| fannkuch                         | 179 ms                                                         | 188 ms: 1.05x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 42.8 ns: 1.05x slower                                                  |
| shortest_path                    | 225 ms                                                         | 237 ms: 1.06x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.37 us: 1.06x slower                                                  |
| pprint_safe_repr                 | 322 ms                                                         | 341 ms: 1.06x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.60 us: 1.06x slower                                                  |
| nqueens                          | 37.2 ms                                                        | 39.5 ms: 1.06x slower                                                  |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 109 ms: 1.06x slower                                                   |
| genshi_text                      | 9.97 ms                                                        | 10.6 ms: 1.06x slower                                                  |
| python_startup                   | 8.63 ms                                                        | 9.21 ms: 1.07x slower                                                  |
| deltablue                        | 1.45 ms                                                        | 1.55 ms: 1.07x slower                                                  |
| async_tree_eager                 | 43.2 ms                                                        | 46.2 ms: 1.07x slower                                                  |
| json_loads                       | 10.8 us                                                        | 11.6 us: 1.07x slower                                                  |
| pprint_pformat                   | 650 ms                                                         | 696 ms: 1.07x slower                                                   |
| sqlalchemy_declarative           | 44.4 ms                                                        | 47.6 ms: 1.07x slower                                                  |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.39 ms: 1.08x slower                                                  |
| pylint                           | 106 ms                                                         | 114 ms: 1.08x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 102 ms: 1.08x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 141 us: 1.08x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 70.1 us: 1.08x slower                                                  |
| json_dumps                       | 4.65 ms                                                        | 5.06 ms: 1.09x slower                                                  |
| telco                            | 3.07 ms                                                        | 3.34 ms: 1.09x slower                                                  |
| sympy_sum                        | 52.3 ms                                                        | 57.1 ms: 1.09x slower                                                  |
| sympy_str                        | 95.5 ms                                                        | 104 ms: 1.09x slower                                                   |
| connected_components             | 208 ms                                                         | 229 ms: 1.10x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 175 ms: 1.10x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.1 ms: 1.11x slower                                                  |
| meteor_contest                   | 47.9 ms                                                        | 53.5 ms: 1.12x slower                                                  |
| many_optionals                   | 200 us                                                         | 228 us: 1.14x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 141 ms: 1.14x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 49.9 ms: 1.14x slower                                                  |
| chaos                            | 24.3 ms                                                        | 28.0 ms: 1.15x slower                                                  |
| comprehensions                   | 6.80 us                                                        | 7.89 us: 1.16x slower                                                  |
| crypto_pyaes                     | 33.6 ms                                                        | 39.7 ms: 1.18x slower                                                  |
| raytrace                         | 109 ms                                                         | 130 ms: 1.19x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 50.9 ms: 1.19x slower                                                  |
| django_template                  | 12.5 ms                                                        | 15.2 ms: 1.22x slower                                                  |
| python_startup_no_site           | 5.95 ms                                                        | 7.28 ms: 1.22x slower                                                  |
| mako                             | 4.41 ms                                                        | 5.46 ms: 1.24x slower                                                  |
| coverage                         | 31.2 ms                                                        | 38.6 ms: 1.24x slower                                                  |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.21 ms: 1.24x slower                                                  |
| subparsers                       | 6.26 ms                                                        | 8.29 ms: 1.32x slower                                                  |
| bench_thread_pool                | 412 us                                                         | 581 us: 1.41x slower                                                   |
| nbody                            | 42.5 ms                                                        | 61.3 ms: 1.44x slower                                                  |
| async_tree_eager_tg              | 28.9 ms                                                        | 74.0 ms: 2.56x slower                                                  |
| Geometric mean                   | (ref)                                                          | 1.04x faster                                                           |

Benchmark hidden because not significant (2): thrift, pathlib
Ignored benchmarks (9) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250327-3.14.0a6+-dd2ec59-CLANG,NOGIL/bm-20250327-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6+-dd2ec59.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.049x faster

# HPT report

- Reliability score: 66.15% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.18x