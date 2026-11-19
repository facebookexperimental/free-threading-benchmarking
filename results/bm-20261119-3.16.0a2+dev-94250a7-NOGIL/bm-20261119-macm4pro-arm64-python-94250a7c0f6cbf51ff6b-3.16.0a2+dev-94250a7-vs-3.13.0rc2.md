# Results vs. 3.13.0rc2

- fork: python
- ref: 94250a7c0f6cbf51ff6b
- machine: darwin-arm64
- commit hash: 94250a7
- commit date: 2026-11-19
- overall geometric mean: 1.013x slower
- HPT reliability: 92.63%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261119-macm4pro-arm64-python-94250a7c0f6cbf51ff6b-3.16.0a2+dev-94250a7 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 127 ms: 1.14x slower                                                        |
| docutils       | 1.05 sec                                                       | 1.03 sec: 1.01x faster                                                      |
| sphinx         | 409 ms                                                         | 448 ms: 1.10x slower                                                        |
| Geometric mean | (ref)                                                          | 1.05x slower                                                                |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261119-macm4pro-arm64-python-94250a7c0f6cbf51ff6b-3.16.0a2+dev-94250a7 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 298 ms: 1.75x faster                                                        |
| async_tree_eager_io              | 525 ms                                                         | 302 ms: 1.74x faster                                                        |
| async_generators                 | 193 ms                                                         | 113 ms: 1.70x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 303 ms: 1.34x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 309 ms: 1.25x faster                                                        |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.04x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 293 ms: 1.03x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 182 ms: 1.02x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 232 ms: 1.03x slower                                                        |
| async_tree_eager_memoization     | 122 ms                                                         | 126 ms: 1.03x slower                                                        |
| async_tree_none_tg               | 133 ms                                                         | 142 ms: 1.07x slower                                                        |
| coroutines                       | 10.8 ms                                                        | 11.9 ms: 1.11x slower                                                       |
| async_tree_eager                 | 43.2 ms                                                        | 50.2 ms: 1.16x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 271 ms: 1.30x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 164 ms: 1.60x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 114 ms: 3.96x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.01x slower                                                                |

Benchmark hidden because not significant (3): async_tree_memoization, async_tree_none, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261119-macm4pro-arm64-python-94250a7c0f6cbf51ff6b-3.16.0a2+dev-94250a7 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 147 ms: 1.13x faster                                                        |
| float          | 31.4 ms                                                        | 33.1 ms: 1.05x slower                                                       |
| nbody          | 42.5 ms                                                        | 60.6 ms: 1.43x slower                                                       |
| Geometric mean | (ref)                                                          | 1.10x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261119-macm4pro-arm64-python-94250a7c0f6cbf51ff6b-3.16.0a2+dev-94250a7 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.33 ms: 1.21x faster                                                       |
| regex_v8       | 10.7 ms                                                        | 9.15 ms: 1.17x faster                                                       |
| regex_dna      | 94.6 ms                                                        | 92.2 ms: 1.03x faster                                                       |
| regex_compile  | 47.9 ms                                                        | 63.7 ms: 1.33x slower                                                       |
| Geometric mean | (ref)                                                          | 1.02x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261119-macm4pro-arm64-python-94250a7c0f6cbf51ff6b-3.16.0a2+dev-94250a7 |
|----------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.80 ms: 1.22x faster                                                       |
| tomli_loads          | 1000 ms                                                        | 880 ms: 1.14x faster                                                        |
| xml_etree_iterparse  | 46.1 ms                                                        | 41.3 ms: 1.12x faster                                                       |
| xml_etree_parse      | 62.4 ms                                                        | 58.9 ms: 1.06x faster                                                       |
| json_loads           | 10.8 us                                                        | 11.2 us: 1.04x slower                                                       |
| xml_etree_generate   | 35.8 ms                                                        | 38.2 ms: 1.07x slower                                                       |
| unpickle_pure_python | 99.5 us                                                        | 109 us: 1.10x slower                                                        |
| xml_etree_process    | 25.4 ms                                                        | 29.6 ms: 1.17x slower                                                       |
| pickle_pure_python   | 130 us                                                         | 159 us: 1.22x slower                                                        |
| Geometric mean       | (ref)                                                          | 1.01x slower                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261119-macm4pro-arm64-python-94250a7c0f6cbf51ff6b-3.16.0a2+dev-94250a7 |
|------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.70 ms: 1.01x slower                                                       |
| python_startup_no_site | 5.95 ms                                                        | 6.80 ms: 1.14x slower                                                       |
| Geometric mean         | (ref)                                                          | 1.07x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261119-macm4pro-arm64-python-94250a7c0f6cbf51ff6b-3.16.0a2+dev-94250a7 |
|-----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 5.63 ms: 1.28x slower                                                       |
| django_template | 12.5 ms                                                        | 16.7 ms: 1.34x slower                                                       |
| Geometric mean  | (ref)                                                          | 1.31x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261119-macm4pro-arm64-python-94250a7c0f6cbf51ff6b-3.16.0a2+dev-94250a7 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 797 us: 2.56x faster                                                        |
| create_gc_cycles                 | 993 us                                                         | 476 us: 2.09x faster                                                        |
| pylint                           | 106 ms                                                         | 52.6 ms: 2.01x faster                                                       |
| mdp                              | 1.06 sec                                                       | 585 ms: 1.81x faster                                                        |
| async_tree_eager_io_tg           | 521 ms                                                         | 298 ms: 1.75x faster                                                        |
| async_tree_eager_io              | 525 ms                                                         | 302 ms: 1.74x faster                                                        |
| async_generators                 | 193 ms                                                         | 113 ms: 1.70x faster                                                        |
| k_core                           | 1.46 sec                                                       | 993 ms: 1.47x faster                                                        |
| subparsers                       | 6.26 ms                                                        | 4.30 ms: 1.46x faster                                                       |
| async_tree_io_tg                 | 405 ms                                                         | 303 ms: 1.34x faster                                                        |
| deepcopy                         | 145 us                                                         | 111 us: 1.30x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 309 ms: 1.25x faster                                                        |
| json_dumps                       | 4.65 ms                                                        | 3.80 ms: 1.22x faster                                                       |
| regex_effbot                     | 1.61 ms                                                        | 1.33 ms: 1.21x faster                                                       |
| go                               | 72.6 ms                                                        | 60.1 ms: 1.21x faster                                                       |
| typing_runtime_protocols         | 64.6 us                                                        | 53.6 us: 1.21x faster                                                       |
| regex_v8                         | 10.7 ms                                                        | 9.15 ms: 1.17x faster                                                       |
| sqlite_synth                     | 948 ns                                                         | 825 ns: 1.15x faster                                                        |
| tomli_loads                      | 1000 ms                                                        | 880 ms: 1.14x faster                                                        |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.88 sec: 1.13x faster                                                      |
| pidigits                         | 166 ms                                                         | 147 ms: 1.13x faster                                                        |
| deepcopy_memo                    | 16.5 us                                                        | 14.6 us: 1.13x faster                                                       |
| pyflate                          | 222 ms                                                         | 198 ms: 1.12x faster                                                        |
| xml_etree_iterparse              | 46.1 ms                                                        | 41.3 ms: 1.12x faster                                                       |
| scimark_sor                      | 64.0 ms                                                        | 58.3 ms: 1.10x faster                                                       |
| deepcopy_reduce                  | 1.30 us                                                        | 1.21 us: 1.07x faster                                                       |
| xml_etree_parse                  | 62.4 ms                                                        | 58.9 ms: 1.06x faster                                                       |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.04x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 293 ms: 1.03x faster                                                        |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                       |
| regex_dna                        | 94.6 ms                                                        | 92.2 ms: 1.03x faster                                                       |
| async_tree_memoization_tg        | 186 ms                                                         | 182 ms: 1.02x faster                                                        |
| docutils                         | 1.05 sec                                                       | 1.03 sec: 1.01x faster                                                      |
| dulwich_log                      | 19.8 ms                                                        | 19.7 ms: 1.01x faster                                                       |
| fannkuch                         | 179 ms                                                         | 180 ms: 1.01x slower                                                        |
| python_startup                   | 8.63 ms                                                        | 8.70 ms: 1.01x slower                                                       |
| telco                            | 3.07 ms                                                        | 3.11 ms: 1.01x slower                                                       |
| json                             | 1.94 ms                                                        | 1.97 ms: 1.02x slower                                                       |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 232 ms: 1.03x slower                                                        |
| async_tree_eager_memoization     | 122 ms                                                         | 126 ms: 1.03x slower                                                        |
| json_loads                       | 10.8 us                                                        | 11.2 us: 1.04x slower                                                       |
| pycparser                        | 470 ms                                                         | 491 ms: 1.04x slower                                                        |
| float                            | 31.4 ms                                                        | 33.1 ms: 1.05x slower                                                       |
| xml_etree_generate               | 35.8 ms                                                        | 38.2 ms: 1.07x slower                                                       |
| async_tree_none_tg               | 133 ms                                                         | 142 ms: 1.07x slower                                                        |
| scimark_fft                      | 124 ms                                                         | 132 ms: 1.07x slower                                                        |
| sympy_integrate                  | 7.53 ms                                                        | 8.10 ms: 1.08x slower                                                       |
| pprint_safe_repr                 | 322 ms                                                         | 350 ms: 1.09x slower                                                        |
| richards                         | 22.1 ms                                                        | 24.1 ms: 1.09x slower                                                       |
| logging_simple                   | 2.24 us                                                        | 2.45 us: 1.10x slower                                                       |
| sphinx                           | 409 ms                                                         | 448 ms: 1.10x slower                                                        |
| unpickle_pure_python             | 99.5 us                                                        | 109 us: 1.10x slower                                                        |
| bench_mp_pool                    | 37.8 ms                                                        | 41.6 ms: 1.10x slower                                                       |
| shortest_path                    | 225 ms                                                         | 249 ms: 1.11x slower                                                        |
| hexiom                           | 2.85 ms                                                        | 3.16 ms: 1.11x slower                                                       |
| logging_format                   | 2.45 us                                                        | 2.71 us: 1.11x slower                                                       |
| coroutines                       | 10.8 ms                                                        | 11.9 ms: 1.11x slower                                                       |
| meteor_contest                   | 47.9 ms                                                        | 53.4 ms: 1.11x slower                                                       |
| richards_super                   | 24.7 ms                                                        | 27.6 ms: 1.12x slower                                                       |
| thrift                           | 309 us                                                         | 347 us: 1.12x slower                                                        |
| pprint_pformat                   | 650 ms                                                         | 734 ms: 1.13x slower                                                        |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.8 ms: 1.13x slower                                                       |
| bench_thread_pool                | 412 us                                                         | 469 us: 1.14x slower                                                        |
| 2to3                             | 112 ms                                                         | 127 ms: 1.14x slower                                                        |
| spectral_norm                    | 43.7 ms                                                        | 49.9 ms: 1.14x slower                                                       |
| python_startup_no_site           | 5.95 ms                                                        | 6.80 ms: 1.14x slower                                                       |
| connected_components             | 208 ms                                                         | 238 ms: 1.15x slower                                                        |
| sympy_str                        | 95.5 ms                                                        | 111 ms: 1.16x slower                                                        |
| nqueens                          | 37.2 ms                                                        | 43.3 ms: 1.16x slower                                                       |
| async_tree_eager                 | 43.2 ms                                                        | 50.2 ms: 1.16x slower                                                       |
| sympy_sum                        | 52.3 ms                                                        | 60.8 ms: 1.16x slower                                                       |
| xml_etree_process                | 25.4 ms                                                        | 29.6 ms: 1.17x slower                                                       |
| chaos                            | 24.3 ms                                                        | 28.6 ms: 1.18x slower                                                       |
| sympy_expand                     | 159 ms                                                         | 190 ms: 1.19x slower                                                        |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.16 ms: 1.21x slower                                                       |
| comprehensions                   | 6.80 us                                                        | 8.30 us: 1.22x slower                                                       |
| pickle_pure_python               | 130 us                                                         | 159 us: 1.22x slower                                                        |
| deltablue                        | 1.45 ms                                                        | 1.79 ms: 1.23x slower                                                       |
| crypto_pyaes                     | 33.6 ms                                                        | 41.6 ms: 1.24x slower                                                       |
| raytrace                         | 109 ms                                                         | 137 ms: 1.26x slower                                                        |
| logging_silent                   | 40.6 ns                                                        | 51.1 ns: 1.26x slower                                                       |
| many_optionals                   | 200 us                                                         | 254 us: 1.27x slower                                                        |
| mako                             | 4.41 ms                                                        | 5.63 ms: 1.28x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 271 ms: 1.30x slower                                                        |
| regex_compile                    | 47.9 ms                                                        | 63.7 ms: 1.33x slower                                                       |
| coverage                         | 31.2 ms                                                        | 41.5 ms: 1.33x slower                                                       |
| django_template                  | 12.5 ms                                                        | 16.7 ms: 1.34x slower                                                       |
| nbody                            | 42.5 ms                                                        | 60.6 ms: 1.43x slower                                                       |
| generators                       | 15.7 ms                                                        | 23.7 ms: 1.51x slower                                                       |
| scimark_lu                       | 42.8 ms                                                        | 67.0 ms: 1.57x slower                                                       |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 164 ms: 1.60x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 114 ms: 3.96x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.02x slower                                                                |

Benchmark hidden because not significant (4): async_tree_memoization, async_tree_none, html5lib, async_tree_cpu_io_mixed
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261119-3.16.0a2+dev-94250a7-NOGIL/bm-20261119-macm4pro-arm64-python-94250a7c0f6cbf51ff6b-3.16.0a2+dev-94250a7.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.013x slower

# HPT report

- Reliability score: 92.63% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.19x