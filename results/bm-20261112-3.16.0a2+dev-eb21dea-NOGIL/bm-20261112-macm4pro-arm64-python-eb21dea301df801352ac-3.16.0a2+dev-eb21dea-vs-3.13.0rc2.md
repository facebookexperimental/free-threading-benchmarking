# Results vs. 3.13.0rc2

- fork: python
- ref: eb21dea301df801352ac
- machine: darwin-arm64
- commit hash: eb21dea
- commit date: 2026-11-12
- overall geometric mean: 1.016x slower
- HPT reliability: 94.35%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261112-macm4pro-arm64-python-eb21dea301df801352ac-3.16.0a2+dev-eb21dea |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 126 ms: 1.13x slower                                                        |
| docutils       | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                      |
| html5lib       | 23.1 ms                                                        | 22.9 ms: 1.01x faster                                                       |
| sphinx         | 409 ms                                                         | 451 ms: 1.10x slower                                                        |
| Geometric mean | (ref)                                                          | 1.05x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261112-macm4pro-arm64-python-eb21dea301df801352ac-3.16.0a2+dev-eb21dea |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 297 ms: 1.75x faster                                                        |
| async_tree_eager_io              | 525 ms                                                         | 302 ms: 1.74x faster                                                        |
| async_generators                 | 193 ms                                                         | 112 ms: 1.73x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 300 ms: 1.35x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 301 ms: 1.28x faster                                                        |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 291 ms: 1.03x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 231 ms: 1.03x slower                                                        |
| async_tree_eager_memoization     | 122 ms                                                         | 125 ms: 1.03x slower                                                        |
| async_tree_none_tg               | 133 ms                                                         | 142 ms: 1.07x slower                                                        |
| coroutines                       | 10.8 ms                                                        | 11.9 ms: 1.11x slower                                                       |
| async_tree_eager                 | 43.2 ms                                                        | 50.2 ms: 1.16x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 270 ms: 1.30x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 156 ms: 1.52x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 114 ms: 3.94x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.01x slower                                                                |

Benchmark hidden because not significant (4): async_tree_memoization_tg, async_tree_none, async_tree_memoization, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261112-macm4pro-arm64-python-eb21dea301df801352ac-3.16.0a2+dev-eb21dea |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 150 ms: 1.11x faster                                                        |
| float          | 31.4 ms                                                        | 33.3 ms: 1.06x slower                                                       |
| nbody          | 42.5 ms                                                        | 59.3 ms: 1.39x slower                                                       |
| Geometric mean | (ref)                                                          | 1.10x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261112-macm4pro-arm64-python-eb21dea301df801352ac-3.16.0a2+dev-eb21dea |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.36 ms: 1.19x faster                                                       |
| regex_v8       | 10.7 ms                                                        | 9.17 ms: 1.17x faster                                                       |
| regex_dna      | 94.6 ms                                                        | 92.8 ms: 1.02x faster                                                       |
| regex_compile  | 47.9 ms                                                        | 64.1 ms: 1.34x slower                                                       |
| Geometric mean | (ref)                                                          | 1.01x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261112-macm4pro-arm64-python-eb21dea301df801352ac-3.16.0a2+dev-eb21dea |
|----------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.79 ms: 1.23x faster                                                       |
| tomli_loads          | 1000 ms                                                        | 877 ms: 1.14x faster                                                        |
| xml_etree_iterparse  | 46.1 ms                                                        | 41.7 ms: 1.11x faster                                                       |
| xml_etree_parse      | 62.4 ms                                                        | 60.0 ms: 1.04x faster                                                       |
| json_loads           | 10.8 us                                                        | 11.3 us: 1.05x slower                                                       |
| xml_etree_generate   | 35.8 ms                                                        | 38.1 ms: 1.06x slower                                                       |
| unpickle_pure_python | 99.5 us                                                        | 109 us: 1.10x slower                                                        |
| xml_etree_process    | 25.4 ms                                                        | 29.3 ms: 1.16x slower                                                       |
| pickle_pure_python   | 130 us                                                         | 159 us: 1.22x slower                                                        |
| Geometric mean       | (ref)                                                          | 1.01x slower                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261112-macm4pro-arm64-python-eb21dea301df801352ac-3.16.0a2+dev-eb21dea |
|------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.95 ms: 1.04x slower                                                       |
| python_startup_no_site | 5.95 ms                                                        | 6.92 ms: 1.16x slower                                                       |
| Geometric mean         | (ref)                                                          | 1.10x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261112-macm4pro-arm64-python-eb21dea301df801352ac-3.16.0a2+dev-eb21dea |
|-----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 5.58 ms: 1.26x slower                                                       |
| django_template | 12.5 ms                                                        | 16.8 ms: 1.34x slower                                                       |
| Geometric mean  | (ref)                                                          | 1.30x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261112-macm4pro-arm64-python-eb21dea301df801352ac-3.16.0a2+dev-eb21dea |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 787 us: 2.59x faster                                                        |
| create_gc_cycles                 | 993 us                                                         | 473 us: 2.10x faster                                                        |
| pylint                           | 106 ms                                                         | 52.4 ms: 2.02x faster                                                       |
| mdp                              | 1.06 sec                                                       | 584 ms: 1.81x faster                                                        |
| async_tree_eager_io_tg           | 521 ms                                                         | 297 ms: 1.75x faster                                                        |
| async_tree_eager_io              | 525 ms                                                         | 302 ms: 1.74x faster                                                        |
| async_generators                 | 193 ms                                                         | 112 ms: 1.73x faster                                                        |
| subparsers                       | 6.26 ms                                                        | 4.30 ms: 1.46x faster                                                       |
| k_core                           | 1.46 sec                                                       | 1.01 sec: 1.45x faster                                                      |
| async_tree_io_tg                 | 405 ms                                                         | 300 ms: 1.35x faster                                                        |
| deepcopy                         | 145 us                                                         | 110 us: 1.32x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 301 ms: 1.28x faster                                                        |
| json_dumps                       | 4.65 ms                                                        | 3.79 ms: 1.23x faster                                                       |
| typing_runtime_protocols         | 64.6 us                                                        | 53.5 us: 1.21x faster                                                       |
| go                               | 72.6 ms                                                        | 60.2 ms: 1.21x faster                                                       |
| regex_effbot                     | 1.61 ms                                                        | 1.36 ms: 1.19x faster                                                       |
| regex_v8                         | 10.7 ms                                                        | 9.17 ms: 1.17x faster                                                       |
| sqlite_synth                     | 948 ns                                                         | 828 ns: 1.14x faster                                                        |
| tomli_loads                      | 1000 ms                                                        | 877 ms: 1.14x faster                                                        |
| pyflate                          | 222 ms                                                         | 198 ms: 1.12x faster                                                        |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.90 sec: 1.12x faster                                                      |
| deepcopy_memo                    | 16.5 us                                                        | 14.7 us: 1.12x faster                                                       |
| pidigits                         | 166 ms                                                         | 150 ms: 1.11x faster                                                        |
| xml_etree_iterparse              | 46.1 ms                                                        | 41.7 ms: 1.11x faster                                                       |
| scimark_sor                      | 64.0 ms                                                        | 58.1 ms: 1.10x faster                                                       |
| deepcopy_reduce                  | 1.30 us                                                        | 1.20 us: 1.08x faster                                                       |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                        |
| xml_etree_parse                  | 62.4 ms                                                        | 60.0 ms: 1.04x faster                                                       |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 291 ms: 1.03x faster                                                        |
| regex_dna                        | 94.6 ms                                                        | 92.8 ms: 1.02x faster                                                       |
| html5lib                         | 23.1 ms                                                        | 22.9 ms: 1.01x faster                                                       |
| docutils                         | 1.05 sec                                                       | 1.04 sec: 1.01x faster                                                      |
| dulwich_log                      | 19.8 ms                                                        | 19.7 ms: 1.01x faster                                                       |
| telco                            | 3.07 ms                                                        | 3.09 ms: 1.01x slower                                                       |
| json                             | 1.94 ms                                                        | 1.96 ms: 1.01x slower                                                       |
| fannkuch                         | 179 ms                                                         | 181 ms: 1.01x slower                                                        |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 231 ms: 1.03x slower                                                        |
| async_tree_eager_memoization     | 122 ms                                                         | 125 ms: 1.03x slower                                                        |
| python_startup                   | 8.63 ms                                                        | 8.95 ms: 1.04x slower                                                       |
| pycparser                        | 470 ms                                                         | 490 ms: 1.04x slower                                                        |
| json_loads                       | 10.8 us                                                        | 11.3 us: 1.05x slower                                                       |
| float                            | 31.4 ms                                                        | 33.3 ms: 1.06x slower                                                       |
| xml_etree_generate               | 35.8 ms                                                        | 38.1 ms: 1.06x slower                                                       |
| scimark_fft                      | 124 ms                                                         | 132 ms: 1.07x slower                                                        |
| async_tree_none_tg               | 133 ms                                                         | 142 ms: 1.07x slower                                                        |
| richards                         | 22.1 ms                                                        | 24.0 ms: 1.09x slower                                                       |
| sympy_integrate                  | 7.53 ms                                                        | 8.19 ms: 1.09x slower                                                       |
| bench_mp_pool                    | 37.8 ms                                                        | 41.3 ms: 1.09x slower                                                       |
| shortest_path                    | 225 ms                                                         | 246 ms: 1.09x slower                                                        |
| logging_simple                   | 2.24 us                                                        | 2.45 us: 1.10x slower                                                       |
| unpickle_pure_python             | 99.5 us                                                        | 109 us: 1.10x slower                                                        |
| sphinx                           | 409 ms                                                         | 451 ms: 1.10x slower                                                        |
| pprint_safe_repr                 | 322 ms                                                         | 356 ms: 1.11x slower                                                        |
| coroutines                       | 10.8 ms                                                        | 11.9 ms: 1.11x slower                                                       |
| logging_format                   | 2.45 us                                                        | 2.71 us: 1.11x slower                                                       |
| thrift                           | 309 us                                                         | 343 us: 1.11x slower                                                        |
| hexiom                           | 2.85 ms                                                        | 3.17 ms: 1.11x slower                                                       |
| richards_super                   | 24.7 ms                                                        | 27.6 ms: 1.12x slower                                                       |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.4 ms: 1.12x slower                                                       |
| meteor_contest                   | 47.9 ms                                                        | 53.8 ms: 1.12x slower                                                       |
| 2to3                             | 112 ms                                                         | 126 ms: 1.13x slower                                                        |
| bench_thread_pool                | 412 us                                                         | 469 us: 1.14x slower                                                        |
| spectral_norm                    | 43.7 ms                                                        | 50.0 ms: 1.14x slower                                                       |
| connected_components             | 208 ms                                                         | 238 ms: 1.15x slower                                                        |
| pprint_pformat                   | 650 ms                                                         | 749 ms: 1.15x slower                                                        |
| xml_etree_process                | 25.4 ms                                                        | 29.3 ms: 1.16x slower                                                       |
| async_tree_eager                 | 43.2 ms                                                        | 50.2 ms: 1.16x slower                                                       |
| python_startup_no_site           | 5.95 ms                                                        | 6.92 ms: 1.16x slower                                                       |
| sympy_str                        | 95.5 ms                                                        | 111 ms: 1.16x slower                                                        |
| nqueens                          | 37.2 ms                                                        | 43.7 ms: 1.17x slower                                                       |
| sympy_sum                        | 52.3 ms                                                        | 61.4 ms: 1.17x slower                                                       |
| chaos                            | 24.3 ms                                                        | 28.8 ms: 1.19x slower                                                       |
| sympy_expand                     | 159 ms                                                         | 190 ms: 1.19x slower                                                        |
| comprehensions                   | 6.80 us                                                        | 8.24 us: 1.21x slower                                                       |
| logging_silent                   | 40.6 ns                                                        | 49.2 ns: 1.21x slower                                                       |
| pickle_pure_python               | 130 us                                                         | 159 us: 1.22x slower                                                        |
| deltablue                        | 1.45 ms                                                        | 1.78 ms: 1.23x slower                                                       |
| pathlib                          | 11.1 ms                                                        | 13.8 ms: 1.24x slower                                                       |
| crypto_pyaes                     | 33.6 ms                                                        | 41.7 ms: 1.24x slower                                                       |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.21 ms: 1.24x slower                                                       |
| raytrace                         | 109 ms                                                         | 136 ms: 1.24x slower                                                        |
| many_optionals                   | 200 us                                                         | 252 us: 1.26x slower                                                        |
| mako                             | 4.41 ms                                                        | 5.58 ms: 1.26x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 270 ms: 1.30x slower                                                        |
| coverage                         | 31.2 ms                                                        | 40.9 ms: 1.31x slower                                                       |
| regex_compile                    | 47.9 ms                                                        | 64.1 ms: 1.34x slower                                                       |
| django_template                  | 12.5 ms                                                        | 16.8 ms: 1.34x slower                                                       |
| nbody                            | 42.5 ms                                                        | 59.3 ms: 1.39x slower                                                       |
| generators                       | 15.7 ms                                                        | 23.8 ms: 1.52x slower                                                       |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 156 ms: 1.52x slower                                                        |
| scimark_lu                       | 42.8 ms                                                        | 67.6 ms: 1.58x slower                                                       |
| async_tree_eager_tg              | 28.9 ms                                                        | 114 ms: 3.94x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.02x slower                                                                |

Benchmark hidden because not significant (4): async_tree_memoization_tg, async_tree_none, async_tree_memoization, async_tree_cpu_io_mixed
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261112-3.16.0a2+dev-eb21dea-NOGIL/bm-20261112-macm4pro-arm64-python-eb21dea301df801352ac-3.16.0a2+dev-eb21dea.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.016x slower

# HPT report

- Reliability score: 94.35% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.20x