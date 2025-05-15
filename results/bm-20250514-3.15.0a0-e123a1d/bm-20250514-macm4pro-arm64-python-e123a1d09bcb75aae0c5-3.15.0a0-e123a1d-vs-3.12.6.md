# Results vs. 3.12.6

- fork: python
- ref: e123a1d09bcb75aae0c5
- machine: darwin-arm64
- commit hash: e123a1d
- commit date: 2025-05-14
- overall geometric mean: 1.093x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250514-macm4pro-arm64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 114 ms: 1.00x faster                                                    |
| docutils       | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                  |
| html5lib       | 23.0 ms                                                  | 26.4 ms: 1.15x slower                                                   |
| sphinx         | 434 ms                                                   | 417 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                    | 1.03x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250514-macm4pro-arm64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 247 ms: 2.01x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 251 ms: 1.91x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 256 ms: 1.80x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 254 ms: 1.75x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 105 ms: 1.65x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 110 ms: 1.62x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 148 ms: 1.56x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 147 ms: 1.51x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 261 ms: 1.30x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.28x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 265 ms: 1.26x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                    |
| async_generators                 | 206 ms                                                   | 177 ms: 1.17x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 42.5 ms: 1.07x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.03x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 246 ms: 1.16x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.5 ms: 2.72x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.25x faster                                                            |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250514-macm4pro-arm64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 30.1 ms: 1.26x faster                                                   |
| nbody          | 54.2 ms                                                  | 50.4 ms: 1.08x faster                                                   |
| pidigits       | 161 ms                                                   | 165 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.10x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250514-macm4pro-arm64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 49.3 ms: 1.11x faster                                                   |
| regex_effbot   | 1.67 ms                                                  | 1.58 ms: 1.05x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 102 ms: 1.03x slower                                                    |
| regex_v8       | 9.59 ms                                                  | 9.99 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                    | 1.02x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250514-macm4pro-arm64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 45.3 ms: 1.14x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 36.8 ms: 1.06x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 65.6 ms: 1.04x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 101 us: 1.02x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 26.1 ms: 1.02x faster                                                   |
| pickle_pure_python   | 139 us                                                   | 146 us: 1.05x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.7 us: 1.08x slower                                                   |
| json_dumps           | 4.26 ms                                                  | 4.62 ms: 1.08x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.01x faster                                                            |

Benchmark hidden because not significant (1): tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250514-macm4pro-arm64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.55 ms: 1.07x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.13 ms: 1.07x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.07x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250514-macm4pro-arm64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 10.3 ms: 1.02x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 21.9 ms: 1.01x slower                                                   |
| django_template | 13.6 ms                                                  | 15.5 ms: 1.14x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.03x slower                                                            |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250514-macm4pro-arm64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 9.73 ms: 2.13x faster                                                   |
| mdp                              | 1.09 sec                                                 | 531 ms: 2.06x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 247 ms: 2.01x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 251 ms: 1.91x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 256 ms: 1.80x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 254 ms: 1.75x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 105 ms: 1.65x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 110 ms: 1.62x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 148 ms: 1.56x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 147 ms: 1.51x faster                                                    |
| deepcopy                         | 161 us                                                   | 112 us: 1.44x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.9 us: 1.42x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 261 ms: 1.30x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.28x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.16 us: 1.26x faster                                                   |
| float                            | 37.9 ms                                                  | 30.1 ms: 1.26x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 265 ms: 1.26x faster                                                    |
| generators                       | 21.9 ms                                                  | 17.6 ms: 1.25x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.91 us: 1.24x faster                                                   |
| go                               | 70.0 ms                                                  | 57.7 ms: 1.21x faster                                                   |
| raytrace                         | 145 ms                                                   | 120 ms: 1.21x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.1 ms: 1.18x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 52.2 ms: 1.17x faster                                                   |
| async_generators                 | 206 ms                                                   | 177 ms: 1.17x faster                                                    |
| k_core                           | 1.12 sec                                                 | 960 ms: 1.17x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.50 ms: 1.15x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.95 sec: 1.15x faster                                                  |
| xml_etree_iterparse              | 51.6 ms                                                  | 45.3 ms: 1.14x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 48.1 ms: 1.13x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 38.9 ms: 1.12x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 49.3 ms: 1.11x faster                                                   |
| pylint                           | 128 ms                                                   | 116 ms: 1.11x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.3 ms: 1.09x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.5 ms: 1.09x faster                                                   |
| pyflate                          | 216 ms                                                   | 198 ms: 1.09x faster                                                    |
| chaos                            | 28.9 ms                                                  | 26.6 ms: 1.09x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 131 ms: 1.08x faster                                                    |
| nbody                            | 54.2 ms                                                  | 50.4 ms: 1.08x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 66.0 us: 1.08x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.82 ms: 1.08x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 42.5 ms: 1.07x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 48.4 ms: 1.06x faster                                                   |
| thrift                           | 322 us                                                   | 304 us: 1.06x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 36.8 ms: 1.06x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.96 ms: 1.06x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.58 ms: 1.05x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.61 ms: 1.05x faster                                                   |
| sphinx                           | 434 ms                                                   | 417 ms: 1.04x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 37.5 ms: 1.04x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 65.6 ms: 1.04x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.03x faster                                                    |
| sympy_str                        | 104 ms                                                   | 101 ms: 1.03x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 101 us: 1.02x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 26.1 ms: 1.02x faster                                                   |
| genshi_text                      | 10.5 ms                                                  | 10.3 ms: 1.02x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 56.8 ms: 1.01x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 25.0 ms: 1.01x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 954 ns: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 521 ms: 1.01x faster                                                    |
| richards                         | 22.4 ms                                                  | 22.2 ms: 1.01x faster                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 325 ms: 1.01x faster                                                    |
| shortest_path                    | 219 ms                                                   | 217 ms: 1.01x faster                                                    |
| 2to3                             | 114 ms                                                   | 114 ms: 1.00x faster                                                    |
| connected_components             | 201 ms                                                   | 200 ms: 1.00x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.82 us: 1.01x slower                                                   |
| genshi_xml                       | 21.8 ms                                                  | 21.9 ms: 1.01x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 169 ms: 1.01x slower                                                    |
| json                             | 1.93 ms                                                  | 1.95 ms: 1.01x slower                                                   |
| logging_simple                   | 2.57 us                                                  | 2.61 us: 1.01x slower                                                   |
| pidigits                         | 161 ms                                                   | 165 ms: 1.02x slower                                                    |
| regex_dna                        | 99.6 ms                                                  | 102 ms: 1.03x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                  |
| gc_traversal                     | 2.01 ms                                                  | 2.07 ms: 1.03x slower                                                   |
| fannkuch                         | 176 ms                                                   | 182 ms: 1.04x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.99 ms: 1.04x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 438 us: 1.05x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 146 us: 1.05x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 50.5 ms: 1.06x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 8.55 ms: 1.07x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.13 ms: 1.07x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.7 us: 1.08x slower                                                   |
| json_dumps                       | 4.26 ms                                                  | 4.62 ms: 1.08x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 43.7 ms: 1.10x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 929 us: 1.12x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.5 ms: 1.14x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 26.4 ms: 1.15x slower                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 246 ms: 1.16x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.05 ms: 1.17x slower                                                   |
| coverage                         | 26.9 ms                                                  | 32.7 ms: 1.22x slower                                                   |
| many_optionals                   | 195 us                                                   | 246 us: 1.26x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.5 ms: 2.72x slower                                                   |
| logging_silent                   | 50.9 ns                                                  | 197 ns: 3.87x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                            |

Benchmark hidden because not significant (5): tomli_loads, pprint_pformat, pycparser, asyncio_websockets, mako
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250514-3.15.0a0-e123a1d/bm-20250514-macm4pro-arm64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.093x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.13x