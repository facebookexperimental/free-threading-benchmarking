# Results vs. 3.13.0rc2

- fork: python
- ref: 06f8d7aa9f448128d6eb
- machine: darwin-arm64
- commit hash: 06f8d7a
- commit date: 2025-09-04
- overall geometric mean: 1.003x slower
- HPT reliability: 80.13%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250904-macm4pro-arm64-python-06f8d7aa9f448128d6eb-3.15.0a0-06f8d7a |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 126 ms: 1.13x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.00 sec: 1.04x faster                                                  |
| html5lib       | 23.1 ms                                                        | 23.8 ms: 1.03x slower                                                   |
| sphinx         | 409 ms                                                         | 414 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250904-macm4pro-arm64-python-06f8d7aa9f448128d6eb-3.15.0a0-06f8d7a |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 197 ms: 2.64x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 206 ms: 2.54x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 199 ms: 2.03x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 211 ms: 1.83x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 87.8 ms: 1.51x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 125 ms: 1.49x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 131 ms: 1.41x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.39x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 237 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 244 ms: 1.20x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 185 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.00x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.9 ms: 1.01x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 228 ms: 1.10x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 113 ms: 1.10x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 49.8 ms: 1.15x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.9 ms: 2.73x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.23x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250904-macm4pro-arm64-python-06f8d7aa9f448128d6eb-3.15.0a0-06f8d7a |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 30.3 ms: 1.04x faster                                                   |
| pidigits       | 166 ms                                                         | 165 ms: 1.00x faster                                                    |
| nbody          | 42.5 ms                                                        | 56.8 ms: 1.34x slower                                                   |
| Geometric mean | (ref)                                                          | 1.09x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250904-macm4pro-arm64-python-06f8d7aa9f448128d6eb-3.15.0a0-06f8d7a |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.58 ms: 1.12x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 97.6 ms: 1.03x slower                                                   |
| regex_compile  | 47.9 ms                                                        | 53.4 ms: 1.11x slower                                                   |
| Geometric mean | (ref)                                                          | 1.01x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250904-macm4pro-arm64-python-06f8d7aa9f448128d6eb-3.15.0a0-06f8d7a |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 37.6 ms: 1.23x faster                                                   |
| json_dumps           | 4.65 ms                                                        | 4.00 ms: 1.16x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 59.4 ms: 1.05x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 985 ms: 1.01x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.2 ms: 1.04x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.4 us: 1.05x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 27.2 ms: 1.07x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 113 us: 1.14x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 156 us: 1.20x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250904-macm4pro-arm64-python-06f8d7aa9f448128d6eb-3.15.0a0-06f8d7a |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.62 ms: 1.11x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.98 ms: 1.17x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.14x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250904-macm4pro-arm64-python-06f8d7aa9f448128d6eb-3.15.0a0-06f8d7a |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 24.5 ms: 1.15x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 11.8 ms: 1.18x slower                                                   |
| mako            | 4.41 ms                                                        | 5.77 ms: 1.31x slower                                                   |
| django_template | 12.5 ms                                                        | 16.7 ms: 1.34x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.24x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250904-macm4pro-arm64-python-06f8d7aa9f448128d6eb-3.15.0a0-06f8d7a |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 197 ms: 2.64x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 783 us: 2.61x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 206 ms: 2.54x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 480 us: 2.07x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 199 ms: 2.03x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 211 ms: 1.83x faster                                                    |
| mdp                              | 1.06 sec                                                       | 609 ms: 1.74x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 87.8 ms: 1.51x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 125 ms: 1.49x faster                                                    |
| k_core                           | 1.46 sec                                                       | 996 ms: 1.47x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 131 ms: 1.41x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.39x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 237 ms: 1.27x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 37.6 ms: 1.23x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 244 ms: 1.20x faster                                                    |
| deepcopy                         | 145 us                                                         | 122 us: 1.18x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.00 ms: 1.16x faster                                                   |
| go                               | 72.6 ms                                                        | 62.6 ms: 1.16x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 14.2 us: 1.16x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 56.2 ms: 1.14x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 833 ns: 1.14x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.58 ms: 1.12x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| pyflate                          | 222 ms                                                         | 202 ms: 1.10x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.00 sec: 1.06x faster                                                  |
| xml_etree_parse                  | 62.4 ms                                                        | 59.4 ms: 1.05x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.9 ms: 1.05x faster                                                   |
| async_generators                 | 193 ms                                                         | 185 ms: 1.05x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.00 sec: 1.04x faster                                                  |
| float                            | 31.4 ms                                                        | 30.3 ms: 1.04x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                    |
| telco                            | 3.07 ms                                                        | 3.00 ms: 1.02x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 985 ms: 1.01x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.01x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.00x faster                                                    |
| pidigits                         | 166 ms                                                         | 165 ms: 1.00x faster                                                    |
| dask                             | 525 ms                                                         | 527 ms: 1.00x slower                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.31 us: 1.01x slower                                                   |
| coroutines                       | 10.8 ms                                                        | 10.9 ms: 1.01x slower                                                   |
| sphinx                           | 409 ms                                                         | 414 ms: 1.01x slower                                                    |
| json                             | 1.94 ms                                                        | 1.98 ms: 1.02x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 23.8 ms: 1.03x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 97.6 ms: 1.03x slower                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 37.2 ms: 1.04x slower                                                   |
| fannkuch                         | 179 ms                                                         | 186 ms: 1.04x slower                                                    |
| shortest_path                    | 225 ms                                                         | 235 ms: 1.05x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.4 us: 1.05x slower                                                   |
| connected_components             | 208 ms                                                         | 222 ms: 1.07x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 27.2 ms: 1.07x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 8.09 ms: 1.08x slower                                                   |
| richards                         | 22.1 ms                                                        | 24.0 ms: 1.09x slower                                                   |
| thrift                           | 309 us                                                         | 339 us: 1.10x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 228 ms: 1.10x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 113 ms: 1.10x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 356 ms: 1.11x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 27.4 ms: 1.11x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 9.62 ms: 1.11x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 53.4 ms: 1.11x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 725 ms: 1.12x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.18 ms: 1.12x slower                                                   |
| 2to3                             | 112 ms                                                         | 126 ms: 1.13x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 45.8 ns: 1.13x slower                                                   |
| pylint                           | 106 ms                                                         | 119 ms: 1.13x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.54 us: 1.13x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 113 us: 1.14x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 43.0 ms: 1.14x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 34.3 ms: 1.15x slower                                                   |
| genshi_xml                       | 21.4 ms                                                        | 24.5 ms: 1.15x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 74.4 us: 1.15x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 1.67 ms: 1.15x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.82 us: 1.15x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 49.8 ms: 1.15x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.98 ms: 1.17x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 61.7 ms: 1.18x slower                                                   |
| genshi_text                      | 9.97 ms                                                        | 11.8 ms: 1.18x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 113 ms: 1.18x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 44.1 ms: 1.18x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 147 ms: 1.19x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 57.2 ms: 1.20x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 156 us: 1.20x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 52.4 ms: 1.20x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 193 ms: 1.21x slower                                                    |
| chaos                            | 24.3 ms                                                        | 29.6 ms: 1.22x slower                                                   |
| raytrace                         | 109 ms                                                         | 133 ms: 1.22x slower                                                    |
| generators                       | 15.7 ms                                                        | 19.4 ms: 1.24x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 8.44 us: 1.24x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 43.1 ms: 1.28x slower                                                   |
| coverage                         | 31.2 ms                                                        | 40.1 ms: 1.28x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.77 ms: 1.31x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.33 ms: 1.31x slower                                                   |
| django_template                  | 12.5 ms                                                        | 16.7 ms: 1.34x slower                                                   |
| nbody                            | 42.5 ms                                                        | 56.8 ms: 1.34x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 57.3 ms: 1.34x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 586 us: 1.42x slower                                                    |
| many_optionals                   | 200 us                                                         | 338 us: 1.69x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.9 ms: 2.73x slower                                                   |
| subparsers                       | 6.26 ms                                                        | 18.7 ms: 2.98x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.01x slower                                                            |

Benchmark hidden because not significant (1): pycparser
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250904-3.15.0a0-06f8d7a-NOGIL/bm-20250904-macm4pro-arm64-python-06f8d7aa9f448128d6eb-3.15.0a0-06f8d7a.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.003x slower

# HPT report

- Reliability score: 80.13% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.20x