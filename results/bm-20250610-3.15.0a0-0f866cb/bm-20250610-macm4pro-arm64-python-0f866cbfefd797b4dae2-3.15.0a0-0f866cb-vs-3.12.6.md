# Results vs. 3.12.6

- fork: python
- ref: 0f866cbfefd797b4dae2
- machine: darwin-arm64
- commit hash: 0f866cb
- commit date: 2025-06-10
- overall geometric mean: 1.120x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250610-macm4pro-arm64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 113 ms: 1.01x faster                                                    |
| docutils       | 1.02 sec                                                 | 1.04 sec: 1.01x slower                                                  |
| html5lib       | 23.0 ms                                                  | 23.5 ms: 1.02x slower                                                   |
| sphinx         | 434 ms                                                   | 403 ms: 1.08x faster                                                    |
| Geometric mean | (ref)                                                    | 1.01x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250610-macm4pro-arm64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 245 ms: 2.02x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 248 ms: 1.93x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 252 ms: 1.82x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 253 ms: 1.76x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 105 ms: 1.63x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 113 ms: 1.58x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 146 ms: 1.57x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 146 ms: 1.53x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 263 ms: 1.29x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 265 ms: 1.26x faster                                                    |
| async_generators                 | 206 ms                                                   | 171 ms: 1.21x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.19x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 42.0 ms: 1.08x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.03x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 249 ms: 1.17x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 86.9 ms: 2.71x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.25x faster                                                            |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250610-macm4pro-arm64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.7 ms: 1.27x faster                                                   |
| nbody          | 54.2 ms                                                  | 47.6 ms: 1.14x faster                                                   |
| pidigits       | 161 ms                                                   | 162 ms: 1.00x slower                                                    |
| Geometric mean | (ref)                                                    | 1.13x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250610-macm4pro-arm64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 47.2 ms: 1.16x faster                                                   |
| regex_effbot   | 1.67 ms                                                  | 1.47 ms: 1.13x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 95.6 ms: 1.04x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.72 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                    | 1.08x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250610-macm4pro-arm64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 44.7 ms: 1.15x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 34.7 ms: 1.12x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 24.6 ms: 1.08x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 95.3 us: 1.08x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 63.7 ms: 1.07x faster                                                   |
| tomli_loads          | 957 ms                                                   | 901 ms: 1.06x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.7 us: 1.02x faster                                                   |
| pickle_pure_python   | 139 us                                                   | 143 us: 1.03x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 4.41 ms: 1.04x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250610-macm4pro-arm64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.53 ms: 1.06x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.11 ms: 1.07x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.07x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250610-macm4pro-arm64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.76 ms: 1.07x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 21.1 ms: 1.03x faster                                                   |
| django_template | 13.6 ms                                                  | 15.2 ms: 1.12x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.00x slower                                                            |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250610-macm4pro-arm64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 9.64 ms: 2.15x faster                                                   |
| mdp                              | 1.09 sec                                                 | 507 ms: 2.15x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 245 ms: 2.02x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 248 ms: 1.93x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 252 ms: 1.82x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 253 ms: 1.76x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 105 ms: 1.63x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 113 ms: 1.58x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 146 ms: 1.57x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 146 ms: 1.53x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.1 us: 1.51x faster                                                   |
| deepcopy                         | 161 us                                                   | 108 us: 1.50x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.26 us: 1.36x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 263 ms: 1.29x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.14 us: 1.28x faster                                                   |
| go                               | 70.0 ms                                                  | 54.9 ms: 1.27x faster                                                   |
| float                            | 37.9 ms                                                  | 29.7 ms: 1.27x faster                                                   |
| generators                       | 21.9 ms                                                  | 17.3 ms: 1.27x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 265 ms: 1.26x faster                                                    |
| raytrace                         | 145 ms                                                   | 117 ms: 1.24x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 50.3 ms: 1.21x faster                                                   |
| async_generators                 | 206 ms                                                   | 171 ms: 1.21x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 17.7 ms: 1.20x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.19x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 46.0 ms: 1.18x faster                                                   |
| k_core                           | 1.12 sec                                                 | 948 ms: 1.18x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 61.3 us: 1.16x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 47.2 ms: 1.16x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 44.7 ms: 1.15x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.50 ms: 1.15x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 37.8 ms: 1.15x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.95 sec: 1.15x faster                                                  |
| pylint                           | 128 ms                                                   | 112 ms: 1.14x faster                                                    |
| nbody                            | 54.2 ms                                                  | 47.6 ms: 1.14x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.83 ms: 1.14x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 28.5 ms: 1.13x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.47 ms: 1.13x faster                                                   |
| pyflate                          | 216 ms                                                   | 192 ms: 1.13x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.71 ms: 1.12x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 11.0 ms: 1.12x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 34.7 ms: 1.12x faster                                                   |
| chaos                            | 28.9 ms                                                  | 25.8 ms: 1.12x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 128 ms: 1.11x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.34 ms: 1.09x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 24.6 ms: 1.08x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 42.0 ms: 1.08x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 95.3 us: 1.08x faster                                                   |
| sphinx                           | 434 ms                                                   | 403 ms: 1.08x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.76 ms: 1.07x faster                                                   |
| thrift                           | 322 us                                                   | 301 us: 1.07x faster                                                    |
| sympy_str                        | 104 ms                                                   | 97.6 ms: 1.07x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 48.1 ms: 1.07x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 63.7 ms: 1.07x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 901 ms: 1.06x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 23.9 ms: 1.06x faster                                                   |
| richards                         | 22.4 ms                                                  | 21.2 ms: 1.06x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 55.1 ms: 1.05x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 95.6 ms: 1.04x faster                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 37.4 ms: 1.04x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.71 us: 1.03x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.03x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 21.1 ms: 1.03x faster                                                   |
| json                             | 1.93 ms                                                  | 1.88 ms: 1.03x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.50 us: 1.03x faster                                                   |
| pycparser                        | 497 ms                                                   | 486 ms: 1.02x faster                                                    |
| json_loads                       | 10.9 us                                                  | 10.7 us: 1.02x faster                                                   |
| meteor_contest                   | 47.7 ms                                                  | 47.0 ms: 1.02x faster                                                   |
| 2to3                             | 114 ms                                                   | 113 ms: 1.01x faster                                                    |
| sympy_expand                     | 167 ms                                                   | 165 ms: 1.01x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 957 ns: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                    |
| shortest_path                    | 219 ms                                                   | 218 ms: 1.00x faster                                                    |
| pidigits                         | 161 ms                                                   | 162 ms: 1.00x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.72 ms: 1.01x slower                                                   |
| docutils                         | 1.02 sec                                                 | 1.04 sec: 1.01x slower                                                  |
| html5lib                         | 23.0 ms                                                  | 23.5 ms: 1.02x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 143 us: 1.03x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 431 us: 1.03x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 4.41 ms: 1.04x slower                                                   |
| gc_traversal                     | 2.01 ms                                                  | 2.11 ms: 1.05x slower                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 347 ms: 1.06x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.53 ms: 1.06x slower                                                   |
| pprint_pformat                   | 665 ms                                                   | 711 ms: 1.07x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.11 ms: 1.07x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 43.8 ms: 1.10x slower                                                   |
| django_template                  | 13.6 ms                                                  | 15.2 ms: 1.12x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 927 us: 1.12x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.98 ms: 1.14x slower                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 249 ms: 1.17x slower                                                    |
| coverage                         | 26.9 ms                                                  | 33.0 ms: 1.23x slower                                                   |
| many_optionals                   | 195 us                                                   | 245 us: 1.26x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 86.9 ms: 2.71x slower                                                   |
| logging_silent                   | 50.9 ns                                                  | 195 ns: 3.83x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                            |

Benchmark hidden because not significant (4): fannkuch, mako, connected_components, asyncio_websockets
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250610-3.15.0a0-0f866cb/bm-20250610-macm4pro-arm64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.120x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.15x