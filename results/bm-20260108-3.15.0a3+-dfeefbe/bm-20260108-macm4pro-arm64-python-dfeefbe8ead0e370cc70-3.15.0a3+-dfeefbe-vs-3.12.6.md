# Results vs. 3.12.6

- fork: python
- ref: dfeefbe8ead0e370cc70
- machine: darwin-arm64
- commit hash: dfeefbe
- commit date: 2026-01-08
- overall geometric mean: 1.156x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260108-macm4pro-arm64-python-dfeefbe8ead0e370cc70-3.15.0a3+-dfeefbe |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 115 ms: 1.00x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                   |
| html5lib       | 23.0 ms                                                  | 22.0 ms: 1.05x faster                                                    |
| sphinx         | 434 ms                                                   | 400 ms: 1.08x faster                                                     |
| Geometric mean | (ref)                                                    | 1.03x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260108-macm4pro-arm64-python-dfeefbe8ead0e370cc70-3.15.0a3+-dfeefbe |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 226 ms: 2.20x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 226 ms: 2.12x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 222 ms: 2.01x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 236 ms: 1.94x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 104 ms: 1.72x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 101 ms: 1.71x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 137 ms: 1.69x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 140 ms: 1.59x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 257 ms: 1.32x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 253 ms: 1.32x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.5 ms: 1.29x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 107 ms: 1.23x faster                                                     |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 40.6 ms: 1.12x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 120 ms: 1.07x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 244 ms: 1.15x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 80.5 ms: 2.51x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.31x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260108-macm4pro-arm64-python-dfeefbe8ead0e370cc70-3.15.0a3+-dfeefbe |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.3 ms: 1.39x faster                                                    |
| nbody          | 54.2 ms                                                  | 45.4 ms: 1.19x faster                                                    |
| pidigits       | 161 ms                                                   | 168 ms: 1.04x slower                                                     |
| Geometric mean | (ref)                                                    | 1.17x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260108-macm4pro-arm64-python-dfeefbe8ead0e370cc70-3.15.0a3+-dfeefbe |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 45.3 ms: 1.21x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 97.5 ms: 1.02x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.73 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.09x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260108-macm4pro-arm64-python-dfeefbe8ead0e370cc70-3.15.0a3+-dfeefbe |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.7 ms: 1.30x faster                                                    |
| tomli_loads          | 957 ms                                                   | 840 ms: 1.14x faster                                                     |
| xml_etree_generate   | 38.9 ms                                                  | 34.5 ms: 1.13x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 24.4 ms: 1.10x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.90 ms: 1.09x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 97.1 us: 1.06x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 65.4 ms: 1.04x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 141 us: 1.01x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.09x faster                                                             |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260108-macm4pro-arm64-python-dfeefbe8ead0e370cc70-3.15.0a3+-dfeefbe |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.96 ms: 1.12x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.45 ms: 1.13x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.12x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260108-macm4pro-arm64-python-dfeefbe8ead0e370cc70-3.15.0a3+-dfeefbe |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.70 ms: 1.08x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 21.0 ms: 1.04x faster                                                    |
| mako            | 4.77 ms                                                  | 4.68 ms: 1.02x faster                                                    |
| django_template | 13.6 ms                                                  | 14.8 ms: 1.08x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.01x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260108-macm4pro-arm64-python-dfeefbe8ead0e370cc70-3.15.0a3+-dfeefbe |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.07 ms: 5.10x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 226 ms: 2.20x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 226 ms: 2.12x faster                                                     |
| mdp                              | 1.09 sec                                                 | 543 ms: 2.01x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 222 ms: 2.01x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 236 ms: 1.94x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 104 ms: 1.72x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 101 ms: 1.71x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 137 ms: 1.69x faster                                                     |
| deepcopy                         | 161 us                                                   | 98.4 us: 1.64x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 11.3 us: 1.63x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 140 ms: 1.59x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.05 us: 1.40x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.08 us: 1.39x faster                                                    |
| float                            | 37.9 ms                                                  | 27.3 ms: 1.39x faster                                                    |
| go                               | 70.0 ms                                                  | 52.7 ms: 1.33x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 257 ms: 1.32x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 253 ms: 1.32x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.7 ms: 1.30x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.5 ms: 1.29x faster                                                    |
| raytrace                         | 145 ms                                                   | 114 ms: 1.27x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 43.7 ms: 1.24x faster                                                    |
| k_core                           | 1.12 sec                                                 | 906 ms: 1.23x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 107 ms: 1.23x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 49.7 ms: 1.23x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 41.7 ns: 1.22x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 45.3 ms: 1.21x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 118 ms: 1.20x faster                                                     |
| nbody                            | 54.2 ms                                                  | 45.4 ms: 1.19x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 43.0 ms: 1.19x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.7 ms: 1.17x faster                                                    |
| pyflate                          | 216 ms                                                   | 185 ms: 1.17x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.47 ms: 1.17x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 27.6 ms: 1.17x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.78 ms: 1.16x faster                                                    |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                     |
| logging_simple                   | 2.57 us                                                  | 2.22 us: 1.16x faster                                                    |
| chaos                            | 28.9 ms                                                  | 24.9 ms: 1.16x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.44 us: 1.15x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.15x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 840 ms: 1.14x faster                                                     |
| nqueens                          | 43.5 ms                                                  | 38.5 ms: 1.13x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 62.9 us: 1.13x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.99 sec: 1.13x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 34.5 ms: 1.13x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 40.6 ms: 1.12x faster                                                    |
| richards                         | 22.4 ms                                                  | 20.1 ms: 1.12x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 22.7 ms: 1.12x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 19.2 ms: 1.11x faster                                                    |
| pylint                           | 128 ms                                                   | 116 ms: 1.11x faster                                                     |
| hexiom                           | 3.04 ms                                                  | 2.75 ms: 1.10x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 24.4 ms: 1.10x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.90 ms: 1.09x faster                                                    |
| sphinx                           | 434 ms                                                   | 400 ms: 1.08x faster                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 303 ms: 1.08x faster                                                     |
| genshi_text                      | 10.5 ms                                                  | 9.70 ms: 1.08x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 615 ms: 1.08x faster                                                     |
| pycparser                        | 497 ms                                                   | 465 ms: 1.07x faster                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 7.52 ms: 1.07x faster                                                    |
| thrift                           | 322 us                                                   | 303 us: 1.06x faster                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 36.6 ms: 1.06x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 97.1 us: 1.06x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 22.0 ms: 1.05x faster                                                    |
| sympy_str                        | 104 ms                                                   | 99.9 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 65.4 ms: 1.04x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 21.0 ms: 1.04x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 55.6 ms: 1.04x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 97.5 ms: 1.02x faster                                                    |
| mako                             | 4.77 ms                                                  | 4.68 ms: 1.02x faster                                                    |
| fannkuch                         | 176 ms                                                   | 174 ms: 1.01x faster                                                     |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| 2to3                             | 114 ms                                                   | 115 ms: 1.00x slower                                                     |
| pickle_pure_python               | 139 us                                                   | 141 us: 1.01x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 170 ms: 1.01x slower                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.73 ms: 1.02x slower                                                    |
| shortest_path                    | 219 ms                                                   | 222 ms: 1.02x slower                                                     |
| docutils                         | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                   |
| connected_components             | 201 ms                                                   | 206 ms: 1.03x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 431 us: 1.03x slower                                                     |
| pidigits                         | 161 ms                                                   | 168 ms: 1.04x slower                                                     |
| gc_traversal                     | 2.01 ms                                                  | 2.10 ms: 1.05x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 120 ms: 1.07x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 51.0 ms: 1.07x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.80 ms: 1.07x slower                                                    |
| django_template                  | 13.6 ms                                                  | 14.8 ms: 1.08x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.96 ms: 1.12x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.45 ms: 1.13x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 945 us: 1.14x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 244 ms: 1.15x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 45.8 ms: 1.15x slower                                                    |
| coverage                         | 26.9 ms                                                  | 31.6 ms: 1.17x slower                                                    |
| many_optionals                   | 195 us                                                   | 259 us: 1.33x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 80.5 ms: 2.51x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.15x faster                                                             |

Benchmark hidden because not significant (3): json, sqlite_synth, json_loads
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260108-3.15.0a3+-dfeefbe/bm-20260108-macm4pro-arm64-python-dfeefbe8ead0e370cc70-3.15.0a3+-dfeefbe.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.156x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.22x