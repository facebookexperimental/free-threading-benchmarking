# Results vs. 3.12.6

- fork: python
- ref: 98e2c3af4794d6c6ebe4
- machine: darwin-arm64
- commit hash: 98e2c3a
- commit date: 2025-05-09
- overall geometric mean: 1.082x faster
- HPT reliability: 93.64%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.27x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250509-macm4pro-arm64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 122 ms: 1.07x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                  |
| html5lib       | 23.0 ms                                                  | 25.8 ms: 1.12x slower                                                   |
| sphinx         | 434 ms                                                   | 424 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                    | 1.04x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250509-macm4pro-arm64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 197 ms: 2.44x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 204 ms: 2.43x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 194 ms: 2.30x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 210 ms: 2.19x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 86.7 ms: 1.99x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.86x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.76x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 131 ms: 1.70x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 235 ms: 1.44x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 243 ms: 1.37x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.0 ms: 1.35x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                    |
| async_generators                 | 206 ms                                                   | 179 ms: 1.15x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 228 ms: 1.07x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 49.9 ms: 1.10x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.9 ms: 2.42x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.38x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250509-macm4pro-arm64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.3 ms: 1.34x faster                                                   |
| pidigits       | 161 ms                                                   | 162 ms: 1.01x slower                                                    |
| nbody          | 54.2 ms                                                  | 56.6 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                    | 1.08x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250509-macm4pro-arm64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.50 ms: 1.11x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.31 ms: 1.03x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 98.2 ms: 1.01x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 54.1 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                    | 1.04x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250509-macm4pro-arm64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 37.8 ms: 1.37x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 55.8 ms: 1.22x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 38.2 ms: 1.02x faster                                                   |
| tomli_loads          | 957 ms                                                   | 990 ms: 1.03x slower                                                    |
| xml_etree_process    | 26.7 ms                                                  | 27.8 ms: 1.04x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 111 us: 1.08x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 153 us: 1.10x slower                                                    |
| json_loads           | 10.9 us                                                  | 12.6 us: 1.16x slower                                                   |
| json_dumps           | 4.26 ms                                                  | 5.43 ms: 1.27x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.01x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250509-macm4pro-arm64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.45 ms: 1.18x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.87 ms: 1.20x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.19x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250509-macm4pro-arm64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 23.7 ms: 1.09x slower                                                   |
| genshi_text     | 10.5 ms                                                  | 11.6 ms: 1.11x slower                                                   |
| mako            | 4.77 ms                                                  | 5.64 ms: 1.18x slower                                                   |
| django_template | 13.6 ms                                                  | 17.1 ms: 1.26x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.16x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250509-macm4pro-arm64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 780 us: 2.57x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 197 ms: 2.44x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 204 ms: 2.43x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 194 ms: 2.30x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 210 ms: 2.19x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 9.56 ms: 2.17x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 86.7 ms: 1.99x faster                                                   |
| mdp                              | 1.09 sec                                                 | 582 ms: 1.87x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.86x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.76x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 482 us: 1.72x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 131 ms: 1.70x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 235 ms: 1.44x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 243 ms: 1.37x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 37.8 ms: 1.37x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.0 ms: 1.35x faster                                                   |
| float                            | 37.9 ms                                                  | 28.3 ms: 1.34x faster                                                   |
| deepcopy_memo                    | 18.3 us                                                  | 14.3 us: 1.28x faster                                                   |
| deepcopy                         | 161 us                                                   | 127 us: 1.27x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 55.8 ms: 1.22x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.7 ms: 1.17x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 825 ns: 1.17x faster                                                    |
| async_generators                 | 206 ms                                                   | 179 ms: 1.15x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.28 us: 1.14x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.99 sec: 1.13x faster                                                  |
| k_core                           | 1.12 sec                                                 | 998 ms: 1.12x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 19.0 ms: 1.12x faster                                                   |
| go                               | 70.0 ms                                                  | 63.0 ms: 1.11x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.50 ms: 1.11x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 8.90 us: 1.11x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 11.3 ms: 1.10x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 55.8 ms: 1.09x faster                                                   |
| raytrace                         | 145 ms                                                   | 133 ms: 1.09x faster                                                    |
| pyflate                          | 216 ms                                                   | 201 ms: 1.07x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.61 ms: 1.07x faster                                                   |
| pylint                           | 128 ms                                                   | 120 ms: 1.07x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 41.5 ms: 1.05x faster                                                   |
| pycparser                        | 497 ms                                                   | 476 ms: 1.04x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 52.5 ms: 1.04x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.31 ms: 1.03x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                    |
| sphinx                           | 434 ms                                                   | 424 ms: 1.02x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 38.2 ms: 1.02x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 98.2 ms: 1.01x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 54.1 ms: 1.01x faster                                                   |
| docutils                         | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                  |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                    |
| pidigits                         | 161 ms                                                   | 162 ms: 1.01x slower                                                    |
| scimark_fft                      | 142 ms                                                   | 144 ms: 1.01x slower                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.14 ms: 1.01x slower                                                   |
| chaos                            | 28.9 ms                                                  | 29.5 ms: 1.02x slower                                                   |
| tomli_loads                      | 957 ms                                                   | 990 ms: 1.03x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.15 ms: 1.04x slower                                                   |
| xml_etree_process                | 26.7 ms                                                  | 27.8 ms: 1.04x slower                                                   |
| nbody                            | 54.2 ms                                                  | 56.6 ms: 1.04x slower                                                   |
| thrift                           | 322 us                                                   | 336 us: 1.04x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.17 ms: 1.05x slower                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.8 ms: 1.05x slower                                                   |
| fannkuch                         | 176 ms                                                   | 185 ms: 1.05x slower                                                    |
| shortest_path                    | 219 ms                                                   | 232 ms: 1.06x slower                                                    |
| 2to3                             | 114 ms                                                   | 122 ms: 1.07x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 61.5 ms: 1.07x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 228 ms: 1.07x slower                                                    |
| json                             | 1.93 ms                                                  | 2.08 ms: 1.07x slower                                                   |
| richards                         | 22.4 ms                                                  | 24.1 ms: 1.08x slower                                                   |
| unpickle_pure_python             | 103 us                                                   | 111 us: 1.08x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 76.5 us: 1.08x slower                                                   |
| sympy_str                        | 104 ms                                                   | 112 ms: 1.08x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 27.5 ms: 1.08x slower                                                   |
| genshi_xml                       | 21.8 ms                                                  | 23.7 ms: 1.09x slower                                                   |
| connected_components             | 201 ms                                                   | 219 ms: 1.09x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 49.9 ms: 1.10x slower                                                   |
| pprint_pformat                   | 665 ms                                                   | 729 ms: 1.10x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 153 us: 1.10x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 361 ms: 1.10x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 42.9 ms: 1.10x slower                                                   |
| genshi_text                      | 10.5 ms                                                  | 11.6 ms: 1.11x slower                                                   |
| logging_simple                   | 2.57 us                                                  | 2.85 us: 1.11x slower                                                   |
| logging_format                   | 2.80 us                                                  | 3.13 us: 1.11x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 25.8 ms: 1.12x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.7 ms: 1.13x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 192 ms: 1.15x slower                                                    |
| json_loads                       | 10.9 us                                                  | 12.6 us: 1.16x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 55.5 ms: 1.16x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.45 ms: 1.18x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.64 ms: 1.18x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.87 ms: 1.20x slower                                                   |
| django_template                  | 13.6 ms                                                  | 17.1 ms: 1.26x slower                                                   |
| scimark_lu                       | 51.3 ms                                                  | 64.7 ms: 1.26x slower                                                   |
| json_dumps                       | 4.26 ms                                                  | 5.43 ms: 1.27x slower                                                   |
| many_optionals                   | 195 us                                                   | 252 us: 1.29x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.37 ms: 1.29x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 597 us: 1.43x slower                                                    |
| coverage                         | 26.9 ms                                                  | 40.6 ms: 1.51x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.9 ms: 2.42x slower                                                   |
| logging_silent                   | 50.9 ns                                                  | 215 ns: 4.22x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.06x faster                                                            |
Ignored benchmarks (11) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250509-3.15.0a0-98e2c3a-NOGIL/bm-20250509-macm4pro-arm64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.082x faster

# HPT report

- Reliability score: 93.64% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.27x