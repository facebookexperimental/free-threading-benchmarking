# Results vs. 3.12.6

- fork: python
- ref: 9c1e85fd64cf6a85f7c9
- machine: darwin-arm64
- commit hash: 9c1e85f
- commit date: 2025-03-29
- overall geometric mean: 1.082x faster
- HPT reliability: 97.03%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250329-macm4pro-arm64-python-9c1e85fd64cf6a85f7c9-3.14.0a6+-9c1e85f |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 121 ms: 1.06x slower                                                     |
| docutils       | 1.02 sec                                                 | 997 ms: 1.02x faster                                                     |
| html5lib       | 23.0 ms                                                  | 21.9 ms: 1.05x faster                                                    |
| sphinx         | 434 ms                                                   | 416 ms: 1.04x faster                                                     |
| Geometric mean | (ref)                                                    | 1.02x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250329-macm4pro-arm64-python-9c1e85fd64cf6a85f7c9-3.14.0a6+-9c1e85f |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 213 ms: 2.32x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 207 ms: 2.32x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 203 ms: 2.19x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 220 ms: 2.09x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 90.9 ms: 1.90x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 127 ms: 1.81x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 105 ms: 1.70x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 135 ms: 1.65x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 236 ms: 1.43x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 245 ms: 1.36x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.0 ms: 1.36x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.17x faster                                                     |
| async_generators                 | 206 ms                                                   | 189 ms: 1.09x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 115 ms: 1.02x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 226 ms: 1.06x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 49.5 ms: 1.09x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 81.0 ms: 2.52x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.35x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250329-macm4pro-arm64-python-9c1e85fd64cf6a85f7c9-3.14.0a6+-9c1e85f |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 30.7 ms: 1.23x faster                                                    |
| pidigits       | 161 ms                                                   | 158 ms: 1.02x faster                                                     |
| nbody          | 54.2 ms                                                  | 66.1 ms: 1.22x slower                                                    |
| Geometric mean | (ref)                                                    | 1.01x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250329-macm4pro-arm64-python-9c1e85fd64cf6a85f7c9-3.14.0a6+-9c1e85f |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.40 ms: 1.19x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 91.9 ms: 1.08x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 52.9 ms: 1.03x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.42 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250329-macm4pro-arm64-python-9c1e85fd64cf6a85f7c9-3.14.0a6+-9c1e85f |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 37.0 ms: 1.39x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 54.7 ms: 1.24x faster                                                    |
| tomli_loads          | 957 ms                                                   | 913 ms: 1.05x faster                                                     |
| xml_etree_generate   | 38.9 ms                                                  | 37.8 ms: 1.03x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 27.5 ms: 1.03x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.6 us: 1.07x slower                                                    |
| unpickle_pure_python | 103 us                                                   | 111 us: 1.08x slower                                                     |
| pickle_pure_python   | 139 us                                                   | 152 us: 1.09x slower                                                     |
| json_dumps           | 4.26 ms                                                  | 5.00 ms: 1.17x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.02x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250329-macm4pro-arm64-python-9c1e85fd64cf6a85f7c9-3.14.0a6+-9c1e85f |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.16 ms: 1.14x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.23 ms: 1.27x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.20x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250329-macm4pro-arm64-python-9c1e85fd64cf6a85f7c9-3.14.0a6+-9c1e85f |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 22.9 ms: 1.05x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 11.5 ms: 1.10x slower                                                    |
| mako            | 4.77 ms                                                  | 5.63 ms: 1.18x slower                                                    |
| django_template | 13.6 ms                                                  | 16.2 ms: 1.19x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.13x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250329-macm4pro-arm64-python-9c1e85fd64cf6a85f7c9-3.14.0a6+-9c1e85f |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 8.69 ms: 2.39x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 213 ms: 2.32x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 207 ms: 2.32x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 203 ms: 2.19x faster                                                     |
| gc_traversal                     | 2.01 ms                                                  | 930 us: 2.16x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 220 ms: 2.09x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 90.9 ms: 1.90x faster                                                    |
| mdp                              | 1.09 sec                                                 | 600 ms: 1.82x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 127 ms: 1.81x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 105 ms: 1.70x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 135 ms: 1.65x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 508 us: 1.63x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 236 ms: 1.43x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 37.0 ms: 1.39x faster                                                    |
| deepcopy                         | 161 us                                                   | 117 us: 1.38x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 245 ms: 1.36x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.0 ms: 1.36x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 54.7 ms: 1.24x faster                                                    |
| float                            | 37.9 ms                                                  | 30.7 ms: 1.23x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.3 ms: 1.20x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 15.3 us: 1.19x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.40 ms: 1.19x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 822 ns: 1.18x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.17x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 18.4 ms: 1.16x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.27 us: 1.15x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.61 us: 1.14x faster                                                    |
| go                               | 70.0 ms                                                  | 63.3 ms: 1.11x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.04 sec: 1.10x faster                                                   |
| pylint                           | 128 ms                                                   | 117 ms: 1.09x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 11.3 ms: 1.09x faster                                                    |
| async_generators                 | 206 ms                                                   | 189 ms: 1.09x faster                                                     |
| k_core                           | 1.12 sec                                                 | 1.03 sec: 1.09x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 91.9 ms: 1.08x faster                                                    |
| pycparser                        | 497 ms                                                   | 460 ms: 1.08x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 47.7 ns: 1.07x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 21.9 ms: 1.05x faster                                                    |
| pyflate                          | 216 ms                                                   | 206 ms: 1.05x faster                                                     |
| tomli_loads                      | 957 ms                                                   | 913 ms: 1.05x faster                                                     |
| sphinx                           | 434 ms                                                   | 416 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                     |
| raytrace                         | 145 ms                                                   | 140 ms: 1.03x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 52.9 ms: 1.03x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.8 ms: 1.03x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 59.3 ms: 1.03x faster                                                    |
| docutils                         | 1.02 sec                                                 | 997 ms: 1.02x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 53.1 ms: 1.02x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.42 ms: 1.02x faster                                                    |
| pidigits                         | 161 ms                                                   | 158 ms: 1.02x faster                                                     |
| logging_simple                   | 2.57 us                                                  | 2.54 us: 1.01x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 42.9 ms: 1.01x faster                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 39.2 ms: 1.01x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.71 ms: 1.01x faster                                                    |
| json                             | 1.93 ms                                                  | 1.95 ms: 1.01x slower                                                    |
| sqlalchemy_declarative           | 46.8 ms                                                  | 47.9 ms: 1.02x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 115 ms: 1.02x slower                                                     |
| xml_etree_process                | 26.7 ms                                                  | 27.5 ms: 1.03x slower                                                    |
| scimark_fft                      | 142 ms                                                   | 147 ms: 1.04x slower                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 8.34 ms: 1.04x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 59.9 ms: 1.04x slower                                                    |
| chaos                            | 28.9 ms                                                  | 30.1 ms: 1.04x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 74.0 us: 1.04x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.18 ms: 1.05x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 22.9 ms: 1.05x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.21 ms: 1.06x slower                                                    |
| 2to3                             | 114 ms                                                   | 121 ms: 1.06x slower                                                     |
| sqlalchemy_imperative            | 5.17 ms                                                  | 5.48 ms: 1.06x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 226 ms: 1.06x slower                                                     |
| richards                         | 22.4 ms                                                  | 24.0 ms: 1.07x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.6 us: 1.07x slower                                                    |
| sympy_str                        | 104 ms                                                   | 112 ms: 1.07x slower                                                     |
| shortest_path                    | 219 ms                                                   | 235 ms: 1.07x slower                                                     |
| richards_super                   | 25.4 ms                                                  | 27.3 ms: 1.07x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 111 us: 1.08x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 49.5 ms: 1.09x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 152 us: 1.09x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 42.7 ms: 1.10x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 35.4 ms: 1.10x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.5 ms: 1.10x slower                                                    |
| connected_components             | 201 ms                                                   | 221 ms: 1.10x slower                                                     |
| scimark_lu                       | 51.3 ms                                                  | 56.6 ms: 1.10x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 365 ms: 1.11x slower                                                     |
| pprint_pformat                   | 665 ms                                                   | 743 ms: 1.12x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 190 ms: 1.14x slower                                                     |
| fannkuch                         | 176 ms                                                   | 200 ms: 1.14x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 9.16 ms: 1.14x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 55.0 ms: 1.15x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 5.00 ms: 1.17x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.63 ms: 1.18x slower                                                    |
| django_template                  | 13.6 ms                                                  | 16.2 ms: 1.19x slower                                                    |
| many_optionals                   | 195 us                                                   | 238 us: 1.22x slower                                                     |
| nbody                            | 54.2 ms                                                  | 66.1 ms: 1.22x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.23 ms: 1.27x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.37 ms: 1.29x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 578 us: 1.38x slower                                                     |
| coverage                         | 26.9 ms                                                  | 39.3 ms: 1.46x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 81.0 ms: 2.52x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                             |

Benchmark hidden because not significant (1): logging_format
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250329-3.14.0a6+-9c1e85f-NOGIL/bm-20250329-macm4pro-arm64-python-9c1e85fd64cf6a85f7c9-3.14.0a6+-9c1e85f.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.082x faster

# HPT report

- Reliability score: 97.03% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.22x