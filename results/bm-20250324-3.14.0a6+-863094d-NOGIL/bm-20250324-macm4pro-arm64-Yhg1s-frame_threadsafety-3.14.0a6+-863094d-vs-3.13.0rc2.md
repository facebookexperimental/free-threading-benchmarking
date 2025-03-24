# Results vs. 3.13.0rc2

- fork: Yhg1s
- ref: frame_threadsafety
- machine: darwin-arm64
- commit hash: 863094d
- commit date: 2025-03-24
- overall geometric mean: 1.091x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250324-macm4pro-arm64-Yhg1s-frame_threadsafety-3.14.0a6+-863094d |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 133 ms: 1.19x slower                                                  |
| docutils       | 1.05 sec                                                       | 1.06 sec: 1.01x slower                                                |
| html5lib       | 23.1 ms                                                        | 24.5 ms: 1.06x slower                                                 |
| sphinx         | 409 ms                                                         | 442 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                          | 1.08x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250324-macm4pro-arm64-Yhg1s-frame_threadsafety-3.14.0a6+-863094d |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 225 ms: 2.32x faster                                                  |
| async_tree_eager_io              | 525 ms                                                         | 235 ms: 2.23x faster                                                  |
| async_tree_io_tg                 | 405 ms                                                         | 226 ms: 1.80x faster                                                  |
| async_tree_io                    | 386 ms                                                         | 242 ms: 1.59x faster                                                  |
| async_tree_memoization_tg        | 186 ms                                                         | 137 ms: 1.35x faster                                                  |
| async_tree_none_tg               | 133 ms                                                         | 101 ms: 1.32x faster                                                  |
| async_tree_memoization           | 184 ms                                                         | 146 ms: 1.26x faster                                                  |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 246 ms: 1.22x faster                                                  |
| async_tree_none                  | 142 ms                                                         | 117 ms: 1.22x faster                                                  |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 256 ms: 1.15x faster                                                  |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.01x faster                                                  |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 232 ms: 1.03x slower                                                  |
| coroutines                       | 10.8 ms                                                        | 11.9 ms: 1.11x slower                                                 |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 236 ms: 1.13x slower                                                  |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 124 ms: 1.21x slower                                                  |
| async_tree_eager                 | 43.2 ms                                                        | 56.6 ms: 1.31x slower                                                 |
| async_tree_eager_tg              | 28.9 ms                                                        | 89.6 ms: 3.10x slower                                                 |
| Geometric mean                   | (ref)                                                          | 1.12x faster                                                          |

Benchmark hidden because not significant (2): async_tree_eager_memoization, async_generators

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250324-macm4pro-arm64-Yhg1s-frame_threadsafety-3.14.0a6+-863094d |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 163 ms: 1.02x faster                                                  |
| float          | 31.4 ms                                                        | 35.9 ms: 1.14x slower                                                 |
| nbody          | 42.5 ms                                                        | 78.5 ms: 1.85x slower                                                 |
| Geometric mean | (ref)                                                          | 1.27x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250324-macm4pro-arm64-Yhg1s-frame_threadsafety-3.14.0a6+-863094d |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                 |
| regex_v8       | 10.7 ms                                                        | 9.64 ms: 1.11x faster                                                 |
| regex_dna      | 94.6 ms                                                        | 93.3 ms: 1.01x faster                                                 |
| regex_compile  | 47.9 ms                                                        | 59.7 ms: 1.25x slower                                                 |
| Geometric mean | (ref)                                                          | 1.00x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250324-macm4pro-arm64-Yhg1s-frame_threadsafety-3.14.0a6+-863094d |
|----------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_parse      | 62.4 ms                                                        | 56.0 ms: 1.11x faster                                                 |
| xml_etree_iterparse  | 46.1 ms                                                        | 42.0 ms: 1.10x faster                                                 |
| tomli_loads          | 1000 ms                                                        | 1.08 sec: 1.09x slower                                                |
| json_loads           | 10.8 us                                                        | 11.9 us: 1.10x slower                                                 |
| json_dumps           | 4.65 ms                                                        | 5.17 ms: 1.11x slower                                                 |
| xml_etree_generate   | 35.8 ms                                                        | 41.0 ms: 1.14x slower                                                 |
| xml_etree_process    | 25.4 ms                                                        | 30.5 ms: 1.20x slower                                                 |
| unpickle_pure_python | 99.5 us                                                        | 128 us: 1.29x slower                                                  |
| pickle_pure_python   | 130 us                                                         | 172 us: 1.32x slower                                                  |
| Geometric mean       | (ref)                                                          | 1.11x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250324-macm4pro-arm64-Yhg1s-frame_threadsafety-3.14.0a6+-863094d |
|------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.28 ms: 1.07x slower                                                 |
| python_startup_no_site | 5.95 ms                                                        | 7.31 ms: 1.23x slower                                                 |
| Geometric mean         | (ref)                                                          | 1.15x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250324-macm4pro-arm64-Yhg1s-frame_threadsafety-3.14.0a6+-863094d |
|-----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 26.4 ms: 1.23x slower                                                 |
| genshi_text     | 9.97 ms                                                        | 13.1 ms: 1.31x slower                                                 |
| mako            | 4.41 ms                                                        | 6.20 ms: 1.41x slower                                                 |
| django_template | 12.5 ms                                                        | 18.5 ms: 1.48x slower                                                 |
| Geometric mean  | (ref)                                                          | 1.35x slower                                                          |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250324-macm4pro-arm64-Yhg1s-frame_threadsafety-3.14.0a6+-863094d |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 225 ms: 2.32x faster                                                  |
| async_tree_eager_io              | 525 ms                                                         | 235 ms: 2.23x faster                                                  |
| gc_traversal                     | 2.04 ms                                                        | 932 us: 2.19x faster                                                  |
| create_gc_cycles                 | 993 us                                                         | 506 us: 1.96x faster                                                  |
| async_tree_io_tg                 | 405 ms                                                         | 226 ms: 1.80x faster                                                  |
| async_tree_io                    | 386 ms                                                         | 242 ms: 1.59x faster                                                  |
| k_core                           | 1.46 sec                                                       | 1.06 sec: 1.39x faster                                                |
| async_tree_memoization_tg        | 186 ms                                                         | 137 ms: 1.35x faster                                                  |
| async_tree_none_tg               | 133 ms                                                         | 101 ms: 1.32x faster                                                  |
| async_tree_memoization           | 184 ms                                                         | 146 ms: 1.26x faster                                                  |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 246 ms: 1.22x faster                                                  |
| async_tree_none                  | 142 ms                                                         | 117 ms: 1.22x faster                                                  |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 256 ms: 1.15x faster                                                  |
| deepcopy                         | 145 us                                                         | 129 us: 1.13x faster                                                  |
| sqlite_synth                     | 948 ns                                                         | 846 ns: 1.12x faster                                                  |
| xml_etree_parse                  | 62.4 ms                                                        | 56.0 ms: 1.11x faster                                                 |
| regex_effbot                     | 1.61 ms                                                        | 1.45 ms: 1.11x faster                                                 |
| regex_v8                         | 10.7 ms                                                        | 9.64 ms: 1.11x faster                                                 |
| xml_etree_iterparse              | 46.1 ms                                                        | 42.0 ms: 1.10x faster                                                 |
| pidigits                         | 166 ms                                                         | 163 ms: 1.02x faster                                                  |
| regex_dna                        | 94.6 ms                                                        | 93.3 ms: 1.01x faster                                                 |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.01x faster                                                  |
| docutils                         | 1.05 sec                                                       | 1.06 sec: 1.01x slower                                                |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 232 ms: 1.03x slower                                                  |
| go                               | 72.6 ms                                                        | 75.0 ms: 1.03x slower                                                 |
| json                             | 1.94 ms                                                        | 2.01 ms: 1.04x slower                                                 |
| deepcopy_memo                    | 16.5 us                                                        | 17.2 us: 1.04x slower                                                 |
| pathlib                          | 11.1 ms                                                        | 11.8 ms: 1.06x slower                                                 |
| html5lib                         | 23.1 ms                                                        | 24.5 ms: 1.06x slower                                                 |
| pyflate                          | 222 ms                                                         | 236 ms: 1.06x slower                                                  |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.26 sec: 1.06x slower                                                |
| deepcopy_reduce                  | 1.30 us                                                        | 1.38 us: 1.07x slower                                                 |
| bench_mp_pool                    | 37.8 ms                                                        | 40.6 ms: 1.07x slower                                                 |
| python_startup                   | 8.63 ms                                                        | 9.28 ms: 1.07x slower                                                 |
| sphinx                           | 409 ms                                                         | 442 ms: 1.08x slower                                                  |
| tomli_loads                      | 1000 ms                                                        | 1.08 sec: 1.09x slower                                                |
| pycparser                        | 470 ms                                                         | 511 ms: 1.09x slower                                                  |
| json_loads                       | 10.8 us                                                        | 11.9 us: 1.10x slower                                                 |
| scimark_sor                      | 64.0 ms                                                        | 70.5 ms: 1.10x slower                                                 |
| shortest_path                    | 225 ms                                                         | 248 ms: 1.10x slower                                                  |
| coroutines                       | 10.8 ms                                                        | 11.9 ms: 1.11x slower                                                 |
| json_dumps                       | 4.65 ms                                                        | 5.17 ms: 1.11x slower                                                 |
| mdp                              | 1.06 sec                                                       | 1.19 sec: 1.13x slower                                                |
| thrift                           | 309 us                                                         | 350 us: 1.13x slower                                                  |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 236 ms: 1.13x slower                                                  |
| connected_components             | 208 ms                                                         | 236 ms: 1.13x slower                                                  |
| float                            | 31.4 ms                                                        | 35.9 ms: 1.14x slower                                                 |
| xml_etree_generate               | 35.8 ms                                                        | 41.0 ms: 1.14x slower                                                 |
| sqlalchemy_declarative           | 44.4 ms                                                        | 51.8 ms: 1.17x slower                                                 |
| telco                            | 3.07 ms                                                        | 3.63 ms: 1.18x slower                                                 |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.96 ms: 1.19x slower                                                 |
| 2to3                             | 112 ms                                                         | 133 ms: 1.19x slower                                                  |
| pylint                           | 106 ms                                                         | 126 ms: 1.20x slower                                                  |
| xml_etree_process                | 25.4 ms                                                        | 30.5 ms: 1.20x slower                                                 |
| sympy_integrate                  | 7.53 ms                                                        | 9.08 ms: 1.21x slower                                                 |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 124 ms: 1.21x slower                                                  |
| coverage                         | 31.2 ms                                                        | 38.3 ms: 1.23x slower                                                 |
| python_startup_no_site           | 5.95 ms                                                        | 7.31 ms: 1.23x slower                                                 |
| sympy_sum                        | 52.3 ms                                                        | 64.3 ms: 1.23x slower                                                 |
| genshi_xml                       | 21.4 ms                                                        | 26.4 ms: 1.23x slower                                                 |
| regex_compile                    | 47.9 ms                                                        | 59.7 ms: 1.25x slower                                                 |
| meteor_contest                   | 47.9 ms                                                        | 59.9 ms: 1.25x slower                                                 |
| typing_runtime_protocols         | 64.6 us                                                        | 80.9 us: 1.25x slower                                                 |
| richards                         | 22.1 ms                                                        | 27.6 ms: 1.25x slower                                                 |
| sympy_str                        | 95.5 ms                                                        | 120 ms: 1.26x slower                                                  |
| fannkuch                         | 179 ms                                                         | 226 ms: 1.27x slower                                                  |
| many_optionals                   | 200 us                                                         | 256 us: 1.28x slower                                                  |
| richards_super                   | 24.7 ms                                                        | 31.6 ms: 1.28x slower                                                 |
| sympy_expand                     | 159 ms                                                         | 205 ms: 1.28x slower                                                  |
| pprint_safe_repr                 | 322 ms                                                         | 413 ms: 1.28x slower                                                  |
| logging_simple                   | 2.24 us                                                        | 2.88 us: 1.29x slower                                                 |
| unpickle_pure_python             | 99.5 us                                                        | 128 us: 1.29x slower                                                  |
| logging_format                   | 2.45 us                                                        | 3.17 us: 1.30x slower                                                 |
| pprint_pformat                   | 650 ms                                                         | 843 ms: 1.30x slower                                                  |
| async_tree_eager                 | 43.2 ms                                                        | 56.6 ms: 1.31x slower                                                 |
| genshi_text                      | 9.97 ms                                                        | 13.1 ms: 1.31x slower                                                 |
| scimark_fft                      | 124 ms                                                         | 163 ms: 1.32x slower                                                  |
| pickle_pure_python               | 130 us                                                         | 172 us: 1.32x slower                                                  |
| nqueens                          | 37.2 ms                                                        | 49.6 ms: 1.33x slower                                                 |
| scimark_monte_carlo              | 29.9 ms                                                        | 40.7 ms: 1.36x slower                                                 |
| chaos                            | 24.3 ms                                                        | 33.2 ms: 1.37x slower                                                 |
| spectral_norm                    | 43.7 ms                                                        | 60.0 ms: 1.37x slower                                                 |
| hexiom                           | 2.85 ms                                                        | 3.94 ms: 1.38x slower                                                 |
| logging_silent                   | 40.6 ns                                                        | 56.4 ns: 1.39x slower                                                 |
| deltablue                        | 1.45 ms                                                        | 2.02 ms: 1.39x slower                                                 |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.48 ms: 1.40x slower                                                 |
| crypto_pyaes                     | 33.6 ms                                                        | 47.1 ms: 1.40x slower                                                 |
| mako                             | 4.41 ms                                                        | 6.20 ms: 1.41x slower                                                 |
| generators                       | 15.7 ms                                                        | 22.3 ms: 1.42x slower                                                 |
| raytrace                         | 109 ms                                                         | 160 ms: 1.47x slower                                                  |
| django_template                  | 12.5 ms                                                        | 18.5 ms: 1.48x slower                                                 |
| comprehensions                   | 6.80 us                                                        | 10.1 us: 1.49x slower                                                 |
| subparsers                       | 6.26 ms                                                        | 9.50 ms: 1.52x slower                                                 |
| bench_thread_pool                | 412 us                                                         | 625 us: 1.52x slower                                                  |
| scimark_lu                       | 42.8 ms                                                        | 67.5 ms: 1.58x slower                                                 |
| nbody                            | 42.5 ms                                                        | 78.5 ms: 1.85x slower                                                 |
| async_tree_eager_tg              | 28.9 ms                                                        | 89.6 ms: 3.10x slower                                                 |
| Geometric mean                   | (ref)                                                          | 1.11x slower                                                          |

Benchmark hidden because not significant (3): async_tree_eager_memoization, dulwich_log, async_generators
Ignored benchmarks (9) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250324-3.14.0a6+-863094d-NOGIL/bm-20250324-macm4pro-arm64-Yhg1s-frame_threadsafety-3.14.0a6+-863094d.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.091x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.05x

# Memory
- memory change: 1.18x