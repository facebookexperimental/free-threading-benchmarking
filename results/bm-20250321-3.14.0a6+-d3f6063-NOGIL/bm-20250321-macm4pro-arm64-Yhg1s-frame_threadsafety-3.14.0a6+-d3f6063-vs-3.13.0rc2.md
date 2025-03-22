# Results vs. 3.13.0rc2

- fork: Yhg1s
- ref: frame_threadsafety
- machine: darwin-arm64
- commit hash: d3f6063
- commit date: 2025-03-21
- overall geometric mean: 1.087x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250321-macm4pro-arm64-Yhg1s-frame_threadsafety-3.14.0a6+-d3f6063 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 130 ms: 1.17x slower                                                  |
| html5lib       | 23.1 ms                                                        | 25.3 ms: 1.09x slower                                                 |
| sphinx         | 409 ms                                                         | 442 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                          | 1.08x slower                                                          |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250321-macm4pro-arm64-Yhg1s-frame_threadsafety-3.14.0a6+-d3f6063 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 222 ms: 2.35x faster                                                  |
| async_tree_eager_io              | 525 ms                                                         | 232 ms: 2.26x faster                                                  |
| async_tree_io_tg                 | 405 ms                                                         | 223 ms: 1.81x faster                                                  |
| async_tree_io                    | 386 ms                                                         | 239 ms: 1.62x faster                                                  |
| async_tree_memoization_tg        | 186 ms                                                         | 136 ms: 1.36x faster                                                  |
| async_tree_none_tg               | 133 ms                                                         | 99.2 ms: 1.34x faster                                                 |
| async_tree_memoization           | 184 ms                                                         | 145 ms: 1.27x faster                                                  |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 242 ms: 1.25x faster                                                  |
| async_tree_none                  | 142 ms                                                         | 115 ms: 1.24x faster                                                  |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 252 ms: 1.17x faster                                                  |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                  |
| async_tree_eager_memoization     | 122 ms                                                         | 120 ms: 1.01x faster                                                  |
| async_generators                 | 193 ms                                                         | 191 ms: 1.01x faster                                                  |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 227 ms: 1.01x slower                                                  |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 231 ms: 1.11x slower                                                  |
| coroutines                       | 10.8 ms                                                        | 12.2 ms: 1.13x slower                                                 |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 123 ms: 1.19x slower                                                  |
| async_tree_eager                 | 43.2 ms                                                        | 56.0 ms: 1.30x slower                                                 |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.5 ms: 3.03x slower                                                 |
| Geometric mean                   | (ref)                                                          | 1.14x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250321-macm4pro-arm64-Yhg1s-frame_threadsafety-3.14.0a6+-d3f6063 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 161 ms: 1.03x faster                                                  |
| float          | 31.4 ms                                                        | 35.8 ms: 1.14x slower                                                 |
| nbody          | 42.5 ms                                                        | 77.7 ms: 1.83x slower                                                 |
| Geometric mean | (ref)                                                          | 1.26x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250321-macm4pro-arm64-Yhg1s-frame_threadsafety-3.14.0a6+-d3f6063 |
|----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.64 ms: 1.11x faster                                                 |
| regex_effbot   | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                 |
| regex_dna      | 94.6 ms                                                        | 98.5 ms: 1.04x slower                                                 |
| regex_compile  | 47.9 ms                                                        | 59.4 ms: 1.24x slower                                                 |
| Geometric mean | (ref)                                                          | 1.01x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250321-macm4pro-arm64-Yhg1s-frame_threadsafety-3.14.0a6+-d3f6063 |
|----------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 40.2 ms: 1.15x faster                                                 |
| xml_etree_parse      | 62.4 ms                                                        | 56.2 ms: 1.11x faster                                                 |
| tomli_loads          | 1000 ms                                                        | 1.08 sec: 1.08x slower                                                |
| json_loads           | 10.8 us                                                        | 11.8 us: 1.09x slower                                                 |
| json_dumps           | 4.65 ms                                                        | 5.19 ms: 1.12x slower                                                 |
| xml_etree_generate   | 35.8 ms                                                        | 41.1 ms: 1.15x slower                                                 |
| xml_etree_process    | 25.4 ms                                                        | 30.7 ms: 1.21x slower                                                 |
| unpickle_pure_python | 99.5 us                                                        | 127 us: 1.28x slower                                                  |
| pickle_pure_python   | 130 us                                                         | 171 us: 1.31x slower                                                  |
| Geometric mean       | (ref)                                                          | 1.10x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250321-macm4pro-arm64-Yhg1s-frame_threadsafety-3.14.0a6+-d3f6063 |
|------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.23 ms: 1.07x slower                                                 |
| python_startup_no_site | 5.95 ms                                                        | 7.28 ms: 1.22x slower                                                 |
| Geometric mean         | (ref)                                                          | 1.14x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250321-macm4pro-arm64-Yhg1s-frame_threadsafety-3.14.0a6+-d3f6063 |
|-----------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 26.3 ms: 1.23x slower                                                 |
| genshi_text     | 9.97 ms                                                        | 13.1 ms: 1.32x slower                                                 |
| mako            | 4.41 ms                                                        | 6.21 ms: 1.41x slower                                                 |
| django_template | 12.5 ms                                                        | 18.3 ms: 1.47x slower                                                 |
| Geometric mean  | (ref)                                                          | 1.35x slower                                                          |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250321-macm4pro-arm64-Yhg1s-frame_threadsafety-3.14.0a6+-d3f6063 |
|----------------------------------|:--------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 222 ms: 2.35x faster                                                  |
| async_tree_eager_io              | 525 ms                                                         | 232 ms: 2.26x faster                                                  |
| gc_traversal                     | 2.04 ms                                                        | 935 us: 2.18x faster                                                  |
| create_gc_cycles                 | 993 us                                                         | 510 us: 1.95x faster                                                  |
| async_tree_io_tg                 | 405 ms                                                         | 223 ms: 1.81x faster                                                  |
| async_tree_io                    | 386 ms                                                         | 239 ms: 1.62x faster                                                  |
| k_core                           | 1.46 sec                                                       | 1.06 sec: 1.38x faster                                                |
| async_tree_memoization_tg        | 186 ms                                                         | 136 ms: 1.36x faster                                                  |
| async_tree_none_tg               | 133 ms                                                         | 99.2 ms: 1.34x faster                                                 |
| async_tree_memoization           | 184 ms                                                         | 145 ms: 1.27x faster                                                  |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 242 ms: 1.25x faster                                                  |
| async_tree_none                  | 142 ms                                                         | 115 ms: 1.24x faster                                                  |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 252 ms: 1.17x faster                                                  |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.2 ms: 1.15x faster                                                 |
| deepcopy                         | 145 us                                                         | 128 us: 1.13x faster                                                  |
| sqlite_synth                     | 948 ns                                                         | 840 ns: 1.13x faster                                                  |
| xml_etree_parse                  | 62.4 ms                                                        | 56.2 ms: 1.11x faster                                                 |
| regex_v8                         | 10.7 ms                                                        | 9.64 ms: 1.11x faster                                                 |
| regex_effbot                     | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                 |
| pidigits                         | 166 ms                                                         | 161 ms: 1.03x faster                                                  |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                  |
| async_tree_eager_memoization     | 122 ms                                                         | 120 ms: 1.01x faster                                                  |
| dulwich_log                      | 19.8 ms                                                        | 19.6 ms: 1.01x faster                                                 |
| async_generators                 | 193 ms                                                         | 191 ms: 1.01x faster                                                  |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 227 ms: 1.01x slower                                                  |
| go                               | 72.6 ms                                                        | 74.1 ms: 1.02x slower                                                 |
| json                             | 1.94 ms                                                        | 1.99 ms: 1.02x slower                                                 |
| deepcopy_memo                    | 16.5 us                                                        | 17.1 us: 1.04x slower                                                 |
| regex_dna                        | 94.6 ms                                                        | 98.5 ms: 1.04x slower                                                 |
| pyflate                          | 222 ms                                                         | 232 ms: 1.05x slower                                                  |
| bench_mp_pool                    | 37.8 ms                                                        | 39.9 ms: 1.06x slower                                                 |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.25 sec: 1.06x slower                                                |
| pathlib                          | 11.1 ms                                                        | 11.8 ms: 1.06x slower                                                 |
| deepcopy_reduce                  | 1.30 us                                                        | 1.38 us: 1.07x slower                                                 |
| python_startup                   | 8.63 ms                                                        | 9.23 ms: 1.07x slower                                                 |
| tomli_loads                      | 1000 ms                                                        | 1.08 sec: 1.08x slower                                                |
| pycparser                        | 470 ms                                                         | 508 ms: 1.08x slower                                                  |
| sphinx                           | 409 ms                                                         | 442 ms: 1.08x slower                                                  |
| json_loads                       | 10.8 us                                                        | 11.8 us: 1.09x slower                                                 |
| html5lib                         | 23.1 ms                                                        | 25.3 ms: 1.09x slower                                                 |
| scimark_sor                      | 64.0 ms                                                        | 70.1 ms: 1.09x slower                                                 |
| shortest_path                    | 225 ms                                                         | 248 ms: 1.10x slower                                                  |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 231 ms: 1.11x slower                                                  |
| json_dumps                       | 4.65 ms                                                        | 5.19 ms: 1.12x slower                                                 |
| mdp                              | 1.06 sec                                                       | 1.19 sec: 1.13x slower                                                |
| thrift                           | 309 us                                                         | 350 us: 1.13x slower                                                  |
| connected_components             | 208 ms                                                         | 236 ms: 1.13x slower                                                  |
| coroutines                       | 10.8 ms                                                        | 12.2 ms: 1.13x slower                                                 |
| float                            | 31.4 ms                                                        | 35.8 ms: 1.14x slower                                                 |
| xml_etree_generate               | 35.8 ms                                                        | 41.1 ms: 1.15x slower                                                 |
| sqlalchemy_declarative           | 44.4 ms                                                        | 51.5 ms: 1.16x slower                                                 |
| 2to3                             | 112 ms                                                         | 130 ms: 1.17x slower                                                  |
| telco                            | 3.07 ms                                                        | 3.60 ms: 1.17x slower                                                 |
| pylint                           | 106 ms                                                         | 125 ms: 1.19x slower                                                  |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.95 ms: 1.19x slower                                                 |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 123 ms: 1.19x slower                                                  |
| xml_etree_process                | 25.4 ms                                                        | 30.7 ms: 1.21x slower                                                 |
| sympy_integrate                  | 7.53 ms                                                        | 9.13 ms: 1.21x slower                                                 |
| sympy_sum                        | 52.3 ms                                                        | 64.0 ms: 1.22x slower                                                 |
| python_startup_no_site           | 5.95 ms                                                        | 7.28 ms: 1.22x slower                                                 |
| coverage                         | 31.2 ms                                                        | 38.2 ms: 1.23x slower                                                 |
| genshi_xml                       | 21.4 ms                                                        | 26.3 ms: 1.23x slower                                                 |
| regex_compile                    | 47.9 ms                                                        | 59.4 ms: 1.24x slower                                                 |
| fannkuch                         | 179 ms                                                         | 221 ms: 1.24x slower                                                  |
| meteor_contest                   | 47.9 ms                                                        | 59.6 ms: 1.25x slower                                                 |
| many_optionals                   | 200 us                                                         | 250 us: 1.25x slower                                                  |
| richards                         | 22.1 ms                                                        | 27.6 ms: 1.25x slower                                                 |
| typing_runtime_protocols         | 64.6 us                                                        | 81.4 us: 1.26x slower                                                 |
| sympy_str                        | 95.5 ms                                                        | 120 ms: 1.26x slower                                                  |
| richards_super                   | 24.7 ms                                                        | 31.5 ms: 1.27x slower                                                 |
| unpickle_pure_python             | 99.5 us                                                        | 127 us: 1.28x slower                                                  |
| logging_simple                   | 2.24 us                                                        | 2.86 us: 1.28x slower                                                 |
| sympy_expand                     | 159 ms                                                         | 204 ms: 1.28x slower                                                  |
| pprint_safe_repr                 | 322 ms                                                         | 414 ms: 1.29x slower                                                  |
| logging_format                   | 2.45 us                                                        | 3.15 us: 1.29x slower                                                 |
| async_tree_eager                 | 43.2 ms                                                        | 56.0 ms: 1.30x slower                                                 |
| pprint_pformat                   | 650 ms                                                         | 844 ms: 1.30x slower                                                  |
| pickle_pure_python               | 130 us                                                         | 171 us: 1.31x slower                                                  |
| scimark_fft                      | 124 ms                                                         | 162 ms: 1.31x slower                                                  |
| genshi_text                      | 9.97 ms                                                        | 13.1 ms: 1.32x slower                                                 |
| nqueens                          | 37.2 ms                                                        | 49.3 ms: 1.32x slower                                                 |
| scimark_monte_carlo              | 29.9 ms                                                        | 40.5 ms: 1.35x slower                                                 |
| logging_silent                   | 40.6 ns                                                        | 55.1 ns: 1.36x slower                                                 |
| spectral_norm                    | 43.7 ms                                                        | 59.5 ms: 1.36x slower                                                 |
| crypto_pyaes                     | 33.6 ms                                                        | 45.9 ms: 1.37x slower                                                 |
| deltablue                        | 1.45 ms                                                        | 1.98 ms: 1.37x slower                                                 |
| chaos                            | 24.3 ms                                                        | 33.3 ms: 1.37x slower                                                 |
| hexiom                           | 2.85 ms                                                        | 3.96 ms: 1.39x slower                                                 |
| mako                             | 4.41 ms                                                        | 6.21 ms: 1.41x slower                                                 |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.52 ms: 1.42x slower                                                 |
| generators                       | 15.7 ms                                                        | 22.5 ms: 1.43x slower                                                 |
| django_template                  | 12.5 ms                                                        | 18.3 ms: 1.47x slower                                                 |
| comprehensions                   | 6.80 us                                                        | 10.1 us: 1.48x slower                                                 |
| raytrace                         | 109 ms                                                         | 162 ms: 1.49x slower                                                  |
| subparsers                       | 6.26 ms                                                        | 9.35 ms: 1.49x slower                                                 |
| bench_thread_pool                | 412 us                                                         | 634 us: 1.54x slower                                                  |
| scimark_lu                       | 42.8 ms                                                        | 67.8 ms: 1.58x slower                                                 |
| nbody                            | 42.5 ms                                                        | 77.7 ms: 1.83x slower                                                 |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.5 ms: 3.03x slower                                                 |
| Geometric mean                   | (ref)                                                          | 1.10x slower                                                          |

Benchmark hidden because not significant (1): docutils
Ignored benchmarks (9) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250321-3.14.0a6+-d3f6063-NOGIL/bm-20250321-macm4pro-arm64-Yhg1s-frame_threadsafety-3.14.0a6+-d3f6063.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.087x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.18x