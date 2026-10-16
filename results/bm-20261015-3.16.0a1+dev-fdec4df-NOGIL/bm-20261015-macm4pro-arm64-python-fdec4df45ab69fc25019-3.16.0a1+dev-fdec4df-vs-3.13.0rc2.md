# Results vs. 3.13.0rc2

- fork: python
- ref: fdec4df45ab69fc25019
- machine: darwin-arm64
- commit hash: fdec4df
- commit date: 2026-10-15
- overall geometric mean: 1.024x slower
- HPT reliability: 96.15%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.25x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261015-macm4pro-arm64-python-fdec4df45ab69fc25019-3.16.0a1+dev-fdec4df |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 130 ms: 1.16x slower                                                        |
| docutils       | 1.05 sec                                                       | 1.05 sec: 1.01x slower                                                      |
| sphinx         | 409 ms                                                         | 449 ms: 1.10x slower                                                        |
| Geometric mean | (ref)                                                          | 1.06x slower                                                                |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261015-macm4pro-arm64-python-fdec4df45ab69fc25019-3.16.0a1+dev-fdec4df |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 298 ms: 1.76x faster                                                        |
| async_tree_eager_io_tg           | 521 ms                                                         | 295 ms: 1.76x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 297 ms: 1.36x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 308 ms: 1.25x faster                                                        |
| async_generators                 | 193 ms                                                         | 160 ms: 1.21x faster                                                        |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 182 ms: 1.02x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 297 ms: 1.02x faster                                                        |
| async_tree_eager_memoization     | 122 ms                                                         | 126 ms: 1.03x slower                                                        |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 303 ms: 1.03x slower                                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 237 ms: 1.05x slower                                                        |
| async_tree_none_tg               | 133 ms                                                         | 141 ms: 1.06x slower                                                        |
| async_tree_eager                 | 43.2 ms                                                        | 50.2 ms: 1.16x slower                                                       |
| coroutines                       | 10.8 ms                                                        | 12.7 ms: 1.18x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 277 ms: 1.33x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 164 ms: 1.60x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 114 ms: 3.95x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.04x slower                                                                |

Benchmark hidden because not significant (2): async_tree_none, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261015-macm4pro-arm64-python-fdec4df45ab69fc25019-3.16.0a1+dev-fdec4df |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 33.0 ms: 1.05x slower                                                       |
| nbody          | 42.5 ms                                                        | 57.4 ms: 1.35x slower                                                       |
| Geometric mean | (ref)                                                          | 1.12x slower                                                                |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261015-macm4pro-arm64-python-fdec4df45ab69fc25019-3.16.0a1+dev-fdec4df |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.34 ms: 1.20x faster                                                       |
| regex_v8       | 10.7 ms                                                        | 9.23 ms: 1.16x faster                                                       |
| regex_dna      | 94.6 ms                                                        | 93.0 ms: 1.02x faster                                                       |
| regex_compile  | 47.9 ms                                                        | 64.3 ms: 1.34x slower                                                       |
| Geometric mean | (ref)                                                          | 1.01x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261015-macm4pro-arm64-python-fdec4df45ab69fc25019-3.16.0a1+dev-fdec4df |
|----------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.82 ms: 1.22x faster                                                       |
| xml_etree_iterparse  | 46.1 ms                                                        | 41.1 ms: 1.12x faster                                                       |
| tomli_loads          | 1000 ms                                                        | 892 ms: 1.12x faster                                                        |
| xml_etree_parse      | 62.4 ms                                                        | 59.9 ms: 1.04x faster                                                       |
| json_loads           | 10.8 us                                                        | 11.0 us: 1.02x slower                                                       |
| xml_etree_generate   | 35.8 ms                                                        | 39.0 ms: 1.09x slower                                                       |
| unpickle_pure_python | 99.5 us                                                        | 109 us: 1.09x slower                                                        |
| pickle_pure_python   | 130 us                                                         | 153 us: 1.18x slower                                                        |
| xml_etree_process    | 25.4 ms                                                        | 29.9 ms: 1.18x slower                                                       |
| Geometric mean       | (ref)                                                          | 1.01x slower                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261015-macm4pro-arm64-python-fdec4df45ab69fc25019-3.16.0a1+dev-fdec4df |
|------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 10.1 ms: 1.17x slower                                                       |
| python_startup_no_site | 5.95 ms                                                        | 7.39 ms: 1.24x slower                                                       |
| Geometric mean         | (ref)                                                          | 1.21x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261015-macm4pro-arm64-python-fdec4df45ab69fc25019-3.16.0a1+dev-fdec4df |
|-----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 5.79 ms: 1.31x slower                                                       |
| django_template | 12.5 ms                                                        | 17.1 ms: 1.37x slower                                                       |
| Geometric mean  | (ref)                                                          | 1.34x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261015-macm4pro-arm64-python-fdec4df45ab69fc25019-3.16.0a1+dev-fdec4df |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 785 us: 2.60x faster                                                        |
| create_gc_cycles                 | 993 us                                                         | 473 us: 2.10x faster                                                        |
| pylint                           | 106 ms                                                         | 53.6 ms: 1.97x faster                                                       |
| mdp                              | 1.06 sec                                                       | 597 ms: 1.77x faster                                                        |
| async_tree_eager_io              | 525 ms                                                         | 298 ms: 1.76x faster                                                        |
| async_tree_eager_io_tg           | 521 ms                                                         | 295 ms: 1.76x faster                                                        |
| k_core                           | 1.46 sec                                                       | 1.01 sec: 1.46x faster                                                      |
| subparsers                       | 6.26 ms                                                        | 4.31 ms: 1.45x faster                                                       |
| async_tree_io_tg                 | 405 ms                                                         | 297 ms: 1.36x faster                                                        |
| deepcopy                         | 145 us                                                         | 108 us: 1.34x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 308 ms: 1.25x faster                                                        |
| json_dumps                       | 4.65 ms                                                        | 3.82 ms: 1.22x faster                                                       |
| async_generators                 | 193 ms                                                         | 160 ms: 1.21x faster                                                        |
| regex_effbot                     | 1.61 ms                                                        | 1.34 ms: 1.20x faster                                                       |
| go                               | 72.6 ms                                                        | 60.6 ms: 1.20x faster                                                       |
| sqlite_synth                     | 948 ns                                                         | 804 ns: 1.18x faster                                                        |
| regex_v8                         | 10.7 ms                                                        | 9.23 ms: 1.16x faster                                                       |
| deepcopy_memo                    | 16.5 us                                                        | 14.6 us: 1.13x faster                                                       |
| pyflate                          | 222 ms                                                         | 198 ms: 1.12x faster                                                        |
| xml_etree_iterparse              | 46.1 ms                                                        | 41.1 ms: 1.12x faster                                                       |
| tomli_loads                      | 1000 ms                                                        | 892 ms: 1.12x faster                                                        |
| typing_runtime_protocols         | 64.6 us                                                        | 57.8 us: 1.12x faster                                                       |
| deepcopy_reduce                  | 1.30 us                                                        | 1.18 us: 1.10x faster                                                       |
| scimark_sor                      | 64.0 ms                                                        | 58.5 ms: 1.09x faster                                                       |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.96 sec: 1.09x faster                                                      |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                        |
| xml_etree_parse                  | 62.4 ms                                                        | 59.9 ms: 1.04x faster                                                       |
| async_tree_memoization_tg        | 186 ms                                                         | 182 ms: 1.02x faster                                                        |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                       |
| fannkuch                         | 179 ms                                                         | 175 ms: 1.02x faster                                                        |
| regex_dna                        | 94.6 ms                                                        | 93.0 ms: 1.02x faster                                                       |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 297 ms: 1.02x faster                                                        |
| dulwich_log                      | 19.8 ms                                                        | 19.6 ms: 1.01x faster                                                       |
| docutils                         | 1.05 sec                                                       | 1.05 sec: 1.01x slower                                                      |
| json_loads                       | 10.8 us                                                        | 11.0 us: 1.02x slower                                                       |
| pycparser                        | 470 ms                                                         | 483 ms: 1.03x slower                                                        |
| async_tree_eager_memoization     | 122 ms                                                         | 126 ms: 1.03x slower                                                        |
| telco                            | 3.07 ms                                                        | 3.16 ms: 1.03x slower                                                       |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 303 ms: 1.03x slower                                                        |
| scimark_fft                      | 124 ms                                                         | 128 ms: 1.03x slower                                                        |
| float                            | 31.4 ms                                                        | 33.0 ms: 1.05x slower                                                       |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 237 ms: 1.05x slower                                                        |
| async_tree_none_tg               | 133 ms                                                         | 141 ms: 1.06x slower                                                        |
| sympy_integrate                  | 7.53 ms                                                        | 8.19 ms: 1.09x slower                                                       |
| xml_etree_generate               | 35.8 ms                                                        | 39.0 ms: 1.09x slower                                                       |
| unpickle_pure_python             | 99.5 us                                                        | 109 us: 1.09x slower                                                        |
| richards                         | 22.1 ms                                                        | 24.2 ms: 1.10x slower                                                       |
| pprint_safe_repr                 | 322 ms                                                         | 353 ms: 1.10x slower                                                        |
| sphinx                           | 409 ms                                                         | 449 ms: 1.10x slower                                                        |
| logging_simple                   | 2.24 us                                                        | 2.47 us: 1.11x slower                                                       |
| shortest_path                    | 225 ms                                                         | 250 ms: 1.11x slower                                                        |
| logging_format                   | 2.45 us                                                        | 2.73 us: 1.12x slower                                                       |
| spectral_norm                    | 43.7 ms                                                        | 49.0 ms: 1.12x slower                                                       |
| thrift                           | 309 us                                                         | 347 us: 1.12x slower                                                        |
| richards_super                   | 24.7 ms                                                        | 27.8 ms: 1.12x slower                                                       |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.8 ms: 1.13x slower                                                       |
| meteor_contest                   | 47.9 ms                                                        | 54.3 ms: 1.13x slower                                                       |
| pprint_pformat                   | 650 ms                                                         | 741 ms: 1.14x slower                                                        |
| hexiom                           | 2.85 ms                                                        | 3.25 ms: 1.14x slower                                                       |
| bench_mp_pool                    | 37.8 ms                                                        | 43.5 ms: 1.15x slower                                                       |
| connected_components             | 208 ms                                                         | 240 ms: 1.15x slower                                                        |
| async_tree_eager                 | 43.2 ms                                                        | 50.2 ms: 1.16x slower                                                       |
| nqueens                          | 37.2 ms                                                        | 43.3 ms: 1.16x slower                                                       |
| 2to3                             | 112 ms                                                         | 130 ms: 1.16x slower                                                        |
| sympy_str                        | 95.5 ms                                                        | 112 ms: 1.17x slower                                                        |
| python_startup                   | 8.63 ms                                                        | 10.1 ms: 1.17x slower                                                       |
| sympy_sum                        | 52.3 ms                                                        | 61.6 ms: 1.18x slower                                                       |
| pickle_pure_python               | 130 us                                                         | 153 us: 1.18x slower                                                        |
| coroutines                       | 10.8 ms                                                        | 12.7 ms: 1.18x slower                                                       |
| xml_etree_process                | 25.4 ms                                                        | 29.9 ms: 1.18x slower                                                       |
| sympy_expand                     | 159 ms                                                         | 189 ms: 1.19x slower                                                        |
| chaos                            | 24.3 ms                                                        | 28.9 ms: 1.19x slower                                                       |
| logging_silent                   | 40.6 ns                                                        | 49.6 ns: 1.22x slower                                                       |
| crypto_pyaes                     | 33.6 ms                                                        | 41.5 ms: 1.23x slower                                                       |
| deltablue                        | 1.45 ms                                                        | 1.80 ms: 1.24x slower                                                       |
| python_startup_no_site           | 5.95 ms                                                        | 7.39 ms: 1.24x slower                                                       |
| comprehensions                   | 6.80 us                                                        | 8.47 us: 1.24x slower                                                       |
| raytrace                         | 109 ms                                                         | 136 ms: 1.25x slower                                                        |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.23 ms: 1.25x slower                                                       |
| many_optionals                   | 200 us                                                         | 258 us: 1.29x slower                                                        |
| coverage                         | 31.2 ms                                                        | 40.6 ms: 1.30x slower                                                       |
| mako                             | 4.41 ms                                                        | 5.79 ms: 1.31x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 277 ms: 1.33x slower                                                        |
| regex_compile                    | 47.9 ms                                                        | 64.3 ms: 1.34x slower                                                       |
| nbody                            | 42.5 ms                                                        | 57.4 ms: 1.35x slower                                                       |
| django_template                  | 12.5 ms                                                        | 17.1 ms: 1.37x slower                                                       |
| bench_thread_pool                | 412 us                                                         | 578 us: 1.40x slower                                                        |
| scimark_lu                       | 42.8 ms                                                        | 62.6 ms: 1.46x slower                                                       |
| generators                       | 15.7 ms                                                        | 23.8 ms: 1.52x slower                                                       |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 164 ms: 1.60x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 114 ms: 3.95x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.03x slower                                                                |

Benchmark hidden because not significant (5): html5lib, pidigits, json, async_tree_none, async_tree_memoization
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261015-3.16.0a1+dev-fdec4df-NOGIL/bm-20261015-macm4pro-arm64-python-fdec4df45ab69fc25019-3.16.0a1+dev-fdec4df.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.024x slower

# HPT report

- Reliability score: 96.15% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.25x