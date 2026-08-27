# Results vs. 3.13.0rc2

- fork: python
- ref: fe3a26f43fad1d6eed20
- machine: darwin-arm64
- commit hash: fe3a26f
- commit date: 2026-08-26
- overall geometric mean: 1.060x slower
- HPT reliability: 99.62%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.28x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260826-macm4pro-arm64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 137 ms: 1.23x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.10 sec: 1.05x slower                                                  |
| html5lib       | 23.1 ms                                                        | 24.2 ms: 1.05x slower                                                   |
| sphinx         | 409 ms                                                         | 459 ms: 1.12x slower                                                    |
| Geometric mean | (ref)                                                          | 1.11x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260826-macm4pro-arm64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 311 ms: 1.67x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 315 ms: 1.67x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 315 ms: 1.29x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 320 ms: 1.21x faster                                                    |
| async_generators                 | 193 ms                                                         | 166 ms: 1.16x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 192 ms: 1.04x slower                                                    |
| async_tree_none                  | 142 ms                                                         | 149 ms: 1.04x slower                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 308 ms: 1.05x slower                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 128 ms: 1.05x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 238 ms: 1.06x slower                                                    |
| async_tree_none_tg               | 133 ms                                                         | 147 ms: 1.11x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 51.9 ms: 1.20x slower                                                   |
| coroutines                       | 10.8 ms                                                        | 13.1 ms: 1.22x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 281 ms: 1.35x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 160 ms: 1.56x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 119 ms: 4.13x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.07x slower                                                            |

Benchmark hidden because not significant (2): async_tree_cpu_io_mixed_tg, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260826-macm4pro-arm64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 165 ms: 1.01x faster                                                    |
| float          | 31.4 ms                                                        | 35.0 ms: 1.11x slower                                                   |
| nbody          | 42.5 ms                                                        | 62.0 ms: 1.46x slower                                                   |
| Geometric mean | (ref)                                                          | 1.17x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260826-macm4pro-arm64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.09 ms: 1.18x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.37 ms: 1.17x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 92.2 ms: 1.03x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 68.4 ms: 1.43x slower                                                   |
| Geometric mean | (ref)                                                          | 1.00x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260826-macm4pro-arm64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.76 ms: 1.24x faster                                                   |
| xml_etree_iterparse  | 46.1 ms                                                        | 43.0 ms: 1.07x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 944 ms: 1.06x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 62.1 ms: 1.00x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 39.4 ms: 1.10x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 119 us: 1.20x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 31.4 ms: 1.24x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 164 us: 1.26x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.04x slower                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260826-macm4pro-arm64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 10.2 ms: 1.18x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 7.51 ms: 1.26x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.22x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260826-macm4pro-arm64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 5.85 ms: 1.33x slower                                                   |
| django_template | 12.5 ms                                                        | 17.9 ms: 1.43x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.38x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260826-macm4pro-arm64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 773 us: 2.64x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 484 us: 2.05x faster                                                    |
| pylint                           | 106 ms                                                         | 54.4 ms: 1.94x faster                                                   |
| mdp                              | 1.06 sec                                                       | 624 ms: 1.69x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 311 ms: 1.67x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 315 ms: 1.67x faster                                                    |
| k_core                           | 1.46 sec                                                       | 1.00 sec: 1.46x faster                                                  |
| subparsers                       | 6.26 ms                                                        | 4.55 ms: 1.38x faster                                                   |
| async_tree_io_tg                 | 405 ms                                                         | 315 ms: 1.29x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.76 ms: 1.24x faster                                                   |
| deepcopy                         | 145 us                                                         | 118 us: 1.23x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 320 ms: 1.21x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 805 ns: 1.18x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.09 ms: 1.18x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.37 ms: 1.17x faster                                                   |
| async_generators                 | 193 ms                                                         | 166 ms: 1.16x faster                                                    |
| go                               | 72.6 ms                                                        | 66.8 ms: 1.09x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 15.2 us: 1.08x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.96 sec: 1.08x faster                                                  |
| xml_etree_iterparse              | 46.1 ms                                                        | 43.0 ms: 1.07x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 944 ms: 1.06x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 61.1 us: 1.06x faster                                                   |
| pyflate                          | 222 ms                                                         | 211 ms: 1.05x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 61.0 ms: 1.05x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.24 us: 1.04x faster                                                   |
| regex_dna                        | 94.6 ms                                                        | 92.2 ms: 1.03x faster                                                   |
| json                             | 1.94 ms                                                        | 1.90 ms: 1.02x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.01x faster                                                   |
| pidigits                         | 166 ms                                                         | 165 ms: 1.01x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 62.1 ms: 1.00x faster                                                   |
| telco                            | 3.07 ms                                                        | 3.09 ms: 1.01x slower                                                   |
| async_tree_memoization           | 184 ms                                                         | 192 ms: 1.04x slower                                                    |
| async_tree_none                  | 142 ms                                                         | 149 ms: 1.04x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 24.2 ms: 1.05x slower                                                   |
| docutils                         | 1.05 sec                                                       | 1.10 sec: 1.05x slower                                                  |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 308 ms: 1.05x slower                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 128 ms: 1.05x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 238 ms: 1.06x slower                                                    |
| fannkuch                         | 179 ms                                                         | 190 ms: 1.06x slower                                                    |
| pycparser                        | 470 ms                                                         | 511 ms: 1.09x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 136 ms: 1.10x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 39.4 ms: 1.10x slower                                                   |
| async_tree_none_tg               | 133 ms                                                         | 147 ms: 1.11x slower                                                    |
| float                            | 31.4 ms                                                        | 35.0 ms: 1.11x slower                                                   |
| sphinx                           | 409 ms                                                         | 459 ms: 1.12x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.49 ms: 1.13x slower                                                   |
| shortest_path                    | 225 ms                                                         | 254 ms: 1.13x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 54.4 ms: 1.14x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 367 ms: 1.14x slower                                                    |
| thrift                           | 309 us                                                         | 356 us: 1.15x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 753 ms: 1.16x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 44.1 ms: 1.17x slower                                                   |
| connected_components             | 208 ms                                                         | 245 ms: 1.18x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 10.2 ms: 1.18x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 44.0 ms: 1.18x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 35.4 ms: 1.18x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.67 us: 1.19x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 119 us: 1.20x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 114 ms: 1.20x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 62.7 ms: 1.20x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 51.9 ms: 1.20x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.94 us: 1.20x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 194 ms: 1.22x slower                                                    |
| richards                         | 22.1 ms                                                        | 26.9 ms: 1.22x slower                                                   |
| coroutines                       | 10.8 ms                                                        | 13.1 ms: 1.22x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.18 ms: 1.22x slower                                                   |
| 2to3                             | 112 ms                                                         | 137 ms: 1.23x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 53.7 ms: 1.23x slower                                                   |
| richards_super                   | 24.7 ms                                                        | 30.5 ms: 1.24x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 50.3 ns: 1.24x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 31.4 ms: 1.24x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 3.54 ms: 1.24x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 7.51 ms: 1.26x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 164 us: 1.26x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 42.9 ms: 1.28x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 8.77 us: 1.29x slower                                                   |
| chaos                            | 24.3 ms                                                        | 31.8 ms: 1.31x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.85 ms: 1.33x slower                                                   |
| coverage                         | 31.2 ms                                                        | 41.4 ms: 1.33x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 281 ms: 1.35x slower                                                    |
| many_optionals                   | 200 us                                                         | 275 us: 1.37x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 581 us: 1.41x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 68.4 ms: 1.43x slower                                                   |
| django_template                  | 12.5 ms                                                        | 17.9 ms: 1.43x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 2.09 ms: 1.44x slower                                                   |
| raytrace                         | 109 ms                                                         | 157 ms: 1.44x slower                                                    |
| nbody                            | 42.5 ms                                                        | 62.0 ms: 1.46x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 160 ms: 1.56x slower                                                    |
| generators                       | 15.7 ms                                                        | 24.8 ms: 1.58x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 70.4 ms: 1.65x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 119 ms: 4.13x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.07x slower                                                            |

Benchmark hidden because not significant (4): json_loads, dulwich_log, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260826-3.16.0a0-fe3a26f-NOGIL/bm-20260826-macm4pro-arm64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.060x slower

# HPT report

- Reliability score: 99.62% likely to be slow
- 90% likely to have a slowdown of 1.04x
- 95% likely to have a slowdown of 1.03x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.28x