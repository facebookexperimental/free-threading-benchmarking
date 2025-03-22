# Results vs. 3.12.6

- fork: Yhg1s
- ref: frame_threadsafety
- machine: darwin-arm64
- commit hash: d3f6063
- commit date: 2025-03-21
- overall geometric mean: 1.016x slower
- HPT reliability: 99.56%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250321-macm4pro-arm64-Yhg1s-frame_threadsafety-3.14.0a6+-d3f6063 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 130 ms: 1.14x slower                                                  |
| docutils       | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                |
| html5lib       | 23.0 ms                                                  | 25.3 ms: 1.10x slower                                                 |
| sphinx         | 434 ms                                                   | 442 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                    | 1.07x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250321-macm4pro-arm64-Yhg1s-frame_threadsafety-3.14.0a6+-d3f6063 |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 223 ms: 2.15x faster                                                  |
| async_tree_eager_io              | 496 ms                                                   | 232 ms: 2.14x faster                                                  |
| async_tree_eager_io_tg           | 446 ms                                                   | 222 ms: 2.01x faster                                                  |
| async_tree_io                    | 459 ms                                                   | 239 ms: 1.92x faster                                                  |
| async_tree_none_tg               | 172 ms                                                   | 99.2 ms: 1.74x faster                                                 |
| async_tree_memoization_tg        | 231 ms                                                   | 136 ms: 1.69x faster                                                  |
| async_tree_none                  | 178 ms                                                   | 115 ms: 1.55x faster                                                  |
| async_tree_memoization           | 223 ms                                                   | 145 ms: 1.53x faster                                                  |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 242 ms: 1.40x faster                                                  |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 252 ms: 1.32x faster                                                  |
| coroutines                       | 13.6 ms                                                  | 12.2 ms: 1.11x faster                                                 |
| async_tree_eager_memoization     | 132 ms                                                   | 120 ms: 1.10x faster                                                  |
| async_generators                 | 206 ms                                                   | 191 ms: 1.08x faster                                                  |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 227 ms: 1.01x faster                                                  |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                  |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 231 ms: 1.09x slower                                                  |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 123 ms: 1.09x slower                                                  |
| async_tree_eager                 | 45.6 ms                                                  | 56.0 ms: 1.23x slower                                                 |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.5 ms: 2.72x slower                                                 |
| Geometric mean                   | (ref)                                                    | 1.26x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250321-macm4pro-arm64-Yhg1s-frame_threadsafety-3.14.0a6+-d3f6063 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 35.8 ms: 1.06x faster                                                 |
| pidigits       | 161 ms                                                   | 161 ms: 1.00x faster                                                  |
| nbody          | 54.2 ms                                                  | 77.7 ms: 1.43x slower                                                 |
| Geometric mean | (ref)                                                    | 1.10x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250321-macm4pro-arm64-Yhg1s-frame_threadsafety-3.14.0a6+-d3f6063 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.47 ms: 1.14x faster                                                 |
| regex_dna      | 99.6 ms                                                  | 98.5 ms: 1.01x faster                                                 |
| regex_compile  | 54.6 ms                                                  | 59.4 ms: 1.09x slower                                                 |
| Geometric mean | (ref)                                                    | 1.01x faster                                                          |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250321-macm4pro-arm64-Yhg1s-frame_threadsafety-3.14.0a6+-d3f6063 |
|----------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.2 ms: 1.28x faster                                                 |
| xml_etree_parse      | 67.9 ms                                                  | 56.2 ms: 1.21x faster                                                 |
| xml_etree_generate   | 38.9 ms                                                  | 41.1 ms: 1.06x slower                                                 |
| json_loads           | 10.9 us                                                  | 11.8 us: 1.09x slower                                                 |
| tomli_loads          | 957 ms                                                   | 1.08 sec: 1.12x slower                                                |
| xml_etree_process    | 26.7 ms                                                  | 30.7 ms: 1.15x slower                                                 |
| json_dumps           | 4.26 ms                                                  | 5.19 ms: 1.22x slower                                                 |
| pickle_pure_python   | 139 us                                                   | 171 us: 1.23x slower                                                  |
| unpickle_pure_python | 103 us                                                   | 127 us: 1.24x slower                                                  |
| Geometric mean       | (ref)                                                    | 1.07x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250321-macm4pro-arm64-Yhg1s-frame_threadsafety-3.14.0a6+-d3f6063 |
|------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.23 ms: 1.15x slower                                                 |
| python_startup_no_site | 5.71 ms                                                  | 7.28 ms: 1.28x slower                                                 |
| Geometric mean         | (ref)                                                    | 1.21x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250321-macm4pro-arm64-Yhg1s-frame_threadsafety-3.14.0a6+-d3f6063 |
|-----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 26.3 ms: 1.21x slower                                                 |
| genshi_text     | 10.5 ms                                                  | 13.1 ms: 1.25x slower                                                 |
| mako            | 4.77 ms                                                  | 6.21 ms: 1.30x slower                                                 |
| django_template | 13.6 ms                                                  | 18.3 ms: 1.35x slower                                                 |
| Geometric mean  | (ref)                                                    | 1.28x slower                                                          |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250321-macm4pro-arm64-Yhg1s-frame_threadsafety-3.14.0a6+-d3f6063 |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 9.35 ms: 2.22x faster                                                 |
| gc_traversal                     | 2.01 ms                                                  | 935 us: 2.15x faster                                                  |
| async_tree_io_tg                 | 480 ms                                                   | 223 ms: 2.15x faster                                                  |
| async_tree_eager_io              | 496 ms                                                   | 232 ms: 2.14x faster                                                  |
| async_tree_eager_io_tg           | 446 ms                                                   | 222 ms: 2.01x faster                                                  |
| async_tree_io                    | 459 ms                                                   | 239 ms: 1.92x faster                                                  |
| async_tree_none_tg               | 172 ms                                                   | 99.2 ms: 1.74x faster                                                 |
| async_tree_memoization_tg        | 231 ms                                                   | 136 ms: 1.69x faster                                                  |
| create_gc_cycles                 | 830 us                                                   | 510 us: 1.63x faster                                                  |
| async_tree_none                  | 178 ms                                                   | 115 ms: 1.55x faster                                                  |
| async_tree_memoization           | 223 ms                                                   | 145 ms: 1.53x faster                                                  |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 242 ms: 1.40x faster                                                  |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 252 ms: 1.32x faster                                                  |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.2 ms: 1.28x faster                                                 |
| deepcopy                         | 161 us                                                   | 128 us: 1.26x faster                                                  |
| xml_etree_parse                  | 67.9 ms                                                  | 56.2 ms: 1.21x faster                                                 |
| sqlite_synth                     | 967 ns                                                   | 840 ns: 1.15x faster                                                  |
| regex_effbot                     | 1.67 ms                                                  | 1.47 ms: 1.14x faster                                                 |
| coroutines                       | 13.6 ms                                                  | 12.2 ms: 1.11x faster                                                 |
| async_tree_eager_memoization     | 132 ms                                                   | 120 ms: 1.10x faster                                                  |
| dulwich_log                      | 21.3 ms                                                  | 19.6 ms: 1.09x faster                                                 |
| async_generators                 | 206 ms                                                   | 191 ms: 1.08x faster                                                  |
| deepcopy_memo                    | 18.3 us                                                  | 17.1 us: 1.07x faster                                                 |
| float                            | 37.9 ms                                                  | 35.8 ms: 1.06x faster                                                 |
| deepcopy_reduce                  | 1.46 us                                                  | 1.38 us: 1.06x faster                                                 |
| k_core                           | 1.12 sec                                                 | 1.06 sec: 1.05x faster                                                |
| pathlib                          | 12.4 ms                                                  | 11.8 ms: 1.05x faster                                                 |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 227 ms: 1.01x faster                                                  |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                  |
| regex_dna                        | 99.6 ms                                                  | 98.5 ms: 1.01x faster                                                 |
| pidigits                         | 161 ms                                                   | 161 ms: 1.00x faster                                                  |
| bench_mp_pool                    | 39.7 ms                                                  | 39.9 ms: 1.01x slower                                                 |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.25 sec: 1.01x slower                                                |
| sphinx                           | 434 ms                                                   | 442 ms: 1.02x slower                                                  |
| pycparser                        | 497 ms                                                   | 508 ms: 1.02x slower                                                  |
| docutils                         | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                |
| generators                       | 21.9 ms                                                  | 22.5 ms: 1.02x slower                                                 |
| comprehensions                   | 9.84 us                                                  | 10.1 us: 1.03x slower                                                 |
| json                             | 1.93 ms                                                  | 1.99 ms: 1.03x slower                                                 |
| xml_etree_generate               | 38.9 ms                                                  | 41.1 ms: 1.06x slower                                                 |
| go                               | 70.0 ms                                                  | 74.1 ms: 1.06x slower                                                 |
| pyflate                          | 216 ms                                                   | 232 ms: 1.07x slower                                                  |
| logging_silent                   | 50.9 ns                                                  | 55.1 ns: 1.08x slower                                                 |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 231 ms: 1.09x slower                                                  |
| json_loads                       | 10.9 us                                                  | 11.8 us: 1.09x slower                                                 |
| thrift                           | 322 us                                                   | 350 us: 1.09x slower                                                  |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 123 ms: 1.09x slower                                                  |
| regex_compile                    | 54.6 ms                                                  | 59.4 ms: 1.09x slower                                                 |
| spectral_norm                    | 54.4 ms                                                  | 59.5 ms: 1.09x slower                                                 |
| mdp                              | 1.09 sec                                                 | 1.19 sec: 1.09x slower                                                |
| html5lib                         | 23.0 ms                                                  | 25.3 ms: 1.10x slower                                                 |
| sqlalchemy_declarative           | 46.8 ms                                                  | 51.5 ms: 1.10x slower                                                 |
| sympy_sum                        | 57.6 ms                                                  | 64.0 ms: 1.11x slower                                                 |
| logging_simple                   | 2.57 us                                                  | 2.86 us: 1.11x slower                                                 |
| raytrace                         | 145 ms                                                   | 162 ms: 1.12x slower                                                  |
| logging_format                   | 2.80 us                                                  | 3.15 us: 1.12x slower                                                 |
| tomli_loads                      | 957 ms                                                   | 1.08 sec: 1.12x slower                                                |
| nqueens                          | 43.5 ms                                                  | 49.3 ms: 1.13x slower                                                 |
| shortest_path                    | 219 ms                                                   | 248 ms: 1.13x slower                                                  |
| sympy_integrate                  | 8.02 ms                                                  | 9.13 ms: 1.14x slower                                                 |
| 2to3                             | 114 ms                                                   | 130 ms: 1.14x slower                                                  |
| scimark_fft                      | 142 ms                                                   | 162 ms: 1.14x slower                                                  |
| typing_runtime_protocols         | 71.0 us                                                  | 81.4 us: 1.15x slower                                                 |
| xml_etree_process                | 26.7 ms                                                  | 30.7 ms: 1.15x slower                                                 |
| scimark_sor                      | 61.0 ms                                                  | 70.1 ms: 1.15x slower                                                 |
| sqlalchemy_imperative            | 5.17 ms                                                  | 5.95 ms: 1.15x slower                                                 |
| chaos                            | 28.9 ms                                                  | 33.3 ms: 1.15x slower                                                 |
| deltablue                        | 1.73 ms                                                  | 1.98 ms: 1.15x slower                                                 |
| python_startup                   | 8.01 ms                                                  | 9.23 ms: 1.15x slower                                                 |
| sympy_str                        | 104 ms                                                   | 120 ms: 1.16x slower                                                  |
| connected_components             | 201 ms                                                   | 236 ms: 1.17x slower                                                  |
| crypto_pyaes                     | 38.8 ms                                                  | 45.9 ms: 1.18x slower                                                 |
| genshi_xml                       | 21.8 ms                                                  | 26.3 ms: 1.21x slower                                                 |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.52 ms: 1.21x slower                                                 |
| json_dumps                       | 4.26 ms                                                  | 5.19 ms: 1.22x slower                                                 |
| sympy_expand                     | 167 ms                                                   | 204 ms: 1.22x slower                                                  |
| pickle_pure_python               | 139 us                                                   | 171 us: 1.23x slower                                                  |
| richards                         | 22.4 ms                                                  | 27.6 ms: 1.23x slower                                                 |
| async_tree_eager                 | 45.6 ms                                                  | 56.0 ms: 1.23x slower                                                 |
| unpickle_pure_python             | 103 us                                                   | 127 us: 1.24x slower                                                  |
| richards_super                   | 25.4 ms                                                  | 31.5 ms: 1.24x slower                                                 |
| meteor_contest                   | 47.7 ms                                                  | 59.6 ms: 1.25x slower                                                 |
| genshi_text                      | 10.5 ms                                                  | 13.1 ms: 1.25x slower                                                 |
| scimark_monte_carlo              | 32.2 ms                                                  | 40.5 ms: 1.26x slower                                                 |
| fannkuch                         | 176 ms                                                   | 221 ms: 1.26x slower                                                  |
| pprint_safe_repr                 | 328 ms                                                   | 414 ms: 1.26x slower                                                  |
| pprint_pformat                   | 665 ms                                                   | 844 ms: 1.27x slower                                                  |
| python_startup_no_site           | 5.71 ms                                                  | 7.28 ms: 1.28x slower                                                 |
| many_optionals                   | 195 us                                                   | 250 us: 1.28x slower                                                  |
| mako                             | 4.77 ms                                                  | 6.21 ms: 1.30x slower                                                 |
| hexiom                           | 3.04 ms                                                  | 3.96 ms: 1.30x slower                                                 |
| scimark_lu                       | 51.3 ms                                                  | 67.8 ms: 1.32x slower                                                 |
| django_template                  | 13.6 ms                                                  | 18.3 ms: 1.35x slower                                                 |
| telco                            | 2.61 ms                                                  | 3.60 ms: 1.38x slower                                                 |
| coverage                         | 26.9 ms                                                  | 38.2 ms: 1.42x slower                                                 |
| nbody                            | 54.2 ms                                                  | 77.7 ms: 1.43x slower                                                 |
| bench_thread_pool                | 419 us                                                   | 634 us: 1.51x slower                                                  |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.5 ms: 2.72x slower                                                 |
| Geometric mean                   | (ref)                                                    | 1.02x slower                                                          |

Benchmark hidden because not significant (2): pylint, regex_v8
Ignored benchmarks (9) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250321-3.14.0a6+-d3f6063-NOGIL/bm-20250321-macm4pro-arm64-Yhg1s-frame_threadsafety-3.14.0a6+-d3f6063.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.016x slower

# HPT report

- Reliability score: 99.56% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.22x