# Results vs. 3.12.6

- fork: python
- ref: 4e00e2504fdcf06b5d55
- machine: darwin-arm64
- commit hash: 4e00e25
- commit date: 2025-09-16
- overall geometric mean: 1.091x faster
- HPT reliability: 97.71%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.26x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250916-macm4pro-arm64-python-4e00e2504fdcf06b5d55-3.15.0a0-4e00e25 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 123 ms: 1.08x slower                                                    |
| docutils       | 1.02 sec                                                 | 979 ms: 1.04x faster                                                    |
| html5lib       | 23.0 ms                                                  | 23.5 ms: 1.02x slower                                                   |
| sphinx         | 434 ms                                                   | 408 ms: 1.06x faster                                                    |
| Geometric mean | (ref)                                                    | 1.00x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250916-macm4pro-arm64-python-4e00e2504fdcf06b5d55-3.15.0a0-4e00e25 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 204 ms: 2.43x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 197 ms: 2.43x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 195 ms: 2.29x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 209 ms: 2.20x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 86.2 ms: 2.00x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 123 ms: 1.87x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 100 ms: 1.78x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.72x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 234 ms: 1.45x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 242 ms: 1.38x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.8 ms: 1.25x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.21x faster                                                    |
| async_generators                 | 206 ms                                                   | 183 ms: 1.13x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 226 ms: 1.06x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 48.8 ms: 1.07x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.4 ms: 2.41x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.38x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250916-macm4pro-arm64-python-4e00e2504fdcf06b5d55-3.15.0a0-4e00e25 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.1 ms: 1.30x faster                                                   |
| pidigits       | 161 ms                                                   | 160 ms: 1.01x faster                                                    |
| nbody          | 54.2 ms                                                  | 56.8 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                    | 1.08x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250916-macm4pro-arm64-python-4e00e2504fdcf06b5d55-3.15.0a0-4e00e25 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 95.3 ms: 1.04x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.22 ms: 1.04x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 53.0 ms: 1.03x faster                                                   |
| Geometric mean | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250916-macm4pro-arm64-python-4e00e2504fdcf06b5d55-3.15.0a0-4e00e25 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 37.5 ms: 1.38x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 56.6 ms: 1.20x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.93 ms: 1.08x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 36.6 ms: 1.06x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 26.7 ms: 1.00x faster                                                   |
| json_loads           | 10.9 us                                                  | 11.2 us: 1.03x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 111 us: 1.07x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 152 us: 1.09x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.05x faster                                                            |

Benchmark hidden because not significant (1): tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250916-macm4pro-arm64-python-4e00e2504fdcf06b5d55-3.15.0a0-4e00e25 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.47 ms: 1.18x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.89 ms: 1.21x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.19x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250916-macm4pro-arm64-python-4e00e2504fdcf06b5d55-3.15.0a0-4e00e25 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 11.6 ms: 1.11x slower                                                   |
| genshi_xml      | 21.8 ms                                                  | 24.3 ms: 1.12x slower                                                   |
| mako            | 4.77 ms                                                  | 5.73 ms: 1.20x slower                                                   |
| django_template | 13.6 ms                                                  | 16.6 ms: 1.22x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.16x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250916-macm4pro-arm64-python-4e00e2504fdcf06b5d55-3.15.0a0-4e00e25 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 752 us: 2.67x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 204 ms: 2.43x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 197 ms: 2.43x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 195 ms: 2.29x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 209 ms: 2.20x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 86.2 ms: 2.00x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 123 ms: 1.87x faster                                                    |
| mdp                              | 1.09 sec                                                 | 608 ms: 1.80x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 100 ms: 1.78x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 470 us: 1.76x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.72x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 234 ms: 1.45x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 13.1 us: 1.39x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 37.5 ms: 1.38x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 242 ms: 1.38x faster                                                    |
| deepcopy                         | 161 us                                                   | 118 us: 1.36x faster                                                    |
| float                            | 37.9 ms                                                  | 29.1 ms: 1.30x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.8 ms: 1.25x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.21x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 56.6 ms: 1.20x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.5 ms: 1.18x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 8.35 us: 1.18x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 825 ns: 1.17x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.27 us: 1.15x faster                                                   |
| go                               | 70.0 ms                                                  | 61.0 ms: 1.15x faster                                                   |
| generators                       | 21.9 ms                                                  | 19.2 ms: 1.15x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 44.5 ns: 1.14x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.7 ms: 1.13x faster                                                   |
| async_generators                 | 206 ms                                                   | 183 ms: 1.13x faster                                                    |
| k_core                           | 1.12 sec                                                 | 994 ms: 1.12x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.01 sec: 1.12x faster                                                  |
| raytrace                         | 145 ms                                                   | 131 ms: 1.11x faster                                                    |
| pylint                           | 128 ms                                                   | 117 ms: 1.10x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 19.0 ms: 1.09x faster                                                   |
| pyflate                          | 216 ms                                                   | 198 ms: 1.09x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.93 ms: 1.08x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 57.3 ms: 1.06x faster                                                   |
| sphinx                           | 434 ms                                                   | 408 ms: 1.06x faster                                                    |
| pycparser                        | 497 ms                                                   | 468 ms: 1.06x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 36.6 ms: 1.06x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.63 ms: 1.06x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 95.3 ms: 1.04x faster                                                   |
| docutils                         | 1.02 sec                                                 | 979 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 52.2 ms: 1.04x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.22 ms: 1.04x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.49 us: 1.03x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 53.0 ms: 1.03x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.77 us: 1.01x faster                                                   |
| pidigits                         | 161 ms                                                   | 160 ms: 1.01x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 26.7 ms: 1.00x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 44.0 ms: 1.01x slower                                                   |
| chaos                            | 28.9 ms                                                  | 29.3 ms: 1.01x slower                                                   |
| json                             | 1.93 ms                                                  | 1.96 ms: 1.01x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 23.5 ms: 1.02x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.2 us: 1.03x slower                                                   |
| hexiom                           | 3.04 ms                                                  | 3.15 ms: 1.04x slower                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 73.7 us: 1.04x slower                                                   |
| fannkuch                         | 176 ms                                                   | 183 ms: 1.04x slower                                                    |
| thrift                           | 322 us                                                   | 335 us: 1.04x slower                                                    |
| richards                         | 22.4 ms                                                  | 23.4 ms: 1.04x slower                                                   |
| nbody                            | 54.2 ms                                                  | 56.8 ms: 1.05x slower                                                   |
| richards_super                   | 25.4 ms                                                  | 26.7 ms: 1.05x slower                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.9 ms: 1.05x slower                                                   |
| sympy_sum                        | 57.6 ms                                                  | 60.9 ms: 1.06x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 226 ms: 1.06x slower                                                    |
| sympy_str                        | 104 ms                                                   | 111 ms: 1.06x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 350 ms: 1.07x slower                                                    |
| shortest_path                    | 219 ms                                                   | 234 ms: 1.07x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 42.5 ms: 1.07x slower                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 48.8 ms: 1.07x slower                                                   |
| unpickle_pure_python             | 103 us                                                   | 111 us: 1.07x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 715 ms: 1.07x slower                                                    |
| 2to3                             | 114 ms                                                   | 123 ms: 1.08x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 152 us: 1.09x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 55.9 ms: 1.09x slower                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 42.5 ms: 1.09x slower                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.28 ms: 1.10x slower                                                   |
| genshi_text                      | 10.5 ms                                                  | 11.6 ms: 1.11x slower                                                   |
| connected_components             | 201 ms                                                   | 224 ms: 1.11x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 24.3 ms: 1.12x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 190 ms: 1.14x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.99 ms: 1.14x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.47 ms: 1.18x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 56.6 ms: 1.19x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.73 ms: 1.20x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.89 ms: 1.21x slower                                                   |
| django_template                  | 13.6 ms                                                  | 16.6 ms: 1.22x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 580 us: 1.39x slower                                                    |
| coverage                         | 26.9 ms                                                  | 40.0 ms: 1.49x slower                                                   |
| many_optionals                   | 195 us                                                   | 338 us: 1.73x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.4 ms: 2.41x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.09x faster                                                            |

Benchmark hidden because not significant (4): sympy_integrate, scimark_fft, dask, tomli_loads
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250916-3.15.0a0-4e00e25-NOGIL/bm-20250916-macm4pro-arm64-python-4e00e2504fdcf06b5d55-3.15.0a0-4e00e25.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.091x faster

# HPT report

- Reliability score: 97.71% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.26x