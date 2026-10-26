# Results vs. 3.13.0rc2

- fork: python
- ref: 1c327a4464fa47f5d3aa
- machine: darwin-arm64
- commit hash: 1c327a4
- commit date: 2026-10-26
- overall geometric mean: 1.011x faster
- HPT reliability: 59.09%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261026-macm4pro-arm64-python-1c327a4464fa47f5d3aa-3.16.0a1+dev-1c327a4 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 121 ms: 1.09x slower                                                        |
| docutils       | 1.05 sec                                                       | 1.02 sec: 1.03x faster                                                      |
| html5lib       | 23.1 ms                                                        | 22.5 ms: 1.03x faster                                                       |
| sphinx         | 409 ms                                                         | 437 ms: 1.07x slower                                                        |
| Geometric mean | (ref)                                                          | 1.02x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261026-macm4pro-arm64-python-1c327a4464fa47f5d3aa-3.16.0a1+dev-1c327a4 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 285 ms: 1.84x faster                                                        |
| async_tree_eager_io_tg           | 521 ms                                                         | 283 ms: 1.84x faster                                                        |
| async_generators                 | 193 ms                                                         | 109 ms: 1.78x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 286 ms: 1.42x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 291 ms: 1.33x faster                                                        |
| asyncio_websockets               | 194 ms                                                         | 179 ms: 1.08x faster                                                        |
| async_tree_none                  | 142 ms                                                         | 134 ms: 1.07x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 175 ms: 1.06x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 285 ms: 1.06x faster                                                        |
| async_tree_memoization           | 184 ms                                                         | 176 ms: 1.05x faster                                                        |
| coroutines                       | 10.8 ms                                                        | 11.5 ms: 1.07x slower                                                       |
| async_tree_eager                 | 43.2 ms                                                        | 48.1 ms: 1.11x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 261 ms: 1.25x slower                                                        |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 159 ms: 1.55x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 107 ms: 3.71x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.03x faster                                                                |

Benchmark hidden because not significant (4): async_tree_cpu_io_mixed, async_tree_eager_memoization, async_tree_eager_cpu_io_mixed, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261026-macm4pro-arm64-python-1c327a4464fa47f5d3aa-3.16.0a1+dev-1c327a4 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 157 ms: 1.06x faster                                                        |
| float          | 31.4 ms                                                        | 32.0 ms: 1.02x slower                                                       |
| nbody          | 42.5 ms                                                        | 59.0 ms: 1.39x slower                                                       |
| Geometric mean | (ref)                                                          | 1.10x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261026-macm4pro-arm64-python-1c327a4464fa47f5d3aa-3.16.0a1+dev-1c327a4 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.31 ms: 1.23x faster                                                       |
| regex_v8       | 10.7 ms                                                        | 8.96 ms: 1.19x faster                                                       |
| regex_dna      | 94.6 ms                                                        | 88.6 ms: 1.07x faster                                                       |
| regex_compile  | 47.9 ms                                                        | 62.8 ms: 1.31x slower                                                       |
| Geometric mean | (ref)                                                          | 1.05x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261026-macm4pro-arm64-python-1c327a4464fa47f5d3aa-3.16.0a1+dev-1c327a4 |
|----------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.66 ms: 1.27x faster                                                       |
| tomli_loads          | 1000 ms                                                        | 884 ms: 1.13x faster                                                        |
| xml_etree_iterparse  | 46.1 ms                                                        | 41.0 ms: 1.12x faster                                                       |
| xml_etree_parse      | 62.4 ms                                                        | 59.9 ms: 1.04x faster                                                       |
| json_loads           | 10.8 us                                                        | 10.7 us: 1.01x faster                                                       |
| xml_etree_generate   | 35.8 ms                                                        | 38.3 ms: 1.07x slower                                                       |
| unpickle_pure_python | 99.5 us                                                        | 108 us: 1.08x slower                                                        |
| xml_etree_process    | 25.4 ms                                                        | 29.1 ms: 1.15x slower                                                       |
| pickle_pure_python   | 130 us                                                         | 155 us: 1.19x slower                                                        |
| Geometric mean       | (ref)                                                          | 1.01x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261026-macm4pro-arm64-python-1c327a4464fa47f5d3aa-3.16.0a1+dev-1c327a4 |
|------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.78 ms: 1.02x slower                                                       |
| python_startup_no_site | 5.95 ms                                                        | 6.80 ms: 1.14x slower                                                       |
| Geometric mean         | (ref)                                                          | 1.08x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261026-macm4pro-arm64-python-1c327a4464fa47f5d3aa-3.16.0a1+dev-1c327a4 |
|-----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 5.55 ms: 1.26x slower                                                       |
| django_template | 12.5 ms                                                        | 16.7 ms: 1.33x slower                                                       |
| Geometric mean  | (ref)                                                          | 1.30x slower                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20261026-macm4pro-arm64-python-1c327a4464fa47f5d3aa-3.16.0a1+dev-1c327a4 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 747 us: 2.73x faster                                                        |
| create_gc_cycles                 | 993 us                                                         | 457 us: 2.17x faster                                                        |
| pylint                           | 106 ms                                                         | 50.5 ms: 2.09x faster                                                       |
| mdp                              | 1.06 sec                                                       | 572 ms: 1.85x faster                                                        |
| async_tree_eager_io              | 525 ms                                                         | 285 ms: 1.84x faster                                                        |
| async_tree_eager_io_tg           | 521 ms                                                         | 283 ms: 1.84x faster                                                        |
| async_generators                 | 193 ms                                                         | 109 ms: 1.78x faster                                                        |
| subparsers                       | 6.26 ms                                                        | 4.19 ms: 1.49x faster                                                       |
| k_core                           | 1.46 sec                                                       | 995 ms: 1.47x faster                                                        |
| async_tree_io_tg                 | 405 ms                                                         | 286 ms: 1.42x faster                                                        |
| deepcopy                         | 145 us                                                         | 108 us: 1.34x faster                                                        |
| async_tree_io                    | 386 ms                                                         | 291 ms: 1.33x faster                                                        |
| json_dumps                       | 4.65 ms                                                        | 3.66 ms: 1.27x faster                                                       |
| regex_effbot                     | 1.61 ms                                                        | 1.31 ms: 1.23x faster                                                       |
| go                               | 72.6 ms                                                        | 59.0 ms: 1.23x faster                                                       |
| typing_runtime_protocols         | 64.6 us                                                        | 53.5 us: 1.21x faster                                                       |
| regex_v8                         | 10.7 ms                                                        | 8.96 ms: 1.19x faster                                                       |
| deepcopy_memo                    | 16.5 us                                                        | 13.9 us: 1.19x faster                                                       |
| sqlite_synth                     | 948 ns                                                         | 820 ns: 1.16x faster                                                        |
| pyflate                          | 222 ms                                                         | 195 ms: 1.14x faster                                                        |
| tomli_loads                      | 1000 ms                                                        | 884 ms: 1.13x faster                                                        |
| xml_etree_iterparse              | 46.1 ms                                                        | 41.0 ms: 1.12x faster                                                       |
| scimark_sor                      | 64.0 ms                                                        | 57.1 ms: 1.12x faster                                                       |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.91 sec: 1.11x faster                                                      |
| deepcopy_reduce                  | 1.30 us                                                        | 1.16 us: 1.11x faster                                                       |
| asyncio_websockets               | 194 ms                                                         | 179 ms: 1.08x faster                                                        |
| regex_dna                        | 94.6 ms                                                        | 88.6 ms: 1.07x faster                                                       |
| async_tree_none                  | 142 ms                                                         | 134 ms: 1.07x faster                                                        |
| pidigits                         | 166 ms                                                         | 157 ms: 1.06x faster                                                        |
| async_tree_memoization_tg        | 186 ms                                                         | 175 ms: 1.06x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 285 ms: 1.06x faster                                                        |
| pathlib                          | 11.1 ms                                                        | 10.6 ms: 1.05x faster                                                       |
| dulwich_log                      | 19.8 ms                                                        | 18.8 ms: 1.05x faster                                                       |
| async_tree_memoization           | 184 ms                                                         | 176 ms: 1.05x faster                                                        |
| xml_etree_parse                  | 62.4 ms                                                        | 59.9 ms: 1.04x faster                                                       |
| json                             | 1.94 ms                                                        | 1.88 ms: 1.04x faster                                                       |
| docutils                         | 1.05 sec                                                       | 1.02 sec: 1.03x faster                                                      |
| html5lib                         | 23.1 ms                                                        | 22.5 ms: 1.03x faster                                                       |
| json_loads                       | 10.8 us                                                        | 10.7 us: 1.01x faster                                                       |
| python_startup                   | 8.63 ms                                                        | 8.78 ms: 1.02x slower                                                       |
| float                            | 31.4 ms                                                        | 32.0 ms: 1.02x slower                                                       |
| sympy_integrate                  | 7.53 ms                                                        | 7.91 ms: 1.05x slower                                                       |
| scimark_fft                      | 124 ms                                                         | 131 ms: 1.06x slower                                                        |
| sphinx                           | 409 ms                                                         | 437 ms: 1.07x slower                                                        |
| pprint_safe_repr                 | 322 ms                                                         | 344 ms: 1.07x slower                                                        |
| coroutines                       | 10.8 ms                                                        | 11.5 ms: 1.07x slower                                                       |
| xml_etree_generate               | 35.8 ms                                                        | 38.3 ms: 1.07x slower                                                       |
| richards                         | 22.1 ms                                                        | 23.7 ms: 1.08x slower                                                       |
| meteor_contest                   | 47.9 ms                                                        | 51.5 ms: 1.08x slower                                                       |
| unpickle_pure_python             | 99.5 us                                                        | 108 us: 1.08x slower                                                        |
| hexiom                           | 2.85 ms                                                        | 3.08 ms: 1.08x slower                                                       |
| logging_simple                   | 2.24 us                                                        | 2.42 us: 1.08x slower                                                       |
| logging_format                   | 2.45 us                                                        | 2.65 us: 1.09x slower                                                       |
| 2to3                             | 112 ms                                                         | 121 ms: 1.09x slower                                                        |
| pprint_pformat                   | 650 ms                                                         | 708 ms: 1.09x slower                                                        |
| richards_super                   | 24.7 ms                                                        | 27.1 ms: 1.10x slower                                                       |
| shortest_path                    | 225 ms                                                         | 247 ms: 1.10x slower                                                        |
| bench_thread_pool                | 412 us                                                         | 454 us: 1.10x slower                                                        |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.3 ms: 1.11x slower                                                       |
| async_tree_eager                 | 43.2 ms                                                        | 48.1 ms: 1.11x slower                                                       |
| spectral_norm                    | 43.7 ms                                                        | 48.8 ms: 1.12x slower                                                       |
| thrift                           | 309 us                                                         | 345 us: 1.12x slower                                                        |
| bench_mp_pool                    | 37.8 ms                                                        | 42.6 ms: 1.13x slower                                                       |
| nqueens                          | 37.2 ms                                                        | 42.1 ms: 1.13x slower                                                       |
| sympy_sum                        | 52.3 ms                                                        | 59.7 ms: 1.14x slower                                                       |
| python_startup_no_site           | 5.95 ms                                                        | 6.80 ms: 1.14x slower                                                       |
| xml_etree_process                | 25.4 ms                                                        | 29.1 ms: 1.15x slower                                                       |
| sympy_str                        | 95.5 ms                                                        | 110 ms: 1.15x slower                                                        |
| connected_components             | 208 ms                                                         | 240 ms: 1.16x slower                                                        |
| chaos                            | 24.3 ms                                                        | 28.3 ms: 1.17x slower                                                       |
| sympy_expand                     | 159 ms                                                         | 187 ms: 1.17x slower                                                        |
| logging_silent                   | 40.6 ns                                                        | 47.9 ns: 1.18x slower                                                       |
| comprehensions                   | 6.80 us                                                        | 8.06 us: 1.18x slower                                                       |
| pickle_pure_python               | 130 us                                                         | 155 us: 1.19x slower                                                        |
| deltablue                        | 1.45 ms                                                        | 1.74 ms: 1.20x slower                                                       |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.14 ms: 1.20x slower                                                       |
| many_optionals                   | 200 us                                                         | 242 us: 1.21x slower                                                        |
| crypto_pyaes                     | 33.6 ms                                                        | 40.6 ms: 1.21x slower                                                       |
| raytrace                         | 109 ms                                                         | 135 ms: 1.24x slower                                                        |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 261 ms: 1.25x slower                                                        |
| mako                             | 4.41 ms                                                        | 5.55 ms: 1.26x slower                                                       |
| coverage                         | 31.2 ms                                                        | 40.0 ms: 1.28x slower                                                       |
| regex_compile                    | 47.9 ms                                                        | 62.8 ms: 1.31x slower                                                       |
| django_template                  | 12.5 ms                                                        | 16.7 ms: 1.33x slower                                                       |
| nbody                            | 42.5 ms                                                        | 59.0 ms: 1.39x slower                                                       |
| generators                       | 15.7 ms                                                        | 22.6 ms: 1.44x slower                                                       |
| scimark_lu                       | 42.8 ms                                                        | 66.3 ms: 1.55x slower                                                       |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 159 ms: 1.55x slower                                                        |
| async_tree_eager_tg              | 28.9 ms                                                        | 107 ms: 3.71x slower                                                        |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                                |

Benchmark hidden because not significant (7): async_tree_cpu_io_mixed, async_tree_eager_memoization, pycparser, fannkuch, async_tree_eager_cpu_io_mixed, telco, async_tree_none_tg
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261026-3.16.0a1+dev-1c327a4-NOGIL/bm-20261026-macm4pro-arm64-python-1c327a4464fa47f5d3aa-3.16.0a1+dev-1c327a4.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.011x faster

# HPT report

- Reliability score: 59.09% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.23x