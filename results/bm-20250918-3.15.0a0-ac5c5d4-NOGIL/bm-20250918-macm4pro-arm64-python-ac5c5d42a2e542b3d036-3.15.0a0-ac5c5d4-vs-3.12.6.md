# Results vs. 3.12.6

- fork: python
- ref: ac5c5d42a2e542b3d036
- machine: darwin-arm64
- commit hash: ac5c5d4
- commit date: 2025-09-18
- overall geometric mean: 1.091x faster
- HPT reliability: 97.79%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.25x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250918-macm4pro-arm64-python-ac5c5d42a2e542b3d036-3.15.0a0-ac5c5d4 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 122 ms: 1.07x slower                                                    |
| docutils       | 1.02 sec                                                 | 979 ms: 1.04x faster                                                    |
| html5lib       | 23.0 ms                                                  | 23.4 ms: 1.02x slower                                                   |
| sphinx         | 434 ms                                                   | 406 ms: 1.07x faster                                                    |
| Geometric mean | (ref)                                                    | 1.01x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250918-macm4pro-arm64-python-ac5c5d42a2e542b3d036-3.15.0a0-ac5c5d4 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 202 ms: 2.45x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 197 ms: 2.44x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 194 ms: 2.30x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 208 ms: 2.20x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 86.0 ms: 2.00x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 123 ms: 1.87x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 99.0 ms: 1.80x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 129 ms: 1.72x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 234 ms: 1.45x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 241 ms: 1.39x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.9 ms: 1.25x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.21x faster                                                    |
| async_generators                 | 206 ms                                                   | 181 ms: 1.14x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.04x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 111 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 225 ms: 1.06x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 48.7 ms: 1.07x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.5 ms: 2.41x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.38x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250918-macm4pro-arm64-python-ac5c5d42a2e542b3d036-3.15.0a0-ac5c5d4 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.7 ms: 1.27x faster                                                   |
| pidigits       | 161 ms                                                   | 160 ms: 1.01x faster                                                    |
| nbody          | 54.2 ms                                                  | 57.0 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                    | 1.07x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250918-macm4pro-arm64-python-ac5c5d42a2e542b3d036-3.15.0a0-ac5c5d4 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 95.1 ms: 1.05x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 53.0 ms: 1.03x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.31 ms: 1.03x faster                                                   |
| Geometric mean | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250918-macm4pro-arm64-python-ac5c5d42a2e542b3d036-3.15.0a0-ac5c5d4 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 37.6 ms: 1.37x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 57.1 ms: 1.19x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.92 ms: 1.09x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 37.0 ms: 1.05x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 26.9 ms: 1.01x slower                                                   |
| json_loads           | 10.9 us                                                  | 11.4 us: 1.05x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 151 us: 1.08x slower                                                    |
| unpickle_pure_python | 103 us                                                   | 112 us: 1.09x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.05x faster                                                            |

Benchmark hidden because not significant (1): tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250918-macm4pro-arm64-python-ac5c5d42a2e542b3d036-3.15.0a0-ac5c5d4 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.52 ms: 1.19x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.92 ms: 1.21x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.20x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250918-macm4pro-arm64-python-ac5c5d42a2e542b3d036-3.15.0a0-ac5c5d4 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 24.0 ms: 1.10x slower                                                   |
| genshi_text     | 10.5 ms                                                  | 11.6 ms: 1.11x slower                                                   |
| django_template | 13.6 ms                                                  | 16.5 ms: 1.21x slower                                                   |
| mako            | 4.77 ms                                                  | 5.84 ms: 1.22x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.16x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250918-macm4pro-arm64-python-ac5c5d42a2e542b3d036-3.15.0a0-ac5c5d4 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 759 us: 2.65x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 202 ms: 2.45x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 197 ms: 2.44x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 194 ms: 2.30x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 208 ms: 2.20x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 86.0 ms: 2.00x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 123 ms: 1.87x faster                                                    |
| mdp                              | 1.09 sec                                                 | 601 ms: 1.82x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 99.0 ms: 1.80x faster                                                   |
| create_gc_cycles                 | 830 us                                                   | 472 us: 1.76x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 129 ms: 1.72x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 234 ms: 1.45x faster                                                    |
| deepcopy                         | 161 us                                                   | 115 us: 1.40x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 241 ms: 1.39x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 13.2 us: 1.38x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 37.6 ms: 1.37x faster                                                   |
| float                            | 37.9 ms                                                  | 29.7 ms: 1.27x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.9 ms: 1.25x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.21x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 57.1 ms: 1.19x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 820 ns: 1.18x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.35 us: 1.18x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.5 ms: 1.17x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.26 us: 1.16x faster                                                   |
| generators                       | 21.9 ms                                                  | 19.1 ms: 1.15x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| async_generators                 | 206 ms                                                   | 181 ms: 1.14x faster                                                    |
| pylint                           | 128 ms                                                   | 113 ms: 1.14x faster                                                    |
| go                               | 70.0 ms                                                  | 61.7 ms: 1.14x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.7 ms: 1.13x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.98 sec: 1.13x faster                                                  |
| k_core                           | 1.12 sec                                                 | 992 ms: 1.13x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 45.3 ns: 1.12x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 55.1 ms: 1.11x faster                                                   |
| subparsers                       | 20.8 ms                                                  | 18.8 ms: 1.11x faster                                                   |
| raytrace                         | 145 ms                                                   | 133 ms: 1.09x faster                                                    |
| pyflate                          | 216 ms                                                   | 199 ms: 1.09x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.92 ms: 1.09x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.61 ms: 1.07x faster                                                   |
| sphinx                           | 434 ms                                                   | 406 ms: 1.07x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 51.4 ms: 1.06x faster                                                   |
| pycparser                        | 497 ms                                                   | 471 ms: 1.06x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.0 ms: 1.05x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 95.1 ms: 1.05x faster                                                   |
| docutils                         | 1.02 sec                                                 | 979 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.04x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 53.0 ms: 1.03x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.31 ms: 1.03x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.50 us: 1.03x faster                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 111 ms: 1.01x faster                                                    |
| pidigits                         | 161 ms                                                   | 160 ms: 1.01x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.79 us: 1.01x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.99 ms: 1.00x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 43.8 ms: 1.01x slower                                                   |
| xml_etree_process                | 26.7 ms                                                  | 26.9 ms: 1.01x slower                                                   |
| dask                             | 528 ms                                                   | 531 ms: 1.01x slower                                                    |
| chaos                            | 28.9 ms                                                  | 29.3 ms: 1.01x slower                                                   |
| json                             | 1.93 ms                                                  | 1.96 ms: 1.01x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 23.4 ms: 1.02x slower                                                   |
| hexiom                           | 3.04 ms                                                  | 3.14 ms: 1.03x slower                                                   |
| thrift                           | 322 us                                                   | 335 us: 1.04x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 74.3 us: 1.05x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.4 us: 1.05x slower                                                   |
| richards                         | 22.4 ms                                                  | 23.5 ms: 1.05x slower                                                   |
| nbody                            | 54.2 ms                                                  | 57.0 ms: 1.05x slower                                                   |
| richards_super                   | 25.4 ms                                                  | 26.8 ms: 1.05x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 42.0 ms: 1.06x slower                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 34.1 ms: 1.06x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 225 ms: 1.06x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 61.1 ms: 1.06x slower                                                   |
| fannkuch                         | 176 ms                                                   | 186 ms: 1.06x slower                                                    |
| sympy_str                        | 104 ms                                                   | 111 ms: 1.06x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 48.7 ms: 1.07x slower                                                   |
| 2to3                             | 114 ms                                                   | 122 ms: 1.07x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 352 ms: 1.07x slower                                                    |
| shortest_path                    | 219 ms                                                   | 235 ms: 1.07x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 716 ms: 1.08x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 151 us: 1.08x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 112 us: 1.09x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.28 ms: 1.10x slower                                                   |
| genshi_xml                       | 21.8 ms                                                  | 24.0 ms: 1.10x slower                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 43.0 ms: 1.11x slower                                                   |
| connected_components             | 201 ms                                                   | 222 ms: 1.11x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.6 ms: 1.11x slower                                                   |
| scimark_lu                       | 51.3 ms                                                  | 57.0 ms: 1.11x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 190 ms: 1.14x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.03 ms: 1.16x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 56.1 ms: 1.18x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.52 ms: 1.19x slower                                                   |
| django_template                  | 13.6 ms                                                  | 16.5 ms: 1.21x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.92 ms: 1.21x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.84 ms: 1.22x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 589 us: 1.41x slower                                                    |
| coverage                         | 26.9 ms                                                  | 40.1 ms: 1.49x slower                                                   |
| many_optionals                   | 195 us                                                   | 331 us: 1.69x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.5 ms: 2.41x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.09x faster                                                            |

Benchmark hidden because not significant (2): scimark_fft, tomli_loads
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250918-3.15.0a0-ac5c5d4-NOGIL/bm-20250918-macm4pro-arm64-python-ac5c5d42a2e542b3d036-3.15.0a0-ac5c5d4.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.091x faster

# HPT report

- Reliability score: 97.79% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.25x