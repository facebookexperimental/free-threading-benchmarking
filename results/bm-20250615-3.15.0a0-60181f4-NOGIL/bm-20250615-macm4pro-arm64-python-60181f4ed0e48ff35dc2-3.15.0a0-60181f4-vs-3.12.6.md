# Results vs. 3.12.6

- fork: python
- ref: 60181f4ed0e48ff35dc2
- machine: darwin-arm64
- commit hash: 60181f4
- commit date: 2025-06-15
- overall geometric mean: 1.087x faster
- HPT reliability: 95.11%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.27x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250615-macm4pro-arm64-python-60181f4ed0e48ff35dc2-3.15.0a0-60181f4 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 122 ms: 1.07x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.00 sec: 1.02x faster                                                  |
| html5lib       | 23.0 ms                                                  | 23.5 ms: 1.02x slower                                                   |
| sphinx         | 434 ms                                                   | 421 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                    | 1.01x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250615-macm4pro-arm64-python-60181f4ed0e48ff35dc2-3.15.0a0-60181f4 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 206 ms: 2.41x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 199 ms: 2.41x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 196 ms: 2.28x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 211 ms: 2.18x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 87.6 ms: 1.96x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 125 ms: 1.85x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.75x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 131 ms: 1.70x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 237 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 245 ms: 1.36x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.31x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.19x faster                                                    |
| async_generators                 | 206 ms                                                   | 182 ms: 1.13x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 228 ms: 1.07x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 49.5 ms: 1.09x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.5 ms: 2.44x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.37x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250615-macm4pro-arm64-python-60181f4ed0e48ff35dc2-3.15.0a0-60181f4 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.1 ms: 1.30x faster                                                   |
| pidigits       | 161 ms                                                   | 167 ms: 1.03x slower                                                    |
| nbody          | 54.2 ms                                                  | 56.9 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250615-macm4pro-arm64-python-60181f4ed0e48ff35dc2-3.15.0a0-60181f4 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.47 ms: 1.14x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.24 ms: 1.04x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 53.5 ms: 1.02x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 98.0 ms: 1.02x faster                                                   |
| Geometric mean | (ref)                                                    | 1.05x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250615-macm4pro-arm64-python-60181f4ed0e48ff35dc2-3.15.0a0-60181f4 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.4 ms: 1.34x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 57.9 ms: 1.17x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 37.1 ms: 1.05x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 27.3 ms: 1.02x slower                                                   |
| tomli_loads          | 957 ms                                                   | 1.00 sec: 1.04x slower                                                  |
| json_loads           | 10.9 us                                                  | 11.5 us: 1.06x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 111 us: 1.08x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 4.66 ms: 1.09x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 155 us: 1.11x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.01x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250615-macm4pro-arm64-python-60181f4ed0e48ff35dc2-3.15.0a0-60181f4 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.58 ms: 1.19x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.96 ms: 1.22x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.21x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250615-macm4pro-arm64-python-60181f4ed0e48ff35dc2-3.15.0a0-60181f4 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 11.3 ms: 1.08x slower                                                   |
| genshi_xml      | 21.8 ms                                                  | 23.7 ms: 1.09x slower                                                   |
| mako            | 4.77 ms                                                  | 5.71 ms: 1.20x slower                                                   |
| django_template | 13.6 ms                                                  | 16.6 ms: 1.22x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.14x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250615-macm4pro-arm64-python-60181f4ed0e48ff35dc2-3.15.0a0-60181f4 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 800 us: 2.51x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 206 ms: 2.41x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 199 ms: 2.41x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 196 ms: 2.28x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 211 ms: 2.18x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 9.71 ms: 2.14x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 87.6 ms: 1.96x faster                                                   |
| mdp                              | 1.09 sec                                                 | 569 ms: 1.92x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 125 ms: 1.85x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.75x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 131 ms: 1.70x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 494 us: 1.68x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 237 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 245 ms: 1.36x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.4 ms: 1.34x faster                                                   |
| deepcopy                         | 161 us                                                   | 122 us: 1.33x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.31x faster                                                   |
| deepcopy_memo                    | 18.3 us                                                  | 14.0 us: 1.31x faster                                                   |
| float                            | 37.9 ms                                                  | 29.1 ms: 1.30x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.95 us: 1.24x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.19x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 57.9 ms: 1.17x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 826 ns: 1.17x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.26 us: 1.16x faster                                                   |
| generators                       | 21.9 ms                                                  | 19.0 ms: 1.16x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.47 ms: 1.14x faster                                                   |
| go                               | 70.0 ms                                                  | 61.6 ms: 1.14x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.97 sec: 1.13x faster                                                  |
| k_core                           | 1.12 sec                                                 | 986 ms: 1.13x faster                                                    |
| async_generators                 | 206 ms                                                   | 182 ms: 1.13x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.9 ms: 1.13x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 55.0 ms: 1.11x faster                                                   |
| raytrace                         | 145 ms                                                   | 131 ms: 1.10x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.2 ms: 1.10x faster                                                   |
| pyflate                          | 216 ms                                                   | 198 ms: 1.09x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 50.3 ms: 1.08x faster                                                   |
| pylint                           | 128 ms                                                   | 119 ms: 1.08x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 41.2 ms: 1.05x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 37.1 ms: 1.05x faster                                                   |
| pycparser                        | 497 ms                                                   | 478 ms: 1.04x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.24 ms: 1.04x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                    |
| sphinx                           | 434 ms                                                   | 421 ms: 1.03x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.68 ms: 1.03x faster                                                   |
| docutils                         | 1.02 sec                                                 | 1.00 sec: 1.02x faster                                                  |
| regex_compile                    | 54.6 ms                                                  | 53.5 ms: 1.02x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 98.0 ms: 1.02x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 140 ms: 1.01x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.06 ms: 1.00x slower                                                   |
| dask                             | 528 ms                                                   | 532 ms: 1.01x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.07 ms: 1.01x slower                                                   |
| chaos                            | 28.9 ms                                                  | 29.5 ms: 1.02x slower                                                   |
| xml_etree_process                | 26.7 ms                                                  | 27.3 ms: 1.02x slower                                                   |
| thrift                           | 322 us                                                   | 329 us: 1.02x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 23.5 ms: 1.02x slower                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 72.7 us: 1.02x slower                                                   |
| fannkuch                         | 176 ms                                                   | 181 ms: 1.03x slower                                                    |
| pidigits                         | 161 ms                                                   | 167 ms: 1.03x slower                                                    |
| json                             | 1.93 ms                                                  | 2.01 ms: 1.04x slower                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.5 ms: 1.04x slower                                                   |
| tomli_loads                      | 957 ms                                                   | 1.00 sec: 1.04x slower                                                  |
| nbody                            | 54.2 ms                                                  | 56.9 ms: 1.05x slower                                                   |
| sympy_str                        | 104 ms                                                   | 109 ms: 1.05x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.5 us: 1.06x slower                                                   |
| shortest_path                    | 219 ms                                                   | 233 ms: 1.06x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 61.2 ms: 1.06x slower                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.22 ms: 1.07x slower                                                   |
| 2to3                             | 114 ms                                                   | 122 ms: 1.07x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 228 ms: 1.07x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.3 ms: 1.08x slower                                                   |
| unpickle_pure_python             | 103 us                                                   | 111 us: 1.08x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 49.5 ms: 1.09x slower                                                   |
| richards                         | 22.4 ms                                                  | 24.4 ms: 1.09x slower                                                   |
| genshi_xml                       | 21.8 ms                                                  | 23.7 ms: 1.09x slower                                                   |
| json_dumps                       | 4.26 ms                                                  | 4.66 ms: 1.09x slower                                                   |
| richards_super                   | 25.4 ms                                                  | 27.8 ms: 1.09x slower                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 42.7 ms: 1.10x slower                                                   |
| connected_components             | 201 ms                                                   | 221 ms: 1.10x slower                                                    |
| logging_simple                   | 2.57 us                                                  | 2.84 us: 1.10x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 155 us: 1.11x slower                                                    |
| logging_format                   | 2.80 us                                                  | 3.13 us: 1.12x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.6 ms: 1.12x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 189 ms: 1.13x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 54.3 ms: 1.14x slower                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 379 ms: 1.16x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 771 ms: 1.16x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.58 ms: 1.19x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.71 ms: 1.20x slower                                                   |
| django_template                  | 13.6 ms                                                  | 16.6 ms: 1.22x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.96 ms: 1.22x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.23 ms: 1.24x slower                                                   |
| scimark_lu                       | 51.3 ms                                                  | 65.8 ms: 1.28x slower                                                   |
| many_optionals                   | 195 us                                                   | 253 us: 1.30x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 595 us: 1.42x slower                                                    |
| coverage                         | 26.9 ms                                                  | 40.8 ms: 1.52x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.5 ms: 2.44x slower                                                   |
| logging_silent                   | 50.9 ns                                                  | 215 ns: 4.23x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.06x faster                                                            |
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250615-3.15.0a0-60181f4-NOGIL/bm-20250615-macm4pro-arm64-python-60181f4ed0e48ff35dc2-3.15.0a0-60181f4.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.087x faster

# HPT report

- Reliability score: 95.11% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.27x