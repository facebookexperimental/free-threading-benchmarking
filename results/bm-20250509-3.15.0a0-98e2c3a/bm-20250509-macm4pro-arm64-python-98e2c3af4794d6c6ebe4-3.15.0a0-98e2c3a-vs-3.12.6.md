# Results vs. 3.12.6

- fork: python
- ref: 98e2c3af4794d6c6ebe4
- machine: darwin-arm64
- commit hash: 98e2c3a
- commit date: 2025-05-09
- overall geometric mean: 1.086x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250509-macm4pro-arm64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 116 ms: 1.02x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.06 sec: 1.03x slower                                                  |
| html5lib       | 23.0 ms                                                  | 26.4 ms: 1.15x slower                                                   |
| sphinx         | 434 ms                                                   | 416 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                    | 1.04x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250509-macm4pro-arm64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 255 ms: 1.95x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 256 ms: 1.87x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 259 ms: 1.77x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 260 ms: 1.72x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.62x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 115 ms: 1.55x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 149 ms: 1.54x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 149 ms: 1.50x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 266 ms: 1.27x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.26x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 270 ms: 1.23x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.18x faster                                                    |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 43.1 ms: 1.06x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 132 ms: 1.17x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 249 ms: 1.17x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 88.7 ms: 2.76x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.23x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250509-macm4pro-arm64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 30.5 ms: 1.24x faster                                                   |
| nbody          | 54.2 ms                                                  | 51.4 ms: 1.06x faster                                                   |
| pidigits       | 161 ms                                                   | 163 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                    | 1.09x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250509-macm4pro-arm64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 49.2 ms: 1.11x faster                                                   |
| regex_effbot   | 1.67 ms                                                  | 1.58 ms: 1.06x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 102 ms: 1.02x slower                                                    |
| regex_v8       | 9.59 ms                                                  | 9.90 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                    | 1.03x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250509-macm4pro-arm64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a |
|---------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse | 51.6 ms                                                  | 44.5 ms: 1.16x faster                                                   |
| xml_etree_parse     | 67.9 ms                                                  | 63.3 ms: 1.07x faster                                                   |
| xml_etree_generate  | 38.9 ms                                                  | 36.4 ms: 1.07x faster                                                   |
| xml_etree_process   | 26.7 ms                                                  | 25.9 ms: 1.03x faster                                                   |
| pickle_pure_python  | 139 us                                                   | 148 us: 1.06x slower                                                    |
| json_loads          | 10.9 us                                                  | 11.7 us: 1.08x slower                                                   |
| json_dumps          | 4.26 ms                                                  | 5.18 ms: 1.22x slower                                                   |
| Geometric mean      | (ref)                                                    | 1.00x slower                                                            |

Benchmark hidden because not significant (2): tomli_loads, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250509-macm4pro-arm64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.51 ms: 1.06x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.09 ms: 1.07x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.06x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250509-macm4pro-arm64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 10.3 ms: 1.01x faster                                                   |
| mako            | 4.77 ms                                                  | 4.82 ms: 1.01x slower                                                   |
| genshi_xml      | 21.8 ms                                                  | 22.0 ms: 1.01x slower                                                   |
| django_template | 13.6 ms                                                  | 15.6 ms: 1.15x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.04x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250509-macm4pro-arm64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 9.65 ms: 2.15x faster                                                   |
| mdp                              | 1.09 sec                                                 | 537 ms: 2.03x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 255 ms: 1.95x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 256 ms: 1.87x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 259 ms: 1.77x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 260 ms: 1.72x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.62x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 115 ms: 1.55x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 149 ms: 1.54x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 149 ms: 1.50x faster                                                    |
| deepcopy                         | 161 us                                                   | 110 us: 1.46x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.7 us: 1.44x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.14 us: 1.28x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 266 ms: 1.27x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.26x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.88 us: 1.25x faster                                                   |
| float                            | 37.9 ms                                                  | 30.5 ms: 1.24x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 270 ms: 1.23x faster                                                    |
| generators                       | 21.9 ms                                                  | 17.9 ms: 1.23x faster                                                   |
| go                               | 70.0 ms                                                  | 57.4 ms: 1.22x faster                                                   |
| raytrace                         | 145 ms                                                   | 120 ms: 1.21x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.0 ms: 1.18x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.18x faster                                                    |
| k_core                           | 1.12 sec                                                 | 959 ms: 1.17x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 52.4 ms: 1.16x faster                                                   |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 44.5 ms: 1.16x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 47.4 ms: 1.15x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.51 ms: 1.14x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.99 sec: 1.13x faster                                                  |
| nqueens                          | 43.5 ms                                                  | 39.1 ms: 1.11x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 49.2 ms: 1.11x faster                                                   |
| pylint                           | 128 ms                                                   | 116 ms: 1.11x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.2 ms: 1.10x faster                                                   |
| pyflate                          | 216 ms                                                   | 198 ms: 1.09x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 63.3 ms: 1.07x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.84 ms: 1.07x faster                                                   |
| chaos                            | 28.9 ms                                                  | 27.0 ms: 1.07x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 36.4 ms: 1.07x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 30.2 ms: 1.07x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.55 ms: 1.06x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 134 ms: 1.06x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 43.1 ms: 1.06x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.58 ms: 1.06x faster                                                   |
| thrift                           | 322 us                                                   | 305 us: 1.06x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 67.2 us: 1.06x faster                                                   |
| nbody                            | 54.2 ms                                                  | 51.4 ms: 1.06x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 48.9 ms: 1.05x faster                                                   |
| sphinx                           | 434 ms                                                   | 416 ms: 1.04x faster                                                    |
| sympy_str                        | 104 ms                                                   | 100 ms: 1.04x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 25.9 ms: 1.03x faster                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 38.0 ms: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.04 ms: 1.02x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 56.5 ms: 1.02x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 948 ns: 1.02x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 25.0 ms: 1.02x faster                                                   |
| genshi_text                      | 10.5 ms                                                  | 10.3 ms: 1.01x faster                                                   |
| richards                         | 22.4 ms                                                  | 22.1 ms: 1.01x faster                                                   |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 659 ms: 1.01x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 325 ms: 1.01x faster                                                    |
| connected_components             | 201 ms                                                   | 200 ms: 1.01x faster                                                    |
| shortest_path                    | 219 ms                                                   | 218 ms: 1.01x faster                                                    |
| sympy_expand                     | 167 ms                                                   | 168 ms: 1.00x slower                                                    |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                    |
| mako                             | 4.77 ms                                                  | 4.82 ms: 1.01x slower                                                   |
| genshi_xml                       | 21.8 ms                                                  | 22.0 ms: 1.01x slower                                                   |
| pidigits                         | 161 ms                                                   | 163 ms: 1.01x slower                                                    |
| 2to3                             | 114 ms                                                   | 116 ms: 1.02x slower                                                    |
| json                             | 1.93 ms                                                  | 1.97 ms: 1.02x slower                                                   |
| logging_simple                   | 2.57 us                                                  | 2.62 us: 1.02x slower                                                   |
| logging_format                   | 2.80 us                                                  | 2.86 us: 1.02x slower                                                   |
| regex_dna                        | 99.6 ms                                                  | 102 ms: 1.02x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.07 ms: 1.03x slower                                                   |
| docutils                         | 1.02 sec                                                 | 1.06 sec: 1.03x slower                                                  |
| regex_v8                         | 9.59 ms                                                  | 9.90 ms: 1.03x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 437 us: 1.04x slower                                                    |
| fannkuch                         | 176 ms                                                   | 185 ms: 1.06x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 148 us: 1.06x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.51 ms: 1.06x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.09 ms: 1.07x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 51.0 ms: 1.07x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.7 us: 1.08x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.0 ms: 1.11x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 930 us: 1.12x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 26.4 ms: 1.15x slower                                                   |
| django_template                  | 13.6 ms                                                  | 15.6 ms: 1.15x slower                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 132 ms: 1.17x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.05 ms: 1.17x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 249 ms: 1.17x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 5.18 ms: 1.22x slower                                                   |
| coverage                         | 26.9 ms                                                  | 33.3 ms: 1.24x slower                                                   |
| many_optionals                   | 195 us                                                   | 250 us: 1.28x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 88.7 ms: 2.76x slower                                                   |
| logging_silent                   | 50.9 ns                                                  | 196 ns: 3.85x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.07x faster                                                            |

Benchmark hidden because not significant (3): tomli_loads, pycparser, unpickle_pure_python
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250509-3.15.0a0-98e2c3a/bm-20250509-macm4pro-arm64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.086x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.14x