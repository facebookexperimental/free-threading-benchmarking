# Results vs. 3.12.6

- fork: python
- ref: bde12919522b0c40fd9e
- machine: darwin-arm64
- commit hash: bde1291
- commit date: 2025-09-05
- overall geometric mean: 1.087x faster
- HPT reliability: 97.30%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.25x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250905-macm4pro-arm64-python-bde12919522b0c40fd9e-3.15.0a0-bde1291 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 124 ms: 1.09x slower                                                    |
| docutils       | 1.02 sec                                                 | 982 ms: 1.04x faster                                                    |
| html5lib       | 23.0 ms                                                  | 23.5 ms: 1.02x slower                                                   |
| sphinx         | 434 ms                                                   | 406 ms: 1.07x faster                                                    |
| Geometric mean | (ref)                                                    | 1.00x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250905-macm4pro-arm64-python-bde12919522b0c40fd9e-3.15.0a0-bde1291 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 204 ms: 2.43x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 198 ms: 2.42x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 195 ms: 2.28x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 210 ms: 2.18x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 86.7 ms: 1.99x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.86x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.77x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.71x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 236 ms: 1.44x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 243 ms: 1.37x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 11.0 ms: 1.23x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| async_generators                 | 206 ms                                                   | 183 ms: 1.13x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 227 ms: 1.07x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 48.8 ms: 1.07x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.1 ms: 2.43x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.37x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250905-macm4pro-arm64-python-bde12919522b0c40fd9e-3.15.0a0-bde1291 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.7 ms: 1.27x faster                                                   |
| nbody          | 54.2 ms                                                  | 57.2 ms: 1.06x slower                                                   |
| Geometric mean | (ref)                                                    | 1.06x faster                                                            |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250905-macm4pro-arm64-python-bde12919522b0c40fd9e-3.15.0a0-bde1291 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 95.2 ms: 1.05x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 52.9 ms: 1.03x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.31 ms: 1.03x faster                                                   |
| Geometric mean | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250905-macm4pro-arm64-python-bde12919522b0c40fd9e-3.15.0a0-bde1291 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.7 ms: 1.33x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 60.2 ms: 1.13x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.99 ms: 1.07x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 36.8 ms: 1.06x faster                                                   |
| tomli_loads          | 957 ms                                                   | 965 ms: 1.01x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.3 us: 1.04x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 112 us: 1.09x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 152 us: 1.09x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.04x faster                                                            |

Benchmark hidden because not significant (1): xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250905-macm4pro-arm64-python-bde12919522b0c40fd9e-3.15.0a0-bde1291 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.49 ms: 1.18x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.89 ms: 1.21x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.20x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250905-macm4pro-arm64-python-bde12919522b0c40fd9e-3.15.0a0-bde1291 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 24.3 ms: 1.12x slower                                                   |
| genshi_text     | 10.5 ms                                                  | 11.8 ms: 1.12x slower                                                   |
| mako            | 4.77 ms                                                  | 5.76 ms: 1.21x slower                                                   |
| django_template | 13.6 ms                                                  | 16.6 ms: 1.22x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.16x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250905-macm4pro-arm64-python-bde12919522b0c40fd9e-3.15.0a0-bde1291 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 758 us: 2.65x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 204 ms: 2.43x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 198 ms: 2.42x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 195 ms: 2.28x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 210 ms: 2.18x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 86.7 ms: 1.99x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.86x faster                                                    |
| mdp                              | 1.09 sec                                                 | 602 ms: 1.81x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.77x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 472 us: 1.76x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.71x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 236 ms: 1.44x faster                                                    |
| deepcopy                         | 161 us                                                   | 116 us: 1.39x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 13.2 us: 1.39x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 243 ms: 1.37x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.7 ms: 1.33x faster                                                   |
| float                            | 37.9 ms                                                  | 29.7 ms: 1.27x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 11.0 ms: 1.23x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 824 ns: 1.17x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.42 us: 1.17x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.26 us: 1.16x faster                                                   |
| generators                       | 21.9 ms                                                  | 19.0 ms: 1.15x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.7 ms: 1.13x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.13x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 60.2 ms: 1.13x faster                                                   |
| k_core                           | 1.12 sec                                                 | 991 ms: 1.13x faster                                                    |
| go                               | 70.0 ms                                                  | 62.1 ms: 1.13x faster                                                   |
| async_generators                 | 206 ms                                                   | 183 ms: 1.13x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.99 sec: 1.13x faster                                                  |
| subparsers                       | 20.8 ms                                                  | 18.5 ms: 1.13x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 45.5 ns: 1.12x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 55.3 ms: 1.10x faster                                                   |
| pylint                           | 128 ms                                                   | 117 ms: 1.09x faster                                                    |
| raytrace                         | 145 ms                                                   | 133 ms: 1.09x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 50.3 ms: 1.08x faster                                                   |
| pyflate                          | 216 ms                                                   | 200 ms: 1.08x faster                                                    |
| sphinx                           | 434 ms                                                   | 406 ms: 1.07x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.99 ms: 1.07x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 36.8 ms: 1.06x faster                                                   |
| pycparser                        | 497 ms                                                   | 471 ms: 1.06x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.64 ms: 1.05x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 95.2 ms: 1.05x faster                                                   |
| docutils                         | 1.02 sec                                                 | 982 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.03x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 52.9 ms: 1.03x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.49 us: 1.03x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.31 ms: 1.03x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.78 us: 1.01x faster                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 965 ms: 1.01x slower                                                    |
| nqueens                          | 43.5 ms                                                  | 44.0 ms: 1.01x slower                                                   |
| chaos                            | 28.9 ms                                                  | 29.5 ms: 1.02x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 23.5 ms: 1.02x slower                                                   |
| hexiom                           | 3.04 ms                                                  | 3.13 ms: 1.03x slower                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 73.4 us: 1.03x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.3 us: 1.04x slower                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 341 ms: 1.04x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 694 ms: 1.04x slower                                                    |
| thrift                           | 322 us                                                   | 336 us: 1.04x slower                                                    |
| richards                         | 22.4 ms                                                  | 23.4 ms: 1.04x slower                                                   |
| richards_super                   | 25.4 ms                                                  | 26.8 ms: 1.05x slower                                                   |
| nbody                            | 54.2 ms                                                  | 57.2 ms: 1.06x slower                                                   |
| sympy_sum                        | 57.6 ms                                                  | 61.1 ms: 1.06x slower                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 34.2 ms: 1.06x slower                                                   |
| fannkuch                         | 176 ms                                                   | 187 ms: 1.07x slower                                                    |
| sympy_str                        | 104 ms                                                   | 111 ms: 1.07x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 227 ms: 1.07x slower                                                    |
| shortest_path                    | 219 ms                                                   | 234 ms: 1.07x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 48.8 ms: 1.07x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 42.7 ms: 1.07x slower                                                   |
| unpickle_pure_python             | 103 us                                                   | 112 us: 1.09x slower                                                    |
| 2to3                             | 114 ms                                                   | 124 ms: 1.09x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 152 us: 1.09x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 56.1 ms: 1.09x slower                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 42.8 ms: 1.10x slower                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.29 ms: 1.10x slower                                                   |
| connected_components             | 201 ms                                                   | 223 ms: 1.11x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 24.3 ms: 1.12x slower                                                   |
| genshi_text                      | 10.5 ms                                                  | 11.8 ms: 1.12x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 190 ms: 1.14x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.99 ms: 1.15x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 56.2 ms: 1.18x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.49 ms: 1.18x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.76 ms: 1.21x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.89 ms: 1.21x slower                                                   |
| django_template                  | 13.6 ms                                                  | 16.6 ms: 1.22x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 591 us: 1.41x slower                                                    |
| coverage                         | 26.9 ms                                                  | 39.9 ms: 1.49x slower                                                   |
| many_optionals                   | 195 us                                                   | 334 us: 1.71x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.1 ms: 2.43x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                            |

Benchmark hidden because not significant (6): dask, scimark_fft, sympy_integrate, pidigits, xml_etree_process, json
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250905-3.15.0a0-bde1291-NOGIL/bm-20250905-macm4pro-arm64-python-bde12919522b0c40fd9e-3.15.0a0-bde1291.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.087x faster

# HPT report

- Reliability score: 97.30% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.25x