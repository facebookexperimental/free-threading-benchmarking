# Results vs. 3.13.0rc2

- fork: python
- ref: b09a7e92fb0ab958a52a
- machine: darwin-arm64
- commit hash: b09a7e9
- commit date: 2026-11-19
- overall geometric mean: 1.016x slower
- HPT reliability: 94.86%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261119-macm4pro-arm64-python-b09a7e92fb0ab958a52a-3.16.0a2+dev-b09a7e9 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 128 ms: 1.14x slower                                                        |
| docutils       | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                      |
| html5lib       | 23.1 ms                                                        | 23.0 ms: 1.01x faster                                                       |
| sphinx         | 409 ms                                                         | 452 ms: 1.11x slower                                                        |
| Geometric mean | (ref)                                                          | 1.06x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261119-macm4pro-arm64-python-b09a7e92fb0ab958a52a-3.16.0a2+dev-b09a7e9 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 298 ms: 1.75x faster                                                        |
| async_tree_eager_io              | 525 ms                                                         | 302 ms: 1.74x faster                                                        |
| async_generators                 | 193 ms                                                         | 111 ms: 1.74x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 302 ms: 1.34x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 308 ms: 1.25x faster                                                        |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.04x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 294 ms: 1.02x faster                                                        |
| async_tree_eager_memoization     | 122 ms                                                         | 126 ms: 1.03x slower                                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 233 ms: 1.04x slower                                                        |
| async_tree_none_tg               | 133 ms                                                         | 142 ms: 1.07x slower                                                        |
| coroutines                       | 10.8 ms                                                        | 11.8 ms: 1.10x slower                                                       |
| async_tree_eager                 | 43.2 ms                                                        | 50.0 ms: 1.16x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 272 ms: 1.31x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 164 ms: 1.60x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 115 ms: 3.98x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.01x slower                                                                |

Benchmark hidden because not significant (4): async_tree_memoization_tg, async_tree_memoization, async_tree_none, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261119-macm4pro-arm64-python-b09a7e92fb0ab958a52a-3.16.0a2+dev-b09a7e9 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 151 ms: 1.10x faster                                                        |
| float          | 31.4 ms                                                        | 33.1 ms: 1.05x slower                                                       |
| nbody          | 42.5 ms                                                        | 60.8 ms: 1.43x slower                                                       |
| Geometric mean | (ref)                                                          | 1.11x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261119-macm4pro-arm64-python-b09a7e92fb0ab958a52a-3.16.0a2+dev-b09a7e9 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.35 ms: 1.19x faster                                                       |
| regex_v8       | 10.7 ms                                                        | 9.22 ms: 1.16x faster                                                       |
| regex_dna      | 94.6 ms                                                        | 92.0 ms: 1.03x faster                                                       |
| regex_compile  | 47.9 ms                                                        | 64.0 ms: 1.34x slower                                                       |
| Geometric mean | (ref)                                                          | 1.02x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261119-macm4pro-arm64-python-b09a7e92fb0ab958a52a-3.16.0a2+dev-b09a7e9 |
|----------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.79 ms: 1.23x faster                                                       |
| tomli_loads          | 1000 ms                                                        | 861 ms: 1.16x faster                                                        |
| xml_etree_iterparse  | 46.1 ms                                                        | 41.8 ms: 1.10x faster                                                       |
| xml_etree_parse      | 62.4 ms                                                        | 60.9 ms: 1.02x faster                                                       |
| json_loads           | 10.8 us                                                        | 11.4 us: 1.06x slower                                                       |
| xml_etree_generate   | 35.8 ms                                                        | 37.9 ms: 1.06x slower                                                       |
| unpickle_pure_python | 99.5 us                                                        | 109 us: 1.10x slower                                                        |
| xml_etree_process    | 25.4 ms                                                        | 29.3 ms: 1.15x slower                                                       |
| pickle_pure_python   | 130 us                                                         | 158 us: 1.21x slower                                                        |
| Geometric mean       | (ref)                                                          | 1.01x slower                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261119-macm4pro-arm64-python-b09a7e92fb0ab958a52a-3.16.0a2+dev-b09a7e9 |
|------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.02 ms: 1.04x slower                                                       |
| python_startup_no_site | 5.95 ms                                                        | 7.03 ms: 1.18x slower                                                       |
| Geometric mean         | (ref)                                                          | 1.11x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261119-macm4pro-arm64-python-b09a7e92fb0ab958a52a-3.16.0a2+dev-b09a7e9 |
|-----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 5.58 ms: 1.26x slower                                                       |
| django_template | 12.5 ms                                                        | 16.8 ms: 1.35x slower                                                       |
| Geometric mean  | (ref)                                                          | 1.31x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261119-macm4pro-arm64-python-b09a7e92fb0ab958a52a-3.16.0a2+dev-b09a7e9 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 808 us: 2.53x faster                                                        |
| create_gc_cycles                 | 993 us                                                         | 478 us: 2.08x faster                                                        |
| pylint                           | 106 ms                                                         | 52.8 ms: 2.00x faster                                                       |
| mdp                              | 1.06 sec                                                       | 578 ms: 1.83x faster                                                        |
| async_tree_eager_io_tg           | 521 ms                                                         | 298 ms: 1.75x faster                                                        |
| async_tree_eager_io              | 525 ms                                                         | 302 ms: 1.74x faster                                                        |
| async_generators                 | 193 ms                                                         | 111 ms: 1.74x faster                                                        |
| subparsers                       | 6.26 ms                                                        | 4.33 ms: 1.45x faster                                                       |
| k_core                           | 1.46 sec                                                       | 1.01 sec: 1.45x faster                                                      |
| async_tree_io_tg                 | 405 ms                                                         | 302 ms: 1.34x faster                                                        |
| deepcopy                         | 145 us                                                         | 110 us: 1.32x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 308 ms: 1.25x faster                                                        |
| json_dumps                       | 4.65 ms                                                        | 3.79 ms: 1.23x faster                                                       |
| go                               | 72.6 ms                                                        | 60.0 ms: 1.21x faster                                                       |
| typing_runtime_protocols         | 64.6 us                                                        | 54.2 us: 1.19x faster                                                       |
| regex_effbot                     | 1.61 ms                                                        | 1.35 ms: 1.19x faster                                                       |
| tomli_loads                      | 1000 ms                                                        | 861 ms: 1.16x faster                                                        |
| regex_v8                         | 10.7 ms                                                        | 9.22 ms: 1.16x faster                                                       |
| sqlite_synth                     | 948 ns                                                         | 820 ns: 1.16x faster                                                        |
| deepcopy_memo                    | 16.5 us                                                        | 14.3 us: 1.15x faster                                                       |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.88 sec: 1.13x faster                                                      |
| pyflate                          | 222 ms                                                         | 199 ms: 1.11x faster                                                        |
| xml_etree_iterparse              | 46.1 ms                                                        | 41.8 ms: 1.10x faster                                                       |
| pidigits                         | 166 ms                                                         | 151 ms: 1.10x faster                                                        |
| scimark_sor                      | 64.0 ms                                                        | 58.6 ms: 1.09x faster                                                       |
| deepcopy_reduce                  | 1.30 us                                                        | 1.19 us: 1.09x faster                                                       |
| asyncio_websockets               | 194 ms                                                         | 187 ms: 1.04x faster                                                        |
| regex_dna                        | 94.6 ms                                                        | 92.0 ms: 1.03x faster                                                       |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                       |
| xml_etree_parse                  | 62.4 ms                                                        | 60.9 ms: 1.02x faster                                                       |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 294 ms: 1.02x faster                                                        |
| docutils                         | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                      |
| html5lib                         | 23.1 ms                                                        | 23.0 ms: 1.01x faster                                                       |
| telco                            | 3.07 ms                                                        | 3.08 ms: 1.00x slower                                                       |
| json                             | 1.94 ms                                                        | 1.97 ms: 1.01x slower                                                       |
| fannkuch                         | 179 ms                                                         | 182 ms: 1.02x slower                                                        |
| async_tree_eager_memoization     | 122 ms                                                         | 126 ms: 1.03x slower                                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 233 ms: 1.04x slower                                                        |
| python_startup                   | 8.63 ms                                                        | 9.02 ms: 1.04x slower                                                       |
| pycparser                        | 470 ms                                                         | 493 ms: 1.05x slower                                                        |
| float                            | 31.4 ms                                                        | 33.1 ms: 1.05x slower                                                       |
| json_loads                       | 10.8 us                                                        | 11.4 us: 1.06x slower                                                       |
| xml_etree_generate               | 35.8 ms                                                        | 37.9 ms: 1.06x slower                                                       |
| scimark_fft                      | 124 ms                                                         | 132 ms: 1.07x slower                                                        |
| async_tree_none_tg               | 133 ms                                                         | 142 ms: 1.07x slower                                                        |
| sympy_integrate                  | 7.53 ms                                                        | 8.13 ms: 1.08x slower                                                       |
| pprint_safe_repr                 | 322 ms                                                         | 350 ms: 1.09x slower                                                        |
| richards                         | 22.1 ms                                                        | 24.1 ms: 1.09x slower                                                       |
| hexiom                           | 2.85 ms                                                        | 3.12 ms: 1.09x slower                                                       |
| unpickle_pure_python             | 99.5 us                                                        | 109 us: 1.10x slower                                                        |
| coroutines                       | 10.8 ms                                                        | 11.8 ms: 1.10x slower                                                       |
| sphinx                           | 409 ms                                                         | 452 ms: 1.11x slower                                                        |
| logging_simple                   | 2.24 us                                                        | 2.47 us: 1.11x slower                                                       |
| bench_mp_pool                    | 37.8 ms                                                        | 41.9 ms: 1.11x slower                                                       |
| shortest_path                    | 225 ms                                                         | 250 ms: 1.11x slower                                                        |
| thrift                           | 309 us                                                         | 345 us: 1.12x slower                                                        |
| richards_super                   | 24.7 ms                                                        | 27.7 ms: 1.12x slower                                                       |
| logging_format                   | 2.45 us                                                        | 2.75 us: 1.13x slower                                                       |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.8 ms: 1.13x slower                                                       |
| pprint_pformat                   | 650 ms                                                         | 736 ms: 1.13x slower                                                        |
| meteor_contest                   | 47.9 ms                                                        | 54.5 ms: 1.14x slower                                                       |
| bench_thread_pool                | 412 us                                                         | 469 us: 1.14x slower                                                        |
| spectral_norm                    | 43.7 ms                                                        | 49.9 ms: 1.14x slower                                                       |
| 2to3                             | 112 ms                                                         | 128 ms: 1.14x slower                                                        |
| xml_etree_process                | 25.4 ms                                                        | 29.3 ms: 1.15x slower                                                       |
| async_tree_eager                 | 43.2 ms                                                        | 50.0 ms: 1.16x slower                                                       |
| sympy_str                        | 95.5 ms                                                        | 111 ms: 1.16x slower                                                        |
| nqueens                          | 37.2 ms                                                        | 43.4 ms: 1.17x slower                                                       |
| connected_components             | 208 ms                                                         | 244 ms: 1.17x slower                                                        |
| sympy_sum                        | 52.3 ms                                                        | 61.4 ms: 1.17x slower                                                       |
| python_startup_no_site           | 5.95 ms                                                        | 7.03 ms: 1.18x slower                                                       |
| chaos                            | 24.3 ms                                                        | 28.8 ms: 1.19x slower                                                       |
| sympy_expand                     | 159 ms                                                         | 190 ms: 1.19x slower                                                        |
| logging_silent                   | 40.6 ns                                                        | 49.0 ns: 1.21x slower                                                       |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.15 ms: 1.21x slower                                                       |
| comprehensions                   | 6.80 us                                                        | 8.26 us: 1.21x slower                                                       |
| pickle_pure_python               | 130 us                                                         | 158 us: 1.21x slower                                                        |
| crypto_pyaes                     | 33.6 ms                                                        | 41.4 ms: 1.23x slower                                                       |
| deltablue                        | 1.45 ms                                                        | 1.79 ms: 1.24x slower                                                       |
| raytrace                         | 109 ms                                                         | 137 ms: 1.26x slower                                                        |
| mako                             | 4.41 ms                                                        | 5.58 ms: 1.26x slower                                                       |
| many_optionals                   | 200 us                                                         | 255 us: 1.27x slower                                                        |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 272 ms: 1.31x slower                                                        |
| coverage                         | 31.2 ms                                                        | 41.3 ms: 1.33x slower                                                       |
| regex_compile                    | 47.9 ms                                                        | 64.0 ms: 1.34x slower                                                       |
| django_template                  | 12.5 ms                                                        | 16.8 ms: 1.35x slower                                                       |
| nbody                            | 42.5 ms                                                        | 60.8 ms: 1.43x slower                                                       |
| generators                       | 15.7 ms                                                        | 23.7 ms: 1.51x slower                                                       |
| scimark_lu                       | 42.8 ms                                                        | 66.7 ms: 1.56x slower                                                       |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 164 ms: 1.60x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 115 ms: 3.98x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.02x slower                                                                |

Benchmark hidden because not significant (5): async_tree_memoization_tg, async_tree_memoization, dulwich_log, async_tree_none, async_tree_cpu_io_mixed
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261119-3.16.0a2+dev-b09a7e9-NOGIL/bm-20261119-macm4pro-arm64-python-b09a7e92fb0ab958a52a-3.16.0a2+dev-b09a7e9.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.016x slower

# HPT report

- Reliability score: 94.86% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.19x