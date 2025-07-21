# Results vs. 3.12.6

- fork: python
- ref: 246be21de1e2a51d757c
- machine: darwin-arm64
- commit hash: 246be21
- commit date: 2025-07-20
- overall geometric mean: 1.090x faster
- HPT reliability: 98.98%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.26x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250720-macm4pro-arm64-python-246be21de1e2a51d757c-3.15.0a0-246be21 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 121 ms: 1.06x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.01 sec: 1.02x faster                                                  |
| html5lib       | 23.0 ms                                                  | 23.6 ms: 1.02x slower                                                   |
| sphinx         | 434 ms                                                   | 410 ms: 1.06x faster                                                    |
| Geometric mean | (ref)                                                    | 1.00x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250720-macm4pro-arm64-python-246be21de1e2a51d757c-3.15.0a0-246be21 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 202 ms: 2.46x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 197 ms: 2.43x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 193 ms: 2.30x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 208 ms: 2.21x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 86.3 ms: 2.00x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.87x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 99.4 ms: 1.79x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 129 ms: 1.72x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 236 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 243 ms: 1.37x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.8 ms: 1.26x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.21x faster                                                    |
| async_generators                 | 206 ms                                                   | 182 ms: 1.14x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 48.0 ms: 1.05x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 228 ms: 1.07x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.6 ms: 2.41x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.38x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250720-macm4pro-arm64-python-246be21de1e2a51d757c-3.15.0a0-246be21 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.6 ms: 1.32x faster                                                   |
| pidigits       | 161 ms                                                   | 166 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                    | 1.09x faster                                                            |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250720-macm4pro-arm64-python-246be21de1e2a51d757c-3.15.0a0-246be21 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.49 ms: 1.12x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 51.9 ms: 1.05x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.42 ms: 1.02x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 98.5 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                    | 1.05x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250720-macm4pro-arm64-python-246be21de1e2a51d757c-3.15.0a0-246be21 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.2 ms: 1.35x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 57.1 ms: 1.19x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 36.5 ms: 1.07x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 26.5 ms: 1.01x faster                                                   |
| json_loads           | 10.9 us                                                  | 11.4 us: 1.05x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 110 us: 1.07x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 4.57 ms: 1.07x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 152 us: 1.09x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.03x faster                                                            |

Benchmark hidden because not significant (1): tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250720-macm4pro-arm64-python-246be21de1e2a51d757c-3.15.0a0-246be21 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.71 ms: 1.21x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 7.03 ms: 1.23x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.22x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250720-macm4pro-arm64-python-246be21de1e2a51d757c-3.15.0a0-246be21 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 23.4 ms: 1.08x slower                                                   |
| genshi_text     | 10.5 ms                                                  | 11.3 ms: 1.08x slower                                                   |
| mako            | 4.77 ms                                                  | 5.60 ms: 1.17x slower                                                   |
| django_template | 13.6 ms                                                  | 16.2 ms: 1.19x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.13x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250720-macm4pro-arm64-python-246be21de1e2a51d757c-3.15.0a0-246be21 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 787 us: 2.55x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 202 ms: 2.46x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 197 ms: 2.43x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 193 ms: 2.30x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 208 ms: 2.21x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 86.3 ms: 2.00x faster                                                   |
| mdp                              | 1.09 sec                                                 | 573 ms: 1.90x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.87x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 99.4 ms: 1.79x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 129 ms: 1.72x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 494 us: 1.68x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 236 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 243 ms: 1.37x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.2 ms: 1.35x faster                                                   |
| deepcopy                         | 161 us                                                   | 121 us: 1.34x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 13.7 us: 1.33x faster                                                   |
| float                            | 37.9 ms                                                  | 28.6 ms: 1.32x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.8 ms: 1.26x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.95 us: 1.24x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.21x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 57.1 ms: 1.19x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 815 ns: 1.19x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.23 us: 1.18x faster                                                   |
| go                               | 70.0 ms                                                  | 60.8 ms: 1.15x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.95 sec: 1.15x faster                                                  |
| subparsers                       | 20.8 ms                                                  | 18.1 ms: 1.15x faster                                                   |
| async_generators                 | 206 ms                                                   | 182 ms: 1.14x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.8 ms: 1.13x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 45.0 ns: 1.13x faster                                                   |
| generators                       | 21.9 ms                                                  | 19.4 ms: 1.13x faster                                                   |
| k_core                           | 1.12 sec                                                 | 989 ms: 1.13x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.49 ms: 1.12x faster                                                   |
| raytrace                         | 145 ms                                                   | 131 ms: 1.11x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 55.1 ms: 1.11x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 11.2 ms: 1.11x faster                                                   |
| pyflate                          | 216 ms                                                   | 197 ms: 1.10x faster                                                    |
| pylint                           | 128 ms                                                   | 118 ms: 1.08x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 36.5 ms: 1.07x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 51.2 ms: 1.06x faster                                                   |
| pycparser                        | 497 ms                                                   | 471 ms: 1.06x faster                                                    |
| sphinx                           | 434 ms                                                   | 410 ms: 1.06x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 51.9 ms: 1.05x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.65 ms: 1.04x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 42.1 ms: 1.03x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 139 ms: 1.02x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.42 ms: 1.02x faster                                                   |
| docutils                         | 1.02 sec                                                 | 1.01 sec: 1.02x faster                                                  |
| regex_dna                        | 99.6 ms                                                  | 98.5 ms: 1.01x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 26.5 ms: 1.01x faster                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 3.02 ms: 1.00x faster                                                   |
| fannkuch                         | 176 ms                                                   | 177 ms: 1.01x slower                                                    |
| dask                             | 528 ms                                                   | 532 ms: 1.01x slower                                                    |
| chaos                            | 28.9 ms                                                  | 29.3 ms: 1.01x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 23.6 ms: 1.02x slower                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 72.9 us: 1.03x slower                                                   |
| thrift                           | 322 us                                                   | 331 us: 1.03x slower                                                    |
| logging_format                   | 2.80 us                                                  | 2.88 us: 1.03x slower                                                   |
| pidigits                         | 161 ms                                                   | 166 ms: 1.03x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.5 ms: 1.04x slower                                                   |
| json                             | 1.93 ms                                                  | 2.01 ms: 1.04x slower                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 343 ms: 1.05x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 696 ms: 1.05x slower                                                    |
| sympy_str                        | 104 ms                                                   | 110 ms: 1.05x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 48.0 ms: 1.05x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.4 us: 1.05x slower                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.20 ms: 1.06x slower                                                   |
| sympy_sum                        | 57.6 ms                                                  | 61.1 ms: 1.06x slower                                                   |
| richards                         | 22.4 ms                                                  | 23.8 ms: 1.06x slower                                                   |
| 2to3                             | 114 ms                                                   | 121 ms: 1.06x slower                                                    |
| shortest_path                    | 219 ms                                                   | 233 ms: 1.07x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 27.1 ms: 1.07x slower                                                   |
| unpickle_pure_python             | 103 us                                                   | 110 us: 1.07x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 228 ms: 1.07x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 4.57 ms: 1.07x slower                                                   |
| genshi_xml                       | 21.8 ms                                                  | 23.4 ms: 1.08x slower                                                   |
| genshi_text                      | 10.5 ms                                                  | 11.3 ms: 1.08x slower                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 42.2 ms: 1.09x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 152 us: 1.09x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 56.3 ms: 1.10x slower                                                   |
| connected_components             | 201 ms                                                   | 222 ms: 1.11x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 187 ms: 1.12x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 45.1 ms: 1.14x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 55.2 ms: 1.16x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.60 ms: 1.17x slower                                                   |
| django_template                  | 13.6 ms                                                  | 16.2 ms: 1.19x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.71 ms: 1.21x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 7.03 ms: 1.23x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.23 ms: 1.24x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 599 us: 1.43x slower                                                    |
| coverage                         | 26.9 ms                                                  | 40.8 ms: 1.52x slower                                                   |
| many_optionals                   | 195 us                                                   | 331 us: 1.69x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.6 ms: 2.41x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                            |

Benchmark hidden because not significant (4): tomli_loads, logging_simple, sympy_integrate, nbody
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250720-3.15.0a0-246be21-NOGIL/bm-20250720-macm4pro-arm64-python-246be21de1e2a51d757c-3.15.0a0-246be21.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.090x faster

# HPT report

- Reliability score: 98.98% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.26x